---
title: Bir görev veya proje ekibine genel ayrılabilir kaynaklar atama
description: Bu konu görevlere ve proje takımlarına genel kaynaklar ayırma hakkında bilgi sağlar.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: 5b4c47513b96310745fd2cdb296988a57df0e966
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291418"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a><span data-ttu-id="b454e-103">Göreve genel ayrılabilir kaynaklar atama ve kaynak gereksinimleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="b454e-103">Assign generic bookable resources to a task and generate resource requirements</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="b454e-104">Projenize adlandırılmış veya gerçek kaynakları atamanın ve ayırmanın yanı sıra, proje görevlerine genel kaynaklar atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b454e-104">In addition to booking and assigning named or real resources to your project, you can assign generic resources to project tasks.</span></span> <span data-ttu-id="b454e-105">Bu kaynaklar, projenize adlandırılmış kaynaklarla personel atamak için hazır oluncaya kadar adlandırılmış kaynaklar için yer tutucu olarak hizmet verebilir.</span><span class="sxs-lookup"><span data-stu-id="b454e-105">These resources can serve as placeholders for named resources until you are ready to staff your project with named resources.</span></span> 

1. <span data-ttu-id="b454e-106">Project Service Automation'da (PSA) **Proje** sayfasını açın ve **Zamanla** sekmesinde, zamanlamanın **kaynak** hücresine genel kaynağın pozisyon adını girin.</span><span class="sxs-lookup"><span data-stu-id="b454e-106">In Project Service Automation (PSA), open the **Project** page and on the **Schedule** tab, enter the position name of the generic resource in the **Resource** cell of the schedule.</span></span> <span data-ttu-id="b454e-107">Veya kaynak seçiciyi açmak için **Kaynak** simgesine tıklayın ve ardından oluşturmak istediğiniz genel kaynağın adını girin.</span><span class="sxs-lookup"><span data-stu-id="b454e-107">Or, click the **Resource** icon in the cell to open the resource picker and then enter the name of the generic resource that you want to create.</span></span>

![Bir genel takım üyesi oluşturma ve atama](media/RM-how-to-9.png)

<span data-ttu-id="b454e-109">Bu, **Hızlı Oluştur: Proje Ekibi Üyesi** panelini açar.</span><span class="sxs-lookup"><span data-stu-id="b454e-109">This will open the **Quick Create: Project Team Member** panel.</span></span> 

2. <span data-ttu-id="b454e-110">Genel kaynak ekibi üyesinin rolünü ve kuruluş birimini girin ve ardından **Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b454e-110">Enter the role and organization unit of the generic resource team member and then click **Save**.</span></span>

![Genel takım üyesi hızlı oluşturma](media/RM-how-to-10.png)

3. <span data-ttu-id="b454e-112">Yeni genel kaynak ekibi üyesi oluşturulduktan sonra, göreve atanır.</span><span class="sxs-lookup"><span data-stu-id="b454e-112">After you have created the new generic resource team member, it is assigned to the task.</span></span> <span data-ttu-id="b454e-113">Bu genel kaynağı görev zamanlamasında diğer görevlere atamaya devam edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b454e-113">You can continue to assign that generic resource to other tasks in the task schedule.</span></span>

![Varolan genel takım üyesini görevlere atama](media/RM-how-to-11.png)

4. <span data-ttu-id="b454e-115">Genel kaynağı atandıktan sonra, bir kaynak gereksinimi oluşturabilir ve bir kaynak yöneticisine doğrudan kaynak isteği ayırarak veya göndererek bunu gerçekleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b454e-115">After you have assigned the generic resource, you can generate a resource requirement and fulfill it by directly booking or submitting a resource request to a resource manager.</span></span>

![Genel takım üyesi için gereksinim oluşturma](media/RM-how-to-12.png)

<span data-ttu-id="b454e-117">Takım üyesi ızgarasında, yukarıda bahsedildiği gibi kaynak seçiciyi kullanmanın yanı sıra genel kaynakları doğrudan ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b454e-117">On the team member grid, in addition to being able to use the resource picker as mentioned above, you can add generic resources directly.</span></span> <span data-ttu-id="b454e-118">Kaynaklar, **Hızlı OLuştur: Proje Ekibi Üyesi** panelinde belirtilen başlangıç/bitiş tarihlerini ve tahsisat yöntemini temel alan bir kaynak gereksinimiyle eklenir.</span><span class="sxs-lookup"><span data-stu-id="b454e-118">The resources are added with a resource requirement that is based on the start/end dates and allocation method specified in the **Quick Create: Project Team Member** panel.</span></span>

<span data-ttu-id="b454e-119">Genel takım üyesini doğrudan ekleyip daha sonra genel kaynağa karşılaması gereken saaten daha fazla görev atarsanız bir fark görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b454e-119">You can see a difference if you add the generic team member directly and then assign more tasks to the generic resource than they have required hours to cover.</span></span> <span data-ttu-id="b454e-120">Gerekli saatleri atamalarla dengelemek için gereksinimi yeniden oluşturmak üzere **Gereksinim Oluştur**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b454e-120">Click **Generate Requirement** to regenerate the requirement to balance the required hours against assignments.</span></span>

<span data-ttu-id="b454e-121">Gereksinimi açmak ve beceriler, tercih edilen kaynaklar, vb. eklemek için takım kılavuzundaki **Kaynak gereksinimi** bağlantısına da tıklayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b454e-121">You can also click the **Resource requirement** link in the team grid to open the requirement and add skills, preferred resources, etc.</span></span>

![Kaynak gereksinimi](media/RM-how-to-13.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]