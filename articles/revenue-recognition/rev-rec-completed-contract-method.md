---
title: Gelir tahminlerini yönetme
description: Bu konu, projelerde gelir tahminleriyle nasıl çalışılacağı hakkında bilgi sağlar.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 98df0301eaa8e9f8e9cd51fc5714254ae3bbc83d
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531579"
---
# <a name="manage-revenue-estimates"></a><span data-ttu-id="a715f-103">Gelir tahminlerini yönetme</span><span class="sxs-lookup"><span data-stu-id="a715f-103">Manage revenue estimates</span></span>

<span data-ttu-id="a715f-104">_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="a715f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="a715f-105">Gelir tahminleri oluşturabilir, hesaplayabilir, deftere nakledebilir, tersine çevirebilir veya ortadan kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a715f-105">You can create, calculate, post, reverse, or eliminate revenue estimates.</span></span> <span data-ttu-id="a715f-106">Bunu el ile veya dönemsel bir işlem kullanarak yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a715f-106">You can do this either manually or by using a periodic process.</span></span> <span data-ttu-id="a715f-107">Bu konu, projelerde gelir tahminleriyle nasıl çalışılacağı hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="a715f-107">This topic provides information about how to work with revenue estimates for projects.</span></span>

### <a name="manage-revenue-estimates-manually"></a><span data-ttu-id="a715f-108">Gelir tahminlerini el ile yönetme</span><span class="sxs-lookup"><span data-stu-id="a715f-108">Manage revenue estimates manually</span></span>

<span data-ttu-id="a715f-109">Sabit fiyat gelir tahmini projesinde veya **Tahmin sorgusu** sayfasında (**Proje yönetimi ve muhasebe** > **Raporlar ve sorgular** > **Tahmin sorguları ve raporlar**) **Tahminler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a715f-109">On the fixed price revenue estimate project or the **Estimate inquiry** page (**Project management and accounting** > **Reports and inquiries** > **Estimates inquiries and reports**), select **Estimates**.</span></span>

### <a name="manage-revenue-estimates-using-a-periodic-process"></a><span data-ttu-id="a715f-110">Gelir tahminlerini dönemsel bir işlem kullanarak yönetme</span><span class="sxs-lookup"><span data-stu-id="a715f-110">Manage revenue estimates using a periodic process</span></span>

<span data-ttu-id="a715f-111">**Proje yönetimi ve muhasebe** > **Dönemsel** > **Tahminler**'e gidin ve ilgili işlemi seçin.</span><span class="sxs-lookup"><span data-stu-id="a715f-111">Go to **Project management and accounting** > **Periodic** > **Estimates** and select the corresponding process.</span></span>

## <a name="create-a-revenue-estimate"></a><span data-ttu-id="a715f-112">Gelir tahmini oluşturma</span><span class="sxs-lookup"><span data-stu-id="a715f-112">Create a revenue estimate</span></span>

<span data-ttu-id="a715f-113">Gelir tahmini oluşturmak için aşağıdaki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="a715f-113">Complete the following steps to create a revenue estimate.</span></span> 

