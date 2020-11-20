---
title: Düzeltilen faturalar - lite
description: Bu konuda, Project Operations'ta doğrulanan faturalar hakkında bilgiler sağlanmaktadır.
author: rumant
manager: Annbe
ms.date: 10/15/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 55bec8ad1d9c2b55cabb453321f13df8b7cd1614
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176455"
---
# <a name="corrected-invoices---lite"></a><span data-ttu-id="d3cdf-103">Düzeltilen faturalar - lite</span><span class="sxs-lookup"><span data-stu-id="d3cdf-103">Corrected invoices - lite</span></span>

<span data-ttu-id="d3cdf-104">_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_</span><span class="sxs-lookup"><span data-stu-id="d3cdf-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d3cdf-105">Onaylı proje faturaları müşteri ve proje yöneticisiyle görüşülür, değişiklikleri veya kredileri işlemek için düzeltilebilir.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="d3cdf-106">Onaylı bir faturada düzenlemeler yapmak için, onaylanan faturayı açın ve **Bu faturayı Düzelt**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="d3cdf-107">Bir proje faturası onaylanmadıkça bu seçim kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="d3cdf-108">Onaylanan faturadan yeni bir taslak fatura oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="d3cdf-109">Daha önce onaylanan faturadan tüm fatura satırı ayrıntıları yeni taslağın kopyası alınır.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="d3cdf-110">Yeni düzeltilen fatura hakkındaki satır ayrıntılarını anlamak için aşağıda yer alan önemli noktaların bazıları aşağıda verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="d3cdf-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="d3cdf-111">Tüm miktarlar sıfıra güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-111">All quantities are updated to zero.</span></span> <span data-ttu-id="d3cdf-112">Uygulama tüm faturalanan maddelerin tam olarak alacaklandırıldığını kabul eder.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-112">The application assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="d3cdf-113">Gerekirse, bu miktarları, alacaklandırılan miktarı değil, faturalanan miktarı yansıtacak şekilde el ile güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="d3cdf-114">Girdiğiniz miktara bağlı olarak, uygulama alacaklı miktarı hesaplar.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="d3cdf-115">Bu miktar, düzeltilen fatura onaylandığı zaman oluşturulan fiili değerlere yansıtılır.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="d3cdf-116">Vergi tutarında değişiklikler yapıyorsanız, alacak kaydedilen vergi tutarını değil, doğru vergi tutarını girmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="d3cdf-117">Önceden onaylanmış ürün tabanlı sözleşme satırları üzerine kopyalanmaz.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-117">Previously confirmed product-based contract lines are not copied over.</span></span> <span data-ttu-id="d3cdf-118">Ürün tabanlı bir proje faturasındaki düzeltmelerin işlenmesi desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-118">Processing corrections on a product-based project invoice is not supported.</span></span>
- <span data-ttu-id="d3cdf-119">Kilometre taşı düzeltmeleri her zaman tam kredi olarak işlenir.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-119">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="d3cdf-120">Müşteri hatalı bir tutar için faturalandıysa, Retainer veya avans tutarları düzeltilebilir.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-120">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="d3cdf-121">Önceden onaylanmış bir faturadaki giderlere göre mutabakat sağlamak için yanlış bir tutar kullanılmışsa, retainers ve avanslar mutabakatları düzeltilebilir.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-121">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d3cdf-122">Önceden faturalandırılmış diğer giderlere yönelik düzeltmeler olan fatura satırı ayrıntıları, alan **düzeltmesi** **Evet** olarak ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-122">Invoice line details that are corrections to other already invoiced charges have the field **Correction** set to **Yes**.</span></span> <span data-ttu-id="d3cdf-123">Düzeltilen fatura satırı ayrıntıları olan faturalarda **Evet** olarak ayarlanmış **düzeltmeler vardır** adlı alanı bulunur.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-123">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="d3cdf-124">Düzeltme faturasının onaylanması sırasında oluşturulan gerçek değerler:</span><span class="sxs-lookup"><span data-stu-id="d3cdf-124">Actuals created on Confirmation of a corrective invoice:</span></span>

