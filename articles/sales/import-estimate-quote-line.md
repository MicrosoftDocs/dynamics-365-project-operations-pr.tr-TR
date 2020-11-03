---
title: Proje için tahminleri proje tabanlı teklif satırına içe aktarma
description: Bu konuda, tahminleri projeden teklif satırına içe aktarma hakkında bilgiler sağlanmaktadır.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8c0fe18b33207f73848709b99334f64aadc7867a
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086240"
---
# <a name="import-estimates-for-a-project-to-a-project-based-quote-line"></a><span data-ttu-id="f6891-103">Proje için tahminleri proje tabanlı teklif satırına içe aktarma</span><span class="sxs-lookup"><span data-stu-id="f6891-103">Import estimates for a project to a project-based quote line</span></span>

<span data-ttu-id="f6891-104">_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="f6891-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="f6891-105">Projenin satış öncesi aşama sırasında oluşturulması durumunda mali tahmini, projeden proje tabanlı teklif satırına içe aktarmayı seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f6891-105">If a project is created during the pre-sales stage, you can select to import the financial estimate from the project to the project-based quote line.</span></span>

1. <span data-ttu-id="f6891-106">Proje tabanlı teklif satırının **Proje** alanında proje bilgilerine sahip olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="f6891-106">Make sure that the project-based quote line has the project information in the **Project** field.</span></span>
2. <span data-ttu-id="f6891-107">**Teklif satırı ayrıntıları** sekmesinde, **Proje Tahmininden İçe Aktar** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f6891-107">On the **Quote line details** tab, select **Import from Project Estimation**.</span></span>
3. <span data-ttu-id="f6891-108">İletişim sayfası açıldığında, aşağıdaki özetleme seçeneklerinden birini belirleyin:</span><span class="sxs-lookup"><span data-stu-id="f6891-108">On the dialog page opens, select one of the following summarization options:</span></span>

  - <span data-ttu-id="f6891-109">**İşlem sınıfı**</span><span class="sxs-lookup"><span data-stu-id="f6891-109">**Transaction class**</span></span>
  - <span data-ttu-id="f6891-110">**Kategori**</span><span class="sxs-lookup"><span data-stu-id="f6891-110">**Category**</span></span>
  - <span data-ttu-id="f6891-111">**Rol**</span><span class="sxs-lookup"><span data-stu-id="f6891-111">**Role**</span></span> 
  - <span data-ttu-id="f6891-112">**Proje görevi**</span><span class="sxs-lookup"><span data-stu-id="f6891-112">**Project task**</span></span>

<span data-ttu-id="f6891-113">Seçiminize bağlı olarak, bu teklif satırındaki tüm işlem sınıfları için projeden alınan tahmin, üzerine kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="f6891-113">Based on your selection, the estimate from the project for all transaction classes included on this quote line are copied over.</span></span> <span data-ttu-id="f6891-114">Hangi işlem sınıflarının eklendiğini denetlemek için proje tabanlı teklif satırında **Genel** sekmesini seçin ve **Zaman Ekle** , **Gider Ekle** ve **Ücret Ekle** değerlerini kontrol edin.</span><span class="sxs-lookup"><span data-stu-id="f6891-114">To check what transaction classes are included, select the **General** tab on the project-based quote line, and check the values for **Include Time** , **Include Expenses** , and **Include Fees**.</span></span>

<span data-ttu-id="f6891-115">Tahminleri içe aktardığınızda sistem, fiyatlandırmayı proje tabanlı teklif satırında ayarlanan teklife ve faturalama türüne eklenen proje fiyat listelerine bağlı olarak varsayılan yapar.</span><span class="sxs-lookup"><span data-stu-id="f6891-115">When you import estimates, the system will default pricing based on the project price lists attached to the quote and the billing type set up on the project-based quote line.</span></span> <span data-ttu-id="f6891-116">Proje tabanlı teklif satırında bir rol veya kategori borçlandırılamaz olarak ayarlanırsa içe aktarılan tahmin satırı borçlandırılamaz olarak ayarlanır ve teklif satırının teklif değerine eklenmez.</span><span class="sxs-lookup"><span data-stu-id="f6891-116">If a role or category is set up on the project-based quote line as non-chargeable, the imported estimate line will set as non-chargeable and won't add up to the quoted value of quote line.</span></span>

