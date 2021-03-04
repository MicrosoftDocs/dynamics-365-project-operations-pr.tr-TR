---
title: Proje ilerleme durumu ve maliyet tüketimi
description: Bu konuda, proje ilerleme durumu ve maliyet tüketiminin nasıl izleneceği hakkında bilgiler sağlanmaktadır.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/21/2020
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
ms.openlocfilehash: 0b69cee49e028b98bbb32e4a7e7aedf5479527dc
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148037"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="dcfde-103">Proje ilerleme durumu ve maliyet tüketimi</span><span class="sxs-lookup"><span data-stu-id="dcfde-103">Project progress and cost consumption</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="dcfde-104">Zamanlamaya göre ilerleme durumunun izlenmesi ihtiyacı endüstriye göre değişir.</span><span class="sxs-lookup"><span data-stu-id="dcfde-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="dcfde-105">Bazı endüstriler ayrıntılı düzeyde; diğer endüstrilerse daha yüksek bir düzeyde izler.</span><span class="sxs-lookup"><span data-stu-id="dcfde-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="dcfde-106">Bu konu, kuruluşunuzun gereksinimlerini karşılamak için nasıl zamanlanacağınızı gösterir.</span><span class="sxs-lookup"><span data-stu-id="dcfde-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="dcfde-107">Çalışma izleme görünümü</span><span class="sxs-lookup"><span data-stu-id="dcfde-107">Effort tracking view</span></span>

<span data-ttu-id="dcfde-108">**Çalışma İzleme** görünümü zamanlamadaki görevlerin ilerleme durumunu izler.</span><span class="sxs-lookup"><span data-stu-id="dcfde-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="dcfde-109">Bu, bir görev üzerindeki planlanan saatleri, görevin tamamlanmasına kadar harcanan gerçek saatlerle kıyaslar.</span><span class="sxs-lookup"><span data-stu-id="dcfde-109">It compares the actual effort hours spent on a task to the task's planned effort hours.</span></span> <span data-ttu-id="dcfde-110">Project Service Automation, izleme ölçümlerini hesaplamak için aşağıdaki formülleri kullanır:</span><span class="sxs-lookup"><span data-stu-id="dcfde-110">Project Service Automation uses the following formulas to calculate the tracking metrics:</span></span>

<span data-ttu-id="dcfde-111">Başlangıçta görev oluşturma sırasında: Planlanan maliyet, Tahmini tamamlama maliyeti olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="dcfde-111">Initially on the task creation: Planned cost will be set to the Estimated cost at complete.</span></span> <span data-ttu-id="dcfde-112">Gerçek değerler görevde kaydedildikten sonra, Çaba için İzleme görünümünde aşağıdakiler hesaplanır</span><span class="sxs-lookup"><span data-stu-id="dcfde-112">Once Actuals are recorded on the task, the following will be calculation on the Tracking view for Effort</span></span>

- <span data-ttu-id="dcfde-113">İlerleme yüzdesi = Bugüne kadar harcanan gerçek çalışma süresi ÷ Tahmini tamamlanma (EAC)</span><span class="sxs-lookup"><span data-stu-id="dcfde-113">Progress percentage = Actual effort spent to date ÷ Estimate at complete (EAC)</span></span> 
- <span data-ttu-id="dcfde-114">Tahmini tamamlanma zamanı (ETC) = Tahmini tamamlanma (EAC) – Bugüne kadar harcanan gerçek çalışma süresi</span><span class="sxs-lookup"><span data-stu-id="dcfde-114">Estimate to complete (ETC) = Estimate at complete (EAC)  – Actual effort spent to date</span></span> 
- <span data-ttu-id="dcfde-115">EAC = Kalan çalışma süresi + Bugüne kadar harcanan gerçek çalışma süresi</span><span class="sxs-lookup"><span data-stu-id="dcfde-115">EAC = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="dcfde-116">Öngörülen çalışma farkı = Planlanan çalışma süresi – EAC</span><span class="sxs-lookup"><span data-stu-id="dcfde-116">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="dcfde-117">Project Service Automation, görevdeki çalışma süresi farkının bir projeksiyonunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="dcfde-117">Project Service Automation shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="dcfde-118">EAC planlanan çalışma süresinden daha fazlaysa görevin başlangıçta planlanandan daha fazla zaman alacağı öngörülmektedir.</span><span class="sxs-lookup"><span data-stu-id="dcfde-118">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="dcfde-119">Bu nedenle, zamanlamanın gerisindedir.</span><span class="sxs-lookup"><span data-stu-id="dcfde-119">Therefore, it's behind schedule.</span></span> <span data-ttu-id="dcfde-120">EAC planlanan çalışma süresinden daha az ise görevin başlangıçta planlanandan daha az zaman alacağı öngörülmektedir.</span><span class="sxs-lookup"><span data-stu-id="dcfde-120">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="dcfde-121">Bu nedenle, zamanlamanın ilerisindedir.</span><span class="sxs-lookup"><span data-stu-id="dcfde-121">Therefore, it's ahead of schedule.</span></span>

