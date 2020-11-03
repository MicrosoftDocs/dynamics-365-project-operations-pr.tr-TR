---
title: Düzeltilen faturalar
description: Bu konu düzeltilen faturalar hakkında bilgi sağlar.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: b31e702cc15bbb3937e8c4b305064212f63ce919
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086492"
---
# <a name="corrected-invoices"></a><span data-ttu-id="ef889-103">Düzeltilen faturalar</span><span class="sxs-lookup"><span data-stu-id="ef889-103">Corrected invoices</span></span>

<span data-ttu-id="ef889-104">_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="ef889-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="ef889-105">Onaylanan faturalar düzenlenebilir.</span><span class="sxs-lookup"><span data-stu-id="ef889-105">Confirmed invoices can be edited.</span></span> <span data-ttu-id="ef889-106">Onaylı bir faturayı düzeltirken, düzeltilen faturaya ait bir taslak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="ef889-106">When you edit a confirmed invoice, a draft of the corrected invoice is created.</span></span> <span data-ttu-id="ef889-107">Orijinal faturadaki tüm hareketleri ve miktarları tersine çevirmek istediğiniz varsayıldığından, düzeltilen fatura orijinal faturadaki tüm işlemleri içerir ve üzerindeki tüm miktarlar 0 (sıfır) olur.</span><span class="sxs-lookup"><span data-stu-id="ef889-107">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, the corrected invoice includes all the transactions from the original invoice, and all the quantities on it are zero (0).</span></span>

<span data-ttu-id="ef889-108">Herhangi bir hareketin düzeltilmesi gerekmiyorsa, bunları taslak düzeltme faturasından kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ef889-108">When transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="ef889-109">Yalnızca kısmi miktarı ters çevirmek veya geri döndürmek için, satır ayrıntısında Miktar alanını düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ef889-109">To reverse or return only a partial quantity, you can edit the Quantity field on the line detail.</span></span> <span data-ttu-id="ef889-110">Fatura satırı ayrıntısını açarsanız, orijinal fatura miktarını görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ef889-110">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="ef889-111">Ardından, geçerli fatura miktarını, orijinal fatura miktarından az veya daha fazla olacak şekilde düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ef889-111">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="ef889-112">Düzeltme faturasını onaylandıktan sonra, orijinal faturalanmış satış fiili değeri tersine çevrilir ve yeni bir faturalanmış satış fiili değeri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="ef889-112">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="ef889-113">Miktar azaltılırsa, fark faturalanmamış yeni bir satış fiili değeri oluşturulmasına neden olur.</span><span class="sxs-lookup"><span data-stu-id="ef889-113">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="ef889-114">Örneğin, orijinal faturalanmış satış sekiz saat içinse ve düzeltilen fatura satır ayrıntısı altı saatlik bir miktar içeriyorsa, orijinal faturalanan satış satırı ters çevrilir ve iki yeni gerçek değer oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="ef889-114">For example, if the original billed sale was for eight hours, and the corrected invoice line detail has a reduced quantity of six hours, the original billed sales line is revered and two new actuals are created:</span></span>

- <span data-ttu-id="ef889-115">Altı saat için faturalanmış satış fiili değeri.</span><span class="sxs-lookup"><span data-stu-id="ef889-115">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="ef889-116">Kalan iki saat için faturalandırılmamış bir satış fiili değeri.</span><span class="sxs-lookup"><span data-stu-id="ef889-116">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="ef889-117">Müşteriyle yapılan anlaşmaya bağlı olarak bu hareket daha sonra faturalanabilir veya borçlandırılamaz olarak işaretlenebilir.</span><span class="sxs-lookup"><span data-stu-id="ef889-117">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>
