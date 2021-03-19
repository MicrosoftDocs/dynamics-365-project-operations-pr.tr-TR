---
title: Takım üyelerini koruma
description: Bu konuda, proje takımlarına adlandırılmış kaynaklar ayırma ve bunları görevlere atama hakkında bilgiler sağlanmaktadır.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 60b6788d881518502d314e9ee5daf6bbc0ae8764
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286857"
---
# <a name="maintain-team-members"></a><span data-ttu-id="7d398-103">Takım üyelerini koruma</span><span class="sxs-lookup"><span data-stu-id="7d398-103">Maintain team members</span></span>

<span data-ttu-id="7d398-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="7d398-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7d398-105">Doğrudan takıma ayırarak proje takımınıza adlandırılmış bir kaynak ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7d398-105">You can add a named resource to your project team by booking them directly to the team.</span></span>

1. <span data-ttu-id="7d398-106">Dynamics 365 Project Operations'ta, **Projeler**'e gidin ve ayırdığınız projeyi seçip açın.</span><span class="sxs-lookup"><span data-stu-id="7d398-106">In Dynamics 365 Project Operations, go to **Projects**, and select the open the project that you're booking for.</span></span>
2. <span data-ttu-id="7d398-107">**Proje** sayfasında, **Takım** sekmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7d398-107">On the **Project** page, on the **Team** tab, select **New**.</span></span> 
3. <span data-ttu-id="7d398-108">**Proje Takım Üyesi Hızlı Oluştur** iletişim kutusunda, ayrılabilir kaynağı seçin.</span><span class="sxs-lookup"><span data-stu-id="7d398-108">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="7d398-109">**Rol** alanı, atanmış olan varsa kaynağın varsayılan rolüyle doldurulur.</span><span class="sxs-lookup"><span data-stu-id="7d398-109">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="7d398-110">Rolü değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7d398-110">You can change the role.</span></span> 
4. <span data-ttu-id="7d398-111">Kaynağın gerekli olduğu başlangıç ve bitiş tarihlerini seçin ve kaynağın kapasitesinin tahsisat yöntemini seçin.</span><span class="sxs-lookup"><span data-stu-id="7d398-111">Select the from and to dates that the resource will be needed, and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="7d398-112">Takım üyesinin bir proje onaylayanı olmasını istiyorsanız **Proje Onaylayanı** alanında **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7d398-112">In the **Project Approver** field, select **Yes** if you want the team member to be a project approver.</span></span> <span data-ttu-id="7d398-113">Takım üyesi bu projeye ait gönderilen zaman ve gider girişlerini onaylayabilir.</span><span class="sxs-lookup"><span data-stu-id="7d398-113">The team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="7d398-114">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7d398-114">Select **Save**.</span></span>

<span data-ttu-id="7d398-115">Artık, ayrılan kaynağı projedeki görevlere atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7d398-115">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="7d398-116">**Proje** sayfasındaki **Zamanlama** sekmesinde görevleri yeni kaynağa atayın.</span><span class="sxs-lookup"><span data-stu-id="7d398-116">On the **Project** page, on the **Schedule** tab, assign tasks to the new resource.</span></span> <span data-ttu-id="7d398-117">Görev kılavuzundaki **Kaynaklar** alanından başlatılan kaynak seçici, seçebileceğiniz takım üyelerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="7d398-117">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>


<span data-ttu-id="7d398-118">Project Operations'ta, kaynak ayırmaları ve görev atamaları kesin bir şekilde eşleştirilmez.</span><span class="sxs-lookup"><span data-stu-id="7d398-118">In Project Operations, resource bookings and task assignments aren't tightly coupled.</span></span> <span data-ttu-id="7d398-119">Zamanlamadaki kaynak seçiciyi kullandığınızda proje üzerinde bulunan ayırmaların kapasitelerinden daha fazla saat için takım üyelerine görevler atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7d398-119">When you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>

<span data-ttu-id="7d398-120">Takım üyesi ayırmaları ve atamalar arasındaki farklar **Takım** ve **Kaynak Mutabakatı** sekmelerinde gösterilir.</span><span class="sxs-lookup"><span data-stu-id="7d398-120">The differences between team member bookings and assignments are shown on the **Team** and **Resource Reconciliation** tabs.</span></span> <span data-ttu-id="7d398-121">Ayrıca kaynaklar için ayırmalar ve atamalar arasındaki farkları daha ayrıntılı bir düzeyde de mutabık kılabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7d398-121">You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

<span data-ttu-id="7d398-122">**Zamanlama** sekmesindeki kaynak seçiciyi proje takımının parçası olmayan ayrılabilir kaynakları aramak ve seçmek için kullanın.</span><span class="sxs-lookup"><span data-stu-id="7d398-122">Use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="7d398-123">Bu kaynaklar, kaynak seçicide **Diğer Kaynaklar** olarak gösterilir.</span><span class="sxs-lookup"><span data-stu-id="7d398-123">These resources are shown in the resource picker as **Other Resources**.</span></span>

<span data-ttu-id="7d398-124">Seçim yaptığınızda kaynak, proje takımına eklenir ve göreve atanır ancak herhangi bir ayırma oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="7d398-124">When you make a selection, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

<span data-ttu-id="7d398-125">Kaynağın kapasitesini projeye ayırmak için **Mutabakat** sekmesinin ayırmayı uzatma özelliğini veya **Zamanlama Panosu**'nu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7d398-125">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

<span data-ttu-id="7d398-126">Takım üyesi, projenize ayrıldıktan sonra ayırmalarını doğrudan yönetmek için **Ayırmaları koruma**'yı veya **Zamanlama Panosu**'nu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7d398-126">After a team member is booked on your project, you can use **Maintain bookings** or the **Schedule Board** directly to manage their bookings.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]