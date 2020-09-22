---
title: Proje ilerleme durumu ve maliyet tüketimi
description: Bu konu, proje ilerleme durumu ve maliyet tüketiminin nasıl izleneceği hakkında bilgi sağlar.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756694"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="fd681-103">Proje ilerleme durumu ve maliyet tüketimi</span><span class="sxs-lookup"><span data-stu-id="fd681-103">Project progress and cost consumption</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="fd681-104">Zamanlamaya göre ilerleme durumunun izlenmesi ihtiyacı endüstriye göre değişir.</span><span class="sxs-lookup"><span data-stu-id="fd681-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="fd681-105">Bazı endüstriler ayrıntılı düzeyde; diğer endüstrilerse daha yüksek bir düzeyde izler.</span><span class="sxs-lookup"><span data-stu-id="fd681-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="fd681-106">Bu konu, kuruluşunuzun gereksinimlerini karşılamak için nasıl zamanlanacağınızı gösterir.</span><span class="sxs-lookup"><span data-stu-id="fd681-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="fd681-107">Çalışma izleme görünümü</span><span class="sxs-lookup"><span data-stu-id="fd681-107">Effort tracking view</span></span>

<span data-ttu-id="fd681-108">**Çalışma İzleme** görünümü zamanlamadaki görevlerin ilerleme durumunu izler.</span><span class="sxs-lookup"><span data-stu-id="fd681-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="fd681-109">Bu, bir görev için planlanan çalışma saatlerini görev için harcanan gerçek çalışma saatleriyle kıyaslar.</span><span class="sxs-lookup"><span data-stu-id="fd681-109">It compares the actual effort hours that have been spent on a task to the planned effort hours for that task.</span></span> <span data-ttu-id="fd681-110">PSA, izleme ölçümlerini hesaplamak için aşağıdaki formülleri kullanır:</span><span class="sxs-lookup"><span data-stu-id="fd681-110">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="fd681-111">İlerleme yüzdesi = Bugüne kadar harcanan gerçek çalışma süresi ÷ Görev için planlanan çalışma süresi</span><span class="sxs-lookup"><span data-stu-id="fd681-111">Progress percentage = Actual effort spent to date ÷ Planned effort for the task</span></span> 
- <span data-ttu-id="fd681-112">Tahmini tamamlanma zamanı (ETC) = Planlanan çalışma süresi – Bugüne kadar harcanan gerçek çalışma süresi</span><span class="sxs-lookup"><span data-stu-id="fd681-112">Estimate to complete (ETC) = Planned effort – Actual effort spent to date</span></span> 
- <span data-ttu-id="fd681-113">Tahmini tamamlanma zamanı (EAC) = Kalan çalışma süresi + Bugüne kadar harcanan gerçek çalışma süresi</span><span class="sxs-lookup"><span data-stu-id="fd681-113">Estimate at complete (EAC) = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="fd681-114">Öngörülen çalışma farkı = Planlanan çalışma süresi – EAC</span><span class="sxs-lookup"><span data-stu-id="fd681-114">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="fd681-115">PSA, görevdeki çalışma süresi farkının bir projeksiyonunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="fd681-115">PSA shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="fd681-116">EAC planlanan çalışma süresinden daha fazlaysa görevin başlangıçta planlanandan daha fazla zaman alacağı öngörülmektedir.</span><span class="sxs-lookup"><span data-stu-id="fd681-116">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="fd681-117">Bu nedenle, zamanlamanın gerisindedir.</span><span class="sxs-lookup"><span data-stu-id="fd681-117">Therefore, it's behind schedule.</span></span> <span data-ttu-id="fd681-118">EAC planlanan çalışma süresinden daha az ise görevin başlangıçta planlanandan daha az zaman alacağı öngörülmektedir.</span><span class="sxs-lookup"><span data-stu-id="fd681-118">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="fd681-119">Bu nedenle, zamanlamanın ilerisindedir.</span><span class="sxs-lookup"><span data-stu-id="fd681-119">Therefore, it's ahead of schedule.</span></span>

## <a name="re-projecting-effort"></a><span data-ttu-id="fd681-120">Çalışmayı yeniden tasarlama</span><span class="sxs-lookup"><span data-stu-id="fd681-120">Re-projecting effort</span></span>

