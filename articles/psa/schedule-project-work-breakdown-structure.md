---
title: İş kırılım yapısına sahip bir projeyi zamanlama
description: Project Service'ta iş kırılım yapısına sahip bir projeyi zamanlama
author: ruhercul
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
ms.openlocfilehash: 027bcbc8995ed39af78c7ff9b1028f401c3b0d4d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008605"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a><span data-ttu-id="44fc1-103">İş kırılım yapısına sahip bir projeyi zamanlama (Project Service)</span><span class="sxs-lookup"><span data-stu-id="44fc1-103">Schedule a project with a work breakdown structure (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="44fc1-104">Proje zamanlaması, çalışmanın gerçekleştirilmesi için gereken kaynaklarla ve çalışmanın zaman dilimi ile iletişim kurar.</span><span class="sxs-lookup"><span data-stu-id="44fc1-104">A project schedule communicates what work needs to be performed, which resources will perform the work, and the timeframe in which that work needs to be completed.</span></span> <span data-ttu-id="44fc1-105">Proje zamanlaması, projenin zamanında teslimi ile ilişkili tüm çalışmayı yansıtır.</span><span class="sxs-lookup"><span data-stu-id="44fc1-105">The project schedule reflects all the work associated with delivering the project on time.</span></span> <span data-ttu-id="44fc1-106">Projenin başlangıç aşamasının ilk adımlardan biri, bir proje takvimi oluşturmaktır.</span><span class="sxs-lookup"><span data-stu-id="44fc1-106">One of the first steps in the initiation phase of the project is to come up with a project schedule.</span></span> <span data-ttu-id="44fc1-107">Bir proje planı oluşturmak için, iş kırılım yapısı oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="44fc1-107">To establish a project schedule, you need to create a work breakdown structure.</span></span>  
  
 <span data-ttu-id="44fc1-108">Aşağıdakilerde size yardımcı olan bir iş kırılım yapısına sahip proje yapısını oluşturun:</span><span class="sxs-lookup"><span data-stu-id="44fc1-108">Create a project structure with a work breakdown structure, which helps you:</span></span>  
  
- <span data-ttu-id="44fc1-109">Yönetilebilir görevlerde çalışmayı bölme</span><span class="sxs-lookup"><span data-stu-id="44fc1-109">Break down work into manageable tasks</span></span>  
  
- <span data-ttu-id="44fc1-110">Bir görevi tamamlamak için gereken zamanı tahmin etme</span><span class="sxs-lookup"><span data-stu-id="44fc1-110">Estimate the time required to complete a task</span></span>  
  
- <span data-ttu-id="44fc1-111">Görev bağımlılıkları ve görev süresini ayarlama</span><span class="sxs-lookup"><span data-stu-id="44fc1-111">Set task dependencies and task duration</span></span>  
  
- <span data-ttu-id="44fc1-112">Her bir görevi tamamlamak için gereken rollerini tanımla</span><span class="sxs-lookup"><span data-stu-id="44fc1-112">Determine the roles required to complete each task</span></span>  
  
  <span data-ttu-id="44fc1-113">İş kırılım yapısındaki proje zamanlaması, etkileşimli bir Gantt şemasına benzer bir görünüm ve kullanıma sahiptir.</span><span class="sxs-lookup"><span data-stu-id="44fc1-113">The project schedule in the work breakdown structure has a familiar look and feel, complete with an interactive Gantt chart.</span></span>  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a><span data-ttu-id="44fc1-114">Bir proje için iş kırılım yapısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="44fc1-114">Create a work breakdown structure for a project</span></span>  
 <span data-ttu-id="44fc1-115">Projedeki görevlerin sırasını göstermek için bir iş kırılım yapısı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="44fc1-115">Create a work breakdown structure to represent the sequence of tasks in a project.</span></span> <span data-ttu-id="44fc1-116">İş kırılım yapısı, görevleri, her görevin gereksinimlerini ve gelir ve maliyet bilgilerini içerir.</span><span class="sxs-lookup"><span data-stu-id="44fc1-116">The work breakdown structure includes tasks, requirements for each task, and revenue and cost information.</span></span> <span data-ttu-id="44fc1-117">İş kırılım yapınızda şunları ekleyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="44fc1-117">In your work breakdown structure, you can add:</span></span>  
  
