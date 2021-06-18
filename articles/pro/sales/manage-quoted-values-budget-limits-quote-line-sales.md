---
title: Proje tabanlı teklif satırlarına genel bakış
description: Bu konuda, proje çalışmaları için proje tabanlı teklif satırlarını kullanma hakkında bilgiler sağlanmaktadır.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 32337b05f09ef7c5b84fdff9870744d6367e2693
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994880"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="416fa-103">Proje tabanlı teklif satırlarına genel bakış</span><span class="sxs-lookup"><span data-stu-id="416fa-103">Project-based quote lines overview</span></span> 

<span data-ttu-id="416fa-104">_**Aşağıdakilere İçin Geçerlidir:** Lite dağıtımı - anlaşmadan proforma faturaya, kaynak/stoklanmayan tabanlı senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="416fa-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="416fa-105">Proje tabanlı teklif satırları, bir etkileşimdeki proje çalışmalarının tahmin edilmesine yardımcı olmak için tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="416fa-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="416fa-106">Proje tabanlı teklif satırının yapısı, aşağıdaki kavramlarla proje tahminleri için genişletilmiştir:</span><span class="sxs-lookup"><span data-stu-id="416fa-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="416fa-107">Faturalama Yöntemi</span><span class="sxs-lookup"><span data-stu-id="416fa-107">Billing Method</span></span>
- <span data-ttu-id="416fa-108">Proje ve Görev Eşleme</span><span class="sxs-lookup"><span data-stu-id="416fa-108">Project and Task Mapping</span></span>
- <span data-ttu-id="416fa-109">Dahil Edilen İşlem sınıfları</span><span class="sxs-lookup"><span data-stu-id="416fa-109">Included Transaction classes</span></span>
- <span data-ttu-id="416fa-110">Aşılamaz Limit</span><span class="sxs-lookup"><span data-stu-id="416fa-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="416fa-111">Borçlandırılabilirlik ayarı</span><span class="sxs-lookup"><span data-stu-id="416fa-111">Chargeability setup</span></span>
- <span data-ttu-id="416fa-112">Teklif Satırı Ayrıntılarını kullanarak tahmin yürütme</span><span class="sxs-lookup"><span data-stu-id="416fa-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="416fa-113">Teklif satırı Müşterileri</span><span class="sxs-lookup"><span data-stu-id="416fa-113">Quote line Customers</span></span>

