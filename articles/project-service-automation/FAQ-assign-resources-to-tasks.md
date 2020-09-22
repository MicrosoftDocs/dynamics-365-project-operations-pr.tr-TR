---
title: Göreve kaynak atama
description: Bu konu, görevlere kaynak atama hakkında bilgi sağlar.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
ms.topic: article
ms.prod: Project Service
ms.technology: Dynamics 365 Project Service Automation 3.x
ms.assetid: 3ea9516c-0276-4e30-b308-f792f64d608b
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 509f7a4464b2e810900b31a78219ba696192a18b
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756737"
---
# <a name="assign-a-resource-to-a-task"></a><span data-ttu-id="aa161-103">Göreve kaynak atama</span><span class="sxs-lookup"><span data-stu-id="aa161-103">Assign a resource to a task</span></span>

<span data-ttu-id="aa161-104">Microsoft Dynamics 365 Project Service Automation'ta bir göreve kaynak atamak için üç yol vardır.</span><span class="sxs-lookup"><span data-stu-id="aa161-104">There are three ways to assign a resource to a task in Microsoft Dynamics 365 Project Service Automation.</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="aa161-105">Bir kaynağı bir takım üyesi olarak ayırın ve ardından kaynağı bir göreve atayın.</span><span class="sxs-lookup"><span data-stu-id="aa161-105">Book a resource as a team member, and then assign the resource to a task</span></span>

<span data-ttu-id="aa161-106">Bir kaynağı proje takımına ekleyebilir ve ardından kaynağı proje zamanlamasındaki görevlere atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aa161-106">You can add a resource to the project team, and then assign the resource to tasks in the project schedule.</span></span>

1. <span data-ttu-id="aa161-107">**Takım üyesi** sekmesinde **Yeni**'yi seçerek yeni bir takım üyesi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="aa161-107">On the **Team Member** tab, add a new team member by selecting **New**.</span></span> 

2. <span data-ttu-id="aa161-108">Ayrılabilir kaynağın adını seçip bir rol ayarlayabileceğiniz **Takım Üyesi Hızlı Oluştur** panelini açılır.</span><span class="sxs-lookup"><span data-stu-id="aa161-108">The **Team Member Quick Create** panel opens, where you can select the bookable resource name and set a role.</span></span> 

    <span data-ttu-id="aa161-109">Kaynak ayırma için aşağıdaki tahsisat yöntemlerinden birini seçin:</span><span class="sxs-lookup"><span data-stu-id="aa161-109">Select one of the following allocation methods for the resource’s booking:</span></span>

    - <span data-ttu-id="aa161-110">**Tam Kapasite**, belirtilen başlangıç ve bitiş tarihleri için kaynağın tam kapasitesini ayırır.</span><span class="sxs-lookup"><span data-stu-id="aa161-110">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="aa161-111">**Yüzde Kapasite**, belirtilen başlangıç ve bitiş tarihleri için kaynak kapasitesinin bir yüzdesini ayırır.</span><span class="sxs-lookup"><span data-stu-id="aa161-111">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="aa161-112">**Saatlere Göre - Eşit Dağıt**, kaynağı, belirtilen sayıda saatler için ayırır ve belirtilen başlangıç ve bitiş tarihleri arasında her güne eşit olarak dağıtır.</span><span class="sxs-lookup"><span data-stu-id="aa161-112">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing them evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="aa161-113">**Saatlere Göre - Ön Yük**, kaynağı, belirtilen sayıda saatler için ayırır ve günlük saat sayısını, belirtilen başlangıç ve bitiş tarihleri arasında ön yükler.</span><span class="sxs-lookup"><span data-stu-id="aa161-113">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>
    - <span data-ttu-id="aa161-114">**Hiçbiri**, kaynağı takıma ekler ancak kaynağın kapasitesini kullanan herhangi bir ayırma oluşturmaz.</span><span class="sxs-lookup"><span data-stu-id="aa161-114">**None** adds the resource to the team but doesn’t create any bookings that absorb their capacity.</span></span>

