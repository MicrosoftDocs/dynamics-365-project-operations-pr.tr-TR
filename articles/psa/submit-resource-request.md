---
title: Kaynak isteği gönderme
description: Bu konu, proje kaynağı için istek gönderme hakkında bilgi sağlar.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: bcea3d640d7e9ee2b071c55bff9ade3268edb319
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086417"
---
# <a name="submitting-a-resource-request"></a><span data-ttu-id="8cf2d-103">Kaynak isteği gönderme</span><span class="sxs-lookup"><span data-stu-id="8cf2d-103">Submitting a resource request</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="8cf2d-104">Oluşturulmuş bir kaynak gereksinimini bir kaynak isteği olarak gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8cf2d-104">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="8cf2d-105">İstek daha sonra yerine getirilmesi için bir kaynak yöneticisine gönderilir.</span><span class="sxs-lookup"><span data-stu-id="8cf2d-105">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="8cf2d-106">Project Service Automation'da (PSA) **Projeler** sayfasında ayrılabilir kaynakların listesini görüntülemek için **Takım** sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8cf2d-106">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab to view a list bookable resources.</span></span> 
2. <span data-ttu-id="8cf2d-107">Listeden kaynak gereksinimi olan genel kaynağı seçin ve ardından **İstek Gönder** 'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8cf2d-107">Select the generic resource that has a resource requirement from the list and then click **Submit Request**.</span></span>

![Kaynak isteği gönderme](media/RM-how-to-18.png)

<span data-ttu-id="8cf2d-109">Genel takım üyesinin istek durumu **Gönderildi** olarak değişir.</span><span class="sxs-lookup"><span data-stu-id="8cf2d-109">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="8cf2d-110">İstek kaynak yöneticisi tarafından yerine getirildikten sonra kaynak yöneticisi isteği adlandırılmış kaynak ayırmasıyla yerine getirirse, genel kaynağın yerini adlandırılmış kaynak alır.</span><span class="sxs-lookup"><span data-stu-id="8cf2d-110">After the request is fulfilled by the resource manager, the generic resource will be replaced by a named resource if the resource manager fulfills the request with the booking of a named resource.</span></span> <span data-ttu-id="8cf2d-111">Aksi takdirde, genel kaynak takım üzerinde kalır ve kaynak yöneticisi adlandırılmış bir kaynak önermişse istek durumu **İnceleme Gerekiyor** olarak değişir.</span><span class="sxs-lookup"><span data-stu-id="8cf2d-111">Otherwise, the generic resource will remain on the team and the request status will change to **Needs Review** , if the resource manager has proposed a named resource.</span></span>
