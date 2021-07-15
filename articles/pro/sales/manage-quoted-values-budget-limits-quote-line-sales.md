---
title: Proje tabanlı teklif satırlarına genel bakış
description: Bu konuda, proje çalışmaları için proje tabanlı teklif satırlarını kullanma hakkında bilgiler sağlanmaktadır.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: b7076a4b9280472f8c30d0b58c3aa9b9bc86d651
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369895"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="2de7a-103">Proje tabanlı teklif satırlarına genel bakış</span><span class="sxs-lookup"><span data-stu-id="2de7a-103">Project-based quote lines overview</span></span> 

<span data-ttu-id="2de7a-104">_**Aşağıdakilere İçin Geçerlidir:** Lite dağıtımı - anlaşmadan proforma faturaya, kaynak/stoklanmayan tabanlı senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="2de7a-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="2de7a-105">Proje tabanlı teklif satırları, bir etkileşimdeki proje çalışmalarının tahmin edilmesine yardımcı olmak için tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="2de7a-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="2de7a-106">Proje tabanlı teklif satırının yapısı, aşağıdaki kavramlarla proje tahminleri için genişletilmiştir:</span><span class="sxs-lookup"><span data-stu-id="2de7a-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="2de7a-107">Faturalama Yöntemi</span><span class="sxs-lookup"><span data-stu-id="2de7a-107">Billing Method</span></span>
- <span data-ttu-id="2de7a-108">Proje ve Görev Eşleme</span><span class="sxs-lookup"><span data-stu-id="2de7a-108">Project and Task Mapping</span></span>
- <span data-ttu-id="2de7a-109">Dahil Edilen İşlem sınıfları</span><span class="sxs-lookup"><span data-stu-id="2de7a-109">Included Transaction classes</span></span>
- <span data-ttu-id="2de7a-110">Aşılamaz Limit</span><span class="sxs-lookup"><span data-stu-id="2de7a-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="2de7a-111">Borçlandırılabilirlik ayarı</span><span class="sxs-lookup"><span data-stu-id="2de7a-111">Chargeability setup</span></span>
- <span data-ttu-id="2de7a-112">Teklif Satırı Ayrıntılarını kullanarak tahmin yürütme</span><span class="sxs-lookup"><span data-stu-id="2de7a-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="2de7a-113">Teklif satırı Müşterileri</span><span class="sxs-lookup"><span data-stu-id="2de7a-113">Quote line Customers</span></span>

