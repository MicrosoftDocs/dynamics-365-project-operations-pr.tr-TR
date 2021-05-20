---
title: Project Service Automation Güncelleştirme Sürümü 15, V3'teki yenilikler veya değişiklikler
description: Bu konu Project Service Automation Güncelleştirme Sürüm 15, V3'teki yenilikler hakkında bilgi sağlar.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.openlocfilehash: fe1e2b2046faeee4e4c71484a976d70e8722e090
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949343"
---
# <a name="project-service-automation-update-release-15-v3"></a><span data-ttu-id="b22f0-103">Project Service Automation, Güncelleştirme Sürümü 15, V3</span><span class="sxs-lookup"><span data-stu-id="b22f0-103">Project Service Automation Update Release 15, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="b22f0-104">Dynamics 365 Project Service Automation (PSA) uygulaması için en son güncelleştirmeyi duyurmaktan mutluluk duyuyoruz.</span><span class="sxs-lookup"><span data-stu-id="b22f0-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="b22f0-105">Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir.</span><span class="sxs-lookup"><span data-stu-id="b22f0-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="b22f0-106">Bu sürüm Dynamics 365 9.x ile uyumludur.</span><span class="sxs-lookup"><span data-stu-id="b22f0-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="b22f0-107">Bu sürüme güncelleştirmek için Dynamics 365 (online) için Yönetim Merkezi'ni ziyaret edin ve güncelleştirmeyi yüklemek için çözümler sayfasına gidin.</span><span class="sxs-lookup"><span data-stu-id="b22f0-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="b22f0-108">Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="b22f0-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="b22f0-109">Bu konuda, PSA V3, Güncelleştirme Sürümü 15'te yeni veya değiştirilmiş özellikler ve düzeltmeler listelenir.</span><span class="sxs-lookup"><span data-stu-id="b22f0-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 15.</span></span> <span data-ttu-id="b22f0-110">Bu sürüm, V3.10.5.28 derleme numarasına sahiptir ve Ocak 2020 tarihinde kendi kendine güncelleştirme ile genel kullanıma sunulmuştur.</span><span class="sxs-lookup"><span data-stu-id="b22f0-110">This version has a build number of V3.10.5.28 and is generally available through a self-update in January 2020.</span></span>

## <a name="update-release-15"></a><span data-ttu-id="b22f0-111">Güncelleştirme Sürümü 15</span><span class="sxs-lookup"><span data-stu-id="b22f0-111">Update Release 15</span></span> 

### <a name="enhancements"></a><span data-ttu-id="b22f0-112">Geliştirmeler</span><span class="sxs-lookup"><span data-stu-id="b22f0-112">Enhancements</span></span>

- <span data-ttu-id="b22f0-113">Proje Yönetimi</span><span class="sxs-lookup"><span data-stu-id="b22f0-113">Project Management</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="b22f0-114">Hata düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="b22f0-114">Bug fixes</span></span>

- <span data-ttu-id="b22f0-115">Zaman ve Gider</span><span class="sxs-lookup"><span data-stu-id="b22f0-115">Time and Expense</span></span>

  - <span data-ttu-id="b22f0-116">Düzeltildi: Mutabakat görünümünde eklenti yükleme hatası işleme.</span><span class="sxs-lookup"><span data-stu-id="b22f0-116">Fixed: Add on-load error handling in the reconciliation view.</span></span>
  - <span data-ttu-id="b22f0-117">Düzeltildi: Proje Kaynak Merkezi: Belirsizliği azaltmak için **Tutar** olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="b22f0-117">Fixed: Project Resource Hub: Rename **Amount** to reduce ambiguity.</span></span>
  - <span data-ttu-id="b22f0-118">Düzeltildi: **Zaman Girişi Sütunlarını Kopyala** görünümü, türü de içerecek şekilde düzenlendi.</span><span class="sxs-lookup"><span data-stu-id="b22f0-118">Fixed: Adjust the view **Copy Time Entry Columns** to include the type.</span></span>
  - <span data-ttu-id="b22f0-119">Düzeltildi: Kılavuz görünümünde zaman girişi süresinin ondalık sayılar kullanarak düzenlenmesi bazı sayılarda bilinmeyen hatalara neden oluyor.</span><span class="sxs-lookup"><span data-stu-id="b22f0-119">Fixed: Editing time entry duration in the grid view using decimal numbers results in unknown error for some numbers.</span></span>

