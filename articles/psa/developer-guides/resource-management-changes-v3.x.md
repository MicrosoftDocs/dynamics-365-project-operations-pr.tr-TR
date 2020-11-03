---
title: Kaynak yöneticisi değişiklikleri (Project Service Automation 3.x)
description: Bu konu, Kaynak yönetimi alanındaki değişiklikler hakkında bilgi sağlar.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 5176d2c6b7b00d47d4aeb12f54bdb84d4b87304c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086515"
---
# <a name="resource-management-changes-project-service-automation-3x"></a><span data-ttu-id="87731-103">Kaynak yöneticisi değişiklikleri (Project Service Automation 3.x)</span><span class="sxs-lookup"><span data-stu-id="87731-103">Resource management changes (Project Service Automation 3.x)</span></span>

<span data-ttu-id="87731-104">Bu konunun bölümleri, Dynamics 365 Project Service Automation sürüm 3.x'in Kaynak yönetimi alanında yapılan değişiklikler hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="87731-104">The sections of this topic provide information about the changes that have been made to the Resource management area of Dynamics 365 Project Service Automation version 3.x.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="87731-105">Proje tahminleri</span><span class="sxs-lookup"><span data-stu-id="87731-105">Project estimates</span></span>

<span data-ttu-id="87731-106">Proje tahminleri **msdyn\_projecttask** varlığını ( **Proje Görevi** ) temel almak yerine **msdyn\_resourceassignment** varlığını ( **Kaynak Atama** ) temel alır.</span><span class="sxs-lookup"><span data-stu-id="87731-106">Instead of being based on the **msdyn\_projecttask** entity ( **Project Task** ), project estimates are based on the **msdyn\_resourceassignment** entity ( **Resource Assignment** ).</span></span> <span data-ttu-id="87731-107">Kaynak atamaları, görev zamanlama ve fiyatlandırma için "gerçeğin kaynağı" haline geldi.</span><span class="sxs-lookup"><span data-stu-id="87731-107">Resource assignments have become the "source of truth" for task scheduling and pricing.</span></span>

## <a name="line-tasks"></a><span data-ttu-id="87731-108">Satır görevleri</span><span class="sxs-lookup"><span data-stu-id="87731-108">Line tasks</span></span>

<span data-ttu-id="87731-109">PSA 3.x'te satır görevleri güncel değildir (kullanım dışı).</span><span class="sxs-lookup"><span data-stu-id="87731-109">In PSA 3.x, line tasks are obsolete (deprecated).</span></span> <span data-ttu-id="87731-110">Atamalar artık satır görevleri yerine tüm görevi işaret eder.</span><span class="sxs-lookup"><span data-stu-id="87731-110">Assignments now point to the whole task instead of the line tasks.</span></span>

<span data-ttu-id="87731-111">Aşağıdaki örnek, "Test görevi" adlı bir görevin, A ve B takım üyelerine PSA'nın önceki sürümlerinde ve PSA 3.x'te nasıl atandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="87731-111">The following example shows how a task that is named "Test task" is assigned to team members A and B in earlier versions of PSA and in PSA 3.x.</span></span>

- <span data-ttu-id="87731-112">**PSA 3.x'ten önce:**</span><span class="sxs-lookup"><span data-stu-id="87731-112">**Before PSA 3.x:**</span></span>

    - <span data-ttu-id="87731-113">Test görevi</span><span class="sxs-lookup"><span data-stu-id="87731-113">Test task</span></span>

        - <span data-ttu-id="87731-114">Test görevi – Satır görevi 1</span><span class="sxs-lookup"><span data-stu-id="87731-114">Test task – Line task 1</span></span>

            - <span data-ttu-id="87731-115">A'ya Atama</span><span class="sxs-lookup"><span data-stu-id="87731-115">Assignment to A</span></span>

        - <span data-ttu-id="87731-116">Test görevi – Satır görevi 2</span><span class="sxs-lookup"><span data-stu-id="87731-116">Test task – Line task 2</span></span>

            - <span data-ttu-id="87731-117">B'ye Atama</span><span class="sxs-lookup"><span data-stu-id="87731-117">Assignment to B</span></span>

