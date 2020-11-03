---
title: Kaynak yönetimi modlarına genel bakış
description: Bu konuda, Dynamics 365 Project Operations içindeki Kaynak yönetimi özellikleri hakkında bilgiler sağlanmaktadır.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4a8e605109e48b50da68abeee989f8ac8d3d659c
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086212"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="18c95-103">Kaynak yönetimi modlarına genel bakış</span><span class="sxs-lookup"><span data-stu-id="18c95-103">Resource management modes overview</span></span>

<span data-ttu-id="18c95-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="18c95-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="18c95-105">Dynamics 365 Project Operations genel ayırma akışını yürütebilmenizi sağlayan iki modu destekler.</span><span class="sxs-lookup"><span data-stu-id="18c95-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="18c95-106">Yönetim modu, proje parametresi olarak tanımlanır ve işinizde değişiklik gerekiyorsa değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="18c95-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="18c95-107">Merkezi mod</span><span class="sxs-lookup"><span data-stu-id="18c95-107">Central mode</span></span>
<span data-ttu-id="18c95-108">Merkezi mod, kaynakların projelere tahsisatını merkezileştiren kuruluşlara Proje yöneticilerinin proje düzeyinde kaynak gereksinimlerini tanımlayabilmesini sağlamak için bir yol sunar.</span><span class="sxs-lookup"><span data-stu-id="18c95-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="18c95-109">Kaynak gereksinimlerinin yerine getirilmesi görevi Kaynak yöneticisine verilir.</span><span class="sxs-lookup"><span data-stu-id="18c95-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="18c95-110">Proje yöneticileri, Kaynak yöneticisinin önerdiği kaynakları kabul edebilir veya reddedebilir.</span><span class="sxs-lookup"><span data-stu-id="18c95-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![Merkezi Mod](./media/resource-management-central.png)

<span data-ttu-id="18c95-112">Merkezi modda kaynakları yönetmek için bkz:</span><span class="sxs-lookup"><span data-stu-id="18c95-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="18c95-113">Göreve genel ayrılabilir kaynaklar atama ve kaynak gereksinimleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="18c95-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="18c95-114">Kaynak gereksinimlerinden adlandırılmış kaynaklar ayırma</span><span class="sxs-lookup"><span data-stu-id="18c95-114">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="18c95-115">Kaynak isteği gönderme</span><span class="sxs-lookup"><span data-stu-id="18c95-115">Submit a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="18c95-116">Kaynak isteğini karşılama</span><span class="sxs-lookup"><span data-stu-id="18c95-116">Fulfill a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="18c95-117">Kaynak isteğinden bir önerilen proje kaynağını kabul etme veya reddetme</span><span class="sxs-lookup"><span data-stu-id="18c95-117">Accept or reject a proposed project resource from a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="18c95-118">Karma mod</span><span class="sxs-lookup"><span data-stu-id="18c95-118">Hybrid mode</span></span>
<span data-ttu-id="18c95-119">Karma mod, kaynakların tahsisatında esneklik isteyen kuruluşlarda Proje yöneticilerinin ve Kaynak yöneticilerinin kaynakları ayırabilmelerini sağlar.</span><span class="sxs-lookup"><span data-stu-id="18c95-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![Karma Mod](./media/resource-management-hybrid.png)

<span data-ttu-id="18c95-121">Desteklenen Merkezi mod işlemine ek olarak, Karma modda desteklenen diğer tüm ayırma akışlarını yönetmek için aşağıdaki konulara bakın:</span><span class="sxs-lookup"><span data-stu-id="18c95-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="18c95-122">Kaynağı doğrudan bir projeye ayırma:</span><span class="sxs-lookup"><span data-stu-id="18c95-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="18c95-123">Proje takımına adlandırılmış ayrılabilir kaynaklar ayırma ve görevler atama</span><span class="sxs-lookup"><span data-stu-id="18c95-123">Book named bookable resources to a project team and assign tasks</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="18c95-124">Kaynak gereksinimden bir kaynak ayırma:</span><span class="sxs-lookup"><span data-stu-id="18c95-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="18c95-125">Göreve genel ayrılabilir kaynaklar atama ve kaynak gereksinimleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="18c95-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="18c95-126">Kaynak gereksinimlerinden adlandırılmış kaynaklar ayırma</span><span class="sxs-lookup"><span data-stu-id="18c95-126">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)