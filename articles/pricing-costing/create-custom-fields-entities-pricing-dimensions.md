---
title: Fiyatlandırma boyutları olarak özel alanlar ve varlıklar oluşturma
description: Bu konu özel seçenek kümeleri veya varlıklar oluşturma hakkında bilgi sağlar.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 2000f7e710267560fe2bd52b0e33024617d108ea
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898285"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="8fa0e-103">Fiyatlandırma boyutları olarak özel alanlar ve varlıklar oluşturma</span><span class="sxs-lookup"><span data-stu-id="8fa0e-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="8fa0e-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="8fa0e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8fa0e-105">Özel bir seçenek kümesi veya varlık oluşturmak istediğinizde aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="8fa0e-105">Complete the following steps any time that you want to create a custom option set or entity.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8fa0e-106">Tüm özel fiyatlandırma boyutu değişikliklerini ayrı bir çözümde yapmanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="8fa0e-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="8fa0e-107">Bu önemli en iyi uygulama, gelecekte değişiklikleri güncelleştirmek veya kaldırmak için esneklik sağlar, işinizi yeniden kullanmanıza yardımcı olur ve bu değişiklikleri başka bir kuruluma aktarmayı kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="8fa0e-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="8fa0e-108">Gerekli tüm değişiklikleri yaptıktan sonra, bu çözümü bir **Yönetilen çözüm** olarak dışa aktarın ve fiyatlandırma ayarını yeniden kullanmak için diğer kurulumlara aktarın.</span><span class="sxs-lookup"><span data-stu-id="8fa0e-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="8fa0e-109">Fiyatlandırma boyutları için özel bir çözüm oluşturma</span><span class="sxs-lookup"><span data-stu-id="8fa0e-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="8fa0e-110">**Ayarlar** > **Çözümler**'e gidin ve ardından yeni bir çözüm oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8fa0e-110">Go to **Settings** > **Solutions**, and then select **New** to create a new solution.</span></span> 
2. <span data-ttu-id="8fa0e-111">Çözümü, **\<your organization name> fiyatlandırma boyutları** şeklinde adlandırın, kalan gerekli bilgileri girin ve ardından **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8fa0e-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="8fa0e-112">Fiyatlandırma boyutu çözümünde özel alanlar ve seçenek kümeleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="8fa0e-112">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="8fa0e-113">Bir fiyatlandırma boyutu bir seçenek kümesi veya varlık olabilir.</span><span class="sxs-lookup"><span data-stu-id="8fa0e-113">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="8fa0e-114">Her ikisinin de fiyatlandırma çözümünüz içinde oluşturulması gerekir.</span><span class="sxs-lookup"><span data-stu-id="8fa0e-114">Both must be created in your pricing solution.</span></span> <span data-ttu-id="8fa0e-115">Bu yordamdaki adımlarda varlık tabanlı boyutların ve seçenek kümesi tabanlı boyutların nasıl oluşturulacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="8fa0e-115">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="8fa0e-116">Varlık tabanlı boyutlar</span><span class="sxs-lookup"><span data-stu-id="8fa0e-116">Entity-based dimensions</span></span>

1. <span data-ttu-id="8fa0e-117">**Ayarlar** > **Çözümler**'e gidin ve ardından **\<your organization name> fiyatlandırma boyutları** ayarını çift tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8fa0e-117">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="8fa0e-118">Çözüm Gezgininde, sol gezinti bölmesinde **Varlıkları**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="8fa0e-118">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="8fa0e-119">**Standart Başlık** adlı yeni bir varlık oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8fa0e-119">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="8fa0e-120">Kalan gerekli bilgileri girin ve ardından **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8fa0e-120">Enter the remaining required information, and then select **Save**.</span></span>


