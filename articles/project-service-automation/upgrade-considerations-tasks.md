---
title: İş kırılım yapısı için yükseltme hususları
description: Bu konu, iş kırılım yapısını Project Service Automation 2.x'ten 3.x'e yükseltme hakkında bilgi sağlar.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 2.x
author: ruhercul
ms.assetid: 9e43d5b5-ca5d-41f5-9012-c48f8e3080f9
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 9aa35dd8784bfa55737b0836e653afd0442b80c2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756672"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a><span data-ttu-id="a49ae-103">İş kırılım yapısı için yükseltme hususları</span><span class="sxs-lookup"><span data-stu-id="a49ae-103">Upgrade considerations for the work breakdown structure</span></span>
<span data-ttu-id="a49ae-104">Bu konu, iş kırılım yapısını Project Service Automation 2.x'ten 3.x'e yükseltme hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="a49ae-104">This topic provides information about upgrading the work breakdown structure from Project Service Automation 2.x to 3.x.</span></span> <span data-ttu-id="a49ae-105">Bu konu, Project Service Automation (PSA) uygulamasında bir projenin başarılı yükseltme için gereken durumunu tanımlar.</span><span class="sxs-lookup"><span data-stu-id="a49ae-105">This topic defines the healthy state of a project in Project Service Automation (PSA) that is required for a successful upgrade.</span></span> <span data-ttu-id="a49ae-106">Ayrıca yükseltme işleminin başarısız olmasına neden olacak yaygın engelleme koşulları hakkında da bilgi verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="a49ae-106">There is also information about the common blocking conditions that will cause upgrade to fail.</span></span> <span data-ttu-id="a49ae-107">Proje görevlerini ve bir proje zamanlaması içindeki işlevlerini tanımlama hakkında daha fazla bilgi için [Proje zamanlamaları](project-creating.md) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="a49ae-107">For more information about defining project tasks and their functions within a project schedule, see [Project schedules](project-creating.md).</span></span>

## <a name="key-entities"></a><span data-ttu-id="a49ae-108">Önemli varlıklar</span><span class="sxs-lookup"><span data-stu-id="a49ae-108">Key entities</span></span>
<span data-ttu-id="a49ae-109">Kaynaklarla yüklü doğru bir iş kırılım yapısı için aşağıdaki varlıklar gereklidir:</span><span class="sxs-lookup"><span data-stu-id="a49ae-109">For an accurate work breakdown structure that is already loaded with resources, the following entities are required:</span></span>

- [<span data-ttu-id="a49ae-110">Proje</span><span class="sxs-lookup"><span data-stu-id="a49ae-110">Project</span></span>](../developer/entities/msdyn_project.md)
- [<span data-ttu-id="a49ae-111">Proje Takımı</span><span class="sxs-lookup"><span data-stu-id="a49ae-111">Project Team</span></span>](../developer/entities/msdyn_projectteam.md)
- [<span data-ttu-id="a49ae-112">Proje Görevi</span><span class="sxs-lookup"><span data-stu-id="a49ae-112">Project Task</span></span>](../developer/entities/msdyn_projecttask.md)
- [<span data-ttu-id="a49ae-113">Kaynak Atamaları</span><span class="sxs-lookup"><span data-stu-id="a49ae-113">Resource Assignments</span></span>](../developer/entities/msdyn_resourceassignment.md)
- [<span data-ttu-id="a49ae-114">Proje Görevi Bağımlılığı</span><span class="sxs-lookup"><span data-stu-id="a49ae-114">Project Task Dependency</span></span>](../developer/entities/msdyn_projecttaskdependency.md)
- [<span data-ttu-id="a49ae-115">Ayrılabilir Kaynaklar</span><span class="sxs-lookup"><span data-stu-id="a49ae-115">Bookable Resources</span></span>](../developer/entities/bookableresource.md)

<span data-ttu-id="a49ae-116">Kaynağı yüklü bir iş kırılım yapısını tanımlamak için aşağıdaki adımları tamamlamanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="a49ae-116">To define a resource loaded work breakdown structure, you must complete the following steps:</span></span>