-   <span data-ttu-id="44fc1-118">Bir hiyerarşideki görev dizisi</span><span class="sxs-lookup"><span data-stu-id="44fc1-118">The sequence of tasks in a hierarchy</span></span>  
  
-   <span data-ttu-id="44fc1-119">Varsa, bir görev başlatılmadan önce tamamlanması gereken diğer görevler</span><span class="sxs-lookup"><span data-stu-id="44fc1-119">Other tasks, if any, that must be completed before a task can be started</span></span>  
  
-   <span data-ttu-id="44fc1-120">Başlangıç tarihi, bitiş tarihi ve görev süresi</span><span class="sxs-lookup"><span data-stu-id="44fc1-120">The starting date, ending date, and duration of a task</span></span>  
  
-   <span data-ttu-id="44fc1-121">Bir görev için gereken saat sayısı</span><span class="sxs-lookup"><span data-stu-id="44fc1-121">The number of hours required for a task</span></span>  
  
-   <span data-ttu-id="44fc1-122">Tüm gerekli çalışan becerileri ve eğitimi</span><span class="sxs-lookup"><span data-stu-id="44fc1-122">Any required worker skills and education</span></span>  
  
-   <span data-ttu-id="44fc1-123">Bir göreve atanan çalışanlar</span><span class="sxs-lookup"><span data-stu-id="44fc1-123">The workers who are assigned to a task</span></span>  
  
-   <span data-ttu-id="44fc1-124">Tahmini gelir ve maliyetler</span><span class="sxs-lookup"><span data-stu-id="44fc1-124">Estimated revenue and costs</span></span>  
  
