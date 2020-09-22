---
title: iOS ve Android cihazlarda Microsoft Dynamics 365 Project Timesheet mobil uygulaması için özel alanlar uygulama
description: Bu konuda, özel alanları uygulamak üzere uzantıları kullanmak için yaygın kalıplar sağlanır.
author: KimANelson
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: 4564bbda-34ea-4647-a9bc-f6ef17b1038b
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 16c3b79dcaaf8c5c491587618256694f82f44753
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756596"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="dc3ec-103">iOS ve Android cihazlarda Microsoft Dynamics 365 Project Timesheet mobil uygulaması için özel alanlar uygulama</span><span class="sxs-lookup"><span data-stu-id="dc3ec-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dc3ec-104">Bu konuda, özel alanları uygulamak üzere uzantıları kullanmak için yaygın kalıplar sağlanır.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="dc3ec-105">Aşağıdaki konular ele alınmıştır:</span><span class="sxs-lookup"><span data-stu-id="dc3ec-105">The following topics are covered:</span></span>

- <span data-ttu-id="dc3ec-106">Özel alan çerçevesinin desteklediği çeşitli veri türleri</span><span class="sxs-lookup"><span data-stu-id="dc3ec-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="dc3ec-107">Zaman çizelgesi girişlerinde salt okunur veya düzenlenebilir alanları gösterme ve kullanıcı tarafından sağlanan değerleri veritabanına yeniden kaydetme</span><span class="sxs-lookup"><span data-stu-id="dc3ec-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="dc3ec-108">Zaman çizelgesi üstbilgisindeki salt okunur alanlar nasıl gösterilir</span><span class="sxs-lookup"><span data-stu-id="dc3ec-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="dc3ec-109">Diğer özel iş mantığı, alanlara varsayılan değerler girmek için nasıl tümleştirilir ve ek doğrulama yapılır</span><span class="sxs-lookup"><span data-stu-id="dc3ec-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="dc3ec-110">Hedef Kitle</span><span class="sxs-lookup"><span data-stu-id="dc3ec-110">Audience</span></span>