<span data-ttu-id="416fa-114">Aşağıdaki tabloda proje tabanlı teklif satırının **Genel** sekmesindeki alanlar hakkında bilgi sağlanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="416fa-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="416fa-115">Bu alanlar, proje çalışmaları için ayrıntılı, baştan sona bir tahmin için temel oluşturulmasına yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="416fa-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="416fa-116">**Alan**</span><span class="sxs-lookup"><span data-stu-id="416fa-116">**Field**</span></span> | <span data-ttu-id="416fa-117">**Açıklama**</span><span class="sxs-lookup"><span data-stu-id="416fa-117">**Description**</span></span> | <span data-ttu-id="416fa-118">**Aşağı yönlü etki**</span><span class="sxs-lookup"><span data-stu-id="416fa-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="416fa-119">Adı</span><span class="sxs-lookup"><span data-stu-id="416fa-119">Name</span></span> | <span data-ttu-id="416fa-120">Tahmin edilen teklifin farklı bileşenini belirlemenize yardımcı olan teklif satırı adı.</span><span class="sxs-lookup"><span data-stu-id="416fa-120">The name of quote line that helps you to identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="416fa-121">Teklif kazanıldığında, bu teklif satırından oluşturulan proje sözleşme satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="416fa-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="416fa-122">Faturalama Yöntemi</span><span class="sxs-lookup"><span data-stu-id="416fa-122">Billing Method</span></span> | <span data-ttu-id="416fa-123">Fırsattan oluşturulan bir teklifte bu değer, fırsat satırındaki ilgili alandan kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="416fa-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="416fa-124">Bu alan, Dynamics 365 Project Operations tarafından desteklenen iki ana sözleşme modeli içerir:</span><span class="sxs-lookup"><span data-stu-id="416fa-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="416fa-125">- Sabit fiyat</span><span class="sxs-lookup"><span data-stu-id="416fa-125">- Fixed price</span></span></br><span data-ttu-id="416fa-126">- Zaman ve malzeme.</span><span class="sxs-lookup"><span data-stu-id="416fa-126">- Time and material.</span></span>| <span data-ttu-id="416fa-127">Bu değer, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşmesi satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="416fa-127">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="416fa-128">Project</span><span class="sxs-lookup"><span data-stu-id="416fa-128">Project</span></span> | <span data-ttu-id="416fa-129">Bu etkileşimde kullanılacak projeyi belirleyerek çalışmayı teslim etmek için bu isteğe bağlı alanı kullanın.</span><span class="sxs-lookup"><span data-stu-id="416fa-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="416fa-130">Proje bir teklif satırına eşlendiğinde, borçlandırılabilir görevler oluşturulmasına ve ayrıca proje bazlı bir tahminin teklif satırına teklif satırı ayrıntıları olarak getirilmesine yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="416fa-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="416fa-131">Proje, proje bazlı bir teklif satırına eşlenmediğinde tahmin, her bir teklif satırı ayrıntısının el ile oluşturulmasıyla elde edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="416fa-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="416fa-132">Bu değer, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşmesi satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="416fa-132">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="416fa-133">Dahil Edilen Görevler</span><span class="sxs-lookup"><span data-stu-id="416fa-133">Included Tasks</span></span> | <span data-ttu-id="416fa-134">Bu teklif satırının seçilen projenin görevlerinin tümünde veya bazılarında kullanılıp kullanılmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="416fa-134">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="416fa-135">Bu alan aşağıdaki olası değerlere sahiptir:</span><span class="sxs-lookup"><span data-stu-id="416fa-135">This field has the following possible values:</span></span></br><span data-ttu-id="416fa-136">- Tüm proje görevleri</span><span class="sxs-lookup"><span data-stu-id="416fa-136">- All project tasks</span></span></br><span data-ttu-id="416fa-137">- Yalnızca seçili proje görevleri</span><span class="sxs-lookup"><span data-stu-id="416fa-137">- Selected project tasks only</span></span></br><span data-ttu-id="416fa-138">Bu alandaki boş bir değer **Tüm proje görevleri** seçeneğinin eşdeğeridir.</span><span class="sxs-lookup"><span data-stu-id="416fa-138">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="416fa-139">Proje sayfasında **Yalnızca seçili proje görevleri** seçeneği belirlendiğinde **Görev fatura ayarı** sekmesi, bu teklif satırıyla ilişkilendirmek üzere belirli görevleri seçmenize olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="416fa-139">When **Selected project tasks only** is selected on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="416fa-140">Bu değer, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşmesi satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="416fa-140">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="416fa-141">Zaman Ekle</span><span class="sxs-lookup"><span data-stu-id="416fa-141">Include Time</span></span> | <span data-ttu-id="416fa-142">**Evet**/**Hayır** değeri, seçili projedeki zaman hareketlerinin veya işçilik maliyetlerinin bu teklif satırı tahminine dahil edilip edilmeyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="416fa-142">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="416fa-143">**Hayır** değeri, zaman işlemlerinin veya işçilik maliyetinin bu teklif satırındaki tahmine dahil edilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="416fa-143">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="416fa-144">**Evet** değeri, zaman işlemlerinin veya işçilik maliyetinin bu teklif satırındaki tahmine dahil edileceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="416fa-144">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="416fa-145">Bu değer, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşmesi satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="416fa-145">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="416fa-146">Gider Ekle</span><span class="sxs-lookup"><span data-stu-id="416fa-146">Include Expense</span></span> | <span data-ttu-id="416fa-147">**Evet**/**Hayır** değeri, seçili projedeki gider maliyetlerinin bu teklif satırı tahminine dahil edilip edilmeyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="416fa-147">A **Yes**/**No** value indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="416fa-148">**Hayır** değeri, gider maliyetinin bu teklif satırındaki tahmine dahil edilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="416fa-148">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="416fa-149">**Evet** değeri, gider maliyetinin bu teklif satırındaki tahmine dahil edileceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="416fa-149">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="416fa-150">Bu değer, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşmesi satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="416fa-150">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="416fa-151">Malzeme Ekle</span><span class="sxs-lookup"><span data-stu-id="416fa-151">Include Material</span></span> | <span data-ttu-id="416fa-152">**Evet**/**Hayır** değeri, seçili projedeki malzeme maliyetlerinin bu teklif satırı tahminine dahil edilip edilmeyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="416fa-152">A **Yes**/**No** value indicates if material costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="416fa-153">**Hayır** değeri, malzeme maliyetlerinin bu teklif satırı tahminine dahil edilmeyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="416fa-153">A **No** value indicates that the material costs will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="416fa-154">**Evet** değeri, malzeme maliyetlerinin bu teklif satırı tahminine dahil edileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="416fa-154">A **Yes** value indicates that the material costs will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="416fa-155">Bu değer, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşmesi satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="416fa-155">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="416fa-156">Ücret Ekle</span><span class="sxs-lookup"><span data-stu-id="416fa-156">Include Fee</span></span> | <span data-ttu-id="416fa-157">**Evet**/**Hayır** değeri, seçili projedeki ücretlerin bu teklif satırı tahminine dahil edilip edilmeyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="416fa-157">A **Yes**/**No** value indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="416fa-158">**Hayır** değeri, ücretlerin bu teklif satırındaki tahmine dahil edilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="416fa-158">A **No** value indicates that the fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="416fa-159">**Evet** değeri, ücretlerin bu teklif satırındaki tahmine dahil edileceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="416fa-159">A **Yes** value indicates that the fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="416fa-160">Bu değer, teklif kazanıldığında bu teklif satırından oluşturulan Proje sözleşmesi satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="416fa-160">This value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="416fa-161">Teklif Edilen Tutar</span><span class="sxs-lookup"><span data-stu-id="416fa-161">Quoted Amount</span></span> | <span data-ttu-id="416fa-162">Bu, proje tabanlı teklif satırındaki tüm tahmin edilen çalışma için müşteriye teklif edilecek tutardır.</span><span class="sxs-lookup"><span data-stu-id="416fa-162">This is the amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="416fa-163">Fırsattan oluşturulan bir teklifte, bu değer fırsat satırındaki **Müşteri Bütçesi** alanından kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="416fa-163">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="416fa-164">Proje tabanlı teklif satırı satır ayrıntılarına sahip olduğunda, bu alan düzenlemeye kilitlenir ve teklif satırı ayrıntılarındaki tutardan özetlenir.</span><span class="sxs-lookup"><span data-stu-id="416fa-164">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="416fa-165">Bu değer, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşmesi satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="416fa-165">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="416fa-166">Tahmini Vergi</span><span class="sxs-lookup"><span data-stu-id="416fa-166">Estimated Tax</span></span> | <span data-ttu-id="416fa-167">Bu, kullanıcının teklif satırına tahmini vergi tutarını ekleyebileceği düzenlenebilir bir alandır.</span><span class="sxs-lookup"><span data-stu-id="416fa-167">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="416fa-168">Proje tabanlı teklif satırı, satır ayrıntılarına sahip olduğunda, bu alan düzenlemeye kilitlenir ve teklif satırı ayrıntılarındaki vergi tutarından özetlenir.</span><span class="sxs-lookup"><span data-stu-id="416fa-168">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="416fa-169">Bu değer, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşmesi satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="416fa-169">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="416fa-170">Vergi Sonrası Teklif Tutarı</span><span class="sxs-lookup"><span data-stu-id="416fa-170">Quoted Amount after Tax</span></span> | <span data-ttu-id="416fa-171">Bu alan, vergi sonrası teklif satırı tutarıdır ve salt okunurdur.</span><span class="sxs-lookup"><span data-stu-id="416fa-171">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="416fa-172">Bu alandaki tutar *Teklif Tutarı + Vergi* olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="416fa-172">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="416fa-173">Bu değer, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşmesi satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="416fa-173">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="416fa-174">Aşılamaz Limit</span><span class="sxs-lookup"><span data-stu-id="416fa-174">Not-to-exceed Limit</span></span> | <span data-ttu-id="416fa-175">Bu alan, düzenlenebilirdir ve yalnızca **Zaman ve Malzeme** faturalama yöntemine sahip proje bazlı teklif satırlarında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="416fa-175">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="416fa-176">Bu değer, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşmesi satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="416fa-176">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="416fa-177">Müşteri Bütçesi</span><span class="sxs-lookup"><span data-stu-id="416fa-177">Customer Budget</span></span> | <span data-ttu-id="416fa-178">Bu alan, düzenlenebilirdir ve teklif bir fırsattan oluşturulmuşsa fırsat satırındaki ilgili alandan kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="416fa-178">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="416fa-179">Bu değer, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşmesi satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="416fa-179">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="416fa-180">Proje tabanlı teklif satırlarının Genel sekmesindeki alanları için doğrulama kuralları</span><span class="sxs-lookup"><span data-stu-id="416fa-180">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="416fa-181">**Kural 1**: **Eklenen Görevler** alanı boşsa veya bu alan **Tüm proje görevleri** olarak ayarlanmışsa teklif satırına bir proje dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="416fa-181">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="416fa-182">**Kural 2**: **Eklenen Görevler** alanı boşsa veya bu alan **Tüm proje görevleri** olarak ayarlanmışsa bir proje ve belirli bir işlem sınıfı, bir teklifin yalnızca proje tabanlı bir teklif satırına dahil edilebilir.</span><span class="sxs-lookup"><span data-stu-id="416fa-182">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="416fa-183">**Kural 3**: **Eklenen Görevler** alanı **Yalnızca seçili proje görevleri** olarak ayarlanmışsa bir proje ve belirli bir işlem sınıfı, bir teklifin birden çok proje tabanlı teklif satırına dahil edilebilir.</span><span class="sxs-lookup"><span data-stu-id="416fa-183">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="416fa-184">**Kural 4**: Bir fırsatın birden fazla teklifi varsa hepsi aynı projeye atıfta bulunan ve aynı işlem sınıfını içeren farklı tekliflerden teklif satırları olabilir.</span><span class="sxs-lookup"><span data-stu-id="416fa-184">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="416fa-185">**Kural 5**: Teklifler aynı fırsata ait değilse aynı projeyi ve işlem sınıfını içeremezler.</span><span class="sxs-lookup"><span data-stu-id="416fa-185">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p><span data-ttu-id="416fa-186">
                    <strong>Fırsat</strong>
                </span><span class="sxs-lookup"><span data-stu-id="416fa-186">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="39" valign="top">
                <p><span data-ttu-id="416fa-187">
                    <strong>Teklif</strong>
                </span><span class="sxs-lookup"><span data-stu-id="416fa-187">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="40" valign="top">
                <p><span data-ttu-id="416fa-188">
                    <strong>Teklif satırı</strong>
                </span><span class="sxs-lookup"><span data-stu-id="416fa-188">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="416fa-189">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="416fa-189">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="77" valign="top">
                <p><span data-ttu-id="416fa-190">
                    <strong>Dahil edilen görevler</strong>
                </span><span class="sxs-lookup"><span data-stu-id="416fa-190">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="45" valign="top">
                <p><span data-ttu-id="416fa-191">
                    <strong>Zaman Ekle</strong>
                </span><span class="sxs-lookup"><span data-stu-id="416fa-191">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="46" valign="top">
                <p><span data-ttu-id="416fa-192">
                    <strong>Gider Ekle</strong>
                </span><span class="sxs-lookup"><span data-stu-id="416fa-192">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="43" valign="top">
                <p><span data-ttu-id="416fa-193">
                    <strong>Malzeme Ekle</strong>
                </span><span class="sxs-lookup"><span data-stu-id="416fa-193">
                    <strong>Include Material</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="416fa-194">
                    <strong>Ekle</strong>
                </span><span class="sxs-lookup"><span data-stu-id="416fa-194">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="416fa-195">
                    <strong>Ücret</strong>
                </span><span class="sxs-lookup"><span data-stu-id="416fa-195">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="49" valign="top">
                <p><span data-ttu-id="416fa-196">
                    <strong>Geçerli/Geçerli değil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="416fa-196">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="200" valign="top">
                <p><span data-ttu-id="416fa-197">
                    <strong>Neden</strong>
                </span><span class="sxs-lookup"><span data-stu-id="416fa-197">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="416fa-198">O1</span><span class="sxs-lookup"><span data-stu-id="416fa-198">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="416fa-199">Ç1</span><span class="sxs-lookup"><span data-stu-id="416fa-199">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="416fa-200">QL1</span><span class="sxs-lookup"><span data-stu-id="416fa-200">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="416fa-201">P1</span><span class="sxs-lookup"><span data-stu-id="416fa-201">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="416fa-202">Boş</span><span class="sxs-lookup"><span data-stu-id="416fa-202">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="416fa-203">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-203">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="416fa-204">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-204">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="416fa-205">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-205">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="416fa-206">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-206">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="416fa-207">Geçerli değil</span><span class="sxs-lookup"><span data-stu-id="416fa-207">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="416fa-208">Kural 2'nin ihlali.</span><span class="sxs-lookup"><span data-stu-id="416fa-208">Violation of Rule #2.</span></span> <span data-ttu-id="416fa-209">P1 projesindeki Zaman, Gider ve Ücretler, QL1 ve QL2 teklif satırlarına dahil edilir</span><span class="sxs-lookup"><span data-stu-id="416fa-209">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="416fa-210">O1</span><span class="sxs-lookup"><span data-stu-id="416fa-210">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="416fa-211">Ç1</span><span class="sxs-lookup"><span data-stu-id="416fa-211">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="416fa-212">QL2</span><span class="sxs-lookup"><span data-stu-id="416fa-212">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="416fa-213">P1</span><span class="sxs-lookup"><span data-stu-id="416fa-213">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="416fa-214">Boş</span><span class="sxs-lookup"><span data-stu-id="416fa-214">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="416fa-215">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-215">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="416fa-216">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-216">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="416fa-217">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-217">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="416fa-218">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-218">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="416fa-219">O1</span><span class="sxs-lookup"><span data-stu-id="416fa-219">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="416fa-220">Ç1</span><span class="sxs-lookup"><span data-stu-id="416fa-220">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="416fa-221">QL1</span><span class="sxs-lookup"><span data-stu-id="416fa-221">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="416fa-222">P1</span><span class="sxs-lookup"><span data-stu-id="416fa-222">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="416fa-223">Boş</span><span class="sxs-lookup"><span data-stu-id="416fa-223">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="416fa-224">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-224">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="416fa-225">No</span><span class="sxs-lookup"><span data-stu-id="416fa-225">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="416fa-226">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-226">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="416fa-227">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-227">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="416fa-228">Geçerli değil</span><span class="sxs-lookup"><span data-stu-id="416fa-228">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="416fa-229">Kural 2'nin ihlali.</span><span class="sxs-lookup"><span data-stu-id="416fa-229">Violation of Rule #2.</span></span> <span data-ttu-id="416fa-230">P1 projesindeki Zaman, Malzeme ve Ücretler, QL1 ve QL2 teklif satırlarına dahil edilir</span><span class="sxs-lookup"><span data-stu-id="416fa-230">Time, Material, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="416fa-231">O1</span><span class="sxs-lookup"><span data-stu-id="416fa-231">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="416fa-232">Ç1</span><span class="sxs-lookup"><span data-stu-id="416fa-232">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="416fa-233">QL2</span><span class="sxs-lookup"><span data-stu-id="416fa-233">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="416fa-234">P1</span><span class="sxs-lookup"><span data-stu-id="416fa-234">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="416fa-235">Boş</span><span class="sxs-lookup"><span data-stu-id="416fa-235">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="416fa-236">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-236">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="416fa-237">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-237">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="416fa-238">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-238">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="416fa-239">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-239">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="416fa-240">O1</span><span class="sxs-lookup"><span data-stu-id="416fa-240">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="416fa-241">Ç1</span><span class="sxs-lookup"><span data-stu-id="416fa-241">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="416fa-242">QL1</span><span class="sxs-lookup"><span data-stu-id="416fa-242">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="416fa-243">P1</span><span class="sxs-lookup"><span data-stu-id="416fa-243">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="416fa-244">Boş</span><span class="sxs-lookup"><span data-stu-id="416fa-244">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="416fa-245">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-245">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="416fa-246">No</span><span class="sxs-lookup"><span data-stu-id="416fa-246">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="416fa-247">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-247">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="416fa-248">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-248">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="416fa-249">Geçerli</span><span class="sxs-lookup"><span data-stu-id="416fa-249">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="416fa-250">P1 projesindeki Zaman, Malzeme ve Ücretler QL1'e dahil edilir</span><span class="sxs-lookup"><span data-stu-id="416fa-250">Time, Material, and Fees on P1 project are included on QL1</span></span> <br>