## <a name="task-types"></a><span data-ttu-id="44fc1-125">Görev türleri</span><span class="sxs-lookup"><span data-stu-id="44fc1-125">Task types</span></span>  
<span data-ttu-id="44fc1-126">İş kırılım yapınızı oluştururken aşağıdaki görev türlerini kullanırsınız:</span><span class="sxs-lookup"><span data-stu-id="44fc1-126">You’ll use the following types of tasks when creating your work breakdown structure:</span></span>  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| <span data-ttu-id="44fc1-127">**Proje kök düğümü**</span><span class="sxs-lookup"><span data-stu-id="44fc1-127">**Project root node**</span></span> | <span data-ttu-id="44fc1-128">Proje için en üst düzey özet görevi.</span><span class="sxs-lookup"><span data-stu-id="44fc1-128">The top-level summary task for the project.</span></span> <span data-ttu-id="44fc1-129">Diğer tüm proje görevleri, proje altında oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="44fc1-129">All other project tasks are created under it.</span></span> <span data-ttu-id="44fc1-130">Kök görevin adı proje adıdır.</span><span class="sxs-lookup"><span data-stu-id="44fc1-130">The name of the root task is the project name.</span></span> <span data-ttu-id="44fc1-131">Kök düğümün çalışması, tarihleri ve süresi aşağıdaki hiyerarşide bulunan değerleri temel alır.</span><span class="sxs-lookup"><span data-stu-id="44fc1-131">The effort, dates, and duration of the root node are based on the values on the hierarchy below it.</span></span> <span data-ttu-id="44fc1-132">Kök düğümü özelliklerini düzenleyemez veya kök düğümü silemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="44fc1-132">You can’t edit root node properties or delete the root node.</span></span> | 
| <span data-ttu-id="44fc1-133">**Özet veya kapsayıcı görevleri**</span><span class="sxs-lookup"><span data-stu-id="44fc1-133">**Summary or container tasks**</span></span> | <span data-ttu-id="44fc1-134">Bir özet görev, altında alt görevlere sahip olan bir görevdir.</span><span class="sxs-lookup"><span data-stu-id="44fc1-134">A summary task is a task that has sub-tasks under it.</span></span> <span data-ttu-id="44fc1-135">Bir özet görev herhangi bir iş çalışmasına veya kendi maliyetine sahip değildir.</span><span class="sxs-lookup"><span data-stu-id="44fc1-135">A summary task doesn’t have any work effort or cost of its own.</span></span> <span data-ttu-id="44fc1-136">Çalışma ve maliyet alt görevlerinin toplu değeridir.</span><span class="sxs-lookup"><span data-stu-id="44fc1-136">Its work effort and cost are a rollup of its sub-tasks.</span></span> <span data-ttu-id="44fc1-137">Bir özet görevin adını değiştirebilirsiniz ancak, otomatik olarak hesaplandığı için çalışmayı, tarihleri veya süreyi değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="44fc1-137">You can change the name of a summary task, but you can’t change the effort, dates, or duration, because those are automatically calculated.</span></span> <span data-ttu-id="44fc1-138">Bir özet görevin silinmesi, görevi ve onun alt görevlerini siler.</span><span class="sxs-lookup"><span data-stu-id="44fc1-138">Deleting a summary task deletes the task and all of its sub-tasks.</span></span>|  
| <span data-ttu-id="44fc1-139">**Yaprak düğüm görevleri**</span><span class="sxs-lookup"><span data-stu-id="44fc1-139">**Leaf node tasks**</span></span> | <span data-ttu-id="44fc1-140">Bir yaprak düğüm görevi, projedeki en ayrıntılı çalışmayı temsil eder.</span><span class="sxs-lookup"><span data-stu-id="44fc1-140">A leaf node task represents the most detailed work on the project.</span></span> <span data-ttu-id="44fc1-141">Bu, bir tahmini çalışmaya, kaynakların planlanan sayısını, planlanan başlangıç ve bitiş tarihlerini ve bir süreye sahiptir.</span><span class="sxs-lookup"><span data-stu-id="44fc1-141">It has an estimated effort, a planned number of resources, planned start and end dates, and a duration.</span></span>|

  
## <a name="task-hierarchy"></a><span data-ttu-id="44fc1-142">Görev hiyerarşisi</span><span class="sxs-lookup"><span data-stu-id="44fc1-142">Task hierarchy</span></span>  
 <span data-ttu-id="44fc1-143">Görev hiyerarşisi oluşturma sırasında aşağıdaki seçeneklere sahipsiniz:</span><span class="sxs-lookup"><span data-stu-id="44fc1-143">You have the following options when creating a task hierarchy:</span></span>  
  
- <span data-ttu-id="44fc1-144">**Görev ekle**.</span><span class="sxs-lookup"><span data-stu-id="44fc1-144">**Add task**.</span></span>   <span data-ttu-id="44fc1-145">Görev hiyerarşisinde seçtiğiniz bir konuma görev ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="44fc1-145">You can add a task at a position you choose in the task hierarchy.</span></span> <span data-ttu-id="44fc1-146">Bir konum seçmezseniz, yeni göreviniz en sonda görünür.</span><span class="sxs-lookup"><span data-stu-id="44fc1-146">If you don’t select a position, your new task appears at the end.</span></span>  
  
- <span data-ttu-id="44fc1-147">**Görevi girintile**.</span><span class="sxs-lookup"><span data-stu-id="44fc1-147">**Indent task**.</span></span>   <span data-ttu-id="44fc1-148">Görevi hemen üstündekinin alt görevi yapmak için bir görevi girintileyin.</span><span class="sxs-lookup"><span data-stu-id="44fc1-148">Indent a task to make it a child of the task directly above it.</span></span>  
  
- <span data-ttu-id="44fc1-149">**Görevi çıkıntıla**.</span><span class="sxs-lookup"><span data-stu-id="44fc1-149">**Outdent task**.</span></span>   <span data-ttu-id="44fc1-150">Artık kendi özgün üst görevin alt görevi olmaması için bir görevi çıkıntılayın.</span><span class="sxs-lookup"><span data-stu-id="44fc1-150">Outdent a task to make it so it’s no longer a sub-task of its original parent task.</span></span>  
  
