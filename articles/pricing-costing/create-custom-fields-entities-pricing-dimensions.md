---
title: Fiyatlandırma boyutları olarak özel alanlar ve varlıklar oluşturma
description: Bu konu özel seçenek kümeleri veya varlıklar oluşturma hakkında bilgi sağlar.
author: rumant
manager: AnnBe
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: fc5917856b8f28d36dc55593a68eba7823a00b36
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642837"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="7bdc7-103">Fiyatlandırma boyutları olarak özel alanlar ve varlıklar oluşturma</span><span class="sxs-lookup"><span data-stu-id="7bdc7-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="7bdc7-104">_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="7bdc7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7bdc7-105">Fiyatlandırma boyutu olarak kullanmak için özel bir seçenek kümesi veya varlık oluşturmak istediğinizde aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="7bdc7-105">Complete the following steps when you want to create a custom option set or entity for using it as a pricing dimension.</span></span> <span data-ttu-id="7bdc7-106">Daha fazla bilgi için bkz. [Fiyatlandırma boyutlarına genel bakış](pricing-dimensions-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7bdc7-106">For more information, see [Pricing dimensions overview](pricing-dimensions-overview.md).</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="7bdc7-107">Tüm özel fiyatlandırma boyutu değişikliklerini ayrı bir çözümde yapmanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="7bdc7-107">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="7bdc7-108">Bu önemli en iyi uygulama, gerektiğinde değişiklikleri güncelleştirmek veya kaldırmak için gelecekte esneklik sağlar.</span><span class="sxs-lookup"><span data-stu-id="7bdc7-108">This important best practice provides flexibility in the future to update or remove changes as needed.</span></span> <span data-ttu-id="7bdc7-109">Bu ayrıca çalışmanızın yeniden kullanımına yardımcı olur ve bu değişiklikleri diğer kuruluma aktarmayı kolaylaştırır. Gerekli tüm değişiklikleri yaptıktan sonra bu çözümü bir **Yönetilen çözüm** olarak dışarı aktarın ve fiyatlandırma ayarınızı yeniden kullanmak için diğer kurulumlara içeri aktarın.</span><span class="sxs-lookup"><span data-stu-id="7bdc7-109">This will also help with re-use of your work and make it easier to port these changes to another instance After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="7bdc7-110">Fiyatlandırma boyutu çözümünde özel alanlar ve seçenek kümeleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="7bdc7-110">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="7bdc7-111">Bir fiyatlandırma boyutu bir seçenek kümesi veya varlık olabilir.</span><span class="sxs-lookup"><span data-stu-id="7bdc7-111">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="7bdc7-112">Her ikisinin de fiyatlandırma çözümünüz içinde oluşturulması gerekir.</span><span class="sxs-lookup"><span data-stu-id="7bdc7-112">Both must be created in your pricing solution.</span></span> <span data-ttu-id="7bdc7-113">Bu yordamdaki adımlarda varlık tabanlı boyutların ve seçenek kümesi tabanlı boyutların nasıl oluşturulacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="7bdc7-113">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="7bdc7-114">Varlık tabanlı boyutlar</span><span class="sxs-lookup"><span data-stu-id="7bdc7-114">Entity-based dimensions</span></span>
<span data-ttu-id="7bdc7-115">Varlık tabanlı boyutlar oluşturmak için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="7bdc7-115">To create entity-based dimensions, follow these steps:</span></span>

1. <span data-ttu-id="7bdc7-116">**Ayarlar** > **Çözümler**'e gidin ve ardından **\<your organization name> fiyatlandırma boyutları** ayarını çift tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7bdc7-116">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="7bdc7-117">Çözüm Gezgini'nde, sol gezinti bölmesinde **Varlıklar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7bdc7-117">In Solution Explorer, in the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="7bdc7-118">**Standart Başlık** adlı yeni bir varlık oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7bdc7-118">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="7bdc7-119">Kalan gerekli bilgileri girin ve ardından **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7bdc7-119">Enter the remaining required information, and then select **Save**.</span></span>

> ![Standart başlık varlığı tanımı](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a><span data-ttu-id="7bdc7-121">Seçenek kümesi tabanlı boyutlar</span><span class="sxs-lookup"><span data-stu-id="7bdc7-121">Option set-based dimensions</span></span> 
<span data-ttu-id="7bdc7-122">İki seçenek kümesi tabanlı boyut oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7bdc7-122">You can create two option set-based dimensions.</span></span> 

- <span data-ttu-id="7bdc7-123">**Ev** konumu ve **Yerinde** çalışmanın fiyatını izlemek için **Kaynak Çalışma Konumunu** kullanın.</span><span class="sxs-lookup"><span data-stu-id="7bdc7-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work.</span></span> 
- <span data-ttu-id="7bdc7-124">Çalışma tamamlandığında sair gider uygulamak için **Normal** ve **Fazla Mesai** değerlerinin olduğu **Kaynak Çalışma saatlerini** kullanın.</span><span class="sxs-lookup"><span data-stu-id="7bdc7-124">Use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when the work is complete.</span></span>

<span data-ttu-id="7bdc7-125">Aşağıdaki grafik, **Kaynak Çalışma Konumu** boyutunun görünümünü sağlar.</span><span class="sxs-lookup"><span data-stu-id="7bdc7-125">The following graphic provides a view of the **Resource Work Location** dimension.</span></span> 

> ![Kaynak Çalışma Konumu olarak adlandırılan seçenek kümesi tabanlı fiyatlandırma boyutu](media/Option-set-PD-called-Resource-Work-Location.png)

<span data-ttu-id="7bdc7-127">Aşağıdaki grafik, **Kaynak Çalışma Saatleri** boyutunun görünümünü sağlar.</span><span class="sxs-lookup"><span data-stu-id="7bdc7-127">The following graphic provides a view of the **Resource Work Hours** dimension.</span></span> 

> ![Kaynak Çalışma Saatleri olarak adlandırılan seçenek kümesi tabanlı fiyatlandırma boyutu](media/Option-set-PD-called-Resource-Work-Hours.png)

1. <span data-ttu-id="7bdc7-129">**Ayarlar** > **Çözümler**'e gidin ve ardından **\<your organization name> fiyatlandırma boyutları** ayarını çift tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7bdc7-129">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="7bdc7-130">Çözüm Gezgini'nde, sol gezinti bölmesinde **Seçenek Kümeleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="7bdc7-130">In Solution Explorer, in the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="7bdc7-131">Yeni seçenek kümesi oluşturmak için **Yeni**'yi seçin, kalan gerekli bilgileri girin ve ardından **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7bdc7-131">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="7bdc7-132">Varlık tabanlı boyutlar için veri oluşturma</span><span class="sxs-lookup"><span data-stu-id="7bdc7-132">Create data for entity-based dimensions</span></span>

<span data-ttu-id="7bdc7-133">Varlık tabanlı boyutlarla ilgili verileri el ile veya Microsoft Excel içe aktarma veya servis çağrılarını kullanarak oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7bdc7-133">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="7bdc7-134">Bu yordamdaki adımları, varlık tabanlı **Standart Başlık** boyutundan **Sistem Mühendisi** ve **Kıdemli Sistem Mühendisi** adında iki standart başlık oluşturmak için kullanın.</span><span class="sxs-lookup"><span data-stu-id="7bdc7-134">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="7bdc7-135">Oluşturmak istediğiniz veriler küçük ise, aşağıdaki örnekte olduğu gibi standart bir form kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7bdc7-135">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="7bdc7-136">**Gelişmiş Bul**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="7bdc7-136">Select **Advanced Find**.</span></span>
2. <span data-ttu-id="7bdc7-137">**Standart Başlık** varlığını seçin ve ardından **Sonuçlar** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="7bdc7-137">Select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="7bdc7-138">**Standart Başlık** varlığındaki tüm satırlar gösterilir.</span><span class="sxs-lookup"><span data-stu-id="7bdc7-138">All of the rows in the **Standard Title** entity will be shown.</span></span>
3. <span data-ttu-id="7bdc7-139">**Yeni**'yi seçin ve **Ad** alanına "Sistem Mühendisi" yazın ve **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7bdc7-139">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
4. <span data-ttu-id="7bdc7-140">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="7bdc7-140">Close the page.</span></span> 
5. <span data-ttu-id="7bdc7-141">"Kıdemli Sistem Mühendisi" için başka standart başlık oluşturmak üzere 1-3 arasındaki adımları tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="7bdc7-141">Repeat steps 1-3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![Standart Başlık varlığı için örnek veriler](media/ST-data.png)
