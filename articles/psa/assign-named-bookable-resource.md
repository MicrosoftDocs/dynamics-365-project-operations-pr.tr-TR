---
title: Proje takımına adlandırılmış ayrılabilir kaynaklar ayırma ve görevler atama
description: Bu konuda, proje takımlarına adlandırılmış kaynaklar ayırma ve bunları görevlere atama hakkında bilgiler sağlanmaktadır.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: 6169f2bdc107e63d666fb32d34f531fd5d472c2f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291463"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a><span data-ttu-id="0a730-103">Proje takımına adlandırılmış ayrılabilir kaynaklar ayırma ve görevler atama</span><span class="sxs-lookup"><span data-stu-id="0a730-103">Book named bookable resources to a project team and assign tasks</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="0a730-104">Bir adlandırılmış kaynağı proje ekibinize doğrudan takım üzerinde ayırarak ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0a730-104">You can  add a named resource to your project team by booking them directly onto the team.</span></span> <span data-ttu-id="0a730-105">Bunu yapmak için aşağıdaki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="0a730-105">To do this, complete the following steps.</span></span>

1. <span data-ttu-id="0a730-106">Project Service Automation'da, **Projeler**'e gidin ve ayırma yaptığınız projeyi seçerek açın.</span><span class="sxs-lookup"><span data-stu-id="0a730-106">In  Project Service Automation, go to **Projects**, and select the open the project that you are booking for.</span></span>
2. <span data-ttu-id="0a730-107">**Proje** sayfasında, **Takım** sekmesinde, **Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0a730-107">On the **Project** page, on the **Team** tab, click **New**.</span></span> 

![Takım sekmesinden bir takım üyesi ekleme](media/RM-how-to-1.png)

3. <span data-ttu-id="0a730-109">**Proje Takım Üyesi Hızlı Oluştur** iletişim kutusunda, ayrılabilir kaynağı seçin.</span><span class="sxs-lookup"><span data-stu-id="0a730-109">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="0a730-110">**Rol** alanı, atanmış olan varsa kaynağın varsayılan rolüyle doldurulur.</span><span class="sxs-lookup"><span data-stu-id="0a730-110">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="0a730-111">Gerekirse rolü değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0a730-111">You can change the role if needed.</span></span> 
4. <span data-ttu-id="0a730-112">Kaynağın gerekli olduğu başlangıç ve bitiş tarihlerini seçin ve kaynağın kapasitesinin tahsisat yöntemini seçin.</span><span class="sxs-lookup"><span data-stu-id="0a730-112">Select the from and to dates that the resource will be needed and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="0a730-113">Takım üyesinin bir proje onaylayanı olmasını istiyorsanız, **Proje Onaylayanı** alanında **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0a730-113">If you want the team member to be a project approver, select **Yes** in the **Project Approver** field.</span></span> <span data-ttu-id="0a730-114">Bu, takım üyesinin bu projeye ait gönderilen zaman ve gider girişlerini onaylayabileceği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="0a730-114">This will mean that the team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="0a730-115">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0a730-115">Click **Save**.</span></span>

![Hızlı oluştur formunda takım üyesi ekleme](media/RM-how-to-2.png)


<span data-ttu-id="0a730-117">Artık, ayrılan kaynağı projedeki görevlere atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0a730-117">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="0a730-118">**Proje** sayfasında, görevleri yeni kaynağa atamak için **Zamanlama** sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0a730-118">On the **Project** page, click the **Schedule** tab to assign tasks to the new resource.</span></span> <span data-ttu-id="0a730-119">Görev kılavuzundaki **Kaynaklar** alanından başlatılan kaynak seçici, seçebileceğiniz takım üyelerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="0a730-119">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>

![Zamanlama sekmesindeki bir göreve takım üyesi atama](media/RM-how-to-3.png)

<span data-ttu-id="0a730-121">Project Service Automation (PSA) sürüm 3'te, kaynak ayırmaları ve görev atamaları sıkı bir şekilde eşitlenmez.</span><span class="sxs-lookup"><span data-stu-id="0a730-121">In version 3 for Project Service Automation (PSA), resource bookings and task assignments are not tightly coupled.</span></span> <span data-ttu-id="0a730-122">Bu, zamanlamadaki kaynak seçiciyi kullandığınızda, proje üzerinde bulunan rezervasyon kapasitelerinden daha fazla saat için görevleri ekip üyelerine atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0a730-122">This means that when you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>
<span data-ttu-id="0a730-123">Takım üyesi ayırmaları ve atamaları arasındaki farkları **Takım** sekmesinde veya **Kaynak Mutabakatı** sekmesinde görebilirsiniz. Ayrıca, kaynaklar için ayırmalar ve atamalar arasındaki farklılıkları daha ayrıntılı bir düzeyde mutabık kılabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0a730-123">You can see the differences between team member bookings and assignments on the **Team** tab or on the **Resource Reconciliation** tab. You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

![Kaynak mutabakatı sekmesi](media/RM-how-to-4.png)

<span data-ttu-id="0a730-125">**Zamanlama** sekmesindeki kaynak seçiciyi proje takımının parçası olmayan ayrılabilir kaynakları aramak ve seçmek için de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0a730-125">You can also use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="0a730-126">Bunlar, kaynak seçicide **Diğer Kaynaklar** olarak gösterilir.</span><span class="sxs-lookup"><span data-stu-id="0a730-126">These are shown in the resource picker as **Other Resources**.</span></span>

![Bir göreve takım dışı üye kaynağı atama](media/RM-how-to-5.png)

<span data-ttu-id="0a730-128">Bunu yaptığınızda, kaynak proje takımına eklenir ve göreve atanır, ancak herhangi bir ayırma oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="0a730-128">When you do this, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

![Atamaları olan ancak ayırmaları olmayan takım üyesi](media/RM-how-to-6.png)

<span data-ttu-id="0a730-130">Kaynağın kapasitesini projeye ayırmak için **Mutabakat** sekmesinin ayırmayı uzatma özelliğini veya **Zamanlama Panosu**'nu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0a730-130">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

![Kaynak mutabakatı sekmesinde bir takım üyesi için ayırmaları uzatma](media/RM-how-to-7.png)

<span data-ttu-id="0a730-132">Bir takım üyesi projenize ayrıldıktan sonra, ayırmaları doğrudan yönetmek için ayırmaları sürdür özelliğini veya Zamanlama Panosunu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0a730-132">After a team member is booked on your project, you can use maintain bookings or use the Schedule Board directly to manage their bookings.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]