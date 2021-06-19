---
title: Proforma proje faturalarını onaylama
description: Bu konu, Project Operations'ta proforma proje faturalarının onaylanmasının hakkında bilgi sağlar.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0ab40e38f221e57368949b7491578caa8ba88c02
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004150"
---
# <a name="confirm-a-proforma-project-invoice"></a><span data-ttu-id="81918-103">Proforma proje faturalarını onaylama</span><span class="sxs-lookup"><span data-stu-id="81918-103">Confirm a proforma project invoice</span></span> 

<span data-ttu-id="81918-104">_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_</span><span class="sxs-lookup"><span data-stu-id="81918-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="81918-105">Proforma fatura onaylandıktan sonra, proje faturasının durumu **Onaylandı** güncellenir.</span><span class="sxs-lookup"><span data-stu-id="81918-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="81918-106">Bir fatura onaylandığında, salt okunur olur.</span><span class="sxs-lookup"><span data-stu-id="81918-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="81918-107">Devam ederseniz fatura yalnızca müşteri tarafından başlatılan düzeltmeler veya kredi varsa düzeltilebilir.</span><span class="sxs-lookup"><span data-stu-id="81918-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits.</span></span>

<span data-ttu-id="81918-108">Aşağıdaki tabloda sistem tarafından oluşturulan fiili listeler.</span><span class="sxs-lookup"><span data-stu-id="81918-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="81918-109">Bu fiili işlemler, onaylanmadan önce taslak proje faturasında belirli işlemler gerçekleştirildiğinde oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="81918-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="81918-110">
                    <strong>Senaryo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="81918-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="81918-111">
                    <strong>Onayda oluşturulan fiililer</strong>
                </span><span class="sxs-lookup"><span data-stu-id="81918-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="81918-112">Elde tutulan tutar veya avans faturalama</span><span class="sxs-lookup"><span data-stu-id="81918-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="81918-113">Faturalı satış fiili türü, <strong>Elde kalan</strong> avans veya elde kalan üzerindeki tutar için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="81918-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="81918-114">Mutabakat için kullanılacak olan hizmetli veya avansın negatif tutarının faturalandırılmamış satışları.</span><span class="sxs-lookup"><span data-stu-id="81918-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="81918-115">Bir faturada bir elde kalanı veya avansı tamamen uzlaştırdıktan sonra.</span><span class="sxs-lookup"><span data-stu-id="81918-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="81918-116">Mutabakat için oluşturulan hizmetli nin veya avansın faturasız satış tersi.</span><span class="sxs-lookup"><span data-stu-id="81918-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="81918-117">Bu tutar, hizmetli veya avans faturalandığında oluşturulan negatifi iptal etmek amacıyla olduğundan pozitiftir.</span><span class="sxs-lookup"><span data-stu-id="81918-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="81918-118">Bu faturadaki tutar için faturalı satış fiili.</span><span class="sxs-lookup"><span data-stu-id="81918-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="81918-119">Bir faturada bir elde kalanı veya avansı kısmen uzlaştırdıktan sonra.</span><span class="sxs-lookup"><span data-stu-id="81918-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="81918-120">Mutabakat için oluşturulan hizmetli nin veya avansın faturasız satış tersi.</span><span class="sxs-lookup"><span data-stu-id="81918-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="81918-121">Bu tutar, hizmetli veya avans faturalandığında oluşturulan negatifi iptal etmek amacıyla olduğundan pozitiftir.</span><span class="sxs-lookup"><span data-stu-id="81918-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="81918-122">Bu faturadaki tutar için faturalı satış fiili.</span><span class="sxs-lookup"><span data-stu-id="81918-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="81918-123">Gelecek faturalarda mutabakat için kullanılacak olan hizmetli veya avansın negatif tutarının faturalandırılmamış satışları.</span><span class="sxs-lookup"><span data-stu-id="81918-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="81918-124">Taslak faturada herhangi bir işlem yapılmadan bir zaman hareketi faturalandırma.</span><span class="sxs-lookup"><span data-stu-id="81918-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="81918-125">Orijinal saat onayının saat ve tutarı için faturalandırılmamış satış tersi.</span><span class="sxs-lookup"><span data-stu-id="81918-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="81918-126">Orijinal saat onayının saat ve tutarı için faturalandırılmış satış fiili.</span><span class="sxs-lookup"><span data-stu-id="81918-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="81918-127">Miktarı azaltmak için düzenlenen bir zaman hareketinin faturalandırması.</span><span class="sxs-lookup"><span data-stu-id="81918-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="81918-128">Orijinal saat onayının saat ve tutarı için faturalandırılmamış satış tersi.</span><span class="sxs-lookup"><span data-stu-id="81918-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="81918-129">Düzenlenen fatura satırı ayrıntısı üzerindeki saat ve tutar için ücretlendirilebilen yeni bir faturalanmamış satış fiili, satışların fiilinin tersine çevrilmesi ve eşdeğer faturalı satışların fiili.</span><span class="sxs-lookup"><span data-stu-id="81918-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="81918-130">Düzenlenen fatura satırı ayrıntısı üzerindeki doğrulanan rakamlar çıkarıldıktan sonra kalan saat ve tutar için ücretlendirilemeyen yeni bir faturalanmamış satış fiili, satışların fiilinin tersine çevrilmesi ve eşdeğer faturalı satışların fiili.</span><span class="sxs-lookup"><span data-stu-id="81918-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="81918-131">Miktarı artırmak için düzenlenen bir zaman hareketinin faturalandırması.</span><span class="sxs-lookup"><span data-stu-id="81918-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="81918-132">Orijinal saat onayının saat ve tutarı için faturalandırılmamış satış tersi.</span><span class="sxs-lookup"><span data-stu-id="81918-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="81918-133">Düzenlenen fatura satırı ayrıntısı üzerindeki saat ve tutar için ücretlendirilebilen yeni bir faturalanmamış satış fiili, faturalandırılmamış satışların fiilinin tersine çevrilmesi ve eşdeğer faturalı satışların fiili.</span><span class="sxs-lookup"><span data-stu-id="81918-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="81918-134">Taslak faturada herhangi bir işlem yapılmadan bir gider hareketi faturalandırma.</span><span class="sxs-lookup"><span data-stu-id="81918-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="81918-135">Orijinal gider onayının miktarı ve tutarı için faturalandırılmamış satış tersi.</span><span class="sxs-lookup"><span data-stu-id="81918-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="81918-136">Orijinal gider onayının miktarı ve tutarı için faturalandırılmış satış fiili</span><span class="sxs-lookup"><span data-stu-id="81918-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="81918-137">Miktarı azaltmak için düzenlenen bir gider hareketinin faturalandırması.</span><span class="sxs-lookup"><span data-stu-id="81918-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="81918-138">Orijinal gider onayının miktarı ve tutarı için faturalandırılmamış satış tersi.</span><span class="sxs-lookup"><span data-stu-id="81918-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="81918-139">Düzenlenen fatura satırı ayrıntısı üzerindeki miktar ve tutar için ücretlendirilebilen yeni bir faturalanmamış satış fiili, faturalandırılmamış satışların fiilinin tersine çevrilmesi ve eşdeğer faturalı satışların fiili.</span><span class="sxs-lookup"><span data-stu-id="81918-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="81918-140">Düzenlenen fatura satırı ayrıntısı üzerindeki doğrulanan rakamlar çıkarıldıktan sonra kalan miktar ve tutar için ücretlendirilemeyen yeni bir faturalanmamış satış fiili, faturalandırılmamış satışların fiilinin tersine çevrilmesi ve eşdeğer faturalı satışların fiili.</span><span class="sxs-lookup"><span data-stu-id="81918-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="81918-141">Miktarı artırmak için düzenlenen bir gider hareketinin faturalandırması.</span><span class="sxs-lookup"><span data-stu-id="81918-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="81918-142">Orijinal gider onayının miktarı ve tutarı için faturalandırılmamış satış tersi.</span><span class="sxs-lookup"><span data-stu-id="81918-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="81918-143">Düzenlenen fatura satırı ayrıntısı üzerindeki miktar ve tutar için ücretlendirilebilen yeni bir faturalanmamış satış fiili, faturalandırılmamış satışların fiilinin tersine çevrilmesi ve eşdeğer faturalı satışların fiili.</span><span class="sxs-lookup"><span data-stu-id="81918-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="81918-144">Taslak faturasında herhangi bir düzenleme yapmadan bir malzeme hareketini faturalama.</span><span class="sxs-lookup"><span data-stu-id="81918-144">Invoicing a material transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="81918-145">Orijinal malzeme kullanımı onayındaki miktar ve tutar için faturalanmamış satışı tersine çevirme işlemi.</span><span class="sxs-lookup"><span data-stu-id="81918-145">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="81918-146">Orijinal malzeme kullanımı onayındaki miktar ve tutar için faturalanmış satış gerçek değeri.</span><span class="sxs-lookup"><span data-stu-id="81918-146">A billed sales actual for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="81918-147">Miktarı azaltmak için düzenlenen bir malzeme hareketini faturalama.</span><span class="sxs-lookup"><span data-stu-id="81918-147">Invoicing a material transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="81918-148">Orijinal zaman onayındaki miktar ve tutar için faturalanmamış satışı tersine çevirme işlemi.</span><span class="sxs-lookup"><span data-stu-id="81918-148">An unbilled sales reversal for the quantity and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="81918-149">Düzenlenen fatura satırı ayrıntısı üzerindeki miktar ve tutar için ücretlendirilebilen yeni bir faturalanmamış satış fiili, faturalandırılmamış satışların fiilinin tersine çevrilmesi ve eşdeğer faturalı satışların fiili.</span><span class="sxs-lookup"><span data-stu-id="81918-149">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="81918-150">Düzenlenen fatura satırı ayrıntısı üzerindeki doğrulanan rakamlar çıkarıldıktan sonra kalan miktar ve tutar için ücretlendirilemeyen yeni bir faturalanmamış satış fiili, faturalandırılmamış satışların fiilinin tersine çevrilmesi ve eşdeğer faturalı satışların fiili.</span><span class="sxs-lookup"><span data-stu-id="81918-150">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="81918-151">Miktarı artırmak için düzenlenen bir malzeme hareketini faturalama.</span><span class="sxs-lookup"><span data-stu-id="81918-151">Invoicing a material transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="81918-152">Orijinal malzeme kullanımı onayındaki miktar ve tutar için faturalanmamış satışı tersine çevirme işlemi.</span><span class="sxs-lookup"><span data-stu-id="81918-152">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="81918-153">Düzenlenen fatura satırı ayrıntısı üzerindeki miktar ve tutar için ücretlendirilebilen yeni bir faturalanmamış satış fiili, faturalandırılmamış satışların fiilinin tersine çevrilmesi ve eşdeğer faturalı satışların fiili.</span><span class="sxs-lookup"><span data-stu-id="81918-153">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="81918-154">Bir ücret faturalama.</span><span class="sxs-lookup"><span data-stu-id="81918-154">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="81918-155">Orijinal yevmiye defteri satırında ücret tutarı için faturalandırılmamış satış tersi.</span><span class="sxs-lookup"><span data-stu-id="81918-155">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="81918-156">Orijinal ücret yevmiye defteri satırı miktarı ve tutarı için faturalandırılmış satış fiili.</span><span class="sxs-lookup"><span data-stu-id="81918-156">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="81918-157">Bir kilometre taşını faturalama.</span><span class="sxs-lookup"><span data-stu-id="81918-157">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="81918-158">Proje sözleşmesi satırındaki özgün kilometre taşındaki kilometre taşı tutarı için faturalı satış fiili.</span><span class="sxs-lookup"><span data-stu-id="81918-158">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="81918-159">Ürün tabanlı sözleşme satırını faturalandırma.</span><span class="sxs-lookup"><span data-stu-id="81918-159">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="81918-160">Faturalanan bir satış, ürün tabanlı sözleşme satırından gelen miktar ve tutar içeren, ürün satırı için fiili olarak yapılır.</span><span class="sxs-lookup"><span data-stu-id="81918-160">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
