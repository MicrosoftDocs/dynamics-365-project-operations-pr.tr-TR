---
title: Zamanlama varlıklarıyla işlemler gerçekleştirmek için Zamanlama API'lerini kullanma
description: Bu konu, Zamanlama API'leri kullanımına yönelik bilgiler ve örnekler sağlar.
author: sigitac
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a50a2c6220bb49de8146d0758019827e120e0526
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868153"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="42bd6-103">Zamanlama varlıklarıyla işlemler gerçekleştirmek için Zamanlama API'lerini kullanma</span><span class="sxs-lookup"><span data-stu-id="42bd6-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="42bd6-104">_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="42bd6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="42bd6-105">Bu konuda açıklanan bazı veya tüm işlevler, bir önizleme sürümü kapsamındadır.</span><span class="sxs-lookup"><span data-stu-id="42bd6-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="42bd6-106">İçerik ve işlevsellik değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="42bd6-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="42bd6-107">Zamanlama varlıkları</span><span class="sxs-lookup"><span data-stu-id="42bd6-107">Scheduling entities</span></span>

<span data-ttu-id="42bd6-108">Zamanlama API'leri, **Zamanlama Varlıkları**'yla oluşturma, güncelleştirme ve silme işlemlerini gerçekleştirmeye olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="42bd6-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="42bd6-109">Bu varlıklar, webe yönelik projelerde Zamanlama altyapısı üzerinden yönetilir.</span><span class="sxs-lookup"><span data-stu-id="42bd6-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="42bd6-110">Önceki Dynamics 365 Project Operations sürümlerinde **Zamanlama varlıklarıyla** oluşturma, güncelleştirme ve silme işlemleri kısıtlanmıştı.</span><span class="sxs-lookup"><span data-stu-id="42bd6-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="42bd6-111">Aşağıdaki tabloda, **Zamanlama varlıkları**'nın tam bir listesi verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="42bd6-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="42bd6-112">Varlık adı</span><span class="sxs-lookup"><span data-stu-id="42bd6-112">Entity name</span></span>  | <span data-ttu-id="42bd6-113">Varlık mantıksal adı</span><span class="sxs-lookup"><span data-stu-id="42bd6-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="42bd6-114">Project</span><span class="sxs-lookup"><span data-stu-id="42bd6-114">Project</span></span> | <span data-ttu-id="42bd6-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="42bd6-115">msdyn_project</span></span> |
| <span data-ttu-id="42bd6-116">Proje Görevi</span><span class="sxs-lookup"><span data-stu-id="42bd6-116">Project Task</span></span>  | <span data-ttu-id="42bd6-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="42bd6-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="42bd6-118">Proje Görevi Bağımlılığı</span><span class="sxs-lookup"><span data-stu-id="42bd6-118">Project Task Dependency</span></span>  | <span data-ttu-id="42bd6-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="42bd6-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="42bd6-120">Kaynak Atama</span><span class="sxs-lookup"><span data-stu-id="42bd6-120">Resource Assignment</span></span> | <span data-ttu-id="42bd6-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="42bd6-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="42bd6-122">Proje Demeti</span><span class="sxs-lookup"><span data-stu-id="42bd6-122">Project Bucket</span></span>  | <span data-ttu-id="42bd6-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="42bd6-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="42bd6-124">Proje Takımı Üyesi</span><span class="sxs-lookup"><span data-stu-id="42bd6-124">Project Team Member</span></span> | <span data-ttu-id="42bd6-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="42bd6-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="42bd6-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="42bd6-126">OperationSet</span></span>

<span data-ttu-id="42bd6-127">OperationSet, bir hareket içinde işlenmesi gereken, zamanlamayı etkileyen birkaç isteğin işlenmesi gerektiğinde kullanılabilen bir çalışma birimi düzenidir.</span><span class="sxs-lookup"><span data-stu-id="42bd6-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="42bd6-128">Zamanlama API'leri</span><span class="sxs-lookup"><span data-stu-id="42bd6-128">Schedule APIs</span></span>