1. <span data-ttu-id="a49ae-117">Yeni bir proje oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a49ae-117">Create a new project.</span></span> <span data-ttu-id="a49ae-118">Yeni proje oluşturma hakkında daha fazla bilgi için [msdyn_project](../developer/entities/msdyn_project.md) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="a49ae-118">For more information about how to create a new project, see [msdyn_project](../developer/entities/msdyn_project.md).</span></span>
2. <span data-ttu-id="a49ae-119">Bir veya daha fazla görev oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a49ae-119">Create one or more tasks.</span></span> <span data-ttu-id="a49ae-120">Görev oluşturma hakkında daha fazla bilgi için [msdyn_projecttask](../developer/entities/msdyn_projecttask.md) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="a49ae-120">For more information about how to create a task, see [msdyn_projecttask](../developer/entities/msdyn_projecttask.md).</span></span>
3. <span data-ttu-id="a49ae-121">Görev bağımlılıklarını tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="a49ae-121">Define the task dependencies.</span></span> <span data-ttu-id="a49ae-122">Daha fazla bilgi için bkz. [Proje Görevi Bağımlılığı](../developer/entities/msdyn_projecttaskdependency.md).</span><span class="sxs-lookup"><span data-stu-id="a49ae-122">For more information, see [Project Task Dependency](../developer/entities/msdyn_projecttaskdependency.md).</span></span>
4. <span data-ttu-id="a49ae-123">Proje takım üyelerini projeye atayın.</span><span class="sxs-lookup"><span data-stu-id="a49ae-123">Assign project team members to the project.</span></span> <span data-ttu-id="a49ae-124">Daha fazla bilgi için [msdyn_projectteam](../developer/entities/msdyn_projectteam.md) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="a49ae-124">For more information, see [msdyn_projectteam](../developer/entities/msdyn_projectteam.md).</span></span>
5. <span data-ttu-id="a49ae-125">Proje takım üyelerini görevlere atayın.</span><span class="sxs-lookup"><span data-stu-id="a49ae-125">Assign project team members to the tasks.</span></span> <span data-ttu-id="a49ae-126">Daha fazla bilgi için [msdyn_resourceassignment](../developer/entities/msdyn_resourceassignment.md) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="a49ae-126">For more information, see [msdyn_resourceassignment](../developer/entities/msdyn_resourceassignment.md).</span></span>

## <a name="project-team-relationships"></a><span data-ttu-id="a49ae-127">Proje takım ilişkileri</span><span class="sxs-lookup"><span data-stu-id="a49ae-127">Project team relationships</span></span>

<span data-ttu-id="a49ae-128">Başarılı bir yükseltme yapıldığından emin olmak için aşağıdaki ilişkilerin doğru şekilde korunması gerekir:</span><span class="sxs-lookup"><span data-stu-id="a49ae-128">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>
- <span data-ttu-id="a49ae-129">Tüm proje takım üyeleri bir ayrılabilir kaynakla ilişkili olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a49ae-129">All project team members must be associated with a bookable resource.</span></span>
- <span data-ttu-id="a49ae-130">Tüm proje takım üyeleri aynı projeyle ilişkili olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a49ae-130">All project team members must be associated with the same project.</span></span> 

## <a name="project-task-relationships"></a><span data-ttu-id="a49ae-131">Proje görev ilişkileri</span><span class="sxs-lookup"><span data-stu-id="a49ae-131">Project task relationships</span></span>
<span data-ttu-id="a49ae-132">Başarılı bir yükseltme yapıldığından emin olmak için aşağıdaki ilişkilerin doğru şekilde korunması gerekir:</span><span class="sxs-lookup"><span data-stu-id="a49ae-132">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="a49ae-133">İlgili tüm görevlerin aynı projeyle ilişkili olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a49ae-133">Any related tasks must be associated with the same project.</span></span>
- <span data-ttu-id="a49ae-134">Her satır görevinin bir ana görevi olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a49ae-134">Every line task must have a parent task.</span></span>
- <span data-ttu-id="a49ae-135">Her görevin bir ana projesi olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a49ae-135">Every task must have a parent project.</span></span>

### <a name="valid-conditions"></a><span data-ttu-id="a49ae-136">Geçerli koşullar</span><span class="sxs-lookup"><span data-stu-id="a49ae-136">Valid conditions</span></span>

