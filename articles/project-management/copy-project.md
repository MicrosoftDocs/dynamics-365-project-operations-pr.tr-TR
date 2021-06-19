---
title: Proje kopyalama
description: Bu konuda, Dynamics 365 Project Operations'ta projeleri kopyalama hakkında bilgiler sağlanmaktadır.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c3055ab5b8c07faa2bc9167956d283e2a66029dd
ms.sourcegitcommit: 173f2b1f4e063c440a5f78d76d456c62aadbd89e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2021
ms.locfileid: "6091278"
---
# <a name="copy-a-project"></a><span data-ttu-id="ee3c7-103">Projeyi kopyalama</span><span class="sxs-lookup"><span data-stu-id="ee3c7-103">Copy a project</span></span>

<span data-ttu-id="ee3c7-104">_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="ee3c7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ee3c7-105">Dynamics 365 Project Operations ile, **Projeler** formunda **Projeyi Kopyala** seçeneğini belirleyerek hızlıca yeni projeler oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ee3c7-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="ee3c7-106">Bir proje kopyalamak için kopyalamak istediğiniz projeyi açın ve **proje Kopyala** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="ee3c7-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="ee3c7-107">Eylem, aşağıdakileri kopyalayacaktır:</span><span class="sxs-lookup"><span data-stu-id="ee3c7-107">The action will copy the following:</span></span>

- <span data-ttu-id="ee3c7-108">Proje özellikleri</span><span class="sxs-lookup"><span data-stu-id="ee3c7-108">Project properties</span></span> 
- <span data-ttu-id="ee3c7-109">İş kırılım yapısı</span><span class="sxs-lookup"><span data-stu-id="ee3c7-109">Work breakdown structure</span></span>
- <span data-ttu-id="ee3c7-110">Proje takımı üyeleri</span><span class="sxs-lookup"><span data-stu-id="ee3c7-110">Project team members</span></span>
- <span data-ttu-id="ee3c7-111">Proje tahminleri</span><span class="sxs-lookup"><span data-stu-id="ee3c7-111">Project estimates</span></span>
- <span data-ttu-id="ee3c7-112">Proje gider tahminleri</span><span class="sxs-lookup"><span data-stu-id="ee3c7-112">Project expense estimates</span></span>
- <span data-ttu-id="ee3c7-113">Proje malzeme tahminleri</span><span class="sxs-lookup"><span data-stu-id="ee3c7-113">Project material estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="ee3c7-114">Proje özellikleri</span><span class="sxs-lookup"><span data-stu-id="ee3c7-114">Project properties</span></span>

<span data-ttu-id="ee3c7-115">Proje kopyalandığında, aşağıdaki alanlardaki değerler kopyalanır:</span><span class="sxs-lookup"><span data-stu-id="ee3c7-115">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="ee3c7-116">Veri Akışı Adı</span><span class="sxs-lookup"><span data-stu-id="ee3c7-116">Name</span></span>
- <span data-ttu-id="ee3c7-117">Veri Akışı Açıklaması</span><span class="sxs-lookup"><span data-stu-id="ee3c7-117">Description</span></span>
- <span data-ttu-id="ee3c7-118">Müşteri</span><span class="sxs-lookup"><span data-stu-id="ee3c7-118">Customer</span></span>
- <span data-ttu-id="ee3c7-119">Takvim Şablonu</span><span class="sxs-lookup"><span data-stu-id="ee3c7-119">Calendar Template</span></span>
- <span data-ttu-id="ee3c7-120">Para birimi</span><span class="sxs-lookup"><span data-stu-id="ee3c7-120">Currency</span></span>
- <span data-ttu-id="ee3c7-121">Sözleşme Birimi</span><span class="sxs-lookup"><span data-stu-id="ee3c7-121">Contracting Unit</span></span>
- <span data-ttu-id="ee3c7-122">Proje Yöneticisi</span><span class="sxs-lookup"><span data-stu-id="ee3c7-122">Project Manager</span></span>
- <span data-ttu-id="ee3c7-123">Durum</span><span class="sxs-lookup"><span data-stu-id="ee3c7-123">Status</span></span>
- <span data-ttu-id="ee3c7-124">Genel Proje Durumu</span><span class="sxs-lookup"><span data-stu-id="ee3c7-124">Overall Project Status</span></span>
- <span data-ttu-id="ee3c7-125">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="ee3c7-125">Comments</span></span>
- <span data-ttu-id="ee3c7-126">Tahminler</span><span class="sxs-lookup"><span data-stu-id="ee3c7-126">Estimates</span></span>
- <span data-ttu-id="ee3c7-127">Tahmini Başlangıç Tarihi: Bu, projenin kopyadan oluşturulduğu tarihtir.</span><span class="sxs-lookup"><span data-stu-id="ee3c7-127">Estimated Start Date: This is the date that the project is created from the copy.</span></span>
- <span data-ttu-id="ee3c7-128">Tahmini Bitiş Tarihi: Bu tarih, kopyadan oluşturulan yeni projenin başlangıç tarihine göre belirlenir.</span><span class="sxs-lookup"><span data-stu-id="ee3c7-128">Estimated Finish Date: This date is adjusted based on the start date of the new project that was made from the copy.</span></span>
- <span data-ttu-id="ee3c7-129">Çalışma Süresi (Saat)</span><span class="sxs-lookup"><span data-stu-id="ee3c7-129">Effort (Hours)</span></span>
- <span data-ttu-id="ee3c7-130">Tahmini İşçilik Maliyeti</span><span class="sxs-lookup"><span data-stu-id="ee3c7-130">Estimated Labor Cost</span></span>
- <span data-ttu-id="ee3c7-131">Tahmini Gider Maliyeti</span><span class="sxs-lookup"><span data-stu-id="ee3c7-131">Estimated Expense Cost</span></span>
- <span data-ttu-id="ee3c7-132">Tahmini Malzeme Maliyeti</span><span class="sxs-lookup"><span data-stu-id="ee3c7-132">Estimated Material Cost</span></span>