<span data-ttu-id="416fa-251">P1 projesindeki giderler QL2'ye dahildir</span><span class="sxs-lookup"><span data-stu-id="416fa-251">Expense on P1 project is included on QL2</span></span> <br>
<span data-ttu-id="416fa-252">Her bir teklif satırına dahil edilenler arasında çakışma yok ve bu nedenle geçerli.</span><span class="sxs-lookup"><span data-stu-id="416fa-252">No overlap in what is being included on each quote line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="416fa-253">O1</span><span class="sxs-lookup"><span data-stu-id="416fa-253">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="416fa-254">Ç1</span><span class="sxs-lookup"><span data-stu-id="416fa-254">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="416fa-255">QL2</span><span class="sxs-lookup"><span data-stu-id="416fa-255">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="416fa-256">P1</span><span class="sxs-lookup"><span data-stu-id="416fa-256">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="416fa-257">Boş</span><span class="sxs-lookup"><span data-stu-id="416fa-257">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="416fa-258">No</span><span class="sxs-lookup"><span data-stu-id="416fa-258">No</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="416fa-259">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-259">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="416fa-260">No</span><span class="sxs-lookup"><span data-stu-id="416fa-260">No</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="416fa-261">No</span><span class="sxs-lookup"><span data-stu-id="416fa-261">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="416fa-262">O1</span><span class="sxs-lookup"><span data-stu-id="416fa-262">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="416fa-263">Ç1</span><span class="sxs-lookup"><span data-stu-id="416fa-263">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="416fa-264">QL1</span><span class="sxs-lookup"><span data-stu-id="416fa-264">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="416fa-265">P1</span><span class="sxs-lookup"><span data-stu-id="416fa-265">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="416fa-266">Yalnızca seçili görevler</span><span class="sxs-lookup"><span data-stu-id="416fa-266">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="416fa-267">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-267">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="416fa-268">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-268">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="416fa-269">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-269">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="416fa-270">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-270">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="416fa-271">Geçerli değil</span><span class="sxs-lookup"><span data-stu-id="416fa-271">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="416fa-272">Kural 2'nin ihlali</span><span class="sxs-lookup"><span data-stu-id="416fa-272">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="416fa-273">Q1'e, proje P1 üzerindeki bir görev alt kümesinde Zaman, Malzeme, Giderler ve Ücretler dahildir</span><span class="sxs-lookup"><span data-stu-id="416fa-273">Q1 includes Time, Material, Expenses and Fees on a subset of tasks on project P1</span></span> </p>
                <p>
