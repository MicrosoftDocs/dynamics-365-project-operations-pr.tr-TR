---
title: Proforma faturaları onaylama - lite
description: Bu konuda, Project Operations'ta proforma faturaların onaylanması hakkında bilgiler sağlanmaktadır.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 02b671e4ad327b2448529d7119211613f3a9cb27
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176545"
---
# <a name="confirm-a-proforma-invoice---lite"></a><span data-ttu-id="35864-103">Proforma faturaları onaylama - lite</span><span class="sxs-lookup"><span data-stu-id="35864-103">Confirm a proforma invoice - lite</span></span>

<span data-ttu-id="35864-104">_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_</span><span class="sxs-lookup"><span data-stu-id="35864-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="35864-105">Proforma fatura onaylandıktan sonra, proje faturasının durumu **Onaylandı** güncellenir.</span><span class="sxs-lookup"><span data-stu-id="35864-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="35864-106">Bir fatura onaylandığında, salt okunur olur.</span><span class="sxs-lookup"><span data-stu-id="35864-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="35864-107">İleriye dönük olarak, fatura yalnızca müşteri tarafından başlatılan düzeltmeler veya krediler varsa veya ödeme olarak işaretlendiğinde düzeltilebilir.</span><span class="sxs-lookup"><span data-stu-id="35864-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, of if the invoice is marked as paid.</span></span>