> [!NOTE]
> <span data-ttu-id="ee3c7-133">Projeyi kopyala, uzun süre çalışan bir işlemdir.</span><span class="sxs-lookup"><span data-stu-id="ee3c7-133">Copy project is a long running operation.</span></span> <span data-ttu-id="ee3c7-134">Proje kayıtları, bunların ilgili öznitelikleri ve pek çok ilişkili varlık da kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="ee3c7-134">Project records, their relevant attributes, and many related entities are also copied.</span></span> <span data-ttu-id="ee3c7-135">İşlemin uzun süre çalışması nedeniyle, kopyalama başladıktan sonra hedef proje sayfası kopyalama işlemi tamamlanana kadar düzenleme için kilitlenir.</span><span class="sxs-lookup"><span data-stu-id="ee3c7-135">Because of the long running nature of the operation, after the copy starts, the target project page is locked for editing until the copy operation is complete.</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="ee3c7-136">İş kırılım yapısı</span><span class="sxs-lookup"><span data-stu-id="ee3c7-136">Work breakdown structure</span></span>

<span data-ttu-id="ee3c7-137">Proje kopyalandığında, kaynağı yüklü iş kırılım yapısının tamamı kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="ee3c7-137">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="ee3c7-138">Adlandırılmış kaynaklar, genel kaynaklarla değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="ee3c7-138">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="ee3c7-139">Adlandırılmış kaynaklarda genel kaynakla aynı çalışma saatleri yoksa zamanlama yeniden hesaplanır ve görev süreleri değişebilir.</span><span class="sxs-lookup"><span data-stu-id="ee3c7-139">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="ee3c7-140">Proje takımı üyeleri</span><span class="sxs-lookup"><span data-stu-id="ee3c7-140">Project team members</span></span>

<span data-ttu-id="ee3c7-141">Proje takımı, kaynak projeden kopyalandığında, genel kaynaklar kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="ee3c7-141">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="ee3c7-142">Genel kaynak atamaları da kaynak projede olduğu gibi korunur.</span><span class="sxs-lookup"><span data-stu-id="ee3c7-142">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="ee3c7-143">Adlandırılmış kaynaklar, genel takım üyelerine dönüştürülür.</span><span class="sxs-lookup"><span data-stu-id="ee3c7-143">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="ee3c7-144">Tahminler</span><span class="sxs-lookup"><span data-stu-id="ee3c7-144">Estimates</span></span>

<span data-ttu-id="ee3c7-145">Proje kopyalandığında, kaynak, gider ve malzeme tahmin satırları kaynak projeden kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="ee3c7-145">When the project is copied, resource, expense and material estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="ee3c7-146">Program aracılığıyla uygulamasına yönelik kopyalama projesi hakkında daha fazla bilgi için bkz. [Kopyalama projesi ile proje şablonları geliştirme](dev-copy-project.md).</span><span class="sxs-lookup"><span data-stu-id="ee3c7-146">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