<span data-ttu-id="416fa-274">QL2 tüm proje P1 için Zaman, Giderler ve Ücretleri içerir, bu nedenle Q1'in içerdiği verilerle örtüşür.</span><span class="sxs-lookup"><span data-stu-id="416fa-274">QL2 includes Time, Expenses, and Fees for the whole project P1 and therefore overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="416fa-275">O1</span><span class="sxs-lookup"><span data-stu-id="416fa-275">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="416fa-276">Ç1</span><span class="sxs-lookup"><span data-stu-id="416fa-276">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="416fa-277">QL2</span><span class="sxs-lookup"><span data-stu-id="416fa-277">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="416fa-278">P1</span><span class="sxs-lookup"><span data-stu-id="416fa-278">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="416fa-279">Boş</span><span class="sxs-lookup"><span data-stu-id="416fa-279">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="416fa-280">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-280">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="416fa-281">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-281">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="416fa-282">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-282">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="416fa-283">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-283">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="416fa-284">O1</span><span class="sxs-lookup"><span data-stu-id="416fa-284">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="416fa-285">Ç1</span><span class="sxs-lookup"><span data-stu-id="416fa-285">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="416fa-286">QL1</span><span class="sxs-lookup"><span data-stu-id="416fa-286">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="416fa-287">P1</span><span class="sxs-lookup"><span data-stu-id="416fa-287">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="416fa-288">Yalnızca seçili görevler</span><span class="sxs-lookup"><span data-stu-id="416fa-288">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="416fa-289">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-289">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="416fa-290">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-290">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="416fa-291">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-291">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="416fa-292">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-292">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="416fa-293">Geçerli</span><span class="sxs-lookup"><span data-stu-id="416fa-293">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="416fa-294">Kural 3 uyarınca,</span><span class="sxs-lookup"><span data-stu-id="416fa-294">Per Rule #3,</span></span> </p>
                <p>
