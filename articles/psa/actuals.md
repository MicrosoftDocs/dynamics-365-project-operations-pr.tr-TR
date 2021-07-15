---
title: Gerçek değerlere genel bakış
description: Bu konu proje fiili değerleri hakkında bilgi sağlar.
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: cbb3e5c7f74cdf37ae4d259687bf7a98102a8131
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368185"
---
# <a name="actuals-overview"></a><span data-ttu-id="835d5-103">Gerçek değerlere genel bakış</span><span class="sxs-lookup"><span data-stu-id="835d5-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="835d5-104">Fiili değerler, bir projeki tamamlanmış iş tutarıdır.</span><span class="sxs-lookup"><span data-stu-id="835d5-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="835d5-105">Proje fiili değerleri, kaynak belgelerine doğru izlenebilir.</span><span class="sxs-lookup"><span data-stu-id="835d5-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="835d5-106">Bu kaynak belgeler arasında zaman, gider, günlük girişleri ve ayrıca faturalar vardır.</span><span class="sxs-lookup"><span data-stu-id="835d5-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Proje fiili değerlerini kaynak belgelerde izleme](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="835d5-108">Bir zaman girişi gönderme</span><span class="sxs-lookup"><span data-stu-id="835d5-108">Submitting a time entry</span></span>

<span data-ttu-id="835d5-109">PSA'da, zaman ve malzemeler sözleşmesi satırıyla eşlenen bir proje için bir zaman girişi gönderildiğinde iki günlük satırı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="835d5-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="835d5-110">Bir satır maliyet için ve diğer satır faturalanmamış satış içindir.</span><span class="sxs-lookup"><span data-stu-id="835d5-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="835d5-111">Sabit fiyat sözleşme satırıyla eşlenen bir proje için bir zaman girişi gönderildiğinde yalnızca maliyet için bir günlük satırı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="835d5-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="835d5-112">Varsayılan fiyatların girileceği mantık günlük satırında yer alır.</span><span class="sxs-lookup"><span data-stu-id="835d5-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="835d5-113">Bir zaman girişindeki tüm alan değerleri günlük satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="835d5-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="835d5-114">Bu alanlar işlemin tarihini, projenin eşlendiği sözleşme satırını ve ilgili fiyat listesindeki para birimi sonucunu içerir.</span><span class="sxs-lookup"><span data-stu-id="835d5-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="835d5-115">**Rol** ve **Kuruluş Birimi** gibi varsayılan fiyatları etkileyen alanlar, günlük satırında varsayılan olarak uygun bir fiyatın girilmesine neden olur.</span><span class="sxs-lookup"><span data-stu-id="835d5-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="835d5-116">Zaman girişine bir özel alan ekler ve alan değerinin fiili değerlere yayılmasını isterseniz, alanı Fiili değerler varlığında oluşturun ve alanı zaman girişinden fiili değere kopyalamak için alan eşlemelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="835d5-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="835d5-117">Gider girişi gönderme</span><span class="sxs-lookup"><span data-stu-id="835d5-117">Submitting an expense entry</span></span>