<span data-ttu-id="dc3ec-111">Bu konu, Apple iOS ve Google Android cihazlarda kullanılabilen Microsoft Dynamics 365 Project Timesheet mobil uygulamasıyla özel alanlarını tümleştiren geliştiriciler içindir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="dc3ec-112">Okuyucuların X++ geliştirme ve proje zaman çizelgesi işlevleriyle ilgili bilgi sahibi olduğu varsayılmıştır.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="dc3ec-113">Veri sözleşmesi – TSTimesheetCustomField X + + sınıfı</span><span class="sxs-lookup"><span data-stu-id="dc3ec-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="dc3ec-114">**TSTimesheetCustomField** sınıfı, zaman çizelgesi işlevselliği için özel bir alanla ilgili bilgileri temsil eden X++ veri sözleşmesi sınıfıdır.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="dc3ec-115">Özel alan nesnelerinin listeleri, mobil uygulamadaki özel alanları göstermek için hem TSTimesheetDetails veri sözleşmesine hem de TSTimesheetEntry veri sözleşmesine aktarılır.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="dc3ec-116">**TSTimesheetDetails**: zaman çizelgesi başlığı sözleşmesi.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="dc3ec-117">**TSTimesheetEntry**: zaman çizelgesi hareket sözleşmesi.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="dc3ec-118">Aynı proje bilgilerine ve **timesheetLineRecId** değerine sahip olan bu nesnelerin grupları bir satır oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="dc3ec-119">fieldBaseType (Türler)</span><span class="sxs-lookup"><span data-stu-id="dc3ec-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="dc3ec-120">**TsTimesheetCustom** nesnesindeki **FieldBaseType** özelliği, uygulamada görünen alanın türünü belirler.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="dc3ec-121">Aşağıdaki **Türler** değerleri desteklenir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="dc3ec-122">Türler değeri</span><span class="sxs-lookup"><span data-stu-id="dc3ec-122">Types value</span></span> | <span data-ttu-id="dc3ec-123">Tür</span><span class="sxs-lookup"><span data-stu-id="dc3ec-123">Type</span></span>              | <span data-ttu-id="dc3ec-124">Notlar</span><span class="sxs-lookup"><span data-stu-id="dc3ec-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="dc3ec-125">0</span><span class="sxs-lookup"><span data-stu-id="dc3ec-125">0</span></span>           | <span data-ttu-id="dc3ec-126">Dize (ve Enum)</span><span class="sxs-lookup"><span data-stu-id="dc3ec-126">String (and Enum)</span></span> | <span data-ttu-id="dc3ec-127">Alan, bir metin alanı olarak görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="dc3ec-128">1</span><span class="sxs-lookup"><span data-stu-id="dc3ec-128">1</span></span>           | <span data-ttu-id="dc3ec-129">Integer</span><span class="sxs-lookup"><span data-stu-id="dc3ec-129">Integer</span></span>           | <span data-ttu-id="dc3ec-130">Değer, ondalık basamak olmayan bir sayı olarak gösterilir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="dc3ec-131">2</span><span class="sxs-lookup"><span data-stu-id="dc3ec-131">2</span></span>           | <span data-ttu-id="dc3ec-132">Gerçek sayı</span><span class="sxs-lookup"><span data-stu-id="dc3ec-132">Real</span></span>              | <span data-ttu-id="dc3ec-133">Değer, ondalık basamağı olan bir sayı olarak gösterilir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="dc3ec-134">Gerçek değeri uygulamada bir para birimi olarak göstermek için, **fieldExtenededType** özelliğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="dc3ec-135">Gösterilen ondalık basamak sayısını ayarlamak için **numberOfDecimals** özelliğini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="dc3ec-136">3</span><span class="sxs-lookup"><span data-stu-id="dc3ec-136">3</span></span>           | <span data-ttu-id="dc3ec-137">Tarih</span><span class="sxs-lookup"><span data-stu-id="dc3ec-137">Date</span></span>              | <span data-ttu-id="dc3ec-138">Tarih biçimleri, **Kullanıcı seçenekleri** bölümünde **Dil ve ülke/bölge tercihi** altında belirtilen kullanıcının **Tarih, zaman ve sayı biçimi** ayarından belirlenir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="dc3ec-139">4</span><span class="sxs-lookup"><span data-stu-id="dc3ec-139">4</span></span>           | <span data-ttu-id="dc3ec-140">Boolean</span><span class="sxs-lookup"><span data-stu-id="dc3ec-140">Boolean</span></span>           | |
| <span data-ttu-id="dc3ec-141">15</span><span class="sxs-lookup"><span data-stu-id="dc3ec-141">15</span></span>          | <span data-ttu-id="dc3ec-142">GUID</span><span class="sxs-lookup"><span data-stu-id="dc3ec-142">GUID</span></span>              | |
| <span data-ttu-id="dc3ec-143">16</span><span class="sxs-lookup"><span data-stu-id="dc3ec-143">16</span></span>          | <span data-ttu-id="dc3ec-144">Int64</span><span class="sxs-lookup"><span data-stu-id="dc3ec-144">Int64</span></span>             | |