- <span data-ttu-id="b22f0-120">Proje Yönetimi</span><span class="sxs-lookup"><span data-stu-id="b22f0-120">Project Management</span></span>

  - <span data-ttu-id="b22f0-121">Düzeltildi: **İzleme Görünümünde Kullan** açılır menüsü artık seçeneklerin genişliğine göre genişliyor.</span><span class="sxs-lookup"><span data-stu-id="b22f0-121">Fixed: The drop-down menu for **Use in Tracking View** now expands based on the width of the options.</span></span>
  - <span data-ttu-id="b22f0-122">Düzeltildi: Projeler +13 saat diliminde yönetilirken görev hesaplamaları yanlış sonuçlar gösterebilir.</span><span class="sxs-lookup"><span data-stu-id="b22f0-122">Fixed: When managing projects in the +13 time zone, tasks calculations can display inaccurate results.</span></span>
  - <span data-ttu-id="b22f0-123">Düzeltildi: **Takım Üyesi Bitiş Saati** 24 saatlik takvim seçeneği için düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="b22f0-123">Fixed: **Team Member End Time** has been corrected when using a 24-hour calendar.</span></span>
  - <span data-ttu-id="b22f0-124">Düzeltildi: **msdyn_project** ana formunda **BPF** yeniden etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b22f0-124">Fixed: Re-activated the **BPF** in **msdyn_project** main form.</span></span>
  - <span data-ttu-id="b22f0-125">Düzeltildi: Atama hesaplaması artık bir günü yok saymıyor.</span><span class="sxs-lookup"><span data-stu-id="b22f0-125">Fixed: Assignments calculation no longer ignores one day.</span></span>
  - <span data-ttu-id="b22f0-126">Düzeltildi: Kullanıcının ve projenin saat diliminin farklı olduğu durumlarda proje formuna yeni bir bildirim başlığı eklendi.</span><span class="sxs-lookup"><span data-stu-id="b22f0-126">Fixed: A new notification banner has been added to the project form when the time zone differs between user and project.</span></span>

- <span data-ttu-id="b22f0-127">Sales</span><span class="sxs-lookup"><span data-stu-id="b22f0-127">Sales</span></span>

  - <span data-ttu-id="b22f0-128">Düzeltildi: Gider tahmini kategori araması, yinelenen öğeleri filtrelemek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="b22f0-128">Fixed: Expense estimate category lookup can be used to filter duplicates.</span></span>
  - <span data-ttu-id="b22f0-129">Düzeltildi: **PluginDomain.ExecuteInTryCatchBlock(..)** içindeki kod artık özel durumun kaynağını gizlemiyor.</span><span class="sxs-lookup"><span data-stu-id="b22f0-129">Fixed: Code in **PluginDomain.ExecuteInTryCatchBlock(..)** no longer hides the origin of the exception.</span></span>
  - <span data-ttu-id="b22f0-130">Düzeltildi: 1000'den fazla proje olduğunda, **Teklif Satırı** formundaki **Proje arama** hata iletisi artık görünmüyor.</span><span class="sxs-lookup"><span data-stu-id="b22f0-130">Fixed: No longer get an error message in **Project lookup** in the **Quote Line** form when there are more than 1000 projects.</span></span>
  - <span data-ttu-id="b22f0-131">Düzeltildi: İşçilik tahminleri ve gider tahminleri için **Tahminler** ızgarası artık doğru para birimi simgesiyle görüntüleniyor.</span><span class="sxs-lookup"><span data-stu-id="b22f0-131">Fixed: **Estimates** grid for labor estimates and expense estimates now displays the correct currency symbol.</span></span>
  - <span data-ttu-id="b22f0-132">Düzeltildi: Bir kuruluş PSA'yı Güncelleştirme Sürümü 14'ten Güncelleştirme Sürümü 15'e güncelleştirdiğinde, **Zamanlama** sekmesi **Proje** formunda artık boş görünmüyor.</span><span class="sxs-lookup"><span data-stu-id="b22f0-132">Fixed: After an organization updates PSA from Update Release 14 to Update Release 15, the **Schedule** tab no longer appears as blank on the **Project** form.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]