<span data-ttu-id="d3cdf-125">Aşağıda, onay öncesinde taslak düzeltme faturasında gerçekleştirilen operasyonlara dayalı olarak düzeltme onaylamada uygulama tarafından oluşturulan fiili değerler yer alır.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-125">Below are the actuals created by the application on confirmation of a corrective based on the operations performed on the draft corrective invoice before confirmation.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="d3cdf-126">
                    <strong>Senaryo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d3cdf-126">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="d3cdf-127">
                    <strong>Onayda oluşturulan fiililer</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d3cdf-127">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="d3cdf-128">Faturalandırılmış bir avans veya Retainer düzeltmesini onaylayın.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="d3cdf-128">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3cdf-129">Mutabakat için oluşturulan hizmetli nin veya avansın faturasız satış tersi.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-129">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="d3cdf-130">Bu tutar, hizmetli veya avans faturalandığında oluşturulan negatifi iptal etmek amacıyla olduğundan pozitiftir.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-130">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3cdf-131">Bir faturalanmış satış ters çevirme fiili, Retainer üzerindeki tutar için oluşturulur veya orijinal Faturalanan Satışlar tersine çevrilmesine karşı ilerletir.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-131">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3cdf-132">Yeni faturalı satış fiili türü, Elde kalan avans veya elde kalan üzerindeki tutar için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-132">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3cdf-133">Mutabakat için kullanılacak olan hizmetli veya avansa dayalı düzeltilmiş fatura satırının negatif tutarının faturalandırılmamış satışları.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-133">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="d3cdf-134">Daha önce mutabakat sağlanmış bir elde kalan veya avans düzeltmesi onayı.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-134">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3cdf-135">Mutabakat için oluşturulan hizmetli nin veya avansın faturasız satış tersi.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-135">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="d3cdf-136">Bu tutar, önceki mutabakat meydana geldiğinde oluşturulan negatifi iptal etmek amacıyla olduğundan pozitiftir.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-136">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3cdf-137">Önceki faturadaki tutar için faturalı satış ters fiili.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-137">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3cdf-138">Yeni faturalı satış fiili türü, doğrulanan faturaya uyguanan elde kalan doğrulanan tutar içindir.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-138">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3cdf-139">Sonraki faturalarda mutabakat için kullanılacak olan hizmetli veya avansa dayalı düzeltilmiş fatura satırının negatif tutarının faturalandırılmamış satışları.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-139">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d3cdf-140">Daha önce faturalandırılmış bir zaman hareketinin tam kredisinin faturalandırılması.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-140">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3cdf-141">Saat için orijinal fatura satırı ayrıntısındaki saat ve tutarı için faturalandırılmış satış tersi.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-141">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3cdf-142">Saat için orijinal fatura satırı ayrıntısındaki saat ve tutarı için yeni faturalandırılmış satış fiili.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-142">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="d3cdf-143">Bir zaman hareketinde kısmi kredi faturalama.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-143">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3cdf-144">Saat için orijinal fatura satırı ayrıntısındaki saat ve tutarı için faturalandırılmış satış tersi.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-144">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3cdf-145">Düzenlenen fatura satırı ayrıntısı üzerindeki saat ve tutar için ücretlendirilebilen yeni bir faturalanmamış satış fiili, satışların fiilinin tersine çevrilmesi ve eşdeğer faturalı satışların fiili.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-145">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3cdf-146">Fatura satırı ayrıntısıyla düzeltilen rakamların düşüldükten sonra kalan saatler ve tutar için masraflandırılabilen yeni faturalandırılamayan satış fiili gerçek değeri.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-146">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d3cdf-147">Daha önce faturalandırılmış bir gider hareketinin tam kredisinin faturalandırılması.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-147">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3cdf-148">Gider için orijinal fatura satırı ayrıntısındaki miktar ve tutarı için faturalandırılmış satış tersi.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-148">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3cdf-149">Gider için orijinal fatura satırı ayrıntısındaki miktar ve tutarı için yeni faturalandırılmamış satış fiili.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-149">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="d3cdf-150">Daha önce faturalandırılmış bir gider hareketinin kısmi kredisinin faturalandırılması.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-150">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3cdf-151">Gider için orijinal fatura satırı ayrıntısında faturalandırılan miktar ve tutarı için faturalandırılmış satış tersi.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-151">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3cdf-152">Doğrulanan fatura satırı ayrıntısı üzerindeki miktar ve tutar için ücretlendirilebilen yeni bir faturalanmamış satış fiili, satışların fiilinin tersine çevrilmesi ve eşdeğer faturalı satışların fiili.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-152">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3cdf-153">Fatura satırı ayrıntısıyla düzeltilen rakamların düşüldükten sonra kalan miktar ve tutar için masraflandırılabilen yeni faturalandırılamayan satış fiili gerçek değeri.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-153">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d3cdf-154">Daha önce faturalandırılmış bir ücret hareketinin tam kredisinin faturalandırılması.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-154">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3cdf-155">Ücret için orijinal fatura satırı ayrıntısındaki miktar ve tutarı için faturalandırılmış satış tersi.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-155">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3cdf-156">Ücret için orijinal fatura satırı ayrıntısındaki miktar ve tutarı için yeni faturalandırılmamış satış fiili.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-156">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d3cdf-157">Daha önce faturalandırılmış bir ücret hareketinin kısmi kredisinin faturalandırılması.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-157">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3cdf-158">Ücret için orijinal fatura satırında faturalanan miktar ve tutarı için faturalandırılmış satış tersi.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-158">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3cdf-159">Doğrulanan fatura satırı ayrıntısı üzerindeki miktar ve tutar için ücretlendirilebilen yeni bir faturalanmamış satış fiili, satışların fiilinin tersine çevrilmesi ve eşdeğer faturalı satışların fiili.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-159">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="d3cdf-160">Daha önce faturalandırılmış bir dönüm noktasının tam kredisinin faturalandırılması.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-160">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3cdf-161">Dönüm noktası için orijinal fatura satırı ayrıntısındaki tutarı için faturalandırılmış satış tersi.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-161">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="d3cdf-162">Proje sözleşmesi satırındaki kilometre taşı faturası veya fatura durumu **faturaya hazır** olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-162">The milestone invoice or billing status on the project contract line is updated to **Ready to Invoice**.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="d3cdf-163">Daha önce faturalandırılmış bir dönüm noktasının kısmi kredisinin faturalandırılması.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-163">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3cdf-164">Desteklenmiyor</span><span class="sxs-lookup"><span data-stu-id="d3cdf-164">Unsupported</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="d3cdf-165">Daha önce faturalandırılmış ürün tabanlı bir sözleşme satırındaki jenerik ve düzeltmeler.</span><span class="sxs-lookup"><span data-stu-id="d3cdf-165">Credits and corrections of a previously invoiced product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3cdf-166">Desteklenmiyor</span><span class="sxs-lookup"><span data-stu-id="d3cdf-166">Unsupported</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>