## <a name="reprojecting-effort"></a><span data-ttu-id="dcfde-122">Çalışmayı yeniden tasarlama</span><span class="sxs-lookup"><span data-stu-id="dcfde-122">Reprojecting effort</span></span>

<span data-ttu-id="dcfde-123">Proje yöneticisinin bir görevdeki özgün tahminleri düzeltmesi yaygın bir uygulamadır.</span><span class="sxs-lookup"><span data-stu-id="dcfde-123">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="dcfde-124">Projelerin tekrar tasarımları, proje yöneticisinin projenin mevcut durumunu göz önüne aldığı tahmin algısıdır.</span><span class="sxs-lookup"><span data-stu-id="dcfde-124">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="dcfde-125">Bununla birlikte, proje yöneticilerinin taban sayılarını değiştirmelerini tavsiye etmeyiz çünkü proje tabanı, projedeki tüm paydaşların kabul ettiği projenin zamanlamasının ve maliyetlerin belirlenmiş tahmini için gerçeğin kaynağıdır.</span><span class="sxs-lookup"><span data-stu-id="dcfde-125">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="dcfde-126">Proje yöneticisinin görevlerdeki çalışmayı yeniden tasarlamasının iki yolu vardır:</span><span class="sxs-lookup"><span data-stu-id="dcfde-126">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="dcfde-127">Görevdeki gerçek kalan çalışmanın yeni bir tahminiyle varsayılan ETC'yi geçersiz kılın.</span><span class="sxs-lookup"><span data-stu-id="dcfde-127">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="dcfde-128">Görevdeki gerçek ilerleme durumunun yeni bir tahminiyle varsayılan ilerleme durumu yüzdesini geçersiz kılın.</span><span class="sxs-lookup"><span data-stu-id="dcfde-128">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="dcfde-129">Bu yaklaşımların her biri görevin ETC, EAC ve ilerleme durumu yüzdesinin yeniden hesaplanmasına ve bir görevde öngörülen çalışma farkına neden olur.</span><span class="sxs-lookup"><span data-stu-id="dcfde-129">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="dcfde-130">EAC, ETC ve özet görevlerindeki ilerleme durumu yüzdesi de yeniden hesaplanır ve yeni bir çalışma farkı projeksiyonu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dcfde-130">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="reprojection-of-effort-on-summary-tasks"></a><span data-ttu-id="dcfde-131">Özet görevlerde çalışmanın yeniden tasarlanması</span><span class="sxs-lookup"><span data-stu-id="dcfde-131">Reprojection of effort on summary tasks</span></span>

