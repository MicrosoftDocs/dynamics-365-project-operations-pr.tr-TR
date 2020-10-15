---
title: Saat dilimlerini yönetme
description: Proje oluşturulduğunda projenin saat dilimi, uygulanan çalışma saati şablonunda tanımlanan saat dilimini temel alır.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 27f58f0dacc3404119a719547ad374629c740740
ms.sourcegitcommit: 396e0fea2f1598a5313cb0128eca4fe0bb5aade9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961966"
---
# <a name="manage-time-zones"></a><span data-ttu-id="2df29-103">Saat dilimlerini yönetme</span><span class="sxs-lookup"><span data-stu-id="2df29-103">Manage time zones</span></span>

<span data-ttu-id="2df29-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="2df29-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


## <a name="projects"></a><span data-ttu-id="2df29-105">Projeler</span><span class="sxs-lookup"><span data-stu-id="2df29-105">Projects</span></span>

<span data-ttu-id="2df29-106">Proje oluşturulduğunda saat dilimi, uygulanan çalışma saati şablonunda tanımlanan saat dilimini temel alır.</span><span class="sxs-lookup"><span data-stu-id="2df29-106">When a project is created, the time zone is based on the time zone defined in the applied work hour template.</span></span> <span data-ttu-id="2df29-107">**Proje**'de tarihler, **Görev** sekmesi dışındaki tüm sekmelerde her zaman oturum açan kullanıcının saat dilimine göredir. İş kırılım yapısını görüntülediğinizde, tarihler her zaman, projenin saat diliminde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="2df29-107">On the **Project** for, the dates are always relative to the time zone of the user that is logged in on each tab, except the **Task** tab. When you view the work breakdown structure, the dates will always be displayed in the project’s time zone.</span></span>

## <a name="tasks"></a><span data-ttu-id="2df29-108">Görevler</span><span class="sxs-lookup"><span data-stu-id="2df29-108">Tasks</span></span>

<span data-ttu-id="2df29-109">Görev oluşturulduğunda başlangıç saati, bitiş saati ve saat/gün değerleri projenin çalışma saatleri tarafından denetlenir.</span><span class="sxs-lookup"><span data-stu-id="2df29-109">When a task is created, the start time, end time, and hours/day is controlled by the working hours of the project.</span></span> <span data-ttu-id="2df29-110">Örneğin, saat dilimi -8 PST olan bir projeyle bir görev oluşturulursa ve bu projenin çalışma saatleri Pazartesiden Cumaya 09:00 ile 17:00 arasındaysa atama yapılmadan oluşturulan herhangi bir görev, proje takviminin başlangıç ve bitiş saatlerine uyacaktır.</span><span class="sxs-lookup"><span data-stu-id="2df29-110">For example, if a task is created with a project whose time zone is -8 PST and has the following working hours: 9:00 AM to 5:00 PM Monday to Friday, any task created without an assignment will respect the start time and end time of the project calendar.</span></span>

## <a name="manage-resources-with-time-zones"></a><span data-ttu-id="2df29-111">Kaynakları saat dilimleriyle yönetme</span><span class="sxs-lookup"><span data-stu-id="2df29-111">Manage resources with time zones</span></span>

<span data-ttu-id="2df29-112">**Ayırmayı Genişlet**özelliğini kullanılırken doğru ve tahmin edilebilir sonuçlar elde etmek için karşılanması gereken iki temel önkoşul vardır:</span><span class="sxs-lookup"><span data-stu-id="2df29-112">For accurate and predictable results when using **Extend Booking**, there are two key prerequisites that must be met:</span></span>  

