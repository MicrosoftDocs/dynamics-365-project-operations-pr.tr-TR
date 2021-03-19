---
title: Proforma faturaları onaylama
description: Bu konuda, bir proforma faturanın onaylanması hakkında bilgiler sağlanmaktadır.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b2ed241509d2643d841ce55777e6e316612f70b8
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287892"
---
# <a name="confirm-a-proforma-invoice"></a><span data-ttu-id="6c1e6-103">Proforma faturaları onaylama</span><span class="sxs-lookup"><span data-stu-id="6c1e6-103">Confirm a proforma invoice</span></span>

<span data-ttu-id="6c1e6-104">_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="6c1e6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="6c1e6-105">Proforma fatura onaylandıktan sonra, proje faturasının durumu **Onaylandı** güncellenir.</span><span class="sxs-lookup"><span data-stu-id="6c1e6-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="6c1e6-106">Bir fatura onaylandığında, salt okunur olur.</span><span class="sxs-lookup"><span data-stu-id="6c1e6-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="6c1e6-107">İleriye dönük olarak, fatura yalnızca müşteri tarafından başlatılan düzeltmeler veya krediler varsa veya ödeme olarak işaretlendiğinde düzeltilebilir.</span><span class="sxs-lookup"><span data-stu-id="6c1e6-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, or when it's marked as paid.</span></span>

