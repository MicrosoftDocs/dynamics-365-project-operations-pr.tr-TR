---
title: Fiyatlandırma boyutları için özel çözümler oluşturma
description: Bu konuda, özel fiyatlandırma boyutları oluştururken özel bir çözümün nasıl oluşturulacağı açıklanmaktadır.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 1d8117d6f6bcedc97264401fc941470f34efb1ae
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285012"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a><span data-ttu-id="d29ae-103">Fiyatlandırma boyutları için özel çözümler oluşturma</span><span class="sxs-lookup"><span data-stu-id="d29ae-103">Create custom solutions for pricing dimensions</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> <span data-ttu-id="d29ae-104">Tüm özel fiyatlandırma boyutu değişiklikleri ayrı bir çözümde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d29ae-104">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="d29ae-105">Bu önemli en iyi uygulama, gelecekte değişiklikleri güncelleştirmek veya kaldırmak için esneklik sağlar, işinizi yeniden kullanmanıza yardımcı olur ve bu değişiklikleri başka bir kuruluma aktarmayı kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="d29ae-105">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="d29ae-106">Gerekli değişiklikleri yaptıktan sonra bu çözümü bir **Yönetilen çözüm** olarak dışa aktarın ve fiyatlandırma ayarını yeniden kullanmak için diğer kurulumlara aktarın.</span><span class="sxs-lookup"><span data-stu-id="d29ae-106">After you make the required changes, export this solution as a **Managed solution**, and import it into other instances to reuse your pricing setup.</span></span>

1. <span data-ttu-id="d29ae-107">**Ayarlar** > **Çözümler**'i seçin ve ardından **Yeni** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="d29ae-107">Select **Settings** > **Solutions**, and then select **New**.</span></span> 
2. <span data-ttu-id="d29ae-108">Çözümü, **\<your organization name> fiyatlandırma boyutları** şeklinde adlandırın, kalan gerekli bilgileri girin ve ardından **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d29ae-108">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>

> ![Fiyatlandırma boyutları için özel bir çözüm oluşturma](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="d29ae-110">Gerekli tüm varlıkları ve ilgili bileşenleri Fiyatlandırma boyutu çözümüne ekleme</span><span class="sxs-lookup"><span data-stu-id="d29ae-110">Add all required entities and related components to the Pricing dimension solution</span></span>
<span data-ttu-id="d29ae-111">Fiyatlandırma çözümünüz için aşağıdaki Project Service varlıklarını eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="d29ae-111">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="d29ae-112">Bu yordamdaki adımları tamamlayarak varlıkların yeni fiyatlandırma boyutlarından haberdar olmasını sağlamak için fiyatlandırma çözümünde bazı önemli şema değişiklikleri yapın.</span><span class="sxs-lookup"><span data-stu-id="d29ae-112">Complete the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="d29ae-113">**Ayarlar** > **Çözümler**'i seçin ve ardından **\<your organization name> fiyatlandırma boyutları** ayarını çift tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d29ae-113">Select **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="d29ae-114">Çözüm Gezgininde, sol gezinti bölmesinde **Var Olanı Ekle** > **Varlıkları**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d29ae-114">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="d29ae-115">**Çözüm Bileşenleri** iletişim kutusunda aşağıdaki varlıkları seçin:</span><span class="sxs-lookup"><span data-stu-id="d29ae-115">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="d29ae-116">Gerçek</span><span class="sxs-lookup"><span data-stu-id="d29ae-116">Actual</span></span>
- <span data-ttu-id="d29ae-117">Ayrılabilir Kaynak</span><span class="sxs-lookup"><span data-stu-id="d29ae-117">Bookable Resource</span></span>
- <span data-ttu-id="d29ae-118">Tahmin Satırı</span><span class="sxs-lookup"><span data-stu-id="d29ae-118">Estimate Line</span></span>
- <span data-ttu-id="d29ae-119">Proje Görevi</span><span class="sxs-lookup"><span data-stu-id="d29ae-119">Project Task</span></span>
- <span data-ttu-id="d29ae-120">Fatura Satırı Ayrıntısı</span><span class="sxs-lookup"><span data-stu-id="d29ae-120">Invoice Line Detail</span></span>
- <span data-ttu-id="d29ae-121">Yevmiye Defteri Satırı</span><span class="sxs-lookup"><span data-stu-id="d29ae-121">Journal Line</span></span>
- <span data-ttu-id="d29ae-122">Proje Sözleşme Satırı Ayrıntısı</span><span class="sxs-lookup"><span data-stu-id="d29ae-122">Project Contract Line Detail</span></span>
- <span data-ttu-id="d29ae-123">Proje Takımı Üyesi</span><span class="sxs-lookup"><span data-stu-id="d29ae-123">Project Team Member</span></span>
- <span data-ttu-id="d29ae-124">Teklif Satırı Ayrıntısı</span><span class="sxs-lookup"><span data-stu-id="d29ae-124">Quote Line Detail</span></span>
- <span data-ttu-id="d29ae-125">Rol Fiyatı Kar Payı</span><span class="sxs-lookup"><span data-stu-id="d29ae-125">Role Price Markup</span></span>
- <span data-ttu-id="d29ae-126">Rol Fiyatı</span><span class="sxs-lookup"><span data-stu-id="d29ae-126">Role Price</span></span> 
- <span data-ttu-id="d29ae-127">Zaman Girişi</span><span class="sxs-lookup"><span data-stu-id="d29ae-127">Time Entry</span></span> 

> ![Varolan varlıkları fiyatlandırma boyutları çözümüne ekleme](media/Existing-entities-to-PD-solution.png)

> ![Çözüm bileşenleri seçme](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="d29ae-130">Seçili varlıkların her biri için tüm formları ve görünümleri eklediğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="d29ae-130">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="d29ae-131">Seçilen varlıklar için herhangi bir bağımlı varlık eklemeniz istendiğinde **Hayır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d29ae-131">When prompted to include any dependent entities for the selected entities, select **No**.</span></span>

> ![İlgili tüm bileşenleri eklemeyin](media/Do-not-include-required.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]