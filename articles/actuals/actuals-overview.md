---
title: Gerçek değerler
description: Bu konuda, Microsoft Dynamics 365 Project Operations'ta gerçek değerlerle çalışma hakkında bilgiler sağlanmaktadır.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 93a945ffbe9c6dd998456b506b95e717ab8fbab7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086314"
---
# <a name="actuals"></a><span data-ttu-id="3ec6e-103">Gerçek değerler</span><span class="sxs-lookup"><span data-stu-id="3ec6e-103">Actuals</span></span> 

<span data-ttu-id="3ec6e-104">_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="3ec6e-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="3ec6e-105">Fiili değerler, bir projeki tamamlanmış iş tutarıdır.</span><span class="sxs-lookup"><span data-stu-id="3ec6e-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="3ec6e-106">Zaman ve gider girişleri, yevmiye defteri girişleri ve faturaların sonucu olarak oluşturulurlar.</span><span class="sxs-lookup"><span data-stu-id="3ec6e-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="3ec6e-107">Yevmiye defteri satırları ve zaman gönderimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-107">Journal lines and time submission</span></span>

<span data-ttu-id="3ec6e-108">Zaman girişi hakkında daha fazla bilgi için bkz. [Zaman girişine genel bakış](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3ec6e-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="3ec6e-109">Zaman ve malzemeler</span><span class="sxs-lookup"><span data-stu-id="3ec6e-109">Time and materials</span></span>

<span data-ttu-id="3ec6e-110">Gönderilen bir zaman girişi, bir zaman ve malzeme sözleşme satırına eşlenen bir projeye bağlandığında sistem, biri maliyet ve diğeri faturalanmamış satışlar için olmak üzere iki yevmiye defteri satırı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3ec6e-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="3ec6e-111">Sabit fiyat</span><span class="sxs-lookup"><span data-stu-id="3ec6e-111">Fixed price</span></span>

<span data-ttu-id="3ec6e-112">Gönderilen bir zaman girişi, sabit fiyatlı bir sözleşme satırına eşlenen bir projeye bağlandığında sistem, maliyet için bir yevmiye defteri satırı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3ec6e-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="3ec6e-113">Varsayılan fiyatlandırma</span><span class="sxs-lookup"><span data-stu-id="3ec6e-113">Default pricing</span></span>

<span data-ttu-id="3ec6e-114">Varsayılan fiyatların oluşturulacağı mantık, yevmiye defteri satırında yer alır.</span><span class="sxs-lookup"><span data-stu-id="3ec6e-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="3ec6e-115">Zaman girişindeki alan değerleri yevmiye defteri satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="3ec6e-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="3ec6e-116">Bu değerler; işlem tarihini, projenin eşlendiği sözleşme satırını ve ilgili fiyat listesindeki para birimi sonucunu içerir.</span><span class="sxs-lookup"><span data-stu-id="3ec6e-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="3ec6e-117">**Rol** ve **Kuruluş Birimi** gibi varsayılan fiyatlandırmayı etkileyen alanlar, yevmiye defteri satırında uygun fiyatı belirlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3ec6e-117">The fields that affect default pricing, such as **Role** and **Org Unit** , are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="3ec6e-118">Zaman girişine özel bir alan ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3ec6e-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="3ec6e-119">Alan değerinin gerçek değerlere doldurulmasını isterseniz alanı Gerçek değerler varlığında oluşturun ve alanı zaman girişinden gerçek değere kopyalamak için alan eşlemelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="3ec6e-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="3ec6e-120">Yevmiye defteri satırları ve temel gider gönderimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="3ec6e-121">Gider girişi hakkında daha fazla bilgi için bkz. [Gidere genel bakış](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3ec6e-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="3ec6e-122">Zaman ve malzemeler</span><span class="sxs-lookup"><span data-stu-id="3ec6e-122">Time and materials</span></span>

<span data-ttu-id="3ec6e-123">Gönderilen bir temel gider girişi, bir zaman ve malzeme sözleşme satırına eşlenen bir projeye bağlandığında sistem, biri maliyet ve diğeri faturalanmamış satışlar için olmak üzere iki yevmiye defteri satırı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3ec6e-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="3ec6e-124">Sabit fiyat</span><span class="sxs-lookup"><span data-stu-id="3ec6e-124">Fixed price</span></span>

<span data-ttu-id="3ec6e-125">Gönderilen bir temel gider girişi, sabit fiyatlı bir sözleşme satırına eşlenen bir projeye bağlandığında sistem, maliyet için bir yevmiye defteri satırı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3ec6e-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="3ec6e-126">Varsayılan fiyatlandırma</span><span class="sxs-lookup"><span data-stu-id="3ec6e-126">Default pricing</span></span>

<span data-ttu-id="3ec6e-127">Giderler için varsayılan fiyatların girilmesi mantığı, gider kategorisini temel alır.</span><span class="sxs-lookup"><span data-stu-id="3ec6e-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="3ec6e-128">İşlemin tarihini, projenin eşlendiği sözleşme satırı ve ilgili fiyat listesindeki para birimi sonucu uygun fiyat listesini belirlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3ec6e-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="3ec6e-129">Ancak varsayılan olarak fiyatın kendisi için girilen tutar, maliyet ve satışlar için ilgili gider yevmiye defteri satırlarında doğrudan ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="3ec6e-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="3ec6e-130">Gider girişlerinde, birim başına varsayılan fiyatların kategori tabanlı girişi kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="3ec6e-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="3ec6e-131">Maliyetleri kaydetmek için giriş yevmiye defterlerini kullanma</span><span class="sxs-lookup"><span data-stu-id="3ec6e-131">Use entry journals to record costs</span></span>

<span data-ttu-id="3ec6e-132">Giriş yevmiye defterlerini malzeme, ücret, zaman, gider veya vergi işlemi sınıflarında maliyeti veya geliri kaydetmek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3ec6e-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="3ec6e-133">Yevmiye defterleri aşağıdaki amaçlar için kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="3ec6e-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="3ec6e-134">Projedeki gerçek malzeme ve satış maliyetini kaydedin.</span><span class="sxs-lookup"><span data-stu-id="3ec6e-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="3ec6e-135">İşlem gerçek değerlerini başka bir sistemden Microsoft Dynamics 365 Project Operations'a taşıyın.</span><span class="sxs-lookup"><span data-stu-id="3ec6e-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="3ec6e-136">Başka bir sistemde gerçekleşen maliyetleri kaydedin.</span><span class="sxs-lookup"><span data-stu-id="3ec6e-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="3ec6e-137">Bu maliyetler, satın alma veya alt yüklenici maliyetlerini içerebilir.</span><span class="sxs-lookup"><span data-stu-id="3ec6e-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3ec6e-138">Uygulama, yevmiye defteri satırı türünü veya yevmiye defteri satırına girilen ilgili fiyatlandırmayı doğrulamaz.</span><span class="sxs-lookup"><span data-stu-id="3ec6e-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="3ec6e-139">Bu nedenle, yalnızca gerçek değerlerin proje üzerindeki muhasebe etkisinin tam olarak farkında olan bir kullanıcı, gerçek değerleri oluşturmak için giriş yevmiye defterlerini kullanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="3ec6e-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="3ec6e-140">Bu yevmiye defteri türünün etkisi nedeniyle giriş yevmiye defteri oluşturma işlemine kimlerin erişimi olacağını dikkatlice seçmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="3ec6e-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="3ec6e-141">Proje olaylarına göre gerçek değerleri kaydetme</span><span class="sxs-lookup"><span data-stu-id="3ec6e-141">Record actuals based on project events</span></span>

<span data-ttu-id="3ec6e-142">Project Operations, bir proje sırasında gerçekleşen finansal işlemleri kaydeder.</span><span class="sxs-lookup"><span data-stu-id="3ec6e-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="3ec6e-143">Bu işlemler fiili değerler olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="3ec6e-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="3ec6e-144">Aşağıdaki tablolar, projenin zaman ve malzeme veya sabit fiyatlı proje olmasına, ön satış aşamasında bulunmasına veya dahili bir proje olmasına bağlı olarak oluşturulan farklı fiili değer türlerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="3ec6e-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="3ec6e-145">Kaynak, projenin sözleşme birimiyle aynı kuruluş birimine aittir.</span><span class="sxs-lookup"><span data-stu-id="3ec6e-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="3ec6e-146">Olay</span><span class="sxs-lookup"><span data-stu-id="3ec6e-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="3ec6e-147">Faturalandırılabilir veya satılmış proje</span><span class="sxs-lookup"><span data-stu-id="3ec6e-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="3ec6e-148">Ön satış aşamasındaki proje</span><span class="sxs-lookup"><span data-stu-id="3ec6e-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="3ec6e-149">Dahili proje</span><span class="sxs-lookup"><span data-stu-id="3ec6e-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="3ec6e-150">Zaman ve malzemeler</span><span class="sxs-lookup"><span data-stu-id="3ec6e-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="3ec6e-151">Sabit fiyat</span><span class="sxs-lookup"><span data-stu-id="3ec6e-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="3ec6e-152">Gerçekler</span><span class="sxs-lookup"><span data-stu-id="3ec6e-152">Actuals</span></span></th>
<th><span data-ttu-id="3ec6e-153">İşlem para birimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-153">Transaction currency</span></span></th>
<th><span data-ttu-id="3ec6e-154">Sabit fiyat</span><span class="sxs-lookup"><span data-stu-id="3ec6e-154">Fixed price</span></span></th>
<th><span data-ttu-id="3ec6e-155">İşlem para birimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3ec6e-156">Bir zaman girişi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="3ec6e-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="3ec6e-157">Fiili değerler varlığında etkinlik yok</span><span class="sxs-lookup"><span data-stu-id="3ec6e-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ec6e-158">Bir zaman girişi gönderilir.</span><span class="sxs-lookup"><span data-stu-id="3ec6e-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="3ec6e-159">Fiili değerler varlığında etkinlik yok</span><span class="sxs-lookup"><span data-stu-id="3ec6e-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="3ec6e-160">Zaman onaylanır ve onay sırasında faturalanabilir saatlerde değişiklik veya artış yoktur.</span><span class="sxs-lookup"><span data-stu-id="3ec6e-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="3ec6e-161">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="3ec6e-161">Cost actual</span></span></td>
<td><span data-ttu-id="3ec6e-162">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="3ec6e-163">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="3ec6e-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="3ec6e-164">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="3ec6e-165">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="3ec6e-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="3ec6e-166">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="3ec6e-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ec6e-167">Faturalandırılmamış satış fiili değer - Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="3ec6e-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="3ec6e-168">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="3ec6e-169">Zaman onaylanır ve onay sırasında faturalanabilir saatlerde azalma vardır.</span><span class="sxs-lookup"><span data-stu-id="3ec6e-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="3ec6e-170">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="3ec6e-170">Cost actual</span></span></td>
<td><span data-ttu-id="3ec6e-171">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="3ec6e-172">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="3ec6e-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="3ec6e-173">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="3ec6e-174">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="3ec6e-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="3ec6e-175">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="3ec6e-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ec6e-176">Faturalanmamış satış fiili değeri - Yeni miktar için borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="3ec6e-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="3ec6e-177">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ec6e-178">Faturalanmamış satış fiili değeri - Fark için borçlandırılamaz</span><span class="sxs-lookup"><span data-stu-id="3ec6e-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="3ec6e-179">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="3ec6e-180">Bir fatura onaylanır ve onay sırasında faturalanabilir saatlerde değişiklik veya artış yoktur.</span><span class="sxs-lookup"><span data-stu-id="3ec6e-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="3ec6e-181">Faturalanmamış satış geri çevirme</span><span class="sxs-lookup"><span data-stu-id="3ec6e-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="3ec6e-182">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="3ec6e-183">Kilometre taşı için faturalanan satış</span><span class="sxs-lookup"><span data-stu-id="3ec6e-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="3ec6e-184">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="3ec6e-185">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="3ec6e-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="3ec6e-186">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="3ec6e-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ec6e-187">Faturalanan satış</span><span class="sxs-lookup"><span data-stu-id="3ec6e-187">Billed sales</span></span></td>
<td><span data-ttu-id="3ec6e-188">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="3ec6e-189">Bir fatura onaylanır ve onay sırasında faturalanabilir saatlerde azalma vardır.</span><span class="sxs-lookup"><span data-stu-id="3ec6e-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="3ec6e-190">Faturalanmamış satış geri çevirme</span><span class="sxs-lookup"><span data-stu-id="3ec6e-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="3ec6e-191">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="3ec6e-192">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="3ec6e-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="3ec6e-193">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="3ec6e-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="3ec6e-194">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="3ec6e-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="3ec6e-195">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="3ec6e-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ec6e-196">Faturalanan satış - Yeni miktar için borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="3ec6e-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="3ec6e-197">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ec6e-198">Faturalanan satış - Fark için borçlandırılamaz</span><span class="sxs-lookup"><span data-stu-id="3ec6e-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="3ec6e-199">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="3ec6e-200">Borçlandırılabilir miktarı artırmak için fatura düzeltilir.</span><span class="sxs-lookup"><span data-stu-id="3ec6e-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="3ec6e-201">Faturalanan satış - Geri çevirme</span><span class="sxs-lookup"><span data-stu-id="3ec6e-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="3ec6e-202">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="3ec6e-203">Kilometre taşı için faturalanan satış geri çevirme</span><span class="sxs-lookup"><span data-stu-id="3ec6e-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="3ec6e-204">Kilometre taşı durumunda <strong>Faturalandı</strong>yerine <strong>Fatura için hazır</strong> olarak değişiklik</span><span class="sxs-lookup"><span data-stu-id="3ec6e-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="3ec6e-205">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="3ec6e-206">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="3ec6e-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="3ec6e-207">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="3ec6e-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ec6e-208">Faturalanan satış</span><span class="sxs-lookup"><span data-stu-id="3ec6e-208">Billed sales</span></span></td>
<td><span data-ttu-id="3ec6e-209">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="3ec6e-210">Borçlandırılabilir miktarı azaltmak için fatura düzeltilir.</span><span class="sxs-lookup"><span data-stu-id="3ec6e-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="3ec6e-211">Faturalanan satış - Geri çevirme</span><span class="sxs-lookup"><span data-stu-id="3ec6e-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="3ec6e-212">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ec6e-213">Yeni miktar için faturalanan satış</span><span class="sxs-lookup"><span data-stu-id="3ec6e-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="3ec6e-214">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ec6e-215">Faturalanmamış satış - Fark için borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="3ec6e-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="3ec6e-216">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="3ec6e-217">Kaynak, projenin sözleşme biriminden farklı bir kuruluş birimine aittir.</span><span class="sxs-lookup"><span data-stu-id="3ec6e-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="3ec6e-218">Olay</span><span class="sxs-lookup"><span data-stu-id="3ec6e-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="3ec6e-219">Faturalandırılabilir veya satılmış proje</span><span class="sxs-lookup"><span data-stu-id="3ec6e-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="3ec6e-220">Ön satış aşamasındaki proje</span><span class="sxs-lookup"><span data-stu-id="3ec6e-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="3ec6e-221">Dahili proje</span><span class="sxs-lookup"><span data-stu-id="3ec6e-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="3ec6e-222">Zaman ve malzemeler</span><span class="sxs-lookup"><span data-stu-id="3ec6e-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="3ec6e-223">Sabit fiyat</span><span class="sxs-lookup"><span data-stu-id="3ec6e-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="3ec6e-224">Gerçekler</span><span class="sxs-lookup"><span data-stu-id="3ec6e-224">Actuals</span></span></th>
<th><span data-ttu-id="3ec6e-225">İşlem para birimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-225">Transaction currency</span></span></th>
<th><span data-ttu-id="3ec6e-226">Sabit fiyat</span><span class="sxs-lookup"><span data-stu-id="3ec6e-226">Fixed price</span></span></th>
<th><span data-ttu-id="3ec6e-227">İşlem para birimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3ec6e-228">Bir zaman girişi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="3ec6e-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="3ec6e-229">Fiili değerler varlığında etkinlik yok</span><span class="sxs-lookup"><span data-stu-id="3ec6e-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ec6e-230">Bir zaman girişi gönderilir.</span><span class="sxs-lookup"><span data-stu-id="3ec6e-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="3ec6e-231">Fiili değerler varlığında etkinlik yok</span><span class="sxs-lookup"><span data-stu-id="3ec6e-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="3ec6e-232">Zaman onaylanır ve onay sırasında faturalanabilir saatlerde değişiklik veya artış yoktur.</span><span class="sxs-lookup"><span data-stu-id="3ec6e-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="3ec6e-233">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="3ec6e-233">Cost actual</span></span></td>
<td><span data-ttu-id="3ec6e-234">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="3ec6e-235">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="3ec6e-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="3ec6e-236">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="3ec6e-237">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="3ec6e-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="3ec6e-238">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="3ec6e-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ec6e-239">Faturalandırılmamış satış fiili değer - Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="3ec6e-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="3ec6e-240">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ec6e-241">Kaynak belirleme birimi maliyeti</span><span class="sxs-lookup"><span data-stu-id="3ec6e-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="3ec6e-242">Kaynak belirleme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ec6e-243">Kuruluşlar arası satış</span><span class="sxs-lookup"><span data-stu-id="3ec6e-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="3ec6e-244">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="3ec6e-245">Zaman onaylanır ve onay sırasında faturalanabilir saatlerde azalma vardır.</span><span class="sxs-lookup"><span data-stu-id="3ec6e-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="3ec6e-246">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="3ec6e-246">Cost actual</span></span></td>
<td><span data-ttu-id="3ec6e-247">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="3ec6e-248">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="3ec6e-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="3ec6e-249">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="3ec6e-250">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="3ec6e-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="3ec6e-251">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="3ec6e-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ec6e-252">Kaynak belirleme birimi maliyeti</span><span class="sxs-lookup"><span data-stu-id="3ec6e-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="3ec6e-253">Kaynak belirleme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ec6e-254">Kuruluşlar arası satış</span><span class="sxs-lookup"><span data-stu-id="3ec6e-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="3ec6e-255">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ec6e-256">Faturalanmamış satış fiili değeri - Yeni miktar için borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="3ec6e-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="3ec6e-257">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ec6e-258">Faturalanmamış satış fiili değeri - Fark için borçlandırılamaz</span><span class="sxs-lookup"><span data-stu-id="3ec6e-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="3ec6e-259">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="3ec6e-260">Bir fatura onaylanır ve onay sırasında faturalanabilir saatlerde değişiklik veya artış yoktur.</span><span class="sxs-lookup"><span data-stu-id="3ec6e-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="3ec6e-261">Faturalanmamış satış geri çevirme</span><span class="sxs-lookup"><span data-stu-id="3ec6e-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="3ec6e-262">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="3ec6e-263">Kilometre taşı için faturalanan satış</span><span class="sxs-lookup"><span data-stu-id="3ec6e-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="3ec6e-264">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="3ec6e-265">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="3ec6e-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="3ec6e-266">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="3ec6e-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ec6e-267">Faturalanan satış</span><span class="sxs-lookup"><span data-stu-id="3ec6e-267">Billed sales</span></span></td>
<td><span data-ttu-id="3ec6e-268">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="3ec6e-269">Bir fatura onaylanır ve onay sırasında faturalanabilir saatlerde azalma vardır.</span><span class="sxs-lookup"><span data-stu-id="3ec6e-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="3ec6e-270">Faturalanmamış satış geri çevirme</span><span class="sxs-lookup"><span data-stu-id="3ec6e-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="3ec6e-271">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="3ec6e-272">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="3ec6e-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="3ec6e-273">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="3ec6e-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="3ec6e-274">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="3ec6e-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="3ec6e-275">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="3ec6e-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ec6e-276">Faturalanan satış - Yeni miktar için borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="3ec6e-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="3ec6e-277">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ec6e-278">Faturalanan satış - Fark için borçlandırılamaz</span><span class="sxs-lookup"><span data-stu-id="3ec6e-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="3ec6e-279">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="3ec6e-280">Borçlandırılabilir miktarı artırmak için fatura düzeltilir.</span><span class="sxs-lookup"><span data-stu-id="3ec6e-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="3ec6e-281">Faturalanan satış - Geri çevirme</span><span class="sxs-lookup"><span data-stu-id="3ec6e-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="3ec6e-282">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="3ec6e-283">Kilometre taşı için faturalanan satış geri çevirme</span><span class="sxs-lookup"><span data-stu-id="3ec6e-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="3ec6e-284">Kilometre taşı durumunda <strong>Faturalandı</strong>yerine <strong>Fatura için hazır</strong> olarak değişiklik</span><span class="sxs-lookup"><span data-stu-id="3ec6e-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="3ec6e-285">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="3ec6e-286">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="3ec6e-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="3ec6e-287">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="3ec6e-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ec6e-288">Faturalanan satış</span><span class="sxs-lookup"><span data-stu-id="3ec6e-288">Billed sales</span></span></td>
<td><span data-ttu-id="3ec6e-289">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="3ec6e-290">Borçlandırılabilir miktarı azaltmak için fatura düzeltilir.</span><span class="sxs-lookup"><span data-stu-id="3ec6e-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="3ec6e-291">Faturalanan satış - Geri çevirme</span><span class="sxs-lookup"><span data-stu-id="3ec6e-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="3ec6e-292">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ec6e-293">Yeni miktar için faturalanan satış</span><span class="sxs-lookup"><span data-stu-id="3ec6e-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="3ec6e-294">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3ec6e-295">Faturalanmamış satış - Fark için borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="3ec6e-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="3ec6e-296">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="3ec6e-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
