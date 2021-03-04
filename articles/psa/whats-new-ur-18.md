---
title: Project Service Automation Güncelleştirme Sürümü 18, V3'teki yenilikler veya değişiklikler
description: Bu konuda, Project Service Automation, Güncelleştirme Sürümü 18, V3'teki özellikler ve düzeltmeler listelenir.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: d6e0bb669513185ca266858ea9b8a89ed6dd4408
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147227"
---
# <a name="project-service-automation-update-release-18-v3"></a><span data-ttu-id="a6a82-103">Project Service Automation, Güncelleştirme Sürümü 18, V3</span><span class="sxs-lookup"><span data-stu-id="a6a82-103">Project Service Automation Update Release 18, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="a6a82-104">Dynamics 365 için Project Service Automation uygulamasına yönelik en son güncelleştirmeyi duyurmaktan mutluluk duyuyoruz.</span><span class="sxs-lookup"><span data-stu-id="a6a82-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="a6a82-105">Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir.</span><span class="sxs-lookup"><span data-stu-id="a6a82-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="a6a82-106">Bu sürüm Dynamics 365 9.x ile uyumludur.</span><span class="sxs-lookup"><span data-stu-id="a6a82-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="a6a82-107">Bu sürüme güncelleştirmek için Dynamics 365 online Yönetim Merkezi'ni ziyaret edin ve çözümler sayfasından güncelleştirmeyi yükleyin.</span><span class="sxs-lookup"><span data-stu-id="a6a82-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="a6a82-108">Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="a6a82-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="a6a82-109">Bu konuda, Project Service Automation Güncelleştirme Sürümü 18 V3'te yeni veya değiştirilmiş özellikler ve düzeltmeler listelenmektedir.</span><span class="sxs-lookup"><span data-stu-id="a6a82-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 18.</span></span> <span data-ttu-id="a6a82-110">Bu sürüm, V3.10.8.12 derleme numarasına sahiptir ve Nisan 2020'de kendi başına güncelleştirme olarak genel kullanıma sunulmuştur.</span><span class="sxs-lookup"><span data-stu-id="a6a82-110">This version has a build number of V3.10.8.12 and is generally available through a self-update in April 2020.</span></span>

## <a name="update-release-18"></a><span data-ttu-id="a6a82-111">Güncelleştirme Sürümü 18</span><span class="sxs-lookup"><span data-stu-id="a6a82-111">Update Release 18</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="a6a82-112">Hata düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="a6a82-112">Bug fixes</span></span>

<span data-ttu-id="a6a82-113">**Zaman ve Gider**</span><span class="sxs-lookup"><span data-stu-id="a6a82-113">**Time and Expense**</span></span>

- <span data-ttu-id="a6a82-114">Düzeltildi: **Geri Çek**, **İste** ve **Onayı İptal Et** akışları anlaşılamaz hata iletileriyle özel durumlar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a6a82-114">Fixed: **Recall**, **Request**, and **Cancel Approval** flows throw exceptions with unclear error messages.</span></span>
- <span data-ttu-id="a6a82-115">Düzeltildi: **Onayı İptal Et** bir gider için başarısız olduğunda ilgili özel durum hatası oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="a6a82-115">Fixed: When **Cancel Approval** fails for an expense, a relevant exception error is not thrown.</span></span>
- <span data-ttu-id="a6a82-116">Düzeltildi: Zaman Girişi ızgarası, Avustralya'da Ekim ayında günışığından tasarrufa (DST) geçişten sonra iş günü olmayan günleri yanlış şekilde işler.</span><span class="sxs-lookup"><span data-stu-id="a6a82-116">Fixed: The Time Entry grid incorrectly handles non-working days in Australia after the daylight savings time (DST) switch in October.</span></span>
- <span data-ttu-id="a6a82-117">Düzeltildi: Yanlış varsayılan mantığı, giderlerin gönderilmesini engeller.</span><span class="sxs-lookup"><span data-stu-id="a6a82-117">Fixed: Incorrect defaulting logic prevents submission of expenses.</span></span>
- <span data-ttu-id="a6a82-118">Düzeltildi: Zaman girişi onayı başarısız olduğunda onay **Beklemede** durumunda kalır.</span><span class="sxs-lookup"><span data-stu-id="a6a82-118">Fixed: When time entry approval fails, the approval remains in a state of **Pending**.</span></span>
- <span data-ttu-id="a6a82-119">Düzeltildi: Toplu onaylardaki SQL Hataları (kilitlenme/zaman aşımı).</span><span class="sxs-lookup"><span data-stu-id="a6a82-119">Fixed: SQL Errors on bulk approvals (deadlock/timeout).</span></span>
- <span data-ttu-id="a6a82-120">Düzeltildi: Zaman girdilerini onaylarken takım üyelerini güncelleştirmeden kaynaklanan kullanıcı deneyiminde önemli performans sorunları.</span><span class="sxs-lookup"><span data-stu-id="a6a82-120">Fixed: Significant performance issues in the user experience caused by updating team members while approving time entries.</span></span>