<span data-ttu-id="2de7a-114">Aşağıdaki tabloda proje tabanlı teklif satırının **Genel** sekmesindeki alanlar hakkında bilgi sağlanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="2de7a-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="2de7a-115">Bu alanlar, proje çalışmaları için ayrıntılı, baştan sona bir tahmin için temel oluşturulmasına yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="2de7a-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="2de7a-116">**Alan**</span><span class="sxs-lookup"><span data-stu-id="2de7a-116">**Field**</span></span> | <span data-ttu-id="2de7a-117">**Açıklama**</span><span class="sxs-lookup"><span data-stu-id="2de7a-117">**Description**</span></span> | <span data-ttu-id="2de7a-118">**Aşağı yönlü etki**</span><span class="sxs-lookup"><span data-stu-id="2de7a-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="2de7a-119">Adı</span><span class="sxs-lookup"><span data-stu-id="2de7a-119">Name</span></span> | <span data-ttu-id="2de7a-120">Tahmin edilen teklifin farklı bileşenini belirlemenize yardımcı olan teklif satırı adı.</span><span class="sxs-lookup"><span data-stu-id="2de7a-120">The name of quote line that helps you to identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="2de7a-121">Teklif kazanıldığında, bu teklif satırından oluşturulan proje sözleşme satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="2de7a-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2de7a-122">Faturalama Yöntemi</span><span class="sxs-lookup"><span data-stu-id="2de7a-122">Billing Method</span></span> | <span data-ttu-id="2de7a-123">Fırsattan oluşturulan bir teklifte bu değer, fırsat satırındaki ilgili alandan kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="2de7a-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="2de7a-124">Bu alan, Dynamics 365 Project Operations tarafından desteklenen iki ana sözleşme modeli içerir:</span><span class="sxs-lookup"><span data-stu-id="2de7a-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="2de7a-125">- Sabit fiyat</span><span class="sxs-lookup"><span data-stu-id="2de7a-125">- Fixed price</span></span></br><span data-ttu-id="2de7a-126">- Zaman ve malzeme.</span><span class="sxs-lookup"><span data-stu-id="2de7a-126">- Time and material.</span></span>| <span data-ttu-id="2de7a-127">Bu değer, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşmesi satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="2de7a-127">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2de7a-128">Project</span><span class="sxs-lookup"><span data-stu-id="2de7a-128">Project</span></span> | <span data-ttu-id="2de7a-129">Bu etkileşimde kullanılacak projeyi belirleyerek çalışmayı teslim etmek için bu isteğe bağlı alanı kullanın.</span><span class="sxs-lookup"><span data-stu-id="2de7a-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="2de7a-130">Proje bir teklif satırına eşlendiğinde, borçlandırılabilir görevler oluşturulmasına ve ayrıca proje bazlı bir tahminin teklif satırına teklif satırı ayrıntıları olarak getirilmesine yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="2de7a-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="2de7a-131">Proje, proje bazlı bir teklif satırına eşlenmediğinde tahmin, her bir teklif satırı ayrıntısının el ile oluşturulmasıyla elde edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="2de7a-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="2de7a-132">Bu değer, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşmesi satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="2de7a-132">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="2de7a-133">Dahil Edilen Görevler</span><span class="sxs-lookup"><span data-stu-id="2de7a-133">Included Tasks</span></span> | <span data-ttu-id="2de7a-134">Bu teklif satırının seçilen projenin görevlerinin tümünde veya bazılarında kullanılıp kullanılmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2de7a-134">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="2de7a-135">Bu alan aşağıdaki olası değerlere sahiptir:</span><span class="sxs-lookup"><span data-stu-id="2de7a-135">This field has the following possible values:</span></span></br><span data-ttu-id="2de7a-136">- Tüm proje görevleri</span><span class="sxs-lookup"><span data-stu-id="2de7a-136">- All project tasks</span></span></br><span data-ttu-id="2de7a-137">- Yalnızca seçili proje görevleri</span><span class="sxs-lookup"><span data-stu-id="2de7a-137">- Selected project tasks only</span></span></br><span data-ttu-id="2de7a-138">Bu alandaki boş bir değer **Tüm proje görevleri** seçeneğinin eşdeğeridir.</span><span class="sxs-lookup"><span data-stu-id="2de7a-138">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="2de7a-139">Proje sayfasında **Yalnızca seçili proje görevleri** seçeneği belirlendiğinde **Görev fatura ayarı** sekmesi, bu teklif satırıyla ilişkilendirmek üzere belirli görevleri seçmenize olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="2de7a-139">When **Selected project tasks only** is selected on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="2de7a-140">Bu değer, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşmesi satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="2de7a-140">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2de7a-141">Zaman Ekle</span><span class="sxs-lookup"><span data-stu-id="2de7a-141">Include Time</span></span> | <span data-ttu-id="2de7a-142">**Evet**/**Hayır** değeri, seçili projedeki zaman hareketlerinin veya işçilik maliyetlerinin bu teklif satırı tahminine dahil edilip edilmeyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="2de7a-142">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="2de7a-143">**Hayır** değeri, zaman işlemlerinin veya işçilik maliyetinin bu teklif satırındaki tahmine dahil edilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2de7a-143">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="2de7a-144">**Evet** değeri, zaman işlemlerinin veya işçilik maliyetinin bu teklif satırındaki tahmine dahil edileceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2de7a-144">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="2de7a-145">Bu değer, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşmesi satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="2de7a-145">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2de7a-146">Gider Ekle</span><span class="sxs-lookup"><span data-stu-id="2de7a-146">Include Expense</span></span> | <span data-ttu-id="2de7a-147">**Evet**/**Hayır** değeri, seçili projedeki gider maliyetlerinin bu teklif satırı tahminine dahil edilip edilmeyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="2de7a-147">A **Yes**/**No** value indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="2de7a-148">**Hayır** değeri, gider maliyetinin bu teklif satırındaki tahmine dahil edilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2de7a-148">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="2de7a-149">**Evet** değeri, gider maliyetinin bu teklif satırındaki tahmine dahil edileceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2de7a-149">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="2de7a-150">Bu değer, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşmesi satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="2de7a-150">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2de7a-151">Malzeme Ekle</span><span class="sxs-lookup"><span data-stu-id="2de7a-151">Include Material</span></span> | <span data-ttu-id="2de7a-152">**Evet**/**Hayır** değeri, seçili projedeki malzeme maliyetlerinin bu teklif satırı tahminine dahil edilip edilmeyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="2de7a-152">A **Yes**/**No** value indicates if material costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="2de7a-153">**Hayır** değeri, malzeme maliyetlerinin bu teklif satırı tahminine dahil edilmeyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="2de7a-153">A **No** value indicates that the material costs will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="2de7a-154">**Evet** değeri, malzeme maliyetlerinin bu teklif satırı tahminine dahil edileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="2de7a-154">A **Yes** value indicates that the material costs will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="2de7a-155">Bu değer, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşmesi satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="2de7a-155">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2de7a-156">Ücret Ekle</span><span class="sxs-lookup"><span data-stu-id="2de7a-156">Include Fee</span></span> | <span data-ttu-id="2de7a-157">**Evet**/**Hayır** değeri, seçili projedeki ücretlerin bu teklif satırı tahminine dahil edilip edilmeyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="2de7a-157">A **Yes**/**No** value indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="2de7a-158">**Hayır** değeri, ücretlerin bu teklif satırındaki tahmine dahil edilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2de7a-158">A **No** value indicates that the fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="2de7a-159">**Evet** değeri, ücretlerin bu teklif satırındaki tahmine dahil edileceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2de7a-159">A **Yes** value indicates that the fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="2de7a-160">Bu değer, teklif kazanıldığında bu teklif satırından oluşturulan Proje sözleşmesi satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="2de7a-160">This value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2de7a-161">Teklif Edilen Tutar</span><span class="sxs-lookup"><span data-stu-id="2de7a-161">Quoted Amount</span></span> | <span data-ttu-id="2de7a-162">Bu, proje tabanlı teklif satırındaki tüm tahmin edilen çalışma için müşteriye teklif edilecek tutardır.</span><span class="sxs-lookup"><span data-stu-id="2de7a-162">This is the amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="2de7a-163">Fırsattan oluşturulan bir teklifte, bu değer fırsat satırındaki **Müşteri Bütçesi** alanından kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="2de7a-163">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="2de7a-164">Proje tabanlı teklif satırı satır ayrıntılarına sahip olduğunda, bu alan düzenlemeye kilitlenir ve teklif satırı ayrıntılarındaki tutardan özetlenir.</span><span class="sxs-lookup"><span data-stu-id="2de7a-164">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="2de7a-165">Bu değer, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşmesi satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="2de7a-165">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2de7a-166">Tahmini Vergi</span><span class="sxs-lookup"><span data-stu-id="2de7a-166">Estimated Tax</span></span> | <span data-ttu-id="2de7a-167">Bu, kullanıcının teklif satırına tahmini vergi tutarını ekleyebileceği düzenlenebilir bir alandır.</span><span class="sxs-lookup"><span data-stu-id="2de7a-167">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="2de7a-168">Proje tabanlı teklif satırı, satır ayrıntılarına sahip olduğunda, bu alan düzenlemeye kilitlenir ve teklif satırı ayrıntılarındaki vergi tutarından özetlenir.</span><span class="sxs-lookup"><span data-stu-id="2de7a-168">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="2de7a-169">Bu değer, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşmesi satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="2de7a-169">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2de7a-170">Vergi Sonrası Teklif Tutarı</span><span class="sxs-lookup"><span data-stu-id="2de7a-170">Quoted Amount after Tax</span></span> | <span data-ttu-id="2de7a-171">Bu alan, vergi sonrası teklif satırı tutarıdır ve salt okunurdur.</span><span class="sxs-lookup"><span data-stu-id="2de7a-171">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="2de7a-172">Bu alandaki tutar *Teklif Tutarı + Vergi* olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="2de7a-172">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="2de7a-173">Bu değer, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşmesi satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="2de7a-173">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2de7a-174">Aşılamaz Limit</span><span class="sxs-lookup"><span data-stu-id="2de7a-174">Not-to-exceed Limit</span></span> | <span data-ttu-id="2de7a-175">Bu alan, düzenlenebilirdir ve yalnızca **Zaman ve Malzeme** faturalama yöntemine sahip proje bazlı teklif satırlarında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="2de7a-175">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="2de7a-176">Bu değer, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşmesi satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="2de7a-176">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="2de7a-177">Müşteri Bütçesi</span><span class="sxs-lookup"><span data-stu-id="2de7a-177">Customer Budget</span></span> | <span data-ttu-id="2de7a-178">Bu alan, düzenlenebilirdir ve teklif bir fırsattan oluşturulmuşsa fırsat satırındaki ilgili alandan kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="2de7a-178">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="2de7a-179">Bu değer, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşmesi satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="2de7a-179">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="2de7a-180">Proje tabanlı teklif satırlarının Genel sekmesindeki alanları için doğrulama kuralları</span><span class="sxs-lookup"><span data-stu-id="2de7a-180">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="2de7a-181">**Kural 1**: **Eklenen Görevler** alanı boşsa veya bu alan **Tüm proje görevleri** olarak ayarlanmışsa teklif satırına bir proje dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="2de7a-181">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="2de7a-182">**Kural 2**: **Eklenen Görevler** alanı boşsa veya bu alan **Tüm proje görevleri** olarak ayarlanmışsa bir proje ve belirli bir işlem sınıfı, bir teklifin yalnızca proje tabanlı bir teklif satırına dahil edilebilir.</span><span class="sxs-lookup"><span data-stu-id="2de7a-182">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="2de7a-183">**Kural 3**: **Eklenen Görevler** alanı **Yalnızca seçili proje görevleri** olarak ayarlanmışsa bir proje ve belirli bir işlem sınıfı, bir teklifin birden çok proje tabanlı teklif satırına dahil edilebilir.</span><span class="sxs-lookup"><span data-stu-id="2de7a-183">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="2de7a-184">**Kural 4**: Bir fırsatın birden fazla teklifi varsa hepsi aynı projeye atıfta bulunan ve aynı işlem sınıfını içeren farklı tekliflerden teklif satırları olabilir.</span><span class="sxs-lookup"><span data-stu-id="2de7a-184">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="2de7a-185">**Kural 5**: Teklifler aynı fırsata ait değilse aynı projeyi ve işlem sınıfını içeremezler.</span><span class="sxs-lookup"><span data-stu-id="2de7a-185">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p><span data-ttu-id="2de7a-186">
                    <strong>Fırsat</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2de7a-186">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="39" valign="top">
                <p><span data-ttu-id="2de7a-187">
                    <strong>Teklif</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2de7a-187">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="40" valign="top">
                <p><span data-ttu-id="2de7a-188">
                    <strong>Teklif satırı</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2de7a-188">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="2de7a-189">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2de7a-189">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="77" valign="top">
                <p><span data-ttu-id="2de7a-190">
                    <strong>Dahil edilen görevler</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2de7a-190">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="45" valign="top">
                <p><span data-ttu-id="2de7a-191">
                    <strong>Zaman Ekle</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2de7a-191">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="46" valign="top">
                <p><span data-ttu-id="2de7a-192">
                    <strong>Gider Ekle</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2de7a-192">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="43" valign="top">
                <p><span data-ttu-id="2de7a-193">
                    <strong>Malzeme Ekle</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2de7a-193">
                    <strong>Include Material</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="2de7a-194">
                    <strong>Ekle</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2de7a-194">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="2de7a-195">
                    <strong>Ücret</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2de7a-195">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="49" valign="top">
                <p><span data-ttu-id="2de7a-196">
                    <strong>Geçerli/Geçerli değil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2de7a-196">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="200" valign="top">
                <p><span data-ttu-id="2de7a-197">
                    <strong>Neden</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2de7a-197">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="2de7a-198">O1</span><span class="sxs-lookup"><span data-stu-id="2de7a-198">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="2de7a-199">Ç1</span><span class="sxs-lookup"><span data-stu-id="2de7a-199">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="2de7a-200">QL1</span><span class="sxs-lookup"><span data-stu-id="2de7a-200">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2de7a-201">P1</span><span class="sxs-lookup"><span data-stu-id="2de7a-201">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="2de7a-202">Boş</span><span class="sxs-lookup"><span data-stu-id="2de7a-202">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="2de7a-203">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-203">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="2de7a-204">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-204">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2de7a-205">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-205">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2de7a-206">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-206">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2de7a-207">Geçerli değil</span><span class="sxs-lookup"><span data-stu-id="2de7a-207">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2de7a-208">Kural 2'nin ihlali.</span><span class="sxs-lookup"><span data-stu-id="2de7a-208">Violation of Rule #2.</span></span> <span data-ttu-id="2de7a-209">P1 projesindeki Zaman, Gider ve Ücretler, QL1 ve QL2 teklif satırlarına dahil edilir</span><span class="sxs-lookup"><span data-stu-id="2de7a-209">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="2de7a-210">O1</span><span class="sxs-lookup"><span data-stu-id="2de7a-210">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="2de7a-211">Ç1</span><span class="sxs-lookup"><span data-stu-id="2de7a-211">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="2de7a-212">QL2</span><span class="sxs-lookup"><span data-stu-id="2de7a-212">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2de7a-213">P1</span><span class="sxs-lookup"><span data-stu-id="2de7a-213">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="2de7a-214">Boş</span><span class="sxs-lookup"><span data-stu-id="2de7a-214">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="2de7a-215">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-215">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="2de7a-216">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-216">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2de7a-217">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-217">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2de7a-218">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-218">Yes</span></span> </p>
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
<span data-ttu-id="2de7a-219">O1</span><span class="sxs-lookup"><span data-stu-id="2de7a-219">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="2de7a-220">Ç1</span><span class="sxs-lookup"><span data-stu-id="2de7a-220">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="2de7a-221">QL1</span><span class="sxs-lookup"><span data-stu-id="2de7a-221">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2de7a-222">P1</span><span class="sxs-lookup"><span data-stu-id="2de7a-222">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="2de7a-223">Boş</span><span class="sxs-lookup"><span data-stu-id="2de7a-223">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="2de7a-224">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-224">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="2de7a-225">No</span><span class="sxs-lookup"><span data-stu-id="2de7a-225">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2de7a-226">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-226">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2de7a-227">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-227">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2de7a-228">Geçerli değil</span><span class="sxs-lookup"><span data-stu-id="2de7a-228">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2de7a-229">Kural 2'nin ihlali.</span><span class="sxs-lookup"><span data-stu-id="2de7a-229">Violation of Rule #2.</span></span> <span data-ttu-id="2de7a-230">P1 projesindeki Zaman, Malzeme ve Ücretler, QL1 ve QL2 teklif satırlarına dahil edilir</span><span class="sxs-lookup"><span data-stu-id="2de7a-230">Time, Material, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="2de7a-231">O1</span><span class="sxs-lookup"><span data-stu-id="2de7a-231">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="2de7a-232">Ç1</span><span class="sxs-lookup"><span data-stu-id="2de7a-232">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="2de7a-233">QL2</span><span class="sxs-lookup"><span data-stu-id="2de7a-233">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2de7a-234">P1</span><span class="sxs-lookup"><span data-stu-id="2de7a-234">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="2de7a-235">Boş</span><span class="sxs-lookup"><span data-stu-id="2de7a-235">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="2de7a-236">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-236">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="2de7a-237">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-237">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2de7a-238">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-238">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2de7a-239">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-239">Yes</span></span> </p>
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
<span data-ttu-id="2de7a-240">O1</span><span class="sxs-lookup"><span data-stu-id="2de7a-240">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="2de7a-241">Ç1</span><span class="sxs-lookup"><span data-stu-id="2de7a-241">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="2de7a-242">QL1</span><span class="sxs-lookup"><span data-stu-id="2de7a-242">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2de7a-243">P1</span><span class="sxs-lookup"><span data-stu-id="2de7a-243">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="2de7a-244">Boş</span><span class="sxs-lookup"><span data-stu-id="2de7a-244">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="2de7a-245">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-245">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="2de7a-246">No</span><span class="sxs-lookup"><span data-stu-id="2de7a-246">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2de7a-247">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-247">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2de7a-248">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-248">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2de7a-249">Geçerli</span><span class="sxs-lookup"><span data-stu-id="2de7a-249">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2de7a-250">P1 projesindeki Zaman, Malzeme ve Ücretler QL1'e dahil edilir</span><span class="sxs-lookup"><span data-stu-id="2de7a-250">Time, Material, and Fees on P1 project are included on QL1</span></span> <br>
<span data-ttu-id="2de7a-251">P1 projesindeki giderler QL2'ye dahildir</span><span class="sxs-lookup"><span data-stu-id="2de7a-251">Expense on P1 project is included on QL2</span></span> <br>
<span data-ttu-id="2de7a-252">Her bir teklif satırına dahil edilenler arasında çakışma yok ve bu nedenle geçerli.</span><span class="sxs-lookup"><span data-stu-id="2de7a-252">No overlap in what is being included on each quote line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="2de7a-253">O1</span><span class="sxs-lookup"><span data-stu-id="2de7a-253">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="2de7a-254">Ç1</span><span class="sxs-lookup"><span data-stu-id="2de7a-254">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="2de7a-255">QL2</span><span class="sxs-lookup"><span data-stu-id="2de7a-255">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2de7a-256">P1</span><span class="sxs-lookup"><span data-stu-id="2de7a-256">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="2de7a-257">Boş</span><span class="sxs-lookup"><span data-stu-id="2de7a-257">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="2de7a-258">No</span><span class="sxs-lookup"><span data-stu-id="2de7a-258">No</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="2de7a-259">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-259">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2de7a-260">No</span><span class="sxs-lookup"><span data-stu-id="2de7a-260">No</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2de7a-261">No</span><span class="sxs-lookup"><span data-stu-id="2de7a-261">No</span></span> </p>
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
<span data-ttu-id="2de7a-262">O1</span><span class="sxs-lookup"><span data-stu-id="2de7a-262">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="2de7a-263">Ç1</span><span class="sxs-lookup"><span data-stu-id="2de7a-263">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="2de7a-264">QL1</span><span class="sxs-lookup"><span data-stu-id="2de7a-264">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2de7a-265">P1</span><span class="sxs-lookup"><span data-stu-id="2de7a-265">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="2de7a-266">Yalnızca seçili görevler</span><span class="sxs-lookup"><span data-stu-id="2de7a-266">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="2de7a-267">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-267">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="2de7a-268">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-268">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2de7a-269">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-269">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2de7a-270">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-270">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2de7a-271">Geçerli değil</span><span class="sxs-lookup"><span data-stu-id="2de7a-271">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2de7a-272">Kural 2'nin ihlali</span><span class="sxs-lookup"><span data-stu-id="2de7a-272">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="2de7a-273">Q1'e, proje P1 üzerindeki bir görev alt kümesinde Zaman, Malzeme, Giderler ve Ücretler dahildir</span><span class="sxs-lookup"><span data-stu-id="2de7a-273">Q1 includes Time, Material, Expenses and Fees on a subset of tasks on project P1</span></span> </p>
                <p>
