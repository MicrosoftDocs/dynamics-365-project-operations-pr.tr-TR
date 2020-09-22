---
title: Web uygulamasında göreve nasıl ayrılabilir kaynak atarım?
description: Kullanılabilir kaynakları atayabileceğiniz yöntemlere genel bakış.
author: JohnPBurrows
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 2.x on platform version 9.x
ms.assetid: 9db35b39-8dfc-4989-9160-fd841fe0ae5a
ms.author: john.burrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 521ea73c948619816d3cd06d72140fcc85366397
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756732"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="4512c-103">Web uygulamasında (Project Service uygulaması v2.x) bir göreve nasıl bir ayrılabilir kaynak atayabilirim?</span><span class="sxs-lookup"><span data-stu-id="4512c-103">How do I assign a bookable resource to a task in the web app (Project Service app v2.x)?</span></span>

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="4512c-104">Project Service'te bir göreve kaynak atamak için iki yol vardır.</span><span class="sxs-lookup"><span data-stu-id="4512c-104">There are two ways to assign a resource to a task in Project Service.</span></span> <span data-ttu-id="4512c-105">Bir kaynağı bir takım üyesi olarak ayırabilir ve ardından bir göreve atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4512c-105">You can book a resource as a team member and then assign it to a task.</span></span> <span data-ttu-id="4512c-106">Veya görevlerde rol atamayla genel bir takım üyesi oluşturabilir, bir takım kurabilir ve adlandırılmış bir kaynakla, destekleyici gereksinimleri karşılayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4512c-106">Or, you can create a generic team member through role assignment on tasks, generate a team, and then fulfill the backing requirements with a named resource.</span></span>

<span data-ttu-id="4512c-107">Bir göreve bir ayrılabilir kaynak atamak istiyorsanız, ayrılabilir kaynak takım üyesinin yeterli kullanılabilir ayırmalara sahip olması gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="4512c-107">Note that if you’d like to assign a bookable resource to a task, the bookable resource team member must have enough available bookings.</span></span> <span data-ttu-id="4512c-108">Ayırmanın durumu Kesin Ayırma ve taahhüt türü Taahhüt Edildi olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4512c-108">The status of the booking must be Commit Type Hard Book and Status Committed.</span></span> <span data-ttu-id="4512c-109">Kaynak için yeterli ayırma yoksa, Project Service atamayı kaldırır ve aşağıdaki hata iletisini görüntüler:</span><span class="sxs-lookup"><span data-stu-id="4512c-109">If there aren’t enough bookings for the resource, Project Service removes the assignment and displays the following error message:</span></span>

<span data-ttu-id="4512c-110">*Göreve kaynak atanamıyor - Aşağıdaki kaynakta veya kaynaklarda proje için yeterli saat ayrılmamış*</span><span class="sxs-lookup"><span data-stu-id="4512c-110">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project*</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="4512c-111">Bir kaynağı bir takım üyesi olarak ayırın ve ardından kaynağı bir göreve atayın.</span><span class="sxs-lookup"><span data-stu-id="4512c-111">Book a resource as a team member and then assign the resource to a task</span></span>