<span data-ttu-id="f6891-117">Teklif satırında satır ayrıntıları bulunduğunda, teklif satırındaki **Teklif Değeri** ve **Tahmini Vergi** alanları özetlenir ve düzenlenemez.</span><span class="sxs-lookup"><span data-stu-id="f6891-117">When a quote line has line details, the **Quote Value** and the **Estimated Tax** fields on the quote line are summarized and can't be edited.</span></span>

<span data-ttu-id="f6891-118">Birden çok özet seçeneği belirlendiğinde sistem, seçilen tüm seçeneklere göre özetlemeye çalışır.</span><span class="sxs-lookup"><span data-stu-id="f6891-118">When multiple summarization options are selected, the system attempts to summarize by all selected options.</span></span> <span data-ttu-id="f6891-119">Bu, içe aktarılan teklif satırlarının çıktısının yalnızca bir özetleme seçeneği belirlemenizden daha fazlası olacağı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="f6891-119">The result is that the output of imported quote lines will be more than if you selected only one summarization option.</span></span>

<span data-ttu-id="f6891-120">Örneğin, projede giderler için aşağıdaki tahmin satırları varsa.</span><span class="sxs-lookup"><span data-stu-id="f6891-120">For example, if the project has the following estimate lines for expenses.</span></span>

| <span data-ttu-id="f6891-121">Görev</span><span class="sxs-lookup"><span data-stu-id="f6891-121">Task</span></span> | <span data-ttu-id="f6891-122">Kategori</span><span class="sxs-lookup"><span data-stu-id="f6891-122">Category</span></span> | <span data-ttu-id="f6891-123">Tarih</span><span class="sxs-lookup"><span data-stu-id="f6891-123">Date</span></span> | <span data-ttu-id="f6891-124">Miktar</span><span class="sxs-lookup"><span data-stu-id="f6891-124">Quantity</span></span> | <span data-ttu-id="f6891-125">Birim fiyatı</span><span class="sxs-lookup"><span data-stu-id="f6891-125">Unit price</span></span> | <span data-ttu-id="f6891-126">Miktar</span><span class="sxs-lookup"><span data-stu-id="f6891-126">Amount</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="f6891-127">A Görevi</span><span class="sxs-lookup"><span data-stu-id="f6891-127">Task A</span></span> | <span data-ttu-id="f6891-128">Uçak bileti ücreti</span><span class="sxs-lookup"><span data-stu-id="f6891-128">Airfare</span></span> | <span data-ttu-id="f6891-129">1.10.2020</span><span class="sxs-lookup"><span data-stu-id="f6891-129">10/1/2020</span></span> | <span data-ttu-id="f6891-130">4</span><span class="sxs-lookup"><span data-stu-id="f6891-130">4</span></span> | <span data-ttu-id="f6891-131">400</span><span class="sxs-lookup"><span data-stu-id="f6891-131">400</span></span> | <span data-ttu-id="f6891-132">1600</span><span class="sxs-lookup"><span data-stu-id="f6891-132">1600</span></span> |
| <span data-ttu-id="f6891-133">B Görevi</span><span class="sxs-lookup"><span data-stu-id="f6891-133">Task B</span></span> | <span data-ttu-id="f6891-134">Otel</span><span class="sxs-lookup"><span data-stu-id="f6891-134">Hotel</span></span> | <span data-ttu-id="f6891-135">1.10.2020</span><span class="sxs-lookup"><span data-stu-id="f6891-135">10/1/2020</span></span> | <span data-ttu-id="f6891-136">4</span><span class="sxs-lookup"><span data-stu-id="f6891-136">4</span></span> | <span data-ttu-id="f6891-137">200</span><span class="sxs-lookup"><span data-stu-id="f6891-137">200</span></span> | <span data-ttu-id="f6891-138">800</span><span class="sxs-lookup"><span data-stu-id="f6891-138">800</span></span> |
| <span data-ttu-id="f6891-139">C Görevi</span><span class="sxs-lookup"><span data-stu-id="f6891-139">Task C</span></span> | <span data-ttu-id="f6891-140">Otel</span><span class="sxs-lookup"><span data-stu-id="f6891-140">Hotel</span></span> | <span data-ttu-id="f6891-141">1.11.2020</span><span class="sxs-lookup"><span data-stu-id="f6891-141">11/1/2020</span></span> | <span data-ttu-id="f6891-142">2</span><span class="sxs-lookup"><span data-stu-id="f6891-142">2</span></span> | <span data-ttu-id="f6891-143">200</span><span class="sxs-lookup"><span data-stu-id="f6891-143">200</span></span> | <span data-ttu-id="f6891-144">400</span><span class="sxs-lookup"><span data-stu-id="f6891-144">400</span></span> |

