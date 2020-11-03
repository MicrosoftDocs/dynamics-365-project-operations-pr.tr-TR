---
title: Proje tabanlı teklif satırları (Pro)
description: Bu konuda, proje çalışmaları için proje tabanlı teklif satırlarını kullanma hakkında bilgiler sağlanmaktadır. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a409d1e378afe97de7fb6c77cf3ad6703661bdff
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086254"
---
# <a name="project-based-quote-lines-pro"></a><span data-ttu-id="2e4d0-104">Proje tabanlı teklif satırları (Pro)</span><span class="sxs-lookup"><span data-stu-id="2e4d0-104">Project-based quote lines (Pro)</span></span>

<span data-ttu-id="2e4d0-105">_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_</span><span class="sxs-lookup"><span data-stu-id="2e4d0-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2e4d0-106">Proje tabanlı teklif satırları, bir etkileşimdeki proje çalışmalarının tahmin edilmesine yardımcı olmak için tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="2e4d0-107">Proje tabanlı teklif satırının yapısı, aşağıdaki kavramlarla proje tahminleri için genişletilmiştir:</span><span class="sxs-lookup"><span data-stu-id="2e4d0-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="2e4d0-108">Faturalama Yöntemi</span><span class="sxs-lookup"><span data-stu-id="2e4d0-108">Billing Method</span></span>
- <span data-ttu-id="2e4d0-109">Proje ve Görev Eşleme</span><span class="sxs-lookup"><span data-stu-id="2e4d0-109">Project and Task Mapping</span></span>
- <span data-ttu-id="2e4d0-110">Dahil Edilen İşlem sınıfları</span><span class="sxs-lookup"><span data-stu-id="2e4d0-110">Included Transaction classes</span></span>
- <span data-ttu-id="2e4d0-111">Aşılamaz Limit</span><span class="sxs-lookup"><span data-stu-id="2e4d0-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="2e4d0-112">Borçlandırılabilirlik ayarı</span><span class="sxs-lookup"><span data-stu-id="2e4d0-112">Chargeability setup</span></span>
- <span data-ttu-id="2e4d0-113">Teklif Satırı Ayrıntılarını kullanarak tahmin yürütme</span><span class="sxs-lookup"><span data-stu-id="2e4d0-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="2e4d0-114">Teklif satırı Müşterileri</span><span class="sxs-lookup"><span data-stu-id="2e4d0-114">Quote line Customers</span></span>