- <span data-ttu-id="a49ae-137">Tüm görev süreleri, bir saat değerine eşit veya bu değerden çok (> =) ve 1.800.000 dakikadan (1.250 gün) az olmalıdır.\*</span><span class="sxs-lookup"><span data-stu-id="a49ae-137">All task durations must be greater than or equal to (>=) one hour and less than 1,800,000 minutes (1,250 days).\*</span></span>
- <span data-ttu-id="a49ae-138">Tüm görevlerin başlangıç tarihi 01/01/2000 tarihinden önce olmalıdır.\*</span><span class="sxs-lookup"><span data-stu-id="a49ae-138">All tasks must have a start date no earlier than 2000/01/01.\*</span></span>
- <span data-ttu-id="a49ae-139">Tüm görevlerin başlangıç tarihi şimdiki tarihten en geç 17 yıldan sonrası olmalıdır.\*</span><span class="sxs-lookup"><span data-stu-id="a49ae-139">All tasks must have a start date no later than 17 years from the present day.\*</span></span>
- <span data-ttu-id="a49ae-140">Tüm görevlerin başlangıç tarihi bitiş tarihinden önce veya bu tarih olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a49ae-140">All tasks must have a start date earlier or equal to their finish date.</span></span>
- <span data-ttu-id="a49ae-141">Sınıflandırmalardaki tüm hareket türlerinin (Gider, Malzeme, Vergi ve Süre) **Varsayılan Birim** ve **Birim Grubu** değeri olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a49ae-141">All transaction types on classifications (Expense, Material, Tax, and Time) must have values for **Default Unit** and **Unit Group**.</span></span>
- <span data-ttu-id="a49ae-142">Harflerle yazılan tarih biçimleri kullanılmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="a49ae-142">Date formats with letters should be avoided.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="a49ae-143">Potansiyel risk azaltma adımları</span><span class="sxs-lookup"><span data-stu-id="a49ae-143">Potential mitigation steps</span></span>
- <span data-ttu-id="a49ae-144">Proje kimliğini içermeyen Proje görevlerini tanımlamak için Gelişmiş Bul seçeneğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a49ae-144">Use Advanced Find to identify Project tasks that do not contain a Project ID.</span></span>
- <span data-ttu-id="a49ae-145">Zamanlanmış sürenin 1.800.000'den fazla olduğu proje görevlerini tanımlamak için Gelişmiş Bul seçeneğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a49ae-145">Use Advanced Find to identify Project tasks where the scheduled duration is greater than > 1,800,000.</span></span>
- <span data-ttu-id="a49ae-146">Veri değişikliği yapmadan önce, verilerin hatalı duruma geçmesine neden olabilecek varlıkla ilişkili tüm özelleştirmeleri araştırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="a49ae-146">Prior to making any data changes, you should investigate any customizations associated with the entity that may have led to getting the data into a bad state.</span></span> <span data-ttu-id="a49ae-147">Bu özelleştirmeler, veriyle ilgili herhangi bir güncelleştirme yapmadan önce incelenmelidir.</span><span class="sxs-lookup"><span data-stu-id="a49ae-147">These customizations should be addressed before proceeding with any data-related updates.</span></span>
- <span data-ttu-id="a49ae-148">Sahipsiz kalan tanımlı görevler için, gerekli değillerse veya doğru ana projeyle ilişkilendirilmeleri gerekiyorsa bu görevleri silebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a49ae-148">For the identified tasks that have been orphaned, consider deleting these tasks if they are not needed or if they should be associated with the correct parent project.</span></span>
- <span data-ttu-id="a49ae-149">Sürenin 1.250 günden fazla olduğu tüm görevlerde uygunsa, toplam süreyi temsil etmesi için ek görevler ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a49ae-149">For any tasks where the duration is greater than 1,250 days, consider adding multiple tasks to represent the total duration, if feasible.</span></span>

> [!NOTE]
> <span data-ttu-id="a49ae-150">Müşteri ilişkileri yönetiminin (CRM) yalnızca 7.320 yineleme genişletmesini desteklemesi nedeniyle yıldız (\*) işareti olan öğelerin sınırları vardır.</span><span class="sxs-lookup"><span data-stu-id="a49ae-150">Items noted with an asterisk (\*) have limits that are due to the fact that customer relationship management (CRM) supports only 7,320 recurrence expansions.</span></span> <span data-ttu-id="a49ae-151">Bu sınırın altında kalmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="a49ae-151">You must stay below this limit.</span></span>

## <a name="resource-assignment-relationships"></a><span data-ttu-id="a49ae-152">Kaynak Atama ilişkileri</span><span class="sxs-lookup"><span data-stu-id="a49ae-152">Resource Assignment relationships</span></span>
<span data-ttu-id="a49ae-153">Başarılı bir yükseltme yapıldığından emin olmak için aşağıdaki ilişkilerin doğru şekilde korunması gerekir:</span><span class="sxs-lookup"><span data-stu-id="a49ae-153">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="a49ae-154">Bir iş kırılım yapısındaki tüm Kaynak Atamaları aynı projeyle ilişkili olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a49ae-154">All Resource Assignments in a work breakdown structure must be related to the same project.</span></span>
- <span data-ttu-id="a49ae-155">Bir iş kırılım yapısındaki tüm Kaynak Atamaları aynı projedeki proje takım üyeleriyle ilişkili olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a49ae-155">All Resource Assignments in a work breakdown structure must be associated to project team members in the same project.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="a49ae-156">Potansiyel risk azaltma adımları</span><span class="sxs-lookup"><span data-stu-id="a49ae-156">Potential mitigation steps</span></span>
- <span data-ttu-id="a49ae-157">Yukarıda açıklanan koşulların dışında kalan tüm görevleri tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="a49ae-157">Identify all tasks that fall outside the conditions described above.</span></span>  
- <span data-ttu-id="a49ae-158">Artık geçerli olmayan tüm Kaynak Atamaları silinmelidir.</span><span class="sxs-lookup"><span data-stu-id="a49ae-158">Any Resource Assignments that are no longer valid should be deleted.</span></span>

## <a name="project-task-dependency-relationships"></a><span data-ttu-id="a49ae-159">Proje görevi bağımlılığı durumu</span><span class="sxs-lookup"><span data-stu-id="a49ae-159">Project task dependency relationships</span></span>
<span data-ttu-id="a49ae-160">Başarılı bir yükseltme yapıldığından emin olmak için aşağıdaki ilişkilerin doğru şekilde korunması gerekir:</span><span class="sxs-lookup"><span data-stu-id="a49ae-160">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="a49ae-161">Tüm proje görevi bağımlılıkları aynı projeyle ilişkili olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a49ae-161">All project task dependencies must be related to the same project.</span></span>
- <span data-ttu-id="a49ae-162">Bir görev için aynı bağımlılığa birden başvuru yapılamaz.</span><span class="sxs-lookup"><span data-stu-id="a49ae-162">A task can't have the same dependency referenced more than once.</span></span>