- <span data-ttu-id="44fc1-151">**Yukarı taşı ve Aşağı taşı**.</span><span class="sxs-lookup"><span data-stu-id="44fc1-151">**Move up and Move down**.</span></span>   <span data-ttu-id="44fc1-152">Görevleri kendi ana görev hiyerarşisinde yukarı ve aşağı taşıyın.</span><span class="sxs-lookup"><span data-stu-id="44fc1-152">Move tasks up and down in the hierarchy of its parent task.</span></span> <span data-ttu-id="44fc1-153">Bir görevin yukarı veya aşağı taşınması çalışma, maliyet, tarihler veya süre üzerinde hiçbir etkisi olmaz.</span><span class="sxs-lookup"><span data-stu-id="44fc1-153">Moving a task up or down has no effect on its effort, cost, dates, or duration.</span></span>  
  
## <a name="task-attributes"></a><span data-ttu-id="44fc1-154">Görev öznitelikleri</span><span class="sxs-lookup"><span data-stu-id="44fc1-154">Task attributes</span></span>  
 <span data-ttu-id="44fc1-155">Görevin adı tamamlanması gereken işi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="44fc1-155">A task’s name describes the work that needs to be completed.</span></span> <span data-ttu-id="44fc1-156">Görev için zamanlama ve kadro ihtiyaçlarını tanımlamak için görev öznitelikleri kullanın.</span><span class="sxs-lookup"><span data-stu-id="44fc1-156">You use various task attributes to describe the schedule and staffing requirements for the task.</span></span>  
  
### <a name="schedule-attributes"></a><span data-ttu-id="44fc1-157">Zamanlama öznitelikleri</span><span class="sxs-lookup"><span data-stu-id="44fc1-157">Schedule attributes</span></span>

 - <span data-ttu-id="44fc1-158">Görevin zamanlamasını belirlemek için **Çalışma saati**, **Kaynak sayısı**, **Başlangıç tarihi**, **Bitiş tarihi** ve **Süre** öğelerine değer atayın.</span><span class="sxs-lookup"><span data-stu-id="44fc1-158">Assign values to **Effort hours**, **Number of resources**, **Start date**, **End date**, and **Duration** to determine the schedule for the task.</span></span> 
 - <span data-ttu-id="44fc1-159">**Çalışma**, görevi tamamlamak için gereken saatlik bir tahmindir.</span><span class="sxs-lookup"><span data-stu-id="44fc1-159">**Effort** is an estimate of the hours it takes to complete the task.</span></span>
 - <span data-ttu-id="44fc1-160">**Kaynak sayısı**, proje yöneticisinin olası en iyi zamanlamayı oluşturmasına yardımcı olması için göreve eklediği bir tahmindir.</span><span class="sxs-lookup"><span data-stu-id="44fc1-160">**Number of resources** is an estimate that the project manager puts in the task to help come up with the best possible schedule.</span></span> 
 - <span data-ttu-id="44fc1-161">**Süre** (gün cinsinden), görevi tamamlamak için gereken iş günü sayısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="44fc1-161">**Duration** (in days) indicates the number of work days it will take to complete the task.</span></span>  
  
