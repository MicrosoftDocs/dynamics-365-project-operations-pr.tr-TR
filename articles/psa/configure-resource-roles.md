---
title: Kaynak rollerini yapılandır
description: Project Service'ta kaynak rollerini yapılandırma
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 0b573bec395217e105cc8d9c669343e37ff6662e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129162"
---
# <a name="configure-resource-roles-project-service"></a><span data-ttu-id="64f40-103">Kaynak rollerini yapılandırma (Project Service)</span><span class="sxs-lookup"><span data-stu-id="64f40-103">Configure resource roles (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="64f40-104">Roller, proje kaynak gereksinimlerini veya bir projenin maliyetlerini belirlerken proje planlamasında önemli bir rol oynarlar.</span><span class="sxs-lookup"><span data-stu-id="64f40-104">Roles play an important part in project planning, when determining resource requirements or costs of a project.</span></span> <span data-ttu-id="64f40-105">Projelerinizin gerektirdiği her rol için, söz konusu role kaynak rolü oluşturmanız ve beceri ve uzmanlıklar ilişkilendirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="64f40-105">For each role your projects require, you need to create a resource role and associate skills and proficiencies to that role.</span></span> <span data-ttu-id="64f40-106">Örneğin geliştirici, proje yöneticisi veya oyun sınayıcı için roller oluşturmak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="64f40-106">For example, you might want to create roles for developer, project manager, or game tester.</span></span> <span data-ttu-id="64f40-107">Ayrıca, rol için gerekli beceri ve uzmanlık düzeylerini ayarlarsınız.</span><span class="sxs-lookup"><span data-stu-id="64f40-107">You’ll also set the skills and proficiency levels required for the role.</span></span>  
  
 <span data-ttu-id="64f40-108">Kuruluşunuz için etkin proje tahmini sağlamak üzere kaynak roller yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="64f40-108">Configure resource roles to ensure effective project estimation for your organization.</span></span>  <span data-ttu-id="64f40-109">Ayrıca, faturalama türünü doğru şekilde ayarladığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="64f40-109">Also make sure you accurately set the billing type.</span></span> <span data-ttu-id="64f40-110">Borçlandırılamayan bir ödeme türüne sahip bir öğe kümesi, sözleşme veya teklif satırlarında gösterilmez.</span><span class="sxs-lookup"><span data-stu-id="64f40-110">An item set with a non-chargeable billing type doesn’t show up on contract or quote lines.</span></span>  
  
 <span data-ttu-id="64f40-111">Kaynak rollerini ayarladıktan sonra, fiyat listesine sahip maliyet ve satış fiyatları ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="64f40-111">Once you’ve set up resource roles, you can set up cost and sales prices with a price list.</span></span>  
  
 <span data-ttu-id="64f40-112">Eklemek istediğiniz her rol için aşağıdakileri yapın:</span><span class="sxs-lookup"><span data-stu-id="64f40-112">For each role you want to add, do the following:</span></span>  
  
1.  <span data-ttu-id="64f40-113">**Project Service > Kaynak Rolleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="64f40-113">Go to **Project Service > Resource Roles**.</span></span>  
  
2.  <span data-ttu-id="64f40-114">**Yeni** düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="64f40-114">Click **New**.</span></span>  
  
3.  <span data-ttu-id="64f40-115">**Genel** alanındaki **Ad** alanında rol için bir ad girin ve ardından diğer alanları gerektiği şekilde doldurun.</span><span class="sxs-lookup"><span data-stu-id="64f40-115">In the **General** area, enter a name for the role in **Name**, and then fill in the other fields as necessary.</span></span>  
  
4.  <span data-ttu-id="64f40-116">Düzenlemeye devam edebilmeniz için kaydı oluşturmak üzere **Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="64f40-116">Click **Save** to create the record so you can continue editing it.</span></span>  
  
5.  <span data-ttu-id="64f40-117">**Beceriler** alanında, beceri eklemek için **+** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="64f40-117">In the **Skills** area, click **+** to add a skill.</span></span>  
  
6.  <span data-ttu-id="64f40-118">**Rol uzmanlığı gereksinimi** bölmesinde, **Beceri** alanına tıklayın, **Ara** düğmesine tıklayın ve ardından bir beceri seçin.</span><span class="sxs-lookup"><span data-stu-id="64f40-118">In the **Role competency requirement** pane, click in the **Skill** field, click the **Search** button, and then select a skill.</span></span>  
  
7.  <span data-ttu-id="64f40-119">Bu yetenek için bir uzmanlık seçin ve ardından **Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="64f40-119">Select a proficiency for that skill, and then click **Save**.</span></span>  
  
8.  <span data-ttu-id="64f40-120">Gerekirse beceri eklemeye devam edin.</span><span class="sxs-lookup"><span data-stu-id="64f40-120">Continue adding skills as necessary.</span></span> <span data-ttu-id="64f40-121">Bitirdiğinizde, ekranın sağ alt köşesindeki **Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="64f40-121">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
9. <span data-ttu-id="64f40-122">Bu kaynak rolünün kullanılacak projeler için kullanılabilir yapmak üzere **Etkinleştir**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="64f40-122">To make this resource role available for projects to use, click **Activate**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="64f40-123">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="64f40-123">See Also</span></span>  
 [<span data-ttu-id="64f40-124">Kaynakları ayarlama</span><span class="sxs-lookup"><span data-stu-id="64f40-124">Set up resources</span></span>](../psa/set-up-resources.md)
