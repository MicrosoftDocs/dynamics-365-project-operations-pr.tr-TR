---
title: Gerçek değerler
description: Bu konuda, Microsoft Dynamics 365 Project Operations'ta gerçek değerlerle çalışma hakkında bilgiler sağlanmaktadır.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 13c429763fa805fae5324e4dcf1bf7669e842281
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126348"
---
# <a name="actuals"></a><span data-ttu-id="49559-103">Gerçek değerler</span><span class="sxs-lookup"><span data-stu-id="49559-103">Actuals</span></span> 

<span data-ttu-id="49559-104">_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="49559-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="49559-105">Fiili değerler, bir projeki tamamlanmış iş tutarıdır.</span><span class="sxs-lookup"><span data-stu-id="49559-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="49559-106">Zaman ve gider girişleri, yevmiye defteri girişleri ve faturaların sonucu olarak oluşturulurlar.</span><span class="sxs-lookup"><span data-stu-id="49559-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="49559-107">Yevmiye defteri satırları ve zaman gönderimi</span><span class="sxs-lookup"><span data-stu-id="49559-107">Journal lines and time submission</span></span>

<span data-ttu-id="49559-108">Zaman girişi hakkında daha fazla bilgi için bkz. [Zaman girişine genel bakış](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="49559-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="49559-109">Zaman ve malzemeler</span><span class="sxs-lookup"><span data-stu-id="49559-109">Time and materials</span></span>

<span data-ttu-id="49559-110">Gönderilen bir zaman girişi, bir zaman ve malzeme sözleşme satırına eşlenen bir projeye bağlandığında sistem, biri maliyet ve diğeri faturalanmamış satışlar için olmak üzere iki yevmiye defteri satırı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="49559-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="49559-111">Sabit fiyat</span><span class="sxs-lookup"><span data-stu-id="49559-111">Fixed price</span></span>

<span data-ttu-id="49559-112">Gönderilen bir zaman girişi, sabit fiyatlı bir sözleşme satırına eşlenen bir projeye bağlandığında sistem, maliyet için bir yevmiye defteri satırı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="49559-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="49559-113">Varsayılan fiyatlandırma</span><span class="sxs-lookup"><span data-stu-id="49559-113">Default pricing</span></span>

<span data-ttu-id="49559-114">Varsayılan fiyatların oluşturulacağı mantık, yevmiye defteri satırında yer alır.</span><span class="sxs-lookup"><span data-stu-id="49559-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="49559-115">Zaman girişindeki alan değerleri yevmiye defteri satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="49559-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="49559-116">Bu değerler; işlem tarihini, projenin eşlendiği sözleşme satırını ve ilgili fiyat listesindeki para birimi sonucunu içerir.</span><span class="sxs-lookup"><span data-stu-id="49559-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="49559-117">**Rol** ve **Kuruluş Birimi** gibi varsayılan fiyatlandırmayı etkileyen alanlar, yevmiye defteri satırında uygun fiyatı belirlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="49559-117">The fields that affect default pricing, such as **Role** and **Org Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="49559-118">Zaman girişine özel bir alan ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="49559-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="49559-119">Alan değerinin gerçek değerlere doldurulmasını isterseniz alanı Gerçek değerler varlığında oluşturun ve alanı zaman girişinden gerçek değere kopyalamak için alan eşlemelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="49559-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="49559-120">Yevmiye defteri satırları ve temel gider gönderimi</span><span class="sxs-lookup"><span data-stu-id="49559-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="49559-121">Gider girişi hakkında daha fazla bilgi için bkz. [Gidere genel bakış](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="49559-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="49559-122">Zaman ve malzemeler</span><span class="sxs-lookup"><span data-stu-id="49559-122">Time and materials</span></span>

<span data-ttu-id="49559-123">Gönderilen bir temel gider girişi, bir zaman ve malzeme sözleşme satırına eşlenen bir projeye bağlandığında sistem, biri maliyet ve diğeri faturalanmamış satışlar için olmak üzere iki yevmiye defteri satırı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="49559-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="49559-124">Sabit fiyat</span><span class="sxs-lookup"><span data-stu-id="49559-124">Fixed price</span></span>

<span data-ttu-id="49559-125">Gönderilen bir temel gider girişi, sabit fiyatlı bir sözleşme satırına eşlenen bir projeye bağlandığında sistem, maliyet için bir yevmiye defteri satırı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="49559-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="49559-126">Varsayılan fiyatlandırma</span><span class="sxs-lookup"><span data-stu-id="49559-126">Default pricing</span></span>

<span data-ttu-id="49559-127">Giderler için varsayılan fiyatların girilmesi mantığı, gider kategorisini temel alır.</span><span class="sxs-lookup"><span data-stu-id="49559-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="49559-128">İşlemin tarihini, projenin eşlendiği sözleşme satırı ve ilgili fiyat listesindeki para birimi sonucu uygun fiyat listesini belirlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="49559-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="49559-129">Ancak varsayılan olarak fiyatın kendisi için girilen tutar, maliyet ve satışlar için ilgili gider yevmiye defteri satırlarında doğrudan ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="49559-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="49559-130">Gider girişlerinde, birim başına varsayılan fiyatların kategori tabanlı girişi kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="49559-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="49559-131">Maliyetleri kaydetmek için giriş yevmiye defterlerini kullanma</span><span class="sxs-lookup"><span data-stu-id="49559-131">Use entry journals to record costs</span></span>

<span data-ttu-id="49559-132">Giriş yevmiye defterlerini malzeme, ücret, zaman, gider veya vergi işlemi sınıflarında maliyeti veya geliri kaydetmek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="49559-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="49559-133">Yevmiye defterleri aşağıdaki amaçlar için kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="49559-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="49559-134">Projedeki gerçek malzeme ve satış maliyetini kaydedin.</span><span class="sxs-lookup"><span data-stu-id="49559-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="49559-135">İşlem gerçek değerlerini başka bir sistemden Microsoft Dynamics 365 Project Operations'a taşıyın.</span><span class="sxs-lookup"><span data-stu-id="49559-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="49559-136">Başka bir sistemde gerçekleşen maliyetleri kaydedin.</span><span class="sxs-lookup"><span data-stu-id="49559-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="49559-137">Bu maliyetler, satın alma veya alt yüklenici maliyetlerini içerebilir.</span><span class="sxs-lookup"><span data-stu-id="49559-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="49559-138">Uygulama, yevmiye defteri satırı türünü veya yevmiye defteri satırına girilen ilgili fiyatlandırmayı doğrulamaz.</span><span class="sxs-lookup"><span data-stu-id="49559-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="49559-139">Bu nedenle, yalnızca gerçek değerlerin proje üzerindeki muhasebe etkisinin tam olarak farkında olan bir kullanıcı, gerçek değerleri oluşturmak için giriş yevmiye defterlerini kullanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="49559-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="49559-140">Bu yevmiye defteri türünün etkisi nedeniyle giriş yevmiye defteri oluşturma işlemine kimlerin erişimi olacağını dikkatlice seçmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="49559-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="49559-141">Proje olaylarına göre gerçek değerleri kaydetme</span><span class="sxs-lookup"><span data-stu-id="49559-141">Record actuals based on project events</span></span>

<span data-ttu-id="49559-142">Project Operations, bir proje sırasında gerçekleşen finansal işlemleri kaydeder.</span><span class="sxs-lookup"><span data-stu-id="49559-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="49559-143">Bu işlemler fiili değerler olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="49559-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="49559-144">Aşağıdaki tablolar, projenin zaman ve malzeme veya sabit fiyatlı proje olmasına, ön satış aşamasında bulunmasına veya dahili bir proje olmasına bağlı olarak oluşturulan farklı fiili değer türlerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="49559-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="49559-145">Kaynak, projenin sözleşme birimiyle aynı kuruluş birimine aittir.</span><span class="sxs-lookup"><span data-stu-id="49559-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="49559-146">Olay</span><span class="sxs-lookup"><span data-stu-id="49559-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="49559-147">Faturalandırılabilir veya satılmış proje</span><span class="sxs-lookup"><span data-stu-id="49559-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="49559-148">Ön satış aşamasındaki proje</span><span class="sxs-lookup"><span data-stu-id="49559-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="49559-149">Dahili proje</span><span class="sxs-lookup"><span data-stu-id="49559-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="49559-150">Zaman ve malzemeler</span><span class="sxs-lookup"><span data-stu-id="49559-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="49559-151">Sabit fiyat</span><span class="sxs-lookup"><span data-stu-id="49559-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="49559-152">Gerçekler</span><span class="sxs-lookup"><span data-stu-id="49559-152">Actuals</span></span></th>
<th><span data-ttu-id="49559-153">İşlem para birimi</span><span class="sxs-lookup"><span data-stu-id="49559-153">Transaction currency</span></span></th>
<th><span data-ttu-id="49559-154">Sabit fiyat</span><span class="sxs-lookup"><span data-stu-id="49559-154">Fixed price</span></span></th>
<th><span data-ttu-id="49559-155">İşlem para birimi</span><span class="sxs-lookup"><span data-stu-id="49559-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="49559-156">Bir zaman girişi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="49559-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="49559-157">Fiili değerler varlığında etkinlik yok</span><span class="sxs-lookup"><span data-stu-id="49559-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49559-158">Bir zaman girişi gönderilir.</span><span class="sxs-lookup"><span data-stu-id="49559-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="49559-159">Fiili değerler varlığında etkinlik yok</span><span class="sxs-lookup"><span data-stu-id="49559-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="49559-160">Zaman onaylanır ve onay sırasında faturalanabilir saatlerde değişiklik veya artış yoktur.</span><span class="sxs-lookup"><span data-stu-id="49559-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="49559-161">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="49559-161">Cost actual</span></span></td>
<td><span data-ttu-id="49559-162">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="49559-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="49559-163">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="49559-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="49559-164">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="49559-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="49559-165">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="49559-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="49559-166">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="49559-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49559-167">Faturalandırılmamış satış fiili değer - Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="49559-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="49559-168">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="49559-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="49559-169">Zaman onaylanır ve onay sırasında faturalanabilir saatlerde azalma vardır.</span><span class="sxs-lookup"><span data-stu-id="49559-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="49559-170">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="49559-170">Cost actual</span></span></td>
<td><span data-ttu-id="49559-171">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="49559-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="49559-172">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="49559-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="49559-173">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="49559-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="49559-174">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="49559-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="49559-175">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="49559-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49559-176">Faturalanmamış satış fiili değeri - Yeni miktar için borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="49559-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="49559-177">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="49559-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49559-178">Faturalanmamış satış fiili değeri - Fark için borçlandırılamaz</span><span class="sxs-lookup"><span data-stu-id="49559-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="49559-179">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="49559-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="49559-180">Bir fatura onaylanır ve onay sırasında faturalanabilir saatlerde değişiklik veya artış yoktur.</span><span class="sxs-lookup"><span data-stu-id="49559-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="49559-181">Faturalanmamış satış geri çevirme</span><span class="sxs-lookup"><span data-stu-id="49559-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="49559-182">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="49559-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="49559-183">Kilometre taşı için faturalanan satış</span><span class="sxs-lookup"><span data-stu-id="49559-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="49559-184">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="49559-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="49559-185">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="49559-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="49559-186">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="49559-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49559-187">Faturalanan satış</span><span class="sxs-lookup"><span data-stu-id="49559-187">Billed sales</span></span></td>
<td><span data-ttu-id="49559-188">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="49559-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="49559-189">Bir fatura onaylanır ve onay sırasında faturalanabilir saatlerde azalma vardır.</span><span class="sxs-lookup"><span data-stu-id="49559-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="49559-190">Faturalanmamış satış geri çevirme</span><span class="sxs-lookup"><span data-stu-id="49559-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="49559-191">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="49559-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="49559-192">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="49559-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="49559-193">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="49559-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="49559-194">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="49559-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="49559-195">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="49559-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49559-196">Faturalanan satış - Yeni miktar için borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="49559-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="49559-197">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="49559-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49559-198">Faturalanan satış - Fark için borçlandırılamaz</span><span class="sxs-lookup"><span data-stu-id="49559-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="49559-199">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="49559-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="49559-200">Borçlandırılabilir miktarı artırmak için fatura düzeltilir.</span><span class="sxs-lookup"><span data-stu-id="49559-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="49559-201">Faturalanan satış - Geri çevirme</span><span class="sxs-lookup"><span data-stu-id="49559-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="49559-202">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="49559-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="49559-203">Kilometre taşı için faturalanan satış geri çevirme</span><span class="sxs-lookup"><span data-stu-id="49559-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="49559-204">Kilometre taşı durumunda <strong>Faturalandı</strong>yerine <strong>Fatura için hazır</strong> olarak değişiklik</span><span class="sxs-lookup"><span data-stu-id="49559-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="49559-205">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="49559-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="49559-206">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="49559-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="49559-207">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="49559-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49559-208">Faturalanan satış</span><span class="sxs-lookup"><span data-stu-id="49559-208">Billed sales</span></span></td>
<td><span data-ttu-id="49559-209">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="49559-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="49559-210">Borçlandırılabilir miktarı azaltmak için fatura düzeltilir.</span><span class="sxs-lookup"><span data-stu-id="49559-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="49559-211">Faturalanan satış - Geri çevirme</span><span class="sxs-lookup"><span data-stu-id="49559-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="49559-212">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="49559-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49559-213">Yeni miktar için faturalanan satış</span><span class="sxs-lookup"><span data-stu-id="49559-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="49559-214">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="49559-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49559-215">Faturalanmamış satış - Fark için borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="49559-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="49559-216">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="49559-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="49559-217">Kaynak, projenin sözleşme biriminden farklı bir kuruluş birimine aittir.</span><span class="sxs-lookup"><span data-stu-id="49559-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="49559-218">Olay</span><span class="sxs-lookup"><span data-stu-id="49559-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="49559-219">Faturalandırılabilir veya satılmış proje</span><span class="sxs-lookup"><span data-stu-id="49559-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="49559-220">Ön satış aşamasındaki proje</span><span class="sxs-lookup"><span data-stu-id="49559-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="49559-221">Dahili proje</span><span class="sxs-lookup"><span data-stu-id="49559-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="49559-222">Zaman ve malzemeler</span><span class="sxs-lookup"><span data-stu-id="49559-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="49559-223">Sabit fiyat</span><span class="sxs-lookup"><span data-stu-id="49559-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="49559-224">Gerçekler</span><span class="sxs-lookup"><span data-stu-id="49559-224">Actuals</span></span></th>
<th><span data-ttu-id="49559-225">İşlem para birimi</span><span class="sxs-lookup"><span data-stu-id="49559-225">Transaction currency</span></span></th>
<th><span data-ttu-id="49559-226">Sabit fiyat</span><span class="sxs-lookup"><span data-stu-id="49559-226">Fixed price</span></span></th>
<th><span data-ttu-id="49559-227">İşlem para birimi</span><span class="sxs-lookup"><span data-stu-id="49559-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="49559-228">Bir zaman girişi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="49559-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="49559-229">Fiili değerler varlığında etkinlik yok</span><span class="sxs-lookup"><span data-stu-id="49559-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49559-230">Bir zaman girişi gönderilir.</span><span class="sxs-lookup"><span data-stu-id="49559-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="49559-231">Fiili değerler varlığında etkinlik yok</span><span class="sxs-lookup"><span data-stu-id="49559-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="49559-232">Zaman onaylanır ve onay sırasında faturalanabilir saatlerde değişiklik veya artış yoktur.</span><span class="sxs-lookup"><span data-stu-id="49559-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="49559-233">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="49559-233">Cost actual</span></span></td>
<td><span data-ttu-id="49559-234">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="49559-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="49559-235">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="49559-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="49559-236">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="49559-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="49559-237">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="49559-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="49559-238">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="49559-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49559-239">Faturalandırılmamış satış fiili değer - Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="49559-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="49559-240">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="49559-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49559-241">Kaynak belirleme birimi maliyeti</span><span class="sxs-lookup"><span data-stu-id="49559-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="49559-242">Kaynak belirleme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="49559-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49559-243">Kuruluşlar arası satış</span><span class="sxs-lookup"><span data-stu-id="49559-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="49559-244">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="49559-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="49559-245">Zaman onaylanır ve onay sırasında faturalanabilir saatlerde azalma vardır.</span><span class="sxs-lookup"><span data-stu-id="49559-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="49559-246">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="49559-246">Cost actual</span></span></td>
<td><span data-ttu-id="49559-247">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="49559-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="49559-248">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="49559-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="49559-249">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="49559-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="49559-250">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="49559-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="49559-251">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="49559-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49559-252">Kaynak belirleme birimi maliyeti</span><span class="sxs-lookup"><span data-stu-id="49559-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="49559-253">Kaynak belirleme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="49559-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49559-254">Kuruluşlar arası satış</span><span class="sxs-lookup"><span data-stu-id="49559-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="49559-255">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="49559-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49559-256">Faturalanmamış satış fiili değeri - Yeni miktar için borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="49559-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="49559-257">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="49559-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49559-258">Faturalanmamış satış fiili değeri - Fark için borçlandırılamaz</span><span class="sxs-lookup"><span data-stu-id="49559-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="49559-259">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="49559-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="49559-260">Bir fatura onaylanır ve onay sırasında faturalanabilir saatlerde değişiklik veya artış yoktur.</span><span class="sxs-lookup"><span data-stu-id="49559-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="49559-261">Faturalanmamış satış geri çevirme</span><span class="sxs-lookup"><span data-stu-id="49559-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="49559-262">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="49559-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="49559-263">Kilometre taşı için faturalanan satış</span><span class="sxs-lookup"><span data-stu-id="49559-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="49559-264">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="49559-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="49559-265">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="49559-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="49559-266">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="49559-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49559-267">Faturalanan satış</span><span class="sxs-lookup"><span data-stu-id="49559-267">Billed sales</span></span></td>
<td><span data-ttu-id="49559-268">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="49559-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="49559-269">Bir fatura onaylanır ve onay sırasında faturalanabilir saatlerde azalma vardır.</span><span class="sxs-lookup"><span data-stu-id="49559-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="49559-270">Faturalanmamış satış geri çevirme</span><span class="sxs-lookup"><span data-stu-id="49559-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="49559-271">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="49559-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="49559-272">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="49559-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="49559-273">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="49559-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="49559-274">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="49559-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="49559-275">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="49559-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49559-276">Faturalanan satış - Yeni miktar için borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="49559-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="49559-277">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="49559-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49559-278">Faturalanan satış - Fark için borçlandırılamaz</span><span class="sxs-lookup"><span data-stu-id="49559-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="49559-279">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="49559-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="49559-280">Borçlandırılabilir miktarı artırmak için fatura düzeltilir.</span><span class="sxs-lookup"><span data-stu-id="49559-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="49559-281">Faturalanan satış - Geri çevirme</span><span class="sxs-lookup"><span data-stu-id="49559-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="49559-282">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="49559-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="49559-283">Kilometre taşı için faturalanan satış geri çevirme</span><span class="sxs-lookup"><span data-stu-id="49559-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="49559-284">Kilometre taşı durumunda <strong>Faturalandı</strong>yerine <strong>Fatura için hazır</strong> olarak değişiklik</span><span class="sxs-lookup"><span data-stu-id="49559-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="49559-285">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="49559-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="49559-286">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="49559-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="49559-287">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="49559-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49559-288">Faturalanan satış</span><span class="sxs-lookup"><span data-stu-id="49559-288">Billed sales</span></span></td>
<td><span data-ttu-id="49559-289">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="49559-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="49559-290">Borçlandırılabilir miktarı azaltmak için fatura düzeltilir.</span><span class="sxs-lookup"><span data-stu-id="49559-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="49559-291">Faturalanan satış - Geri çevirme</span><span class="sxs-lookup"><span data-stu-id="49559-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="49559-292">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="49559-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49559-293">Yeni miktar için faturalanan satış</span><span class="sxs-lookup"><span data-stu-id="49559-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="49559-294">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="49559-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="49559-295">Faturalanmamış satış - Fark için borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="49559-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="49559-296">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="49559-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