<span data-ttu-id="6c1e6-108">Aşağıdaki tabloda sistem tarafından oluşturulan fiili listeler.</span><span class="sxs-lookup"><span data-stu-id="6c1e6-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="6c1e6-109">Bu fiili işlemler, onaylanmadan önce taslak proje faturasında belirli işlemler gerçekleştirildiğinde oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="6c1e6-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p><span data-ttu-id="6c1e6-110">
                    <strong>Senaryo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6c1e6-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="608" valign="top">
                <p><span data-ttu-id="6c1e6-111">
                    <strong>Onayda oluşturulan fiililer</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6c1e6-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6c1e6-112">Taslak faturada herhangi bir işlem yapılmadan bir zaman hareketi faturalandırma.</span><span class="sxs-lookup"><span data-stu-id="6c1e6-112">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6c1e6-113">Orijinal saat onayının saat ve tutarı için faturalandırılmamış satış tersi.</span><span class="sxs-lookup"><span data-stu-id="6c1e6-113">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6c1e6-114">Orijinal saat onayının saat ve tutarı için faturalandırılmış satış fiili.</span><span class="sxs-lookup"><span data-stu-id="6c1e6-114">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="6c1e6-115">Miktarı azaltmak için düzenlenen bir zaman hareketinin faturalandırması.</span><span class="sxs-lookup"><span data-stu-id="6c1e6-115">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6c1e6-116">Orijinal saat onayının saat ve tutarı için faturalandırılmamış satış tersi.</span><span class="sxs-lookup"><span data-stu-id="6c1e6-116">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6c1e6-117">Düzenlenen fatura satırı ayrıntısı üzerindeki saat ve tutar için ücretlendirilebilen yeni bir faturalanmamış satış fiili, faturalandırılmamış satışların fiilinin tersine çevrilmesi ve eşdeğer faturalı satışların fiili.</span><span class="sxs-lookup"><span data-stu-id="6c1e6-117">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6c1e6-118">Düzenlenen fatura satırı ayrıntısı üzerindeki doğrulanan rakamlar çıkarıldıktan sonra kalan saat ve tutar için ücretlendirilemeyen yeni bir faturalanmamış satış fiili, faturalandırılmamış satışların fiilinin tersine çevrilmesi ve eşdeğer faturalı satışların fiili.</span><span class="sxs-lookup"><span data-stu-id="6c1e6-118">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6c1e6-119">Miktarı artırmak için düzenlenen bir zaman hareketinin faturalandırması.</span><span class="sxs-lookup"><span data-stu-id="6c1e6-119">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6c1e6-120">Orijinal saat onayının saat ve tutarı için faturalandırılmamış satış tersi.</span><span class="sxs-lookup"><span data-stu-id="6c1e6-120">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6c1e6-121">Düzenlenen fatura satırı ayrıntısı üzerindeki saat ve tutar için ücretlendirilebilen yeni bir faturalanmamış satış fiili, faturalandırılmamış satışların fiilinin tersine çevrilmesi ve eşdeğer faturalı satışların fiili.</span><span class="sxs-lookup"><span data-stu-id="6c1e6-121">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6c1e6-122">Taslak faturada herhangi bir işlem yapılmadan bir gider hareketi faturalandırma.</span><span class="sxs-lookup"><span data-stu-id="6c1e6-122">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6c1e6-123">Orijinal gider onayının miktarı ve tutarı için faturalandırılmamış satış tersi.</span><span class="sxs-lookup"><span data-stu-id="6c1e6-123">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6c1e6-124">Orijinal gider onayının miktarı ve tutarı için faturalandırılmış satış fiili.</span><span class="sxs-lookup"><span data-stu-id="6c1e6-124">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="6c1e6-125">Miktarı azaltmak için düzenlenen bir gider hareketinin faturalandırması.</span><span class="sxs-lookup"><span data-stu-id="6c1e6-125">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6c1e6-126">Orijinal gider onayının miktarı ve tutarı için faturalandırılmamış satış tersi.</span><span class="sxs-lookup"><span data-stu-id="6c1e6-126">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6c1e6-127">Düzenlenen fatura satırı ayrıntısı üzerindeki miktar ve tutar için ücretlendirilebilen yeni bir faturalanmamış satış fiili, faturalandırılmamış satışların fiilinin tersine çevrilmesi ve eşdeğer faturalı satışların fiili.</span><span class="sxs-lookup"><span data-stu-id="6c1e6-127">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6c1e6-128">Düzenlenen fatura satırı ayrıntısı üzerindeki doğrulanan rakamlar çıkarıldıktan sonra kalan miktar ve tutar için ücretlendirilemeyen yeni bir faturalanmamış satış fiili, faturalandırılmamış satışların fiilinin tersine çevrilmesi ve eşdeğer faturalı satışların fiili.</span><span class="sxs-lookup"><span data-stu-id="6c1e6-128">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent of the billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6c1e6-129">Miktarı artırmak için düzenlenen bir gider hareketinin faturalandırması.</span><span class="sxs-lookup"><span data-stu-id="6c1e6-129">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6c1e6-130">Orijinal gider onayının miktarı ve tutarı için faturalandırılmamış satış tersi.</span><span class="sxs-lookup"><span data-stu-id="6c1e6-130">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6c1e6-131">Düzenlenen fatura satırı ayrıntısı üzerindeki miktar ve tutar için ücretlendirilebilen yeni bir faturalanmamış satış fiili, faturalandırılmamış satışların fiilinin tersine çevrilmesi ve eşdeğer faturalı satışların fiili.</span><span class="sxs-lookup"><span data-stu-id="6c1e6-131">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the untilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6c1e6-132">Bir ücret faturalama.</span><span class="sxs-lookup"><span data-stu-id="6c1e6-132">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6c1e6-133">Orijinal yevmiye defteri satırında ücret tutarı için faturalandırılmamış satış tersi.</span><span class="sxs-lookup"><span data-stu-id="6c1e6-133">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6c1e6-134">Orijinal ücret yevmiye defteri satırı miktarı ve tutarı için faturalandırılmış satış fiili.</span><span class="sxs-lookup"><span data-stu-id="6c1e6-134">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="6c1e6-135">Bir kilometre taşını faturalama.</span><span class="sxs-lookup"><span data-stu-id="6c1e6-135">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6c1e6-136">Proje sözleşmesi satırındaki özgün kilometre taşındaki kilometre taşı tutarı için faturalı satış fiili.</span><span class="sxs-lookup"><span data-stu-id="6c1e6-136">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]