### <a name="option-set-based-dimensions"></a><span data-ttu-id="8fa0e-121">Seçenek kümesi tabanlı boyutlar</span><span class="sxs-lookup"><span data-stu-id="8fa0e-121">Option set-based dimensions</span></span> 
<span data-ttu-id="8fa0e-122">İki seçenek kümesi tabanlı boyut oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8fa0e-122">You can create two option set-based dimensions.</span></span> <span data-ttu-id="8fa0e-123">**Ana** konum çalışması ve **Yerinde** çalışma fiyatını izlemek için **Kaynak Çalışma Konumu**'nu ve iş tamamlandığında kar payı uygulamak için **Normal** ve **Fazla Mesai** değerleriyle **Kaynak Çalışma saatleri**'ni kullanın.</span><span class="sxs-lookup"><span data-stu-id="8fa0e-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="8fa0e-124">**Ayarlar** > **Çözümler**'e gidin ve ardından **\<your organization name> fiyatlandırma boyutları** ayarını çift tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8fa0e-124">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="8fa0e-125">Çözüm Gezgininde, sol gezinti bölmesinde **Seçenek Kümeleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="8fa0e-125">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="8fa0e-126">Yeni seçenek kümesi oluşturmak için **Yeni**'yi seçin, kalan gerekli bilgileri girin ve ardından **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8fa0e-126">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="8fa0e-127">Varlık tabanlı boyutlar için veri oluşturma</span><span class="sxs-lookup"><span data-stu-id="8fa0e-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="8fa0e-128">Varlık tabanlı boyutlarla ilgili verileri el ile veya Microsoft Excel içe aktarma veya servis çağrılarını kullanarak oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8fa0e-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="8fa0e-129">Bu yordamdaki adımları, varlık tabanlı **Standart Başlık** boyutundan **Sistem Mühendisi** ve **Kıdemli Sistem Mühendisi** adında iki standart başlık oluşturmak için kullanın.</span><span class="sxs-lookup"><span data-stu-id="8fa0e-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="8fa0e-130">Oluşturmak istediğiniz veriler küçük ise, aşağıdaki örnekte olduğu gibi standart bir form kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8fa0e-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="8fa0e-131">**Gelişmiş Bul**'u seçin, **Standart Başlık** varlığını seçin ve ardından **Sonuçlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="8fa0e-131">Select **Advanced Find**, select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="8fa0e-132">**Standart Başlık** varlığındaki tüm satırlar gösterilir.</span><span class="sxs-lookup"><span data-stu-id="8fa0e-132">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="8fa0e-133">**Yeni**'yi seçin ve **Ad** alanına "Sistem Mühendisi" yazın ve **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8fa0e-133">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
3. <span data-ttu-id="8fa0e-134">Formu kapatın.</span><span class="sxs-lookup"><span data-stu-id="8fa0e-134">Close the form.</span></span> 
4. <span data-ttu-id="8fa0e-135">"Kıdemli Sistem Mühendisi" için başka standart başlık oluşturmak üzere 1-3 arasındaki adımları tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="8fa0e-135">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="8fa0e-136">Gerekli tüm varlıkları ve ilgili bileşenleri Fiyatlandırma Boyutu Çözümüne ekleme</span><span class="sxs-lookup"><span data-stu-id="8fa0e-136">Add all required entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="8fa0e-137">Fiyatlandırma çözümünüz için aşağıdaki varlıkları eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="8fa0e-137">You will need to add the following entities to your pricing solution.</span></span> <span data-ttu-id="8fa0e-138">Bu yordamdaki adımları kullanarak varlıkların yeni fiyatlandırma boyutlarından haberdar olmasını sağlamak için fiyatlandırma çözümünde bazı önemli şema değişiklikleri yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8fa0e-138">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="8fa0e-139">**Ayarlar** > **Çözümler**'i seçin ve **\<your organization name> fiyatlandırma boyutları** ayarını çift tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8fa0e-139">Select **Settings** > **Solutions**, and double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="8fa0e-140">Çözüm Gezgininde, sol gezinti bölmesinde **Var Olanı Ekle** > **Varlıkları**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="8fa0e-140">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="8fa0e-141">**Çözüm Bileşenleri** iletişim kutusunda aşağıdaki varlıkları seçin:</span><span class="sxs-lookup"><span data-stu-id="8fa0e-141">In the **Solution Components** dialog box, select the following entities:</span></span>

  - <span data-ttu-id="8fa0e-142">Gerçek</span><span class="sxs-lookup"><span data-stu-id="8fa0e-142">Actual</span></span>
  - <span data-ttu-id="8fa0e-143">Ayrılabilir Kaynak</span><span class="sxs-lookup"><span data-stu-id="8fa0e-143">Bookable Resource</span></span>
  - <span data-ttu-id="8fa0e-144">Tahmin Satırı</span><span class="sxs-lookup"><span data-stu-id="8fa0e-144">Estimate Line</span></span>
  - <span data-ttu-id="8fa0e-145">Fatura Satırı Ayrıntısı</span><span class="sxs-lookup"><span data-stu-id="8fa0e-145">Invoice Line Detail</span></span>
  - <span data-ttu-id="8fa0e-146">Yevmiye Defteri Satırı</span><span class="sxs-lookup"><span data-stu-id="8fa0e-146">Journal Line</span></span>
  - <span data-ttu-id="8fa0e-147">Proje Sözleşmesi Satırı Ayrıntısı</span><span class="sxs-lookup"><span data-stu-id="8fa0e-147">Project Contract Line Detail</span></span>
  - <span data-ttu-id="8fa0e-148">Proje Takımı Üyesi</span><span class="sxs-lookup"><span data-stu-id="8fa0e-148">Project Team Member</span></span>
  - <span data-ttu-id="8fa0e-149">Teklif Satırı Ayrıntısı</span><span class="sxs-lookup"><span data-stu-id="8fa0e-149">Quote Line Detail</span></span>
  - <span data-ttu-id="8fa0e-150">Rol Fiyatı Kar Payı</span><span class="sxs-lookup"><span data-stu-id="8fa0e-150">Role Price Markup</span></span>
  - <span data-ttu-id="8fa0e-151">Rol Fiyatı</span><span class="sxs-lookup"><span data-stu-id="8fa0e-151">Role Price</span></span> 
  - <span data-ttu-id="8fa0e-152">Zaman Girişi</span><span class="sxs-lookup"><span data-stu-id="8fa0e-152">Time Entry</span></span> 


> [!NOTE]
> <span data-ttu-id="8fa0e-153">Seçili varlıkların her biri için tüm formları ve görünümleri eklediğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="8fa0e-153">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="8fa0e-154">Yukarıda seçilen varlıklar için herhangi bir bağımlı varlık eklemeniz istendiğinde **Hayır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="8fa0e-154">When prompted to include any dependent entities for the entities selected above, select **No**.</span></span>