- <span data-ttu-id="dc3ec-145">**TSTimesheetCustomField** nesnesinde **stringOptions** özelliği verilmemişse, kullanıcıya serbest metin alanı sağlanır.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="dc3ec-146">**stringLength** özelliği, kullanıcıların girebileceği en fazla dize uzunluğunu ayarlamak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="dc3ec-147">**TSTimesheetCustomField** nesnesinde **stringOptions** özelliği verilmişse, kullanıcıların seçenek düğmelerini (radyo düğmeleri) kullanarak seçim yapmasına yönelik değerler yalnızca bu liste öğelerinden oluşur.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="dc3ec-148">Bu durumda, dize alanı kullanıcı giriş yapmasına yönelik bir Enum değeri olarak işlev görebilir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="dc3ec-149">Değeri veritabanına enum olarak kaydetmek için, komut zincirini kullanarak veritabanına kaydetmeden önce dize değerini el ile enum değerine tekrar eşleştirin. (Örnek için bu konu içinde ilerleyen bölümlerde yer alan "Uygulamadan zaman çizelgesi girişini yeniden veritabanına kaydetmek için TSTimesheetEntryService sınıfında komut zincirini kullanma" bölümüne bakın.)</span><span class="sxs-lookup"><span data-stu-id="dc3ec-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="dc3ec-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="dc3ec-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="dc3ec-151">Bu özelliği, gerçek değerleri para birimi olarak biçimlendirmek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="dc3ec-152">Bu yaklaşım yalnızca **fieldBaseType** değeri **Gerçek** olduğunda uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="dc3ec-153">**TSCustomFieldExtendedType:None**: Hiçbir biçimlendirme uygulanmaz.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="dc3ec-154">**TSCustomFieldExtendedType::Para birimi**: Değeri para birimi olarak biçimlendirir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="dc3ec-155">Para birimi olarak biçimlendirme etkin olduğunda, **stringValue** alanı, uygulamada gösterilmesi gereken para birimi kodunu aktarmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="dc3ec-156">Salt okunur bir değerdir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-156">The value is a read-only value.</span></span>

    <span data-ttu-id="dc3ec-157">**realValue** alanı, veritabanına kaydedilmesi gereken para tutarını içerir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="dc3ec-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="dc3ec-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="dc3ec-159">Özel alanın uygulamada nerede görüntüleneceğini belirtmek için bu özelliği kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="dc3ec-160">**TsccustomFieldSection::Başlık**: Alan, uygulamada **Daha fazla ayrıntı görüntüle** bölümünde gösterilir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="dc3ec-161">Bu alanlar her zaman salt okunurdur.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-161">These fields are always read-only.</span></span>
- <span data-ttu-id="dc3ec-162">**TSCustomFieldSection::Satır**: Alan, zaman çizelgesi girişlerindeki tüm hazır satır alanlarından sonra görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="dc3ec-163">Bu alanlar düzenlenebilir ya da salt okunur olabilir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="dc3ec-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="dc3ec-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="dc3ec-165">Bu özellik, uygulamanın sağladığı değerlerin veritabanına tekrar ne zaman kaydedileceğini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="dc3ec-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="dc3ec-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="dc3ec-167">Bu özellik, uygulamanın sağladığı değerlerin veritabanına tekrar ne zaman kaydedileceğini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="dc3ec-168">isEditable (NoYes)</span><span class="sxs-lookup"><span data-stu-id="dc3ec-168">isEditable (NoYes)</span></span>

<span data-ttu-id="dc3ec-169">Zaman çizelgesi girişi bölümündeki alanının kullanıcılar tarafından düzenlenebilir olması gerektiğini belirtmek için bu özelliği **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="dc3ec-170">Alanı salt okunur yapmak için, özelliğini **Hayır** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="dc3ec-171">isMandatory (NoYes)</span><span class="sxs-lookup"><span data-stu-id="dc3ec-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="dc3ec-172">Zaman çizelgesi girişi bölümündeki alanının zorunlu olması gerektiğini belirtmek için bu özelliği **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="dc3ec-173">label (str)</span><span class="sxs-lookup"><span data-stu-id="dc3ec-173">label (str)</span></span>

