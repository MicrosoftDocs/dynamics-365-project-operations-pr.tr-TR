---
title: Fiyatlandırma boyutları olarak Project Operations alanları
description: Bu konu, Dynamics 365 Project Operations içindeki fiyatlandırma boyutları olarak alanları kullanma hakkında bilgi sağlar.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 59367b35f15f806b109f606e912edc487d9e7685
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119262"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="3ce53-103">Fiyatlandırma boyutları olarak Project Operations alanları</span><span class="sxs-lookup"><span data-stu-id="3ce53-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="3ce53-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="3ce53-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3ce53-105">**Gerçek değerler** varlığı, kaynak tabanlı fiyatlandırma için fiyatlandırma boyutları olarak kullanılabilen çok sayıda alana sahiptir.</span><span class="sxs-lookup"><span data-stu-id="3ce53-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="3ce53-106">Örneğin, **Ayrılabilir Kaynak** sık kullanılan alanlardan biridir.</span><span class="sxs-lookup"><span data-stu-id="3ce53-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="3ce53-107">20-30'dan az faturalanabilir kaynağa sahip olan daha küçük şirketler için her kaynağa özgü fatura ve maliyet oranları daha basit bir yaklaşım olabilir.</span><span class="sxs-lookup"><span data-stu-id="3ce53-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="3ce53-108">Ancak, faturalandırılabilir iş gücü büyüdükçe kaynağa özgü oranları korumak için gerçekçi olmaz.</span><span class="sxs-lookup"><span data-stu-id="3ce53-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="3ce53-109">Kaynak maliyeti ve fatura oranları kaynak olarak öne çıkar, daha fazla deneyim kazanın veya farklı yetenekler kümesi alın.</span><span class="sxs-lookup"><span data-stu-id="3ce53-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="3ce53-110">Bir diğer örnek de işlem kategorisinde yer alır.</span><span class="sxs-lookup"><span data-stu-id="3ce53-110">Another example is that of transaction category.</span></span> <span data-ttu-id="3ce53-111">Müşteriler ve Uygulayıcılar işlem kategorisini işi sınıflandırmak, alanı işin kategorisine göre fiyatlandırıp maliyetlendirmek için kullanır.</span><span class="sxs-lookup"><span data-stu-id="3ce53-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>