- <span data-ttu-id="87731-118">**PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="87731-118">**PSA 3.x:**</span></span>

    - <span data-ttu-id="87731-119">Test görevi</span><span class="sxs-lookup"><span data-stu-id="87731-119">Test task</span></span>

        - <span data-ttu-id="87731-120">A'ya Atama</span><span class="sxs-lookup"><span data-stu-id="87731-120">Assignment to A</span></span>
        - <span data-ttu-id="87731-121">B'ye Atama</span><span class="sxs-lookup"><span data-stu-id="87731-121">Assignment to B</span></span>

## <a name="unassigned-assignment"></a><span data-ttu-id="87731-122">Atanmamış atama</span><span class="sxs-lookup"><span data-stu-id="87731-122">Unassigned assignment</span></span>

<span data-ttu-id="87731-123">PSA 3.x'te atanmamış bir atama, bir **BOŞ** takım üyesine ve bir **BOŞ** kaynağa atanmış bir atamadır.</span><span class="sxs-lookup"><span data-stu-id="87731-123">In PSA 3.x, an unassigned assignment is an assignment that is assigned to a **NULL** team member and a **NULL** resource.</span></span> <span data-ttu-id="87731-124">Atanmamış atamalar birkaç senaryoda gerçekleşebilir:</span><span class="sxs-lookup"><span data-stu-id="87731-124">Unassigned assignments can occur in a couple of scenarios:</span></span>

- <span data-ttu-id="87731-125">Bir görev oluşturulmuş ancak henüz herhangi bir takım üyesine atanmamışsa, atanmamış bir atama her zaman oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="87731-125">If a task has been created, but it hasn't yet been assigned to any team member, an unassigned assignment is always created.</span></span> 
- <span data-ttu-id="87731-126">Bir görevdeki tüm atamalar kaldırılırsa bu görev için atanmamış bir atama yeniden oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="87731-126">If all assignees on a task are removed, an unassigned assignment is re-created for that task.</span></span>

## <a name="scheduling-fields-on-the-project-task-entity"></a><span data-ttu-id="87731-127">Proje Görevi varlığındaki zamanlama alanları</span><span class="sxs-lookup"><span data-stu-id="87731-127">Scheduling fields on the Project Task entity</span></span>

<span data-ttu-id="87731-128">**msdyn\_projecttask** varlığındaki alanlar kullanım dışı bırakıldı veya **msdyn\_resourceassignment** varlığına taşındı ya da bu alanlara artık **msdyn\_projectteam** varlığından ( **Proje Takım Üyesi** ) başvuruluyor.</span><span class="sxs-lookup"><span data-stu-id="87731-128">The fields on the **msdyn\_projecttask** entity have been deprecated or moved to the **msdyn\_resourceassignment** entity, or they are now referenced from the **msdyn\_projectteam** entity ( **Project Team Member** ).</span></span>

| <span data-ttu-id="87731-129">msdyn\_projecttask (Proje Görevi) varlığındaki kullanım dışı alan</span><span class="sxs-lookup"><span data-stu-id="87731-129">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="87731-130">msdyn\_resourceassignment (Kaynak Atama) varlığındaki yeni alan</span><span class="sxs-lookup"><span data-stu-id="87731-130">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> | <span data-ttu-id="87731-131">Açıklama</span><span class="sxs-lookup"><span data-stu-id="87731-131">Comment</span></span> |
|---|---|---|
| <span data-ttu-id="87731-132">msdyn\_assignedresources</span><span class="sxs-lookup"><span data-stu-id="87731-132">msdyn\_assignedresources</span></span> | <span data-ttu-id="87731-133">Yok</span><span class="sxs-lookup"><span data-stu-id="87731-133">None</span></span> | |
| <span data-ttu-id="87731-134">msdyn\_assignedteammembers</span><span class="sxs-lookup"><span data-stu-id="87731-134">msdyn\_assignedteammembers</span></span> | <span data-ttu-id="87731-135">Yok</span><span class="sxs-lookup"><span data-stu-id="87731-135">None</span></span> | |
| <span data-ttu-id="87731-136">msdyn\_numberofresources</span><span class="sxs-lookup"><span data-stu-id="87731-136">msdyn\_numberofresources</span></span> | <span data-ttu-id="87731-137">Yok</span><span class="sxs-lookup"><span data-stu-id="87731-137">None</span></span> | |
| <span data-ttu-id="87731-138">msdyn\_scheduledhours</span><span class="sxs-lookup"><span data-stu-id="87731-138">msdyn\_scheduledhours</span></span> | <span data-ttu-id="87731-139">Yok</span><span class="sxs-lookup"><span data-stu-id="87731-139">None</span></span> | |
| <span data-ttu-id="87731-140">msdyn\_effortcontour</span><span class="sxs-lookup"><span data-stu-id="87731-140">msdyn\_effortcontour</span></span> | <span data-ttu-id="87731-141">msdyn\_plannedwork</span><span class="sxs-lookup"><span data-stu-id="87731-141">msdyn\_plannedwork</span></span> | <span data-ttu-id="87731-142">Alanda saklanan JavaScript Nesne Gösterimi (JSON) veri yapısının biçimi değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="87731-142">The format of the JavaScript Object Notation (JSON) data structure that is stored in the field has been changed.</span></span> |