<span data-ttu-id="f6891-145">Kullanıcı, İşlem sınıfına göre özetlemeyi seçtiğinde, aşağıdaki bilgiler içe aktarılır.</span><span class="sxs-lookup"><span data-stu-id="f6891-145">When the user selects to summarize by Transaction class, the following information will be imported.</span></span>

| <span data-ttu-id="f6891-146">Görev</span><span class="sxs-lookup"><span data-stu-id="f6891-146">Task</span></span> | <span data-ttu-id="f6891-147">Kategori</span><span class="sxs-lookup"><span data-stu-id="f6891-147">Category</span></span> | <span data-ttu-id="f6891-148">Tarih</span><span class="sxs-lookup"><span data-stu-id="f6891-148">Date</span></span> | <span data-ttu-id="f6891-149">Miktar</span><span class="sxs-lookup"><span data-stu-id="f6891-149">Quantity</span></span> | <span data-ttu-id="f6891-150">Birim fiyatı</span><span class="sxs-lookup"><span data-stu-id="f6891-150">Unit price</span></span> | <span data-ttu-id="f6891-151">Miktar</span><span class="sxs-lookup"><span data-stu-id="f6891-151">Amount</span></span> |
| --- | --- | --- | --- | --- | --- |
| | | <span data-ttu-id="f6891-152">1.10.2020</span><span class="sxs-lookup"><span data-stu-id="f6891-152">10/1/2020</span></span> | <span data-ttu-id="f6891-153">3.34</span><span class="sxs-lookup"><span data-stu-id="f6891-153">3.34</span></span> | <span data-ttu-id="f6891-154">840</span><span class="sxs-lookup"><span data-stu-id="f6891-154">840</span></span> | <span data-ttu-id="f6891-155">2800</span><span class="sxs-lookup"><span data-stu-id="f6891-155">2800</span></span> |

<span data-ttu-id="f6891-156">Kullanıcı, İşlem sınıfı ve Kategoriye göre özetlemeyi seçtiğinde, aşağıdaki bilgiler içe aktarılır.</span><span class="sxs-lookup"><span data-stu-id="f6891-156">When the user selects to summarize by Transaction class and Category, the following information will be imported.</span></span>

| <span data-ttu-id="f6891-157">Görev</span><span class="sxs-lookup"><span data-stu-id="f6891-157">Task</span></span> | <span data-ttu-id="f6891-158">Kategori</span><span class="sxs-lookup"><span data-stu-id="f6891-158">Category</span></span> | <span data-ttu-id="f6891-159">Tarih</span><span class="sxs-lookup"><span data-stu-id="f6891-159">Date</span></span> | <span data-ttu-id="f6891-160">Miktar</span><span class="sxs-lookup"><span data-stu-id="f6891-160">Quantity</span></span> | <span data-ttu-id="f6891-161">Birim fiyatı</span><span class="sxs-lookup"><span data-stu-id="f6891-161">Unit price</span></span> | <span data-ttu-id="f6891-162">Miktar</span><span class="sxs-lookup"><span data-stu-id="f6891-162">Amount</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="f6891-163">A Görevi</span><span class="sxs-lookup"><span data-stu-id="f6891-163">Task A</span></span> | <span data-ttu-id="f6891-164">Uçak bileti ücreti</span><span class="sxs-lookup"><span data-stu-id="f6891-164">Airfare</span></span> | <span data-ttu-id="f6891-165">1.10.2020</span><span class="sxs-lookup"><span data-stu-id="f6891-165">10/1/2020</span></span> | <span data-ttu-id="f6891-166">4</span><span class="sxs-lookup"><span data-stu-id="f6891-166">4</span></span> | <span data-ttu-id="f6891-167">400</span><span class="sxs-lookup"><span data-stu-id="f6891-167">400</span></span> | <span data-ttu-id="f6891-168">1600</span><span class="sxs-lookup"><span data-stu-id="f6891-168">1600</span></span> |
| | <span data-ttu-id="f6891-169">Otel</span><span class="sxs-lookup"><span data-stu-id="f6891-169">Hotel</span></span> | <span data-ttu-id="f6891-170">1.10.2020</span><span class="sxs-lookup"><span data-stu-id="f6891-170">10/1/2020</span></span> | <span data-ttu-id="f6891-171">6</span><span class="sxs-lookup"><span data-stu-id="f6891-171">6</span></span> | <span data-ttu-id="f6891-172">200</span><span class="sxs-lookup"><span data-stu-id="f6891-172">200</span></span> | <span data-ttu-id="f6891-173">1200</span><span class="sxs-lookup"><span data-stu-id="f6891-173">1200</span></span> |