<span data-ttu-id="fd681-121">Proje yöneticisinin bir görevdeki özgün tahminleri düzeltmesi yaygın bir uygulamadır.</span><span class="sxs-lookup"><span data-stu-id="fd681-121">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="fd681-122">Projelerin tekrar tasarımları, proje yöneticisinin projenin mevcut durumunu göz önüne aldığı tahmin algısıdır.</span><span class="sxs-lookup"><span data-stu-id="fd681-122">Project re-projections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="fd681-123">Bununla birlikte, proje yöneticilerinin taban sayılarını değiştirmelerini tavsiye etmeyiz çünkü proje tabanı, projedeki tüm paydaşların kabul ettiği projenin zamanlamasının ve maliyetlerin belirlenmiş tahmini için gerçeğin kaynağıdır.</span><span class="sxs-lookup"><span data-stu-id="fd681-123">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="fd681-124">Proje yöneticisinin görevlerdeki çalışmayı yeniden tasarlamasının iki yolu vardır:</span><span class="sxs-lookup"><span data-stu-id="fd681-124">There are two ways that a project manager can re-project effort on tasks:</span></span>

- <span data-ttu-id="fd681-125">Görevdeki gerçek kalan çalışmanın yeni bir tahminiyle varsayılan ETC'yi geçersiz kılın.</span><span class="sxs-lookup"><span data-stu-id="fd681-125">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="fd681-126">Görevdeki gerçek ilerleme durumunun yeni bir tahminiyle varsayılan ilerleme durumu yüzdesini geçersiz kılın.</span><span class="sxs-lookup"><span data-stu-id="fd681-126">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="fd681-127">Bu yaklaşımların her biri görevin ETC, EAC ve ilerleme durumu yüzdesinin yeniden hesaplanmasına ve bir görevde öngörülen çalışma farkına neden olur.</span><span class="sxs-lookup"><span data-stu-id="fd681-127">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="fd681-128">EAC, ETC ve özet görevlerindeki ilerleme durumu yüzdesi de yeniden hesaplanır ve yeni bir çalışma farkı projeksiyonu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fd681-128">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="re-projection-of-effort-on-summary-tasks"></a><span data-ttu-id="fd681-129">Özet görevlerde çalışmanın yeniden tasarlanması</span><span class="sxs-lookup"><span data-stu-id="fd681-129">Re-projection of effort on summary tasks</span></span>

<span data-ttu-id="fd681-130">Özet veya kapsayıcı görevlerdeki çalışmalar yeniden tasarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="fd681-130">Effort on summary tasks or container tasks can be re-projected.</span></span> <span data-ttu-id="fd681-131">Kullanıcının, özet görevlerdeki kalan çalışma değerini veya ilerleme durumu yüzdesini kullanarak yeniden tasarım yapmasından bağımsız olarak aşağıdaki hesaplamalar başlar:</span><span class="sxs-lookup"><span data-stu-id="fd681-131">Regardless of whether the user re-projects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="fd681-132">Görevdeki EAC, ETC. ve ilerleme durumu yüzdesi hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="fd681-132">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="fd681-133">Yeni EAC alt öğe görevlerine, özgün EAC'nin görevde sahip olduğu oranda dağıtılır.</span><span class="sxs-lookup"><span data-stu-id="fd681-133">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="fd681-134">Tek tek her görevin yaprak düğüm görevlerine kadar yeni EAC'si hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="fd681-134">The new EAC on each of the individualt tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="fd681-135">Yaprak düğümlerine kadar etkilenen alt öğe görevleri ETC değerlerine sahiptir ve ilerleme durumu yüzdesi, EAC değerine göre yeniden hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="fd681-135">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="fd681-136">Bu, görevin çalışma farkı için yeni bir projeksiyonla sonuçlanır.</span><span class="sxs-lookup"><span data-stu-id="fd681-136">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="fd681-137">Özet görevlerden kök düğümlere kadar tüm EAC'ler yeniden hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="fd681-137">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="fd681-138">Maliyet izleme görünümü</span><span class="sxs-lookup"><span data-stu-id="fd681-138">Cost tracking view</span></span> 

<span data-ttu-id="fd681-139">**Maliyet izleme** görünümü bir göreve harcanan gerçek maliyeti, bir görevin planlanan maliyetiyle karşılaştırır.</span><span class="sxs-lookup"><span data-stu-id="fd681-139">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost on a task.</span></span> 