## <a name="schedule-contour"></a><span data-ttu-id="87731-143">Zamanlama sınırı</span><span class="sxs-lookup"><span data-stu-id="87731-143">Schedule contour</span></span>

<span data-ttu-id="87731-144">Zamanlama sınırı her **Kaynak Atama** varlığının ( **msdyn\_resourceassignment** ) **Planlanan İş** alanında ( **msdyn\_plannedwork** ) depolanır.</span><span class="sxs-lookup"><span data-stu-id="87731-144">The schedule contour is stored in the **Planned Work** field ( **msdyn\_plannedwork** ) of each **Resource Assignment** entity ( **msdyn\_resourceassignment** ).</span></span>

### <a name="structure"></a><span data-ttu-id="87731-145">Yapı</span><span class="sxs-lookup"><span data-stu-id="87731-145">Structure</span></span>

<span data-ttu-id="87731-146">Zamanlama sınırının yeni yapısı, zamanlamanın her günü için tanımlanan esnek zaman dilimlerinden oluşur.</span><span class="sxs-lookup"><span data-stu-id="87731-146">The new structure of the schedule contour consists of flexible time slices that are defined for each day of the schedule.</span></span> <span data-ttu-id="87731-147">Her zaman dilimi aşağıdaki özellikleri sahiptir:</span><span class="sxs-lookup"><span data-stu-id="87731-147">Each time slice has the following properties:</span></span>

- <span data-ttu-id="87731-148">**Başlangıç** : Proje takvimine göre günün çalışma saatlerinin başlangıcı.</span><span class="sxs-lookup"><span data-stu-id="87731-148">**Start** – The start of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="87731-149">**Bitiş** : Proje takvimine göre günün çalışma saatlerinin bitişi.</span><span class="sxs-lookup"><span data-stu-id="87731-149">**End** – The end of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="87731-150">**Saatler** : Günde atanan saat sayısı.</span><span class="sxs-lookup"><span data-stu-id="87731-150">**Hours** – The number of hours that are assigned on the day.</span></span>

<span data-ttu-id="87731-151">**Örnek**</span><span class="sxs-lookup"><span data-stu-id="87731-151">**Example**</span></span>

<span data-ttu-id="87731-152">Bu örnek, UTC-8 saat diliminde iş gününün sabah 9'dan akşam 5'e kadar olduğu bir proje takvimi kullanır.</span><span class="sxs-lookup"><span data-stu-id="87731-152">This example uses a project calendar where the workday is from 9 AM to 5 PM in the UTC-8 time zone.</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a><span data-ttu-id="87731-153">Otomatik zamanlama ve el ile zamanlama</span><span class="sxs-lookup"><span data-stu-id="87731-153">Auto-scheduling and manual scheduling</span></span>

<span data-ttu-id="87731-154">Görev otomatik zamanlanmışsa saatler ön yüklemelidir ve görev süresi azaltılabilir.</span><span class="sxs-lookup"><span data-stu-id="87731-154">If a task is auto-scheduled, the hours are front-loaded, and the task duration might be reduced.</span></span>

