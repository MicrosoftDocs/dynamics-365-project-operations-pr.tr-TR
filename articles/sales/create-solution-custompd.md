---
title: Özel fiyatlandırma boyutları için çözüm oluşturma
description: Bu konu, özel fiyatlandırma boyutları için çözüm oluşturma hakkında bilgi sağlar.
author: Rumant
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 86f4cd2c26ebfca621d1b226b571d220d3b2441e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010360"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="9e41d-103">Özel fiyatlandırma boyutları için çözüm oluşturma</span><span class="sxs-lookup"><span data-stu-id="9e41d-103">Create a solution for custom pricing dimensions</span></span>

 <span data-ttu-id="9e41d-104">_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="9e41d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span> 

>[!IMPORTANT]
><span data-ttu-id="9e41d-105">Tüm özel fiyatlandırma boyutu değişiklikleri ayrı bir çözümde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="9e41d-105">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="9e41d-106">Bu önemli en iyi uygulama, gerektiğinde değişiklikleri güncelleştirmek veya kaldırmak için esneklik sağlar, çalışmanızı yeniden kullanmanıza yardımcı olur ve değişiklikleri diğer kurulumlara aktarmayı kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="9e41d-106">This important best practice allows the flexibility to update or remove changes as needed, helps with re-use of your work, and makes it easier to port changes to other instances.</span></span> <span data-ttu-id="9e41d-107">Gerekli değişiklikleri yaptıktan sonra bu çözümü bir **Yönetilen** çözüm olarak dışarı aktarın ve ardından yeniden kullanmak için diğer kurulumlara içeri aktarın.</span><span class="sxs-lookup"><span data-stu-id="9e41d-107">After you make the required changes, export this solution as a **Managed** solution, and then import into other instances for reuse.</span></span>

## <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="9e41d-108">Özel fiyatlandırma boyutları için çözüm oluşturma</span><span class="sxs-lookup"><span data-stu-id="9e41d-108">Create a solution for custom pricing dimensions</span></span>

