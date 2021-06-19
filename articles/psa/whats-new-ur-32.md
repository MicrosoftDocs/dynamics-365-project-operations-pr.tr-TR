---
title: Project Service Automation Güncelleştirme Sürümü 32, V3'teki yenilikler veya değişiklikler
description: Bu konuda, Project Service Automation, Güncelleştirme Sürümü 32, V3'teki özellikler ve düzeltmeler listelenir.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 11bf451ef4f24e2301ffde4f86a556a8a4fe30b0
ms.sourcegitcommit: 886102894244887d72e5a6213071e8d8a52c9d48
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129690"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a><span data-ttu-id="c4461-103">Project Service Automation Güncelleştirme Sürümü 32, V3'teki yenilikler veya değişiklikler</span><span class="sxs-lookup"><span data-stu-id="c4461-103">What's new or changed in Project Service Automation Update Release 32, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="c4461-104">Microsoft Dynamics 365 Project Service Automation uygulaması için en yeni güncelleştirmeyi sunmaktan mutluluk duyarız.</span><span class="sxs-lookup"><span data-stu-id="c4461-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="c4461-105">Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir.</span><span class="sxs-lookup"><span data-stu-id="c4461-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="c4461-106">Dynamics 365 9.x ile uyumludur.</span><span class="sxs-lookup"><span data-stu-id="c4461-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="c4461-107">Bu sürüme güncelleştirmek için Dynamics 365 çevrimiçi çözümler sayfasının için Yönetici Merkezi sayfasını ziyaret edin ve güncelleştirmeyi kurun.</span><span class="sxs-lookup"><span data-stu-id="c4461-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="c4461-108">Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="c4461-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="c4461-109">Bu konuda, Project Service Automation Güncelleştirme Sürümü 32 V3'te yeni veya değiştirilmiş özellikler ve düzeltmeler listelenmektedir.</span><span class="sxs-lookup"><span data-stu-id="c4461-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 32.</span></span> <span data-ttu-id="c4461-110">Bu sürümün derleme numarası V3.10.53.108'dir ve genellikle Haziran 2021'de kendi kendine güncelleştirme aracılığıyla kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c4461-110">This version has a build number of V3.10.53.108 and is generally available through a self-update in June 2021.</span></span>

## <a name="update-release-32"></a><span data-ttu-id="c4461-111">Güncelleştirme Sürümü 32</span><span class="sxs-lookup"><span data-stu-id="c4461-111">Update Release 32</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="c4461-112">Hata düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="c4461-112">Bug fixes</span></span>

#### <a name="general"></a><span data-ttu-id="c4461-113">Genel</span><span class="sxs-lookup"><span data-stu-id="c4461-113">General</span></span>

- <span data-ttu-id="c4461-114">Büyük bir yükseltme başarısız olduğunda, paylaşılan varlıkların hala erişilebilir olduğundan emin olmak için yalnızca ana uygulama giriş noktalarının engellenmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="c4461-114">When a major upgrade fails, only the main application entry points should be blocked, to ensure that shared entities are still accessible.</span></span>

#### <a name="time-and-expense"></a><span data-ttu-id="c4461-115">Zaman ve Gider</span><span class="sxs-lookup"><span data-stu-id="c4461-115">Time and Expense</span></span>

<span data-ttu-id="c4461-116">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="c4461-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="c4461-117">**TimeEntriesImportFromResourceAssignment**, kaynak atama kontur diliminin başlangıç ve bitiş saatlerini korumaz.</span><span class="sxs-lookup"><span data-stu-id="c4461-117">**TimeEntriesImportFromResourceAssignment** doesn't maintain the start and end times of the resource assignment contour slice.</span></span>
- <span data-ttu-id="c4461-118">**Zaman Girişi** ızgarasında **Açık Giriş**'i seçtiğinizde, diğer formların seçilmesini engellemiş olabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c4461-118">When you select **Open Entry** on the **Time Entry** grid, you might be prevented from selecting other forms.</span></span>
- <span data-ttu-id="c4461-119">Zaman girişlerine atamaları aktarırken istemci kod sorgusu, sorguyu geçemeyen uzun bir URL oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="c4461-119">While you import assignments to time entries, the client code query could generate a long URL that fails the query.</span></span>
- <span data-ttu-id="c4461-120">**Zaman Girişi** ızgarasında bir değer bir hücreden silindikten sonra, odak ızgara içinde kalmaz.</span><span class="sxs-lookup"><span data-stu-id="c4461-120">In the **Time Entry** grid, after a value is deleted from a cell, the focus doesn't remain in the grid.</span></span>
- <span data-ttu-id="c4461-121">Modern onaylar için **İşleme onayları** görünümünden **Reddet** düğmesi kaldırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="c4461-121">The **Reject** button has been removed from the **Processing approvals** view for modern approvals.</span></span>
- <span data-ttu-id="c4461-122">Zaman girişi toplu onayının kararlılığı ve performansı, kilitlenmelerden etkilenir ve **Zaman Girişi** varlığıyla ilişkili özelleştirmelerin uygun şekilde işlenememesinden etkilenir.</span><span class="sxs-lookup"><span data-stu-id="c4461-122">The stability and performance of time entry bulk approval are affected by deadlocks and a failure to appropriately handle customizations that are related to the **Time Entry** entity.</span></span>

