---
title: Gelişmiş Teklif Verme, Fiyatlandırma ve Faturalama
description: Bu konu, Project Service Automation'da teklif verme, faturalama ve fiyatlandırma hakkında bilgiler sağlar.
author: kfend
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 2/14/2019
ms.topic: article
ms.author: kfend
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: c4674aba1d152289c78a202f9da1f710e28f9960
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275247"
---
# <a name="advanced-quoting-pricing-and-billing-guide"></a><span data-ttu-id="07813-103">Gelişmiş teklif verme, fiyatlama ve faturalama kılavuzu</span><span class="sxs-lookup"><span data-stu-id="07813-103">Advanced quoting, pricing, and billing guide</span></span>

[!include [banner](../../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="07813-104">Doğru kaynakları doğru zamanda bulma, bu kaynakları projelere ayırma ve bunların kullanılmalarını sağlama yetenekleri kuruluşların gelir ve müşteri memnuniyeti hedeflerine ulaşmasına yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="07813-104">The ability to find the right resources at the right time, book those resources on projects, and keep resources utilized helps organizations meet revenue targets and customer satisfaction goals.</span></span> 

<span data-ttu-id="07813-105">daha önce bu konuda yer alan PDF bağlantısı kaldırılmış ve içerik aşağıdaki konulara taşınmıştır:</span><span class="sxs-lookup"><span data-stu-id="07813-105">The PDF link that was previously in this topic has been removed and the content has been moved to the following topics:</span></span>

- [<span data-ttu-id="07813-106">Teklif verme, fiyatlandırma ve faturalama</span><span class="sxs-lookup"><span data-stu-id="07813-106">Quoting, pricing, and billing</span></span>](../quote-bill-price.md)
- [<span data-ttu-id="07813-107">Satış süreçleri</span><span class="sxs-lookup"><span data-stu-id="07813-107">Sales processes</span></span>](../basic-sales-process.md)
- [<span data-ttu-id="07813-108">Teklifler ve teklif satırları</span><span class="sxs-lookup"><span data-stu-id="07813-108">Quotes and quote lines</span></span>](../basic-quote-lines.md)
- [<span data-ttu-id="07813-109">Ürün tabanlı teklif satırları</span><span class="sxs-lookup"><span data-stu-id="07813-109">Product-based quote lines</span></span>](../product-based-quote-lines.md)
- [<span data-ttu-id="07813-110">Fiyatlandırma</span><span class="sxs-lookup"><span data-stu-id="07813-110">Pricing</span></span>](../basic-pricing.md)
- [<span data-ttu-id="07813-111">Ürün kataloğu fiyatlandırması</span><span class="sxs-lookup"><span data-stu-id="07813-111">Product catalog pricing</span></span>](../product-catalog-pricing.md)
- [<span data-ttu-id="07813-112">İş işlemleri</span><span class="sxs-lookup"><span data-stu-id="07813-112">Business transactions</span></span>](../basic-business-transactions.md)
- [<span data-ttu-id="07813-113">Tahminler</span><span class="sxs-lookup"><span data-stu-id="07813-113">Estimates</span></span>](../estimates.md)
- [<span data-ttu-id="07813-114">Gerçekler</span><span class="sxs-lookup"><span data-stu-id="07813-114">Actuals</span></span>](../actuals.md)
- [<span data-ttu-id="07813-115">Proje tekliflerini analiz etme</span><span class="sxs-lookup"><span data-stu-id="07813-115">Analyzing project quotes</span></span>](../basic-analyzing-quotes.md)
- [<span data-ttu-id="07813-116">Kuruluş birimleri</span><span class="sxs-lookup"><span data-stu-id="07813-116">Organizational units</span></span>](../advanced-organizational.md)
- [<span data-ttu-id="07813-117">Birim grupları ve birimler</span><span class="sxs-lookup"><span data-stu-id="07813-117">Unit groups and units</span></span>](../advanced-units.md)
- [<span data-ttu-id="07813-118">Birden fazla para birimi senaryoları</span><span class="sxs-lookup"><span data-stu-id="07813-118">Multi-currency scenarios</span></span>](../advanced-currency.md)
- [<span data-ttu-id="07813-119">Fiili değerleri kaydetme</span><span class="sxs-lookup"><span data-stu-id="07813-119">Recording actuals</span></span>](../advanced-actuals.md)

> [!NOTE]
> <span data-ttu-id="07813-120">Bu konu gelecekteki bir belge güncelleştirmesinde kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="07813-120">This topic will be removed in a future documentation update.</span></span> 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]