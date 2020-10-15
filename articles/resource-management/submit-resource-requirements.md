---
title: Kaynak isteği gönderme
description: Oluşturulmuş bir kaynak gereksinimini bir kaynak isteği olarak gönderebilirsiniz. İstek daha sonra yerine getirilmesi için bir kaynak yöneticisine gönderilir.
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 94cf0f0d88e9be2522936b45122ed0037434d4f3
ms.sourcegitcommit: 2cf93d8bf0be5b61a739195a41334c34d910e9ba
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961756"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="537a7-104">Kaynak isteği gönderme</span><span class="sxs-lookup"><span data-stu-id="537a7-104">Submit a resource request</span></span>

<span data-ttu-id="537a7-105">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="537a7-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="537a7-106">Oluşturulmuş bir kaynak gereksinimini bir kaynak isteği olarak gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="537a7-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="537a7-107">İstek daha sonra yerine getirilmesi için bir kaynak yöneticisine gönderilir.</span><span class="sxs-lookup"><span data-stu-id="537a7-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="537a7-108">Dynamics 365 Project Operations'ta, **Projeler** sayfasında ayrılabilir kaynakların listesini görüntülemek için **Takım** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="537a7-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="537a7-109">Listeden kaynak gereksinimi olan genel kaynağı seçin ve ardından **İstek Gönder**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="537a7-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="537a7-110">Genel takım üyesinin istek durumu **Gönderildi** olarak değişir.</span><span class="sxs-lookup"><span data-stu-id="537a7-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="537a7-111">İstek yerine getirildikten sonra kaynak yöneticisi, isteği adlandırılmış bir kaynağı ayırarak yerine getirirse genel kaynağın yerini adlandırılmış kaynak alır.</span><span class="sxs-lookup"><span data-stu-id="537a7-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="537a7-112">Aksi takdirde, kaynak yöneticisi adlandırılmış bir kaynak önerirse genel kaynak, takımda kalır ve istek durumu **İnceleme Gerekiyor** olarak değişir.</span><span class="sxs-lookup"><span data-stu-id="537a7-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>
