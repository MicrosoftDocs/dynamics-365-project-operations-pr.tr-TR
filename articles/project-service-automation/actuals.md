---
title: Gerçekler
description: Bu konu proje fiili değerleri hakkında bilgi sağlar.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 44c6e85f-5b21-4e24-999c-15a2f065d977
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8291e0eb8531e8e9690368675f333c44b6e92e48
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756698"
---
# <a name="actuals"></a><span data-ttu-id="6b9f2-103">Gerçekler</span><span class="sxs-lookup"><span data-stu-id="6b9f2-103">Actuals</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="6b9f2-104">Fiili değerler, bir projeki tamamlanmış iş tutarıdır.</span><span class="sxs-lookup"><span data-stu-id="6b9f2-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="6b9f2-105">Proje fiili değerleri, kaynak belgelerine doğru izlenebilir.</span><span class="sxs-lookup"><span data-stu-id="6b9f2-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="6b9f2-106">Bu kaynak belgeler arasında zaman, gider, günlük girişleri ve ayrıca faturalar vardır.</span><span class="sxs-lookup"><span data-stu-id="6b9f2-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Proje fiili değerlerini kaynak belgelerde izleme](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="6b9f2-108">Bir zaman girişi gönderme</span><span class="sxs-lookup"><span data-stu-id="6b9f2-108">Submitting a time entry</span></span>

<span data-ttu-id="6b9f2-109">PSA'da, zaman ve malzemeler sözleşmesi satırıyla eşlenen bir proje için bir zaman girişi gönderildiğinde iki günlük satırı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="6b9f2-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="6b9f2-110">Bir satır maliyet için ve diğer satır faturalandırılmamış satış içindir.</span><span class="sxs-lookup"><span data-stu-id="6b9f2-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="6b9f2-111">Sabit fiyat sözleşme satırıyla eşlenen bir proje için bir zaman girişi gönderildiğinde yalnızca maliyet için bir günlük satırı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="6b9f2-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="6b9f2-112">Varsayılan fiyatların girileceği mantık günlük satırında yer alır.</span><span class="sxs-lookup"><span data-stu-id="6b9f2-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="6b9f2-113">Bir zaman girişindeki tüm alan değerleri günlük satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="6b9f2-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="6b9f2-114">Bu alanlar işlemin tarihini, projenin eşlendiği sözleşme satırını ve ilgili fiyat listesindeki para birimi sonucunu içerir.</span><span class="sxs-lookup"><span data-stu-id="6b9f2-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="6b9f2-115">**Rol** ve **Kuruluş Birimi** gibi varsayılan fiyatları etkileyen alanlar, günlük satırında varsayılan olarak uygun bir fiyatın girilmesine neden olur.</span><span class="sxs-lookup"><span data-stu-id="6b9f2-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="6b9f2-116">Zaman girişine bir özel alan ekler ve alan değerinin fiili değerlere yayılmasını isterseniz, alanı Fiili değerler varlığında oluşturun ve alanı zaman girişinden fiili değere kopyalamak için alan eşlemelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6b9f2-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="6b9f2-117">Gider girişi gönderme</span><span class="sxs-lookup"><span data-stu-id="6b9f2-117">Submitting an expense entry</span></span>

<span data-ttu-id="6b9f2-118">PSA'da, zaman ve malzemeler sözleşmesi satırıyla eşlenen bir proje için bir gider girişi gönderildiğinde iki günlük satırı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="6b9f2-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="6b9f2-119">Bir satır maliyet için ve diğer satır faturalandırılmamış satış içindir.</span><span class="sxs-lookup"><span data-stu-id="6b9f2-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="6b9f2-120">Sabit fiyat sözleşme satırıyla eşlenen bir proje için bir gider girişi gönderildiğinde yalnızca maliyet için bir günlük satırı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="6b9f2-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="6b9f2-121">Giderler için varsayılan fiyatları girme mantığı **Gider girişi** sayfasında seçilen gider kategorisine dayanır.</span><span class="sxs-lookup"><span data-stu-id="6b9f2-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="6b9f2-122">İşlemin tarihini, projenin eşlendiği sözleşme satırı ve ilgili fiyat listesindeki para birimi sonucu uygun fiyat listesini belirlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6b9f2-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="6b9f2-123">Ancak, fiyatın kendisi için, kullanıcının girdiği tutar varsayılan olarak maliyet ve satışlar için ilgili gider günlüğü satırlarında doğrudan ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="6b9f2-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="6b9f2-124">Geçerli PSA sürümünde, gider girişlerinde birim başına varsayılan fiyatların kategori tabanlı girişi kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="6b9f2-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-journals-to-record-costs"></a><span data-ttu-id="6b9f2-125">Maliyetleri kaydetmek için günlükleri kullanma</span><span class="sxs-lookup"><span data-stu-id="6b9f2-125">Using journals to record costs</span></span>