<span data-ttu-id="42bd6-129">Aşağıda, mevcut Zamanlama API'lerinin bir listesi verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="42bd6-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="42bd6-130">**msdyn_CreateProjectV1**: Bu API, proje oluşturmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="42bd6-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="42bd6-131">Proje ve varsayılan proje demeti hemen oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="42bd6-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="42bd6-132">**msdyn_CreateTeamMemberV1**: Bu API, proje takımı üyesi oluşturmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="42bd6-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="42bd6-133">Takım üyesi kaydı hemen oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="42bd6-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="42bd6-134">**msdyn_CreateOperationSetV1**: Bu API, bir hareket içinde gerçekleştirilmesi gereken çok sayıda isteği zamanlamak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="42bd6-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="42bd6-135">**msdyn_PSSCreateV1**: Bu API, bir varlık oluşturmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="42bd6-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="42bd6-136">Varlık, oluşturma işlemini destekleyen Zamanlama varlıklarından herhangi biri olabilir.</span><span class="sxs-lookup"><span data-stu-id="42bd6-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="42bd6-137">**msdyn_PSSUpdateV1**: Bu API, bir varlık güncelleştirmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="42bd6-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="42bd6-138">Varlık, güncelleştirme işlemini destekleyen Zamanlama varlıklarından herhangi biri olabilir.</span><span class="sxs-lookup"><span data-stu-id="42bd6-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="42bd6-139">**msdyn_PSSDeleteV1**: Bu API, bir varlığı silmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="42bd6-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="42bd6-140">Varlık, silme işlemini destekleyen Zamanlama varlıklarından herhangi biri olabilir.</span><span class="sxs-lookup"><span data-stu-id="42bd6-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="42bd6-141">**msdyn_ExecuteOperationSetV1**: Bu API, bir işlem kümesindeki tüm işlemleri yürütmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="42bd6-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="42bd6-142">Zamanlama API'lerini OperationSet ile kullanma</span><span class="sxs-lookup"><span data-stu-id="42bd6-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="42bd6-143">Hem **CreateProjectV1** hem de **CreateTeamMemberV1** içeren kayıtlar hemen oluşturulduğundan, bu API'ler doğrudan **OperationSet** içinde kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="42bd6-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="42bd6-144">Ancak API'yi kullanarak gerekli kayıtları oluşturup bir **OperationSet** oluşturabilir ve ardından **OperationSet** içinde bu önceden oluşturulmuş kayıtları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="42bd6-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="42bd6-145">Desteklenen işlemler</span><span class="sxs-lookup"><span data-stu-id="42bd6-145">Supported operations</span></span>