<span data-ttu-id="dc3ec-174">Bu özellik, uygulamadaki alanların yanında gösterilen etiketi belirtir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="dc3ec-175">stringOptions (Dize Listesi)</span><span class="sxs-lookup"><span data-stu-id="dc3ec-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="dc3ec-176">Bu özellik yalnızca **fieldBaseType** alanı **String** olarak ayarlandığında uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="dc3ec-177">**stringOptions** ayarlanmışsa, seçenek düğmeleri (radyo düğmeleri) aracılığıyla seçim için kullanılacak dize değerler listedeki dizeler ile belirtilir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="dc3ec-178">Herhangi bir dize verilmezse, dize alanında serbest metin girdisine izin verilir. (Örnek için bu konu içinde ilerleyen bölümlerde yer alan "Uygulamadan zaman çizelgesi girişini yeniden veritabanına kaydetmek için TSTimesheetEntryService sınıfında komut zincirini kullanma" bölümüne bakın.)</span><span class="sxs-lookup"><span data-stu-id="dc3ec-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="dc3ec-179">stringLength (int)</span><span class="sxs-lookup"><span data-stu-id="dc3ec-179">stringLength (int)</span></span>

<span data-ttu-id="dc3ec-180">Bu özellik bir dize alanındaki en fazla uzunluğu belirtir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="dc3ec-181">Yalnızca **fieldBaseType** alanı **String** olarak ayarlandığında uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="dc3ec-182">numberOfDecimals (int)</span><span class="sxs-lookup"><span data-stu-id="dc3ec-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="dc3ec-183">Bu özellik, gerçek bir alan için gösterilen ondalık basamak sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="dc3ec-184">Yalnızca **fieldBaseType** alanı **Gerçek** olarak ayarlandığında uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="dc3ec-185">orderSequence (int)</span><span class="sxs-lookup"><span data-stu-id="dc3ec-185">orderSequence (int)</span></span>

<span data-ttu-id="dc3ec-186">Bu özellik birden çok özel alan belirtildiğinde, özel alanların uygulamada gösterilme sırasını denetler.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="dc3ec-187">Daha küçük sayılar içeren alanlar önce gösterilir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="dc3ec-188">booleanValue (boolean)</span><span class="sxs-lookup"><span data-stu-id="dc3ec-188">booleanValue (boolean)</span></span>

<span data-ttu-id="dc3ec-189">Bu özellik, **Boolean** türündeki alanlar için, alanın Boolean değerini sunucu ile uygulama arasında iletir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="dc3ec-190">guidValue (guid)</span><span class="sxs-lookup"><span data-stu-id="dc3ec-190">guidValue (guid)</span></span>

<span data-ttu-id="dc3ec-191">Bu özellik, **GUID** türündeki alanlar için, alanın genel benzersiz tanımlayıcı (GUID) değerini sunucu ile uygulama arasında iletir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="dc3ec-192">int64Value (int64)</span><span class="sxs-lookup"><span data-stu-id="dc3ec-192">int64Value (int64)</span></span>

<span data-ttu-id="dc3ec-193">Bu özellik, **Int64** türündeki alanlar için, alanın int64 değerini sunucu ile uygulama arasında iletir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="dc3ec-194">intValue (int)</span><span class="sxs-lookup"><span data-stu-id="dc3ec-194">intValue (int)</span></span>

<span data-ttu-id="dc3ec-195">Bu özellik, **Int** türündeki alanlar için, alanın int değerini sunucu ile uygulama arasında iletir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="dc3ec-196">realValue (real)</span><span class="sxs-lookup"><span data-stu-id="dc3ec-196">realValue (real)</span></span>

<span data-ttu-id="dc3ec-197">Bu özellik, **Gerçek** türündeki alanlar için, alanın gerçek sayı değerini sunucu ile uygulama arasında iletir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="dc3ec-198">stringValue (str)</span><span class="sxs-lookup"><span data-stu-id="dc3ec-198">stringValue (str)</span></span>