### <a name="staffing-attributes"></a><span data-ttu-id="44fc1-162">Kadro oluşturma öznitelikleri</span><span class="sxs-lookup"><span data-stu-id="44fc1-162">Staffing attributes</span></span>

 - <span data-ttu-id="44fc1-163">**Rol**, **Kaynak kuruluş birimi**, **Kaynak sayısı** ve **Kaynaklar**, görevin kadro oluşturma gereksinimlerini açıklar.</span><span class="sxs-lookup"><span data-stu-id="44fc1-163">**Role**, **Resource organizational unit**, **Number of resources**, and **Resources** describe the staffing requirements for the task.</span></span> 
 - <span data-ttu-id="44fc1-164">**Rol**, görevi gerçekleştirmek için gereken kaynak türünü açıklar.</span><span class="sxs-lookup"><span data-stu-id="44fc1-164">**Role** describes the type of resource needed to perform the task.</span></span> 
 - <span data-ttu-id="44fc1-165">**Kaynak kuruluş birimi**, görev için personel sağlanması gereken kuruluş birimini gösterir; bu aynı zamanda kaynak için birim satış fiyatını belirlerken hesaplandığından görevin maliyet ve satış tahminini de etkiler.</span><span class="sxs-lookup"><span data-stu-id="44fc1-165">**Resource organizational unit** indicates the organizational unit from which resources should be staffed for that task; this also impacts the cost and sales estimate of the task, since this is accounted for when determining the unit sales price for the resource.</span></span> 
 - <span data-ttu-id="44fc1-166">**Kaynaklar**, genel bir kaynak veya biri bulunduğunda adlandırılmış bir kaynak barındırır.</span><span class="sxs-lookup"><span data-stu-id="44fc1-166">**Resources** holds a generic resource or a named resource when one is found.</span></span>  
  
## <a name="task-dependencies"></a><span data-ttu-id="44fc1-167">Görev bağımlılıkları</span><span class="sxs-lookup"><span data-stu-id="44fc1-167">Task dependencies</span></span>  
 <span data-ttu-id="44fc1-168">İş kırılım yapısında bir veya daha fazla görev arasında öncül ilişkileri oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="44fc1-168">You can create predecessor relationships between one or more tasks in the work breakdown structure.</span></span> <span data-ttu-id="44fc1-169">Görevlere bağımlı görevleri göstermek üzere öncül alan için bir veya daha fazla değer ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="44fc1-169">You can set one or more values for the predecessor field on tasks to indicate the tasks that it will be dependent on.</span></span> <span data-ttu-id="44fc1-170">Görev için bir öncül değer atadığınızda, yalnızca tüm öncül görevler tamamlandığında görev başlatabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="44fc1-170">When you assign a predecessor value to a task, the task can only start when all the predecessor tasks have completed.</span></span> <span data-ttu-id="44fc1-171">Görev üzerinde bu bağımlılığı ayarlamanız, görevin planlanan başlangıç tarihinin tüm öncüllerinin sonu olarak hesaplanmasıyla sonuçlanır.</span><span class="sxs-lookup"><span data-stu-id="44fc1-171">Setting this dependency on a task will result in the recalculation of the planned start date of the task as the latest end of all of its predecessors.</span></span> <span data-ttu-id="44fc1-172">Bir zamanlamadaki öncül ile ilgili etkiler, görevde tanımlı görev modu ile sınırlı değildir.</span><span class="sxs-lookup"><span data-stu-id="44fc1-172">Predecessor-related impacts on a schedule are not limited by the task mode defined on the task.</span></span>  
  
## <a name="task-mode"></a><span data-ttu-id="44fc1-173">Görev modu</span><span class="sxs-lookup"><span data-stu-id="44fc1-173">Task mode</span></span>  
 <span data-ttu-id="44fc1-174">Görev modu, yaprak düğüm görevlerini zamanlamayı belirleyen önemli etkenlerden biridir.</span><span class="sxs-lookup"><span data-stu-id="44fc1-174">Task mode is one of the important factors that determine scheduling leaf node tasks.</span></span> <span data-ttu-id="44fc1-175">Her görev için iki görev modu vardır: otomatik zamanlama modu ve el ile zamanlama modu.</span><span class="sxs-lookup"><span data-stu-id="44fc1-175">There are two task modes for every task: auto scheduling mode and manual scheduling mode.</span></span>  
  