| <span data-ttu-id="42bd6-146">Zamanlama varlığı</span><span class="sxs-lookup"><span data-stu-id="42bd6-146">Scheduling entity</span></span> | <span data-ttu-id="42bd6-147">Oluştur</span><span class="sxs-lookup"><span data-stu-id="42bd6-147">Create</span></span> | <span data-ttu-id="42bd6-148">Güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="42bd6-148">Update</span></span> | <span data-ttu-id="42bd6-149">Delete</span><span class="sxs-lookup"><span data-stu-id="42bd6-149">Delete</span></span> | <span data-ttu-id="42bd6-150">Dikkat edilmesi gereken önemli hususlar</span><span class="sxs-lookup"><span data-stu-id="42bd6-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="42bd6-151">Proje görevi</span><span class="sxs-lookup"><span data-stu-id="42bd6-151">Project task</span></span> | <span data-ttu-id="42bd6-152">Evet</span><span class="sxs-lookup"><span data-stu-id="42bd6-152">Yes</span></span> | <span data-ttu-id="42bd6-153">Evet</span><span class="sxs-lookup"><span data-stu-id="42bd6-153">Yes</span></span> | <span data-ttu-id="42bd6-154">Evet</span><span class="sxs-lookup"><span data-stu-id="42bd6-154">Yes</span></span> | <span data-ttu-id="42bd6-155">Hiçbiri</span><span class="sxs-lookup"><span data-stu-id="42bd6-155">None</span></span> |
| <span data-ttu-id="42bd6-156">Proje görevi bağımlılığı</span><span class="sxs-lookup"><span data-stu-id="42bd6-156">Project task dependency</span></span> | <span data-ttu-id="42bd6-157">Evet</span><span class="sxs-lookup"><span data-stu-id="42bd6-157">Yes</span></span> | <span data-ttu-id="42bd6-158">Evet</span><span class="sxs-lookup"><span data-stu-id="42bd6-158">Yes</span></span> | | <span data-ttu-id="42bd6-159">Proje görev bağımlılığı kayıtları güncelleştirilmemiş.</span><span class="sxs-lookup"><span data-stu-id="42bd6-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="42bd6-160">Bunun yerine, eski bir kayıt silinebilir ve yeni bir kayıt oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="42bd6-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="42bd6-161">Kaynak atama</span><span class="sxs-lookup"><span data-stu-id="42bd6-161">Resource assignment</span></span> | <span data-ttu-id="42bd6-162">Evet</span><span class="sxs-lookup"><span data-stu-id="42bd6-162">Yes</span></span> | <span data-ttu-id="42bd6-163">Evet</span><span class="sxs-lookup"><span data-stu-id="42bd6-163">Yes</span></span> | | <span data-ttu-id="42bd6-164">Şu alanlara sahip işlemler desteklenmez: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** ve **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="42bd6-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="42bd6-165">Kaynak atama kayıtları güncelleştirilmemiş.</span><span class="sxs-lookup"><span data-stu-id="42bd6-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="42bd6-166">Bunun yerine, eski kayıt silinebilir ve yeni bir kayıt oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="42bd6-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="42bd6-167">Proje demeti</span><span class="sxs-lookup"><span data-stu-id="42bd6-167">Project bucket</span></span> | <span data-ttu-id="42bd6-168">Yok</span><span class="sxs-lookup"><span data-stu-id="42bd6-168">N/A</span></span> | <span data-ttu-id="42bd6-169">Yok</span><span class="sxs-lookup"><span data-stu-id="42bd6-169">N/A</span></span> | <span data-ttu-id="42bd6-170">Yok</span><span class="sxs-lookup"><span data-stu-id="42bd6-170">N/A</span></span> | <span data-ttu-id="42bd6-171">Varsayılan demet, **CreateProjectV1** API kullanılarak oluşturulmuş.</span><span class="sxs-lookup"><span data-stu-id="42bd6-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="42bd6-172">Proje takımı üyesi</span><span class="sxs-lookup"><span data-stu-id="42bd6-172">Project team member</span></span> | <span data-ttu-id="42bd6-173">Evet</span><span class="sxs-lookup"><span data-stu-id="42bd6-173">Yes</span></span> | <span data-ttu-id="42bd6-174">Evet</span><span class="sxs-lookup"><span data-stu-id="42bd6-174">Yes</span></span> | <span data-ttu-id="42bd6-175">Evet</span><span class="sxs-lookup"><span data-stu-id="42bd6-175">Yes</span></span> | <span data-ttu-id="42bd6-176">Oluşturma işlemi için **CreateTeamMemberV1** API'sini kullanın.</span><span class="sxs-lookup"><span data-stu-id="42bd6-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="42bd6-177">Project</span><span class="sxs-lookup"><span data-stu-id="42bd6-177">Project</span></span> | <span data-ttu-id="42bd6-178">Evet</span><span class="sxs-lookup"><span data-stu-id="42bd6-178">Yes</span></span> | <span data-ttu-id="42bd6-179">Evet</span><span class="sxs-lookup"><span data-stu-id="42bd6-179">Yes</span></span> | <span data-ttu-id="42bd6-180">Yok</span><span class="sxs-lookup"><span data-stu-id="42bd6-180">N/A</span></span> | <span data-ttu-id="42bd6-181">Şu alanlara sahip işlemler desteklenmez: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** ve **Duration**.</span><span class="sxs-lookup"><span data-stu-id="42bd6-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="42bd6-182">Bu API'ler özel alanlar içeren varlık nesneleriyle çağrılabilir.</span><span class="sxs-lookup"><span data-stu-id="42bd6-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="42bd6-183">Kimlik özelliği isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="42bd6-183">The ID property is optional.</span></span> <span data-ttu-id="42bd6-184">Sağlanmışsa, sistem bunu kullanmayı dener ve kullanılamaz ise bir özel durum oluşturur.</span><span class="sxs-lookup"><span data-stu-id="42bd6-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="42bd6-185">Sağlanmazsa, sistem bunu oluşturacaktır.</span><span class="sxs-lookup"><span data-stu-id="42bd6-185">If it isn't provided, the system will generate it.</span></span>

