---
title: Düzeltici proje tabanlı faturalar
description: Bu konu, Project Operations'ta düzeltici proje tabanlı fatura oluşturma ve onaylama hakkında bilgi sağlar.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6b6670f823577bf7f784443f97f0b77e1e9a6aa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012295"
---
# <a name="corrective-project-based-invoices"></a><span data-ttu-id="366b4-103">Düzeltici proje tabanlı faturalar</span><span class="sxs-lookup"><span data-stu-id="366b4-103">Corrective project-based invoices</span></span>

<span data-ttu-id="366b4-104">_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="366b4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="366b4-105">Onaylı proje faturaları müşteri ve proje yöneticisiyle görüşülür, değişiklikleri veya kredileri işlemek için düzeltilebilir.</span><span class="sxs-lookup"><span data-stu-id="366b4-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="366b4-106">Onaylı bir faturada düzenlemeler yapmak için, onaylanan faturayı açın ve **Bu faturayı Düzelt**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="366b4-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="366b4-107">Proje faturası onaylanmadıkça veya proje tabanlı faturada avanslar veya elde tutulan tutar ya da avansların veya elde tutulan tutarların mutabakatları yoksa bu seçim kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="366b4-107">This selection isn't available unless a project invoice is confirmed or the project-based invoice has advances or retainers or reconciliations of advances or retainers.</span></span>

