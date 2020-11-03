---
title: Project Service Automation Güncelleştirme Sürümü 19, V3'teki yenilikler veya değişiklikler
description: Bu konuda, Project Service Automation, Güncelleştirme Sürümü 19, V3'teki özellikler ve düzeltmeler listelenir.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: ecc923cccfad21985025ab9d8006aaff16afc25f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086277"
---
# <a name="project-service-automation-update-release-19-v3"></a><span data-ttu-id="8dc66-103">Project Service Automation, Güncelleştirme Sürümü 19, V3</span><span class="sxs-lookup"><span data-stu-id="8dc66-103">Project Service Automation Update Release 19, V3</span></span>

<span data-ttu-id="8dc66-104">Dynamics 365 için Project Service Automation uygulamasına yönelik en son güncelleştirmeyi duyurmaktan mutluluk duyuyoruz.</span><span class="sxs-lookup"><span data-stu-id="8dc66-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="8dc66-105">Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir.</span><span class="sxs-lookup"><span data-stu-id="8dc66-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="8dc66-106">Bu sürüm Dynamics 365 9.x ile uyumludur.</span><span class="sxs-lookup"><span data-stu-id="8dc66-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="8dc66-107">Bu sürüme güncelleştirmek için Dynamics 365 online çözümler sayfası için Yönetim Merkezi'ni ziyaret edin ve güncelleştirmeyi yükleyin.</span><span class="sxs-lookup"><span data-stu-id="8dc66-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="8dc66-108">Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="8dc66-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="8dc66-109">Bu konuda, PSA V3, Güncelleştirme Sürümü 19'te yeni veya değiştirilmiş özellikler ve düzeltmeler listelenir.</span><span class="sxs-lookup"><span data-stu-id="8dc66-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 19.</span></span> <span data-ttu-id="8dc66-110">Bu sürüm, V3.10.30.41 derleme numarasına sahiptir ve Mayıs 2020'de kendi başına güncelleştirme olarak genel kullanıma sunulmuştur.</span><span class="sxs-lookup"><span data-stu-id="8dc66-110">This version has a build number of V3.10.30.41 and is generally available through a self-update in May 2020.</span></span>

## <a name="update-release-19"></a><span data-ttu-id="8dc66-111">Güncelleştirme Sürümü 19</span><span class="sxs-lookup"><span data-stu-id="8dc66-111">Update Release 19</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="8dc66-112">Hata düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="8dc66-112">Bug fixes</span></span>

<span data-ttu-id="8dc66-113">**Zaman ve Gider**</span><span class="sxs-lookup"><span data-stu-id="8dc66-113">**Time and Expense**</span></span>

<span data-ttu-id="8dc66-114">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="8dc66-114">The following issues have been fixed:</span></span> 

- <span data-ttu-id="8dc66-115">Zaman girişi içeri aktarma işlemlerinden kaynaklanan hatalar doğru şekilde görüntülenmiyor.</span><span class="sxs-lookup"><span data-stu-id="8dc66-115">Errors derived from time entry imports are not surfaced correctly.</span></span>
- <span data-ttu-id="8dc66-116">Zaman Girişi Kılavuzu **Yalnızca Tarih** alanı davranışını desteklemez.</span><span class="sxs-lookup"><span data-stu-id="8dc66-116">Time Entry Grid does not support **Date Only** field behavior.</span></span>
- <span data-ttu-id="8dc66-117">Proje Kaynakları projeyle bir gider oluşturamıyor.</span><span class="sxs-lookup"><span data-stu-id="8dc66-117">Project Resources are unable to create an expense with a project.</span></span>

<span data-ttu-id="8dc66-118">**Proje Yönetimi**</span><span class="sxs-lookup"><span data-stu-id="8dc66-118">**Project Management**</span></span>

<span data-ttu-id="8dc66-119">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="8dc66-119">The following issues have been fixed:</span></span> 

-  <span data-ttu-id="8dc66-120">En alt görev Tamamlama Hesaplaması (EAC) sırasında yanlış çalışma tahmini oluşturulmasına neden oluyor.</span><span class="sxs-lookup"><span data-stu-id="8dc66-120">Grandchild task causes an incorrect effort estimate during the Completion (EAC) Calculation.</span></span>

<span data-ttu-id="8dc66-121">**Sales**</span><span class="sxs-lookup"><span data-stu-id="8dc66-121">**Sales**</span></span>

