---
title: Proje tabanlı fırsat yönetimi
description: Bu konu, projelerle ilgili fırsatlarla nasıl çalışılacağı hakkında bilgi sağlar.
author: rumant
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2d1f9b29e0e9516ff78517e47694a2385c083ec7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277857"
---
# <a name="manage-project-based-opportunities"></a><span data-ttu-id="909ba-103">Proje tabanlı fırsat yönetimi</span><span class="sxs-lookup"><span data-stu-id="909ba-103">Manage project-based opportunities</span></span>

<span data-ttu-id="909ba-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="909ba-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="909ba-105">Proje tabanlı şirketlerin, genellikle birden çok ülkeye ve coğrafi bölgelerde teslimat işlemleri vardır.</span><span class="sxs-lookup"><span data-stu-id="909ba-105">Project-based companies typically have their operations for delivery spread across multiple countries and geographies.</span></span> <span data-ttu-id="909ba-106">Projenin yürütülme ve teslimat maliyeti, teslimi hangi Coğrafya veya bölmenin yönetmediğini temel alarak değişiklik gösterebilir.</span><span class="sxs-lookup"><span data-stu-id="909ba-106">The cost of the project execution and delivery can vary  based on which geography or division manages the delivery.</span></span> <span data-ttu-id="909ba-107">Bunun için, bu işlem, anlaşma kenar boşluklarını etkileyebilir.</span><span class="sxs-lookup"><span data-stu-id="909ba-107">In turn, this can impact the margins of the deal.</span></span> <span data-ttu-id="909ba-108">Proje tabanlı servislerin teslimatı genellikle büyük miktarda insan kaynakları süresi, seyahat için önemli giderler, malzeme maliyetleri ve diğer giderler içerir.</span><span class="sxs-lookup"><span data-stu-id="909ba-108">Delivery of project-based services typically involves large quantities of human resource time, considerable expenses for travel, material costs, and other expenses.</span></span>

<span data-ttu-id="909ba-109">Dynamics 365 Project Operations'ta proje tabanlı fırsatlar, Dynamics 365 Sales için uzantılarla tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="909ba-109">Project-based opportunities in Dynamics 365 Project Operations are designed with extensions to Dynamics 365 Sales.</span></span> <span data-ttu-id="909ba-110">Konu, proje tabanlı şirketlerin proje bazlı fırsatları yönetmesi için gereken ek işlevselliğe dahil edilen farklı alanlar ve iş mantığı hakkında ayrıntılar sağlar.</span><span class="sxs-lookup"><span data-stu-id="909ba-110">The topic provides details about the different fields and business logic included in the additional functionality that is required by project-based companies to manage project-based opportunities.</span></span>

## <a name="view-all-project-based-opportunities"></a><span data-ttu-id="909ba-111">Proje tabanlı fırsatları görüntüleme</span><span class="sxs-lookup"><span data-stu-id="909ba-111">View all project-based opportunities</span></span>

<span data-ttu-id="909ba-112">Proje tabanlı tüm fırsatların listesi **Fırsat** listesi sayfasından görülebilir.</span><span class="sxs-lookup"><span data-stu-id="909ba-112">A list of all the project-based opportunities can be seen from the **Opportunity** list page.</span></span> 

1. <span data-ttu-id="909ba-113">**Satış** > **Fırsatlar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="909ba-113">Go to **Sales** > **Opportunities**.</span></span>
2. <span data-ttu-id="909ba-114">Fırsatların diğer filtre uygulanmış görünümlerini seçmek için **görünüm değiştiriciyi** kullanın.</span><span class="sxs-lookup"><span data-stu-id="909ba-114">Use the **View switcher** to select other filtered views of the opportunities.</span></span> <span data-ttu-id="909ba-115">Bu görünümleri ve gezinti seçeneklerini yapılandırmak için özel filtre ölçütleriyle birlikte kendi görünümlerinizi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="909ba-115">You can create your own views with custom filter criteria to configure these views and navigation options.</span></span>

<span data-ttu-id="909ba-116">Proje Fırsatları, bu liste sayfasından veya ayrıntı sayfasından oluşturulabilir veya silinebilir.</span><span class="sxs-lookup"><span data-stu-id="909ba-116">Project Opportunities can be created or deleted from this list page or the detail page.</span></span>

## <a name="business-process-flow-for-project-based-deals"></a><span data-ttu-id="909ba-117">Proje tabanlı anlaşmalar için iş süreci akışı</span><span class="sxs-lookup"><span data-stu-id="909ba-117">Business process flow for project-based deals</span></span>