1.  <span data-ttu-id="9e41d-109">**Ayarlar** > **Çözümler**'i seçin ve ardından **Yeni** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="9e41d-109">Select **Settings** > **Solutions**, and then select **New**.</span></span>
2.  <span data-ttu-id="9e41d-110">Çözümü *<your organization name> fiyatlandırma boyutları* olarak adlandırın.</span><span class="sxs-lookup"><span data-stu-id="9e41d-110">Name the solution, *<your organization name> pricing dimensions*.</span></span>
3. <span data-ttu-id="9e41d-111">Kalan gerekli bilgileri girin ve ardından **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="9e41d-111">Enter the remaining required information, and then select **Save**.</span></span>

  ![Özel fiyatlandırma boyutu çözümü oluşturma](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="9e41d-113">Gerekli tüm varlıkları ve ilgili bileşenleri Fiyatlandırma boyutu çözümüne ekleme</span><span class="sxs-lookup"><span data-stu-id="9e41d-113">Add all required entities and related components to the Pricing dimension solution</span></span>

<span data-ttu-id="9e41d-114">Fiyatlandırma çözümünüzde önemli şema değişiklikleri yapmak için aşağıdaki Project Service varlıklarını fiyatlandırma çözümünüze ekleyin.</span><span class="sxs-lookup"><span data-stu-id="9e41d-114">Add the following Project Service entities to your pricing solution to make important schema changes in the pricing solution.</span></span> <span data-ttu-id="9e41d-115">Bu yordamı tamamladıktan sonra varlıklar, yeni fiyatlandırma boyutlarını tanır.</span><span class="sxs-lookup"><span data-stu-id="9e41d-115">After you have completed this procedure, the entities will recognize the new pricing dimensions.</span></span>

1.  <span data-ttu-id="9e41d-116">**Ayarlar** > **Çözümler**'i seçin ve ardından **<*kuruluşunuzun adı*> fiyatlandırma boyutları**'na çift tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9e41d-116">Select **Settings** > **Solutions**, and then double-click **<*your organization name*> pricing dimensions**.</span></span>
2.  <span data-ttu-id="9e41d-117">Çözüm Gezgininde, sol gezinti bölmesinde **Var Olanı Ekle** > **Varlıkları**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="9e41d-117">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3.  <span data-ttu-id="9e41d-118">**Çözüm Bileşenleri** iletişim kutusunda aşağıdaki varlıkları seçin:</span><span class="sxs-lookup"><span data-stu-id="9e41d-118">In the **Solution Components** dialog box, select the following entities:</span></span>
 
   - <span data-ttu-id="9e41d-119">**Gerçek**</span><span class="sxs-lookup"><span data-stu-id="9e41d-119">**Actual**</span></span>
   - <span data-ttu-id="9e41d-120">**Ayrılabilir Kaynak**</span><span class="sxs-lookup"><span data-stu-id="9e41d-120">**Bookable Resource**</span></span>
   - <span data-ttu-id="9e41d-121">**Tahmin Satırı**</span><span class="sxs-lookup"><span data-stu-id="9e41d-121">**Estimate Line**</span></span>
   - <span data-ttu-id="9e41d-122">**Proje Görevi**</span><span class="sxs-lookup"><span data-stu-id="9e41d-122">**Project Task**</span></span>
   - <span data-ttu-id="9e41d-123">**Fatura Satırı Ayrıntısı**</span><span class="sxs-lookup"><span data-stu-id="9e41d-123">**Invoice Line Detail**</span></span>
   - <span data-ttu-id="9e41d-124">**Yevmiye Defteri Satırı**</span><span class="sxs-lookup"><span data-stu-id="9e41d-124">**Journal Line**</span></span>
   - <span data-ttu-id="9e41d-125">**Proje Sözleşme Satırı Ayrıntısı**</span><span class="sxs-lookup"><span data-stu-id="9e41d-125">**Project Contract Line Detail**</span></span>
   - <span data-ttu-id="9e41d-126">**Proje Takımı Üyesi**</span><span class="sxs-lookup"><span data-stu-id="9e41d-126">**Project Team Member**</span></span>
   - <span data-ttu-id="9e41d-127">**Teklif Satırı Ayrıntısı**</span><span class="sxs-lookup"><span data-stu-id="9e41d-127">**Quote Line Detail**</span></span>
   - <span data-ttu-id="9e41d-128">**Rol Fiyatı Kar Payı**</span><span class="sxs-lookup"><span data-stu-id="9e41d-128">**Role Price Markup**</span></span>
   - <span data-ttu-id="9e41d-129">**Rol Fiyatı**</span><span class="sxs-lookup"><span data-stu-id="9e41d-129">**Role Price**</span></span>
   - <span data-ttu-id="9e41d-130">**Zaman Girişi**</span><span class="sxs-lookup"><span data-stu-id="9e41d-130">**Time Entry**</span></span>
 
   ![Var olan varlıkları özel fiyatlandırma boyutu çözümüne ekleme](./media/Existing-entities-to-PD-solution.png)
 
 4. <span data-ttu-id="9e41d-132">Her varlık için eklenen bileşenleri ve her varlığın varlık kıymetlerinin nihai listesini gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="9e41d-132">For each entity, review the components being added and the final list of entity assets for each entity.</span></span> 

   >[!NOTE]
   > <span data-ttu-id="9e41d-133">Seçili varlıkların her biri için tüm formları ve görünümleri ekleyin.</span><span class="sxs-lookup"><span data-stu-id="9e41d-133">Include all forms and views for each of the selected entities.</span></span>

  ![Eklenen varlıklar](./media/solution-component-selection.png)


5.  <span data-ttu-id="9e41d-135">Seçilen varlıklar için bağımlı varlıklar eklemeniz istendiğinde **Hayır, gerekli bileşenleri ekleme** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="9e41d-135">When prompted to include any dependent entities for the selected entities, select **No, do not include required components.**</span></span>

    ![Bağımlı varlıklar ekleme](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]