-   <span data-ttu-id="44fc1-176">**Otomatik zamanlama**.</span><span class="sxs-lookup"><span data-stu-id="44fc1-176">**Auto scheduling**.</span></span>   <span data-ttu-id="44fc1-177">Görev modunu Otomatik Olarak Zamanlandı olarak ayarladığınızda, görev zamanlama altyapısı görev için zamanlamayı belirlemek üzere aşağıdaki görev özniteliklerindeki zamanlama kurallarını kullanır:</span><span class="sxs-lookup"><span data-stu-id="44fc1-177">When you set the task mode to Automatically Scheduled, the task scheduling engine uses the scheduling rules on the following task attributes to determine the schedule for the task:</span></span>  
  
    -   <span data-ttu-id="44fc1-178">Öncüller</span><span class="sxs-lookup"><span data-stu-id="44fc1-178">Predecessors</span></span>  
  
    -   <span data-ttu-id="44fc1-179">Çalışma</span><span class="sxs-lookup"><span data-stu-id="44fc1-179">Effort</span></span>  
  
    -   <span data-ttu-id="44fc1-180">Kaynak sayısı</span><span class="sxs-lookup"><span data-stu-id="44fc1-180">Number of resources</span></span>  
  
    -   <span data-ttu-id="44fc1-181">Başlangıç ve bitiş tarihleri</span><span class="sxs-lookup"><span data-stu-id="44fc1-181">Start and end dates</span></span>  
  
-   <span data-ttu-id="44fc1-182">**Zamanlama kuralları**.</span><span class="sxs-lookup"><span data-stu-id="44fc1-182">**Scheduling rules**.</span></span>   <span data-ttu-id="44fc1-183">Öncülleri olmayan bir yaprak düğüm görevinin başlangıç tarihi, projenin zamanlama başlangıç tarihi olarak varsayılana ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="44fc1-183">The start date of a leaf node task that does not have predecessors defaults to the project’s scheduling start date.</span></span> <span data-ttu-id="44fc1-184">Bir yaprak düğüm görevinin süresi her zaman kendi başlangıç ve bitiş tarihleri arasındaki iş günü sayısı olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="44fc1-184">The duration of a leaf node task is always calculated as the number of working days between its start and end dates.</span></span> <span data-ttu-id="44fc1-185">Bir görev otomatik olarak zamanlandığında, zamanlama altyapısı aşağıdaki kuralları uygular:</span><span class="sxs-lookup"><span data-stu-id="44fc1-185">When a task is automatically scheduled, the scheduling engine follows the rules below:</span></span>  
  
    -   <span data-ttu-id="44fc1-186">Bir görevin başlangıç ve bitiş tarihleri, projenin zamanlama takvimine bağlı olarak her zaman iş günü olmalıdır</span><span class="sxs-lookup"><span data-stu-id="44fc1-186">Start and end dates of a task must always be working days according to the project’s scheduling calendar</span></span>  
  
    -   <span data-ttu-id="44fc1-187">Öncüllere sahip bir görevin başlangıç tarihi öncüllerinin en son bitiş tarihi varsayılanlarına ayarlanır</span><span class="sxs-lookup"><span data-stu-id="44fc1-187">The start date of a task that has predecessors defaults to the latest end date of its predecessors</span></span>  
  
    -   <span data-ttu-id="44fc1-188">Çalışma = Kişi sayısı \* Süre \* saat, proje takviminin standart iş günüdür</span><span class="sxs-lookup"><span data-stu-id="44fc1-188">Effort = Number of people \* Duration \* hours in a standard work day of the project calendar</span></span>  
  
-   <span data-ttu-id="44fc1-189">**El ile zamanlama**.</span><span class="sxs-lookup"><span data-stu-id="44fc1-189">**Manual scheduling**.</span></span>   <span data-ttu-id="44fc1-190">Bazı durumlarda, bu kuralların dışına çıkmak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="44fc1-190">In some cases, you might want to deviate from these rules.</span></span> <span data-ttu-id="44fc1-191">Bu durumlarda, görevin elle zamanlanması için görev modunu ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="44fc1-191">In these cases, you can set the task mode for the task to be manually scheduled.</span></span> <span data-ttu-id="44fc1-192">Bu, zamanlama altyapısının diğer zamanlama özniteliklerinin değerlerini hesaplamayı durdurur.</span><span class="sxs-lookup"><span data-stu-id="44fc1-192">This stops the scheduling engine from calculating the values for other scheduling attributes.</span></span> <span data-ttu-id="44fc1-193">Görevlerdeki öncüllerin ayarlanması her zaman bağımlı görevin başlangıç tarihini etkiler.</span><span class="sxs-lookup"><span data-stu-id="44fc1-193">Setting predecessors on tasks always impacts the dependent task’s start date.</span></span>  
  
