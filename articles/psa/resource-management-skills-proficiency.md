---
title: Beceriler ve uzmanlık modelleri
description: Bu konu, beceriler ve uzmanlık modellerinin nasıl kullanılacağı hakkında bilgi sağlar.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/13/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: cd243544df062e5801bbfa0a3bd75c4d9a116a6f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086544"
---
# <a name="skills-and-proficiency-models"></a><span data-ttu-id="79f00-103">Beceriler ve uzmanlık modelleri</span><span class="sxs-lookup"><span data-stu-id="79f00-103">Skills and proficiency models</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="79f00-104">Beceriler, Dynamics 365 Project Service Automation ile varsa Dynamics 365 Field Service arasında paylaşılan kaynak özellikleridir.</span><span class="sxs-lookup"><span data-stu-id="79f00-104">Skills are resource characteristics that are shared between Dynamics 365 Project Service Automation and if present, Dynamics 365 Field Service.</span></span> 

<span data-ttu-id="79f00-105">Project Service Automation'daki beceri deposunu korumak için **Kaynaklar** \> **Kaynak Becerileri** 'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="79f00-105">To maintain the repository of skills in Project Service Automation, go to **Resources** \> **Resource Skills**.</span></span> 

> ![Kaynak Becerileri](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="79f00-107">Kaynakları derecelendirmek için uzmanlık modellerini kullanma</span><span class="sxs-lookup"><span data-stu-id="79f00-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="79f00-108">Kaynaklar için beceriler, uzmanlık modellerine göre derecelendirilir.</span><span class="sxs-lookup"><span data-stu-id="79f00-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="79f00-109">Her derecelendirme bir uzmanlık modelidir.</span><span class="sxs-lookup"><span data-stu-id="79f00-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="79f00-110">Uzmanlık modeli oluşturmak için **Kaynaklar** \> **Uzmanlık Modelleri** 'ne gidin ve ardından **Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="79f00-110">To create a proficiency model, go to **Resources** \> **Proficiency Models** , and then select **New**.</span></span>
2. <span data-ttu-id="79f00-111">Yeni derecelendirme modelinde minimum derecelendirme değerini, maksimum derecelendirme değerini ve derecelendirilen varlığı belirtin.</span><span class="sxs-lookup"><span data-stu-id="79f00-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="79f00-112">**Değerlendirme Değerleri** alt ızgarasında, minimumdan maksimuma kadar farklı derecelendirme değerleri tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="79f00-112">In the **Rating Values** sub-grid, you can define the different rating values, from the minimum to the maximum.</span></span>

> ![Minimum ve maksimum derecelendirme tanımlandı](media/Resource-Management-image85.png)

<span data-ttu-id="79f00-114">Bu derecelendirme değerleri; **Kaynak Gereksinimleri** , **Zamanlama Panosu** ve **Zamanlama Yardımcısı** filtrelerinde gösterilir.</span><span class="sxs-lookup"><span data-stu-id="79f00-114">These rating values are shown on the **Resource Requirements** , **Schedule Board** , and **Schedule Assistant** filters.</span></span>