<span data-ttu-id="6b9f2-126">PSA 'da günlükler malzeme, ücret, zaman, masraf veya vergi işlemi sınıflarında maliyeti veya geliri kaydetmenize olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="6b9f2-126">In PSA, journals let you record cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="6b9f2-127">Bir günlükte başlık, satırlar ve **Onayla** eylemi vardır.</span><span class="sxs-lookup"><span data-stu-id="6b9f2-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="6b9f2-128">Aşağıda bir günlüğü kullanabileceğiniz bazı senaryolar vardır:</span><span class="sxs-lookup"><span data-stu-id="6b9f2-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="6b9f2-129">Bir projedeki malzeme fiili maliyetlerini ve satışları kaydetmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="6b9f2-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="6b9f2-130">İşlem fiili değerlerini başka bir sistemden PSA'ya taşımanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="6b9f2-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="6b9f2-131">Başka bir sistemde gerçekleşen (örneğin, tedarik veya taşeron maliyetleri) maliyetleri kaydetmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="6b9f2-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="6b9f2-132">Proje olaylarına göre fiili değerleri kaydetme</span><span class="sxs-lookup"><span data-stu-id="6b9f2-132">Recording actuals based on project events</span></span>

<span data-ttu-id="6b9f2-133">PSA bir proje sırasında gerçekleşen mali işlemleri kaydeder.</span><span class="sxs-lookup"><span data-stu-id="6b9f2-133">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="6b9f2-134">Bu işlemler **fiili değerler** olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="6b9f2-134">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="6b9f2-135">Aşağıdaki tablolar, projenin zaman ve malzeme veya sabit fiyatlı proje olmasına, ön satış aşamasında bulunmasına veya dahili bir proje olmasına bağlı olarak oluşturulan farklı fiili değer türlerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="6b9f2-135">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="6b9f2-136">**Kaynak, projenin sözleşme birimiyle aynı kuruluş birimine aittir.**</span><span class="sxs-lookup"><span data-stu-id="6b9f2-136">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="6b9f2-137">Olay</span><span class="sxs-lookup"><span data-stu-id="6b9f2-137">Event</span></span></th>
<th colspan="4"><span data-ttu-id="6b9f2-138">Faturalandırılabilir veya satılmış proje</span><span class="sxs-lookup"><span data-stu-id="6b9f2-138">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="6b9f2-139">Ön satış aşamasındaki proje</span><span class="sxs-lookup"><span data-stu-id="6b9f2-139">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="6b9f2-140">Dahili proje</span><span class="sxs-lookup"><span data-stu-id="6b9f2-140">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="6b9f2-141">Zaman ve malzemeler</span><span class="sxs-lookup"><span data-stu-id="6b9f2-141">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="6b9f2-142">Sabit fiyat</span><span class="sxs-lookup"><span data-stu-id="6b9f2-142">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="6b9f2-143">Gerçekler</span><span class="sxs-lookup"><span data-stu-id="6b9f2-143">Actuals</span></span></th>
<th><span data-ttu-id="6b9f2-144">İşlem para birimi</span><span class="sxs-lookup"><span data-stu-id="6b9f2-144">Transaction currency</span></span></th>
<th><span data-ttu-id="6b9f2-145">Sabit fiyat</span><span class="sxs-lookup"><span data-stu-id="6b9f2-145">Fixed price</span></span></th>
<th><span data-ttu-id="6b9f2-146">İşlem para birimi</span><span class="sxs-lookup"><span data-stu-id="6b9f2-146">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6b9f2-147">Bir zaman girişi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="6b9f2-147">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="6b9f2-148">Fiili değerler varlığında etkinlik yok</span><span class="sxs-lookup"><span data-stu-id="6b9f2-148">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6b9f2-149">Bir zaman girişi gönderilir.</span><span class="sxs-lookup"><span data-stu-id="6b9f2-149">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="6b9f2-150">Fiili değerler varlığında etkinlik yok</span><span class="sxs-lookup"><span data-stu-id="6b9f2-150">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="6b9f2-151">Zaman onaylanır ve onay sırasında faturalanabilir saatlerde değişiklik veya artış yoktur.</span><span class="sxs-lookup"><span data-stu-id="6b9f2-151">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="6b9f2-152">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="6b9f2-152">Cost actual</span></span></td>
<td><span data-ttu-id="6b9f2-153">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="6b9f2-153">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="6b9f2-154">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="6b9f2-154">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="6b9f2-155">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="6b9f2-155">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="6b9f2-156">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="6b9f2-156">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="6b9f2-157">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="6b9f2-157">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6b9f2-158">Faturalandırılmamış satış fiili değer - Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="6b9f2-158">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="6b9f2-159">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="6b9f2-159">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="6b9f2-160">Zaman onaylanır ve onay sırasında faturalanabilir saatlerde azalma vardır.</span><span class="sxs-lookup"><span data-stu-id="6b9f2-160">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="6b9f2-161">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="6b9f2-161">Cost actual</span></span></td>
<td><span data-ttu-id="6b9f2-162">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="6b9f2-162">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="6b9f2-163">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="6b9f2-163">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="6b9f2-164">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="6b9f2-164">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="6b9f2-165">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="6b9f2-165">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="6b9f2-166">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="6b9f2-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6b9f2-167">Faturalanmamış satış fiili değeri - Yeni miktar için borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="6b9f2-167">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="6b9f2-168">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="6b9f2-168">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6b9f2-169">Faturalanmamış satış fiili değeri - Fark için borçlandırılamaz</span><span class="sxs-lookup"><span data-stu-id="6b9f2-169">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="6b9f2-170">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="6b9f2-170">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="6b9f2-171">Bir fatura onaylanır ve onay sırasında faturalanabilir saatlerde değişiklik veya artış yoktur.</span><span class="sxs-lookup"><span data-stu-id="6b9f2-171">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="6b9f2-172">Faturalanmamış satış geri çevirme</span><span class="sxs-lookup"><span data-stu-id="6b9f2-172">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="6b9f2-173">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="6b9f2-173">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="6b9f2-174">Kilometre taşı için faturalanan satış</span><span class="sxs-lookup"><span data-stu-id="6b9f2-174">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="6b9f2-175">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="6b9f2-175">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="6b9f2-176">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="6b9f2-176">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="6b9f2-177">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="6b9f2-177">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6b9f2-178">Faturalanan satış</span><span class="sxs-lookup"><span data-stu-id="6b9f2-178">Billed sales</span></span></td>
<td><span data-ttu-id="6b9f2-179">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="6b9f2-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="6b9f2-180">Bir fatura onaylanır ve onay sırasında faturalanabilir saatlerde azalma vardır.</span><span class="sxs-lookup"><span data-stu-id="6b9f2-180">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="6b9f2-181">Faturalanmamış satış geri çevirme</span><span class="sxs-lookup"><span data-stu-id="6b9f2-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="6b9f2-182">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="6b9f2-182">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="6b9f2-183">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="6b9f2-183">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="6b9f2-184">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="6b9f2-184">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="6b9f2-185">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="6b9f2-185">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="6b9f2-186">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="6b9f2-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6b9f2-187">Faturalanan satış - Yeni miktar için borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="6b9f2-187">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="6b9f2-188">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="6b9f2-188">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6b9f2-189">Faturalanan satış - Fark için borçlandırılamaz</span><span class="sxs-lookup"><span data-stu-id="6b9f2-189">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="6b9f2-190">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="6b9f2-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="6b9f2-191">Borçlandırılabilir miktarı artırmak için fatura düzeltilir.</span><span class="sxs-lookup"><span data-stu-id="6b9f2-191">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="6b9f2-192">Faturalanan satış - Geri çevirme</span><span class="sxs-lookup"><span data-stu-id="6b9f2-192">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="6b9f2-193">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="6b9f2-193">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="6b9f2-194">Kilometre taşı için faturalanan satış geri çevirme</span><span class="sxs-lookup"><span data-stu-id="6b9f2-194">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="6b9f2-195">Kilometre taşı durumunda <strong>Faturalandı</strong>yerine <strong>Fatura için hazır</strong> olarak değişiklik</span><span class="sxs-lookup"><span data-stu-id="6b9f2-195">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="6b9f2-196">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="6b9f2-196">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="6b9f2-197">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="6b9f2-197">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="6b9f2-198">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="6b9f2-198">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6b9f2-199">Faturalanan satış</span><span class="sxs-lookup"><span data-stu-id="6b9f2-199">Billed sales</span></span></td>
<td><span data-ttu-id="6b9f2-200">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="6b9f2-200">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="6b9f2-201">Borçlandırılabilir miktarı azaltmak için fatura düzeltilir.</span><span class="sxs-lookup"><span data-stu-id="6b9f2-201">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="6b9f2-202">Faturalanan satış - Geri çevirme</span><span class="sxs-lookup"><span data-stu-id="6b9f2-202">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="6b9f2-203">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="6b9f2-203">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6b9f2-204">Yeni miktar için faturalanan satış</span><span class="sxs-lookup"><span data-stu-id="6b9f2-204">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="6b9f2-205">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="6b9f2-205">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6b9f2-206">Faturalanmamış satış - Fark için borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="6b9f2-206">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="6b9f2-207">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="6b9f2-207">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6b9f2-208">**Kaynak, projenin sözleşme biriminden farklı bir kuruluş birimine aittir.**</span><span class="sxs-lookup"><span data-stu-id="6b9f2-208">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="6b9f2-209">Olay</span><span class="sxs-lookup"><span data-stu-id="6b9f2-209">Event</span></span></th>
<th colspan="4"><span data-ttu-id="6b9f2-210">Faturalandırılabilir veya satılmış proje</span><span class="sxs-lookup"><span data-stu-id="6b9f2-210">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="6b9f2-211">Ön satış aşamasındaki proje</span><span class="sxs-lookup"><span data-stu-id="6b9f2-211">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="6b9f2-212">Dahili proje</span><span class="sxs-lookup"><span data-stu-id="6b9f2-212">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="6b9f2-213">Zaman ve malzemeler</span><span class="sxs-lookup"><span data-stu-id="6b9f2-213">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="6b9f2-214">Sabit fiyat</span><span class="sxs-lookup"><span data-stu-id="6b9f2-214">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="6b9f2-215">Gerçekler</span><span class="sxs-lookup"><span data-stu-id="6b9f2-215">Actuals</span></span></th>
<th><span data-ttu-id="6b9f2-216">İşlem para birimi</span><span class="sxs-lookup"><span data-stu-id="6b9f2-216">Transaction currency</span></span></th>
<th><span data-ttu-id="6b9f2-217">Sabit fiyat</span><span class="sxs-lookup"><span data-stu-id="6b9f2-217">Fixed price</span></span></th>
<th><span data-ttu-id="6b9f2-218">İşlem para birimi</span><span class="sxs-lookup"><span data-stu-id="6b9f2-218">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6b9f2-219">Bir zaman girişi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="6b9f2-219">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="6b9f2-220">Fiili değerler varlığında etkinlik yok</span><span class="sxs-lookup"><span data-stu-id="6b9f2-220">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6b9f2-221">Bir zaman girişi gönderilir.</span><span class="sxs-lookup"><span data-stu-id="6b9f2-221">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="6b9f2-222">Fiili değerler varlığında etkinlik yok</span><span class="sxs-lookup"><span data-stu-id="6b9f2-222">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="6b9f2-223">Zaman onaylanır ve onay sırasında faturalanabilir saatlerde değişiklik veya artış yoktur.</span><span class="sxs-lookup"><span data-stu-id="6b9f2-223">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="6b9f2-224">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="6b9f2-224">Cost actual</span></span></td>
<td><span data-ttu-id="6b9f2-225">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="6b9f2-225">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="6b9f2-226">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="6b9f2-226">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="6b9f2-227">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="6b9f2-227">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="6b9f2-228">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="6b9f2-228">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="6b9f2-229">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="6b9f2-229">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6b9f2-230">Faturalandırılmamış satış fiili değer - Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="6b9f2-230">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="6b9f2-231">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="6b9f2-231">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6b9f2-232">Kaynak belirleme birimi maliyeti</span><span class="sxs-lookup"><span data-stu-id="6b9f2-232">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="6b9f2-233">Kaynak belirleme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="6b9f2-233">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6b9f2-234">Kuruluşlar arası satış</span><span class="sxs-lookup"><span data-stu-id="6b9f2-234">Interorganizational sales</span></span></td>
<td><span data-ttu-id="6b9f2-235">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="6b9f2-235">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="6b9f2-236">Zaman onaylanır ve onay sırasında faturalanabilir saatlerde azalma vardır.</span><span class="sxs-lookup"><span data-stu-id="6b9f2-236">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="6b9f2-237">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="6b9f2-237">Cost actual</span></span></td>
<td><span data-ttu-id="6b9f2-238">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="6b9f2-238">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="6b9f2-239">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="6b9f2-239">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="6b9f2-240">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="6b9f2-240">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="6b9f2-241">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="6b9f2-241">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="6b9f2-242">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="6b9f2-242">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6b9f2-243">Kaynak belirleme birimi maliyeti</span><span class="sxs-lookup"><span data-stu-id="6b9f2-243">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="6b9f2-244">Kaynak belirleme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="6b9f2-244">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6b9f2-245">Kuruluşlar arası satış</span><span class="sxs-lookup"><span data-stu-id="6b9f2-245">Interorganizational sales</span></span></td>
<td><span data-ttu-id="6b9f2-246">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="6b9f2-246">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6b9f2-247">Faturalanmamış satış fiili değeri - Yeni miktar için borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="6b9f2-247">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="6b9f2-248">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="6b9f2-248">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6b9f2-249">Faturalanmamış satış fiili değeri - Fark için borçlandırılamaz</span><span class="sxs-lookup"><span data-stu-id="6b9f2-249">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="6b9f2-250">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="6b9f2-250">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="6b9f2-251">Bir fatura onaylanır ve onay sırasında faturalanabilir saatlerde değişiklik veya artış yoktur.</span><span class="sxs-lookup"><span data-stu-id="6b9f2-251">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="6b9f2-252">Faturalanmamış satış geri çevirme</span><span class="sxs-lookup"><span data-stu-id="6b9f2-252">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="6b9f2-253">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="6b9f2-253">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="6b9f2-254">Kilometre taşı için faturalanan satış</span><span class="sxs-lookup"><span data-stu-id="6b9f2-254">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="6b9f2-255">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="6b9f2-255">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="6b9f2-256">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="6b9f2-256">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="6b9f2-257">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="6b9f2-257">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6b9f2-258">Faturalanan satış</span><span class="sxs-lookup"><span data-stu-id="6b9f2-258">Billed sales</span></span></td>
<td><span data-ttu-id="6b9f2-259">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="6b9f2-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="6b9f2-260">Bir fatura onaylanır ve onay sırasında faturalanabilir saatlerde azalma vardır.</span><span class="sxs-lookup"><span data-stu-id="6b9f2-260">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="6b9f2-261">Faturalanmamış satış geri çevirme</span><span class="sxs-lookup"><span data-stu-id="6b9f2-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="6b9f2-262">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="6b9f2-262">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="6b9f2-263">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="6b9f2-263">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="6b9f2-264">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="6b9f2-264">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="6b9f2-265">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="6b9f2-265">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="6b9f2-266">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="6b9f2-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6b9f2-267">Faturalanan satış - Yeni miktar için borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="6b9f2-267">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="6b9f2-268">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="6b9f2-268">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6b9f2-269">Faturalanan satış - Fark için borçlandırılamaz</span><span class="sxs-lookup"><span data-stu-id="6b9f2-269">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="6b9f2-270">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="6b9f2-270">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="6b9f2-271">Borçlandırılabilir miktarı artırmak için fatura düzeltilir.</span><span class="sxs-lookup"><span data-stu-id="6b9f2-271">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="6b9f2-272">Faturalanan satış - Geri çevirme</span><span class="sxs-lookup"><span data-stu-id="6b9f2-272">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="6b9f2-273">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="6b9f2-273">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="6b9f2-274">Kilometre taşı için faturalanan satış geri çevirme</span><span class="sxs-lookup"><span data-stu-id="6b9f2-274">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="6b9f2-275">Kilometre taşı durumunda <strong>Faturalandı</strong>yerine <strong>Fatura için hazır</strong> olarak değişiklik</span><span class="sxs-lookup"><span data-stu-id="6b9f2-275">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="6b9f2-276">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="6b9f2-276">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="6b9f2-277">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="6b9f2-277">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="6b9f2-278">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="6b9f2-278">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6b9f2-279">Faturalanan satış</span><span class="sxs-lookup"><span data-stu-id="6b9f2-279">Billed sales</span></span></td>
<td><span data-ttu-id="6b9f2-280">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="6b9f2-280">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="6b9f2-281">Borçlandırılabilir miktarı azaltmak için fatura düzeltilir.</span><span class="sxs-lookup"><span data-stu-id="6b9f2-281">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="6b9f2-282">Faturalanan satış - Geri çevirme</span><span class="sxs-lookup"><span data-stu-id="6b9f2-282">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="6b9f2-283">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="6b9f2-283">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6b9f2-284">Yeni miktar için faturalanan satış</span><span class="sxs-lookup"><span data-stu-id="6b9f2-284">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="6b9f2-285">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="6b9f2-285">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6b9f2-286">Faturalanmamış satış - Fark için borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="6b9f2-286">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="6b9f2-287">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="6b9f2-287">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
