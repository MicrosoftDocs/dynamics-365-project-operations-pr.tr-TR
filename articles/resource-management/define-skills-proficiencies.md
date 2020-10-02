---
title: Beceriler ve uzmanlıkları tanımlama
description: Bu konu, uzmanlık modellerinin kaynakları değerlendirmek için nasıl kullanılacağı hakkında bilgi sağlar.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
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
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9376e0b268a3ab682716da604ceecfa1e878da68
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897655"
---
# <a name="define-skills-and-proficiencies"></a><span data-ttu-id="052b7-103">Beceriler ve uzmanlıkları tanımlama</span><span class="sxs-lookup"><span data-stu-id="052b7-103">Define skills and proficiencies</span></span>

<span data-ttu-id="052b7-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="052b7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="052b7-105">Beceriler, Dynamics 365 Project Operations ile varsa Dynamics 365 Field Service arasında paylaşılan kaynak özellikleridir.</span><span class="sxs-lookup"><span data-stu-id="052b7-105">Skills are resource characteristics that are shared between Dynamics 365 Project Operations and if present, Dynamics 365 Field Service.</span></span> 

- <span data-ttu-id="052b7-106">Project Operations'daki beceri deposunu korumak için **Kaynaklar** \> **Kaynak Becerileri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="052b7-106">To maintain the repository of skills in Project Operations, go to **Resources** \> **Resource Skills**.</span></span> 

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="052b7-107">Kaynakları derecelendirmek için uzmanlık modellerini kullanma</span><span class="sxs-lookup"><span data-stu-id="052b7-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="052b7-108">Kaynaklar için beceriler, uzmanlık modellerine göre derecelendirilir.</span><span class="sxs-lookup"><span data-stu-id="052b7-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="052b7-109">Her derecelendirme bir uzmanlık modelidir.</span><span class="sxs-lookup"><span data-stu-id="052b7-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="052b7-110">Uzmanlık modeli oluşturmak için **Kaynaklar** \> **Uzmanlık Modelleri**'ne gidin ve ardından **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="052b7-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="052b7-111">Yeni derecelendirme modelinde minimum derecelendirme değerini, maksimum derecelendirme değerini ve derecelendirilen varlığı belirtin.</span><span class="sxs-lookup"><span data-stu-id="052b7-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="052b7-112">**Değerlendirme Değerleri** alt ızgarasında, minimumdan maksimuma kadar farklı derecelendirme değerleri tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="052b7-112">In the **Rating Values** sub-grid, you can define the different rating values, from the minimum to the maximum.</span></span>


<span data-ttu-id="052b7-113">Bu derecelendirme değerleri; **Kaynak Gereksinimleri**, **Zamanlama Panosu** ve **Zamanlama Yardımcısı** filtrelerinde gösterilir.</span><span class="sxs-lookup"><span data-stu-id="052b7-113">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>