#### <a name="project-planning"></a><span data-ttu-id="c4461-123">Proje Planlama</span><span class="sxs-lookup"><span data-stu-id="c4461-123">Project Planning</span></span>

- <span data-ttu-id="c4461-124">**Sözleşme Birimi** alanında null değere sahip bir projeyi güncelleştirdiğinizde null başvuru istisnası oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c4461-124">A null reference exception is generated when you update a project that has a null value in the **Contracting Unit** field.</span></span>
- <span data-ttu-id="c4461-125">**Proje Toplamlarını Yenile**, projedeki kalan maliyeti ve kalan satışları yanlış şekilde hesaplar.</span><span class="sxs-lookup"><span data-stu-id="c4461-125">**Refresh Project Totals** incorrectly calculates the remaining cost and remaining sales on a project.</span></span>
- <span data-ttu-id="c4461-126">Yedek fiyatlandırma hesaplamaları, kaynak atama dağılımlarındaki güncelleştirmelerle ilgili performansı etkiler.</span><span class="sxs-lookup"><span data-stu-id="c4461-126">Redundant pricing calculations affect performance that is related to updates on resource assignment contours.</span></span>

#### <a name="resource-management"></a><span data-ttu-id="c4461-127">Kaynak Yönetimi</span><span class="sxs-lookup"><span data-stu-id="c4461-127">Resource Management</span></span>

<span data-ttu-id="c4461-128">Aşağıdaki sorun düzeltildi:</span><span class="sxs-lookup"><span data-stu-id="c4461-128">The following issue has been fixed:</span></span>

- <span data-ttu-id="c4461-129">Ayrılabilir bir kaynağın takvim kapasitesi 1'den fazla olduğunda, Project Service Automation kapasiteyi yanlış bir şekilde 0 (sıfır) olarak tanır.</span><span class="sxs-lookup"><span data-stu-id="c4461-129">When a bookable resource's calendar capacity is more than 1, Project Service Automation incorrectly recognizes the capacity as 0 (zero).</span></span> <span data-ttu-id="c4461-130">Bu nedenle zamanlama görünümünde sonsuz bir döngü oluşur.</span><span class="sxs-lookup"><span data-stu-id="c4461-130">Therefore, an infinite loop occurs in the schedule view.</span></span>

#### <a name="sales"></a><span data-ttu-id="c4461-131">Satışlar</span><span class="sxs-lookup"><span data-stu-id="c4461-131">Sales</span></span>

<span data-ttu-id="c4461-132">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="c4461-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="c4461-133">Özel bir hareket türüne sahip bir günlük satırı oluşturulduğunda, şu null başvuru özel durumu oluşturulur: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span><span class="sxs-lookup"><span data-stu-id="c4461-133">When a journal line is created that has a custom transaction type, the following null reference exception occurs: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span></span>
- <span data-ttu-id="c4461-134">Bir teklif kopyalanmadan önce devre dışı bırakılan roller ve kategoriler, yeni kopyalanan teklifin borçlandırılabilir rol ve kategorilerine eklenmemelidir.</span><span class="sxs-lookup"><span data-stu-id="c4461-134">Roles and categories that are inactivated before a quotation is copied should not be added to chargeable roles and categories of the newly copied quotation.</span></span>
- <span data-ttu-id="c4461-135">Belge tarihi ve muhasebe tarihi, doğrudan bir taslak faturada oluşturulan fatura satırı ayrıntısı üzerinde sağlanan başlangıç tarihiyle uyumlu değildir.</span><span class="sxs-lookup"><span data-stu-id="c4461-135">The document date and accounting date aren't aligned with the start date that is provided on an invoice line detail that is created directly on a draft invoice.</span></span>
- <span data-ttu-id="c4461-136">Null başvuru istisnaları, bir teklif kopyalanmadan önce rollerin ve kategorilerin etkinleştirilmesiyle ilgili senaryolarda üretilir.</span><span class="sxs-lookup"><span data-stu-id="c4461-136">Null reference exceptions are generated in scenarios that are related to inactivation of roles and categories before a quotation is copied.</span></span>
- <span data-ttu-id="c4461-137">**Projeler** sayfasındaki **Fiyatları güncelleştir** eylemi, masraf tahminlerini ve malzeme tahminlerini güncelleştirmez.</span><span class="sxs-lookup"><span data-stu-id="c4461-137">The **Update Prices** action on the **Projects** page doesn't update expense estimates and material estimates.</span></span>
