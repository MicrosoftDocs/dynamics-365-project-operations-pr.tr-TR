---
title: Proje tabanlı teklif satırlarına genel bakış
description: Bu konuda, proje çalışmaları için proje tabanlı teklif satırlarını kullanma hakkında bilgiler sağlanmaktadır.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e61a9fbf357123884397b930662d11f22bfdeaa0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277812"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="74e6b-103">Proje tabanlı teklif satırlarına genel bakış</span><span class="sxs-lookup"><span data-stu-id="74e6b-103">Project-based quote lines overview</span></span>

<span data-ttu-id="74e6b-104">_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="74e6b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="74e6b-105">Proje tabanlı teklif satırları, bir etkileşimdeki proje çalışmalarının tahmin edilmesine yardımcı olmak için tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="74e6b-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="74e6b-106">Proje tabanlı teklif satırının yapısı, aşağıdaki kavramlarla proje tahminleri için genişletilmiştir:</span><span class="sxs-lookup"><span data-stu-id="74e6b-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="74e6b-107">Faturalama Yöntemi</span><span class="sxs-lookup"><span data-stu-id="74e6b-107">Billing Method</span></span>
- <span data-ttu-id="74e6b-108">Proje Eşlemesi</span><span class="sxs-lookup"><span data-stu-id="74e6b-108">Project Mapping</span></span>
- <span data-ttu-id="74e6b-109">Dahil Edilen İşlem sınıfları</span><span class="sxs-lookup"><span data-stu-id="74e6b-109">Included Transaction classes</span></span>
- <span data-ttu-id="74e6b-110">Aşılamaz Limit</span><span class="sxs-lookup"><span data-stu-id="74e6b-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="74e6b-111">Borçlandırılabilirlik ayarı</span><span class="sxs-lookup"><span data-stu-id="74e6b-111">Chargeability setup</span></span>
- <span data-ttu-id="74e6b-112">Teklif Satırı Ayrıntılarını kullanarak tahmin yürütme</span><span class="sxs-lookup"><span data-stu-id="74e6b-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="74e6b-113">Teklif satırı Müşterileri</span><span class="sxs-lookup"><span data-stu-id="74e6b-113">Quote line Customers</span></span>

