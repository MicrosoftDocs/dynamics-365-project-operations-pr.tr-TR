---
title: Özel alanlar ve varlıklar oluşturma
description: Bu konu, Power Apps platformunda kendi çözümünüzde seçenek kümeleri ve varlıklar oluşturmayı açıklamaktadır.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756701"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="f6d9a-103">Özel alanlar ve varlıklar oluşturma</span><span class="sxs-lookup"><span data-stu-id="f6d9a-103">Create custom fields and entities</span></span> 

<span data-ttu-id="f6d9a-104">Power Apps platformunda özel bir seçenek kümesi veya varlık oluşturmak istediğinizde aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="f6d9a-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="f6d9a-105">Bu konudaki yordamlar Project Service Automation'ın (PSA) web arabirimi kullanılarak tamamlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f6d9a-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f6d9a-106">Tüm özel fiyatlandırma boyutu değişikliklerini ayrı bir çözümde yapmanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="f6d9a-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="f6d9a-107">Bu önemli en iyi uygulama, gelecekte değişiklikleri güncelleştirmek veya kaldırmak için esneklik sağlar, işinizi yeniden kullanmanıza yardımcı olur ve bu değişiklikleri başka bir kuruluma aktarmayı kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="f6d9a-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="f6d9a-108">Gerekli tüm değişiklikleri yaptıktan sonra, bu çözümü bir **Yönetilen çözüm** olarak dışa aktarın ve fiyatlandırma ayarını yeniden kullanmak için diğer kurulumlara aktarın.</span><span class="sxs-lookup"><span data-stu-id="f6d9a-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="f6d9a-109">Fiyatlandırma boyutları için özel bir çözüm oluşturma</span><span class="sxs-lookup"><span data-stu-id="f6d9a-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="f6d9a-110">PSA'da, **Ayarlar** > **Çözümler**'e tıklayın ve ardından yeni bir çözüm oluşturmak için **Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f6d9a-110">In PSA, click **Settings** > **Solutions**, and then click **New** to create a new solution.</span></span> 
2. <span data-ttu-id="f6d9a-111">Çözümü, **\<kuruluş adınız > fiyatlandırma boyutları** şeklinde adlandırın, kalan gerekli bilgileri girin ve ardından **Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f6d9a-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then click **Save**.</span></span>