1. <span data-ttu-id="a715f-114">**Proje yönetimi ve muhasebe** > **Dönemsel** > **Tahminler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="a715f-114">Go to **Project management and accounting** > **Periodic** > **Estimates**.</span></span>
2. <span data-ttu-id="a715f-115">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a715f-115">Select **New**.</span></span> <span data-ttu-id="a715f-116">**Tahmin oluşturma** sayfasında, aşağıdaki parametreleri seçin:</span><span class="sxs-lookup"><span data-stu-id="a715f-116">On the **Estimate creation** page, select the following parameters:</span></span>

   - <span data-ttu-id="a715f-117">**Dönem kodu**: Bu kod, tahminlerin hangi sıklıkla deftere nakledildiğini belirler.</span><span class="sxs-lookup"><span data-stu-id="a715f-117">**Period code**: This code determines how frequently estimates are posted.</span></span>
   - <span data-ttu-id="a715f-118">**Tahmin tarihi**: Tahminin işlendiği tarih.</span><span class="sxs-lookup"><span data-stu-id="a715f-118">**Estimate date**: The date the estimate is processed.</span></span>
   - <span data-ttu-id="a715f-119">**Sürekli**: Tahminler yalnızca önceki dönemde deftere nakledilmişse veya tahmin, oluşturulan ilk tahminse tahmin oluşturmak için bu onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="a715f-119">**Continuous**: Select this check box to create estimates only if estimates were posted in the previous period, or if the estimate is the first estimate that has been created.</span></span> <span data-ttu-id="a715f-120">Bu seçilmezse tahminler önceki dönemde deftere nakledilmemiş olsa bile oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="a715f-120">If this is not selected, estimates are created even if estimates were not posted in the previous period.</span></span>
   - <span data-ttu-id="a715f-121">**Tamamlama maliyeti yöntemleri**: Kalan proje çalışmasının nasıl tahmin edileceğini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="a715f-121">**Cost to complete method**: Define how to estimate the remaining project work.</span></span> <span data-ttu-id="a715f-122">Daha fazla bilgi için bkz. [Tamamlama maliyeti yöntemleri](cost-complete-methods.md).</span><span class="sxs-lookup"><span data-stu-id="a715f-122">For more information, see [Cost to complete methods](cost-complete-methods.md).</span></span>
   - <span data-ttu-id="a715f-123">**Tamamlama yöntemi**: Aşağıdaki seçeneklerden bir tamamlama yöntemi seçin:</span><span class="sxs-lookup"><span data-stu-id="a715f-123">**Completion method**: Select a completion method from the following options:</span></span>
     - <span data-ttu-id="a715f-124">**Otomatik**: Tamamlanma yüzdesi otomatik olarak hesaplanır ve hesaplamaya dahil edilen maliyet satırlarına göre belirlenir.</span><span class="sxs-lookup"><span data-stu-id="a715f-124">**Automatic**: The completion percentage is calculated automatically and based on the cost lines included in the calculation.</span></span> <span data-ttu-id="a715f-125">Maliyet şablonu, dahil edilen maliyet satırlarını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="a715f-125">The cost template defines the cost lines that are included.</span></span>
     - <span data-ttu-id="a715f-126">**El ile**: Tamamlanma yüzdesi, son tahminin tamamlanma yüzdesine eşittir.</span><span class="sxs-lookup"><span data-stu-id="a715f-126">**Manual**: The completion percentage equals the completion percentage of the last estimate.</span></span> <span data-ttu-id="a715f-127">Tahmin oluşturulduktan sonra **Tahminler** sayfasındaki **El ile hesaplama**'yı değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a715f-127">After the estimate is created, you can change the **Manual calculation** on the **Estimates** page.</span></span>
     - <span data-ttu-id="a715f-128">**Maliyet şablonundan**: Otomatik ve el ile yöntemlerin bir birleşimdir.</span><span class="sxs-lookup"><span data-stu-id="a715f-128">**From cost template**: A combination of the automatic and manual methods.</span></span> <span data-ttu-id="a715f-129">Bu seçenek, maliyet şablonundaki varsayılan değere bağlı olarak otomatik veya el ile olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="a715f-129">This option is set automatically or manually, depending on the default value in the cost template.</span></span>
   - <span data-ttu-id="a715f-130">**Tahmin modeli**: Tahmin için bir tahmin modeli seçer.</span><span class="sxs-lookup"><span data-stu-id="a715f-130">**Forecast model**: Select a forecast model for the estimate.</span></span>
   - <span data-ttu-id="a715f-131">**Tahmin listesini yazdır**: Bir tahmin listesi oluşturur ve görüntüler.</span><span class="sxs-lookup"><span data-stu-id="a715f-131">**Print estimate list**: Create and show an estimate list.</span></span> <span data-ttu-id="a715f-132">Liste, var olan işlevin durumunu içerir.</span><span class="sxs-lookup"><span data-stu-id="a715f-132">The list contains the status of the current function.</span></span> <span data-ttu-id="a715f-133">Tahminle ilgili her türlü uyarıyı rapora yazdırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a715f-133">You can print any warnings about the estimate on the report.</span></span> <span data-ttu-id="a715f-134">Aşağıdaki koşullar, tahmin listesinde uyarıların görünmesine neden olur:</span><span class="sxs-lookup"><span data-stu-id="a715f-134">The following conditions cause warnings to appear in the estimate list:</span></span>
     - <span data-ttu-id="a715f-135">Yüzde 100'ün üzerinde bir tamamlanma yüzdesi.</span><span class="sxs-lookup"><span data-stu-id="a715f-135">A completion percentage of more than 100 percent.</span></span>
     - <span data-ttu-id="a715f-136">Yüzde sıfırın altında bir tamamlanma yüzdesi.</span><span class="sxs-lookup"><span data-stu-id="a715f-136">A completion percentage less than zero percent.</span></span>
     - <span data-ttu-id="a715f-137">**Tamamlanacak** sütununda negatif bir tutar.</span><span class="sxs-lookup"><span data-stu-id="a715f-137">A negative amount in the **To complete** column.</span></span>
     - <span data-ttu-id="a715f-138">Karşılık gelen sözleşme tutarı olmayan bir tahmin.</span><span class="sxs-lookup"><span data-stu-id="a715f-138">An estimate with no corresponding contract amount.</span></span>
     - <span data-ttu-id="a715f-139">Ekli maliyet tahmini olmayan bir tahmin.</span><span class="sxs-lookup"><span data-stu-id="a715f-139">An estimate with no attached cost estimate.</span></span>
   - <span data-ttu-id="a715f-140">**Bilgi Günlüğünü Göster**: İş çalıştırıldığında işlenen tahmini projeler hakkında bilgi içeren bir ileti almak üzere bu seçeneği belirleyin.</span><span class="sxs-lookup"><span data-stu-id="a715f-140">**Show Infolog**: Select this option to receive a message that contains information about the estimate projects that were processed when the job was run.</span></span>


