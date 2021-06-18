---
title: Düzeltici proje tabanlı faturalar oluşturma
description: Bu konu, Project Operations'ta düzeltici faturalar hakkında bilgi sağlar.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f0423fe9895b91431b2a83a8fff81118205b0736
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001660"
---
# <a name="create-corrective-project-based-invoices"></a><span data-ttu-id="680a9-103">Düzeltici proje tabanlı faturalar oluşturma</span><span class="sxs-lookup"><span data-stu-id="680a9-103">Create corrective project-based invoices</span></span> 

<span data-ttu-id="680a9-104">_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="680a9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="680a9-105">Onaylı proje faturaları müşteri ve proje yöneticisiyle görüşülür, değişiklikleri veya kredileri işlemek için düzeltilebilir.</span><span class="sxs-lookup"><span data-stu-id="680a9-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="680a9-106">Onaylı bir faturada düzenlemeler yapmak için, onaylanan faturayı açın ve **Bu faturayı Düzelt**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="680a9-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="680a9-107">Bir proje faturası onaylanmadıkça bu seçim kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="680a9-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="680a9-108">Onaylanan faturadan yeni bir taslak fatura oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="680a9-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="680a9-109">Daha önce onaylanan faturadan tüm fatura satırı ayrıntıları yeni taslağın kopyası alınır.</span><span class="sxs-lookup"><span data-stu-id="680a9-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="680a9-110">Aşağıda, yeni düzeltilen faturada satır ayrıntıları hakkında daha fazla bilgi edinmek için kullanabileceğiniz bazı önemli noktalar yer alır:</span><span class="sxs-lookup"><span data-stu-id="680a9-110">The following are some key points to help you understand more about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="680a9-111">Tüm miktarlar sıfıra güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="680a9-111">All quantities are updated to zero.</span></span> <span data-ttu-id="680a9-112">Bu, tüm faturalanan maddelerin tam olarak alacaklandırıldığını varsayar.</span><span class="sxs-lookup"><span data-stu-id="680a9-112">This assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="680a9-113">Gerekirse, bu miktarları, alacaklandırılan miktarı değil, faturalanan miktarı yansıtacak şekilde el ile güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="680a9-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="680a9-114">Girdiğiniz miktara bağlı olarak, uygulama alacaklı miktarı hesaplar.</span><span class="sxs-lookup"><span data-stu-id="680a9-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="680a9-115">Bu miktar, düzeltilen fatura onaylandığı zaman oluşturulan fiili değerlere yansıtılır.</span><span class="sxs-lookup"><span data-stu-id="680a9-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="680a9-116">Vergi tutarında değişiklikler yapıyorsanız, alacak kaydedilen vergi tutarını değil, doğru vergi tutarını girmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="680a9-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="680a9-117">Kilometre taşı düzeltmeleri her zaman tam kredi olarak işlenir.</span><span class="sxs-lookup"><span data-stu-id="680a9-117">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="680a9-118">Müşteri hatalı bir tutar için faturalandıysa, Retainer veya avans tutarları düzeltilebilir.</span><span class="sxs-lookup"><span data-stu-id="680a9-118">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="680a9-119">Önceden onaylanmış bir faturadaki giderlere göre mutabakat sağlamak için yanlış bir tutar kullanılmışsa, retainers ve avanslar mutabakatları düzeltilebilir.</span><span class="sxs-lookup"><span data-stu-id="680a9-119">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="680a9-120">Önceden faturalandırılmış diğer giderlere yönelik düzeltmeler olan fatura satırı ayrıntılarının **Düzeltme** alanı, **Evet** olarak ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="680a9-120">Invoice line details that are corrections to other already invoiced charges have the **Correction** field set to **Yes**.</span></span> <span data-ttu-id="680a9-121">Düzeltilen fatura satırı ayrıntıları olan faturalarda **Evet** olarak ayarlanmış **düzeltmeler vardır** adlı alanı bulunur.</span><span class="sxs-lookup"><span data-stu-id="680a9-121">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="680a9-122">Düzeltme faturasının onaylanması sırasında oluşturulan gerçek değerler</span><span class="sxs-lookup"><span data-stu-id="680a9-122">Actuals created on confirmation of a corrective invoice</span></span>