<span data-ttu-id="a6a82-121">**Proje Yönetimi**</span><span class="sxs-lookup"><span data-stu-id="a6a82-121">**Project Management**</span></span>

- <span data-ttu-id="a6a82-122">Düzeltildi: Saat dilimi bildirimi, **Mutabakat** görünümünden **Proje** ana formuna taşındı.</span><span class="sxs-lookup"><span data-stu-id="a6a82-122">Fixed: Time zone notification moved from the **Reconciliation** view to the **Project** main form.</span></span>
- <span data-ttu-id="a6a82-123">Düzeltildi: Takvim şablonu, yeni bir proje formu açıldığında doğru şekilde varsayılan hale gelmiyor.</span><span class="sxs-lookup"><span data-stu-id="a6a82-123">Fixed: Calendar template is not correctly defaulting when a new project form opens.</span></span>
- <span data-ttu-id="a6a82-124">Düzeltildi: Chromium tabanlı tarayıcılar için kullanıcılar, silinecek öncül görevleri kolay şekilde seçemiyor.</span><span class="sxs-lookup"><span data-stu-id="a6a82-124">Fixed: For chromium-based browsers, users are unable to easily select predecessor tasks to delete.</span></span>
- <span data-ttu-id="a6a82-125">Düzeltildi: **Boş Şablondan Proje** oluşturmak veya kopyalamak, ilişkisiz atamalar getirir.</span><span class="sxs-lookup"><span data-stu-id="a6a82-125">Fixed: Creating or copying **Project from Empty template** fetches unrelated assignments.</span></span>
- <span data-ttu-id="a6a82-126">Düzeltildi: Özel uç durumlarda görev kılavuzundan yeni atama oluşturmak, oluşturulan kayıtların yinelenmesiyle sonuçlanır.</span><span class="sxs-lookup"><span data-stu-id="a6a82-126">Fixed: In specific edge cases, creating a new assignment from the task grid results in duplicate records being created.</span></span>
- <span data-ttu-id="a6a82-127">Düzeltildi: El ile modunda kullanıcılar, görevin başlangıç tarihlerini geçerli kayıt tarihinden sonra olacak şekilde güncelleştiremez.</span><span class="sxs-lookup"><span data-stu-id="a6a82-127">Fixed: In manual mode, users are unable to update task start dates to be later than the current date saved.</span></span>

<span data-ttu-id="a6a82-128">**Kaynak Yönetimi**</span><span class="sxs-lookup"><span data-stu-id="a6a82-128">**Resource Management**</span></span>

- <span data-ttu-id="a6a82-129">Düzeltildi: **Mutabakat** görünümü alt toplam satırı, ayırmaları uzattıktan sonra ayırma farkını yanlış şekilde hesaplar.</span><span class="sxs-lookup"><span data-stu-id="a6a82-129">Fixed: **Reconciliation** view subtotal row incorrectly calculates bookings variance after extending bookings.</span></span>
- <span data-ttu-id="a6a82-130">Düzeltildi: **Mutabakat** görünümü, ayrılabilir kaynak proje takvimiyle eşleşmeyen bir takvime sahip olduğunda kaynak atamalarını yanlış şekilde görüntüler.</span><span class="sxs-lookup"><span data-stu-id="a6a82-130">Fixed: **Reconciliation** view incorrectly displays resource assignments when the bookable resource has a calendar that does not match the project calendar.</span></span>

<span data-ttu-id="a6a82-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="a6a82-131">**Sales**</span></span>

- <span data-ttu-id="a6a82-132">Düzeltildi: Zaman girişleri yeniden onaylandığında (**Onayla > İptal Et >** yeniden onayla) yinelenen bir borçlandırılamaz gerçek değer oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="a6a82-132">Fixed: When time entries are re-approved (**Approve > Cancel >** approve again), a duplicate non-chargeable actual is created.</span></span>
