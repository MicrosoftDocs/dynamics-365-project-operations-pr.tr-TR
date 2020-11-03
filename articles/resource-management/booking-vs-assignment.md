---
title: Ayırmalar ve atamalar
description: Bu konuda, kaynak ayırmaları ile kaynak atamaları arasındaki farklar hakkında bilgiler sağlanmaktadır.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fa99783e52dbcdeaf80bbfd03df0f458f86b5e99
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086173"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="a6fd5-103">Ayırmalar ve atamalar</span><span class="sxs-lookup"><span data-stu-id="a6fd5-103">Bookings vs assignments</span></span>

<span data-ttu-id="a6fd5-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="a6fd5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a6fd5-105">Ayırmalar, kaynakların bir projeye kalıcı veya geçici tahsisatıdır.</span><span class="sxs-lookup"><span data-stu-id="a6fd5-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="a6fd5-106">Kalıcı ayırmalar, bir kaynağın kapasitesini tüketir.</span><span class="sxs-lookup"><span data-stu-id="a6fd5-106">Hard bookings consume a resource's capacity.</span></span> 

<span data-ttu-id="a6fd5-107">Atamalar, kaynakların proje zamanlamasındaki proje görevlerine atanmasıdır.</span><span class="sxs-lookup"><span data-stu-id="a6fd5-107">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="a6fd5-108">Kaynaklar, gerçek veya genel olabilir.</span><span class="sxs-lookup"><span data-stu-id="a6fd5-108">The resources can be real or generic.</span></span> 

<span data-ttu-id="a6fd5-109">İdeal olarak, gerçek kaynaklar için ayırma ve atamalar uyuşmalıdır çünkü farklı değillerdir.</span><span class="sxs-lookup"><span data-stu-id="a6fd5-109">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="a6fd5-110">Ancak Microsoft Dynamics Project Operations bu uyuşmayı zorunlu kılmaz.</span><span class="sxs-lookup"><span data-stu-id="a6fd5-110">However, Microsoft Dynamics Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="a6fd5-111">**Mutabakat** görünümü, proje yöneticisine, bir kaynağın ayırma ve atamalarının uyuşmadığı yerleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="a6fd5-111">The **Reconciliation** view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>