<span data-ttu-id="dcfde-132">Özet veya kapsayıcı görevlerdeki çalışmalar yeniden tasarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="dcfde-132">Effort on summary tasks or container tasks can be reprojected.</span></span> <span data-ttu-id="dcfde-133">Kullanıcının, özet görevlerdeki kalan çalışma değerini veya ilerleme durumu yüzdesini kullanarak yeniden tasarım yapmasından bağımsız olarak aşağıdaki hesaplamalar başlar:</span><span class="sxs-lookup"><span data-stu-id="dcfde-133">Regardless of whether the user reprojects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="dcfde-134">Görevdeki EAC, ETC. ve ilerleme durumu yüzdesi hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="dcfde-134">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="dcfde-135">Yeni EAC alt öğe görevlerine, özgün EAC'nin görevde sahip olduğu oranda dağıtılır.</span><span class="sxs-lookup"><span data-stu-id="dcfde-135">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="dcfde-136">Tek tek her görevin yaprak düğüm görevlerine kadar yeni EAC'si hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="dcfde-136">The new EAC on each of the individual tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="dcfde-137">Yaprak düğümlerine kadar etkilenen alt öğe görevleri ETC değerlerine sahiptir ve ilerleme durumu yüzdesi, EAC değerine göre yeniden hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="dcfde-137">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="dcfde-138">Bu, görevin çalışma farkı için yeni bir projeksiyonla sonuçlanır.</span><span class="sxs-lookup"><span data-stu-id="dcfde-138">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="dcfde-139">Özet görevlerden kök düğümlere kadar tüm EAC'ler yeniden hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="dcfde-139">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="dcfde-140">Maliyet izleme görünümü</span><span class="sxs-lookup"><span data-stu-id="dcfde-140">Cost tracking view</span></span> 

<span data-ttu-id="dcfde-141">**Maliyet izleme** görünümü bir göreve harcanan gerçek maliyeti, planlanan maliyetle karşılaştırır.</span><span class="sxs-lookup"><span data-stu-id="dcfde-141">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost.</span></span> 

> [!NOTE]
> <span data-ttu-id="dcfde-142">Bu görünüm yalnızca işçilik maliyetlerini gösterir ve gider tahminlerindeki maliyetleri içermez.</span><span class="sxs-lookup"><span data-stu-id="dcfde-142">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="dcfde-143">Project Service Automation, izleme ölçümlerini hesaplamak için aşağıdaki formülleri kullanır:</span><span class="sxs-lookup"><span data-stu-id="dcfde-143">Project Service Automation uses the following formulas to calculate the tracking metrics:</span></span>

<span data-ttu-id="dcfde-144">Bir görev oluşturulduğunda planlanan maliyet, tahmini tamamlama maliyetine eşittir.</span><span class="sxs-lookup"><span data-stu-id="dcfde-144">When a task is created, the planned cost is equal to the estimated cost at complete.</span></span> <span data-ttu-id="dcfde-145">Gerçek değerler görevde kaydedildikten sonra maliyet için **İzleme** görünümünde aşağıdakiler hesaplanır:</span><span class="sxs-lookup"><span data-stu-id="dcfde-145">After actuals are recorded on the task, the following is calculated on the **Tracking** view for cost:</span></span>

 - <span data-ttu-id="dcfde-146">Tüketilen maliyetin yüzdesi = Bugüne kadar harcanan gerçek maliyet ÷ Görev için tahmini tamamlama maliyeti</span><span class="sxs-lookup"><span data-stu-id="dcfde-146">Percentage of cost consumed = Actual cost spent to date ÷ Estimated cost at complete for the task</span></span>
 - <span data-ttu-id="dcfde-147">Tamamlamak için gereken maliyet (CTC) = Tahmini tamamlama maliyeti – Bugüne kadar harcanan gerçek maliyet</span><span class="sxs-lookup"><span data-stu-id="dcfde-147">Cost to complete (CTC) = Estimated cost at complete – Actual cost spent to date</span></span>
 - <span data-ttu-id="dcfde-148">Tahmini tamamlama maliyeti = CTC + Bugüne kadar harcanan gerçek maliyet</span><span class="sxs-lookup"><span data-stu-id="dcfde-148">Estimated cost at complete = CTC + Actual cost spent to date</span></span>
 - <span data-ttu-id="dcfde-149">Öngörülen maliyet farkı = Planlanan maliyet – Tahmini tamamlama maliyeti</span><span class="sxs-lookup"><span data-stu-id="dcfde-149">Projected cost variance = Planned cost – Estimated cost at complete</span></span>