<span data-ttu-id="74e6b-114">Aşağıdaki tabloda proje tabanlı teklif satırının **Genel** sekmesindeki alanlar hakkında bilgi sağlanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="74e6b-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="74e6b-115">Bu alanlar, proje çalışmaları için ayrıntılı, baştan sona bir tahmin için temel oluşturulmasına yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="74e6b-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="74e6b-116">**Alan**</span><span class="sxs-lookup"><span data-stu-id="74e6b-116">**Field**</span></span> | <span data-ttu-id="74e6b-117">**Açıklama**</span><span class="sxs-lookup"><span data-stu-id="74e6b-117">**Description**</span></span> | <span data-ttu-id="74e6b-118">**Aşağı yönlü etki**</span><span class="sxs-lookup"><span data-stu-id="74e6b-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="74e6b-119">Veri Akışı Adı</span><span class="sxs-lookup"><span data-stu-id="74e6b-119">Name</span></span> | <span data-ttu-id="74e6b-120">Tahmin edilen teklifin farklı olan bileşenini belirlemenize yardımcı olması gereken teklif satırının adı.</span><span class="sxs-lookup"><span data-stu-id="74e6b-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="74e6b-121">Teklif kazanıldığında, bu teklif satırından oluşturulan proje sözleşme satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="74e6b-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="74e6b-122">Faturalama Yöntemi</span><span class="sxs-lookup"><span data-stu-id="74e6b-122">Billing Method</span></span> | <span data-ttu-id="74e6b-123">Fırsattan oluşturulan bir teklifte bu değer, fırsat satırındaki ilgili alandan kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="74e6b-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="74e6b-124">Bu alan, Dynamics 365 Project Operations tarafından desteklenen iki ana sözleşme modeli içerir:</span><span class="sxs-lookup"><span data-stu-id="74e6b-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="74e6b-125">- Sabit fiyat</span><span class="sxs-lookup"><span data-stu-id="74e6b-125">- Fixed price</span></span></br><span data-ttu-id="74e6b-126">- Zaman ve malzeme.</span><span class="sxs-lookup"><span data-stu-id="74e6b-126">- Time and material.</span></span>| <span data-ttu-id="74e6b-127">Bu alanın değeri, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşme satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="74e6b-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="74e6b-128">Project</span><span class="sxs-lookup"><span data-stu-id="74e6b-128">Project</span></span> | <span data-ttu-id="74e6b-129">Bu etkileşimde kullanılacak projeyi belirleyerek çalışmayı teslim etmek için bu isteğe bağlı alanı kullanın.</span><span class="sxs-lookup"><span data-stu-id="74e6b-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="74e6b-130">Proje bir teklif satırına eşlendiğinde, borçlandırılabilir görevler oluşturulmasına ve ayrıca proje bazlı bir tahminin teklif satırına teklif satırı ayrıntıları olarak getirilmesine yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="74e6b-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="74e6b-131">Proje, proje bazlı bir teklif satırına eşlenmediğinde tahmin, her bir teklif satırı ayrıntısının el ile oluşturulmasıyla elde edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="74e6b-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="74e6b-132">Bu alanın değeri, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşme satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="74e6b-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="74e6b-133">Zaman Ekle</span><span class="sxs-lookup"><span data-stu-id="74e6b-133">Include Time</span></span> | <span data-ttu-id="74e6b-134">**Evet**/**Hayır** bayrağı, seçilen projedeki zaman işlemlerinin veya işçilik maliyetlerinin bu teklif satırındaki tahmine dahil edilip edilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="74e6b-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="74e6b-135">**Hayır** değeri, zaman işlemlerinin veya işçilik maliyetinin bu teklif satırındaki tahmine dahil edilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="74e6b-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="74e6b-136">**Evet** değeri, zaman işlemlerinin veya işçilik maliyetinin bu teklif satırındaki tahmine dahil edileceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="74e6b-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="74e6b-137">Bu alanın değeri, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşme satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="74e6b-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="74e6b-138">Gider Ekle</span><span class="sxs-lookup"><span data-stu-id="74e6b-138">Include Expense</span></span> | <span data-ttu-id="74e6b-139">**Evet**/**Hayır** bayrağı, seçilen projedeki gider maliyetlerinin bu teklif satırındaki tahmine dahil edilip edilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="74e6b-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="74e6b-140">**Hayır** değeri, gider maliyetinin bu teklif satırındaki tahmine dahil edilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="74e6b-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="74e6b-141">**Evet** değeri, gider maliyetinin bu teklif satırındaki tahmine dahil edileceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="74e6b-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="74e6b-142">Bu alanın değeri, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşme satırının üzerine kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="74e6b-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="74e6b-143">Ücret Ekle</span><span class="sxs-lookup"><span data-stu-id="74e6b-143">Include Fee</span></span> | <span data-ttu-id="74e6b-144">**Evet**/**Hayır** bayrağı, seçilen projedeki ücretlerin bu teklif satırındaki tahmine dahil edilip edilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="74e6b-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="74e6b-145">**Hayır** değeri, Ücretlerin bu teklif satırındaki tahmine dahil edilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="74e6b-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="74e6b-146">**Evet** değeri, Ücretlerin bu teklif satırındaki tahmine dahil edileceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="74e6b-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="74e6b-147">Bu alanın değeri, teklif kazanıldığında bu teklif satırından oluşturulan Proje sözleşme satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="74e6b-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="74e6b-148">Teklif Edilen Tutar</span><span class="sxs-lookup"><span data-stu-id="74e6b-148">Quoted Amount</span></span> | <span data-ttu-id="74e6b-149">Bu, proje tabanlı teklif satırında tahmin edilen tüm çalışmalar için müşteriye teklif edilecek tutardır.</span><span class="sxs-lookup"><span data-stu-id="74e6b-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="74e6b-150">Fırsattan oluşturulan bir teklifte, bu değer fırsat satırındaki **Müşteri Bütçesi** alanından kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="74e6b-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="74e6b-151">Proje tabanlı teklif satırı satır ayrıntılarına sahip olduğunda, bu alan düzenlemeye kilitlenir ve teklif satırı ayrıntılarındaki tutardan özetlenir.</span><span class="sxs-lookup"><span data-stu-id="74e6b-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="74e6b-152">Bu alanın değeri, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşme satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="74e6b-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="74e6b-153">Tahmini Vergi</span><span class="sxs-lookup"><span data-stu-id="74e6b-153">Estimated Tax</span></span> | <span data-ttu-id="74e6b-154">Bu, kullanıcının teklif satırına tahmini vergi tutarını ekleyebileceği düzenlenebilir bir alandır.</span><span class="sxs-lookup"><span data-stu-id="74e6b-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="74e6b-155">Proje tabanlı teklif satırı, satır ayrıntılarına sahip olduğunda, bu alan düzenlemeye kilitlenir ve teklif satırı ayrıntılarındaki vergi tutarından özetlenir.</span><span class="sxs-lookup"><span data-stu-id="74e6b-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="74e6b-156">Bu alanın değeri, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşme satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="74e6b-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="74e6b-157">Vergi Sonrası Teklif Tutarı</span><span class="sxs-lookup"><span data-stu-id="74e6b-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="74e6b-158">Bu alan, vergi sonrası teklif satırı tutarıdır ve salt okunurdur.</span><span class="sxs-lookup"><span data-stu-id="74e6b-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="74e6b-159">Bu alandaki tutar *Teklif Tutarı + Vergi* olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="74e6b-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="74e6b-160">Bu alanın değeri, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşme satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="74e6b-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="74e6b-161">Aşılamaz Limit</span><span class="sxs-lookup"><span data-stu-id="74e6b-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="74e6b-162">Bu alan, düzenlenebilirdir ve yalnızca **Zaman ve Malzeme** faturalama yöntemine sahip proje bazlı teklif satırlarında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="74e6b-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="74e6b-163">Bu alanın değeri, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşme satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="74e6b-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="74e6b-164">Müşteri Bütçesi</span><span class="sxs-lookup"><span data-stu-id="74e6b-164">Customer Budget</span></span> | <span data-ttu-id="74e6b-165">Bu alan, düzenlenebilirdir ve teklif bir fırsattan oluşturulmuşsa fırsat satırındaki ilgili alandan kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="74e6b-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="74e6b-166">Bu alanın değeri, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşme satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="74e6b-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="74e6b-167">Proje tabanlı teklif satırlarının Genel sekmesindeki alanları için doğrulama kuralları</span><span class="sxs-lookup"><span data-stu-id="74e6b-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="74e6b-168">**Kural 1**: Seçilen projedeki belirli bir işlem sınıfı bir teklifin yalnızca bir proje tabanlı teklif satırına dahil edilebilir.</span><span class="sxs-lookup"><span data-stu-id="74e6b-168">**Rule 1**: A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="74e6b-169">**Kural 2**: Bir fırsatın birden fazla teklifi varsa hepsi aynı projeye atıfta bulunan ve aynı işlem sınıfını içeren farklı tekliflerden teklif satırları olabilir.</span><span class="sxs-lookup"><span data-stu-id="74e6b-169">**Rule 2**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="74e6b-170">**Kural 3**: Teklifler aynı fırsata ait değilse aynı projeyi ve işlem sınıfını içeremezler.</span><span class="sxs-lookup"><span data-stu-id="74e6b-170">**Rule 3**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="74e6b-171">
                    <strong>Fırsat</strong>
                </span><span class="sxs-lookup"><span data-stu-id="74e6b-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="74e6b-172">
                    <strong>Teklif</strong>
                </span><span class="sxs-lookup"><span data-stu-id="74e6b-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="74e6b-173">
                    <strong>Teklif satırı</strong>
                </span><span class="sxs-lookup"><span data-stu-id="74e6b-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="74e6b-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="74e6b-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="74e6b-175">
                    <strong>Zaman ekle</strong>
                </span><span class="sxs-lookup"><span data-stu-id="74e6b-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="74e6b-176">
                    <strong>Gider ekle</strong>
                </span><span class="sxs-lookup"><span data-stu-id="74e6b-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="74e6b-177">
                    <strong>Ekle</strong>
                </span><span class="sxs-lookup"><span data-stu-id="74e6b-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="74e6b-178">
                    <strong>ücret</strong>
                </span><span class="sxs-lookup"><span data-stu-id="74e6b-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="74e6b-179">
                    <strong>Geçerli/Geçerli değil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="74e6b-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="74e6b-180">
                    <strong>Neden</strong>
                </span><span class="sxs-lookup"><span data-stu-id="74e6b-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="74e6b-181">O1</span><span class="sxs-lookup"><span data-stu-id="74e6b-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="74e6b-182">Ç1</span><span class="sxs-lookup"><span data-stu-id="74e6b-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="74e6b-183">QL1</span><span class="sxs-lookup"><span data-stu-id="74e6b-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="74e6b-184">P1</span><span class="sxs-lookup"><span data-stu-id="74e6b-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="74e6b-185">Evet</span><span class="sxs-lookup"><span data-stu-id="74e6b-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="74e6b-186">Evet</span><span class="sxs-lookup"><span data-stu-id="74e6b-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="74e6b-187">Evet</span><span class="sxs-lookup"><span data-stu-id="74e6b-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="74e6b-188">Geçerli değil</span><span class="sxs-lookup"><span data-stu-id="74e6b-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="74e6b-189">Kural 1'nin ihlali.</span><span class="sxs-lookup"><span data-stu-id="74e6b-189">Violation of Rule #1.</span></span> <span data-ttu-id="74e6b-190">P1 projesindeki Zaman, Gider ve Ücretler, QL1 ve QL2 teklif satırlarının her ikisine de dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="74e6b-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="74e6b-191">O1</span><span class="sxs-lookup"><span data-stu-id="74e6b-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="74e6b-192">Ç1</span><span class="sxs-lookup"><span data-stu-id="74e6b-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="74e6b-193">QL2</span><span class="sxs-lookup"><span data-stu-id="74e6b-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="74e6b-194">P1</span><span class="sxs-lookup"><span data-stu-id="74e6b-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="74e6b-195">Evet</span><span class="sxs-lookup"><span data-stu-id="74e6b-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="74e6b-196">Evet</span><span class="sxs-lookup"><span data-stu-id="74e6b-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="74e6b-197">Evet</span><span class="sxs-lookup"><span data-stu-id="74e6b-197">Yes</span></span> </p>
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
<span data-ttu-id="74e6b-198">O1</span><span class="sxs-lookup"><span data-stu-id="74e6b-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="74e6b-199">Ç1</span><span class="sxs-lookup"><span data-stu-id="74e6b-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="74e6b-200">QL1</span><span class="sxs-lookup"><span data-stu-id="74e6b-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="74e6b-201">P1</span><span class="sxs-lookup"><span data-stu-id="74e6b-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="74e6b-202">Evet</span><span class="sxs-lookup"><span data-stu-id="74e6b-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="74e6b-203">No</span><span class="sxs-lookup"><span data-stu-id="74e6b-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="74e6b-204">Evet</span><span class="sxs-lookup"><span data-stu-id="74e6b-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="74e6b-205">Geçerli değil</span><span class="sxs-lookup"><span data-stu-id="74e6b-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="74e6b-206">Kural 1'nin ihlali.</span><span class="sxs-lookup"><span data-stu-id="74e6b-206">Violation of Rule #1.</span></span> <span data-ttu-id="74e6b-207">P1 projesindeki Zaman ve Ücretler, QL1 ve QL2 teklif satırlarının her ikisine de dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="74e6b-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="74e6b-208">O1</span><span class="sxs-lookup"><span data-stu-id="74e6b-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="74e6b-209">Ç1</span><span class="sxs-lookup"><span data-stu-id="74e6b-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="74e6b-210">QL2</span><span class="sxs-lookup"><span data-stu-id="74e6b-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="74e6b-211">P1</span><span class="sxs-lookup"><span data-stu-id="74e6b-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="74e6b-212">Evet</span><span class="sxs-lookup"><span data-stu-id="74e6b-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="74e6b-213">Evet</span><span class="sxs-lookup"><span data-stu-id="74e6b-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="74e6b-214">Evet</span><span class="sxs-lookup"><span data-stu-id="74e6b-214">Yes</span></span> </p>
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
<span data-ttu-id="74e6b-215">O1</span><span class="sxs-lookup"><span data-stu-id="74e6b-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="74e6b-216">Ç1</span><span class="sxs-lookup"><span data-stu-id="74e6b-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="74e6b-217">QL1</span><span class="sxs-lookup"><span data-stu-id="74e6b-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="74e6b-218">P1</span><span class="sxs-lookup"><span data-stu-id="74e6b-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="74e6b-219">Evet</span><span class="sxs-lookup"><span data-stu-id="74e6b-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="74e6b-220">No</span><span class="sxs-lookup"><span data-stu-id="74e6b-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="74e6b-221">Evet</span><span class="sxs-lookup"><span data-stu-id="74e6b-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="74e6b-222">Geçerli</span><span class="sxs-lookup"><span data-stu-id="74e6b-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="74e6b-223">P1 projesindeki zaman ve ücretler, QL1'e dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="74e6b-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="74e6b-224">P1 projesindeki giderler QL2'ye dahildir.</span><span class="sxs-lookup"><span data-stu-id="74e6b-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="74e6b-225">Dahil edilen teklif satırlarının hiçbirinin birbiriyle çakışması yoktur ve bu yüzden geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="74e6b-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="74e6b-226">O1</span><span class="sxs-lookup"><span data-stu-id="74e6b-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="74e6b-227">Ç1</span><span class="sxs-lookup"><span data-stu-id="74e6b-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="74e6b-228">QL2</span><span class="sxs-lookup"><span data-stu-id="74e6b-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="74e6b-229">P1</span><span class="sxs-lookup"><span data-stu-id="74e6b-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="74e6b-230">No</span><span class="sxs-lookup"><span data-stu-id="74e6b-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="74e6b-231">Evet</span><span class="sxs-lookup"><span data-stu-id="74e6b-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="74e6b-232">No</span><span class="sxs-lookup"><span data-stu-id="74e6b-232">No</span></span> </p>
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
<span data-ttu-id="74e6b-233">O1</span><span class="sxs-lookup"><span data-stu-id="74e6b-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="74e6b-234">Ç1</span><span class="sxs-lookup"><span data-stu-id="74e6b-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="74e6b-235">QL1</span><span class="sxs-lookup"><span data-stu-id="74e6b-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="74e6b-236">P1</span><span class="sxs-lookup"><span data-stu-id="74e6b-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="74e6b-237">Evet</span><span class="sxs-lookup"><span data-stu-id="74e6b-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="74e6b-238">Evet</span><span class="sxs-lookup"><span data-stu-id="74e6b-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="74e6b-239">Evet</span><span class="sxs-lookup"><span data-stu-id="74e6b-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="74e6b-240">Geçerli değil</span><span class="sxs-lookup"><span data-stu-id="74e6b-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="74e6b-241">Kural 1'nin yukarıdaki ihlali</span><span class="sxs-lookup"><span data-stu-id="74e6b-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="74e6b-242">Q1, P1 projesinin tamamı için Zaman, Giderler ve Ücretleri içerir.</span><span class="sxs-lookup"><span data-stu-id="74e6b-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="74e6b-243">QL2, P1 projesinin tamamı için Zaman, Giderler ve Ücretleri içerir ve Q1'e dahil olanlarla örtüşür.</span><span class="sxs-lookup"><span data-stu-id="74e6b-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="74e6b-244">O1</span><span class="sxs-lookup"><span data-stu-id="74e6b-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="74e6b-245">Ç1</span><span class="sxs-lookup"><span data-stu-id="74e6b-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="74e6b-246">QL2</span><span class="sxs-lookup"><span data-stu-id="74e6b-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="74e6b-247">P1</span><span class="sxs-lookup"><span data-stu-id="74e6b-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="74e6b-248">Evet</span><span class="sxs-lookup"><span data-stu-id="74e6b-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="74e6b-249">Evet</span><span class="sxs-lookup"><span data-stu-id="74e6b-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="74e6b-250">Evet</span><span class="sxs-lookup"><span data-stu-id="74e6b-250">Yes</span></span> </p>
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
<span data-ttu-id="74e6b-251">O1</span><span class="sxs-lookup"><span data-stu-id="74e6b-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="74e6b-252">Ç1</span><span class="sxs-lookup"><span data-stu-id="74e6b-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="74e6b-253">QL1</span><span class="sxs-lookup"><span data-stu-id="74e6b-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="74e6b-254">P1</span><span class="sxs-lookup"><span data-stu-id="74e6b-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="74e6b-255">Evet</span><span class="sxs-lookup"><span data-stu-id="74e6b-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="74e6b-256">Evet</span><span class="sxs-lookup"><span data-stu-id="74e6b-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="74e6b-257">Evet</span><span class="sxs-lookup"><span data-stu-id="74e6b-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="74e6b-258">Geçerli</span><span class="sxs-lookup"><span data-stu-id="74e6b-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="74e6b-259">Kural 2'e göre, Q1 ve Q2 aynı fırsatta iki tekliftir; böylelikle projenin aynı bileşenleri için ikisi de tahmin edilebilir.</span><span class="sxs-lookup"><span data-stu-id="74e6b-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="74e6b-260">O1</span><span class="sxs-lookup"><span data-stu-id="74e6b-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="74e6b-261">Ç2</span><span class="sxs-lookup"><span data-stu-id="74e6b-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="74e6b-262">Q2'de QL1</span><span class="sxs-lookup"><span data-stu-id="74e6b-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="74e6b-263">P1</span><span class="sxs-lookup"><span data-stu-id="74e6b-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="74e6b-264">Evet</span><span class="sxs-lookup"><span data-stu-id="74e6b-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="74e6b-265">Evet</span><span class="sxs-lookup"><span data-stu-id="74e6b-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="74e6b-266">Evet</span><span class="sxs-lookup"><span data-stu-id="74e6b-266">Yes</span></span> </p>
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
<span data-ttu-id="74e6b-267">O1</span><span class="sxs-lookup"><span data-stu-id="74e6b-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="74e6b-268">Ç1</span><span class="sxs-lookup"><span data-stu-id="74e6b-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="74e6b-269">QL1</span><span class="sxs-lookup"><span data-stu-id="74e6b-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="74e6b-270">P1</span><span class="sxs-lookup"><span data-stu-id="74e6b-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="74e6b-271">Evet</span><span class="sxs-lookup"><span data-stu-id="74e6b-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="74e6b-272">Evet</span><span class="sxs-lookup"><span data-stu-id="74e6b-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="74e6b-273">Evet</span><span class="sxs-lookup"><span data-stu-id="74e6b-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="74e6b-274">Geçerli</span><span class="sxs-lookup"><span data-stu-id="74e6b-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="74e6b-275">Kural #3 göre, Q1 ve Q2 farklı fırsatlarda iki tekliftir; bu nedenle aynı projenin aynı bileşenleri için tahmin edilemezler.</span><span class="sxs-lookup"><span data-stu-id="74e6b-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="74e6b-276">O2</span><span class="sxs-lookup"><span data-stu-id="74e6b-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="74e6b-277">Ç1</span><span class="sxs-lookup"><span data-stu-id="74e6b-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="74e6b-278">QL1</span><span class="sxs-lookup"><span data-stu-id="74e6b-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="74e6b-279">P1</span><span class="sxs-lookup"><span data-stu-id="74e6b-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="74e6b-280">Evet</span><span class="sxs-lookup"><span data-stu-id="74e6b-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="74e6b-281">Evet</span><span class="sxs-lookup"><span data-stu-id="74e6b-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="74e6b-282">Evet</span><span class="sxs-lookup"><span data-stu-id="74e6b-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="74e6b-283">Geçerli Değil</span><span class="sxs-lookup"><span data-stu-id="74e6b-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../includes/footer-banner.md)]