<span data-ttu-id="f6891-174">Kullanıcı, İşlem sınıfı, Kategori ve Yaprak Düğüm Görevine göre özetlemeyi seçtiğinde, aşağıdaki bilgiler içe aktarılır.</span><span class="sxs-lookup"><span data-stu-id="f6891-174">When the user selects to summarize by Transaction class, Category, and Leaf Node Task, the following information will be imported.</span></span> <span data-ttu-id="f6891-175">Bu sonucun, projedeki sonuçla aynı olduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="f6891-175">Notice that this result is the same as what was on the project.</span></span>

| <span data-ttu-id="f6891-176">Görev</span><span class="sxs-lookup"><span data-stu-id="f6891-176">Task</span></span> | <span data-ttu-id="f6891-177">Kategori</span><span class="sxs-lookup"><span data-stu-id="f6891-177">Category</span></span> | <span data-ttu-id="f6891-178">Tarih</span><span class="sxs-lookup"><span data-stu-id="f6891-178">Date</span></span> | <span data-ttu-id="f6891-179">Miktar</span><span class="sxs-lookup"><span data-stu-id="f6891-179">Quantity</span></span> | <span data-ttu-id="f6891-180">Birim fiyatı</span><span class="sxs-lookup"><span data-stu-id="f6891-180">Unit price</span></span> | <span data-ttu-id="f6891-181">Miktar</span><span class="sxs-lookup"><span data-stu-id="f6891-181">Amount</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="f6891-182">A Görevi</span><span class="sxs-lookup"><span data-stu-id="f6891-182">Task A</span></span> | <span data-ttu-id="f6891-183">Uçak bileti ücreti</span><span class="sxs-lookup"><span data-stu-id="f6891-183">Airfare</span></span> | <span data-ttu-id="f6891-184">1.10.2020</span><span class="sxs-lookup"><span data-stu-id="f6891-184">10/1/2020</span></span> | <span data-ttu-id="f6891-185">4</span><span class="sxs-lookup"><span data-stu-id="f6891-185">4</span></span> | <span data-ttu-id="f6891-186">400</span><span class="sxs-lookup"><span data-stu-id="f6891-186">400</span></span> | <span data-ttu-id="f6891-187">1600</span><span class="sxs-lookup"><span data-stu-id="f6891-187">1600</span></span> |
| <span data-ttu-id="f6891-188">B Görevi</span><span class="sxs-lookup"><span data-stu-id="f6891-188">Task B</span></span> | <span data-ttu-id="f6891-189">Otel</span><span class="sxs-lookup"><span data-stu-id="f6891-189">Hotel</span></span> | <span data-ttu-id="f6891-190">1.10.2020</span><span class="sxs-lookup"><span data-stu-id="f6891-190">10/1/2020</span></span> | <span data-ttu-id="f6891-191">4</span><span class="sxs-lookup"><span data-stu-id="f6891-191">4</span></span> | <span data-ttu-id="f6891-192">200</span><span class="sxs-lookup"><span data-stu-id="f6891-192">200</span></span> | <span data-ttu-id="f6891-193">800</span><span class="sxs-lookup"><span data-stu-id="f6891-193">800</span></span> |
| <span data-ttu-id="f6891-194">C Görevi</span><span class="sxs-lookup"><span data-stu-id="f6891-194">Task C</span></span> | <span data-ttu-id="f6891-195">Otel</span><span class="sxs-lookup"><span data-stu-id="f6891-195">Hotel</span></span> | <span data-ttu-id="f6891-196">1.11.2020</span><span class="sxs-lookup"><span data-stu-id="f6891-196">11/1/2020</span></span> | <span data-ttu-id="f6891-197">2</span><span class="sxs-lookup"><span data-stu-id="f6891-197">2</span></span> | <span data-ttu-id="f6891-198">200</span><span class="sxs-lookup"><span data-stu-id="f6891-198">200</span></span> | <span data-ttu-id="f6891-199">400</span><span class="sxs-lookup"><span data-stu-id="f6891-199">400</span></span> |