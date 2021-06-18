---
title: Kaynak yönetimi temel kavramları
description: Bu konuda, Microsoft Dynamics Project Operations içindeki kaynak yönetimi özellikleri hakkında bilgiler sağlanmaktadır.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 6362daab7e2e01c7b7b2c2b801fe7e258b21ef16
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001000"
---
# <a name="resource-management-key-concepts"></a><span data-ttu-id="be3ac-103">Kaynak yönetimi temel kavramları</span><span class="sxs-lookup"><span data-stu-id="be3ac-103">Resource management key concepts</span></span>

<span data-ttu-id="be3ac-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="be3ac-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="be3ac-105">Kaynaklar, servis tabanlı bir kuruluşun en önemli varlığıdır.</span><span class="sxs-lookup"><span data-stu-id="be3ac-105">Resources are the most important asset of a service-based organization.</span></span> <span data-ttu-id="be3ac-106">Doğru kaynakları doğru zamanda bulma, bu kaynakları projelere ayırma ve bunların kullanılmalarını sağlama yetenekleri; kuruluşun gelir ve müşteri memnuniyeti hedeflerine ulaşmasına yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="be3ac-106">The ability to find the right resources at the right time, book those resources on projects and keep them utilized, helps the organization meet revenue targets and customer satisfaction goals.</span></span> <span data-ttu-id="be3ac-107">Aşağıdaki görevleri yapmak için Dynamics 365 Project Operations'ta proje kaynak belirlemesi işlevini kullanabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="be3ac-107">You can use the project resourcing functionality in Dynamics 365 Project Operations to do the following tasks:</span></span>

- <span data-ttu-id="be3ac-108">Uygun ve nitelikli kaynaklar ayırarak proje takımları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="be3ac-108">Form project teams by booking available and qualified resources.</span></span>
- <span data-ttu-id="be3ac-109">Genel takım üyesi kayıtları oluşturun ve rolleriyle kaynak kuruluş birimini tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="be3ac-109">Create generic team member records and define their roles and resource organization unit.</span></span>
- <span data-ttu-id="be3ac-110">Genel takım üyeleri için görev atamalarından kaynak gereksinimleri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="be3ac-110">Generate resource requirements for generic team members from their task assignments.</span></span>
- <span data-ttu-id="be3ac-111">Kaynak talebinde tanımlanan becerileri belirleyerek kullanılabilir kaynak becerileriyle eşleştirin.</span><span class="sxs-lookup"><span data-stu-id="be3ac-111">Match skills by identifying the skills defined on the resource demand against available resource skills.</span></span>
- <span data-ttu-id="be3ac-112">İkame kaynaklar.</span><span class="sxs-lookup"><span data-stu-id="be3ac-112">Substitute resources.</span></span>
- <span data-ttu-id="be3ac-113">Proje zamanlama atamalarını ve kaynak ayırmalarını hizalayın.</span><span class="sxs-lookup"><span data-stu-id="be3ac-113">Align project schedule assignments and resource bookings.</span></span>
- <span data-ttu-id="be3ac-114">Ayırmalar ve atamalar arasındaki farklarda mutabakat sağlayın.</span><span class="sxs-lookup"><span data-stu-id="be3ac-114">Reconcile differences in bookings and assignments.</span></span>
- <span data-ttu-id="be3ac-115">Ofis dışında durumuna yanıt olarak kaynak ayırmalarını değiştirin.</span><span class="sxs-lookup"><span data-stu-id="be3ac-115">Change resource bookings in response to out-of-office status.</span></span>
- <span data-ttu-id="be3ac-116">Proje ve kaynak yöneticileri arasında iş birliği sağlayın.</span><span class="sxs-lookup"><span data-stu-id="be3ac-116">Collaborate between project managers and resource managers.</span></span>
- <span data-ttu-id="be3ac-117">Kaynakların kullanım sürelerini açıklayan bir döküm de dahil olmak üzere hedefe yönelik kaynak kullanım geçmişini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="be3ac-117">View the history of resource utilization against a target, including a breakdown of how the resources' time was utilized.</span></span>
- <span data-ttu-id="be3ac-118">Beceri ve uzmanlık deposu bulundurun.</span><span class="sxs-lookup"><span data-stu-id="be3ac-118">Maintain a skills and proficiency repository.</span></span>


<span data-ttu-id="be3ac-119">Projenize, Project Operations'ta genel veya adlandırılmış bir kaynak takımı ile personel ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="be3ac-119">You can staff your project with a team of generic or named resources in Project Operations.</span></span> <span data-ttu-id="be3ac-120">Takım üyeleri ekleyip atamak ve takım üyelerinin ayırma ve atamalarını yönetmek için çeşitli yöntemler kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="be3ac-120">You can use various methods to add and assign team members and to manage their bookings and assignments.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]