<span data-ttu-id="2de7a-274">QL2 tüm proje P1 için Zaman, Giderler ve Ücretleri içerir, bu nedenle Q1'in içerdiği verilerle örtüşür.</span><span class="sxs-lookup"><span data-stu-id="2de7a-274">QL2 includes Time, Expenses, and Fees for the whole project P1 and therefore overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="2de7a-275">O1</span><span class="sxs-lookup"><span data-stu-id="2de7a-275">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="2de7a-276">Ç1</span><span class="sxs-lookup"><span data-stu-id="2de7a-276">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="2de7a-277">QL2</span><span class="sxs-lookup"><span data-stu-id="2de7a-277">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2de7a-278">P1</span><span class="sxs-lookup"><span data-stu-id="2de7a-278">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="2de7a-279">Boş</span><span class="sxs-lookup"><span data-stu-id="2de7a-279">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="2de7a-280">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-280">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="2de7a-281">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-281">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2de7a-282">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-282">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2de7a-283">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-283">Yes</span></span> </p>
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
<span data-ttu-id="2de7a-284">O1</span><span class="sxs-lookup"><span data-stu-id="2de7a-284">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="2de7a-285">Ç1</span><span class="sxs-lookup"><span data-stu-id="2de7a-285">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="2de7a-286">QL1</span><span class="sxs-lookup"><span data-stu-id="2de7a-286">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2de7a-287">P1</span><span class="sxs-lookup"><span data-stu-id="2de7a-287">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="2de7a-288">Yalnızca seçili görevler</span><span class="sxs-lookup"><span data-stu-id="2de7a-288">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="2de7a-289">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-289">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="2de7a-290">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-290">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2de7a-291">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-291">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2de7a-292">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-292">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2de7a-293">Geçerli</span><span class="sxs-lookup"><span data-stu-id="2de7a-293">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2de7a-294">Kural 3 uyarınca,</span><span class="sxs-lookup"><span data-stu-id="2de7a-294">Per Rule #3,</span></span> </p>
                <p>