<span data-ttu-id="35864-108">Aşağıdaki tabloda sistem tarafından oluşturulan fiili listeler.</span><span class="sxs-lookup"><span data-stu-id="35864-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="35864-109">Bu fiili işlemler, onaylanmadan önce taslak proje faturasında belirli işlemler gerçekleştirildiğinde oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="35864-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="35864-110">
                    <strong>Senaryo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="35864-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="35864-111">
                    <strong>Onayda oluşturulan fiililer</strong>
                </span><span class="sxs-lookup"><span data-stu-id="35864-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="35864-112">Elde tutulan tutar veya avans faturalama</span><span class="sxs-lookup"><span data-stu-id="35864-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="35864-113">Faturalı satış fiili türü, <strong>Elde kalan</strong> avans veya elde kalan üzerindeki tutar için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="35864-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="35864-114">Mutabakat için kullanılacak olan hizmetli veya avansın negatif tutarının faturalandırılmamış satışları.</span><span class="sxs-lookup"><span data-stu-id="35864-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="35864-115">Bir faturada bir elde kalanı veya avansı tamamen uzlaştırdıktan sonra.</span><span class="sxs-lookup"><span data-stu-id="35864-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="35864-116">Mutabakat için oluşturulan hizmetli nin veya avansın faturasız satış tersi.</span><span class="sxs-lookup"><span data-stu-id="35864-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="35864-117">Bu tutar, hizmetli veya avans faturalandığında oluşturulan negatifi iptal etmek amacıyla olduğundan pozitiftir.</span><span class="sxs-lookup"><span data-stu-id="35864-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="35864-118">Bu faturadaki tutar için faturalı satış fiili.</span><span class="sxs-lookup"><span data-stu-id="35864-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="35864-119">Bir faturada bir elde kalanı veya avansı kısmen uzlaştırdıktan sonra.</span><span class="sxs-lookup"><span data-stu-id="35864-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="35864-120">Mutabakat için oluşturulan hizmetli nin veya avansın faturasız satış tersi.</span><span class="sxs-lookup"><span data-stu-id="35864-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="35864-121">Bu tutar, hizmetli veya avans faturalandığında oluşturulan negatifi iptal etmek amacıyla olduğundan pozitiftir.</span><span class="sxs-lookup"><span data-stu-id="35864-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="35864-122">Bu faturadaki tutar için faturalı satış fiili.</span><span class="sxs-lookup"><span data-stu-id="35864-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="35864-123">Gelecek faturalarda mutabakat için kullanılacak olan hizmetli veya avansın negatif tutarının faturalandırılmamış satışları.</span><span class="sxs-lookup"><span data-stu-id="35864-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="35864-124">Taslak faturada herhangi bir işlem yapılmadan bir zaman hareketi faturalandırma.</span><span class="sxs-lookup"><span data-stu-id="35864-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="35864-125">Orijinal saat onayının saat ve tutarı için faturalandırılmamış satış tersi.</span><span class="sxs-lookup"><span data-stu-id="35864-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="35864-126">Orijinal saat onayının saat ve tutarı için faturalandırılmış satış fiili.</span><span class="sxs-lookup"><span data-stu-id="35864-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="35864-127">Miktarı azaltmak için düzenlenen bir zaman hareketinin faturalandırması.</span><span class="sxs-lookup"><span data-stu-id="35864-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="35864-128">Orijinal saat onayının saat ve tutarı için faturalandırılmamış satış tersi.</span><span class="sxs-lookup"><span data-stu-id="35864-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="35864-129">Düzenlenen fatura satırı ayrıntısı üzerindeki saat ve tutar için ücretlendirilebilen yeni bir faturalanmamış satış fiili, satışların fiilinin tersine çevrilmesi ve eşdeğer faturalı satışların fiili.</span><span class="sxs-lookup"><span data-stu-id="35864-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="35864-130">Düzenlenen fatura satırı ayrıntısı üzerindeki doğrulanan rakamlar çıkarıldıktan sonra kalan saat ve tutar için ücretlendirilemeyen yeni bir faturalanmamış satış fiili, satışların fiilinin tersine çevrilmesi ve eşdeğer faturalı satışların fiili.</span><span class="sxs-lookup"><span data-stu-id="35864-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="35864-131">Miktarı artırmak için düzenlenen bir zaman hareketinin faturalandırması.</span><span class="sxs-lookup"><span data-stu-id="35864-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="35864-132">Orijinal saat onayının saat ve tutarı için faturalandırılmamış satış tersi.</span><span class="sxs-lookup"><span data-stu-id="35864-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="35864-133">Düzenlenen fatura satırı ayrıntısı üzerindeki saat ve tutar için ücretlendirilebilen yeni bir faturalanmamış satış fiili, faturalandırılmamış satışların fiilinin tersine çevrilmesi ve eşdeğer faturalı satışların fiili.</span><span class="sxs-lookup"><span data-stu-id="35864-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="35864-134">Taslak faturada herhangi bir işlem yapılmadan bir gider hareketi faturalandırma.</span><span class="sxs-lookup"><span data-stu-id="35864-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="35864-135">Orijinal gider onayının miktarı ve tutarı için faturalandırılmamış satış tersi.</span><span class="sxs-lookup"><span data-stu-id="35864-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="35864-136">Orijinal gider onayının miktarı ve tutarı için faturalandırılmış satış fiili</span><span class="sxs-lookup"><span data-stu-id="35864-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="35864-137">Miktarı azaltmak için düzenlenen bir gider hareketinin faturalandırması.</span><span class="sxs-lookup"><span data-stu-id="35864-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="35864-138">Orijinal gider onayının miktarı ve tutarı için faturalandırılmamış satış tersi.</span><span class="sxs-lookup"><span data-stu-id="35864-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="35864-139">Düzenlenen fatura satırı ayrıntısı üzerindeki miktar ve tutar için ücretlendirilebilen yeni bir faturalanmamış satış fiili, faturalandırılmamış satışların fiilinin tersine çevrilmesi ve eşdeğer faturalı satışların fiili.</span><span class="sxs-lookup"><span data-stu-id="35864-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="35864-140">Düzenlenen fatura satırı ayrıntısı üzerindeki doğrulanan rakamlar çıkarıldıktan sonra kalan miktar ve tutar için ücretlendirilemeyen yeni bir faturalanmamış satış fiili, faturalandırılmamış satışların fiilinin tersine çevrilmesi ve eşdeğer faturalı satışların fiili.</span><span class="sxs-lookup"><span data-stu-id="35864-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="35864-141">Miktarı artırmak için düzenlenen bir gider hareketinin faturalandırması.</span><span class="sxs-lookup"><span data-stu-id="35864-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="35864-142">Orijinal gider onayının miktarı ve tutarı için faturalandırılmamış satış tersi.</span><span class="sxs-lookup"><span data-stu-id="35864-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="35864-143">Düzenlenen fatura satırı ayrıntısı üzerindeki miktar ve tutar için ücretlendirilebilen yeni bir faturalanmamış satış fiili, faturalandırılmamış satışların fiilinin tersine çevrilmesi ve eşdeğer faturalı satışların fiili.</span><span class="sxs-lookup"><span data-stu-id="35864-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="35864-144">Bir ücret faturalama.</span><span class="sxs-lookup"><span data-stu-id="35864-144">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="35864-145">Orijinal yevmiye defteri satırında ücret tutarı için faturalandırılmamış satış tersi.</span><span class="sxs-lookup"><span data-stu-id="35864-145">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="35864-146">Orijinal ücret yevmiye defteri satırı miktarı ve tutarı için faturalandırılmış satış fiili.</span><span class="sxs-lookup"><span data-stu-id="35864-146">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="35864-147">Bir kilometre taşını faturalama.</span><span class="sxs-lookup"><span data-stu-id="35864-147">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="35864-148">Proje sözleşmesi satırındaki özgün kilometre taşındaki kilometre taşı tutarı için faturalı satış fiili.</span><span class="sxs-lookup"><span data-stu-id="35864-148">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="35864-149">Ürün tabanlı sözleşme satırını faturalandırma.</span><span class="sxs-lookup"><span data-stu-id="35864-149">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="35864-150">Faturalanan bir satış, ürün tabanlı sözleşme satırından gelen miktar ve tutar içeren, ürün satırı için fiili olarak yapılır.</span><span class="sxs-lookup"><span data-stu-id="35864-150">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>
