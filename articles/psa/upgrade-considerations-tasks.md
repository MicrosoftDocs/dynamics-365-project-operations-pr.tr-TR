---
title: İş kırılım yapısı için yükseltme hususları
description: Bu konu, iş kırılım yapısını Project Service Automation 2.x'ten 3.x'e yükseltme hakkında bilgi sağlar.
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
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
ms.openlocfilehash: 868b0daadaf6cf96ca7bf847914bca8014412f26
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005635"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a><span data-ttu-id="0d2cb-103">İş kırılım yapısı için yükseltme hususları</span><span class="sxs-lookup"><span data-stu-id="0d2cb-103">Upgrade considerations for the work breakdown structure</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="0d2cb-104">Bu konu, iş kırılım yapısını Project Service Automation 2.x'ten 3.x'e yükseltme hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="0d2cb-104">This topic provides information about upgrading the work breakdown structure from Project Service Automation 2.x to 3.x.</span></span> <span data-ttu-id="0d2cb-105">Bu konu, Project Service Automation (PSA) uygulamasında bir projenin başarılı yükseltme için gereken durumunu tanımlar.</span><span class="sxs-lookup"><span data-stu-id="0d2cb-105">This topic defines the healthy state of a project in Project Service Automation (PSA) that is required for a successful upgrade.</span></span> <span data-ttu-id="0d2cb-106">Ayrıca yükseltme işleminin başarısız olmasına neden olacak yaygın engelleme koşulları hakkında da bilgi verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="0d2cb-106">There is also information about the common blocking conditions that will cause upgrade to fail.</span></span> <span data-ttu-id="0d2cb-107">Proje görevlerini ve bir proje zamanlaması içindeki işlevlerini tanımlama hakkında daha fazla bilgi için [Proje zamanlamaları](project-creating.md) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="0d2cb-107">For more information about defining project tasks and their functions within a project schedule, see [Project schedules](project-creating.md).</span></span>

## <a name="key-entities"></a><span data-ttu-id="0d2cb-108">Önemli varlıklar</span><span class="sxs-lookup"><span data-stu-id="0d2cb-108">Key entities</span></span>
<span data-ttu-id="0d2cb-109">Kaynaklarla yüklü doğru bir iş kırılım yapısı için aşağıdaki varlıklar gereklidir:</span><span class="sxs-lookup"><span data-stu-id="0d2cb-109">For an accurate work breakdown structure that is already loaded with resources, the following entities are required:</span></span>

