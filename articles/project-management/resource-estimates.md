---
title: Kaynak tahminleri
description: Bu konuda, Project Operations'ta kaynak tahminlerinin nasıl hesaplanacağı hakkında bilgiler sağlanmaktadır.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 454b8931db53739a7bc19364911109802a1ed087
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127406"
---
# <a name="resource-estimates"></a><span data-ttu-id="8784f-103">Kaynak tahminleri</span><span class="sxs-lookup"><span data-stu-id="8784f-103">Resource estimates</span></span>

<span data-ttu-id="8784f-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="8784f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8784f-105">Kaynak tahminleri, uygun fiyatlandırma boyutlarıyla birlikte iş kırılım yapısında tanımlanan zaman aşamalı çalışmadan gelir.</span><span class="sxs-lookup"><span data-stu-id="8784f-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="8784f-106">Genellikle hesaplama **her rol için oran/sa x saat** olarak yapılır.</span><span class="sxs-lookup"><span data-stu-id="8784f-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="8784f-107">Her bir kaynağın zaman aşamalı çalışması, kaynak atama kaydında depolanır.</span><span class="sxs-lookup"><span data-stu-id="8784f-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="8784f-108">Fiyatlandırma, önceden tanımlanmış bir fiyat listesinde depolanır.</span><span class="sxs-lookup"><span data-stu-id="8784f-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="8784f-109">Birim dönüştürme, uygun fiyat listesine göre uygulanır.</span><span class="sxs-lookup"><span data-stu-id="8784f-109">Unit conversion is applied based on the applicable price list.</span></span>

![Kaynak Tahminleri](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="8784f-111">Varsayılan maliyet fiyatı ve maliyet para birimi</span><span class="sxs-lookup"><span data-stu-id="8784f-111">Default cost price and cost currency</span></span>

<span data-ttu-id="8784f-112">Maliyet fiyatları varsayılan olarak Kuruluş Biriminden alınır.</span><span class="sxs-lookup"><span data-stu-id="8784f-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="8784f-113">Varsayılan fatura oranı ve satış para birimi</span><span class="sxs-lookup"><span data-stu-id="8784f-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="8784f-114">Satış fiyatları her anlaşma için bir kere uygulanır.</span><span class="sxs-lookup"><span data-stu-id="8784f-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="8784f-115">Varsayılan satış fiyatı listesi hiyerarşisi aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="8784f-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="8784f-116">Kuruluş</span><span class="sxs-lookup"><span data-stu-id="8784f-116">Organization</span></span>
2. <span data-ttu-id="8784f-117">Müşteri</span><span class="sxs-lookup"><span data-stu-id="8784f-117">Customer</span></span>
3. <span data-ttu-id="8784f-118">Teklif/sözleşme</span><span class="sxs-lookup"><span data-stu-id="8784f-118">Quote/contract</span></span>