## <a name="create-a-work-breakdown-structure"></a><span data-ttu-id="44fc1-194">İş kırılım yapısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="44fc1-194">Create a work breakdown structure</span></span>  
  
1.  <span data-ttu-id="44fc1-195">**Project Service > Projeler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="44fc1-195">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="44fc1-196">Üzerinde çalışmak istediğiniz projeye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="44fc1-196">Click the project you want to work on.</span></span>  
  
3.  <span data-ttu-id="44fc1-197">Ekranın en üstünde bulunan çubukta, proje adının yanındaki aşağı oku seçin ve ardından İş kırılım yapısı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="44fc1-197">In the bar across the top of the screen, select the down arrow next to the project name, and then click Work breakdown structure.</span></span>  
  
4.  <span data-ttu-id="44fc1-198">Bir görev eklemek için, **Görev Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="44fc1-198">To add a task, click **Add Task**.</span></span> <span data-ttu-id="44fc1-199">Görev için alanları doldurun ve **Kaydet** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="44fc1-199">Fill in the fields for the task, and then click **Save**.</span></span>  
  
5.  <span data-ttu-id="44fc1-200">İş kırılım yapınız tamamlanana kadar görev eklemeye devam edin.</span><span class="sxs-lookup"><span data-stu-id="44fc1-200">Continue adding tasks until your work breakdown structure is complete.</span></span> <span data-ttu-id="44fc1-201">İş kırılım yapınızı oluştururken, görevlerinizi düzenlemek için aşağıdakileri yapabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="44fc1-201">While creating your work breakdown structure, you can do the following to organize your tasks:</span></span>  
  
    -   <span data-ttu-id="44fc1-202">Bir görev seçin ve başka bir görevin altına taşımak için **Girintile** ya da bir düzeyden çıkarmak için Çıkıntıla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="44fc1-202">Select a task and click **Indent** to move it under another task or click Outdent to move it out a level.</span></span>  
  
    -   <span data-ttu-id="44fc1-203">Bir görev seçin ve listede aşağı ya da yukarı hareket etmek için **Yukarı Taşı** veya **Aşağı Taşı**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="44fc1-203">Select a task and click **Move Up** or **Move Down** to move it up or down in the list.</span></span>  
  
    -   <span data-ttu-id="44fc1-204">Gantt grafiğini gizlemek için **Gantt'yi gizle**'ye tıklayın ve yeniden görüntülemek için **Gantt'yi göster**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="44fc1-204">Click **Hide Gantt** to hide the Gantt chart, and click **Show Gantt** to display it again.</span></span>  
  
    -   <span data-ttu-id="44fc1-205">**Zaman Ölçeği**'ndeki Gantt grafiği için farklı bir zaman dilimi seçin.</span><span class="sxs-lookup"><span data-stu-id="44fc1-205">Select a different period of time for the Gantt chart in **Time Scale**.</span></span>  
  
6.  <span data-ttu-id="44fc1-206">Projenizin takım üyeleri için iş kırılım yapınızda belirttiğiniz rolleri eklemek üzere, **Proje Takımı Oluştur**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="44fc1-206">To add the roles you specified in your work breakdown structure to your project’s team members, click **Generate Project Team**.</span></span>  
  
7.  <span data-ttu-id="44fc1-207">Değişiklik yapmayı bitirdiğinizde ekranın sağ alt köşesindeki **Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="44fc1-207">Click **Save** at the bottom right corner of the screen when you’re done making changes.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="44fc1-208">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="44fc1-208">See Also</span></span>  
 [<span data-ttu-id="44fc1-209">Proje yöneticisi kılavuzu</span><span class="sxs-lookup"><span data-stu-id="44fc1-209">Project manager guide</span></span>](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]