---
title: Project Service Automation Güncelleştirme Sürümü 25, V3'teki yenilikler veya değişiklikler
description: Bu konuda, Project Service Automation, Güncelleştirme Sürümü 25, V3'teki özellikler ve düzeltmeler listelenir.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: 30822ec64b31e110202a587dd941bdff60116712
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280467"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a><span data-ttu-id="67de8-103">Project Service Automation Güncelleştirme Sürümü 25, V3'teki yenilikler veya değişiklikler</span><span class="sxs-lookup"><span data-stu-id="67de8-103">What's new or changed in Project Service Automation Update Release 25, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="67de8-104">Dynamics 365 için Project Service Automation uygulamasına yönelik en son güncelleştirmeyi duyurmaktan mutluluk duyuyoruz.</span><span class="sxs-lookup"><span data-stu-id="67de8-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="67de8-105">Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir.</span><span class="sxs-lookup"><span data-stu-id="67de8-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="67de8-106">Bu sürüm Dynamics 365 9.x ile uyumludur.</span><span class="sxs-lookup"><span data-stu-id="67de8-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="67de8-107">Bu sürüme güncelleştirmek için Dynamics 365 online çözümler sayfası için Yönetim Merkezi'ni ziyaret edin ve güncelleştirmeyi yükleyin.</span><span class="sxs-lookup"><span data-stu-id="67de8-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="67de8-108">Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="67de8-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="67de8-109">Bu konuda, Project Service Automation Güncelleştirme Sürümü 25 V3'te yeni veya değiştirilmiş özellikler ve düzeltmeler listelenmektedir. Bu sürümde sürüm numarası V 3.10.43.76 şeklindedir ve genellikle Ekim 2020'de kendi kendini güncelleştirme aracılığıyla kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="67de8-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 25 This version has a build number of V 3.10.43.76 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-25"></a><span data-ttu-id="67de8-110">Güncelleştirme Sürümü 25</span><span class="sxs-lookup"><span data-stu-id="67de8-110">Update Release 25</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="67de8-111">Hata düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="67de8-111">Bug fixes</span></span>

<span data-ttu-id="67de8-112">**Zaman ve Gider**</span><span class="sxs-lookup"><span data-stu-id="67de8-112">**Time and Expense**</span></span>

<span data-ttu-id="67de8-113">Aşağıdaki sorun düzeltildi:</span><span class="sxs-lookup"><span data-stu-id="67de8-113">The following issue has been fixed:</span></span>

- <span data-ttu-id="67de8-114">Zaman girişi grafiği çok büyük bir aralığa dayalı olarak daha fazla veri gösteriyor.</span><span class="sxs-lookup"><span data-stu-id="67de8-114">Time entry chart showing additional data based on too large of an interval being retrieved.</span></span>

<span data-ttu-id="67de8-115">**Kaynak Yönetimi**</span><span class="sxs-lookup"><span data-stu-id="67de8-115">**Resource Management**</span></span>

<span data-ttu-id="67de8-116">Aşağıdaki sorun düzeltildi:</span><span class="sxs-lookup"><span data-stu-id="67de8-116">The following issue has been fixed:</span></span>

- <span data-ttu-id="67de8-117">Daha yüksek bir sürüm düzeltme eki zaten varsa, Universal Resource Scheduling düzeltme eki alma işlemini atlamak için paket dağıtıcı kodu eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="67de8-117">Added package deployer code to skip the Universal Resource Scheduling patch import if a higher version patch already exists.</span></span>

<span data-ttu-id="67de8-118">**Proje Yönetimi**</span><span class="sxs-lookup"><span data-stu-id="67de8-118">**Project Management**</span></span>

<span data-ttu-id="67de8-119">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="67de8-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="67de8-120">Düzeltilen yuvarlama ve Döviz Kuru tutarsızlıkları proje izleme ızgarasında yanlış planlanmış maliyete neden olur.</span><span class="sxs-lookup"><span data-stu-id="67de8-120">Corrected rounding and exchange rate discrepancies resulting in incorrect planned cost in the project tracking grid.</span></span>
- <span data-ttu-id="67de8-121">**Proje** formunda iki veya daha fazla yanıt alan gösterimi görüntüleme yeteneğini destekler.</span><span class="sxs-lookup"><span data-stu-id="67de8-121">Support the ability to display two or more react grids on the **Project** form.</span></span>
- <span data-ttu-id="67de8-122">Takvim bitiş tarihinden sonra görev atama yeteneğini ele almak için doğrulama sağlandı, bu da başarısız bir kaynak atamasına neden olacak.</span><span class="sxs-lookup"><span data-stu-id="67de8-122">Provided validation to address the ability to assign a task past the calendar end date, which results in a failed resource assignment.</span></span>
- <span data-ttu-id="67de8-123">Aşağıdaki hatadan dolayı boş başvuru özel durumuna adres olarak geliştirilmiş hata işleme durumu üretildi:</span><span class="sxs-lookup"><span data-stu-id="67de8-123">Improved error handling to address Null Reference Exception generated from the following:</span></span>

    - <span data-ttu-id="67de8-124">**PreValidateProjectTeamMemberCreate** eklentisi</span><span class="sxs-lookup"><span data-stu-id="67de8-124">**PreValidateProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="67de8-125">**PreValidateProjectTaskCreate**, ilişkilendirilen bir proje olmadan bir proje görevi oluşturulduğunda</span><span class="sxs-lookup"><span data-stu-id="67de8-125">**PreValidateProjectTaskCreate** when a project task is created without an associated project</span></span>
    - <span data-ttu-id="67de8-126">**PreProjectTeamMemberCreate** eklentisi</span><span class="sxs-lookup"><span data-stu-id="67de8-126">**PreProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="67de8-127">**PostProjectTeamMemberDelete** eklentisi</span><span class="sxs-lookup"><span data-stu-id="67de8-127">**PostProjectTeamMemberDelete** plug-in</span></span>
    - <span data-ttu-id="67de8-128">**PreValidateProjectTaskDelete** eklentisi</span><span class="sxs-lookup"><span data-stu-id="67de8-128">**PreValidateProjectTaskDelete** plug-in</span></span>

<span data-ttu-id="67de8-129">**Sales**</span><span class="sxs-lookup"><span data-stu-id="67de8-129">**Sales**</span></span>

<span data-ttu-id="67de8-130">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="67de8-130">The following issues have been fixed:</span></span>

- <span data-ttu-id="67de8-131">**Kopyalama Projesi: Yardımcı Kaynağı Yönetimini Tahmin Eder**'den oluşturulan boş başvuru özel durumlarına yönelik olarak geliştirilmiş hata işleme</span><span class="sxs-lookup"><span data-stu-id="67de8-131">Improved error handling to address Null Reference Exceptions generated from **Copy Project: Estimates HelperResource Management**.</span></span>
- <span data-ttu-id="67de8-132">**Zaman ve Malzeme Faturalama Biriktirme listesi** üzerinde **faturalamaya hazır değil** fatura durumunu temizlemez.</span><span class="sxs-lookup"><span data-stu-id="67de8-132">**Not ready to Invoice** on a **Time and Material Billing Backlog** doesn't clear the billing status.</span></span>
- <span data-ttu-id="67de8-133">**Rol fiyatı** ve **Katalog öğeleri** sekmesindeki yanlış etiketli **fiyatlar** düğmeleri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="67de8-133">Corrected mislabeled **Prices** buttons on the **Role Price** and **Catalog Items** tab.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]