<span data-ttu-id="87731-155">**Örnek**</span><span class="sxs-lookup"><span data-stu-id="87731-155">**Example**</span></span>

<span data-ttu-id="87731-156">Aşağıdaki görev, üç günde 18 saat için otomatik zamanlanmıştır (3 Aralık 2018 - 5 Aralık 2018).</span><span class="sxs-lookup"><span data-stu-id="87731-156">The following task is auto-scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

<span data-ttu-id="87731-157">Görev el ile zamanlanırsa saatler tüm tarihlere eşit olarak dağıtılır.</span><span class="sxs-lookup"><span data-stu-id="87731-157">If a task is manually scheduled, the hours are evenly distributed to all the dates.</span></span>

<span data-ttu-id="87731-158">**Örnek**</span><span class="sxs-lookup"><span data-stu-id="87731-158">**Example**</span></span>

<span data-ttu-id="87731-159">Aşağıdaki görev, üç günde 18 saat için el ile zamanlanmıştır (3 Aralık 2018 - 5 Aralık 2018).</span><span class="sxs-lookup"><span data-stu-id="87731-159">The following task is manually scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a><span data-ttu-id="87731-160">Atama birimi</span><span class="sxs-lookup"><span data-stu-id="87731-160">Assignment unit</span></span>

<span data-ttu-id="87731-161">PSA 3.x'te atama birimi kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="87731-161">The assignment unit has been deprecated in PSA 3.x.</span></span> <span data-ttu-id="87731-162">Görev çalışma saatleri artık tüm atanan kaynaklar arasında her gün eşit olarak bölünür.</span><span class="sxs-lookup"><span data-stu-id="87731-162">The task effort hours are now equally divided, per day, among all the assigned resources.</span></span>

<span data-ttu-id="87731-163">**Örnek**</span><span class="sxs-lookup"><span data-stu-id="87731-163">**Example**</span></span>

<span data-ttu-id="87731-164">Bu örnekte, görev iki kaynağa atanmıştır ve üç günde 36 saat için (3 Aralık 2018 - 5 Aralık 2018) otomatik olarak zamanlanır.</span><span class="sxs-lookup"><span data-stu-id="87731-164">In this example, the task is is assigned to two resources and is auto-scheduled for 36 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

- <span data-ttu-id="87731-165">Atama 1:</span><span class="sxs-lookup"><span data-stu-id="87731-165">Assignment 1:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- <span data-ttu-id="87731-166">Atama 2:</span><span class="sxs-lookup"><span data-stu-id="87731-166">Assignment 2:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a><span data-ttu-id="87731-167">Fiyatlandırma boyutları</span><span class="sxs-lookup"><span data-stu-id="87731-167">Pricing dimensions</span></span>

<span data-ttu-id="87731-168">PSA 3.x'te, kaynağa özel fiyatlandırma boyutu alanları ( **Rol** ve **Kuruluş Birimi** ), **msdyn\_projecttask** varlığından kaldırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="87731-168">In PSA 3.x, resource-specific pricing dimension fields (such as **Role** and **Organizational Unit** ) have been removed from the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="87731-169">Bu alanlar artık proje tahminleri üretildiğinde kaynak atamasının ( **msdyn\_resourceassignment** ) ilgili proje takımı üyesinden ( **msdyn\_projectteam** ) alınabilir.</span><span class="sxs-lookup"><span data-stu-id="87731-169">These fields can now be retrieved from the corresponding project team member ( **msdyn\_projectteam** ) of the resource assignment ( **msdyn\_resourceassignment** ) when project estimates are generated.</span></span> <span data-ttu-id="87731-170">**msdyn\_projectteam** varlığına yeni bir alan ( **msdyn\_organizationalunit** ) eklendi.</span><span class="sxs-lookup"><span data-stu-id="87731-170">A new field, **msdyn\_organizationalunit** , has been added to the **msdyn\_projectteam** entity.</span></span>