## <a name="limitations-and-known-issues"></a><span data-ttu-id="42bd6-186">Sınırlamalar ve bilinen sorunlar</span><span class="sxs-lookup"><span data-stu-id="42bd6-186">Limitations and known issues</span></span>
<span data-ttu-id="42bd6-187">Aşağıda, sınırlamalar ve bilinen sorunların bir listesi yer almaktadır:</span><span class="sxs-lookup"><span data-stu-id="42bd6-187">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="42bd6-188">Zamanlama API'leri yalnızca **Microsoft Proje Lisansı olan kullanıcılar** tarafından kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="42bd6-188">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="42bd6-189">Şu kullanıcılar tarafından kullanılamaz:</span><span class="sxs-lookup"><span data-stu-id="42bd6-189">They can't be used by:</span></span>
    - <span data-ttu-id="42bd6-190">Uygulama kullanıcıları</span><span class="sxs-lookup"><span data-stu-id="42bd6-190">Application users</span></span>
    - <span data-ttu-id="42bd6-191">Sistem kullanıcıları</span><span class="sxs-lookup"><span data-stu-id="42bd6-191">System users</span></span>
    - <span data-ttu-id="42bd6-192">Tümleştirme kullanıcıları</span><span class="sxs-lookup"><span data-stu-id="42bd6-192">Integration users</span></span>
    - <span data-ttu-id="42bd6-193">Gerekli lisansa sahip olmayan diğer kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="42bd6-193">Other users that don't have the required license</span></span>
- <span data-ttu-id="42bd6-194">Her bir **OperationSet** yalnızca en fazla 100 işlem içerebilir.</span><span class="sxs-lookup"><span data-stu-id="42bd6-194">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="42bd6-195">Her bir kullanıcının açık en fazla 10 **OperationSet**'i olabilir.</span><span class="sxs-lookup"><span data-stu-id="42bd6-195">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="42bd6-196">Project Operations şu anda bir proje üzerinde en fazla 500 toplam görevi desteklemektedir.</span><span class="sxs-lookup"><span data-stu-id="42bd6-196">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="42bd6-197">**OperationSet** hata durumu ve hata günlükleri şu anda kullanılamıyor.</span><span class="sxs-lookup"><span data-stu-id="42bd6-197">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="42bd6-198">Zamanlama API'leri Genel önizlemededir.</span><span class="sxs-lookup"><span data-stu-id="42bd6-198">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="42bd6-199">Bu API'lerin Üretim ortamlarında kullanımı Microsoft tarafından desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="42bd6-199">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="42bd6-200">Örnek senaryo</span><span class="sxs-lookup"><span data-stu-id="42bd6-200">Sample scenario</span></span>

<span data-ttu-id="42bd6-201">Bu senaryoda; bir proje, bir takım üyesi, dört görev ve iki kaynak ataması oluşturacaksınız.</span><span class="sxs-lookup"><span data-stu-id="42bd6-201">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="42bd6-202">Sonra da tek bir görevi güncelleştirecek, projeyi güncelleştirecek, tek bir görevi silecek, bir kaynak atamasını silecek ve bir görev bağımlılığı oluşturacaksınız.</span><span class="sxs-lookup"><span data-stu-id="42bd6-202">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```C#
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ";, projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment"R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

varassignment1Response = CallPssCreateAction(assignment1, operationSetId);
varassignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

varassignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="42bd6-203">Ek örnekler</span><span class="sxs-lookup"><span data-stu-id="42bd6-203">Additional samples</span></span>

```C#
#region Call actions 

///<summary>
/// Calls the action to create an operationSet
/// </summary>
/// <paramname="projectId">project id for the operations to be included in this operationSet>/param>
/// <paramname="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
privatestring CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary<
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// <summary>
/// <paramname="recordId">Id of the record to be deleted</param>
/// <paramname="entityLogicalName">Entity logical name of the record</param>
/// <paramname="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// <summary>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <paramname="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1";
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);

    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <paramname="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
privatestring CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject><OperationSetResponse>
    ((string)orgResponse.Results["OperationSetResponse";]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet(";msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };
    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
    return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";
    return project;
}

private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort";] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
        task["new_custom1"] = "Just my test";
        task[";new_age"] = 98;
        task["new_amount"] = 591.34m;
        task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }
    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;
    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);
    return taskDependency;
}

#endregion

#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
publicclassOperationSetResponse
{
    [DataMember(Name = "operationSetId")]
    public Guid OperationSetId { get; set; }

    [DataMember(Name = "operationSetDetailId")]
    public Guid OperationSetDetailId { get; set; }

    [DataMember(Name = "operationType")]
    publicstring OperationType { get; set; }

    [DataMember(Name = "recordId")]
    publicstring RecordId { get; set; }

    [DataMember(Name = "correlationId")]
    publicstring CorrelationId { get; set; }
}

#endregion
```