3. <span data-ttu-id="aa161-115">Bir görevin **Zamanlama** kılavuzunda, kaynak hücresindeki **Kaynak** simgesini ve ardından **Takım Üyeleri** altından az önce eklediğiniz takım üyesini seçin.</span><span class="sxs-lookup"><span data-stu-id="aa161-115">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell, and then under **Team Members**, select the team member you just added.</span></span> 

> [!NOTE]
> <span data-ttu-id="aa161-116">**Takım Üyesi** ve **Mutabakat** sekmelerinde kaynak ayrılan ve atanan saatleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="aa161-116">On the **Team Member** and **Reconciliation** tabs, the resource shows booked and assigned hours.</span></span> <span data-ttu-id="aa161-117">Saatlerin aynı olması gerekir ama ayırmalar ve atamalar gibi kesin bir şekilde eşleştirilmiş olmaları gerekmez.</span><span class="sxs-lookup"><span data-stu-id="aa161-117">The hours should be the same, but it isn't required as bookings and assignments are not tightly coupled.</span></span> <span data-ttu-id="aa161-118">**Mutabakat** sekmesi, bunlar farklı olduğu zaman (örneğin, kaynağa, ayırdığınız saat sayısından daha fazla saat sayısı atadığınız zaman) size ayrıntıları verir.</span><span class="sxs-lookup"><span data-stu-id="aa161-118">The **Reconciliation** tab gives you details when they are different, such as when you assign a resource more hours than you have booked.</span></span> <span data-ttu-id="aa161-119">Gerekirse, kaynağın ayırmalarını artırarak veya atamayı değiştirerek bilgileri düzeltebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aa161-119">If needed, you can correct the information by extending the resource's bookings or changing the assignment.</span></span>

## <a name="create-a-generic-team-member-through-task-assignment"></a><span data-ttu-id="aa161-120">Görev atamayla genel bir takım üyesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="aa161-120">Create a generic team member through task assignment</span></span>

<span data-ttu-id="aa161-121">Görev atama aracılığıyla genel bir takım üyesi oluşturduğunuzda, görevlerde nihai olarak çalışmasını istediğiniz adlandırılmış kaynağın temel özelliklerini açıklayan bir yer tutucu veya genel kaynak oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aa161-121">When you create a generic team member through task assignment, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks.</span></span> <span data-ttu-id="aa161-122">Bunun ardından, adlandırılmış kaynağı aramak ve ayırmak için kullanılan bir gereksinim oluşturursunuz (veya gereksinimi kullanma isteği gönderirsiniz).</span><span class="sxs-lookup"><span data-stu-id="aa161-122">You then generate a requirement (or submit a request using the requirement) that is used to search for and book the named resource.</span></span>

1. <span data-ttu-id="aa161-123">Görevin **Zamanlama** kılavuzunda, kaynak hücresindeki **Kaynak** simgesini seçin.</span><span class="sxs-lookup"><span data-stu-id="aa161-123">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="aa161-124">Yer tutucu kaynağın adı olarak işlev görecek bir ad yazın.</span><span class="sxs-lookup"><span data-stu-id="aa161-124">Type a name to serve as the placeholder resource’s name.</span></span> <span data-ttu-id="aa161-125">Örneğin, Program Yöneticisi.</span><span class="sxs-lookup"><span data-stu-id="aa161-125">For example, Program Manager.</span></span>

3. <span data-ttu-id="aa161-126">**Oluştur**'u seçin ve **Proje Takımı Üyesi Hızlı Oluştur** alanında, genel kaynak için rolü ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="aa161-126">Select **Create**, and in the **Quick Create Project Team Member** field, set the role for the generic resource.</span></span>

4. <span data-ttu-id="aa161-127">Görevin **Kaynak Seçicisinde** kaynağı seçerek, bu yer tutucu kaynağa görevler atamaya devam edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aa161-127">You can continue to assign tasks to this placeholder resource by selecting the resource on the **Resource Selector** for the task.</span></span> <span data-ttu-id="aa161-128">Bunlar **Takım Üyeleri** altında listelenir.</span><span class="sxs-lookup"><span data-stu-id="aa161-128">They’re listed under **Team Members**.</span></span>