<span data-ttu-id="4512c-112">Bu yöntemle bir kaynağı proje takımına ekler ve ardından proje zamanlamasındaki kaynağa görevler atarsınız.</span><span class="sxs-lookup"><span data-stu-id="4512c-112">With this method you add a resource to the project team and then assign tasks to the resource in the project schedule.</span></span> <span data-ttu-id="4512c-113">Bunu aşağıda belirtildiği şekilde yapabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="4512c-113">Here’s how you do this:</span></span>
1.  <span data-ttu-id="4512c-114">Takım üyesi kılavuzunda **Yeni**'yi seçerek yeni bir takım üyesi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="4512c-114">On the team member grid, add a new team member by selecting **New**.</span></span>
2.  <span data-ttu-id="4512c-115">Takım Üyesi Hızlı Oluştur ekranında, ayrılabilir kaynağın adını seçin ve rol ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="4512c-115">On the Team Member Quick Create screen, select the bookable resource name and set a role.</span></span>
3.  <span data-ttu-id="4512c-116">**Başlangıç** ve **Bitiş** tarihlerini seçin.</span><span class="sxs-lookup"><span data-stu-id="4512c-116">Select the **From** and **To** dates.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="4512c-117">![Takım üyesi ekleme ekran görüntüsü](media/FAQ-Resources-to-Tasks2-1.png "Takım üyesi ekleme ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="4512c-117">![Screenshot of adding team member](media/FAQ-Resources-to-Tasks2-1.png "Screenshot of adding team member")</span></span>
 
4.  <span data-ttu-id="4512c-118">Kaynak ayırma için aşağıdaki tahsisat yöntemlerinden birini seçin:</span><span class="sxs-lookup"><span data-stu-id="4512c-118">Select one of the following allocation methods for booking the resource:</span></span>
    - <span data-ttu-id="4512c-119">**Tam Kapasite**, belirtilen başlangıç ve bitiş tarihleri için kaynağın tam kapasitesini ayırır.</span><span class="sxs-lookup"><span data-stu-id="4512c-119">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="4512c-120">**Yüzde Kapasite**, belirtilen başlangıç ve bitiş tarihleri için kaynak kapasitesinin bir yüzdesini ayırır.</span><span class="sxs-lookup"><span data-stu-id="4512c-120">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="4512c-121">**Saatlere Göre - Eşit Dağıt**, kaynağı, belirtilen sayıda saatler için ayırır ve belirtilen başlangıç ve bitiş tarihleri arasında her güne eşit olarak dağıtır.</span><span class="sxs-lookup"><span data-stu-id="4512c-121">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing it evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="4512c-122">**Saatlere Göre - Ön Yük**, kaynağı, belirtilen sayıda saatler için ayırır ve günlük saat sayısını, belirtilen başlangıç ve bitiş tarihleri arasında ön yükler.</span><span class="sxs-lookup"><span data-stu-id="4512c-122">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>

    <span data-ttu-id="4512c-123">**Hiçbiri** seçeneğini belirtmeyin çünkü kaynağı takıma ekler ancak kaynağın kapasitesini kullanan herhangi bir ayırma oluşturmaz.</span><span class="sxs-lookup"><span data-stu-id="4512c-123">Don’t select **None** because it adds the resource to the team but doesn’t create any bookings that absorb the resource's capacity.</span></span>
5.  <span data-ttu-id="4512c-124">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4512c-124">Select **Save**.</span></span>

    <span data-ttu-id="4512c-125">Ayırmada, bu kaynağı atadığınız görevlerin tarih aralığını ve çalışılması gereken saat sayısını kapsayacak kadar saat olması gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="4512c-125">Note that the hours of the booking must be enough to cover the effort hours and date ranges of the tasks that you assign this resource to.</span></span> <span data-ttu-id="4512c-126">Bu değerler örtüşmüyorsa, kaynağı göreve atayamazsınız.</span><span class="sxs-lookup"><span data-stu-id="4512c-126">If they aren’t in alignment, you can’t assign the resource to the task.</span></span>

6.  <span data-ttu-id="4512c-127">Görevin iş kırılım yapısında (İKY), kaynak hücresinin açılan listesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4512c-127">On the work breakdown structure (WBS) for the task, click the resource cell dropdown.</span></span> <span data-ttu-id="4512c-128">Bunun ardından:</span><span class="sxs-lookup"><span data-stu-id="4512c-128">Then:</span></span> 

    1. <span data-ttu-id="4512c-129">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4512c-129">Select **Add**.</span></span>
    2. <span data-ttu-id="4512c-130">**Kaynaklar** altındaki açılan listeyi ve bu listeden, yukarıda eklediğiniz takım üyesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4512c-130">Select the dropdown under **Resources** and select the team member you added above.</span></span>
    3. <span data-ttu-id="4512c-131">**Tamam** seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="4512c-131">Select **OK**.</span></span> <span data-ttu-id="4512c-132">Takım üyesi göreve atanır.</span><span class="sxs-lookup"><span data-stu-id="4512c-132">The team member is now assigned to the task.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="4512c-133">![İKY ile kaynak ekleme ekran görüntüsü](media/FAQ-Resources-to-Tasks2-2.png "İKY ile kaynak ekleme ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="4512c-133">![Screenshot of adding resources with WBS](media/FAQ-Resources-to-Tasks2-2.png "Screenshot of adding resources with WBS")</span></span>
 
<span data-ttu-id="4512c-134">Takım üyesi ızgarasında, Atanan Saat Sayısı altında kaynağın atanmış toplam saat sayısını göreceksiniz.</span><span class="sxs-lookup"><span data-stu-id="4512c-134">On the team member grid, you’ll see the aggregate of the resource’s assigned hours under Assigned Hours.</span></span> <span data-ttu-id="4512c-135">Bu değer, kaynak için ayrılan saat sayısından az veya ona eşit olacaktır.</span><span class="sxs-lookup"><span data-stu-id="4512c-135">It will be less than or equal to the booked hours for the resource.</span></span> 

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="4512c-136">![Kaynak için atanan saat sayısı ekran görüntüsü](media/FAQ-Resources-to-Tasks2-3.png "Kaynak için atanan saat sayısı ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="4512c-136">![Screenshot of assigned hours for a resource](media/FAQ-Resources-to-Tasks2-3.png "Screenshot of assigned hours for a resource")</span></span>
 
<span data-ttu-id="4512c-137">Kaynağa atamaya çalıştığınız görev kaynak ayırmalarının bitiş tarihinden sonra başlıyorsa, kaynak açılan listede görünmez.</span><span class="sxs-lookup"><span data-stu-id="4512c-137">If the task you’re attempting to assign to the resource starts after the end date of the resources bookings, the resource won’t appear in the dropdown.</span></span>

<span data-ttu-id="4512c-138">Kaynakta atanmamış kapasite kaldıysa, ayrılan saat sayısından daha fazla saat sayısına bir kaynak atayabileceğinizi unutmayın.</span><span class="sxs-lookup"><span data-stu-id="4512c-138">Note that you can assign a resource to more hours than their booked hours if the resource has some remaining unassigned capacity.</span></span> <span data-ttu-id="4512c-139">Bu durumda kaynak, kısmen atanmış (yalnızca ayırmaları kadar) bir kaynak olacaktır.</span><span class="sxs-lookup"><span data-stu-id="4512c-139">In this case the resource will only be partially assigned up to their bookings.</span></span> <span data-ttu-id="4512c-140">İş kırılım yapısına Personelsiz Saatler sütununu ekleyerek, kalan atanmamış görev saati sayısını görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4512c-140">You can see these remaining unassigned task hours by adding the Unstaffed Hours column to the work breakdown structure.</span></span>

<span data-ttu-id="4512c-141">Kaynaklar ayrılmış saat sayısına atanırsa (ayrılan saat sayısı, atanan saat sayısına eşitse), bunları başka görevlere atamaya çalıştığınız zaman aşağıdaki hata iletisini görürsünüz:</span><span class="sxs-lookup"><span data-stu-id="4512c-141">If resources are assigned to their booked hours (their booked hours equals their assigned hours), you’ll see the following error message when you attempt to assign them further tasks:</span></span>

<span data-ttu-id="4512c-142">*Göreve kaynak atanamıyor - Aşağıdaki kaynakta veya kaynaklarda proje için yeterli saat ayrılmamış.*</span><span class="sxs-lookup"><span data-stu-id="4512c-142">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project.*</span></span>

<span data-ttu-id="4512c-143">Buna ek olarak, projeyi oluşturduğunuz sırada, takıma eklenen varsayılan proje yöneticisi takım üyesi hiç ayırma olmadan eklenir ve herhangi bir göreve atanamaz.</span><span class="sxs-lookup"><span data-stu-id="4512c-143">Additionally, the default project manager team member that is added to the team when you create the project is added without any bookings and can’t be assigned to any task.</span></span> <span data-ttu-id="4512c-144">Bunlar görevler için kaynak açılan listesinde görünmez.</span><span class="sxs-lookup"><span data-stu-id="4512c-144">They won’t show up in the resource dropdown for tasks.</span></span>

<span data-ttu-id="4512c-145">Bu kaynağı atamak isterseniz, takımdan kaldırıp, Hiçbiri dışındaki bir tahsisat yöntemiyle yeniden eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="4512c-145">If you want to assign this resource, you need to remove them from the team and then re-add them with an allocation method other than None.</span></span> <span data-ttu-id="4512c-146">Proje oluşturulurken bunların takıma eklenme nedeni, projede varsayılan olarak en az bir proje onaylayanı bulunmasını sağlamaktır.</span><span class="sxs-lookup"><span data-stu-id="4512c-146">The reason they’re added to the team when the project is created is so that a project has at least one project approver by default.</span></span>

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a><span data-ttu-id="4512c-147">Görevlerde rol atamayla genel bir takım üyesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="4512c-147">Create a generic team member through role assignment on tasks</span></span>

<span data-ttu-id="4512c-148">Bu yöntem, görevler için kaynaklarda yeterli ayırma olmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="4512c-148">This method assures that resources have enough bookings for tasks.</span></span> <span data-ttu-id="4512c-149">Önce, rolleri görevlere atadıktan sonra bir takım oluşturarak, görevlerde nihai olarak çalışmasını istediğiniz adlandırılmış kaynağın temel özelliklerini açıklayan bir yer tutucu veya genel kaynak oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4512c-149">First, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks by generating a team after assigning roles to tasks.</span></span> <span data-ttu-id="4512c-150">Bunu aşağıda belirtildiği şekilde yapabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="4512c-150">Here’s how you do this:</span></span>

1. <span data-ttu-id="4512c-151">İş kırılım yapısında bir görev seçin.</span><span class="sxs-lookup"><span data-stu-id="4512c-151">On the work breakdown structure, select a task.</span></span>
2. <span data-ttu-id="4512c-152">Kaynak hücresindeki **Atanan Rol** açılan liste simgesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4512c-152">Select the **Assigned Role** dropdown icon in the resource cell.</span></span>
3. <span data-ttu-id="4512c-153">**Rol** açılan listesini ve ardından, genel kaynak için rolü seçin.</span><span class="sxs-lookup"><span data-stu-id="4512c-153">Select the **Role** dropdown and select the role for the generic resource.</span></span>
4. <span data-ttu-id="4512c-154">**Tamam** seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="4512c-154">Select **OK**.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="4512c-155">![Kaynak eklemek için İKY kullanma ekran görüntüsü](media/FAQ-Resources-to-Tasks2-4.png "Kaynak eklemek için İKY kullanma ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="4512c-155">![Screenshot of using WBS to add resource](media/FAQ-Resources-to-Tasks2-4.png "Screenshot of using WBS to add resource")</span></span>
 
<span data-ttu-id="4512c-156">İKY'de görevlere rolleri atama işleminizi tamamladıktan sonra **Proje Takımı Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="4512c-156">Once you’ve completed assigning roles to the tasks in the WBS, select **Generate Project Team**.</span></span> <span data-ttu-id="4512c-157">Project Service, görev atamalarını toplayarak rollere, kaynak belirleme kuruluş birimlerine ve proje takvimine göre en az sayıda genel takım üyesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4512c-157">Project Service creates the minimum number of generic team members based on the roles, resourcing organization units, and project calendar by aggregating the task assignments.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="4512c-158">![Proje takımı oluşturma ekran görüntüsü](media/FAQ-Resources-to-Tasks2-5.png "Proje takımı oluşturma ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="4512c-158">![Screenshot of generating project team](media/FAQ-Resources-to-Tasks2-5.png "Screenshot of generating project team")</span></span>
 
<span data-ttu-id="4512c-159">Takım Üyesi kılavuzunda, Genel Kaynak türündeki kaynakları rol ve konum adıyla görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="4512c-159">On the Team Member grid, you’ll see resources of the Generic Resource type with the role and position name.</span></span> <span data-ttu-id="4512c-160">İşi tamamlamak için bir role iki kaynak gerekiyorsa, Takım Oluştur özelliği iki takım üyesi oluşturur ve ikisini ayırt etmek için pozisyon adı kullanır.</span><span class="sxs-lookup"><span data-stu-id="4512c-160">If two resources are needed for a role to complete the work, the Generate Team feature creates two team members and uses position name to set them apart.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="4512c-161">![İki genel kaynak ekleme ekran görüntüsü](media/FAQ-Resources-to-Tasks2-6.png "İki genel kaynak ekleme ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="4512c-161">![Screenshot of adding two generic resources](media/FAQ-Resources-to-Tasks2-6.png "Screenshot of adding two generic resources")</span></span>
 
<span data-ttu-id="4512c-162">Genel takım üyesi için destekleyici kaynak gereksinimini, Kaynak Gereksinimi altındaki bağlantıyı seçerek açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4512c-162">You can open the backing resource requirement for the generic team member by selecting the link under Resource Requirement.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="4512c-163">![Destekleyici kaynak gereksinimi açma ekran görüntüsü](media/FAQ-Resources-to-Tasks2-7.png "Destekleyici kaynak gereksinimi açma ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="4512c-163">![Screenshot of opening backing resource requirement](media/FAQ-Resources-to-Tasks2-7.png "Screenshot of opening backing resource requirement")</span></span>

<span data-ttu-id="4512c-164">Genel kaynak için **Ayır**'ı seçtikten sonra, zamanlama panosunu kullanarak gerçek bir kaynak bulup ayırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4512c-164">Select **Book** for the generic resource, and then you can use the schedule board to find and book a real resource.</span></span> <span data-ttu-id="4512c-165">Ayrıca, gereksinimi, bir kaynak yöneticisi tarafından karşılanması için **İsteği Gönder**'i seçerek gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4512c-165">You can also submit the requirement for fulfillment by a resource manager by selecting **Submit Request**.</span></span>

<span data-ttu-id="4512c-166">Genel kaynak, adlandırılmış bir kaynakla karşılandığı zaman, genel kaynak takımdan kaldırılır ve genel kaynağın görev atamaları, genel kaynağın kaynak gereksinimini karşılayan adlandırılmış kaynağa atanır.</span><span class="sxs-lookup"><span data-stu-id="4512c-166">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>
 

