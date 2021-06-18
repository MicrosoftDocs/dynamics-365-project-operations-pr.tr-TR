---
title: Gerçek değerler
description: Bu konuda, Microsoft Dynamics 365 Project Operations'ta gerçek tutarlarla çalışma hakkında bilgiler sağlanmaktadır.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 78c7a9486d0338adfd7770447f21d17509e654f7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996635"
---
# <a name="actuals"></a><span data-ttu-id="00a09-103">Fiili Değerler</span><span class="sxs-lookup"><span data-stu-id="00a09-103">Actuals</span></span> 

<span data-ttu-id="00a09-104">_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="00a09-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="00a09-105">Fiili değerler, projedeki incelenen ve onaylanan finansal ve zamanlama ilerlemesini yansıtır.</span><span class="sxs-lookup"><span data-stu-id="00a09-105">Actuals represent the reviewed and approved financial and schedule progress on a project.</span></span> <span data-ttu-id="00a09-106">Bunlar; zaman, gider, malzeme kullanım girişlerinin ve günlük girişlerinin ve faturaların onaylanmasının bir sonucu olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="00a09-106">They are created as a result of approval of time, expense, material usage entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="00a09-107">Yevmiye defteri satırları ve zaman gönderimi</span><span class="sxs-lookup"><span data-stu-id="00a09-107">Journal lines and time submission</span></span>

