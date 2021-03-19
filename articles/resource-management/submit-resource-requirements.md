---
title: Kaynak isteği gönderme
description: Oluşturulmuş bir kaynak gereksinimini bir kaynak isteği olarak gönderebilirsiniz. İstek daha sonra yerine getirilmesi için bir kaynak yöneticisine gönderilir.
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: bc97af1ec90e60417c502eb329a85004e769e05b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279162"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="374cd-104">Kaynak isteği gönderme</span><span class="sxs-lookup"><span data-stu-id="374cd-104">Submit a resource request</span></span>

<span data-ttu-id="374cd-105">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="374cd-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="374cd-106">Oluşturulmuş bir kaynak gereksinimini bir kaynak isteği olarak gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="374cd-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="374cd-107">İstek daha sonra yerine getirilmesi için bir kaynak yöneticisine gönderilir.</span><span class="sxs-lookup"><span data-stu-id="374cd-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="374cd-108">Dynamics 365 Project Operations'ta, **Projeler** sayfasında ayrılabilir kaynakların listesini görüntülemek için **Takım** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="374cd-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="374cd-109">Listeden kaynak gereksinimi olan genel kaynağı seçin ve ardından **İstek Gönder**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="374cd-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="374cd-110">Genel takım üyesinin istek durumu **Gönderildi** olarak değişir.</span><span class="sxs-lookup"><span data-stu-id="374cd-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="374cd-111">İstek yerine getirildikten sonra kaynak yöneticisi, isteği adlandırılmış bir kaynağı ayırarak yerine getirirse genel kaynağın yerini adlandırılmış kaynak alır.</span><span class="sxs-lookup"><span data-stu-id="374cd-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="374cd-112">Aksi takdirde, kaynak yöneticisi adlandırılmış bir kaynak önerirse genel kaynak, takımda kalır ve istek durumu **İnceleme Gerekiyor** olarak değişir.</span><span class="sxs-lookup"><span data-stu-id="374cd-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]