## <a name="post-wip-or-accruals"></a><span data-ttu-id="a715f-141">WIP veya tahakkukları deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="a715f-141">Post WIP or accruals</span></span>

<span data-ttu-id="a715f-142">Tahminler, değerlendirildikten sonra korunur, azaltılır veya artırılır.</span><span class="sxs-lookup"><span data-stu-id="a715f-142">After the estimates are evaluated, they are maintained, decreased, or increased.</span></span> <span data-ttu-id="a715f-143">Ardından, **Tamamlanan sözleşme** değerlendirme ilkesiyle çalışırken WIP'yi deftere nakledebilir veya **Tamamlanan yüzde** değerlendirme ilkesiyle çalışırken tahakkukları deftere nakledebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a715f-143">You can then post the WIP when you work with the **Completed contract** assessment principle, or post the accruals when you work with the **Completed percentage** assessment principle.</span></span>
  
<span data-ttu-id="a715f-144">Tahmin dönemi durumu **Oluşturuldu**'dan **Gönderildi**'ye değişir.</span><span class="sxs-lookup"><span data-stu-id="a715f-144">The estimate period status changes from **Created** to **Posted**.</span></span>

## <a name="reverse-wip-or-accruals"></a><span data-ttu-id="a715f-145">Tersine WIP veya tahakkuklar</span><span class="sxs-lookup"><span data-stu-id="a715f-145">Reverse WIP or accruals</span></span>

<span data-ttu-id="a715f-146">Önceden deftere nakledilen WIP veya tahakkukların alacak olarak kaydedilmesi için tersine çevir seçeneğini kullanın ve ardından dönem için tahminler oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a715f-146">Use the reverse option to credit already posted WIP or accruals, and then create estimates for the period.</span></span>

> [!NOTE]
> <span data-ttu-id="a715f-147">Diğer dönemler arasındaki bir dönemi tersine çevirmek için gerekli tahmin dönemlerini tersine çevirin ve ardından bunları yeniden deftere nakledin.</span><span class="sxs-lookup"><span data-stu-id="a715f-147">To reverse a period that is in between other periods, reverse the necessary estimate periods and then repost them.</span></span> <span data-ttu-id="a715f-148">Sonraki tüm dönemler, önceki dönemin tahminlerine bağlı olduğundan herhangi bir dönemi atlamayın.</span><span class="sxs-lookup"><span data-stu-id="a715f-148">Because all subsequent periods depend on the estimates from the previous period, don't skip any periods.</span></span>

## <a name="eliminate-the-estimate-project-and-finish-the-project"></a><span data-ttu-id="a715f-149">Tahmini projeyi ortadan kaldırma ve projeyi bitirme</span><span class="sxs-lookup"><span data-stu-id="a715f-149">Eliminate the estimate project and finish the project</span></span>

