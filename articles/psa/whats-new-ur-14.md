---
title: Project Service Automation Güncelleştirme Sürümü 14, V3'teki yenilikler veya değişiklikler
description: Bu konu Project Service Automation Güncelleştirme Sürüm 14 V3'teki yenilikler hakkında bilgi sağlar.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: 00ce5c68b1141c88671f0534f7500bf0d7eebd8e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086282"
---
# <a name="project-service-automation-update-release-14-v3"></a><span data-ttu-id="bee06-103">Project Service Automation, Güncelleştirme Sürümü 14, V3</span><span class="sxs-lookup"><span data-stu-id="bee06-103">Project Service Automation Update Release 14, V3</span></span>
<span data-ttu-id="bee06-104">Dynamics 365 Project Service Automation (PSA) uygulaması için en son güncelleştirmeyi duyurmaktan mutluluk duyuyoruz.</span><span class="sxs-lookup"><span data-stu-id="bee06-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="bee06-105">Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir.</span><span class="sxs-lookup"><span data-stu-id="bee06-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="bee06-106">Bu sürüm Dynamics 365 9.x ile uyumludur.</span><span class="sxs-lookup"><span data-stu-id="bee06-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="bee06-107">Bu sürüme güncelleştirmek için Dynamics 365 (online) için Yönetim Merkezi'ni ziyaret edin ve güncelleştirmeyi yüklemek için çözümler sayfasına gidin.</span><span class="sxs-lookup"><span data-stu-id="bee06-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="bee06-108">Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="bee06-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="bee06-109">Bu konuda, PSA V3, Güncelleştirme Sürümü 14'te yeni veya değiştirilmiş özellikler ve düzeltmeler listelenir.</span><span class="sxs-lookup"><span data-stu-id="bee06-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 14.</span></span> <span data-ttu-id="bee06-110">Bu sürüm, V3.10.4.21 derleme numarasına sahiptir ve aşağıdaki zamanlamada kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="bee06-110">This version has a build number of V3.10.4.21 and is available on the following schedule:</span></span>

- <span data-ttu-id="bee06-111">**Genel kullanılabilirlik (kendi kendine güncelleştirme):** Ocak 2020</span><span class="sxs-lookup"><span data-stu-id="bee06-111">**General availability (self-update):** January 2020</span></span>
- <span data-ttu-id="bee06-112">**Otomatik Güncelleştirme:** Şubat 2020</span><span class="sxs-lookup"><span data-stu-id="bee06-112">**Auto-update:** February 2020</span></span>

## <a name="update-release-14"></a><span data-ttu-id="bee06-113">Güncelleştirme Sürümü 14</span><span class="sxs-lookup"><span data-stu-id="bee06-113">Update Release 14</span></span>

### <a name="enhancements"></a><span data-ttu-id="bee06-114">Geliştirmeler</span><span class="sxs-lookup"><span data-stu-id="bee06-114">Enhancements</span></span>

- <span data-ttu-id="bee06-115">Sales</span><span class="sxs-lookup"><span data-stu-id="bee06-115">Sales</span></span>

     - <span data-ttu-id="bee06-116">**Teklif Satırı Ayrıntıları** içinden gelen özel alan değerleri bir teklif **Kazanıldı olarak kapatıldı** seçeneğine güncelleştirildiğinde **Proje Sözleşmesi Satır Ayrıntıları** altına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="bee06-116">Custom field values from **Quote Line Details** are copied to **Project Contract Line Details** when a quote is updated to **Closed as won**.</span></span>
     - <span data-ttu-id="bee06-117">Onaylanan projeler **Kaybedildi olarak kapatılabilir**.</span><span class="sxs-lookup"><span data-stu-id="bee06-117">Confirmed projects can be **Closed as lost**.</span></span>

- <span data-ttu-id="bee06-118">Kaynak Yönetimi</span><span class="sxs-lookup"><span data-stu-id="bee06-118">Resource Management</span></span>

     - <span data-ttu-id="bee06-119">Ayırmalar uzatılırken, kullanıcılara ayırma sonuçlarını özetleyen ve Ayırmaları Koru bağlantısı içeren bir onay iletişim kutusu gösterilir.</span><span class="sxs-lookup"><span data-stu-id="bee06-119">When extending bookings, users will be prompted with a confirmation dialog box to summarize booking results and provide a link to Maintain Bookings.</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="bee06-120">Hata düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="bee06-120">Bug fixes</span></span>

- <span data-ttu-id="bee06-121">Zaman ve Gider</span><span class="sxs-lookup"><span data-stu-id="bee06-121">Time and Expense</span></span>

     - <span data-ttu-id="bee06-122">Düzeltildi: Kullanıcı düzeltilecek herhangi bir giriş seçmediğinde gerçekleşen kullanıcı deneyimi iyileştirildi.</span><span class="sxs-lookup"><span data-stu-id="bee06-122">Fixed: Improved the user experience when the user has not selected any entries to be corrected.</span></span>

- <span data-ttu-id="bee06-123">Kaynak Yönetimi</span><span class="sxs-lookup"><span data-stu-id="bee06-123">Resource Management</span></span>

     - <span data-ttu-id="bee06-124">Düzeltildi: Bir kaynağın birden çok kez ayrılması, ayrılabilir kaynağın adının taşmasına neden oluyor.</span><span class="sxs-lookup"><span data-stu-id="bee06-124">Fixed: Booking a resource multiple times overflows the name of the bookable resource.</span></span>

- <span data-ttu-id="bee06-125">Sales</span><span class="sxs-lookup"><span data-stu-id="bee06-125">Sales</span></span>

     - <span data-ttu-id="bee06-126">Düzeltildi: Toplam satış fiyatı kullanıcı projedeki gider tahminleri için bir maliyet fiyatı girene kadar hesaplanmıyor.</span><span class="sxs-lookup"><span data-stu-id="bee06-126">Fixed: The total sales price is not calculated until the user also inputs a cost price for expense estimates on a project.</span></span>
     - <span data-ttu-id="bee06-127">Düzeltildi: İlişkili proje sözleşmesi **Taslak** durumunda değilse, teklif **Kazanıldı** olarak kapatılamıyor.</span><span class="sxs-lookup"><span data-stu-id="bee06-127">Fixed: Closing a quote as **Won** fails if the associated project contract is not in a **Draft** state.</span></span>