| <span data-ttu-id="87731-171">msdyn\_projecttask (Proje Görevi) varlığındaki kullanım dışı alan</span><span class="sxs-lookup"><span data-stu-id="87731-171">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="87731-172">Bunun yerine msdyn\_projectteam varlığından (Proje Takımı Üyesi) kullanılan alan</span><span class="sxs-lookup"><span data-stu-id="87731-172">Field from msdyn\_projectteam (Project Team Member) that is used instead</span></span> |
|---|---|
| <span data-ttu-id="87731-173">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="87731-173">msdyn\_resourcecategory</span></span> | <span data-ttu-id="87731-174">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="87731-174">msdyn\_resourcecategory</span></span> |
| <span data-ttu-id="87731-175">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="87731-175">msdyn\_organizationalunit</span></span> | <span data-ttu-id="87731-176">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="87731-176">msdyn\_organizationalunit</span></span> |

## <a name="contours"></a><span data-ttu-id="87731-177">Sınırlar</span><span class="sxs-lookup"><span data-stu-id="87731-177">Contours</span></span>

<span data-ttu-id="87731-178">Fiyatlandırma ve tahmin sınırı alanları **msdyn\_projecttask** varlığında kullanım dışı bırakılmıştır.</span><span class="sxs-lookup"><span data-stu-id="87731-178">The pricing and estimation contour fields have been deprecated on the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="87731-179">Bunlar **msdyn\_resourceassignment** varlığına taşınmıştır.</span><span class="sxs-lookup"><span data-stu-id="87731-179">They have been moved to the **msdyn\_resourceassignment** entity.</span></span>

| <span data-ttu-id="87731-180">msdyn\_projecttask (Proje Görevi) varlığındaki kullanım dışı alan</span><span class="sxs-lookup"><span data-stu-id="87731-180">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="87731-181">msdyn\_resourceassignment (Kaynak Atama) varlığındaki yeni alan</span><span class="sxs-lookup"><span data-stu-id="87731-181">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> |
|---|---|
| <span data-ttu-id="87731-182">msdyn\_costestimatecontour</span><span class="sxs-lookup"><span data-stu-id="87731-182">msdyn\_costestimatecontour</span></span> | <span data-ttu-id="87731-183">msdyn\_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="87731-183">msdyn\_plannedcostcontour</span></span> |
| <span data-ttu-id="87731-184">msdyn\_salesestimatecontour</span><span class="sxs-lookup"><span data-stu-id="87731-184">msdyn\_salesestimatecontour</span></span> | <span data-ttu-id="87731-185">msdyn\_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="87731-185">msdyn\_plannedsalescontour</span></span> |

<span data-ttu-id="87731-186">Aşağıdaki alanlar **msdyn\_resourceassignment** varlığına eklenmiştir:</span><span class="sxs-lookup"><span data-stu-id="87731-186">The following fields have been added to the **msdyn\_resourceassignment** entity:</span></span>

* <span data-ttu-id="87731-187">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="87731-187">msdyn\_plannedcost</span></span>
* <span data-ttu-id="87731-188">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="87731-188">msdyn\_plannedsales</span></span>

<span data-ttu-id="87731-189">**msdyn\_projecttask** varlığındaki planlanan, gerçek ve kalan maliyet ve satışlar için aşağıdaki alanlar değişmemiştir:</span><span class="sxs-lookup"><span data-stu-id="87731-189">The following fields for planned, actual, and remaining cost and sales are unchanged on the **msdyn\_projecttask** entity:</span></span>

* <span data-ttu-id="87731-190">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="87731-190">msdyn\_plannedcost</span></span>
* <span data-ttu-id="87731-191">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="87731-191">msdyn\_plannedsales</span></span>
* <span data-ttu-id="87731-192">msdyn\_actualcost</span><span class="sxs-lookup"><span data-stu-id="87731-192">msdyn\_actualcost</span></span>
* <span data-ttu-id="87731-193">msdyn\_actualsales</span><span class="sxs-lookup"><span data-stu-id="87731-193">msdyn\_actualsales</span></span>
* <span data-ttu-id="87731-194">msdyn\_remainingcost</span><span class="sxs-lookup"><span data-stu-id="87731-194">msdyn\_remainingcost</span></span>
* <span data-ttu-id="87731-195">msdyn\_remainingsales</span><span class="sxs-lookup"><span data-stu-id="87731-195">msdyn\_remainingsales</span></span>