<span data-ttu-id="a715f-150">Tahmin işlemindeki son adım, tahmini projeyi ortadan kaldırmak ve tamamlanma yüzdesi yüzde 100'e ulaştığında sabit fiyatlı projeyi sonlandırmaktır.</span><span class="sxs-lookup"><span data-stu-id="a715f-150">The final step in the estimate process is to eliminate the estimate project and end the fixed price project when the percentage of completion reaches 100 percent.</span></span>

<span data-ttu-id="a715f-151">Ortadan kaldırmayı çalıştırdığınızda aşağıdakiler gerçekleşir:</span><span class="sxs-lookup"><span data-stu-id="a715f-151">The following occurs when you run the elimination:</span></span>

- <span data-ttu-id="a715f-152">Tamamlanmış bir sözleşmeye sahip sabit fiyatlı bir proje için WIP değerleri bakiye hesaplarından silinir ve kar ve zarar hesaplarına nakledilir.</span><span class="sxs-lookup"><span data-stu-id="a715f-152">For a fixed price project with a completed contract, the WIP values clear from the balance accounts and post to the profit and loss accounts.</span></span>
- <span data-ttu-id="a715f-153">Tamamlanmış bir yüzdeye sahip sabit fiyatlı bir proje için tahakkuklar, kar ve zarar hesaplarından kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="a715f-153">For a fixed-price project with a completed percentage, the accruals are removed from the profit and loss accounts.</span></span>

<span data-ttu-id="a715f-154">Tahmin, durumu **Kaldırıldı** olarak değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a715f-154">The estimate changes the status to **Eliminated**.</span></span>

> [!NOTE]
> <span data-ttu-id="a715f-155">Özel durumlarda yüzde, yüzde 100'ün üzerine çıkabilir.</span><span class="sxs-lookup"><span data-stu-id="a715f-155">In special cases, the percentage can extend beyond 100 percent.</span></span> <span data-ttu-id="a715f-156">Böyle bir durumda, yüzde 100'e ulaşmak için **Tamamlama maliyetini sıfıra ayarlama yöntemi**'ni kullanarak tamamlanma yüzdesini azaltın.</span><span class="sxs-lookup"><span data-stu-id="a715f-156">When this happens, reduce the percentage of completion by using the **Set cost to complete to zero method** to reach 100 percent.</span></span>

## <a name="reverse-elimination"></a><span data-ttu-id="a715f-157">Elemeyi tersine çevirme</span><span class="sxs-lookup"><span data-stu-id="a715f-157">Reverse elimination</span></span>

1. <span data-ttu-id="a715f-158">**Proje yönetimi ve muhasebe** > **Dönemsel** > **Tahminler** > **Elemeyi tersine çevirme**'ye gidin.</span><span class="sxs-lookup"><span data-stu-id="a715f-158">Go to **Project management and accounting** > **Periodic** > **Estimates** > **Reverse elimination**.</span></span> 
2. <span data-ttu-id="a715f-159">Eylem Bölmesinde, **İşlem** sekmesindeki **Koru** grubunda **Tahmin**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a715f-159">On the Action Pane, on the **Process** tab, in the **Maintain** group, select **Estimate**.</span></span> 
3. <span data-ttu-id="a715f-160">**Elemeyi tersine çevir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a715f-160">Select **Reverse elimination**.</span></span>

<span data-ttu-id="a715f-161">Tüm elemeleri belirli bir tahmin tarihi ve **Elendi** tahmin durumuyla tersine çevirmek için bu sayfayı kullanın.</span><span class="sxs-lookup"><span data-stu-id="a715f-161">Use this page to reverse all eliminations with a specified estimate date and with an estimate status of **Eliminated**.</span></span> <span data-ttu-id="a715f-162">Uygun alanları seçmeniz sonrasında işlem durumu değişir.</span><span class="sxs-lookup"><span data-stu-id="a715f-162">The transaction status changes after you select the appropriate fields.</span></span>

<span data-ttu-id="a715f-163">Bu, proje aşaması bitmiş olarak ayarlanmışsa proje durumunu otomatik olarak **Devam ediyor** olarak değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a715f-163">This also automatically changes the project status to **In process** if the project stage is set to finished.</span></span> <span data-ttu-id="a715f-164">Proje döneminin tahmin durumu **Gönderildi** olarak değişir.</span><span class="sxs-lookup"><span data-stu-id="a715f-164">The estimate status of the project period changes back to **Posted**.</span></span>
