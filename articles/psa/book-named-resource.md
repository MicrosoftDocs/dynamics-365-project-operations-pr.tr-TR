---
title: Kaynak gereksinimlerinden adlandırılmış kaynakları ayırma
description: Bu konu, genel bir kaynak gereksinimi için adlandırılmış kaynakları ayırma hakkında bilgi sağlar.
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
ms.openlocfilehash: c7a6370bde434b74d05e342240abd9bba84d34d8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145136"
---
# <a name="book-named-resources-from-resource-requirements"></a><span data-ttu-id="aefd2-103">Kaynak gereksinimlerinden adlandırılmış kaynakları ayırma</span><span class="sxs-lookup"><span data-stu-id="aefd2-103">Book named resources from resource requirements</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="aefd2-104">Kaynak gereksinimi olan genel kaynağı değiştirmek için adlandırılmış bir kaynak kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aefd2-104">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="aefd2-105">Project Service Automation'da (PSA) **Projeler** sayfasında **Takım** sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aefd2-105">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab.</span></span>
2. <span data-ttu-id="aefd2-106">Listeden kaynak gereksinimi olan genel kaynağı seçin ve ardından **Ayır**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aefd2-106">Select the generic resource that has a resource requirement from the list and then click **Book**.</span></span> <span data-ttu-id="aefd2-107">Veya, kaynak gereksinimini açıp **Ayır**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aefd2-107">Or, open the resource requirement and then click **Book**.</span></span>


![Genel takım üyesi ayırma](media/RM-how-to-14.png)


3. <span data-ttu-id="aefd2-109">**Zamanlama Yardımcısı** sayfasında, proje takımınıza ayırmak için adlandırılmış bir kaynak seçin ve ardından **Ayır**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aefd2-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then click **Book**.</span></span>

![Zamanlama yardımcısını kullanarak genel takım üyesi ayırma](media/RM-how-to-15.png)

<span data-ttu-id="aefd2-111">Ayırma işlemi tamamlandığında ve bir adlandırılmış kaynak tarafından gerçekleştirildiğinde, genel kaynak adlandırılan kaynakla değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="aefd2-111">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

![Genel takım üyesinin yerine geçen adlandırılmış takım üyesi](media/RM-how-to-16.png)

<span data-ttu-id="aefd2-113">Zamanlamadaki atamalar da adlandırılan kaynakla güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="aefd2-113">The assignments on the schedule are updated with the named resource as well.</span></span>

![Proje görevlerine atanan adlandırılmış takım üyesi](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="aefd2-115">Bir genel kaynağı birden çok adlandırılmış kaynakla karşılama</span><span class="sxs-lookup"><span data-stu-id="aefd2-115">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="aefd2-116">Bir genel kaynak için bir gereksinimin birden çok adlandırılmış kaynakla karşılama, tek bir adlandırılmış kaynak atamaya benzerdir.</span><span class="sxs-lookup"><span data-stu-id="aefd2-116">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="aefd2-117">Örneğin, süresi beş gün olan ve 120 saat çalışma gerektiren bir görev var.</span><span class="sxs-lookup"><span data-stu-id="aefd2-117">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="aefd2-118">Bu görev, haftasa beş gün günde sekiz saat çalışan bir kaynakla tamamlanamaz.</span><span class="sxs-lookup"><span data-stu-id="aefd2-118">This task can't be completed by one resource that works a typical eight-hour day over a five day week.</span></span> 

![Beş gün boyunca 120 saatlik çalışma gerektiren bir görev](media/RM-how-to-21.png)

<span data-ttu-id="aefd2-120">Gereksinim beş gün boyunca 120 saat robotik mühendisliği içindir, bu da günde 24 saat çalışma gerektirir.</span><span class="sxs-lookup"><span data-stu-id="aefd2-120">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

![Günlük gereksinim](media/RM-how-to-22.png)

<span data-ttu-id="aefd2-122">Bu, genel bir kaynak isteğini yerine getirmek için birden çok adlandırılmış kaynağın gerekli olduğu durum için bir örnektir.</span><span class="sxs-lookup"><span data-stu-id="aefd2-122">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="aefd2-123">Gereksinimi karşılamak için birden fazla kaynak ayırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="aefd2-123">You will need to book multiple resources to fulfill the requirement.</span></span>

![Gereksinimi karşılamak için birden fazla kaynak ayırma](media/RM-how-to-23.png)

<span data-ttu-id="aefd2-125">Bu senaryodaki ana fark genel kaynağın göreve atanan takımda kalması ve ayrılan adlandırılmış kaynak takım üyelerinin pozisyonun parçası olarak atanmamasıdır.</span><span class="sxs-lookup"><span data-stu-id="aefd2-125">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="aefd2-126">Proje yöneticisi, işi gerektiği gibi adlandırılmış kaynaklara atayabilir.</span><span class="sxs-lookup"><span data-stu-id="aefd2-126">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="aefd2-127">**Mutabakat** görünümü, proje yöneticisinin ayırmaları birden çok görev ataması için birden çok kaynak arasında bölmesine yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="aefd2-127">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="aefd2-128">Gereksinim oluşturan bir görev paketinizin olduğu ve proje yöneticisinin bunu atamak isteme amacının tahmin edilmesinin gerektiği gibi yukarıdaki basit örnekten daha karmaşık senaryolar olabileceğinden bu otomatik olarak gerçekleştirilmez.</span><span class="sxs-lookup"><span data-stu-id="aefd2-128">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement, the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="aefd2-129">Sistem amacı anlayamadığından varsayımlar amaçlanandan farklı olabilir ve yanlış veya öngörülemeyen sonuçlara yol açabilir.</span><span class="sxs-lookup"><span data-stu-id="aefd2-129">Because the system can't understand intent, chances are that the assumptions will be different than intended and an incorrect or unpredictable result will happen.</span></span> <span data-ttu-id="aefd2-130">Öngörülebilir sonuç, proje yöneticisi **Mutabakat** görünümünü kullanarak kaynakları bilerek oluşturana kadar genel kaynağın atanmış kalmasıdır.</span><span class="sxs-lookup"><span data-stu-id="aefd2-130">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>