> [!NOTE]
> <span data-ttu-id="fd681-140">Bu görünüm yalnızca işçilik maliyetlerini gösterir ve gider tahminlerindeki maliyetleri içermez.</span><span class="sxs-lookup"><span data-stu-id="fd681-140">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="fd681-141">PSA, izleme ölçümlerini hesaplamak için aşağıdaki formülleri kullanır:</span><span class="sxs-lookup"><span data-stu-id="fd681-141">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="fd681-142">Tüketilen maliyetin yüzdesi = Bugüne kadar harcanan gerçek maliyet ÷ Görev için planlanan maliyet</span><span class="sxs-lookup"><span data-stu-id="fd681-142">Percentage of cost consumed = Actual cost spent to date ÷ Planned cost for the task</span></span>
- <span data-ttu-id="fd681-143">Tamamlamak için gereken maliyet (CTC) = Planlanan maliyet – Bugüne kadar harcanan gerçek maliyet</span><span class="sxs-lookup"><span data-stu-id="fd681-143">Cost to complete (CTC) = Planned cost – Actual cost spent to date</span></span>
- <span data-ttu-id="fd681-144">EAC = CTC + Bugüne kadar harcanan gerçek maliyet</span><span class="sxs-lookup"><span data-stu-id="fd681-144">EAC = CTC + Actual cost spent to date</span></span>
- <span data-ttu-id="fd681-145">Öngörülen maliyet farkı = Planlanan maliyet – EAC</span><span class="sxs-lookup"><span data-stu-id="fd681-145">Projected cost variance = Planned cost – EAC</span></span>

<span data-ttu-id="fd681-146">Görevdeki maliyet farkının bir projeksiyonu gösterilir.</span><span class="sxs-lookup"><span data-stu-id="fd681-146">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="fd681-147">EAC, planlanan maliyetten daha fazlaysa görevin başlangıçta planlanandan daha maliyetli olacağı öngörülür.</span><span class="sxs-lookup"><span data-stu-id="fd681-147">If the EAC is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="fd681-148">Bu nedenle, bütçe üzerinde bir trende sahiptir.</span><span class="sxs-lookup"><span data-stu-id="fd681-148">Therefore, it's trending over budget.</span></span> <span data-ttu-id="fd681-149">EAC, planlanan maliyetten daha azsa görevin başlangıçta planlanandan daha az maliyetli olacağı öngörülmektedir.</span><span class="sxs-lookup"><span data-stu-id="fd681-149">If the EAC is less than the planned cost, the task is projected to cost less than was originally planned.</span></span> <span data-ttu-id="fd681-150">Bu nedenle, bütçe altında bir trende sahiptir.</span><span class="sxs-lookup"><span data-stu-id="fd681-150">Therefore, it's trending under budget.</span></span>

## <a name="project-managers-re-projection-of-cost"></a><span data-ttu-id="fd681-151">Proje yöneticisinin maliyeti yeniden tasarlaması</span><span class="sxs-lookup"><span data-stu-id="fd681-151">Project manager’s re-projection of cost</span></span>

<span data-ttu-id="fd681-152">Çalışma yeniden tasarlandığında CTC, EAC, tüketilen maliyet yüzdesi ve öngörülen maliyet farkı **Maliyet izleme** görünümünde yeniden hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="fd681-152">When effort is re-projected, the CTC, EAC, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="fd681-153">Proje durumu özeti</span><span class="sxs-lookup"><span data-stu-id="fd681-153">Project status summary</span></span>

<span data-ttu-id="fd681-154">**Çalışma İzleme** ve **Maliyet izleme** görünümlerindeki verileri izleme proje kök düğümü, özet görevleri ve yaprak düğümü görevleri düzeylerindeki ilerleme durumunu ve maliyet tüketimini gösterir.</span><span class="sxs-lookup"><span data-stu-id="fd681-154">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="fd681-155">**Proje varlığı** sayfasındaki **Durum** bölümü, proje düzeyi durumunun bir özetini gösterir.</span><span class="sxs-lookup"><span data-stu-id="fd681-155">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="fd681-156">Durum özeti alanları</span><span class="sxs-lookup"><span data-stu-id="fd681-156">Status summary fields</span></span>

<span data-ttu-id="fd681-157">**Genel proje durumu** alanı, projenin genel durumunu gösteren düzenlenebilir bir alandır.</span><span class="sxs-lookup"><span data-stu-id="fd681-157">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="fd681-158">Artan riski göstermek için yeşil, sarı ve kırmızı gibi renk kodlaması kullanır.</span><span class="sxs-lookup"><span data-stu-id="fd681-158">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="fd681-159">**Yorumlar** alanı, proje yöneticisinin durumla ilgili belirli yorumlar girmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="fd681-159">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="fd681-160">**Durum güncelleştirme tarihi** alanı düzenlenemez ve değer, durumun en son güncelleştirildiği tarihi gösteren bir zaman damgasıdır.</span><span class="sxs-lookup"><span data-stu-id="fd681-160">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="fd681-161">**Zamanlama performansı** ve **Maliyet performansı** alanları izleme tarihinden itibaren ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="fd681-161">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="fd681-162">**Çalışma izleme** görünümündeki kök düğümün zamanlama ve maliyet farkı pozitif olduğunda bu alanları **İleride** olarak ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fd681-162">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="fd681-163">Kök düğümün zamanlama ve maliyet farkı negatif olduğunda bunları **Geride** olarak ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fd681-163">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>