<span data-ttu-id="835d5-118">PSA'da, zaman ve malzemeler sözleşmesi satırıyla eşlenen bir proje için bir gider girişi gönderildiğinde iki günlük satırı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="835d5-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="835d5-119">Bir satır maliyet için ve diğer satır faturalanmamış satış içindir.</span><span class="sxs-lookup"><span data-stu-id="835d5-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="835d5-120">Sabit fiyat sözleşme satırıyla eşlenen bir proje için bir gider girişi gönderildiğinde yalnızca maliyet için bir günlük satırı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="835d5-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="835d5-121">Giderler için varsayılan fiyatları girme mantığı **Gider girişi** sayfasında seçilen gider kategorisine dayanır.</span><span class="sxs-lookup"><span data-stu-id="835d5-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="835d5-122">İşlemin tarihini, projenin eşlendiği sözleşme satırı ve ilgili fiyat listesindeki para birimi sonucu uygun fiyat listesini belirlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="835d5-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="835d5-123">Ancak, fiyatın kendisi için, kullanıcının girdiği tutar varsayılan olarak maliyet ve satışlar için ilgili gider günlüğü satırlarında doğrudan ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="835d5-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="835d5-124">Geçerli PSA sürümünde, gider girişlerinde birim başına varsayılan fiyatların kategori tabanlı girişi kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="835d5-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="835d5-125">Maliyetleri kaydetmek için Giriş günlükleri kullanma</span><span class="sxs-lookup"><span data-stu-id="835d5-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="835d5-126">PSA'da Giriş günlükler malzeme, ücret, zaman, masraf veya vergi işlemi sınıflarında maliyeti veya geliri kaydetmenize olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="835d5-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="835d5-127">Bir günlükte başlık, satırlar ve **Onayla** eylemi vardır.</span><span class="sxs-lookup"><span data-stu-id="835d5-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="835d5-128">Aşağıda bir günlüğü kullanabileceğiniz bazı senaryolar vardır:</span><span class="sxs-lookup"><span data-stu-id="835d5-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="835d5-129">Bir projedeki malzeme fiili maliyetlerini ve satışları kaydetmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="835d5-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="835d5-130">İşlem fiili değerlerini başka bir sistemden PSA'ya taşımanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="835d5-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="835d5-131">Başka bir sistemde gerçekleşen (örneğin, tedarik veya taşeron maliyetleri) maliyetleri kaydetmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="835d5-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="835d5-132">Fiili değerler oluşturmak için Giriş günlüklerinin kullanılması, yalnızca, fiili değerlerin projede sahip olduğu muhasebe etkisini tam olarak algılayan bir kullanıcı tarafından gerçekleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="835d5-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="835d5-133">Bunun nedeni, uygulamanın yevmiye defteri satırı türünü veya yevmiye defteri satırına girilen ilgili fiyatlandırmayı doğrulamaması nedeniyle oluşur.</span><span class="sxs-lookup"><span data-stu-id="835d5-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="835d5-134">Bu günlük türünün etkisi nedeniyle, giriş günlükleri oluşturmak için kimlerin erişim sahibi olduğu konusunda uygun bir dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="835d5-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="835d5-135">Proje olaylarına göre fiili değerleri kaydetme</span><span class="sxs-lookup"><span data-stu-id="835d5-135">Recording actuals based on project events</span></span>