- [<span data-ttu-id="0d2cb-110">Proje</span><span class="sxs-lookup"><span data-stu-id="0d2cb-110">Project</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [<span data-ttu-id="0d2cb-111">Proje Takımı</span><span class="sxs-lookup"><span data-stu-id="0d2cb-111">Project Team</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [<span data-ttu-id="0d2cb-112">Proje Görevi</span><span class="sxs-lookup"><span data-stu-id="0d2cb-112">Project Task</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [<span data-ttu-id="0d2cb-113">Kaynak Atamaları</span><span class="sxs-lookup"><span data-stu-id="0d2cb-113">Resource Assignments</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [<span data-ttu-id="0d2cb-114">Proje Görevi Bağımlılığı</span><span class="sxs-lookup"><span data-stu-id="0d2cb-114">Project Task Dependency</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [<span data-ttu-id="0d2cb-115">Ayrılabilir Kaynaklar</span><span class="sxs-lookup"><span data-stu-id="0d2cb-115">Bookable Resources</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

<span data-ttu-id="0d2cb-116">Kaynağı yüklü bir iş kırılım yapısını tanımlamak için aşağıdaki adımları tamamlamanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="0d2cb-116">To define a resource loaded work breakdown structure, you must complete the following steps:</span></span>

1. <span data-ttu-id="0d2cb-117">Yeni bir proje oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0d2cb-117">Create a new project.</span></span> <span data-ttu-id="0d2cb-118">Yeni proje oluşturma hakkında daha fazla bilgi için [msdyn_project](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="0d2cb-118">For more information about how to create a new project, see [msdyn_project](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span></span>
2. <span data-ttu-id="0d2cb-119">Bir veya daha fazla görev oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0d2cb-119">Create one or more tasks.</span></span> <span data-ttu-id="0d2cb-120">Görev oluşturma hakkında daha fazla bilgi için [msdyn_projecttask](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="0d2cb-120">For more information about how to create a task, see [msdyn_projecttask](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span></span>
3. <span data-ttu-id="0d2cb-121">Görev bağımlılıklarını tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="0d2cb-121">Define the task dependencies.</span></span> <span data-ttu-id="0d2cb-122">Daha fazla bilgi için bkz. [Proje Görevi Bağımlılığı](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span><span class="sxs-lookup"><span data-stu-id="0d2cb-122">For more information, see [Project Task Dependency](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span></span>
4. <span data-ttu-id="0d2cb-123">Proje takım üyelerini projeye atayın.</span><span class="sxs-lookup"><span data-stu-id="0d2cb-123">Assign project team members to the project.</span></span> <span data-ttu-id="0d2cb-124">Daha fazla bilgi için [msdyn_projectteam](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="0d2cb-124">For more information, see [msdyn_projectteam](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span></span>
5. <span data-ttu-id="0d2cb-125">Proje takım üyelerini görevlere atayın.</span><span class="sxs-lookup"><span data-stu-id="0d2cb-125">Assign project team members to the tasks.</span></span> <span data-ttu-id="0d2cb-126">Daha fazla bilgi için [msdyn_resourceassignment](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="0d2cb-126">For more information, see [msdyn_resourceassignment](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span></span>

## <a name="project-team-relationships"></a><span data-ttu-id="0d2cb-127">Proje takım ilişkileri</span><span class="sxs-lookup"><span data-stu-id="0d2cb-127">Project team relationships</span></span>

<span data-ttu-id="0d2cb-128">Başarılı bir yükseltme yapıldığından emin olmak için aşağıdaki ilişkilerin doğru şekilde korunması gerekir:</span><span class="sxs-lookup"><span data-stu-id="0d2cb-128">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>
- <span data-ttu-id="0d2cb-129">Tüm proje takım üyeleri bir ayrılabilir kaynakla ilişkili olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="0d2cb-129">All project team members must be associated with a bookable resource.</span></span>
- <span data-ttu-id="0d2cb-130">Tüm proje takım üyeleri aynı projeyle ilişkili olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="0d2cb-130">All project team members must be associated with the same project.</span></span> 

## <a name="project-task-relationships"></a><span data-ttu-id="0d2cb-131">Proje görev ilişkileri</span><span class="sxs-lookup"><span data-stu-id="0d2cb-131">Project task relationships</span></span>
<span data-ttu-id="0d2cb-132">Başarılı bir yükseltme yapıldığından emin olmak için aşağıdaki ilişkilerin doğru şekilde korunması gerekir:</span><span class="sxs-lookup"><span data-stu-id="0d2cb-132">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="0d2cb-133">İlgili tüm görevlerin aynı projeyle ilişkili olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="0d2cb-133">Any related tasks must be associated with the same project.</span></span>
- <span data-ttu-id="0d2cb-134">Her satır görevinin bir ana görevi olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="0d2cb-134">Every line task must have a parent task.</span></span>
- <span data-ttu-id="0d2cb-135">Her görevin bir ana projesi olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="0d2cb-135">Every task must have a parent project.</span></span>

### <a name="valid-conditions"></a><span data-ttu-id="0d2cb-136">Geçerli koşullar</span><span class="sxs-lookup"><span data-stu-id="0d2cb-136">Valid conditions</span></span>

- <span data-ttu-id="0d2cb-137">Tüm görev süreleri, bir saat değerine eşit veya bu değerden çok (> =) ve 1.800.000 dakikadan (1.250 gün) az olmalıdır.\*</span><span class="sxs-lookup"><span data-stu-id="0d2cb-137">All task durations must be greater than or equal to (>=) one hour and less than 1,800,000 minutes (1,250 days).\*</span></span>
- <span data-ttu-id="0d2cb-138">Tüm görevlerin başlangıç tarihi 01/01/2000 tarihinden önce olmalıdır.\*</span><span class="sxs-lookup"><span data-stu-id="0d2cb-138">All tasks must have a start date no earlier than 2000/01/01.\*</span></span>
- <span data-ttu-id="0d2cb-139">Tüm görevlerin başlangıç tarihi şimdiki tarihten en geç 17 yıldan sonrası olmalıdır.\*</span><span class="sxs-lookup"><span data-stu-id="0d2cb-139">All tasks must have a start date no later than 17 years from the present day.\*</span></span>
- <span data-ttu-id="0d2cb-140">Tüm görevlerin başlangıç tarihi bitiş tarihinden önce veya bu tarih olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="0d2cb-140">All tasks must have a start date earlier or equal to their finish date.</span></span>
- <span data-ttu-id="0d2cb-141">Sınıflandırmalardaki tüm hareket türlerinin (Gider, Malzeme, Vergi ve Süre) **Varsayılan Birim** ve **Birim Grubu** değeri olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="0d2cb-141">All transaction types on classifications (Expense, Material, Tax, and Time) must have values for **Default Unit** and **Unit Group**.</span></span>
- <span data-ttu-id="0d2cb-142">Harflerle yazılan tarih biçimleri kullanılmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="0d2cb-142">Date formats with letters should be avoided.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="0d2cb-143">Potansiyel risk azaltma adımları</span><span class="sxs-lookup"><span data-stu-id="0d2cb-143">Potential mitigation steps</span></span>
- <span data-ttu-id="0d2cb-144">Proje kimliğini içermeyen Proje görevlerini tanımlamak için Gelişmiş Bul seçeneğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="0d2cb-144">Use Advanced Find to identify Project tasks that do not contain a Project ID.</span></span>
- <span data-ttu-id="0d2cb-145">Zamanlanmış sürenin 1.800.000'den fazla olduğu proje görevlerini tanımlamak için Gelişmiş Bul seçeneğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="0d2cb-145">Use Advanced Find to identify Project tasks where the scheduled duration is greater than > 1,800,000.</span></span>
- <span data-ttu-id="0d2cb-146">Veri değişikliği yapmadan önce, verilerin hatalı duruma geçmesine neden olabilecek varlıkla ilişkili tüm özelleştirmeleri araştırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="0d2cb-146">Prior to making any data changes, you should investigate any customizations associated with the entity that may have led to getting the data into a bad state.</span></span> <span data-ttu-id="0d2cb-147">Bu özelleştirmeler, veriyle ilgili herhangi bir güncelleştirme yapmadan önce incelenmelidir.</span><span class="sxs-lookup"><span data-stu-id="0d2cb-147">These customizations should be addressed before proceeding with any data-related updates.</span></span>
- <span data-ttu-id="0d2cb-148">Sahipsiz kalan tanımlı görevler için, gerekli değillerse veya doğru ana projeyle ilişkilendirilmeleri gerekiyorsa bu görevleri silebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0d2cb-148">For the identified tasks that have been orphaned, consider deleting these tasks if they are not needed or if they should be associated with the correct parent project.</span></span>
- <span data-ttu-id="0d2cb-149">Sürenin 1.250 günden fazla olduğu tüm görevlerde uygunsa, toplam süreyi temsil etmesi için ek görevler ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0d2cb-149">For any tasks where the duration is greater than 1,250 days, consider adding multiple tasks to represent the total duration, if feasible.</span></span>

> [!NOTE]
> <span data-ttu-id="0d2cb-150">Müşteri ilişkileri yönetiminin (CRM) yalnızca 7.320 yineleme genişletmesini desteklemesi nedeniyle yıldız (\*) işareti olan öğelerin sınırları vardır.</span><span class="sxs-lookup"><span data-stu-id="0d2cb-150">Items noted with an asterisk (\*) have limits that are due to the fact that customer relationship management (CRM) supports only 7,320 recurrence expansions.</span></span> <span data-ttu-id="0d2cb-151">Bu sınırın altında kalmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="0d2cb-151">You must stay below this limit.</span></span>

## <a name="resource-assignment-relationships"></a><span data-ttu-id="0d2cb-152">Kaynak Atama ilişkileri</span><span class="sxs-lookup"><span data-stu-id="0d2cb-152">Resource Assignment relationships</span></span>
<span data-ttu-id="0d2cb-153">Başarılı bir yükseltme yapıldığından emin olmak için aşağıdaki ilişkilerin doğru şekilde korunması gerekir:</span><span class="sxs-lookup"><span data-stu-id="0d2cb-153">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="0d2cb-154">Bir iş kırılım yapısındaki tüm Kaynak Atamaları aynı projeyle ilişkili olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="0d2cb-154">All Resource Assignments in a work breakdown structure must be related to the same project.</span></span>
- <span data-ttu-id="0d2cb-155">Bir iş kırılım yapısındaki tüm Kaynak Atamaları aynı projedeki proje takım üyeleriyle ilişkili olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="0d2cb-155">All Resource Assignments in a work breakdown structure must be associated to project team members in the same project.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="0d2cb-156">Potansiyel risk azaltma adımları</span><span class="sxs-lookup"><span data-stu-id="0d2cb-156">Potential mitigation steps</span></span>
- <span data-ttu-id="0d2cb-157">Yukarıda açıklanan koşulların dışında kalan tüm görevleri tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="0d2cb-157">Identify all tasks that fall outside the conditions described above.</span></span>  
- <span data-ttu-id="0d2cb-158">Artık geçerli olmayan tüm Kaynak Atamaları silinmelidir.</span><span class="sxs-lookup"><span data-stu-id="0d2cb-158">Any Resource Assignments that are no longer valid should be deleted.</span></span>

## <a name="project-task-dependency-relationships"></a><span data-ttu-id="0d2cb-159">Proje görevi bağımlılığı durumu</span><span class="sxs-lookup"><span data-stu-id="0d2cb-159">Project task dependency relationships</span></span>
<span data-ttu-id="0d2cb-160">Başarılı bir yükseltme yapıldığından emin olmak için aşağıdaki ilişkilerin doğru şekilde korunması gerekir:</span><span class="sxs-lookup"><span data-stu-id="0d2cb-160">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="0d2cb-161">Tüm proje görevi bağımlılıkları aynı projeyle ilişkili olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="0d2cb-161">All project task dependencies must be related to the same project.</span></span>
- <span data-ttu-id="0d2cb-162">Bir görev için aynı bağımlılığa birden başvuru yapılamaz.</span><span class="sxs-lookup"><span data-stu-id="0d2cb-162">A task can't have the same dependency referenced more than once.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]