<span data-ttu-id="680a9-123">Aşağıdaki tabloda, bir düzeltici fatura onaylandıktan sonra oluşturulan gerçek değerler listelenmiştir.</span><span class="sxs-lookup"><span data-stu-id="680a9-123">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="680a9-124">
                    <strong>Senaryo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="680a9-124">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="680a9-125">
                    <strong>Onayda oluşturulan fiililer</strong>
                </span><span class="sxs-lookup"><span data-stu-id="680a9-125">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="680a9-126">Faturalandırılmış bir avans veya Retainer düzeltmesini onaylayın.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="680a9-126">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="680a9-127">Mutabakat için oluşturulan hizmetli nin veya avansın faturasız satış tersi.</span><span class="sxs-lookup"><span data-stu-id="680a9-127">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="680a9-128">Bu tutar, hizmetli veya avans faturalandığında oluşturulan negatifi iptal etmek amacıyla olduğundan pozitiftir.</span><span class="sxs-lookup"><span data-stu-id="680a9-128">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="680a9-129">Bir faturalanmış satış ters çevirme fiili, Retainer üzerindeki tutar için oluşturulur veya orijinal Faturalanan Satışlar tersine çevrilmesine karşı ilerletir.</span><span class="sxs-lookup"><span data-stu-id="680a9-129">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="680a9-130">Yeni faturalı satış fiili türü, Elde kalan avans veya elde kalan üzerindeki tutar için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="680a9-130">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="680a9-131">Mutabakat için kullanılacak olan hizmetli veya avansa dayalı düzeltilmiş fatura satırının negatif tutarının faturalandırılmamış satışları.</span><span class="sxs-lookup"><span data-stu-id="680a9-131">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="680a9-132">Daha önce mutabakat sağlanmış bir elde kalan veya avans düzeltmesi onayı.</span><span class="sxs-lookup"><span data-stu-id="680a9-132">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="680a9-133">Mutabakat için oluşturulan hizmetli nin veya avansın faturasız satış tersi.</span><span class="sxs-lookup"><span data-stu-id="680a9-133">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="680a9-134">Bu tutar, önceki mutabakat meydana geldiğinde oluşturulan negatifi iptal etmek amacıyla olduğundan pozitiftir.</span><span class="sxs-lookup"><span data-stu-id="680a9-134">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="680a9-135">Önceki faturadaki tutar için faturalı satış ters fiili.</span><span class="sxs-lookup"><span data-stu-id="680a9-135">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="680a9-136">Yeni faturalı satış fiili türü, doğrulanan faturaya uyguanan elde kalan doğrulanan tutar içindir.</span><span class="sxs-lookup"><span data-stu-id="680a9-136">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="680a9-137">Sonraki faturalarda mutabakat için kullanılacak olan hizmetli veya avansa dayalı düzeltilmiş fatura satırının negatif tutarının faturalandırılmamış satışları.</span><span class="sxs-lookup"><span data-stu-id="680a9-137">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="680a9-138">Daha önce faturalandırılmış bir zaman hareketinin tam kredisinin faturalandırılması.</span><span class="sxs-lookup"><span data-stu-id="680a9-138">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="680a9-139">Saat için orijinal fatura satırı ayrıntısındaki saat ve tutarı için faturalandırılmış satış tersi.</span><span class="sxs-lookup"><span data-stu-id="680a9-139">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="680a9-140">Saat için orijinal fatura satırı ayrıntısındaki saat ve tutarı için yeni faturalandırılmış satış fiili.</span><span class="sxs-lookup"><span data-stu-id="680a9-140">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="680a9-141">Bir zaman hareketinde kısmi kredi faturalama.</span><span class="sxs-lookup"><span data-stu-id="680a9-141">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="680a9-142">Saat için orijinal fatura satırı ayrıntısındaki saat ve tutarı için faturalandırılmış satış tersi.</span><span class="sxs-lookup"><span data-stu-id="680a9-142">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="680a9-143">Düzenlenen fatura satırı ayrıntısı üzerindeki saat ve tutar için ücretlendirilebilen yeni bir faturalanmamış satış fiili, satışların fiilinin tersine çevrilmesi ve eşdeğer faturalı satışların fiili.</span><span class="sxs-lookup"><span data-stu-id="680a9-143">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="680a9-144">Fatura satırı ayrıntısıyla düzeltilen rakamların düşüldükten sonra kalan saatler ve tutar için masraflandırılabilen yeni faturalandırılamayan satış fiili gerçek değeri.</span><span class="sxs-lookup"><span data-stu-id="680a9-144">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="680a9-145">Daha önce faturalandırılmış bir gider hareketinin tam kredisinin faturalandırılması.</span><span class="sxs-lookup"><span data-stu-id="680a9-145">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="680a9-146">Gider için orijinal fatura satırı ayrıntısındaki miktar ve tutarı için faturalandırılmış satış tersi.</span><span class="sxs-lookup"><span data-stu-id="680a9-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="680a9-147">Gider için orijinal fatura satırı ayrıntısındaki miktar ve tutarı için yeni faturalandırılmamış satış fiili.</span><span class="sxs-lookup"><span data-stu-id="680a9-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="680a9-148">Daha önce faturalandırılmış bir gider hareketinin kısmi kredisinin faturalandırılması.</span><span class="sxs-lookup"><span data-stu-id="680a9-148">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="680a9-149">Gider için orijinal fatura satırı ayrıntısında faturalandırılan miktar ve tutarı için faturalandırılmış satış tersi.</span><span class="sxs-lookup"><span data-stu-id="680a9-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="680a9-150">Doğrulanan fatura satırı ayrıntısı üzerindeki miktar ve tutar için ücretlendirilebilen yeni bir faturalanmamış satış fiili, satışların fiilinin tersine çevrilmesi ve eşdeğer faturalı satışların fiili.</span><span class="sxs-lookup"><span data-stu-id="680a9-150">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="680a9-151">Fatura satırı ayrıntısıyla düzeltilen rakamların düşüldükten sonra kalan miktar ve tutar için masraflandırılabilen yeni faturalandırılamayan satış fiili gerçek değeri.</span><span class="sxs-lookup"><span data-stu-id="680a9-151">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="680a9-152">Daha önce faturalandırılmış bir ücret hareketinin tam kredisinin faturalandırılması.</span><span class="sxs-lookup"><span data-stu-id="680a9-152">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="680a9-153">Ücret için orijinal fatura satırı ayrıntısındaki miktar ve tutarı için faturalandırılmış satış tersi.</span><span class="sxs-lookup"><span data-stu-id="680a9-153">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="680a9-154">Ücret için orijinal fatura satırı ayrıntısındaki miktar ve tutarı için yeni faturalandırılmamış satış fiili.</span><span class="sxs-lookup"><span data-stu-id="680a9-154">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="680a9-155">Daha önce faturalandırılmış bir ücret hareketinin kısmi kredisinin faturalandırılması.</span><span class="sxs-lookup"><span data-stu-id="680a9-155">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="680a9-156">Ücret için orijinal fatura satırında faturalanan miktar ve tutarı için faturalandırılmış satış tersi.</span><span class="sxs-lookup"><span data-stu-id="680a9-156">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="680a9-157">Doğrulanan fatura satırı ayrıntısı üzerindeki miktar ve tutar için ücretlendirilebilen yeni bir faturalanmamış satış fiili, satışların fiilinin tersine çevrilmesi ve eşdeğer faturalı satışların fiili.</span><span class="sxs-lookup"><span data-stu-id="680a9-157">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="680a9-158">Daha önce faturalandırılmış bir dönüm noktasının tam kredisinin faturalandırılması.</span><span class="sxs-lookup"><span data-stu-id="680a9-158">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="680a9-159">Dönüm noktası için orijinal fatura satırı ayrıntısındaki tutarı için faturalandırılmış satış tersi.</span><span class="sxs-lookup"><span data-stu-id="680a9-159">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="680a9-160">Kilometre taşındaki fatura durumu, <b>Deftere nakledilen müşteri faturası</b> durumundan <b>Faturalanmaya Hazır</b> durumuna güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="680a9-160">The invoice status on the milestone is updated from <b>Customer invoice posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="680a9-161">Daha önce faturalandırılmış bir dönüm noktasının kısmi kredisinin faturalandırılması.</span><span class="sxs-lookup"><span data-stu-id="680a9-161">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="680a9-162">Desteklenmiyor</span><span class="sxs-lookup"><span data-stu-id="680a9-162">Unsupported</span></span> </p>
            </td>
        </tr>        
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