<span data-ttu-id="835d5-136">PSA bir proje sırasında gerçekleşen mali işlemleri kaydeder.</span><span class="sxs-lookup"><span data-stu-id="835d5-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="835d5-137">Bu işlemler **fiili değerler** olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="835d5-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="835d5-138">Aşağıdaki tablolar, projenin zaman ve malzeme veya sabit fiyatlı proje olmasına, ön satış aşamasında bulunmasına veya dahili bir proje olmasına bağlı olarak oluşturulan farklı fiili değer türlerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="835d5-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="835d5-139">**Kaynak, projenin sözleşme birimiyle aynı kuruluş birimine aittir.**</span><span class="sxs-lookup"><span data-stu-id="835d5-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="835d5-140">Olay</span><span class="sxs-lookup"><span data-stu-id="835d5-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="835d5-141">Faturalandırılabilir veya satılmış proje</span><span class="sxs-lookup"><span data-stu-id="835d5-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="835d5-142">Ön satış aşamasındaki proje</span><span class="sxs-lookup"><span data-stu-id="835d5-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="835d5-143">Dahili proje</span><span class="sxs-lookup"><span data-stu-id="835d5-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="835d5-144">Zaman ve malzemeler</span><span class="sxs-lookup"><span data-stu-id="835d5-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="835d5-145">Sabit fiyat</span><span class="sxs-lookup"><span data-stu-id="835d5-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="835d5-146">Gerçekler</span><span class="sxs-lookup"><span data-stu-id="835d5-146">Actuals</span></span></th>
<th><span data-ttu-id="835d5-147">İşlem para birimi</span><span class="sxs-lookup"><span data-stu-id="835d5-147">Transaction currency</span></span></th>
<th><span data-ttu-id="835d5-148">Sabit fiyat</span><span class="sxs-lookup"><span data-stu-id="835d5-148">Fixed price</span></span></th>
<th><span data-ttu-id="835d5-149">İşlem para birimi</span><span class="sxs-lookup"><span data-stu-id="835d5-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="835d5-150">Bir zaman girişi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="835d5-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="835d5-151">Fiili değerler varlığında etkinlik yok</span><span class="sxs-lookup"><span data-stu-id="835d5-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="835d5-152">Bir zaman girişi gönderilir.</span><span class="sxs-lookup"><span data-stu-id="835d5-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="835d5-153">Fiili değerler varlığında etkinlik yok</span><span class="sxs-lookup"><span data-stu-id="835d5-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="835d5-154">Zaman onaylanır ve onay sırasında faturalanabilir saatlerde değişiklik veya artış yoktur.</span><span class="sxs-lookup"><span data-stu-id="835d5-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="835d5-155">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="835d5-155">Cost actual</span></span></td>
<td><span data-ttu-id="835d5-156">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="835d5-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="835d5-157">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="835d5-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="835d5-158">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="835d5-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="835d5-159">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="835d5-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="835d5-160">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="835d5-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="835d5-161">Faturalanmayan satış gerçek değeri - Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="835d5-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="835d5-162">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="835d5-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="835d5-163">Zaman onaylanır ve onay sırasında faturalanabilir saatlerde azalma vardır.</span><span class="sxs-lookup"><span data-stu-id="835d5-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="835d5-164">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="835d5-164">Cost actual</span></span></td>
<td><span data-ttu-id="835d5-165">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="835d5-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="835d5-166">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="835d5-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="835d5-167">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="835d5-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="835d5-168">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="835d5-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="835d5-169">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="835d5-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="835d5-170">Faturalanmamış satış fiili değeri - Yeni miktar için borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="835d5-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="835d5-171">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="835d5-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="835d5-172">Faturalanmamış satış fiili değeri - Fark için borçlandırılamaz</span><span class="sxs-lookup"><span data-stu-id="835d5-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="835d5-173">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="835d5-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="835d5-174">Bir fatura onaylanır ve onay sırasında faturalanabilir saatlerde değişiklik veya artış yoktur.</span><span class="sxs-lookup"><span data-stu-id="835d5-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="835d5-175">Faturalanmamış satış geri çevirme</span><span class="sxs-lookup"><span data-stu-id="835d5-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="835d5-176">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="835d5-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="835d5-177">Kilometre taşı için faturalanan satış</span><span class="sxs-lookup"><span data-stu-id="835d5-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="835d5-178">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="835d5-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="835d5-179">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="835d5-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="835d5-180">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="835d5-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="835d5-181">Faturalanan satış</span><span class="sxs-lookup"><span data-stu-id="835d5-181">Billed sales</span></span></td>
<td><span data-ttu-id="835d5-182">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="835d5-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="835d5-183">Bir fatura onaylanır ve onay sırasında faturalanabilir saatlerde azalma vardır.</span><span class="sxs-lookup"><span data-stu-id="835d5-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="835d5-184">Faturalanmamış satış geri çevirme</span><span class="sxs-lookup"><span data-stu-id="835d5-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="835d5-185">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="835d5-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="835d5-186">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="835d5-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="835d5-187">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="835d5-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="835d5-188">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="835d5-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="835d5-189">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="835d5-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="835d5-190">Faturalanan satış - Yeni miktar için borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="835d5-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="835d5-191">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="835d5-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="835d5-192">Faturalanan satış - Fark için borçlandırılamaz</span><span class="sxs-lookup"><span data-stu-id="835d5-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="835d5-193">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="835d5-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="835d5-194">Borçlandırılabilir miktarı artırmak için fatura düzeltilir.</span><span class="sxs-lookup"><span data-stu-id="835d5-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="835d5-195">Faturalanan satış - Geri çevirme</span><span class="sxs-lookup"><span data-stu-id="835d5-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="835d5-196">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="835d5-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="835d5-197">Kilometre taşı için faturalanan satış geri çevirme</span><span class="sxs-lookup"><span data-stu-id="835d5-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="835d5-198">Kilometre taşı durumunda <strong>Faturalandı</strong>yerine <strong>Fatura için hazır</strong> olarak değişiklik</span><span class="sxs-lookup"><span data-stu-id="835d5-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="835d5-199">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="835d5-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="835d5-200">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="835d5-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="835d5-201">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="835d5-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="835d5-202">Faturalanan satış</span><span class="sxs-lookup"><span data-stu-id="835d5-202">Billed sales</span></span></td>
<td><span data-ttu-id="835d5-203">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="835d5-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="835d5-204">Borçlandırılabilir miktarı azaltmak için fatura düzeltilir.</span><span class="sxs-lookup"><span data-stu-id="835d5-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="835d5-205">Faturalanan satış - Geri çevirme</span><span class="sxs-lookup"><span data-stu-id="835d5-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="835d5-206">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="835d5-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="835d5-207">Yeni miktar için faturalanan satış</span><span class="sxs-lookup"><span data-stu-id="835d5-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="835d5-208">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="835d5-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="835d5-209">Faturalanmamış satış - Fark için borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="835d5-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="835d5-210">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="835d5-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="835d5-211">**Kaynak, projenin sözleşme biriminden farklı bir kuruluş birimine aittir.**</span><span class="sxs-lookup"><span data-stu-id="835d5-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="835d5-212">Olay</span><span class="sxs-lookup"><span data-stu-id="835d5-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="835d5-213">Faturalandırılabilir veya satılmış proje</span><span class="sxs-lookup"><span data-stu-id="835d5-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="835d5-214">Ön satış aşamasındaki proje</span><span class="sxs-lookup"><span data-stu-id="835d5-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="835d5-215">Dahili proje</span><span class="sxs-lookup"><span data-stu-id="835d5-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="835d5-216">Zaman ve malzemeler</span><span class="sxs-lookup"><span data-stu-id="835d5-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="835d5-217">Sabit fiyat</span><span class="sxs-lookup"><span data-stu-id="835d5-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="835d5-218">Gerçekler</span><span class="sxs-lookup"><span data-stu-id="835d5-218">Actuals</span></span></th>
<th><span data-ttu-id="835d5-219">İşlem para birimi</span><span class="sxs-lookup"><span data-stu-id="835d5-219">Transaction currency</span></span></th>
<th><span data-ttu-id="835d5-220">Sabit fiyat</span><span class="sxs-lookup"><span data-stu-id="835d5-220">Fixed price</span></span></th>
<th><span data-ttu-id="835d5-221">İşlem para birimi</span><span class="sxs-lookup"><span data-stu-id="835d5-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="835d5-222">Bir zaman girişi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="835d5-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="835d5-223">Fiili değerler varlığında etkinlik yok</span><span class="sxs-lookup"><span data-stu-id="835d5-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="835d5-224">Bir zaman girişi gönderilir.</span><span class="sxs-lookup"><span data-stu-id="835d5-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="835d5-225">Fiili değerler varlığında etkinlik yok</span><span class="sxs-lookup"><span data-stu-id="835d5-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="835d5-226">Zaman onaylanır ve onay sırasında faturalanabilir saatlerde değişiklik veya artış yoktur.</span><span class="sxs-lookup"><span data-stu-id="835d5-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="835d5-227">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="835d5-227">Cost actual</span></span></td>
<td><span data-ttu-id="835d5-228">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="835d5-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="835d5-229">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="835d5-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="835d5-230">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="835d5-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="835d5-231">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="835d5-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="835d5-232">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="835d5-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="835d5-233">Faturalanmayan satış gerçek değeri - Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="835d5-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="835d5-234">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="835d5-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="835d5-235">Kaynak belirleme birimi maliyeti</span><span class="sxs-lookup"><span data-stu-id="835d5-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="835d5-236">Kaynak belirleme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="835d5-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="835d5-237">Kuruluşlar arası satış</span><span class="sxs-lookup"><span data-stu-id="835d5-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="835d5-238">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="835d5-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="835d5-239">Zaman onaylanır ve onay sırasında faturalanabilir saatlerde azalma vardır.</span><span class="sxs-lookup"><span data-stu-id="835d5-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="835d5-240">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="835d5-240">Cost actual</span></span></td>
<td><span data-ttu-id="835d5-241">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="835d5-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="835d5-242">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="835d5-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="835d5-243">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="835d5-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="835d5-244">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="835d5-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="835d5-245">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="835d5-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="835d5-246">Kaynak belirleme birimi maliyeti</span><span class="sxs-lookup"><span data-stu-id="835d5-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="835d5-247">Kaynak belirleme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="835d5-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="835d5-248">Kuruluşlar arası satış</span><span class="sxs-lookup"><span data-stu-id="835d5-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="835d5-249">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="835d5-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="835d5-250">Faturalanmamış satış fiili değeri - Yeni miktar için borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="835d5-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="835d5-251">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="835d5-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="835d5-252">Faturalanmamış satış fiili değeri - Fark için borçlandırılamaz</span><span class="sxs-lookup"><span data-stu-id="835d5-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="835d5-253">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="835d5-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="835d5-254">Bir fatura onaylanır ve onay sırasında faturalanabilir saatlerde değişiklik veya artış yoktur.</span><span class="sxs-lookup"><span data-stu-id="835d5-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="835d5-255">Faturalanmamış satış geri çevirme</span><span class="sxs-lookup"><span data-stu-id="835d5-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="835d5-256">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="835d5-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="835d5-257">Kilometre taşı için faturalanan satış</span><span class="sxs-lookup"><span data-stu-id="835d5-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="835d5-258">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="835d5-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="835d5-259">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="835d5-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="835d5-260">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="835d5-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="835d5-261">Faturalanan satış</span><span class="sxs-lookup"><span data-stu-id="835d5-261">Billed sales</span></span></td>
<td><span data-ttu-id="835d5-262">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="835d5-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="835d5-263">Bir fatura onaylanır ve onay sırasında faturalanabilir saatlerde azalma vardır.</span><span class="sxs-lookup"><span data-stu-id="835d5-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="835d5-264">Faturalanmamış satış geri çevirme</span><span class="sxs-lookup"><span data-stu-id="835d5-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="835d5-265">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="835d5-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="835d5-266">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="835d5-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="835d5-267">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="835d5-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="835d5-268">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="835d5-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="835d5-269">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="835d5-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="835d5-270">Faturalanan satış - Yeni miktar için borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="835d5-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="835d5-271">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="835d5-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="835d5-272">Faturalanan satış - Fark için borçlandırılamaz</span><span class="sxs-lookup"><span data-stu-id="835d5-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="835d5-273">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="835d5-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="835d5-274">Borçlandırılabilir miktarı artırmak için fatura düzeltilir.</span><span class="sxs-lookup"><span data-stu-id="835d5-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="835d5-275">Faturalanan satış - Geri çevirme</span><span class="sxs-lookup"><span data-stu-id="835d5-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="835d5-276">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="835d5-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="835d5-277">Kilometre taşı için faturalanan satış geri çevirme</span><span class="sxs-lookup"><span data-stu-id="835d5-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="835d5-278">Kilometre taşı durumunda <strong>Faturalandı</strong>yerine <strong>Fatura için hazır</strong> olarak değişiklik</span><span class="sxs-lookup"><span data-stu-id="835d5-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="835d5-279">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="835d5-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="835d5-280">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="835d5-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="835d5-281">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="835d5-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="835d5-282">Faturalanan satış</span><span class="sxs-lookup"><span data-stu-id="835d5-282">Billed sales</span></span></td>
<td><span data-ttu-id="835d5-283">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="835d5-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="835d5-284">Borçlandırılabilir miktarı azaltmak için fatura düzeltilir.</span><span class="sxs-lookup"><span data-stu-id="835d5-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="835d5-285">Faturalanan satış - Geri çevirme</span><span class="sxs-lookup"><span data-stu-id="835d5-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="835d5-286">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="835d5-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="835d5-287">Yeni miktar için faturalanan satış</span><span class="sxs-lookup"><span data-stu-id="835d5-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="835d5-288">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="835d5-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="835d5-289">Faturalanmamış satış - Fark için borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="835d5-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="835d5-290">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="835d5-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]