<span data-ttu-id="00a09-108">Zaman girişi hakkında daha fazla bilgi için bkz. [Zaman girişine genel bakış](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="00a09-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="00a09-109">Zaman ve malzemeler</span><span class="sxs-lookup"><span data-stu-id="00a09-109">Time and materials</span></span>

<span data-ttu-id="00a09-110">Gönderilen bir zaman girişi, bir zaman ve malzeme sözleşme satırına eşlenen bir projeye bağlandığında sistem, biri maliyet ve diğeri faturalanmamış satışlar için olmak üzere iki yevmiye defteri satırı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="00a09-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="00a09-111">Sabit fiyat</span><span class="sxs-lookup"><span data-stu-id="00a09-111">Fixed price</span></span>

<span data-ttu-id="00a09-112">Gönderilen bir zaman girişi, sabit fiyatlı bir sözleşme satırına eşlenen bir projeye bağlandığında sistem, maliyet için bir yevmiye defteri satırı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="00a09-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="00a09-113">Varsayılan fiyatlandırma</span><span class="sxs-lookup"><span data-stu-id="00a09-113">Default pricing</span></span>

<span data-ttu-id="00a09-114">Varsayılan fiyatların oluşturulacağı mantık, yevmiye defteri satırında yer alır.</span><span class="sxs-lookup"><span data-stu-id="00a09-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="00a09-115">Zaman girişindeki alan değerleri yevmiye defteri satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="00a09-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="00a09-116">Bu değerler; işlem tarihini, projenin eşlendiği sözleşme satırını ve ilgili fiyat listesindeki para birimi sonucunu içerir.</span><span class="sxs-lookup"><span data-stu-id="00a09-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="00a09-117">**Rol** ve **Kaynak Birimi** gibi varsayılan fiyatlandırmayı etkileyen alanlar, günlük satırında uygun fiyatın belirlenmesinde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="00a09-117">The fields that affect default pricing, such as **Role** and **Resourcing Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="00a09-118">Zaman girişine özel bir alan ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="00a09-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="00a09-119">Alan değerinin, fiili değerlere doldurulmasını istiyorsanız bu alanı **Fiili değerler** ve **Yevmiye Defteri Satırı** tablolarında oluşturun.</span><span class="sxs-lookup"><span data-stu-id="00a09-119">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="00a09-120">Seçilen alan değerini, Zaman Girişi'nden Fiili Değerlere hareket kaynaklarını kullanarak yevmiye defteri satırı üzerinden yaymak için özel kod kullanın.</span><span class="sxs-lookup"><span data-stu-id="00a09-120">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="00a09-121">Hareket kaynakları ve bağlantılar hakkında daha fazla bilgi için [Fiili değerleri özgün kayıtlara bağlama konusuna bakın](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="00a09-121">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="00a09-122">Yevmiye defteri satırları ve temel gider gönderimi</span><span class="sxs-lookup"><span data-stu-id="00a09-122">Journal lines and basic expense submission</span></span>

<span data-ttu-id="00a09-123">Gider girişi hakkında daha fazla bilgi için bkz. [Gidere genel bakış](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="00a09-123">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="00a09-124">Zaman ve malzemeler</span><span class="sxs-lookup"><span data-stu-id="00a09-124">Time and materials</span></span>

<span data-ttu-id="00a09-125">Gönderilen bir temel gider girişi, bir zaman ve malzeme sözleşme satırına eşlenen bir projeye bağlandığında sistem, biri maliyet ve diğeri faturalanmamış satışlar için olmak üzere iki yevmiye defteri satırı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="00a09-125">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="00a09-126">Sabit fiyat</span><span class="sxs-lookup"><span data-stu-id="00a09-126">Fixed price</span></span>

<span data-ttu-id="00a09-127">Gönderilen gider girişi, sabit fiyat sözleşme satırıyla eşlenen bir projeye bağlandığında sistem, maliyet için bir yevmiye defteri satırı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="00a09-127">When a submitted basic expense entry is linked to a project that's mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="00a09-128">Varsayılan fiyatlandırma</span><span class="sxs-lookup"><span data-stu-id="00a09-128">Default pricing</span></span>

<span data-ttu-id="00a09-129">Giderler için varsayılan fiyatların girilmesi mantığı, gider kategorisini temel alır.</span><span class="sxs-lookup"><span data-stu-id="00a09-129">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="00a09-130">İşlemin tarihini, projenin eşlendiği sözleşme satırı ve ilgili fiyat listesindeki para birimi sonucu uygun fiyat listesini belirlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="00a09-130">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="00a09-131">**Hareket Kategorisi** ve **Birim** gibi varsayılan fiyatlandırmayı etkileyen alanlar, yevmiye defteri satırında uygun fiyatın belirlenmesinde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="00a09-131">The fields that affect default pricing, such as **Transaction Category** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="00a09-132">Ancak, bu yalnızca fiyat listesindeki fiyatlandırma yöntemi **Birim başına fiyat** olduğunda çalışır.</span><span class="sxs-lookup"><span data-stu-id="00a09-132">However, this only works when the pricing method in the price list is **Price per unit**.</span></span> <span data-ttu-id="00a09-133">Fiyatlandırma yöntemi **Maliyette** veya **Maliyet üzerinden kar payı** ise maliyet için masraf girişi oluşturulduğunda girilen fiyat kullanılır ve Satış yevmiye defteri satırındaki fiyat, fiyatlandırma yöntemi temel alınarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="00a09-133">If pricing method is **At cost** or **Markup over cost**, the price entered when the expense entry is created is used for cost and the price on the sales journal line is calculated based on the pricing method.</span></span> 

<span data-ttu-id="00a09-134">Gider girişinde bir özel alan ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="00a09-134">You can add a custom field on the expense entry.</span></span> <span data-ttu-id="00a09-135">Alan değerinin, fiili değerlere doldurulmasını istiyorsanız bu alanı **Fiili değerler** ve **Yevmiye Defteri Satırı** tablolarında oluşturun.</span><span class="sxs-lookup"><span data-stu-id="00a09-135">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="00a09-136">Seçilen alan değerini, Zaman Girişi'nden Fiili Değerlere hareket kaynaklarını kullanarak yevmiye defteri satırı üzerinden yaymak için özel kod kullanın.</span><span class="sxs-lookup"><span data-stu-id="00a09-136">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="00a09-137">Hareket kaynakları ve bağlantılar hakkında daha fazla bilgi için [Fiili değerleri özgün kayıtlara bağlama konusuna bakın](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="00a09-137">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-material-usage-log-submission"></a><span data-ttu-id="00a09-138">Günlük satırları ve malzeme kullanım günlüğü gönderimi</span><span class="sxs-lookup"><span data-stu-id="00a09-138">Journal lines and material usage log submission</span></span>

<span data-ttu-id="00a09-139">Gider girişi hakkında daha fazla bilgi için [Malzeme Kullanımı Günlüğü konusuna bakın](../material/material-usage-log.md).</span><span class="sxs-lookup"><span data-stu-id="00a09-139">For more information about expense entry, see [Material Usage Log](../material/material-usage-log.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="00a09-140">Zaman ve malzemeler</span><span class="sxs-lookup"><span data-stu-id="00a09-140">Time and materials</span></span>

<span data-ttu-id="00a09-141">Gönderilen malzeme kullanım günlüğü girişi bir zaman ve malzeme sözleşmesi satırıyla eşlenen bir projeye bağlandığında, sistem biri maliyet ve biri faturalanmamış satış için olmak üzere iki yevmiye defteri satırı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="00a09-141">When a submitted material usage log entry is linked to a project that is mapped to a time and materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="00a09-142">Sabit fiyat</span><span class="sxs-lookup"><span data-stu-id="00a09-142">Fixed price</span></span>

<span data-ttu-id="00a09-143">Gönderilen malzeme kullanımı günlüğü girişi, sabit fiyat sözleşme satırıyla eşlenen bir projeye bağlandığında sistem, maliyet için bir yevmiye defteri satırı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="00a09-143">When a submitted material usage log entry is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="00a09-144">Varsayılan fiyatlandırma</span><span class="sxs-lookup"><span data-stu-id="00a09-144">Default pricing</span></span>

<span data-ttu-id="00a09-145">Malzemenin varsayılan fiyatlarını girme mantığı, ürün ve birim birleşimine dayanır.</span><span class="sxs-lookup"><span data-stu-id="00a09-145">The logic for entering default prices for material is based on the product and unit combination.</span></span> <span data-ttu-id="00a09-146">İşlemin tarihini, projenin eşlendiği sözleşme satırı ve ilgili fiyat listesindeki para birimi sonucu uygun fiyat listesini belirlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="00a09-146">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="00a09-147">**Ürün Kimliği** ve **Birim** gibi varsayılan fiyatlandırmayı etkileyen alanlar, günlük satırında uygun fiyatın belirlenmesinde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="00a09-147">The fields that affect default pricing, such as **Product ID** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="00a09-148">Ancak bu yalnızca katalog ürünleri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="00a09-148">However, this only works for catalog products.</span></span> <span data-ttu-id="00a09-149">Serbest ürünler için kullanım kütüğü girişi oluşturulduğunda girilen fiyat, yevmiye defteri satırlarındaki maliyet ve satış fiyatı için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="00a09-149">For write-in products, the price entered when the material usage log entry is created is used for cost and sales price on the journal lines.</span></span> 

<span data-ttu-id="00a09-150">**Malzeme Kullanımı Günlüğü** girişinde bir özel alan ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="00a09-150">You can add a custom field on the **Material Usage Log** entry.</span></span> <span data-ttu-id="00a09-151">Alan değerinin, fiili değerlere doldurulmasını istiyorsanız bu alanı **Fiili değerler** ve **Yevmiye Defteri Satırı** tablolarında oluşturun.</span><span class="sxs-lookup"><span data-stu-id="00a09-151">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="00a09-152">Seçilen alan değerini, Zaman Girişi'nden Fiili Değerlere hareket kaynaklarını kullanarak yevmiye defteri satırı üzerinden yaymak için özel kod kullanın.</span><span class="sxs-lookup"><span data-stu-id="00a09-152">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="00a09-153">Hareket kaynakları ve bağlantılar hakkında daha fazla bilgi için [Fiili değerleri özgün kayıtlara bağlama konusuna bakın](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="00a09-153">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="00a09-154">Maliyetleri kaydetmek için giriş yevmiye defterlerini kullanma</span><span class="sxs-lookup"><span data-stu-id="00a09-154">Use entry journals to record costs</span></span>

<span data-ttu-id="00a09-155">Giriş yevmiye defterlerini malzeme, ücret, zaman, gider veya vergi işlemi sınıflarında maliyeti veya geliri kaydetmek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="00a09-155">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="00a09-156">Yevmiye defterleri aşağıdaki amaçlar için kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="00a09-156">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="00a09-157">İşlem gerçek tutarlarını başka bir sistemden Microsoft Dynamics 365 Project Operations'a taşıyın.</span><span class="sxs-lookup"><span data-stu-id="00a09-157">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="00a09-158">Başka bir sistemde gerçekleşen maliyetleri kaydedin.</span><span class="sxs-lookup"><span data-stu-id="00a09-158">Record costs that occurred in another system.</span></span> <span data-ttu-id="00a09-159">Bu maliyetler, satın alma veya alt yüklenici maliyetlerini içerebilir.</span><span class="sxs-lookup"><span data-stu-id="00a09-159">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="00a09-160">Uygulama, yevmiye defteri satırı türünü veya yevmiye defteri satırına girilen ilgili fiyatlandırmayı doğrulamaz.</span><span class="sxs-lookup"><span data-stu-id="00a09-160">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="00a09-161">Bu nedenle, yalnızca gerçek değerlerin proje üzerindeki muhasebe etkisinin tam olarak farkında olan bir kullanıcı, gerçek değerleri oluşturmak için giriş yevmiye defterlerini kullanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="00a09-161">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="00a09-162">Bu yevmiye defteri türünün etkisi nedeniyle giriş yevmiye defteri oluşturma işlemine kimlerin erişimi olacağını dikkatlice seçmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="00a09-162">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>

## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="00a09-163">Proje olaylarına göre gerçek değerleri kaydetme</span><span class="sxs-lookup"><span data-stu-id="00a09-163">Record actuals based on project events</span></span>

<span data-ttu-id="00a09-164">Project Operations, bir proje sırasında gerçekleşen finansal işlemleri kaydeder.</span><span class="sxs-lookup"><span data-stu-id="00a09-164">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="00a09-165">Bu işlemler fiili değerler olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="00a09-165">These transactions are recorded as actuals.</span></span> <span data-ttu-id="00a09-166">Aşağıdaki tablolar, projenin zaman ve malzeme veya sabit fiyatlı proje olmasına, ön satış aşamasında bulunmasına veya dahili bir proje olmasına bağlı olarak oluşturulan farklı fiili değer türlerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="00a09-166">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="00a09-167">Kaynak, projenin sözleşme birimiyle aynı kuruluş birimine aittir.</span><span class="sxs-lookup"><span data-stu-id="00a09-167">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="00a09-168">Olay</span><span class="sxs-lookup"><span data-stu-id="00a09-168">Event</span></span></th>
<th colspan="4"><span data-ttu-id="00a09-169">Faturalandırılabilir veya satılmış proje</span><span class="sxs-lookup"><span data-stu-id="00a09-169">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="00a09-170">Ön satış aşamasındaki proje</span><span class="sxs-lookup"><span data-stu-id="00a09-170">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="00a09-171">Dahili proje</span><span class="sxs-lookup"><span data-stu-id="00a09-171">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="00a09-172">Zaman ve malzemeler</span><span class="sxs-lookup"><span data-stu-id="00a09-172">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="00a09-173">Sabit fiyat</span><span class="sxs-lookup"><span data-stu-id="00a09-173">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="00a09-174">Gerçekler</span><span class="sxs-lookup"><span data-stu-id="00a09-174">Actuals</span></span></th>
<th><span data-ttu-id="00a09-175">İşlem para birimi</span><span class="sxs-lookup"><span data-stu-id="00a09-175">Transaction currency</span></span></th>
<th><span data-ttu-id="00a09-176">Sabit fiyat</span><span class="sxs-lookup"><span data-stu-id="00a09-176">Fixed price</span></span></th>
<th><span data-ttu-id="00a09-177">İşlem para birimi</span><span class="sxs-lookup"><span data-stu-id="00a09-177">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="00a09-178">Bir zaman girişi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="00a09-178">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="00a09-179">Fiili değerler varlığında etkinlik yok</span><span class="sxs-lookup"><span data-stu-id="00a09-179">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="00a09-180">Bir zaman girişi gönderilir.</span><span class="sxs-lookup"><span data-stu-id="00a09-180">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="00a09-181">Fiili değerler varlığında etkinlik yok</span><span class="sxs-lookup"><span data-stu-id="00a09-181">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="00a09-182">Zaman onaylanır ve onay sırasında faturalanabilir saatlerde değişiklik veya artış yoktur.</span><span class="sxs-lookup"><span data-stu-id="00a09-182">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="00a09-183">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="00a09-183">Cost actual</span></span></td>
<td><span data-ttu-id="00a09-184">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="00a09-184">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="00a09-185">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="00a09-185">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="00a09-186">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="00a09-186">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="00a09-187">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="00a09-187">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="00a09-188">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="00a09-188">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="00a09-189">Faturalanmayan satış gerçek değeri - Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="00a09-189">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="00a09-190">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="00a09-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="00a09-191">Zaman onaylanır ve onay sırasında faturalanabilir saatlerde azalma vardır.</span><span class="sxs-lookup"><span data-stu-id="00a09-191">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="00a09-192">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="00a09-192">Cost actual</span></span></td>
<td><span data-ttu-id="00a09-193">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="00a09-193">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="00a09-194">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="00a09-194">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="00a09-195">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="00a09-195">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="00a09-196">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="00a09-196">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="00a09-197">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="00a09-197">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="00a09-198">Faturalanmamış satış fiili değeri - Yeni miktar için borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="00a09-198">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="00a09-199">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="00a09-199">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="00a09-200">Faturalanmamış satış fiili değeri - Fark için borçlandırılamaz</span><span class="sxs-lookup"><span data-stu-id="00a09-200">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="00a09-201">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="00a09-201">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="00a09-202">Bir fatura onaylanır ve onay sırasında faturalanabilir saatlerde değişiklik veya artış yoktur.</span><span class="sxs-lookup"><span data-stu-id="00a09-202">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="00a09-203">Faturalanmamış satış geri çevirme</span><span class="sxs-lookup"><span data-stu-id="00a09-203">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="00a09-204">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="00a09-204">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="00a09-205">Kilometre taşı için faturalanan satış</span><span class="sxs-lookup"><span data-stu-id="00a09-205">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="00a09-206">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="00a09-206">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="00a09-207">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="00a09-207">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="00a09-208">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="00a09-208">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="00a09-209">Faturalanan satış</span><span class="sxs-lookup"><span data-stu-id="00a09-209">Billed sales</span></span></td>
<td><span data-ttu-id="00a09-210">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="00a09-210">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="00a09-211">Bir fatura onaylanır ve onay sırasında faturalanabilir saatlerde azalma vardır.</span><span class="sxs-lookup"><span data-stu-id="00a09-211">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="00a09-212">Faturalanmamış satış geri çevirme</span><span class="sxs-lookup"><span data-stu-id="00a09-212">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="00a09-213">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="00a09-213">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="00a09-214">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="00a09-214">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="00a09-215">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="00a09-215">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="00a09-216">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="00a09-216">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="00a09-217">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="00a09-217">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="00a09-218">Faturalanan satış - Yeni miktar için borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="00a09-218">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="00a09-219">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="00a09-219">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="00a09-220">Faturalanan satış - Fark için borçlandırılamaz</span><span class="sxs-lookup"><span data-stu-id="00a09-220">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="00a09-221">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="00a09-221">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="00a09-222">Borçlandırılabilir miktarı artırmak için fatura düzeltilir.</span><span class="sxs-lookup"><span data-stu-id="00a09-222">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="00a09-223">Faturalanan satış - Geri çevirme</span><span class="sxs-lookup"><span data-stu-id="00a09-223">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="00a09-224">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="00a09-224">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="00a09-225">Kilometre taşı için faturalanan satış geri çevirme</span><span class="sxs-lookup"><span data-stu-id="00a09-225">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="00a09-226">Kilometre taşı durumunda <strong>Faturalandı</strong>yerine <strong>Fatura için hazır</strong> olarak değişiklik</span><span class="sxs-lookup"><span data-stu-id="00a09-226">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="00a09-227">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="00a09-227">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="00a09-228">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="00a09-228">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="00a09-229">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="00a09-229">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="00a09-230">Faturalanan satış</span><span class="sxs-lookup"><span data-stu-id="00a09-230">Billed sales</span></span></td>
<td><span data-ttu-id="00a09-231">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="00a09-231">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="00a09-232">Borçlandırılabilir miktarı azaltmak için fatura düzeltilir.</span><span class="sxs-lookup"><span data-stu-id="00a09-232">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="00a09-233">Faturalanan satış - Geri çevirme</span><span class="sxs-lookup"><span data-stu-id="00a09-233">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="00a09-234">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="00a09-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="00a09-235">Yeni miktar için faturalanan satış</span><span class="sxs-lookup"><span data-stu-id="00a09-235">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="00a09-236">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="00a09-236">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="00a09-237">Faturalanmamış satış - Fark için borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="00a09-237">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="00a09-238">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="00a09-238">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="00a09-239">Kaynak, projenin sözleşme biriminden farklı bir kuruluş birimine aittir.</span><span class="sxs-lookup"><span data-stu-id="00a09-239">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="00a09-240">Olay</span><span class="sxs-lookup"><span data-stu-id="00a09-240">Event</span></span></th>
<th colspan="4"><span data-ttu-id="00a09-241">Faturalandırılabilir veya satılmış proje</span><span class="sxs-lookup"><span data-stu-id="00a09-241">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="00a09-242">Ön satış aşamasındaki proje</span><span class="sxs-lookup"><span data-stu-id="00a09-242">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="00a09-243">Dahili proje</span><span class="sxs-lookup"><span data-stu-id="00a09-243">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="00a09-244">Zaman ve malzemeler</span><span class="sxs-lookup"><span data-stu-id="00a09-244">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="00a09-245">Sabit fiyat</span><span class="sxs-lookup"><span data-stu-id="00a09-245">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="00a09-246">Gerçekler</span><span class="sxs-lookup"><span data-stu-id="00a09-246">Actuals</span></span></th>
<th><span data-ttu-id="00a09-247">İşlem para birimi</span><span class="sxs-lookup"><span data-stu-id="00a09-247">Transaction currency</span></span></th>
<th><span data-ttu-id="00a09-248">Sabit fiyat</span><span class="sxs-lookup"><span data-stu-id="00a09-248">Fixed price</span></span></th>
<th><span data-ttu-id="00a09-249">İşlem para birimi</span><span class="sxs-lookup"><span data-stu-id="00a09-249">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="00a09-250">Bir zaman girişi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="00a09-250">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="00a09-251">Fiili değerler varlığında etkinlik yok</span><span class="sxs-lookup"><span data-stu-id="00a09-251">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="00a09-252">Bir zaman girişi gönderilir.</span><span class="sxs-lookup"><span data-stu-id="00a09-252">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="00a09-253">Fiili değerler varlığında etkinlik yok</span><span class="sxs-lookup"><span data-stu-id="00a09-253">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="00a09-254">Zaman onaylanır ve onay sırasında faturalanabilir saatlerde değişiklik veya artış yoktur.</span><span class="sxs-lookup"><span data-stu-id="00a09-254">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="00a09-255">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="00a09-255">Cost actual</span></span></td>
<td><span data-ttu-id="00a09-256">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="00a09-256">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="00a09-257">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="00a09-257">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="00a09-258">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="00a09-258">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="00a09-259">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="00a09-259">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="00a09-260">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="00a09-260">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="00a09-261">Faturalanmayan satış gerçek değeri - Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="00a09-261">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="00a09-262">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="00a09-262">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="00a09-263">Kaynak belirleme birimi maliyeti</span><span class="sxs-lookup"><span data-stu-id="00a09-263">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="00a09-264">Kaynak belirleme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="00a09-264">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="00a09-265">Kuruluşlar arası satış</span><span class="sxs-lookup"><span data-stu-id="00a09-265">Interorganizational sales</span></span></td>
<td><span data-ttu-id="00a09-266">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="00a09-266">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="00a09-267">Zaman onaylanır ve onay sırasında faturalanabilir saatlerde azalma vardır.</span><span class="sxs-lookup"><span data-stu-id="00a09-267">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="00a09-268">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="00a09-268">Cost actual</span></span></td>
<td><span data-ttu-id="00a09-269">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="00a09-269">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="00a09-270">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="00a09-270">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="00a09-271">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="00a09-271">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="00a09-272">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="00a09-272">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="00a09-273">Maliyet fiili değeri</span><span class="sxs-lookup"><span data-stu-id="00a09-273">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="00a09-274">Kaynak belirleme birimi maliyeti</span><span class="sxs-lookup"><span data-stu-id="00a09-274">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="00a09-275">Kaynak belirleme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="00a09-275">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="00a09-276">Kuruluşlar arası satış</span><span class="sxs-lookup"><span data-stu-id="00a09-276">Interorganizational sales</span></span></td>
<td><span data-ttu-id="00a09-277">Sözleşme birimi para birimi</span><span class="sxs-lookup"><span data-stu-id="00a09-277">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="00a09-278">Faturalanmamış satış fiili değeri - Yeni miktar için borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="00a09-278">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="00a09-279">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="00a09-279">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="00a09-280">Faturalanmamış satış fiili değeri - Fark için borçlandırılamaz</span><span class="sxs-lookup"><span data-stu-id="00a09-280">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="00a09-281">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="00a09-281">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="00a09-282">Bir fatura onaylanır ve onay sırasında faturalanabilir saatlerde değişiklik veya artış yoktur.</span><span class="sxs-lookup"><span data-stu-id="00a09-282">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="00a09-283">Faturalanmamış satış geri çevirme</span><span class="sxs-lookup"><span data-stu-id="00a09-283">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="00a09-284">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="00a09-284">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="00a09-285">Kilometre taşı için faturalanan satış</span><span class="sxs-lookup"><span data-stu-id="00a09-285">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="00a09-286">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="00a09-286">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="00a09-287">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="00a09-287">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="00a09-288">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="00a09-288">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="00a09-289">Faturalanan satış</span><span class="sxs-lookup"><span data-stu-id="00a09-289">Billed sales</span></span></td>
<td><span data-ttu-id="00a09-290">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="00a09-290">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="00a09-291">Bir fatura onaylanır ve onay sırasında faturalanabilir saatlerde azalma vardır.</span><span class="sxs-lookup"><span data-stu-id="00a09-291">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="00a09-292">Faturalanmamış satış geri çevirme</span><span class="sxs-lookup"><span data-stu-id="00a09-292">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="00a09-293">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="00a09-293">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="00a09-294">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="00a09-294">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="00a09-295">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="00a09-295">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="00a09-296">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="00a09-296">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="00a09-297">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="00a09-297">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="00a09-298">Faturalanan satış - Yeni miktar için borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="00a09-298">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="00a09-299">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="00a09-299">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="00a09-300">Faturalanan satış - Fark için borçlandırılamaz</span><span class="sxs-lookup"><span data-stu-id="00a09-300">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="00a09-301">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="00a09-301">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="00a09-302">Borçlandırılabilir miktarı artırmak için fatura düzeltilir.</span><span class="sxs-lookup"><span data-stu-id="00a09-302">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="00a09-303">Faturalanan satış - Geri çevirme</span><span class="sxs-lookup"><span data-stu-id="00a09-303">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="00a09-304">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="00a09-304">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="00a09-305">Kilometre taşı için faturalanan satış geri çevirme</span><span class="sxs-lookup"><span data-stu-id="00a09-305">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="00a09-306">Kilometre taşı durumunda <strong>Faturalandı</strong>yerine <strong>Fatura için hazır</strong> olarak değişiklik</span><span class="sxs-lookup"><span data-stu-id="00a09-306">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="00a09-307">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="00a09-307">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="00a09-308">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="00a09-308">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="00a09-309">Uygulanamaz</span><span class="sxs-lookup"><span data-stu-id="00a09-309">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="00a09-310">Faturalanan satış</span><span class="sxs-lookup"><span data-stu-id="00a09-310">Billed sales</span></span></td>
<td><span data-ttu-id="00a09-311">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="00a09-311">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="00a09-312">Borçlandırılabilir miktarı azaltmak için fatura düzeltilir.</span><span class="sxs-lookup"><span data-stu-id="00a09-312">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="00a09-313">Faturalanan satış - Geri çevirme</span><span class="sxs-lookup"><span data-stu-id="00a09-313">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="00a09-314">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="00a09-314">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="00a09-315">Yeni miktar için faturalanan satış</span><span class="sxs-lookup"><span data-stu-id="00a09-315">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="00a09-316">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="00a09-316">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="00a09-317">Faturalanmamış satış - Fark için borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="00a09-317">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="00a09-318">Proje sözleşmesi para birimi</span><span class="sxs-lookup"><span data-stu-id="00a09-318">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