<span data-ttu-id="366b4-108">Onaylanan faturadan yeni bir taslak fatura oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="366b4-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="366b4-109">Daha önce onaylanan faturadan tüm fatura satırı ayrıntıları yeni taslağın kopyası alınır.</span><span class="sxs-lookup"><span data-stu-id="366b4-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="366b4-110">Yeni düzeltilen fatura hakkındaki satır ayrıntılarını anlamak için aşağıda yer alan önemli noktaların bazıları aşağıda verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="366b4-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="366b4-111">Tüm miktarlar sıfıra güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="366b4-111">All quantities are updated to zero.</span></span> <span data-ttu-id="366b4-112">Dynamics 365 Project Operations, tüm faturalanan maddelerin tam olarak alacaklandırıldığını varsayar.</span><span class="sxs-lookup"><span data-stu-id="366b4-112">Dynamics 365 Project Operations assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="366b4-113">Gerekirse, bu miktarları, alacaklandırılan miktarı değil, faturalanan miktarı yansıtacak şekilde el ile güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="366b4-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="366b4-114">Girdiğiniz miktara bağlı olarak, uygulama alacaklı miktarı hesaplar.</span><span class="sxs-lookup"><span data-stu-id="366b4-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="366b4-115">Bu miktar, düzeltilen fatura onaylandığı zaman oluşturulan fiili değerlere yansıtılır.</span><span class="sxs-lookup"><span data-stu-id="366b4-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="366b4-116">Vergi tutarında değişiklikler yapıyorsanız, alacak kaydedilen vergi tutarını değil, doğru vergi tutarını girmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="366b4-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="366b4-117">Kilometre taşı düzeltmeleri her zaman tam kredi olarak işlenir.</span><span class="sxs-lookup"><span data-stu-id="366b4-117">Milestone corrections are always processed as full credits.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="366b4-118">Önceden faturalandırılmış diğer giderlere yönelik düzeltmeler olan fatura satırı ayrıntılarının **Düzeltme** alanı, **Evet** olarak ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="366b4-118">For invoice line details that are corrections to other already invoiced charges, the **Correction** field is set to **Yes**.</span></span> <span data-ttu-id="366b4-119">Düzeltilmiş fatura satırı ayrıntıları olan faturaların **Düzeltmeler var** alanı, **Evet** olarak ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="366b4-119">For invoices that have corrected invoice line details, the **Has corrections** field is set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="366b4-120">Bir düzeltici fatura onaylandığında oluşturulan gerçek değerler</span><span class="sxs-lookup"><span data-stu-id="366b4-120">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="366b4-121">Aşağıdaki tabloda, bir düzeltici fatura onaylandıktan sonra oluşturulan gerçek değerler listelenmiştir.</span><span class="sxs-lookup"><span data-stu-id="366b4-121">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="366b4-122">
                    <strong>Senaryo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="366b4-122">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="366b4-123">
                    <strong>Onayda oluşturulan fiililer</strong>
                </span><span class="sxs-lookup"><span data-stu-id="366b4-123">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="366b4-124">Daha önce faturalandırılmış bir zaman hareketinin tam kredisinin faturalandırılması.</span><span class="sxs-lookup"><span data-stu-id="366b4-124">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="366b4-125">Saat için orijinal fatura satırı ayrıntısındaki saat ve tutarı için faturalandırılmış satış tersi.</span><span class="sxs-lookup"><span data-stu-id="366b4-125">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="366b4-126">Saat için orijinal fatura satırı ayrıntısındaki saat ve tutarı için yeni faturalandırılmış satış fiili.</span><span class="sxs-lookup"><span data-stu-id="366b4-126">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="366b4-127">Bir zaman hareketinde kısmi kredi faturalama.</span><span class="sxs-lookup"><span data-stu-id="366b4-127">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="366b4-128">Saat için orijinal fatura satırı ayrıntısındaki saat ve tutarı için faturalandırılmış satış tersi.</span><span class="sxs-lookup"><span data-stu-id="366b4-128">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="366b4-129">Düzenlenen fatura satırı ayrıntısı üzerindeki saat ve tutar için ücretlendirilebilen yeni bir faturalanmamış satış fiili, satışların fiilinin tersine çevrilmesi ve eşdeğer faturalı satışların fiili.</span><span class="sxs-lookup"><span data-stu-id="366b4-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="366b4-130">Fatura satırı ayrıntısıyla düzeltilen rakamların düşüldükten sonra kalan saatler ve tutar için masraflandırılabilen yeni faturalandırılamayan satış fiili gerçek değeri.</span><span class="sxs-lookup"><span data-stu-id="366b4-130">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="366b4-131">Daha önce faturalandırılmış bir gider hareketinin tam kredisinin faturalandırılması.</span><span class="sxs-lookup"><span data-stu-id="366b4-131">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="366b4-132">Gider için orijinal fatura satırı ayrıntısındaki miktar ve tutarı için faturalandırılmış satış tersi.</span><span class="sxs-lookup"><span data-stu-id="366b4-132">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="366b4-133">Gider için orijinal fatura satırı ayrıntısındaki miktar ve tutarı için yeni faturalandırılmamış satış fiili.</span><span class="sxs-lookup"><span data-stu-id="366b4-133">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="366b4-134">Daha önce faturalandırılmış bir gider hareketinin kısmi kredisinin faturalandırılması.</span><span class="sxs-lookup"><span data-stu-id="366b4-134">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="366b4-135">Gider için orijinal fatura satırı ayrıntısında faturalandırılan miktar ve tutarı için faturalandırılmış satış tersi.</span><span class="sxs-lookup"><span data-stu-id="366b4-135">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="366b4-136">Doğrulanan fatura satırı ayrıntısı üzerindeki miktar ve tutar için ücretlendirilebilen yeni bir faturalanmamış satış fiili, satışların fiilinin tersine çevrilmesi ve eşdeğer faturalı satışların fiili.</span><span class="sxs-lookup"><span data-stu-id="366b4-136">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="366b4-137">Fatura satırı ayrıntısıyla düzeltilen rakamların düşüldükten sonra kalan miktar ve tutar için masraflandırılabilen yeni faturalandırılamayan satış fiili gerçek değeri.</span><span class="sxs-lookup"><span data-stu-id="366b4-137">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="366b4-138">Daha önce faturalanmış bir malzeme hareketinin tam kredisinin faturalanması.</span><span class="sxs-lookup"><span data-stu-id="366b4-138">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="366b4-139">Malzemenin orijinal fatura satırı ayrıntılarındaki miktar ve tutar için faturalanmış satışı tersine çevirme işlemi.</span><span class="sxs-lookup"><span data-stu-id="366b4-139">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="366b4-140">Malzemenin orijinal fatura satırı ayrıntılarındaki miktar ve tutar için yeni faturalanmamış satış gerçek değeri.</span><span class="sxs-lookup"><span data-stu-id="366b4-140">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="366b4-141">Malzeme hareketindeki kısmi kredinin faturalanması.</span><span class="sxs-lookup"><span data-stu-id="366b4-141">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="366b4-142">Malzemenin orijinal fatura satırı ayrıntılarındaki miktar ve faturalanan tutar için faturalanmış satışı tersine çevirme işlemi.</span><span class="sxs-lookup"><span data-stu-id="366b4-142">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="366b4-143">Düzenlenen fatura satırı ayrıntısındaki miktar ve tutar için borçlandırılabilen yeni faturalanmayan satış gerçek değeri, bunun tersine çevrilmesi ve eşdeğer faturalanan satış gerçek değeri.</span><span class="sxs-lookup"><span data-stu-id="366b4-143">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="366b4-144">Fatura satırı ayrıntısıyla düzeltilen rakamların düşüldükten sonra kalan miktar ve tutar için masraflandırılabilen yeni faturalandırılamayan satış fiili gerçek değeri.</span><span class="sxs-lookup"><span data-stu-id="366b4-144">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="366b4-145">Daha önce faturalandırılmış bir ücret hareketinin tam kredisinin faturalandırılması.</span><span class="sxs-lookup"><span data-stu-id="366b4-145">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="366b4-146">Ücret için orijinal fatura satırı ayrıntısındaki miktar ve tutarı için faturalandırılmış satış tersi.</span><span class="sxs-lookup"><span data-stu-id="366b4-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="366b4-147">Ücret için orijinal fatura satırı ayrıntısındaki miktar ve tutarı için yeni faturalandırılmamış satış fiili.</span><span class="sxs-lookup"><span data-stu-id="366b4-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="366b4-148">Daha önce faturalandırılmış bir ücret hareketinin kısmi kredisinin faturalandırılması.</span><span class="sxs-lookup"><span data-stu-id="366b4-148">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="366b4-149">Ücret için orijinal fatura satırında faturalanan miktar ve tutarı için faturalandırılmış satış tersi.</span><span class="sxs-lookup"><span data-stu-id="366b4-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="366b4-150">Doğrulanan fatura satırı ayrıntısı üzerindeki miktar ve tutar için ücretlendirilebilen yeni bir faturalanmamış satış fiili, satışların fiilinin tersine çevrilmesi ve eşdeğer faturalı satışların fiili.</span><span class="sxs-lookup"><span data-stu-id="366b4-150">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="366b4-151">Daha önce faturalandırılmış bir dönüm noktasının tam kredisinin faturalandırılması.</span><span class="sxs-lookup"><span data-stu-id="366b4-151">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="366b4-152">Dönüm noktası için orijinal fatura satırı ayrıntısındaki tutarı için faturalandırılmış satış tersi.</span><span class="sxs-lookup"><span data-stu-id="366b4-152">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="366b4-153">Kilometre taşının fatura durumu, <b>Deftere Nakledilen Müşteri Faturası</b> durumundan <b>Faturalanmaya Hazır</b> durumuna güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="366b4-153">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="366b4-154">Daha önce faturalandırılmış bir dönüm noktasının kısmi kredisinin faturalandırılması.</span><span class="sxs-lookup"><span data-stu-id="366b4-154">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="366b4-155">Bu senaryo desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="366b4-155">This scenario isn't supported.</span></span>
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