<span data-ttu-id="8dc66-122">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="8dc66-122">The following issues have been fixed:</span></span> 

- <span data-ttu-id="8dc66-123">**Yeniden hesapla** eylemi gider sözleşme satırı ayrıntıları veya teklif satırı ayrıntıları ile çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8dc66-123">The **Recalculate** action does not work with expense contract line details or quote line details.</span></span>
- <span data-ttu-id="8dc66-124">**Masrafları Güncelleştir** gider tahminlerde eksik.</span><span class="sxs-lookup"><span data-stu-id="8dc66-124">**Update Prices** is missing for expense estimates.</span></span>
-  <span data-ttu-id="8dc66-125">Müşteriler **Proje Sözleşmesi** sayfasından özel sözleşme durumunu seçemiyor.</span><span class="sxs-lookup"><span data-stu-id="8dc66-125">Customers are unable to select custom contract status reasons from the **Project Contract** page.</span></span>
- <span data-ttu-id="8dc66-126">Bir tekliften özel bir fiyat listesi oluştururken, müşterilerin performansta bozulmayla karşılaşıyor.</span><span class="sxs-lookup"><span data-stu-id="8dc66-126">Customers experience degraded performance when creating a custom price list from a quote.</span></span>
- <span data-ttu-id="8dc66-127">Müşteriler **Teklif Satırı Ayrıntıları** ve **Sözleşme Satırı Ayrıntıları** sayfalarında **birim** varsayılanlarıyla ilgili tutarsızlık yaşıyor.</span><span class="sxs-lookup"><span data-stu-id="8dc66-127">Customers experience inconsistency with **unit** defaults on **Quote Line Details** and **Contract Line Details** pages.</span></span>
- <span data-ttu-id="8dc66-128">Borçlandırılabilir sözleşme satırına borçlandırılamayan işlem kategorisi eklemek, işlem kategorisinin **Borçlandırılamaz** faturalama türünü dikkate almaz.</span><span class="sxs-lookup"><span data-stu-id="8dc66-128">Adding non-chargeable transaction category items to a chargeable contract line will not respect the **Non-chargeable** billing type of the transaction category.</span></span>
- <span data-ttu-id="8dc66-129">Müşteriler önceden oluşturulan sözleşmelere yeni eklenen rolleri ve kategoriyi kullanamaz.</span><span class="sxs-lookup"><span data-stu-id="8dc66-129">Customers can't use the newly added roles and category on previously created contracts.</span></span>
- <span data-ttu-id="8dc66-130">Müşteriler PreValidateProjectTeamMemberUpdate.cs öğesinde Gereksiz alma konusunda performansta bozulmayla karşılaşıyor</span><span class="sxs-lookup"><span data-stu-id="8dc66-130">Customers experience degraded performance Unnecessary retrieve in PreValidateProjectTeamMemberUpdate.cs</span></span>
- <span data-ttu-id="8dc66-131">**Kaynak Kategoriler** listesinde borçlandırılamaz olarak ayarlanan rollerin, birprojenin sözleşme satırında **Borçlandırılabilir Roller** sekmesine **Borçlandırılamaz** olarak eklenmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="8dc66-131">Roles set up as non-chargeable in the **Resource Categories** list should be added to the **Chargeable Roles** tab as **Non0chargeable** on the contract line for a project.</span></span>
- <span data-ttu-id="8dc66-132">**GetBookableResourceIdFromUser** yalnızca birincil kimlik yerine ayrılabilir kaynaklara ait tüm sütunları aldığından müşteriler proje oluştururken performans sorunlarıyla karşılaşabilir.</span><span class="sxs-lookup"><span data-stu-id="8dc66-132">Customers may experience degraded performance when creating a project because **GetBookableResourceIdFromUser** retrieves all columns of bookable resources instead of just the primary ID.</span></span>
- <span data-ttu-id="8dc66-133">**TransactionType** varlığında, kullanıcıların işlem türleri için geçerli olmayan **Birimler** ve **UnitGroups** girmesini önlemek için ön doğrulama güncelleştirmesi eklentisi yoktur.</span><span class="sxs-lookup"><span data-stu-id="8dc66-133">**TransactionType** entity missing the pre-validation update plug-in to prevent users from entering **Units** and **UnitGroups** that are not valid for transaction types.</span></span>
- <span data-ttu-id="8dc66-134">**Kaldır** adımı, zaman girişi içeri aktarma için kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="8dc66-134">The **Remove** step does not work for time entry import.</span></span>
