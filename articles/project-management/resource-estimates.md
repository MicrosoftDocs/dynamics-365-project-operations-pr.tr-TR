---
title: Kaynak tahminleri
description: Bu konuda, Project Operations'ta kaynak tahminlerinin nasıl hesaplanacağı hakkında bilgiler sağlanmaktadır.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2ebde2b3c5bcfb5faa02ee476065ac34b1953432
ms.sourcegitcommit: f255b2cbf290973ce62fe2c1c121bd1df15a7392
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/01/2020
ms.locfileid: "3928616"
---
# <a name="resource-estimates"></a><span data-ttu-id="775db-103">Kaynak tahminleri</span><span class="sxs-lookup"><span data-stu-id="775db-103">Resource estimates</span></span>

<span data-ttu-id="775db-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="775db-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="775db-105">Kaynak tahminleri, uygun fiyatlandırma boyutlarıyla birlikte iş kırılım yapısında tanımlanan zaman aşamalı çalışmadan gelir.</span><span class="sxs-lookup"><span data-stu-id="775db-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="775db-106">Genellikle hesaplama **her rol için oran/sa x saat** olarak yapılır.</span><span class="sxs-lookup"><span data-stu-id="775db-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="775db-107">Her bir kaynağın zaman aşamalı çalışması, kaynak atama kaydında depolanır.</span><span class="sxs-lookup"><span data-stu-id="775db-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="775db-108">Fiyatlandırma, önceden tanımlanmış bir fiyat listesinde depolanır.</span><span class="sxs-lookup"><span data-stu-id="775db-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="775db-109">Birim dönüştürme, uygun fiyat listesine göre uygulanır.</span><span class="sxs-lookup"><span data-stu-id="775db-109">Unit conversion is applied based on the applicable price list.</span></span>

![Kaynak Tahminleri](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="775db-111">Varsayılan maliyet fiyatı ve maliyet para birimi</span><span class="sxs-lookup"><span data-stu-id="775db-111">Default cost price and cost currency</span></span>

<span data-ttu-id="775db-112">Maliyet fiyatları varsayılan olarak Kuruluş Biriminden alınır.</span><span class="sxs-lookup"><span data-stu-id="775db-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="775db-113">Varsayılan fatura oranı ve satış para birimi</span><span class="sxs-lookup"><span data-stu-id="775db-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="775db-114">Satış fiyatları her anlaşma için bir kere uygulanır.</span><span class="sxs-lookup"><span data-stu-id="775db-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="775db-115">Varsayılan satış fiyatı listesi hiyerarşisi aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="775db-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="775db-116">Kuruluş</span><span class="sxs-lookup"><span data-stu-id="775db-116">Organization</span></span>
2. <span data-ttu-id="775db-117">Müşteri</span><span class="sxs-lookup"><span data-stu-id="775db-117">Customer</span></span>
3. <span data-ttu-id="775db-118">Teklif/sözleşme</span><span class="sxs-lookup"><span data-stu-id="775db-118">Quote/contract</span></span>
