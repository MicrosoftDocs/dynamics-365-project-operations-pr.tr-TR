---
title: Project Service Automation Güncelleştirme Sürümü 29, V3'teki yenilikler veya değişiklikler
description: Bu konuda, Project Service Automation, Güncelleştirme Sürümü 29, V3'teki özellikler ve düzeltmeler listelenir.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 320f4f74cb5997e42e2dc9e1d8c8a5ab95ae6647
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010495"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a><span data-ttu-id="e3075-103">Project Service Automation Güncelleştirme Sürümü 29, V3'teki yenilikler veya değişiklikler</span><span class="sxs-lookup"><span data-stu-id="e3075-103">What's new or changed in Project Service Automation Update Release 29, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="e3075-104">Dynamics 365 için Project Service Automation uygulamasına yönelik en son güncelleştirmeyi duyurmaktan mutluluk duyuyoruz.</span><span class="sxs-lookup"><span data-stu-id="e3075-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="e3075-105">Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir.</span><span class="sxs-lookup"><span data-stu-id="e3075-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="e3075-106">Bu sürüm Dynamics 365 9.x ile uyumludur.</span><span class="sxs-lookup"><span data-stu-id="e3075-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="e3075-107">Bu sürüme güncelleştirmek için Dynamics 365 online çözümler sayfası için Yönetim Merkezi'ni ziyaret edin ve güncelleştirmeyi yükleyin.</span><span class="sxs-lookup"><span data-stu-id="e3075-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="e3075-108">Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="e3075-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="e3075-109">Bu konuda, Project Service Automation Güncelleştirme Sürümü 29 V3'te yeni veya değiştirilmiş özellikler ve düzeltmeler listelenmektedir.</span><span class="sxs-lookup"><span data-stu-id="e3075-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.</span></span> <span data-ttu-id="e3075-110">Bu sürümün derleme numarası V3.10.47.7'tür ve genellikle Şubat 2021'de kendi kendini güncelleştirme aracılığıyla kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="e3075-110">This version has a build number of V3.10.47.7 and is generally available through a self-update in February 2021.</span></span>

## <a name="update-release-29"></a><span data-ttu-id="e3075-111">Güncelleştirme Sürümü 29</span><span class="sxs-lookup"><span data-stu-id="e3075-111">Update Release 29</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="e3075-112">Hata düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="e3075-112">Bug fixes</span></span>

<span data-ttu-id="e3075-113">**Zaman ve Gider**</span><span class="sxs-lookup"><span data-stu-id="e3075-113">**Time and Expense**</span></span>

<span data-ttu-id="e3075-114">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="e3075-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="e3075-115">Kullanıcılar, zaman girişi ızgarasında çalışma dışı günlerde günlüğe kaydedilen çalışma saatlerini göremez.</span><span class="sxs-lookup"><span data-stu-id="e3075-115">Users can't see working hours logged on non-working days in the time entry grid.</span></span>
- <span data-ttu-id="e3075-116">Onaylanan gider girişleri, kılavuzda düzenlenebilir.</span><span class="sxs-lookup"><span data-stu-id="e3075-116">Approved expense entries can be edited on the grid.</span></span>

<span data-ttu-id="e3075-117">**Proje Yönetimi**</span><span class="sxs-lookup"><span data-stu-id="e3075-117">**Project Management**</span></span>

<span data-ttu-id="e3075-118">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="e3075-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="e3075-119">Kaynak atama çalışma saatlerinin negatif olamamasını sağlamak için doğrulama mantığı eksik.</span><span class="sxs-lookup"><span data-stu-id="e3075-119">Missing validation logic to ensure resource assignment effort hours can't be negative.</span></span>
- <span data-ttu-id="e3075-120">**AssignResourcesForTask** özel eylemi yalnızca değiştirilen alanlar yerine tüm alanları güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e3075-120">The custom action, **AssignResourcesForTask** updates all fields instead of only changed fields.</span></span>
- <span data-ttu-id="e3075-121">**CreateProject** olayında kaydedilen eklentiler veya iş akışları olan bir ortamda bir projeyi kopyalarken **CopyWBSToProject** başarısız olursa **msdyn_bulkgenerationstatus** özniteliği güncelleştirilmez.</span><span class="sxs-lookup"><span data-stu-id="e3075-121">When copying a project in an environment with plug-ins or workflows that are registered on the **CreateProject** event, the **msdyn_bulkgenerationstatus** attribute isn't updated if the **CopyWBSToProject** fails.</span></span>
- <span data-ttu-id="e3075-122">Proje takvimini genişlettiğinizde çalışma günleri, bazı proje görevi güncelleştirmelerinin başarısız olmasına neden olacak şekilde artan düzende sıralanmaz.</span><span class="sxs-lookup"><span data-stu-id="e3075-122">When you expand the project calendar, the working days aren't sorted in ascending order causing some project task updates to fail.</span></span>
- <span data-ttu-id="e3075-123">Mevcut bir projede Proje Yöneticisi'ni değiştirmek, kuruluş birimi varsayılan mantığını tetikler.</span><span class="sxs-lookup"><span data-stu-id="e3075-123">Changing the Project Manager on an existing project triggers the organizational unit defaulting logic.</span></span>

<span data-ttu-id="e3075-124">**Satışlar**</span><span class="sxs-lookup"><span data-stu-id="e3075-124">**Sales**</span></span>

<span data-ttu-id="e3075-125">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="e3075-125">The following issues have been fixed:</span></span>

- <span data-ttu-id="e3075-126">**Sözleşme** sayfasındaki **Sözleşme Performansı** sekmesi, sözleşme satırı olmadığında başlatma sırasında sessizce başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="e3075-126">The **Contract Performance** tab on the **Contract** page fails silently during initialization when no contract lines are present.</span></span>