<span data-ttu-id="909ba-118">Project Operations'ta proje tabanlı anlaşmalar için aşağıdaki iş süreci akışları desteklenir:</span><span class="sxs-lookup"><span data-stu-id="909ba-118">The following business process flows are supported for project-based deals in Project Operations:</span></span>

- <span data-ttu-id="909ba-119">Müşteri Adayından Fırsata iş süreci</span><span class="sxs-lookup"><span data-stu-id="909ba-119">Lead to Opportunity business process</span></span>
- <span data-ttu-id="909ba-120">Fırsat satış süreci</span><span class="sxs-lookup"><span data-stu-id="909ba-120">Opportunity sales process</span></span>

### <a name="lead-to-opportunity-business-process"></a><span data-ttu-id="909ba-121">Müşteri Adayından Fırsata iş süreci</span><span class="sxs-lookup"><span data-stu-id="909ba-121">Lead to opportunity business process</span></span> 
<span data-ttu-id="909ba-122">Müşteri Adayından Fırsata iş süreci aşağıdaki aşamaları destekler:</span><span class="sxs-lookup"><span data-stu-id="909ba-122">The lead to opportunity business process supports the following stages:</span></span>

| <span data-ttu-id="909ba-123">Aşama</span><span class="sxs-lookup"><span data-stu-id="909ba-123">Stage</span></span> | <span data-ttu-id="909ba-124">Eşlenen varlık</span><span class="sxs-lookup"><span data-stu-id="909ba-124">Mapped entity</span></span> | <span data-ttu-id="909ba-125">İşlev</span><span class="sxs-lookup"><span data-stu-id="909ba-125">Functionality</span></span> |
| --- | --- | --- |
| <span data-ttu-id="909ba-126">Nitelikli Hale Getir</span><span class="sxs-lookup"><span data-stu-id="909ba-126">Qualify</span></span> | <span data-ttu-id="909ba-127">Müşteri adayı</span><span class="sxs-lookup"><span data-stu-id="909ba-127">Lead</span></span> | <span data-ttu-id="909ba-128">Firma, ilgili kişi ve fırsat oluşturmak için müşteri adayını uygun bulun.</span><span class="sxs-lookup"><span data-stu-id="909ba-128">Qualify the lead to create an account, contact, and an opportunity.</span></span> |
| <span data-ttu-id="909ba-129">Geliştir</span><span class="sxs-lookup"><span data-stu-id="909ba-129">Develop</span></span> | <span data-ttu-id="909ba-130">Fırsat</span><span class="sxs-lookup"><span data-stu-id="909ba-130">Opportunity</span></span> | <span data-ttu-id="909ba-131">Mevcut çalışmalar, önemli paydaşlar ve rekabet hakkında daha fazla bilgi eklemek için fırsatı geliştirin.</span><span class="sxs-lookup"><span data-stu-id="909ba-131">Develop the opportunity to add more information on the work involved, key stakeholders, and competition.</span></span> |
| <span data-ttu-id="909ba-132">Teklif Et</span><span class="sxs-lookup"><span data-stu-id="909ba-132">Propose</span></span> | <span data-ttu-id="909ba-133">Fırsat</span><span class="sxs-lookup"><span data-stu-id="909ba-133">Opportunity</span></span> | <span data-ttu-id="909ba-134">Teklifi geliştirin ve dahili inceleme takımından onay alın.</span><span class="sxs-lookup"><span data-stu-id="909ba-134">Develop the proposal and get approval from the internal review team.</span></span> |
| <span data-ttu-id="909ba-135">Kapat</span><span class="sxs-lookup"><span data-stu-id="909ba-135">Close</span></span> | <span data-ttu-id="909ba-136">Fırsat</span><span class="sxs-lookup"><span data-stu-id="909ba-136">Opportunity</span></span> | <span data-ttu-id="909ba-137">Anlaşmaya varmak için fırsatı kazanın.</span><span class="sxs-lookup"><span data-stu-id="909ba-137">Win the opportunity to close the deal.</span></span> |

### <a name="opportunity-sales-process"></a><span data-ttu-id="909ba-138">Fırsat satış süreci</span><span class="sxs-lookup"><span data-stu-id="909ba-138">Opportunity sales process</span></span>
<span data-ttu-id="909ba-139">Proje İşlemlerindeki fırsat satış süreci, satış uygulamasındaki fırsat satışları işi iş akışına bir uzantıdır.</span><span class="sxs-lookup"><span data-stu-id="909ba-139">The Opportunity sales process in Project Operations is an extension to the Opportunity sales process business flow in the Sales application.</span></span> <span data-ttu-id="909ba-140">Bu iş süreci proje tabanlı bir fırsatta aşağıdaki aşamaları desteklemek için kullanıma hazır olarak tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="909ba-140">This business process is designed out-of-the-box to support the following stages in a project-based opportunity.</span></span>

