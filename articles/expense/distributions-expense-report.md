---
title: Gider raporundaki dağıtımlar
description: Giderleri bir gider raporuna girdiğinizde, kuruluşunuzdaki birden çok projeye, tüzel kişiliğe veya hesaba dağıtabilirsiniz.
author: suvaidya
manager: AnnBe
ms.date: 10/10/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: a1fa7383e7715fe57380de0a006ccc4e020bb5a5
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086205"
---
# <a name="distributions-on-an-expense-report"></a><span data-ttu-id="8a0ef-103">Gider raporundaki dağıtımlar</span><span class="sxs-lookup"><span data-stu-id="8a0ef-103">Distributions on an expense report</span></span>

<span data-ttu-id="8a0ef-104">_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="8a0ef-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="8a0ef-105">Giderleri bir gider raporuna girdiğinizde, kuruluşunuzdaki birden çok projeye, finansal boyuta veya hesaba dağıtabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8a0ef-105">When you enter expenses on an expense report, you can distribute them across multiple projects, financial dimensions, or accounts in your organization.</span></span>

<span data-ttu-id="8a0ef-106">Örneğin, Fabrikam satış temsilcisi Nancy, Kopenhag'dan Frankfurt'a seyahat etmiştir.</span><span class="sxs-lookup"><span data-stu-id="8a0ef-106">For example, Nancy, a Fabrikam sales representative, traveled from Copenhagen to Frankfurt.</span></span> <span data-ttu-id="8a0ef-107">Frankfurt'ta, Nancy her kuruluşun farklı projelerini tartışmak için iki kuruluşla görüşür.</span><span class="sxs-lookup"><span data-stu-id="8a0ef-107">In Frankfurt, Nancy met with two organizations to discuss separate projects for each organization.</span></span> <span data-ttu-id="8a0ef-108">Nancy, kuruluş A ile A projesi üzerinde yedi iş günü, kuruluş B ile B projesi üzerinde de üç iş günü çalışır.</span><span class="sxs-lookup"><span data-stu-id="8a0ef-108">Nancy spent seven business days working with organization A on project A, and three business days working with organization B on project B.</span></span>

<span data-ttu-id="8a0ef-109">Nancy Frankfurt'tayken iki farklı projede çalıştığından, gider raporunu girerken giderleri her projeye uygun şekilde dağıtır.</span><span class="sxs-lookup"><span data-stu-id="8a0ef-109">Because Nancy worked on two separate projects while was in Frankfurt, when she enters the expense report, Nancy distributes the expenses as appropriate for each project.</span></span> <span data-ttu-id="8a0ef-110">Aşağıdaki tabloda Nancy'nin giderleri nasıl dağıttığı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="8a0ef-110">The following table shows how Nancy distributed the expenses.</span></span>

| <span data-ttu-id="8a0ef-111">Gider türü</span><span class="sxs-lookup"><span data-stu-id="8a0ef-111">Expense type</span></span> | <span data-ttu-id="8a0ef-112">Toplam gider tutarı</span><span class="sxs-lookup"><span data-stu-id="8a0ef-112">Total expense amount</span></span> | <span data-ttu-id="8a0ef-113">A projesine dağıtılan tutar</span><span class="sxs-lookup"><span data-stu-id="8a0ef-113">Amount distributed to project A</span></span> | <span data-ttu-id="8a0ef-114">B projesine dağıtılan tutar</span><span class="sxs-lookup"><span data-stu-id="8a0ef-114">Amount distributed to project B</span></span> |
|--------------|----------------------|---------------------------------|---------------------------------|
| <span data-ttu-id="8a0ef-115">Tren ücreti</span><span class="sxs-lookup"><span data-stu-id="8a0ef-115">Train fare</span></span>   | <span data-ttu-id="8a0ef-116">578 DKK</span><span class="sxs-lookup"><span data-stu-id="8a0ef-116">DKK 578</span></span>              | <span data-ttu-id="8a0ef-117">405 DKK</span><span class="sxs-lookup"><span data-stu-id="8a0ef-117">DKK 405</span></span>                         | <span data-ttu-id="8a0ef-118">173 DKK</span><span class="sxs-lookup"><span data-stu-id="8a0ef-118">DKK 173</span></span>                         |
| <span data-ttu-id="8a0ef-119">Otel</span><span class="sxs-lookup"><span data-stu-id="8a0ef-119">Hotel</span></span>        | <span data-ttu-id="8a0ef-120">725 EUR</span><span class="sxs-lookup"><span data-stu-id="8a0ef-120">EUR 725</span></span>              | <span data-ttu-id="8a0ef-121">557 EUR</span><span class="sxs-lookup"><span data-stu-id="8a0ef-121">EUR 557</span></span>                         | <span data-ttu-id="8a0ef-122">168 EUR</span><span class="sxs-lookup"><span data-stu-id="8a0ef-122">EUR 168</span></span>                         |
| <span data-ttu-id="8a0ef-123">Yemekler</span><span class="sxs-lookup"><span data-stu-id="8a0ef-123">Meals</span></span>        | <span data-ttu-id="8a0ef-124">346 EUR</span><span class="sxs-lookup"><span data-stu-id="8a0ef-124">EUR 346</span></span>              | <span data-ttu-id="8a0ef-125">284 EUR</span><span class="sxs-lookup"><span data-stu-id="8a0ef-125">EUR 284</span></span>                         | <span data-ttu-id="8a0ef-126">62 EUR</span><span class="sxs-lookup"><span data-stu-id="8a0ef-126">EUR 62</span></span>                          |