5. <span data-ttu-id="aa161-129">Genel kaynak atamayı tamamladıktan sonra, **Takım** sekmesinde genel kaynağı seçin ve **Gereksinim Oluştur**'u seçerek, genel kaynak için bir kaynak gereksinimi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="aa161-129">When you’re done assigning the generic resource, select the generic resource on the **Team** tab, and then select **Generate Requirement** to create a resource requirement for the generic resource.</span></span>

6. <span data-ttu-id="aa161-130">Genel kaynak için **Ayır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="aa161-130">Select **Book** for the generic resource.</span></span> <span data-ttu-id="aa161-131">Bunun ardından, gerçek bir kaynağı bulmak ve ayırmak için Zamanlama panosunu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aa161-131">You can then use the Schedule board to find and book a real resource.</span></span> <span data-ttu-id="aa161-132">Ayrıca, gereksinimi, bir kaynak yöneticisi tarafından karşılanması için gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aa161-132">You can also submit the requirement for fulfillment by a resource manager.</span></span>

7. <span data-ttu-id="aa161-133">Genel kaynak, adlandırılmış bir kaynakla karşılandığı zaman, genel kaynak takımdan kaldırılır ve genel kaynağın görev atamaları, genel kaynağın kaynak gereksinimini karşılayan adlandırılmış kaynağa atanır.</span><span class="sxs-lookup"><span data-stu-id="aa161-133">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a><span data-ttu-id="aa161-134">Tüm ayrılabilir kaynaklar listesinden, adlandırılmış bir kaynak atama</span><span class="sxs-lookup"><span data-stu-id="aa161-134">Assign a named resource from the list of all bookable resources</span></span>

<span data-ttu-id="aa161-135">Tüm ayrılabilir kaynakları arayıp bir göreve atamak için **Kaynak Seçicideki** arama kutusunu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aa161-135">You can use the search box in the **Resource Selector** to search all bookable resources and assign them to a task.</span></span>

<span data-ttu-id="aa161-136">Bu şekilde atanan kaynaklar, herhangi bir ayırma olmadan takıma eklenir.</span><span class="sxs-lookup"><span data-stu-id="aa161-136">Resources assigned this way are added to the team without any bookings.</span></span> <span data-ttu-id="aa161-137">Bu, takım üyesi eklenmesine ve tahsisat yöntemi olarak Hiçbirini seçmeye benzer.</span><span class="sxs-lookup"><span data-stu-id="aa161-137">This is similar to adding a team member and selecting None as the allocation method.</span></span> <span data-ttu-id="aa161-138">Kaynak **Takım** sekmesinde ve **Mutabakat** sekmesinde yalnızca atamaları ve ayırma eksiği olan kaynaklar olarak görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="aa161-138">The resource is displayed in the **Team** and **Reconciliation** tabs as resources with only assignments and a booking deficit.</span></span> <span data-ttu-id="aa161-139">Kullanılmalarını istiyorsanız, bunları ayırın.</span><span class="sxs-lookup"><span data-stu-id="aa161-139">Book them if you want to use their availability.</span></span>

1. <span data-ttu-id="aa161-140">Görevin **Zamanlama** kılavuzunda, kaynak hücresindeki **Kaynak** simgesini seçin.</span><span class="sxs-lookup"><span data-stu-id="aa161-140">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="aa161-141">Bir ad yazmaya başlayın.</span><span class="sxs-lookup"><span data-stu-id="aa161-141">Start typing a name.</span></span> <span data-ttu-id="aa161-142">Ad için arama sonuçları, **Diğer Kaynaklar** altındaki **Kaynak Seçicide** görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="aa161-142">The search results for the name are displayed in the **Resource Selector** under **Other Resources**.</span></span>

3. <span data-ttu-id="aa161-143">Göreve atamak istediğiniz kaynağı seçin.</span><span class="sxs-lookup"><span data-stu-id="aa161-143">Select the resource that you want to assign to the task.</span></span>