| <span data-ttu-id="909ba-141">Aşama</span><span class="sxs-lookup"><span data-stu-id="909ba-141">Stage</span></span> | <span data-ttu-id="909ba-142">Eşlenen varlık</span><span class="sxs-lookup"><span data-stu-id="909ba-142">Mapped entity</span></span> | <span data-ttu-id="909ba-143">İşlev</span><span class="sxs-lookup"><span data-stu-id="909ba-143">Functionality</span></span> |
| --- | --- | --- |
| <span data-ttu-id="909ba-144">Nitelikli Hale Getir</span><span class="sxs-lookup"><span data-stu-id="909ba-144">Qualify</span></span> | <span data-ttu-id="909ba-145">Fırsat</span><span class="sxs-lookup"><span data-stu-id="909ba-145">Opportunity</span></span> | <span data-ttu-id="909ba-146">Firma, ilgili kişi ve fırsat oluşturmak için müşteri adayını uygun bulun.</span><span class="sxs-lookup"><span data-stu-id="909ba-146">Qualify the lead to create an account, contact, and an opportunity.</span></span> |
| <span data-ttu-id="909ba-147">Teklif Et</span><span class="sxs-lookup"><span data-stu-id="909ba-147">Propose</span></span> | <span data-ttu-id="909ba-148">Teklif</span><span class="sxs-lookup"><span data-stu-id="909ba-148">Quote</span></span> | <span data-ttu-id="909ba-149">Proje tekliflerini kullanarak teklifi geliştirin ve dahili inceleme takımından onay alın.</span><span class="sxs-lookup"><span data-stu-id="909ba-149">Develop the proposal using project quotes and get approval from the internal review team.</span></span> |
| <span data-ttu-id="909ba-150">Sözleşme</span><span class="sxs-lookup"><span data-stu-id="909ba-150">Contract</span></span> | <span data-ttu-id="909ba-151">Proje Sözleşmesi</span><span class="sxs-lookup"><span data-stu-id="909ba-151">Project Contract</span></span> | <span data-ttu-id="909ba-152">Sözleşmeyi oluşturmak için teklifi kazanın ve projede yürütmeye ve teslimata başlanır.</span><span class="sxs-lookup"><span data-stu-id="909ba-152">Win the quote to create the contract and begin execution and delivery on the project.</span></span> |
| <span data-ttu-id="909ba-153">Kapat</span><span class="sxs-lookup"><span data-stu-id="909ba-153">Close</span></span> | <span data-ttu-id="909ba-154">Proje Sözleşmesi</span><span class="sxs-lookup"><span data-stu-id="909ba-154">Project Contract</span></span> | <span data-ttu-id="909ba-155">İşi başarıyla bitirin ve proje sözleşmesini kapatın.</span><span class="sxs-lookup"><span data-stu-id="909ba-155">Finish the work successfully and close the project contract.</span></span> |

> [!NOTE]
> <span data-ttu-id="909ba-156">Proje tabanlı anlaşma bir müşteri adayıyla başlatıldıysa, fırsatın iş fırsatına göre önceliği vardır.</span><span class="sxs-lookup"><span data-stu-id="909ba-156">If your project-based deal started with a Lead, the Lead to Opportunity business process takes precedence.</span></span>
>
> <span data-ttu-id="909ba-157">Proje tabanlı anlaşma bir Fırsatla başlatıldıysa, Fırsat satışları iş fırsatına göre önceliği vardır.</span><span class="sxs-lookup"><span data-stu-id="909ba-157">If your project-based deal started with an Opportunity, the Opportunity sales process takes precedence.</span></span>

<span data-ttu-id="909ba-158">Satış sürecinizi gerektiği gibi izlemek için ürün iş süreci akışı düzenleyebilir veya kendi iş süreci akışlarınızı oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="909ba-158">You can edit the product business process flow or create your own business process flows to track your sales process as needed.</span></span> <span data-ttu-id="909ba-159">İş süreci akışları hakkında daha fazla bilgi için bkz. [İş süreci akışlarına genel bakış](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).</span><span class="sxs-lookup"><span data-stu-id="909ba-159">For more information about the business process flow, see [Business process flows overview](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]