<span data-ttu-id="2e4d0-115">Aşağıdaki tabloda proje tabanlı teklif satırının **Genel** sekmesindeki alanlar hakkında bilgi sağlanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="2e4d0-116">Bu alanlar, proje çalışmaları için ayrıntılı, baştan sona bir tahmin için temel oluşturulmasına yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="2e4d0-117">**Alan**</span><span class="sxs-lookup"><span data-stu-id="2e4d0-117">**Field**</span></span> | <span data-ttu-id="2e4d0-118">**İlgi, amaç ve kılavuz**</span><span class="sxs-lookup"><span data-stu-id="2e4d0-118">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="2e4d0-119">**Aşağı yönlü etki**</span><span class="sxs-lookup"><span data-stu-id="2e4d0-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="2e4d0-120">Veri Akışı Adı</span><span class="sxs-lookup"><span data-stu-id="2e4d0-120">Name</span></span> | <span data-ttu-id="2e4d0-121">Tahmin edilen teklifin farklı olan bileşenini belirlemenize yardımcı olması gereken teklif satırının adı.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="2e4d0-122">Teklif kazanıldığında, bu teklif satırından oluşturulan proje sözleşme satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2e4d0-123">Faturalama Yöntemi</span><span class="sxs-lookup"><span data-stu-id="2e4d0-123">Billing Method</span></span> | <span data-ttu-id="2e4d0-124">Fırsattan oluşturulan bir teklifte bu değer, fırsat satırındaki ilgili alandan kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="2e4d0-125">Bu alan, Dynamics 365 Project Operations tarafından desteklenen iki ana sözleşme modelini içerir:</span><span class="sxs-lookup"><span data-stu-id="2e4d0-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="2e4d0-126">- Sabit fiyat</span><span class="sxs-lookup"><span data-stu-id="2e4d0-126">- Fixed price</span></span></br><span data-ttu-id="2e4d0-127">- Zaman ve malzeme.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-127">- Time and material.</span></span>| <span data-ttu-id="2e4d0-128">Bu alanın değeri, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşme satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2e4d0-129">Project</span><span class="sxs-lookup"><span data-stu-id="2e4d0-129">Project</span></span> | <span data-ttu-id="2e4d0-130">Bu etkileşimde kullanılacak projeyi belirleyerek çalışmayı teslim etmek için bu isteğe bağlı alanı kullanın.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="2e4d0-131">Proje bir teklif satırına eşlendiğinde, borçlandırılabilir görevler oluşturulmasına ve ayrıca proje bazlı bir tahminin teklif satırına teklif satırı ayrıntıları olarak getirilmesine yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="2e4d0-132">Proje, proje bazlı bir teklif satırına eşlenmediğinde tahmin, her bir teklif satırı ayrıntısının el ile oluşturulmasıyla elde edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="2e4d0-133">Bu alanın değeri, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşme satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="2e4d0-134">Dahil Edilen Görevler</span><span class="sxs-lookup"><span data-stu-id="2e4d0-134">Included Tasks</span></span> | <span data-ttu-id="2e4d0-135">Bu teklif satırının seçilen projenin görevlerinin tümünde veya bazılarında kullanılıp kullanılmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="2e4d0-136">Bu alan aşağıdaki olası değerlere sahiptir:</span><span class="sxs-lookup"><span data-stu-id="2e4d0-136">This field has the following possible values:</span></span></br><span data-ttu-id="2e4d0-137">- Tüm proje görevleri</span><span class="sxs-lookup"><span data-stu-id="2e4d0-137">- All project tasks</span></span></br><span data-ttu-id="2e4d0-138">- Yalnızca seçili proje görevleri</span><span class="sxs-lookup"><span data-stu-id="2e4d0-138">- Selected project tasks only</span></span></br><span data-ttu-id="2e4d0-139">Bu alandaki boş bir değer **Tüm proje görevleri** seçeneğinin eşdeğeridir.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="2e4d0-140">Proje sayfasında **Yalnızca seçili proje görevleri** seçildiğinde, **Görev faturalama ayarları** sekmesi belirli görevleri, bu teklif satırıyla ilişkilendirmek için seçmenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="2e4d0-141">Bu alanın değeri, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşme satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2e4d0-142">Zaman Ekle</span><span class="sxs-lookup"><span data-stu-id="2e4d0-142">Include Time</span></span> | <span data-ttu-id="2e4d0-143">**Evet**/**Hayır** bayrağı, seçilen projedeki zaman işlemlerinin veya işçilik maliyetlerinin bu teklif satırındaki tahmine dahil edilip edilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="2e4d0-144">**Hayır** değeri, zaman işlemlerinin veya işçilik maliyetinin bu teklif satırındaki tahmine dahil edilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="2e4d0-145">**Evet** değeri, zaman işlemlerinin veya işçilik maliyetinin bu teklif satırındaki tahmine dahil edileceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="2e4d0-146">Bu alanın değeri, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşme satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2e4d0-147">Gider Ekle</span><span class="sxs-lookup"><span data-stu-id="2e4d0-147">Include Expense</span></span> | <span data-ttu-id="2e4d0-148">**Evet**/**Hayır** bayrağı, seçilen projedeki gider maliyetlerinin bu teklif satırındaki tahmine dahil edilip edilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="2e4d0-149">**Hayır** değeri, gider maliyetinin bu teklif satırındaki tahmine dahil edilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="2e4d0-150">**Evet** değeri, gider maliyetinin bu teklif satırındaki tahmine dahil edileceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="2e4d0-151">Bu alanın değeri, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşme satırının üzerine kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2e4d0-152">Ücret Ekle</span><span class="sxs-lookup"><span data-stu-id="2e4d0-152">Include Fee</span></span> | <span data-ttu-id="2e4d0-153">**Evet**/**Hayır** bayrağı, seçilen projedeki ücretlerin bu teklif satırındaki tahmine dahil edilip edilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="2e4d0-154">**Hayır** değeri, Ücretlerin bu teklif satırındaki tahmine dahil edilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="2e4d0-155">**Evet** değeri, Ücretlerin bu teklif satırındaki tahmine dahil edileceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="2e4d0-156">Bu alanın değeri, teklif kazanıldığında bu teklif satırından oluşturulan Proje sözleşme satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2e4d0-157">Teklif Edilen Tutar</span><span class="sxs-lookup"><span data-stu-id="2e4d0-157">Quoted Amount</span></span> | <span data-ttu-id="2e4d0-158">Bu, proje tabanlı teklif satırında tahmin edilen tüm çalışmalar için müşteriye teklif edilecek tutardır.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="2e4d0-159">Fırsattan oluşturulan bir teklifte, bu değer fırsat satırındaki **Müşteri Bütçesi** alanından kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="2e4d0-160">Proje tabanlı teklif satırı satır ayrıntılarına sahip olduğunda, bu alan düzenlemeye kilitlenir ve teklif satırı ayrıntılarındaki tutardan özetlenir.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="2e4d0-161">Bu alanın değeri, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşme satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2e4d0-162">Tahmini Vergi</span><span class="sxs-lookup"><span data-stu-id="2e4d0-162">Estimated Tax</span></span> | <span data-ttu-id="2e4d0-163">Bu, kullanıcının teklif satırına tahmini vergi tutarını ekleyebileceği düzenlenebilir bir alandır.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="2e4d0-164">Proje tabanlı teklif satırı, satır ayrıntılarına sahip olduğunda, bu alan düzenlemeye kilitlenir ve teklif satırı ayrıntılarındaki vergi tutarından özetlenir.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="2e4d0-165">Bu alanın değeri, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşme satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2e4d0-166">Vergi Sonrası Teklif Tutarı</span><span class="sxs-lookup"><span data-stu-id="2e4d0-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="2e4d0-167">Bu alan, vergi sonrası teklif satırı tutarıdır ve salt okunurdur.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="2e4d0-168">Bu alandaki tutar *Teklif Tutarı + Vergi* olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="2e4d0-169">Bu alanın değeri, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşme satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2e4d0-170">Aşılamaz Limit</span><span class="sxs-lookup"><span data-stu-id="2e4d0-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="2e4d0-171">Bu alan, düzenlenebilirdir ve yalnızca **Zaman ve Malzeme** faturalama yöntemine sahip proje bazlı teklif satırlarında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="2e4d0-172">Bu alanın değeri, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşme satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2e4d0-173">Müşteri Bütçesi</span><span class="sxs-lookup"><span data-stu-id="2e4d0-173">Customer Budget</span></span> | <span data-ttu-id="2e4d0-174">Bu alan, düzenlenebilirdir ve teklif bir fırsattan oluşturulmuşsa fırsat satırındaki ilgili alandan kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="2e4d0-175">Bu alanın değeri, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşme satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="2e4d0-176">Proje tabanlı teklif satırlarının Genel sekmesindeki alanları için doğrulama kuralları</span><span class="sxs-lookup"><span data-stu-id="2e4d0-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="2e4d0-177">**Kural 1** : **Eklenen Görevler** alanı boşsa veya bu alan **Tüm proje görevleri** olarak ayarlanmışsa teklif satırına bir proje dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-177">**Rule 1** : If the **Included Tasks** field is blank, or if it is set to **All project tasks** , a project is included in the quote line.</span></span>