<span data-ttu-id="2de7a-295">Q1'e, proje P1 üzerindeki bir görev alt kümesinde Zaman, Malzeme, Giderler ve Ücretler dahildir.</span><span class="sxs-lookup"><span data-stu-id="2de7a-295">Q1 includes Time, Material, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="2de7a-296">QL2'e, proje P1 üzerindeki bir görev alt kümesi için Zaman, Malzeme ve Giderler dahildir.</span><span class="sxs-lookup"><span data-stu-id="2de7a-296">QL2 includes Time, Material, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="2de7a-297">Yalnızca tek bir ek doğrulama yapılır. Bu doğrulamanın amacı, çakışmaları önlemek için QL1 üzerindeki alt görevlerin QL2 üzerindeki alt görevlerden farklı olmasını kontrol etmektir.</span><span class="sxs-lookup"><span data-stu-id="2de7a-297">The only additional validation is around the subset of tasks on QL1 which is different from the subset of tasks on QL2 to ensure that there is no overlap.</span></span> <span data-ttu-id="2de7a-298">Bu, görevler ilişkilendirildiğinde sistem tarafından yapılır.</span><span class="sxs-lookup"><span data-stu-id="2de7a-298">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="2de7a-299">O1</span><span class="sxs-lookup"><span data-stu-id="2de7a-299">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="2de7a-300">Ç1</span><span class="sxs-lookup"><span data-stu-id="2de7a-300">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="2de7a-301">QL2</span><span class="sxs-lookup"><span data-stu-id="2de7a-301">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2de7a-302">P1</span><span class="sxs-lookup"><span data-stu-id="2de7a-302">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="2de7a-303">Yalnızca seçili görevler</span><span class="sxs-lookup"><span data-stu-id="2de7a-303">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="2de7a-304">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-304">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="2de7a-305">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-305">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2de7a-306">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-306">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2de7a-307">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-307">Yes</span></span> </p>
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
<span data-ttu-id="2de7a-308">O1</span><span class="sxs-lookup"><span data-stu-id="2de7a-308">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="2de7a-309">Ç1</span><span class="sxs-lookup"><span data-stu-id="2de7a-309">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="2de7a-310">QL1</span><span class="sxs-lookup"><span data-stu-id="2de7a-310">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2de7a-311">P1</span><span class="sxs-lookup"><span data-stu-id="2de7a-311">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="2de7a-312">Tüm proje görevleri veya boş</span><span class="sxs-lookup"><span data-stu-id="2de7a-312">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="2de7a-313">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-313">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="2de7a-314">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-314">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2de7a-315">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-315">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2de7a-316">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-316">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2de7a-317">Geçerli</span><span class="sxs-lookup"><span data-stu-id="2de7a-317">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2de7a-318">Kural 5 uyarınca, Q1 ve Q2 aynı fırsata yönelik iki tekliftir, bu nedenle ikisi de aynı proje bileşenleri için tahminde bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="2de7a-318">Per Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="2de7a-319">O1</span><span class="sxs-lookup"><span data-stu-id="2de7a-319">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="2de7a-320">Ç2</span><span class="sxs-lookup"><span data-stu-id="2de7a-320">Q2</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="2de7a-321">QL1</span><span class="sxs-lookup"><span data-stu-id="2de7a-321">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2de7a-322">P1</span><span class="sxs-lookup"><span data-stu-id="2de7a-322">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="2de7a-323">Tüm proje görevleri veya boş</span><span class="sxs-lookup"><span data-stu-id="2de7a-323">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="2de7a-324">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-324">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="2de7a-325">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-325">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2de7a-326">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-326">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2de7a-327">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-327">Yes</span></span> </p>
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
<span data-ttu-id="2de7a-328">O1</span><span class="sxs-lookup"><span data-stu-id="2de7a-328">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="2de7a-329">Ç1</span><span class="sxs-lookup"><span data-stu-id="2de7a-329">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="2de7a-330">QL1</span><span class="sxs-lookup"><span data-stu-id="2de7a-330">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2de7a-331">P1</span><span class="sxs-lookup"><span data-stu-id="2de7a-331">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="2de7a-332">Tüm proje görevleri veya boş</span><span class="sxs-lookup"><span data-stu-id="2de7a-332">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="2de7a-333">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-333">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="2de7a-334">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-334">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2de7a-335">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-335">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2de7a-336">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-336">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2de7a-337">Geçerli Değil</span><span class="sxs-lookup"><span data-stu-id="2de7a-337">Not Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2de7a-338">Kural 4 uyarınca, Q1 ve Q2 farklı fırsatlara yönelik iki tekliftir, bu nedenle ikisi de aynı projenin aynı bileşenleri için tahminde bulunamaz.</span><span class="sxs-lookup"><span data-stu-id="2de7a-338">Per Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="2de7a-339">O2</span><span class="sxs-lookup"><span data-stu-id="2de7a-339">O2</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="2de7a-340">Ç1</span><span class="sxs-lookup"><span data-stu-id="2de7a-340">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="2de7a-341">QL1</span><span class="sxs-lookup"><span data-stu-id="2de7a-341">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2de7a-342">P1</span><span class="sxs-lookup"><span data-stu-id="2de7a-342">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="2de7a-343">Tüm proje görevleri veya boş</span><span class="sxs-lookup"><span data-stu-id="2de7a-343">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="2de7a-344">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-344">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="2de7a-345">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-345">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="2de7a-346">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-346">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="2de7a-347">Evet</span><span class="sxs-lookup"><span data-stu-id="2de7a-347">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
