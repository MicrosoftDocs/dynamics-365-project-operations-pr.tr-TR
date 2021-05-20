---
title: Project Service Automation Güncelleştirme Sürümü 31, V3'teki yenilikler veya değişiklikler
description: Bu konuda, Project Service Automation, Güncelleştirme Sürümü 31, V3'teki özellikler ve düzeltmeler listelenir.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: a595c0a129ac35d3416984e57908e73e1eaef2fd
ms.sourcegitcommit: 6e1498502461e86cff722ccaf8795ff11c7c47ad
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5945559"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a><span data-ttu-id="a8397-103">Project Service Automation Güncelleştirme Sürümü 31, V3'teki yenilikler veya değişiklikler</span><span class="sxs-lookup"><span data-stu-id="a8397-103">What's new or changed in Project Service Automation Update Release 31, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="a8397-104">Dynamics 365 için Project Service Automation uygulamasına yönelik en son güncelleştirmeyi duyurmaktan mutluluk duyuyoruz.</span><span class="sxs-lookup"><span data-stu-id="a8397-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="a8397-105">Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir.</span><span class="sxs-lookup"><span data-stu-id="a8397-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="a8397-106">Bu sürüm Dynamics 365 9.x ile uyumludur.</span><span class="sxs-lookup"><span data-stu-id="a8397-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="a8397-107">Bu sürüme güncelleştirmek için Dynamics 365 online çözümler sayfası için Yönetim Merkezi'ni ziyaret edin ve güncelleştirmeyi yükleyin.</span><span class="sxs-lookup"><span data-stu-id="a8397-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="a8397-108">Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="a8397-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="a8397-109">Bu konuda, Project Service Automation Güncelleştirme Sürümü 31 V3'te yeni veya değiştirilmiş özellikler ve düzeltmeler listelenmektedir.</span><span class="sxs-lookup"><span data-stu-id="a8397-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 31.</span></span> <span data-ttu-id="a8397-110">Bu sürüm, V3.10.52.77 derleme numarasına sahiptir ve Mayıs 2021'de kendi başına güncelleştirme olarak genel kullanıma sunulmuştur.</span><span class="sxs-lookup"><span data-stu-id="a8397-110">This version has a build number of V3.10.52.77 and is generally available through a self-update in May 2021.</span></span>

## <a name="update-release-31"></a><span data-ttu-id="a8397-111">Güncelleştirme Sürümü 31</span><span class="sxs-lookup"><span data-stu-id="a8397-111">Update Release 31</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="a8397-112">Hata düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="a8397-112">Bug fixes</span></span>

<span data-ttu-id="a8397-113">**Zaman ve Gider**</span><span class="sxs-lookup"><span data-stu-id="a8397-113">**Time and Expense**</span></span>

<span data-ttu-id="a8397-114">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="a8397-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="a8397-115">**Ayrılabilir kaynak** sayfasındaki saat girişi denetimi komut düğmeleri kafa karıştırıcı olarak kullanıldı.</span><span class="sxs-lookup"><span data-stu-id="a8397-115">Time entry control command buttons on the **Bookable Resource** page were confusing.</span></span>
- <span data-ttu-id="a8397-116">**Project.SetTrackingFields**'de bir zaman girişi onaylarken bir null başvuru özel durumu üretildi.</span><span class="sxs-lookup"><span data-stu-id="a8397-116">A null reference exception was generated in **Project.SetTrackingFields** when approving a time entry.</span></span>

<span data-ttu-id="a8397-117">**Kaynak Yönetimi**</span><span class="sxs-lookup"><span data-stu-id="a8397-117">**Resource Management**</span></span>

<span data-ttu-id="a8397-118">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="a8397-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="a8397-119">**Takım üyesi oluşturma**, **Varsayılan ayırma durumu taahhüt** ayarı için ayar meta verileri ayarını doğru olarak görüntülemez.</span><span class="sxs-lookup"><span data-stu-id="a8397-119">**Create Team Member** doesn't correctly display the booking setup metadata setting for **Default Booking Committed Status**.</span></span>
- <span data-ttu-id="a8397-120">PSA 1.X'den 3.X'e yükseltilirken yükseltme işlemi, **UpgradeResourceRequirements**'de başarısız olur .</span><span class="sxs-lookup"><span data-stu-id="a8397-120">When upgrading from PSA 1.X to 3.X, the upgrade process fails at **UpgradeResourceRequirements**.</span></span>


<span data-ttu-id="a8397-121">**Satışlar**</span><span class="sxs-lookup"><span data-stu-id="a8397-121">**Sales**</span></span>

<span data-ttu-id="a8397-122">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="a8397-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="a8397-123">Gerçek gelir miktarları izleme kılavuzundaki proje para birimine dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="a8397-123">Actual revenue converts the amounts to the project currency in the tracking grid.</span></span>
- <span data-ttu-id="a8397-124">Bir kuruluşun temel para biriminin proje para biriminden farklı olduğu senaryolarda günlük satırları, teklif satırları ve sözleşme satırları oluştururken varsayılan para birimi belirsiz olur.</span><span class="sxs-lookup"><span data-stu-id="a8397-124">The currency default is unclear when creating journal lines, quote lines, and contract lines in scenarios where an organization's base currency differs from the project currency.</span></span>
- <span data-ttu-id="a8397-125">**Bekleyen düzeltme günlüğü doğrulama** sorgusu projeye göre filtremiyor.</span><span class="sxs-lookup"><span data-stu-id="a8397-125">**Pending correction journal validation** query doesn't filter by project.</span></span>
- <span data-ttu-id="a8397-126">Kalan satışlar, proje üzerinde yanlış hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="a8397-126">Remaining sales are calculated incorrectly on a project.</span></span>
- <span data-ttu-id="a8397-127">İlgili kişiye dayanan teklifler, Fiyat listesi olmadan oluşturulduklarında başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="a8397-127">Quotes based on a contact fail when they are created without a price list.</span></span>
- <span data-ttu-id="a8397-128">**Faturayı Onayla** seçeneğini belirlediğinizde hiçbir işleme değiştiricisi görüntülenmez.</span><span class="sxs-lookup"><span data-stu-id="a8397-128">No processing spinner is shown when you select **Confirm Invoice**.</span></span>
- <span data-ttu-id="a8397-129">**Fatura Oluştur** seçeneğini belirlediğinizde hiçbir işleme değiştiricisi görüntülenmez.</span><span class="sxs-lookup"><span data-stu-id="a8397-129">No processing spinner is shown when you select **Create Invoice**.</span></span>
- <span data-ttu-id="a8397-130">Bir teklifin kaybedilmesi kayıp olarak kapatılırsa, rezervasyon iptal edilebilir.</span><span class="sxs-lookup"><span data-stu-id="a8397-130">Closing a quote as lost doesn't cancel the bookings.</span></span>