<span data-ttu-id="2e4d0-178">**Kural 2** : **Eklenen Görevler** alanı boşsa veya bu alan **Tüm proje görevleri** olarak ayarlanmışsa bir proje ve belirli bir işlem sınıfı, bir teklifin yalnızca proje tabanlı bir teklif satırına dahil edilebilir.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-178">**Rule 2** : If the **Included Tasks** field is blank, or if it is set to **All project tasks** , a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="2e4d0-179">**Kural 3** : **Eklenen Görevler** alanı **Yalnızca seçili proje görevleri** olarak ayarlanmışsa bir proje ve belirli bir işlem sınıfı, bir teklifin birden çok proje tabanlı teklif satırına dahil edilebilir.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-179">**Rule 3** : If the **Included Tasks** field is set to **Selected project tasks only** , a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="2e4d0-180">**Kural 4** : Bir fırsatın birden fazla teklifi varsa hepsi aynı projeye atıfta bulunan ve aynı işlem sınıfını içeren farklı tekliflerden teklif satırları olabilir.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-180">**Rule 4** : If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="2e4d0-181">**Kural 5** : Teklifler aynı fırsata ait değilse aynı projeyi ve işlem sınıfını içeremezler.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-181">**Rule 5** : If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="2e4d0-182">
                    <strong>Fırsat</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2e4d0-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="2e4d0-183">
                    <strong>Teklif</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2e4d0-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="2e4d0-184">
                    <strong>Teklif satırı</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2e4d0-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="2e4d0-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2e4d0-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="2e4d0-186">
                    <strong>Dahil edilen görevler</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2e4d0-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="2e4d0-187">
                    <strong>Zaman Ekle</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2e4d0-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="2e4d0-188">
                    <strong>Gider Ekle</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2e4d0-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="2e4d0-189">
                    <strong>Ekle</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2e4d0-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="2e4d0-190">
                    <strong>Ücret</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2e4d0-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="2e4d0-191">
                    <strong>Geçerli/Geçerli değil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2e4d0-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="2e4d0-192">
                    <strong>Neden</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2e4d0-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="2e4d0-193">O1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2e4d0-194">Ç1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e4d0-195">QL1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e4d0-196">P1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="2e4d0-197">Boş</span><span class="sxs-lookup"><span data-stu-id="2e4d0-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e4d0-198">Evet</span><span class="sxs-lookup"><span data-stu-id="2e4d0-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e4d0-199">Evet</span><span class="sxs-lookup"><span data-stu-id="2e4d0-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e4d0-200">Evet</span><span class="sxs-lookup"><span data-stu-id="2e4d0-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2e4d0-201">Geçerli değil</span><span class="sxs-lookup"><span data-stu-id="2e4d0-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2e4d0-202">Kural 2'nin ihlali.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-202">Violation of Rule #2.</span></span> <span data-ttu-id="2e4d0-203">P1 projesindeki Zaman, Gider ve Ücretler, QL1 ve QL2 teklif satırlarına dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="2e4d0-204">O1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2e4d0-205">Ç1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e4d0-206">QL2</span><span class="sxs-lookup"><span data-stu-id="2e4d0-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e4d0-207">P1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="2e4d0-208">Boş</span><span class="sxs-lookup"><span data-stu-id="2e4d0-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e4d0-209">Evet</span><span class="sxs-lookup"><span data-stu-id="2e4d0-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e4d0-210">Evet</span><span class="sxs-lookup"><span data-stu-id="2e4d0-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e4d0-211">Evet</span><span class="sxs-lookup"><span data-stu-id="2e4d0-211">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="2e4d0-212">O1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2e4d0-213">Ç1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e4d0-214">QL1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e4d0-215">P1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="2e4d0-216">Boş</span><span class="sxs-lookup"><span data-stu-id="2e4d0-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e4d0-217">Evet</span><span class="sxs-lookup"><span data-stu-id="2e4d0-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e4d0-218">No</span><span class="sxs-lookup"><span data-stu-id="2e4d0-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e4d0-219">Evet</span><span class="sxs-lookup"><span data-stu-id="2e4d0-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2e4d0-220">Geçerli değil</span><span class="sxs-lookup"><span data-stu-id="2e4d0-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2e4d0-221">Kural 2'nin ihlali.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-221">Violation of Rule #2.</span></span> <span data-ttu-id="2e4d0-222">P1 projesindeki Zaman ve Ücretler, QL1 ve QL2 teklif satırlarına dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="2e4d0-223">O1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2e4d0-224">Ç1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e4d0-225">QL2</span><span class="sxs-lookup"><span data-stu-id="2e4d0-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e4d0-226">P1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="2e4d0-227">Boş</span><span class="sxs-lookup"><span data-stu-id="2e4d0-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e4d0-228">Evet</span><span class="sxs-lookup"><span data-stu-id="2e4d0-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e4d0-229">Evet</span><span class="sxs-lookup"><span data-stu-id="2e4d0-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e4d0-230">Evet</span><span class="sxs-lookup"><span data-stu-id="2e4d0-230">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="2e4d0-231">O1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2e4d0-232">Ç1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e4d0-233">QL1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e4d0-234">P1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="2e4d0-235">Boş</span><span class="sxs-lookup"><span data-stu-id="2e4d0-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e4d0-236">Evet</span><span class="sxs-lookup"><span data-stu-id="2e4d0-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e4d0-237">No</span><span class="sxs-lookup"><span data-stu-id="2e4d0-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e4d0-238">Evet</span><span class="sxs-lookup"><span data-stu-id="2e4d0-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2e4d0-239">Geçerli</span><span class="sxs-lookup"><span data-stu-id="2e4d0-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="2e4d0-240">P1 projesindeki Zaman ve Ücretler, QL1'e dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="2e4d0-241">P1 projesindeki giderler QL2'ye dahildir.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="2e4d0-242">Dahil edilen teklif satırlarının hiçbirinin birbiriyle çakışması yoktur ve hepsi geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="2e4d0-243">O1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2e4d0-244">Ç1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e4d0-245">QL2</span><span class="sxs-lookup"><span data-stu-id="2e4d0-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e4d0-246">P1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="2e4d0-247">Boş</span><span class="sxs-lookup"><span data-stu-id="2e4d0-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e4d0-248">No</span><span class="sxs-lookup"><span data-stu-id="2e4d0-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e4d0-249">Evet</span><span class="sxs-lookup"><span data-stu-id="2e4d0-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e4d0-250">No</span><span class="sxs-lookup"><span data-stu-id="2e4d0-250">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="2e4d0-251">O1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2e4d0-252">Ç1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e4d0-253">QL1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e4d0-254">P1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="2e4d0-255">Yalnızca seçili görevler</span><span class="sxs-lookup"><span data-stu-id="2e4d0-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e4d0-256">Evet</span><span class="sxs-lookup"><span data-stu-id="2e4d0-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e4d0-257">Evet</span><span class="sxs-lookup"><span data-stu-id="2e4d0-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e4d0-258">Evet</span><span class="sxs-lookup"><span data-stu-id="2e4d0-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2e4d0-259">Geçerli değil</span><span class="sxs-lookup"><span data-stu-id="2e4d0-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2e4d0-260">Kural 2'nin yukarıdaki ihlali</span><span class="sxs-lookup"><span data-stu-id="2e4d0-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="2e4d0-261">Q1, proje P1 üzerinde bir görev alt kümesinde Zaman, Giderler ve Ücretleri içerir.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="2e4d0-262">QL2, P1 projesinin tamamı için Zaman, Giderler ve Ücretleri içerir ve Q1'e dahil olanlarla örtüşür.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="2e4d0-263">O1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2e4d0-264">Ç1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e4d0-265">QL2</span><span class="sxs-lookup"><span data-stu-id="2e4d0-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e4d0-266">P1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="2e4d0-267">Boş</span><span class="sxs-lookup"><span data-stu-id="2e4d0-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e4d0-268">Evet</span><span class="sxs-lookup"><span data-stu-id="2e4d0-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e4d0-269">Evet</span><span class="sxs-lookup"><span data-stu-id="2e4d0-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e4d0-270">Evet</span><span class="sxs-lookup"><span data-stu-id="2e4d0-270">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="2e4d0-271">O1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2e4d0-272">Ç1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e4d0-273">QL1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e4d0-274">P1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="2e4d0-275">Yalnızca seçili görevler</span><span class="sxs-lookup"><span data-stu-id="2e4d0-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e4d0-276">Evet</span><span class="sxs-lookup"><span data-stu-id="2e4d0-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e4d0-277">Evet</span><span class="sxs-lookup"><span data-stu-id="2e4d0-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e4d0-278">Evet</span><span class="sxs-lookup"><span data-stu-id="2e4d0-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2e4d0-279">Geçerli</span><span class="sxs-lookup"><span data-stu-id="2e4d0-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2e4d0-280">Yukarıdaki Kural 3'e göre,</span><span class="sxs-lookup"><span data-stu-id="2e4d0-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="2e4d0-281">Q1, proje P1 üzerinde bir görev alt kümesinde Zaman, Giderler ve Ücretleri içerir.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="2e4d0-282">QL2, proje P1 üzerinde bir görev alt kümesinde Zaman, Giderler ve Ücretleri içerir.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="2e4d0-283">Tek ek doğrulama, QL2'deki görevlerin alt kümesinden farklı olan QL1'deki görevlerin alt kümesiyle ilgilidir.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="2e4d0-284">Bu sayede hiçbir çakışma olmaması sağlanır.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="2e4d0-285">Bu, görevler ilişkilendirildiğinde sistem tarafından yapılır.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="2e4d0-286">O1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2e4d0-287">Ç1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e4d0-288">QL2</span><span class="sxs-lookup"><span data-stu-id="2e4d0-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e4d0-289">P1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="2e4d0-290">Yalnızca seçili görevler</span><span class="sxs-lookup"><span data-stu-id="2e4d0-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e4d0-291">Evet</span><span class="sxs-lookup"><span data-stu-id="2e4d0-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e4d0-292">Evet</span><span class="sxs-lookup"><span data-stu-id="2e4d0-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e4d0-293">Evet</span><span class="sxs-lookup"><span data-stu-id="2e4d0-293">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="2e4d0-294">O1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2e4d0-295">Ç1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e4d0-296">QL1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e4d0-297">P1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="2e4d0-298">Tüm proje görevleri veya boş</span><span class="sxs-lookup"><span data-stu-id="2e4d0-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e4d0-299">Evet</span><span class="sxs-lookup"><span data-stu-id="2e4d0-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e4d0-300">Evet</span><span class="sxs-lookup"><span data-stu-id="2e4d0-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e4d0-301">Evet</span><span class="sxs-lookup"><span data-stu-id="2e4d0-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="2e4d0-302">Geçerli</span><span class="sxs-lookup"><span data-stu-id="2e4d0-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2e4d0-303">Kural 5'e göre, Q1 ve Q2 aynı fırsatta iki tekliftir; böylelikle projenin aynı bileşenleri için ikisi de tahmin edilebilir.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="2e4d0-304">O1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2e4d0-305">Ç2</span><span class="sxs-lookup"><span data-stu-id="2e4d0-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e4d0-306">QL1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e4d0-307">P1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="2e4d0-308">Tüm proje görevleri veya boş</span><span class="sxs-lookup"><span data-stu-id="2e4d0-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e4d0-309">Evet</span><span class="sxs-lookup"><span data-stu-id="2e4d0-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e4d0-310">Evet</span><span class="sxs-lookup"><span data-stu-id="2e4d0-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e4d0-311">Evet</span><span class="sxs-lookup"><span data-stu-id="2e4d0-311">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="2e4d0-312">O1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2e4d0-313">Ç1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e4d0-314">QL1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e4d0-315">P1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="2e4d0-316">Tüm proje görevleri veya boş</span><span class="sxs-lookup"><span data-stu-id="2e4d0-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e4d0-317">Evet</span><span class="sxs-lookup"><span data-stu-id="2e4d0-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e4d0-318">Evet</span><span class="sxs-lookup"><span data-stu-id="2e4d0-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e4d0-319">Evet</span><span class="sxs-lookup"><span data-stu-id="2e4d0-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="2e4d0-320">Geçerli</span><span class="sxs-lookup"><span data-stu-id="2e4d0-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2e4d0-321">Kural #4 göre, Q1 ve Q2 farklı fırsatlarda iki tekliftir; bu nedenle aynı projenin aynı bileşenleri için tahmin edilemezler.</span><span class="sxs-lookup"><span data-stu-id="2e4d0-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="2e4d0-322">O2</span><span class="sxs-lookup"><span data-stu-id="2e4d0-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2e4d0-323">Ç1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e4d0-324">QL1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e4d0-325">P1</span><span class="sxs-lookup"><span data-stu-id="2e4d0-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="2e4d0-326">Tüm proje görevleri veya boş</span><span class="sxs-lookup"><span data-stu-id="2e4d0-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e4d0-327">Evet</span><span class="sxs-lookup"><span data-stu-id="2e4d0-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="2e4d0-328">Evet</span><span class="sxs-lookup"><span data-stu-id="2e4d0-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="2e4d0-329">Evet</span><span class="sxs-lookup"><span data-stu-id="2e4d0-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="2e4d0-330">Geçerli Değil</span><span class="sxs-lookup"><span data-stu-id="2e4d0-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>