<span data-ttu-id="dc3ec-199">Bu özellik, **Dize** türündeki alanlar için, alanın dize değerini sunucu ile uygulama arasında iletir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="dc3ec-200">Ayrıca, para birimi olarak biçimlendirilmiş **Gerçek** alanları için de kullanılır.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="dc3ec-201">Bu alanlar için, söz konusu özellik para birimi kodunu uygulamaya iletmek amacıyla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="dc3ec-202">dateValue (date)</span><span class="sxs-lookup"><span data-stu-id="dc3ec-202">dateValue (date)</span></span>

<span data-ttu-id="dc3ec-203">Bu özellik, **Tarih** türündeki alanlar için, alanın tarih değerini sunucu ile uygulama arasında iletir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="dc3ec-204">Zaman çizelgesi girişi bölümünde özel alan gösterme ve kaydetme</span><span class="sxs-lookup"><span data-stu-id="dc3ec-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="dc3ec-205">Aşağıda, bir zaman çizelgesi girişi oluşturma sırasında mobil uygulamadan alınan bir ekran görüntüsü yer alınır.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="dc3ec-206">"Zaman girişi" bölümündeki kullanıma hazır alanlar ile daha önceden ayarlanmış "Second option" enum değerine sahip "Test string" adlı özel bir alan gösterilir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![Uygulamadaki Test string özel alanı](media/timesheet-entry.jpg)



<span data-ttu-id="dc3ec-208">Aşağıdaki ekran görüntüsü, "Test string" özel alanı için verilen enum seçeneklerinden birini belirleyen kullanıcının mobil uygulamasından alınmıştır.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="dc3ec-209">Bu iki seçenek, radyo düğmeleri olarak gösterilen "First option" ve "Second option" seçenekleridir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="dc3ec-210">İkinci seçenek seçilidir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-210">The second option is currently selected.</span></span>

