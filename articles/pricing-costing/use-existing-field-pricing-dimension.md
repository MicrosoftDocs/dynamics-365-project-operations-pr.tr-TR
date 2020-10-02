---
title: Fiyatlandırma boyutları olarak Project Operations alanları
description: Bu konu, Dynamics 365 Project Operations içindeki fiyatlandırma boyutları olarak alanları kullanma hakkında bilgi sağlar.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 3ddf3098e45fdc9b99067b64df05e2adc0b6ad05
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896440"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="6fc21-103">Fiyatlandırma boyutları olarak Project Operations alanları</span><span class="sxs-lookup"><span data-stu-id="6fc21-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="6fc21-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="6fc21-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6fc21-105">**Gerçek değerler** varlığı, kaynak tabanlı fiyatlandırma için fiyatlandırma boyutları olarak kullanılabilen çok sayıda alana sahiptir.</span><span class="sxs-lookup"><span data-stu-id="6fc21-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="6fc21-106">Örneğin, **Ayrılabilir Kaynak** sık kullanılan alanlardan biridir.</span><span class="sxs-lookup"><span data-stu-id="6fc21-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="6fc21-107">20-30'dan az faturalanabilir kaynağa sahip olan daha küçük şirketler için her kaynağa özgü fatura ve maliyet oranları daha basit bir yaklaşım olabilir.</span><span class="sxs-lookup"><span data-stu-id="6fc21-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="6fc21-108">Ancak, faturalandırılabilir iş gücü büyüdükçe kaynağa özgü oranları korumak için gerçekçi olmaz.</span><span class="sxs-lookup"><span data-stu-id="6fc21-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="6fc21-109">Kaynak maliyeti ve fatura oranları kaynak olarak öne çıkar, daha fazla deneyim kazanın veya farklı yetenekler kümesi alın.</span><span class="sxs-lookup"><span data-stu-id="6fc21-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="6fc21-110">Bir diğer örnek de işlem kategorisinde yer alır.</span><span class="sxs-lookup"><span data-stu-id="6fc21-110">Another example is that of transaction category.</span></span> <span data-ttu-id="6fc21-111">Müşteriler ve Uygulayıcılar işlem kategorisini işi sınıflandırmak, alanı işin kategorisine göre fiyatlandırıp maliyetlendirmek için kullanır.</span><span class="sxs-lookup"><span data-stu-id="6fc21-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>