<span data-ttu-id="416fa-295">Q1'e, proje P1 üzerindeki bir görev alt kümesinde Zaman, Malzeme, Giderler ve Ücretler dahildir.</span><span class="sxs-lookup"><span data-stu-id="416fa-295">Q1 includes Time, Material, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="416fa-296">QL2'e, proje P1 üzerindeki bir görev alt kümesi için Zaman, Malzeme ve Giderler dahildir.</span><span class="sxs-lookup"><span data-stu-id="416fa-296">QL2 includes Time, Material, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="416fa-297">Yalnızca tek bir ek doğrulama yapılır. Bu doğrulamanın amacı, çakışmaları önlemek için QL1 üzerindeki alt görevlerin QL2 üzerindeki alt görevlerden farklı olmasını kontrol etmektir.</span><span class="sxs-lookup"><span data-stu-id="416fa-297">The only additional validation is around the subset of tasks on QL1 which is different from the subset of tasks on QL2 to ensure that there is no overlap.</span></span> <span data-ttu-id="416fa-298">Bu, görevler ilişkilendirildiğinde sistem tarafından yapılır.</span><span class="sxs-lookup"><span data-stu-id="416fa-298">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="416fa-299">O1</span><span class="sxs-lookup"><span data-stu-id="416fa-299">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="416fa-300">Ç1</span><span class="sxs-lookup"><span data-stu-id="416fa-300">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="416fa-301">QL2</span><span class="sxs-lookup"><span data-stu-id="416fa-301">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="416fa-302">P1</span><span class="sxs-lookup"><span data-stu-id="416fa-302">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="416fa-303">Yalnızca seçili görevler</span><span class="sxs-lookup"><span data-stu-id="416fa-303">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="416fa-304">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-304">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="416fa-305">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-305">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="416fa-306">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-306">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="416fa-307">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-307">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="416fa-308">O1</span><span class="sxs-lookup"><span data-stu-id="416fa-308">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="416fa-309">Ç1</span><span class="sxs-lookup"><span data-stu-id="416fa-309">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="416fa-310">QL1</span><span class="sxs-lookup"><span data-stu-id="416fa-310">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="416fa-311">P1</span><span class="sxs-lookup"><span data-stu-id="416fa-311">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="416fa-312">Tüm proje görevleri veya boş</span><span class="sxs-lookup"><span data-stu-id="416fa-312">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="416fa-313">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-313">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="416fa-314">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-314">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="416fa-315">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-315">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="416fa-316">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-316">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="416fa-317">Geçerli</span><span class="sxs-lookup"><span data-stu-id="416fa-317">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="416fa-318">Kural 5 uyarınca, Q1 ve Q2 aynı fırsata yönelik iki tekliftir, bu nedenle ikisi de aynı proje bileşenleri için tahminde bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="416fa-318">Per Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="416fa-319">O1</span><span class="sxs-lookup"><span data-stu-id="416fa-319">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="416fa-320">Ç2</span><span class="sxs-lookup"><span data-stu-id="416fa-320">Q2</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="416fa-321">QL1</span><span class="sxs-lookup"><span data-stu-id="416fa-321">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="416fa-322">P1</span><span class="sxs-lookup"><span data-stu-id="416fa-322">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="416fa-323">Tüm proje görevleri veya boş</span><span class="sxs-lookup"><span data-stu-id="416fa-323">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="416fa-324">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-324">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="416fa-325">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-325">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="416fa-326">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-326">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="416fa-327">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-327">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="416fa-328">O1</span><span class="sxs-lookup"><span data-stu-id="416fa-328">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="416fa-329">Ç1</span><span class="sxs-lookup"><span data-stu-id="416fa-329">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="416fa-330">QL1</span><span class="sxs-lookup"><span data-stu-id="416fa-330">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="416fa-331">P1</span><span class="sxs-lookup"><span data-stu-id="416fa-331">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="416fa-332">Tüm proje görevleri veya boş</span><span class="sxs-lookup"><span data-stu-id="416fa-332">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="416fa-333">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-333">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="416fa-334">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-334">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="416fa-335">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-335">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="416fa-336">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-336">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="416fa-337">Geçerli Değil</span><span class="sxs-lookup"><span data-stu-id="416fa-337">Not Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="416fa-338">Kural 4 uyarınca, Q1 ve Q2 farklı fırsatlara yönelik iki tekliftir, bu nedenle ikisi de aynı projenin aynı bileşenleri için tahminde bulunamaz.</span><span class="sxs-lookup"><span data-stu-id="416fa-338">Per Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="416fa-339">O2</span><span class="sxs-lookup"><span data-stu-id="416fa-339">O2</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="416fa-340">Ç1</span><span class="sxs-lookup"><span data-stu-id="416fa-340">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="416fa-341">QL1</span><span class="sxs-lookup"><span data-stu-id="416fa-341">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="416fa-342">P1</span><span class="sxs-lookup"><span data-stu-id="416fa-342">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="416fa-343">Tüm proje görevleri veya boş</span><span class="sxs-lookup"><span data-stu-id="416fa-343">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="416fa-344">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-344">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="416fa-345">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-345">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="416fa-346">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-346">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="416fa-347">Evet</span><span class="sxs-lookup"><span data-stu-id="416fa-347">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