- <span data-ttu-id="2df29-113">Kullanıcı, cihazının saat dilimini sistemin **Kişiselleştirme Ayarları**'nda tanımlanan zaman dilimiyle eşleşecek şekilde yapılandırmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2df29-113">The user must configure their device's time zone to match the time zone defined in the system's **Personalization Settings**.</span></span>
 
  ![Windows 10'da saat dilimi ayarları](media/reconcile-assignments-03.png)

  ![Kişiselleştirme ayarlarındaki saat dilimi ayarları](media/reconcile-assignments-04.png)
 
- <span data-ttu-id="2df29-116">Ayrılabilir kaynak, istenen genişletmeyi tanımlamak için kullanılan sınırlarla çakışan en az bir dakikalık çalışma zamanı içermelidir.</span><span class="sxs-lookup"><span data-stu-id="2df29-116">The bookable resource must have at least one minute of working time that overlaps with the contours that are used to define the requested extension.</span></span> <span data-ttu-id="2df29-117">Örneğin, çalışma saatlerinin 09:00 ile 19:00 arasında olduğu aşağıdaki kaynaklar.</span><span class="sxs-lookup"><span data-stu-id="2df29-117">For example, the following resources with working hours that fall between 9:00 AM and 7:00 PM.</span></span> 

  ![Kaynak sınırlarını karşılaştırma](media/reconcile-assignments-05.png)

<span data-ttu-id="2df29-119">Aşağıdaki tabloda şunlar gösterilmektedir:</span><span class="sxs-lookup"><span data-stu-id="2df29-119">The following table shows:</span></span>

- <span data-ttu-id="2df29-120">Proje takvimi şablonu</span><span class="sxs-lookup"><span data-stu-id="2df29-120">A project calendar template</span></span>
- <span data-ttu-id="2df29-121">Kaynak A: Bu kaynak projeyle aynı takvime sahiptir ve aynı saat diliminde yer alır.</span><span class="sxs-lookup"><span data-stu-id="2df29-121">Resource A: This resource has the same calendar and is in the same time zone as the project.</span></span> <span data-ttu-id="2df29-122">Ayırmanın başlangıç saati 09:00 olarak görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="2df29-122">The start time of the bookings will be 9:00 AM.</span></span>
- <span data-ttu-id="2df29-123">Kaynak B: Bu kaynak, projeden farklı bir saat diliminde bulunur ve çalışma saati kendi saat diliminde 07:00'de başlar.</span><span class="sxs-lookup"><span data-stu-id="2df29-123">Resource B: This resource is located in a different time zone than the project and starts at 7:00 AM in their time zone.</span></span> <span data-ttu-id="2df29-124">Ancak, ayırmalar atama sınırının en erken başlangıç saati olan 09:00'da başlar.</span><span class="sxs-lookup"><span data-stu-id="2df29-124">However, the bookings will begin at 9:00 AM as that is the earliest start time of the assignment contour.</span></span>
- <span data-ttu-id="2df29-125">Kaynak C ve D: Bu kaynakların bulundukları saat dilimleri hem birbirlerinden hem de projenin bulunduğu saat diliminden farklıdır ve ayırmaları, uygun oldukları başlangıç saatlerinden daha erken değildir.</span><span class="sxs-lookup"><span data-stu-id="2df29-125">Resources C and D: The resources are located in different time zones, both different from each other and the project, and their bookings start no earlier than their respective available start times.</span></span>

|<span data-ttu-id="2df29-126">Varlık</span><span class="sxs-lookup"><span data-stu-id="2df29-126">Entity</span></span>  |<span data-ttu-id="2df29-127">Takvim</span><span class="sxs-lookup"><span data-stu-id="2df29-127">Calendar</span></span>  |
|-|-|
|<span data-ttu-id="2df29-128">Proje takvimi şablonu</span><span class="sxs-lookup"><span data-stu-id="2df29-128">Project calendar template</span></span>   | ![proje takvimi](media/reconcile-assignments-06.png) |
|<span data-ttu-id="2df29-130">Kaynak A</span><span class="sxs-lookup"><span data-stu-id="2df29-130">Resource A</span></span>  | ![Kaynak A takvimi](media/reconcile-assignments-06.png) |
|<span data-ttu-id="2df29-132">Kaynak B</span><span class="sxs-lookup"><span data-stu-id="2df29-132">Resource B</span></span>  |  ![Kaynak B takvimi](media/reconcile-assignments-07.png) |
|<span data-ttu-id="2df29-134">Kaynak C</span><span class="sxs-lookup"><span data-stu-id="2df29-134">Resource C</span></span>  |  ![Kaynak C takvimi](media/reconcile-assignments-08.png) |
|<span data-ttu-id="2df29-136">Kaynak D</span><span class="sxs-lookup"><span data-stu-id="2df29-136">Resource D</span></span>  | ![Kaynak D takvimi](media/reconcile-assignments-09.png)  |
 
<span data-ttu-id="2df29-138">**Mutabakat** görünümüne gittiğinizde, kaynak atamaları ve ilişkili ayırma eksiklikleri görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="2df29-138">When you navigate to the **Reconciliation** view, the resource assignments and the associated booking shortages are displayed.</span></span>

![Uzatmadan önceki mutabakat görünümü](media/reconcile-assignments-10.png)

<span data-ttu-id="2df29-140">Her kaynak için ayırmayı genişlet işlevi kullanıldıktan sonra her kaynağın çalışma saati var olan eksikliğin sınırlarıyla çakıştığı için ayırmalar, her kaynak için başarıyla genişletilir.</span><span class="sxs-lookup"><span data-stu-id="2df29-140">After the extend booking functionality has been used for each resource, bookings are successfully extended for each resource because each resource’s working hours overlapped with the contours of the shortage.</span></span>

![Ayırmayı uzatma sonrasındaki mutabakat görünümü](media/reconcile-assignments-11.png) 

<span data-ttu-id="2df29-142">Ayırmaların ayrıntılarına daha yakından bakıldığında ayırmaların başlangıç saatlerinde farklılıklar olduğu görülür.</span><span class="sxs-lookup"><span data-stu-id="2df29-142">Notice that a closer look at the details of the bookings shows differences in the start time of the bookings.</span></span> <span data-ttu-id="2df29-143">Ayırmaların başlangıcı, atama sınırının başlangıç zamanından ve kaynağın kullanılabilir başlangıç zamanından daha erken değildir.</span><span class="sxs-lookup"><span data-stu-id="2df29-143">The bookings start no earlier than the start time of the assignment contour and no earlier than the available start time of the resource.</span></span>

![Zamanlama panosunda yeni kaynak ayırmaları](media/reconcile-assignments-12.png)