<span data-ttu-id="dcfde-150">Görevdeki maliyet farkının bir projeksiyonu gösterilir.</span><span class="sxs-lookup"><span data-stu-id="dcfde-150">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="dcfde-151">Tahmini tamamlama maliyeti, planlanan maliyetten daha fazlaysa görevin başlangıçta planlanandan daha maliyetli olacağı öngörülür.</span><span class="sxs-lookup"><span data-stu-id="dcfde-151">If the estimated cost at complete is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="dcfde-152">Bu nedenle, bütçe üzerinde bir trende sahiptir.</span><span class="sxs-lookup"><span data-stu-id="dcfde-152">Therefore, it's trending over budget.</span></span> <span data-ttu-id="dcfde-153">Tahmini tamamlama maliyeti, planlanan maliyetten daha azsa görevin başlangıçta planlanandan daha az maliyetli olacağı ve bütçe altında bir trende sahip olduğu öngörülür.</span><span class="sxs-lookup"><span data-stu-id="dcfde-153">If the Estimated cost at complete is less than the planned cost, the task is projected to cost less than was originally planned and is trending under budget.</span></span>

## <a name="project-managers-reprojection-of-cost"></a><span data-ttu-id="dcfde-154">Proje yöneticisinin maliyeti yeniden tasarlaması</span><span class="sxs-lookup"><span data-stu-id="dcfde-154">Project manager’s reprojection of cost</span></span>

<span data-ttu-id="dcfde-155">Çalışma yeniden tasarlandığında CTC; Tahmini tamamlama maliyeti, tüketilen maliyet yüzdesi ve öngörülen maliyet farkı **Maliyet izleme** görünümünde yeniden hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="dcfde-155">When effort is reprojected, the CTC, Estimated cost at complete, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="dcfde-156">Proje durumu özeti</span><span class="sxs-lookup"><span data-stu-id="dcfde-156">Project status summary</span></span>

<span data-ttu-id="dcfde-157">**Çalışma İzleme** ve **Maliyet izleme** görünümlerindeki verileri izleme proje kök düğümü, özet görevleri ve yaprak düğümü görevleri düzeylerindeki ilerleme durumunu ve maliyet tüketimini gösterir.</span><span class="sxs-lookup"><span data-stu-id="dcfde-157">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="dcfde-158">**Proje varlığı** sayfasındaki **Durum** bölümü, proje düzeyi durumunun bir özetini gösterir.</span><span class="sxs-lookup"><span data-stu-id="dcfde-158">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="dcfde-159">Durum özeti alanları</span><span class="sxs-lookup"><span data-stu-id="dcfde-159">Status summary fields</span></span>

<span data-ttu-id="dcfde-160">İlk olarak **Genel proje durumu** alanı, projenin genel durumunu gösteren düzenlenebilir bir alandır.</span><span class="sxs-lookup"><span data-stu-id="dcfde-160">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="dcfde-161">Artan riski göstermek için yeşil, sarı ve kırmızı gibi renk kodlaması kullanır.</span><span class="sxs-lookup"><span data-stu-id="dcfde-161">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="dcfde-162">İkinci olarak **Yorumlar** alanı, proje yöneticisinin durumla ilgili belirli yorumlar girmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="dcfde-162">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="dcfde-163">**Durum güncelleştirme tarihi** alanı düzenlenemez ve değer, durumun en son güncelleştirildiği tarihi gösteren bir zaman damgasıdır.</span><span class="sxs-lookup"><span data-stu-id="dcfde-163">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="dcfde-164">**Zamanlama performansı** ve **Maliyet performansı** alanları izleme tarihinden itibaren ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="dcfde-164">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="dcfde-165">**Çalışma izleme** görünümündeki kök düğümün zamanlama ve maliyet farkı pozitif olduğunda bu alanları **İleride** olarak ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dcfde-165">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="dcfde-166">Kök düğümün zamanlama ve maliyet farkı negatif olduğunda bunları **Geride** olarak ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dcfde-166">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>
