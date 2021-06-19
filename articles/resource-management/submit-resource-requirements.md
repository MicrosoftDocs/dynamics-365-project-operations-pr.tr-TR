---
title: Kaynak isteği gönderme
description: Oluşturulmuş bir kaynak gereksinimini bir kaynak isteği olarak gönderebilirsiniz. İstek daha sonra yerine getirilmesi için bir kaynak yöneticisine gönderilir.
author: ruhercul
ms.date: 10/04/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 6ac0044a27d1e506c9c62c477014017fd0ca06cb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014050"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="c94fd-104">Kaynak isteği gönderme</span><span class="sxs-lookup"><span data-stu-id="c94fd-104">Submit a resource request</span></span>

<span data-ttu-id="c94fd-105">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="c94fd-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c94fd-106">Oluşturulmuş bir kaynak gereksinimini bir kaynak isteği olarak gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c94fd-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="c94fd-107">İstek daha sonra yerine getirilmesi için bir kaynak yöneticisine gönderilir.</span><span class="sxs-lookup"><span data-stu-id="c94fd-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="c94fd-108">Dynamics 365 Project Operations'ta, **Projeler** sayfasında ayrılabilir kaynakların listesini görüntülemek için **Takım** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c94fd-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="c94fd-109">Listeden kaynak gereksinimi olan genel kaynağı seçin ve ardından **İstek Gönder**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c94fd-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="c94fd-110">Genel takım üyesinin istek durumu **Gönderildi** olarak değişir.</span><span class="sxs-lookup"><span data-stu-id="c94fd-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="c94fd-111">İstek yerine getirildikten sonra kaynak yöneticisi, isteği adlandırılmış bir kaynağı ayırarak yerine getirirse genel kaynağın yerini adlandırılmış kaynak alır.</span><span class="sxs-lookup"><span data-stu-id="c94fd-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="c94fd-112">Aksi takdirde, kaynak yöneticisi adlandırılmış bir kaynak önerirse genel kaynak, takımda kalır ve istek durumu **İnceleme Gerekiyor** olarak değişir.</span><span class="sxs-lookup"><span data-stu-id="c94fd-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]