> ![Fiyatlandırma boyutları için özel bir çözüm oluşturma](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="f6d9a-113">Fiyatlandırma boyutu çözümünde özel alanlar ve seçenek kümeleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="f6d9a-113">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="f6d9a-114">Bir fiyatlandırma boyutu bir seçenek kümesi veya varlık olabilir.</span><span class="sxs-lookup"><span data-stu-id="f6d9a-114">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="f6d9a-115">Her ikisinin de fiyatlandırma çözümünüz içinde oluşturulması gerekir.</span><span class="sxs-lookup"><span data-stu-id="f6d9a-115">Both must be created in your pricing solution.</span></span> <span data-ttu-id="f6d9a-116">Bu yordamdaki adımlarda varlık tabanlı boyutların ve seçenek kümesi tabanlı boyutların nasıl oluşturulacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="f6d9a-116">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="f6d9a-117">Varlık tabanlı boyutlar</span><span class="sxs-lookup"><span data-stu-id="f6d9a-117">Entity-based dimensions</span></span>

1. <span data-ttu-id="f6d9a-118">PSA'da, **Ayarlar** > **Çözümler**'e tıklayın ve ardından **\<kuruluşunuzun adı > fiyatlandırma boyutları**'na çift tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f6d9a-118">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="f6d9a-119">Çözüm Gezgininde, sol gezinti bölmesinde **Varlıkları**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f6d9a-119">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="f6d9a-120">**Standart Başlık** adlı yeni bir varlık oluşturmak için **Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f6d9a-120">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="f6d9a-121">Kalan gerekli bilgileri girin ve ardından **Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f6d9a-121">Enter the remaining required information, and then click **Save**.</span></span>

> ![Standart başlık varlığı tanımı](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="f6d9a-123">Seçenek kümesi tabanlı boyutlar</span><span class="sxs-lookup"><span data-stu-id="f6d9a-123">Option set-based dimensions</span></span> 
<span data-ttu-id="f6d9a-124">İki seçenek kümesi tabanlı boyut oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f6d9a-124">You can create two option set-based dimensions.</span></span> <span data-ttu-id="f6d9a-125">**Ana** konum çalışması ve **Yerinde** çalışma fiyatını izlemek için **Kaynak Çalışma Konumu**'nu ve iş tamamlandığında kar payı uygulamak için **Normal** ve **Fazla Mesai** değerleriyle **Kaynak Çalışma saatleri**'ni kullanın.</span><span class="sxs-lookup"><span data-stu-id="f6d9a-125">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="f6d9a-126">PSA'da, **Ayarlar** > **Çözümler**'e tıklayın ve ardından **\<kuruluşunuzun adı > fiyatlandırma boyutları**'na çift tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f6d9a-126">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="f6d9a-127">Çözüm Gezgininde, sol gezinti bölmesinde **Seçenek Kümeleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="f6d9a-127">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="f6d9a-128">Yeni seçenek kümesi oluşturmak için **Yeni**'ye tıklatın, kalan gerekli bilgileri girin ve ardından **Kaydet**'e tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f6d9a-128">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="f6d9a-129">Kaynak Çalışma Konumu olarak adlandırılan seçenek kümesi tabanlı fiyatlandırma boyutu</span><span class="sxs-lookup"><span data-stu-id="f6d9a-129">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="f6d9a-130">Kaynak Çalışma Saatleri olarak adlandırılan seçenek kümesi tabanlı fiyatlandırma boyutu</span><span class="sxs-lookup"><span data-stu-id="f6d9a-130">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="f6d9a-131">Varlık tabanlı boyutlar için veri oluşturma</span><span class="sxs-lookup"><span data-stu-id="f6d9a-131">Create data for entity-based dimensions</span></span>

<span data-ttu-id="f6d9a-132">Varlık tabanlı boyutlarla ilgili verileri el ile veya Microsoft Excel içe aktarma veya servis çağrılarını kullanarak oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f6d9a-132">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="f6d9a-133">Bu yordamdaki adımları, varlık tabanlı **Standart Başlık** boyutundan **Sistem Mühendisi** ve **Kıdemli Sistem Mühendisi** adında iki standart başlık oluşturmak için kullanın.</span><span class="sxs-lookup"><span data-stu-id="f6d9a-133">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="f6d9a-134">Oluşturmak istediğiniz veriler küçük ise, aşağıdaki örnekte olduğu gibi standart bir form kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f6d9a-134">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="f6d9a-135">PSA'da, **Gelişmiş Bul**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f6d9a-135">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="f6d9a-136">**Standart Başlık** varlığını seçin ve **Sonuçlar** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f6d9a-136">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="f6d9a-137">**Standart Başlık** varlığındaki tüm satırlar gösterilir.</span><span class="sxs-lookup"><span data-stu-id="f6d9a-137">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="f6d9a-138">**Yeni** düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f6d9a-138">Click **New**.</span></span> <span data-ttu-id="f6d9a-139">**Ad** alanına "Sistem Mühendisi" yazın ve **Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f6d9a-139">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="f6d9a-140">Formu kapatın.</span><span class="sxs-lookup"><span data-stu-id="f6d9a-140">Close the form.</span></span> 
4. <span data-ttu-id="f6d9a-141">"Kıdemli Sistem Mühendisi" için başka standart başlık oluşturmak üzere 1-3 arasındaki adımları tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="f6d9a-141">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="f6d9a-142">Standart Başlık varlığı için örnek veriler</span><span class="sxs-lookup"><span data-stu-id="f6d9a-142">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="f6d9a-143">Gerekli tüm PSA varlıklarını ve ilgili bileşenleri Fiyatlandırma Boyutu Çözümüne ekleme</span><span class="sxs-lookup"><span data-stu-id="f6d9a-143">Add all required PSA entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="f6d9a-144">Fiyatlandırma çözümünüz için aşağıdaki Project Service varlıklarını eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="f6d9a-144">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="f6d9a-145">Bu yordamdaki adımları kullanarak varlıkların yeni fiyatlandırma boyutlarından haberdar olmasını sağlamak için fiyatlandırma çözümünde bazı önemli şema değişiklikleri yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f6d9a-145">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="f6d9a-146">PSA'da, **Ayarlar** > **Çözümler**'e tıklayın ve ardından **\<kuruluşunuzun adı > fiyatlandırma boyutları**'na çift tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f6d9a-146">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="f6d9a-147">Çözüm Gezgininde, sol gezinti bölmesinde **Var Olanı Ekle** > **Varlıkları**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f6d9a-147">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="f6d9a-148">**Çözüm Bileşenleri** iletişim kutusunda aşağıdaki varlıkları seçin:</span><span class="sxs-lookup"><span data-stu-id="f6d9a-148">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="f6d9a-149">Gerçek</span><span class="sxs-lookup"><span data-stu-id="f6d9a-149">Actual</span></span>
- <span data-ttu-id="f6d9a-150">Ayrılabilir Kaynak</span><span class="sxs-lookup"><span data-stu-id="f6d9a-150">Bookable Resource</span></span>
- <span data-ttu-id="f6d9a-151">Tahmin Satırı</span><span class="sxs-lookup"><span data-stu-id="f6d9a-151">Estimate Line</span></span>
- <span data-ttu-id="f6d9a-152">Fatura Satırı Ayrıntısı</span><span class="sxs-lookup"><span data-stu-id="f6d9a-152">Invoice Line Detail</span></span>
- <span data-ttu-id="f6d9a-153">Yevmiye Defteri Satırı</span><span class="sxs-lookup"><span data-stu-id="f6d9a-153">Journal Line</span></span>
- <span data-ttu-id="f6d9a-154">Proje Sözleşmesi Satırı Ayrıntısı</span><span class="sxs-lookup"><span data-stu-id="f6d9a-154">Project Contract Line Detail</span></span>
- <span data-ttu-id="f6d9a-155">Proje Takımı Üyesi</span><span class="sxs-lookup"><span data-stu-id="f6d9a-155">Project Team Member</span></span>
- <span data-ttu-id="f6d9a-156">Teklif Satırı Ayrıntısı</span><span class="sxs-lookup"><span data-stu-id="f6d9a-156">Quote Line Detail</span></span>
- <span data-ttu-id="f6d9a-157">Rol Fiyatı Kar Payı</span><span class="sxs-lookup"><span data-stu-id="f6d9a-157">Role Price Markup</span></span>
- <span data-ttu-id="f6d9a-158">Rol Fiyatı</span><span class="sxs-lookup"><span data-stu-id="f6d9a-158">Role Price</span></span> 
- <span data-ttu-id="f6d9a-159">Zaman Girişi</span><span class="sxs-lookup"><span data-stu-id="f6d9a-159">Time Entry</span></span> 

> ![Varolan varlıkları fiyatlandırma boyutları çözümüne ekleme](media/Existing-entities-to-PD-solution.png)

> ![Çözüm bileşenleri seçme](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="f6d9a-162">Seçili varlıkların her biri için tüm formları ve görünümleri eklediğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="f6d9a-162">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="f6d9a-163">Yukarıda seçilen varlıklar için herhangi bir bağımlı varlık eklemeniz istendiğinde **Hayır**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f6d9a-163">When prompted to include any dependent entities for the entities selected above, click **No**.</span></span>

> ![İlgili tüm bileşenleri eklemeyin](media/Do-not-include-required.png)