![Test string özel alanı için seçenek düğmeleri (radyo düğmeleri)](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="dc3ec-212">Özel bir alanı olması için TSTimeheetLine tablosunu genişletme</span><span class="sxs-lookup"><span data-stu-id="dc3ec-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="dc3ec-213">Tipik senaryolarda, zaman çizelgesi girişi bölümündeki özel alana ait veriler TSTimesheetLine tablosuna kaydedilebilir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="dc3ec-214">Ancak, veriler sağlanan bir TSTimesheetTrans kaydına bağlı olarak getirildiğinde veya belirli bir kayıt bağlamına sahip değilse (örneğin, alan proje parametrelerinde salt okunur olarak ayarlandıysa), diğer tablolar kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="dc3ec-215">Özel alanların veritabanı kayıtlarının yedeğinin alınmasının zorunlu olmadığını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="dc3ec-216">Bunlar X++ mantığına bağlı olarak dinamik şekilde oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="dc3ec-217">Bu yaklaşım, salt okunur senaryolarda yararlı olabilir. (Dinamik olarak üretilen özel alan değerleri ile ilgili örnek için "Zaman çizelgesi ayrıntılarını doldurmak için TSTimesheetDetails sınıfı, buildCustomFieldListForHeader yönteminde komut zincirini kullanma" bölümüne bakın.)</span><span class="sxs-lookup"><span data-stu-id="dc3ec-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="dc3ec-218">Aşağıdaki ekran görüntüsü Uygulama Nesne Ağacı'nın Visual Studio öğesine aittir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="dc3ec-219">Özel alan olarak eklenmiş TestLineString alanı bulunan TSTimesheetLine tablosunun bir uzantısını gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![Satır dizesi](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="dc3ec-221">Zaman çizelgesi girişi bölümünde bir alan göstermek için TSTimesheetSettings sınıfının buildCustomFieldList yönteminde komut zinciri kullanma</span><span class="sxs-lookup"><span data-stu-id="dc3ec-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="dc3ec-222">Bu kod, uygulamadaki alanla ilgili görüntü ayarlarını denetler.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="dc3ec-223">Örneğin, alan türünü, etiketi, alanın zorunlu olup olmadığını ve alanın hangi bölümünde görüntüleneceğini denetler.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="dc3ec-224">Aşağıdaki örnekte zaman girişlerinde bir dize alanı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="dc3ec-225">Bu alanda, seçenek düğmeleri (radyo düğmeleri) aracılığıyla kullanılabilen **First option** ve **Second option** olan iki seçenek bulunur.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-225">This field has two options, **First option** and **Second option**, that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="dc3ec-226">Uygulamadaki alan, TSTimesheetLine tablosuna eklenen **TestLineString** alanıyla ilişkilidir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="dc3ec-227">Özel alan özelliklerinin başlatılmasını kolaylaştıracak **TSTimesheetCustomField::newFromMetatdata()** yönteminin kullanımına dikkat edin: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** ve **numberOfDecimals**.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength**, and **numberOfDecimals**.</span></span> <span data-ttu-id="dc3ec-228">Ayrıca, bu parametreleri dilerseniz el ile de ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-228">You can also set these parameters manually, as you prefer.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="dc3ec-229">Zaman çizelgesi girişine değer girmek için TSTimesheetEntry sınıfının buildCustomFieldListForEntry yönteminde komut zinciri kullanma</span><span class="sxs-lookup"><span data-stu-id="dc3ec-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="dc3ec-230">**buildCustomFieldListForEntry** yöntemi, mobil uygulamadaki kaydedilmiş zaman çizelgesi satırlarına değer girmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="dc3ec-231">Parametre olarak bir TSTimesheetTrans kaydı alır.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="dc3ec-232">Bu kayıttaki alanlar, uygulamadaki özel alan değerini doldurmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="dc3ec-233">Uygulamadan zaman çizelgesi girişini yeniden veritabanına kaydetmek için TSTimesheetEntryService sınıfında komut zincirini kullanma</span><span class="sxs-lookup"><span data-stu-id="dc3ec-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="dc3ec-234">Tipik kullanımda özel alanı veritabanına tekrar kaydetmek için, birden çok yöntem genişletmeniz gerekir:</span><span class="sxs-lookup"><span data-stu-id="dc3ec-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="dc3ec-235">**timesheetLineNeedsUpdating** yöntemi, satır kaydının uygulamadaki kullanıcı tarafından değiştirilip değiştirilmediğini ve veritabanına kaydedilmesi gerekip gerekmediğini belirlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="dc3ec-236">Performans sorun değilse, bu yöntem basitleştirilebilir. Böylece her zaman **doğru** sonucu döner.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="dc3ec-237">**populateTimesheetLineFromEntryDuringCreate** ve **populateTimesheetLineFromEntryDuringUpdate** yöntemleri, sağlanan TSTimesheetEntry veri sözleşmesi kaydından TSTimesheetLine veritabanı kaydına değer girilmesi için genişletilebilir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="dc3ec-238">Aşağıdaki örnekte, veritabanı alanıyla giriş alanı arasındaki eşlemenin X++ kodu aracılığıyla el ile nasıl yapıldığı konusunda dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="dc3ec-239">**populateTimesheetWeekFromEntry** yöntemi, **TSTimesheetEntry** nesnesiyle eşlenen özel alanın TSTimesheetLineweek veritabanı tablosuna yeniden yazması için de genişletilebilir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="dc3ec-240">Aşağıdaki örnekte, kullanıcının seçtiği **firstOption** veya **secondOption** değeri veritabanına ham dize değeri olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="dc3ec-241">Veritabanı alanı **Enum** türünde bir alan ise, bu değerler el ile bir enum değerine eşleştirilebilir ve sonra veritabanı tablosundaki bir enum alanına kaydedilebilir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="dc3ec-242">Zaman çizelgesi başlık bölümünde özel alan gösterme</span><span class="sxs-lookup"><span data-stu-id="dc3ec-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="dc3ec-243">Aşağıda; mobil uygulamadan alınan, zaman çizelgesini görüntüleyen bir kullanıcıya ait bir ekran görüntüsü yer alınır.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="dc3ec-244">"Daha fazla ayrıntı görüntüle" seçeneğini göstermek için, sağ üst köşedeki "Daha fazla bilgi" düğmesi seçilmiştir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![Daha fazla ayrıntı görüntüle komutu](media/show-more.png)

<span data-ttu-id="dc3ec-246">Aşağıda; zaman çizelgesindeki "Daha fazla" bölümünün gösterildiği mobil uygulamadan alınan bir ekran görüntüsü yer alınır.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="dc3ec-247">"Utilization rate of this timesheet (computed custom field)" adlı özel alan, zaman çizelgesi başlığı bölümüne eklendi.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="dc3ec-248">Özel alanda salt okunur olan "0,667" değeri ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-248">A read-only value of "0.667" is set on the custom field.</span></span>

![Daha fazla bölümü](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="dc3ec-250">Özel bir alanı olması için TSTimesheetTable tablosunu genişletme</span><span class="sxs-lookup"><span data-stu-id="dc3ec-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="dc3ec-251">Tipik senaryolarda, başlık bölümündeki özel alana ait veriler TSTimesheetHeader tablosundan çekilebilir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="dc3ec-252">Ancak, veriler sağlanan bir TSTimesheetTable kaydına bağlı olarak getirildiğinde veya belirli bir kayıt bağlamına sahip değilse (örneğin, alan proje parametrelerinde salt okunur olarak ayarlandıysa), diğer tablolar kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="dc3ec-253">Özel alanların veritabanı kayıtlarının yedeğinin alınmasının zorunlu olmadığını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="dc3ec-254">Bunlar X++ mantığına bağlı olarak dinamik şekilde oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="dc3ec-255">Aşağıdaki örnek bu yaklaşımı gösterir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="dc3ec-256">Başlık bölümündeki alanlar uygulamada her zaman salt okunurdur.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="dc3ec-257">Başlık bölümünde bir alan göstermek için TSTimesheetSettings sınıfının buildCustomFieldList yönteminde komut zincirini kullanma</span><span class="sxs-lookup"><span data-stu-id="dc3ec-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="dc3ec-258">Bu kod, uygulamadaki alanla ilgili görüntü ayarlarını denetler.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="dc3ec-259">Örneğin, alan türünü, etiketi, alanın zorunlu olup olmadığını ve alanın hangi bölümünde görüntüleneceğini denetler.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="dc3ec-260">Aşağıdaki örnekte, uygulamadaki başlık bölümünde hesaplanan bir değer gösterilir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-260">The following example shows a computed value in the header section in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="dc3ec-261">Zaman çizelgesi ayrıntılarını doldurmak için TSTimesheetEntry sınıfının buildCustomFieldListForEntry yönteminde komut zincirini kullanma</span><span class="sxs-lookup"><span data-stu-id="dc3ec-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="dc3ec-262">**buildCustomFieldListForHeader** yöntemi, mobil uygulamadaki zaman çizelgesi başlık ayrıntılarını doldurmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="dc3ec-263">Parametre olarak bir TSTimesheetTable kaydı alır.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="dc3ec-264">Bu kayıttaki alanlar, uygulamadaki özel alan değerini doldurmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="dc3ec-265">Aşağıdaki örnekte, veritabanından değer okunmaz.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="dc3ec-266">Bunun yerine, uygulamada gösterilen hesaplanan bir değer oluşturmak için X++ mantığını kullanır.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="dc3ec-267">Diğer yapılandırılabilirlik/genişletilebilirlik fırsatları</span><span class="sxs-lookup"><span data-stu-id="dc3ec-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="dc3ec-268">Uygulama için ek doğrulama ekleme</span><span class="sxs-lookup"><span data-stu-id="dc3ec-268">Adding additional validation for the app</span></span>

<span data-ttu-id="dc3ec-269">Veritabanı düzeyindeki zaman çizelgesi işlevselliği için var olan mantık, beklendiği gibi çalışmaya devam eder.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="dc3ec-270">Kaydetme veya gönderme işlemlerinin tamamlanmasını kesmek ve belirli bir hata iletisini göstermek için komut zinciri uzantısı aracılığıyla koda **hata oluştu ("kullanıcıya ileti")** iletisi ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="dc3ec-271">Yararlı genişletilebilir yöntemlerle ilgili üç örnek:</span><span class="sxs-lookup"><span data-stu-id="dc3ec-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="dc3ec-272">Bir zaman çizelgesi satırı için kaydetme işlemi sırasında TSTimesheetLine tablosunda **validatewrite** **false** değerini döndürürse, mobil uygulamada bir hata iletisi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="dc3ec-273">Bir zaman çizelgesi satırı için gönderme işlemi sırasında TSTimesheetTable tablosunda **validateSubmit** **false** değerini döndürürse, kullanıcıya hata iletisi gösterilir.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="dc3ec-274">**insert** yöntemi sırasında, TSTimesheetLine tablosundaki alanları (örneğin, **Satır Özelliği**) dolduran mantık çalışmaya devam eder.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-274">Logic that fills in fields (for example, **Line Property**) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="dc3ec-275">Kullanıma hazır alanları yapılandırma aracılığıyla salt okunur olarak gizleme ve işaretleme</span><span class="sxs-lookup"><span data-stu-id="dc3ec-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="dc3ec-276">Proje parametrelerinden, kullanıma hazır alanları mobil uygulamada salt okunur veya gizli yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="dc3ec-277">**Proje yönetimi ve muhasebe parametreleri** sayfasının **Zaman çizelgesi** sekmesindeki **Mobil zaman çizelgeleri** bölümünden seçenekleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![Proje parametreleri](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="dc3ec-279">Uzantılar aracılığıyla seçim için verilen etkinlikleri değiştirme</span><span class="sxs-lookup"><span data-stu-id="dc3ec-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="dc3ec-280">Bir projede seçim için verilen etkinlikler, **TsTimesheetProjectService** sınıfındaki **getActivitiesForProject()** ve **getActivityQuery()** yöntemleriyle doldurulur.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="dc3ec-281">Belirli bir projede seçim için verilen etkinlikler için bu davranışı iş senaryosuyla eşleşecek şekilde değiştirmek üzere komut zincirini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="dc3ec-282">Zaman çizelgesi girişlerine varsayılan proje kategorisi girme</span><span class="sxs-lookup"><span data-stu-id="dc3ec-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="dc3ec-283">Zaman çizelgesi girişlerinde varsayılan proje kategorisi girişi üç düzeyde oluşur.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="dc3ec-284">İstediğiniz davranışı elde etmek için bu düzeylerin herhangi birinin veya tümünün davranışını uzatmak amacıyla komut zincirini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="dc3ec-285">Aşağıdaki hiyerarşi kullanılır:</span><span class="sxs-lookup"><span data-stu-id="dc3ec-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="dc3ec-286">Uygulama, proje kaynağından varsayılan kategoriyi yerleştirmeye çalışır.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="dc3ec-287">Bu varsayılan kategori, **TSTimesheetSettingsService** sınıfındaki **getCurrentUserResource** ve **getDelegatedResourcesForCurrentUser** yöntemlerinde ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="dc3ec-288">Proje kaynak düzeyinde varsayılan kategori sağlanmamışsa, uygulama proje etkinliğinden almaya çalışır.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="dc3ec-289">Bu varsayılan kategori, **TSTimesheetProjectService** sınıfındaki **getActivitiesForProject** yönteminde ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="dc3ec-290">Proje etkinlik düzeyinde varsayılan kategori sağlanmamışsa, varsayılan kategori proje parametrelerinden alınır.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="dc3ec-291">Bu varsayılan kategori, **TSTimesheetProjectService** sınıfındaki **getProjectDetailsbyRule** yönteminde ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="dc3ec-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>
