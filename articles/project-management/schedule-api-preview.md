---
title: Zamanlama varlıklarıyla işlemler gerçekleştirmek için Zamanlama API'lerini kullanma
description: Bu konu, Zamanlama API'leri kullanımına yönelik bilgiler ve örnekler sağlar.
author: sigitac
manager: Annbe
ms.date: 04/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e03f4e6c49a835206b23cade3fabe3fd26693441
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950828"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="decb8-103">Zamanlama varlıklarıyla işlemler gerçekleştirmek için Zamanlama API'lerini kullanma</span><span class="sxs-lookup"><span data-stu-id="decb8-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="decb8-104">_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="decb8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="decb8-105">Bu konuda açıklanan bazı veya tüm işlevler, bir önizleme sürümü kapsamındadır.</span><span class="sxs-lookup"><span data-stu-id="decb8-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="decb8-106">İçerik ve işlevsellik değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="decb8-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="decb8-107">Zamanlama varlıkları</span><span class="sxs-lookup"><span data-stu-id="decb8-107">Scheduling entities</span></span>

<span data-ttu-id="decb8-108">Zamanlama API'leri, **Zamanlama Varlıkları**'yla oluşturma, güncelleştirme ve silme işlemlerini gerçekleştirmeye olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="decb8-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="decb8-109">Bu varlıklar, webe yönelik projelerde Zamanlama altyapısı üzerinden yönetilir.</span><span class="sxs-lookup"><span data-stu-id="decb8-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="decb8-110">Önceki Dynamics 365 Project Operations sürümlerinde **Zamanlama varlıklarıyla** oluşturma, güncelleştirme ve silme işlemleri kısıtlanmıştı.</span><span class="sxs-lookup"><span data-stu-id="decb8-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="decb8-111">Aşağıdaki tabloda, **Zamanlama varlıkları**'nın tam bir listesi verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="decb8-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="decb8-112">Varlık adı</span><span class="sxs-lookup"><span data-stu-id="decb8-112">Entity name</span></span>  | <span data-ttu-id="decb8-113">Varlık mantıksal adı</span><span class="sxs-lookup"><span data-stu-id="decb8-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="decb8-114">Project</span><span class="sxs-lookup"><span data-stu-id="decb8-114">Project</span></span> | <span data-ttu-id="decb8-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="decb8-115">msdyn_project</span></span> |
| <span data-ttu-id="decb8-116">Proje Görevi</span><span class="sxs-lookup"><span data-stu-id="decb8-116">Project Task</span></span>  | <span data-ttu-id="decb8-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="decb8-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="decb8-118">Proje Görevi Bağımlılığı</span><span class="sxs-lookup"><span data-stu-id="decb8-118">Project Task Dependency</span></span>  | <span data-ttu-id="decb8-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="decb8-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="decb8-120">Kaynak Atama</span><span class="sxs-lookup"><span data-stu-id="decb8-120">Resource Assignment</span></span> | <span data-ttu-id="decb8-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="decb8-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="decb8-122">Proje Demeti</span><span class="sxs-lookup"><span data-stu-id="decb8-122">Project Bucket</span></span>  | <span data-ttu-id="decb8-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="decb8-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="decb8-124">Proje Takımı Üyesi</span><span class="sxs-lookup"><span data-stu-id="decb8-124">Project Team Member</span></span> | <span data-ttu-id="decb8-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="decb8-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="decb8-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="decb8-126">OperationSet</span></span>

<span data-ttu-id="decb8-127">OperationSet, bir hareket içinde işlenmesi gereken, zamanlamayı etkileyen birkaç isteğin işlenmesi gerektiğinde kullanılabilen bir çalışma birimi düzenidir.</span><span class="sxs-lookup"><span data-stu-id="decb8-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="decb8-128">Zamanlama API'leri</span><span class="sxs-lookup"><span data-stu-id="decb8-128">Schedule APIs</span></span>

<span data-ttu-id="decb8-129">Aşağıda, mevcut Zamanlama API'lerinin bir listesi verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="decb8-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="decb8-130">**msdyn_CreateProjectV1**: Bu API, proje oluşturmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="decb8-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="decb8-131">Proje ve varsayılan proje demeti hemen oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="decb8-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="decb8-132">**msdyn_CreateTeamMemberV1**: Bu API, proje takımı üyesi oluşturmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="decb8-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="decb8-133">Takım üyesi kaydı hemen oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="decb8-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="decb8-134">**msdyn_CreateOperationSetV1**: Bu API, bir hareket içinde gerçekleştirilmesi gereken çok sayıda isteği zamanlamak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="decb8-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="decb8-135">**msdyn_PSSCreateV1**: Bu API, bir varlık oluşturmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="decb8-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="decb8-136">Varlık, oluşturma işlemini destekleyen Zamanlama varlıklarından herhangi biri olabilir.</span><span class="sxs-lookup"><span data-stu-id="decb8-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="decb8-137">**msdyn_PSSUpdateV1**: Bu API, bir varlık güncelleştirmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="decb8-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="decb8-138">Varlık, güncelleştirme işlemini destekleyen Zamanlama varlıklarından herhangi biri olabilir.</span><span class="sxs-lookup"><span data-stu-id="decb8-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="decb8-139">**msdyn_PSSDeleteV1**: Bu API, bir varlığı silmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="decb8-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="decb8-140">Varlık, silme işlemini destekleyen Zamanlama varlıklarından herhangi biri olabilir.</span><span class="sxs-lookup"><span data-stu-id="decb8-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="decb8-141">**msdyn_ExecuteOperationSetV1**: Bu API, bir işlem kümesindeki tüm işlemleri yürütmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="decb8-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="decb8-142">Zamanlama API'lerini OperationSet ile kullanma</span><span class="sxs-lookup"><span data-stu-id="decb8-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="decb8-143">Hem **CreateProjectV1** hem de **CreateTeamMemberV1** içeren kayıtlar hemen oluşturulduğundan, bu API'ler doğrudan **OperationSet** içinde kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="decb8-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="decb8-144">Ancak API'yi kullanarak gerekli kayıtları oluşturup bir **OperationSet** oluşturabilir ve ardından **OperationSet** içinde bu önceden oluşturulmuş kayıtları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="decb8-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="decb8-145">Desteklenen işlemler</span><span class="sxs-lookup"><span data-stu-id="decb8-145">Supported operations</span></span>

| <span data-ttu-id="decb8-146">Zamanlama varlığı</span><span class="sxs-lookup"><span data-stu-id="decb8-146">Scheduling entity</span></span> | <span data-ttu-id="decb8-147">Oluştur</span><span class="sxs-lookup"><span data-stu-id="decb8-147">Create</span></span> | <span data-ttu-id="decb8-148">Güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="decb8-148">Update</span></span> | <span data-ttu-id="decb8-149">Delete</span><span class="sxs-lookup"><span data-stu-id="decb8-149">Delete</span></span> | <span data-ttu-id="decb8-150">Dikkat edilmesi gereken önemli hususlar</span><span class="sxs-lookup"><span data-stu-id="decb8-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="decb8-151">Proje görevi</span><span class="sxs-lookup"><span data-stu-id="decb8-151">Project task</span></span> | <span data-ttu-id="decb8-152">Evet</span><span class="sxs-lookup"><span data-stu-id="decb8-152">Yes</span></span> | <span data-ttu-id="decb8-153">Evet</span><span class="sxs-lookup"><span data-stu-id="decb8-153">Yes</span></span> | <span data-ttu-id="decb8-154">Evet</span><span class="sxs-lookup"><span data-stu-id="decb8-154">Yes</span></span> | <span data-ttu-id="decb8-155">Hiçbiri</span><span class="sxs-lookup"><span data-stu-id="decb8-155">None</span></span> |
| <span data-ttu-id="decb8-156">Proje görevi bağımlılığı</span><span class="sxs-lookup"><span data-stu-id="decb8-156">Project task dependency</span></span> | <span data-ttu-id="decb8-157">Evet</span><span class="sxs-lookup"><span data-stu-id="decb8-157">Yes</span></span> | <span data-ttu-id="decb8-158">Evet</span><span class="sxs-lookup"><span data-stu-id="decb8-158">Yes</span></span> | | <span data-ttu-id="decb8-159">Proje görev bağımlılığı kayıtları güncelleştirilmemiş.</span><span class="sxs-lookup"><span data-stu-id="decb8-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="decb8-160">Bunun yerine, eski bir kayıt silinebilir ve yeni bir kayıt oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="decb8-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="decb8-161">Kaynak atama</span><span class="sxs-lookup"><span data-stu-id="decb8-161">Resource assignment</span></span> | <span data-ttu-id="decb8-162">Evet</span><span class="sxs-lookup"><span data-stu-id="decb8-162">Yes</span></span> | <span data-ttu-id="decb8-163">Evet</span><span class="sxs-lookup"><span data-stu-id="decb8-163">Yes</span></span> | | <span data-ttu-id="decb8-164">Şu alanlara sahip işlemler desteklenmez: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** ve **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="decb8-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="decb8-165">Kaynak atama kayıtları güncelleştirilmemiş.</span><span class="sxs-lookup"><span data-stu-id="decb8-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="decb8-166">Bunun yerine, eski kayıt silinebilir ve yeni bir kayıt oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="decb8-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="decb8-167">Proje demeti</span><span class="sxs-lookup"><span data-stu-id="decb8-167">Project bucket</span></span> | <span data-ttu-id="decb8-168">Yok</span><span class="sxs-lookup"><span data-stu-id="decb8-168">N/A</span></span> | <span data-ttu-id="decb8-169">Yok</span><span class="sxs-lookup"><span data-stu-id="decb8-169">N/A</span></span> | <span data-ttu-id="decb8-170">Yok</span><span class="sxs-lookup"><span data-stu-id="decb8-170">N/A</span></span> | <span data-ttu-id="decb8-171">Varsayılan demet, **CreateProjectV1** API kullanılarak oluşturulmuş.</span><span class="sxs-lookup"><span data-stu-id="decb8-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="decb8-172">Proje takımı üyesi</span><span class="sxs-lookup"><span data-stu-id="decb8-172">Project team member</span></span> | <span data-ttu-id="decb8-173">Evet</span><span class="sxs-lookup"><span data-stu-id="decb8-173">Yes</span></span> | <span data-ttu-id="decb8-174">Evet</span><span class="sxs-lookup"><span data-stu-id="decb8-174">Yes</span></span> | <span data-ttu-id="decb8-175">Evet</span><span class="sxs-lookup"><span data-stu-id="decb8-175">Yes</span></span> | <span data-ttu-id="decb8-176">Oluşturma işlemi için **CreateTeamMemberV1** API'sini kullanın.</span><span class="sxs-lookup"><span data-stu-id="decb8-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="decb8-177">Project</span><span class="sxs-lookup"><span data-stu-id="decb8-177">Project</span></span> | <span data-ttu-id="decb8-178">Evet</span><span class="sxs-lookup"><span data-stu-id="decb8-178">Yes</span></span> | <span data-ttu-id="decb8-179">Evet</span><span class="sxs-lookup"><span data-stu-id="decb8-179">Yes</span></span> | <span data-ttu-id="decb8-180">Yok</span><span class="sxs-lookup"><span data-stu-id="decb8-180">N/A</span></span> | <span data-ttu-id="decb8-181">Şu alanlara sahip işlemler desteklenmez: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** ve **Duration**.</span><span class="sxs-lookup"><span data-stu-id="decb8-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="decb8-182">Bu API'ler özel alanlar içeren varlık nesneleriyle çağrılabilir.</span><span class="sxs-lookup"><span data-stu-id="decb8-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="decb8-183">Kimlik özelliği isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="decb8-183">The ID property is optional.</span></span> <span data-ttu-id="decb8-184">Sağlanmışsa, sistem bunu kullanmayı dener ve kullanılamaz ise bir özel durum oluşturur.</span><span class="sxs-lookup"><span data-stu-id="decb8-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="decb8-185">Sağlanmazsa, sistem bunu oluşturacaktır.</span><span class="sxs-lookup"><span data-stu-id="decb8-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="decb8-186">Sınırlandırılmış alanlar</span><span class="sxs-lookup"><span data-stu-id="decb8-186">Restricted fields</span></span>

<span data-ttu-id="decb8-187">Aşağıdaki tablolarda, **oluşturma** ve **düzenleme** için kısıtlanan alanlar tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="decb8-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="decb8-188">Proje görevi</span><span class="sxs-lookup"><span data-stu-id="decb8-188">Project task</span></span>

| <span data-ttu-id="decb8-189">**Mantıksal ad**</span><span class="sxs-lookup"><span data-stu-id="decb8-189">**Logical name**</span></span>                       | <span data-ttu-id="decb8-190">**Oluşturabilir**</span><span class="sxs-lookup"><span data-stu-id="decb8-190">**Can create**</span></span> | <span data-ttu-id="decb8-191">**Düzenleyebilir**</span><span class="sxs-lookup"><span data-stu-id="decb8-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="decb8-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="decb8-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="decb8-193">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-193">no</span></span>             | <span data-ttu-id="decb8-194">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-194">no</span></span>               |
| <span data-ttu-id="decb8-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="decb8-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="decb8-196">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-196">no</span></span>             | <span data-ttu-id="decb8-197">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-197">no</span></span>               |
| <span data-ttu-id="decb8-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="decb8-198">msdyn_actualend</span></span>                        | <span data-ttu-id="decb8-199">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-199">no</span></span>             | <span data-ttu-id="decb8-200">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-200">no</span></span>               |
| <span data-ttu-id="decb8-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="decb8-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="decb8-202">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-202">no</span></span>             | <span data-ttu-id="decb8-203">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-203">no</span></span>               |
| <span data-ttu-id="decb8-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="decb8-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="decb8-205">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-205">no</span></span>             | <span data-ttu-id="decb8-206">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-206">no</span></span>               |
| <span data-ttu-id="decb8-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="decb8-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="decb8-208">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-208">no</span></span>             | <span data-ttu-id="decb8-209">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-209">no</span></span>               |
| <span data-ttu-id="decb8-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="decb8-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="decb8-211">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-211">no</span></span>             | <span data-ttu-id="decb8-212">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-212">no</span></span>               |
| <span data-ttu-id="decb8-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="decb8-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="decb8-214">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-214">no</span></span>             | <span data-ttu-id="decb8-215">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-215">no</span></span>               |
| <span data-ttu-id="decb8-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="decb8-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="decb8-217">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-217">no</span></span>             | <span data-ttu-id="decb8-218">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-218">no</span></span>               |
| <span data-ttu-id="decb8-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="decb8-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="decb8-220">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-220">no</span></span>             | <span data-ttu-id="decb8-221">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-221">no</span></span>               |
| <span data-ttu-id="decb8-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="decb8-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="decb8-223">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-223">no</span></span>             | <span data-ttu-id="decb8-224">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-224">no</span></span>               |
| <span data-ttu-id="decb8-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="decb8-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="decb8-226">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-226">no</span></span>             | <span data-ttu-id="decb8-227">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-227">no</span></span>               |
| <span data-ttu-id="decb8-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="decb8-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="decb8-229">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-229">no</span></span>             | <span data-ttu-id="decb8-230">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-230">no</span></span>               |
| <span data-ttu-id="decb8-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="decb8-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="decb8-232">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-232">no</span></span>             | <span data-ttu-id="decb8-233">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-233">no</span></span>               |
| <span data-ttu-id="decb8-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="decb8-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="decb8-235">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-235">no</span></span>             | <span data-ttu-id="decb8-236">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-236">no</span></span>               |
| <span data-ttu-id="decb8-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="decb8-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="decb8-238">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-238">no</span></span>             | <span data-ttu-id="decb8-239">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-239">no</span></span>               |
| <span data-ttu-id="decb8-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="decb8-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="decb8-241">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-241">no</span></span>             | <span data-ttu-id="decb8-242">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-242">no</span></span>               |
| <span data-ttu-id="decb8-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="decb8-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="decb8-244">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-244">no</span></span>             | <span data-ttu-id="decb8-245">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-245">no</span></span>               |
| <span data-ttu-id="decb8-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="decb8-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="decb8-247">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-247">no</span></span>             | <span data-ttu-id="decb8-248">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-248">no</span></span>               |
| <span data-ttu-id="decb8-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="decb8-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="decb8-250">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-250">no</span></span>             | <span data-ttu-id="decb8-251">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-251">no</span></span>               |
| <span data-ttu-id="decb8-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="decb8-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="decb8-253">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-253">no</span></span>             | <span data-ttu-id="decb8-254">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-254">no</span></span>               |
| <span data-ttu-id="decb8-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="decb8-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="decb8-256">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-256">no</span></span>             | <span data-ttu-id="decb8-257">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-257">no</span></span>               |
| <span data-ttu-id="decb8-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="decb8-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="decb8-259">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-259">no</span></span>             | <span data-ttu-id="decb8-260">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-260">no</span></span>               |
| <span data-ttu-id="decb8-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="decb8-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="decb8-262">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-262">no</span></span>             | <span data-ttu-id="decb8-263">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-263">no</span></span>               |
| <span data-ttu-id="decb8-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="decb8-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="decb8-265">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-265">no</span></span>             | <span data-ttu-id="decb8-266">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-266">no</span></span>               |
| <span data-ttu-id="decb8-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="decb8-267">msdyn_progress</span></span>                         | <span data-ttu-id="decb8-268">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-268">no</span></span>             | <span data-ttu-id="decb8-269">hayır (P4W için evet)</span><span class="sxs-lookup"><span data-stu-id="decb8-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="decb8-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="decb8-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="decb8-271">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-271">no</span></span>             | <span data-ttu-id="decb8-272">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-272">no</span></span>               |
| <span data-ttu-id="decb8-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="decb8-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="decb8-274">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-274">no</span></span>             | <span data-ttu-id="decb8-275">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-275">no</span></span>               |
| <span data-ttu-id="decb8-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="decb8-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="decb8-277">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-277">no</span></span>             | <span data-ttu-id="decb8-278">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-278">no</span></span>               |
| <span data-ttu-id="decb8-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="decb8-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="decb8-280">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-280">no</span></span>             | <span data-ttu-id="decb8-281">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-281">no</span></span>               |
| <span data-ttu-id="decb8-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="decb8-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="decb8-283">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-283">no</span></span>             | <span data-ttu-id="decb8-284">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-284">no</span></span>               |
| <span data-ttu-id="decb8-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="decb8-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="decb8-286">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-286">no</span></span>             | <span data-ttu-id="decb8-287">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-287">no</span></span>               |
| <span data-ttu-id="decb8-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="decb8-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="decb8-289">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-289">no</span></span>             | <span data-ttu-id="decb8-290">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-290">no</span></span>               |
| <span data-ttu-id="decb8-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="decb8-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="decb8-292">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-292">no</span></span>             | <span data-ttu-id="decb8-293">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-293">no</span></span>               |
| <span data-ttu-id="decb8-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="decb8-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="decb8-295">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-295">no</span></span>             | <span data-ttu-id="decb8-296">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-296">no</span></span>               |
| <span data-ttu-id="decb8-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="decb8-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="decb8-298">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-298">no</span></span>             | <span data-ttu-id="decb8-299">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-299">no</span></span>               |
| <span data-ttu-id="decb8-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="decb8-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="decb8-301">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-301">no</span></span>             | <span data-ttu-id="decb8-302">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-302">no</span></span>               |
| <span data-ttu-id="decb8-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="decb8-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="decb8-304">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-304">no</span></span>             | <span data-ttu-id="decb8-305">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-305">no</span></span>               |
| <span data-ttu-id="decb8-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="decb8-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="decb8-307">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-307">no</span></span>             | <span data-ttu-id="decb8-308">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-308">no</span></span>               |
| <span data-ttu-id="decb8-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="decb8-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="decb8-310">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-310">no</span></span>             | <span data-ttu-id="decb8-311">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-311">no</span></span>               |
| <span data-ttu-id="decb8-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="decb8-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="decb8-313">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-313">no</span></span>             | <span data-ttu-id="decb8-314">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-314">no</span></span>               |
| <span data-ttu-id="decb8-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="decb8-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="decb8-316">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-316">no</span></span>             | <span data-ttu-id="decb8-317">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-317">no</span></span>               |
| <span data-ttu-id="decb8-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="decb8-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="decb8-319">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-319">no</span></span>             | <span data-ttu-id="decb8-320">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-320">no</span></span>               |
| <span data-ttu-id="decb8-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="decb8-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="decb8-322">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-322">no</span></span>             | <span data-ttu-id="decb8-323">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-323">no</span></span>               |
| <span data-ttu-id="decb8-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="decb8-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="decb8-325">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-325">no</span></span>             | <span data-ttu-id="decb8-326">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-326">no</span></span>               |
| <span data-ttu-id="decb8-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="decb8-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="decb8-328">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-328">no</span></span>             | <span data-ttu-id="decb8-329">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-329">no</span></span>               |
| <span data-ttu-id="decb8-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="decb8-330">msdyn_summary</span></span>                          | <span data-ttu-id="decb8-331">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-331">no</span></span>             | <span data-ttu-id="decb8-332">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-332">no</span></span>               |
| <span data-ttu-id="decb8-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="decb8-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="decb8-334">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-334">no</span></span>             | <span data-ttu-id="decb8-335">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-335">no</span></span>               |
| <span data-ttu-id="decb8-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="decb8-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="decb8-337">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-337">no</span></span>             | <span data-ttu-id="decb8-338">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="decb8-339">Proje görevi bağımlılığı</span><span class="sxs-lookup"><span data-stu-id="decb8-339">Project task dependency</span></span>

| <span data-ttu-id="decb8-340">**Mantıksal ad**</span><span class="sxs-lookup"><span data-stu-id="decb8-340">**Logical name**</span></span>              | <span data-ttu-id="decb8-341">**Oluşturabilir**</span><span class="sxs-lookup"><span data-stu-id="decb8-341">**Can create**</span></span> | <span data-ttu-id="decb8-342">**Düzenleyebilir**</span><span class="sxs-lookup"><span data-stu-id="decb8-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="decb8-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="decb8-343">msdyn_linktype</span></span>                | <span data-ttu-id="decb8-344">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-344">no</span></span>             | <span data-ttu-id="decb8-345">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-345">no</span></span>           |
| <span data-ttu-id="decb8-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="decb8-346">msdyn_linktypename</span></span>            | <span data-ttu-id="decb8-347">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-347">no</span></span>             | <span data-ttu-id="decb8-348">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-348">no</span></span>           |
| <span data-ttu-id="decb8-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="decb8-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="decb8-350">evet</span><span class="sxs-lookup"><span data-stu-id="decb8-350">yes</span></span>            | <span data-ttu-id="decb8-351">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-351">no</span></span>           |
| <span data-ttu-id="decb8-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="decb8-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="decb8-353">evet</span><span class="sxs-lookup"><span data-stu-id="decb8-353">yes</span></span>            | <span data-ttu-id="decb8-354">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-354">no</span></span>           |
| <span data-ttu-id="decb8-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="decb8-355">msdyn_project</span></span>                 | <span data-ttu-id="decb8-356">evet</span><span class="sxs-lookup"><span data-stu-id="decb8-356">yes</span></span>            | <span data-ttu-id="decb8-357">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-357">no</span></span>           |
| <span data-ttu-id="decb8-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="decb8-358">msdyn_projectname</span></span>             | <span data-ttu-id="decb8-359">evet</span><span class="sxs-lookup"><span data-stu-id="decb8-359">yes</span></span>            | <span data-ttu-id="decb8-360">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-360">no</span></span>           |
| <span data-ttu-id="decb8-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="decb8-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="decb8-362">evet</span><span class="sxs-lookup"><span data-stu-id="decb8-362">yes</span></span>            | <span data-ttu-id="decb8-363">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-363">no</span></span>           |
| <span data-ttu-id="decb8-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="decb8-364">msdyn_successortask</span></span>           | <span data-ttu-id="decb8-365">evet</span><span class="sxs-lookup"><span data-stu-id="decb8-365">yes</span></span>            | <span data-ttu-id="decb8-366">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-366">no</span></span>           |
| <span data-ttu-id="decb8-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="decb8-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="decb8-368">evet</span><span class="sxs-lookup"><span data-stu-id="decb8-368">yes</span></span>            | <span data-ttu-id="decb8-369">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="decb8-370">Kaynak atama</span><span class="sxs-lookup"><span data-stu-id="decb8-370">Resource assignment</span></span>

| <span data-ttu-id="decb8-371">**Mantıksal ad**</span><span class="sxs-lookup"><span data-stu-id="decb8-371">**Logical name**</span></span>             | <span data-ttu-id="decb8-372">**Oluşturabilir**</span><span class="sxs-lookup"><span data-stu-id="decb8-372">**Can create**</span></span> | <span data-ttu-id="decb8-373">**Düzenleyebilir**</span><span class="sxs-lookup"><span data-stu-id="decb8-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="decb8-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="decb8-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="decb8-375">evet</span><span class="sxs-lookup"><span data-stu-id="decb8-375">yes</span></span>            | <span data-ttu-id="decb8-376">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-376">no</span></span>           |
| <span data-ttu-id="decb8-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="decb8-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="decb8-378">evet</span><span class="sxs-lookup"><span data-stu-id="decb8-378">yes</span></span>            | <span data-ttu-id="decb8-379">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-379">no</span></span>           |
| <span data-ttu-id="decb8-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="decb8-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="decb8-381">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-381">no</span></span>             | <span data-ttu-id="decb8-382">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-382">no</span></span>           |
| <span data-ttu-id="decb8-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="decb8-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="decb8-384">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-384">no</span></span>             | <span data-ttu-id="decb8-385">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-385">no</span></span>           |
| <span data-ttu-id="decb8-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="decb8-386">msdyn_committype</span></span>             | <span data-ttu-id="decb8-387">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-387">no</span></span>             | <span data-ttu-id="decb8-388">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-388">no</span></span>           |
| <span data-ttu-id="decb8-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="decb8-389">msdyn_committypename</span></span>         | <span data-ttu-id="decb8-390">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-390">no</span></span>             | <span data-ttu-id="decb8-391">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-391">no</span></span>           |
| <span data-ttu-id="decb8-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="decb8-392">msdyn_effort</span></span>                 | <span data-ttu-id="decb8-393">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-393">no</span></span>             | <span data-ttu-id="decb8-394">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-394">no</span></span>           |
| <span data-ttu-id="decb8-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="decb8-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="decb8-396">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-396">no</span></span>             | <span data-ttu-id="decb8-397">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-397">no</span></span>           |
| <span data-ttu-id="decb8-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="decb8-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="decb8-399">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-399">no</span></span>             | <span data-ttu-id="decb8-400">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-400">no</span></span>           |
| <span data-ttu-id="decb8-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="decb8-401">msdyn_finish</span></span>                 | <span data-ttu-id="decb8-402">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-402">no</span></span>             | <span data-ttu-id="decb8-403">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-403">no</span></span>           |
| <span data-ttu-id="decb8-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="decb8-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="decb8-405">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-405">no</span></span>             | <span data-ttu-id="decb8-406">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-406">no</span></span>           |
| <span data-ttu-id="decb8-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="decb8-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="decb8-408">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-408">no</span></span>             | <span data-ttu-id="decb8-409">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-409">no</span></span>           |
| <span data-ttu-id="decb8-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="decb8-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="decb8-411">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-411">no</span></span>             | <span data-ttu-id="decb8-412">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-412">no</span></span>           |
| <span data-ttu-id="decb8-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="decb8-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="decb8-414">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-414">no</span></span>             | <span data-ttu-id="decb8-415">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-415">no</span></span>           |
| <span data-ttu-id="decb8-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="decb8-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="decb8-417">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-417">no</span></span>             | <span data-ttu-id="decb8-418">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-418">no</span></span>           |
| <span data-ttu-id="decb8-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="decb8-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="decb8-420">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-420">no</span></span>             | <span data-ttu-id="decb8-421">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-421">no</span></span>           |
| <span data-ttu-id="decb8-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="decb8-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="decb8-423">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-423">no</span></span>             | <span data-ttu-id="decb8-424">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-424">no</span></span>           |
| <span data-ttu-id="decb8-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="decb8-425">msdyn_projectid</span></span>              | <span data-ttu-id="decb8-426">evet</span><span class="sxs-lookup"><span data-stu-id="decb8-426">yes</span></span>            | <span data-ttu-id="decb8-427">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-427">no</span></span>           |
| <span data-ttu-id="decb8-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="decb8-428">msdyn_projectidname</span></span>          | <span data-ttu-id="decb8-429">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-429">no</span></span>             | <span data-ttu-id="decb8-430">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-430">no</span></span>           |
| <span data-ttu-id="decb8-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="decb8-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="decb8-432">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-432">no</span></span>             | <span data-ttu-id="decb8-433">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-433">no</span></span>           |
| <span data-ttu-id="decb8-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="decb8-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="decb8-435">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-435">no</span></span>             | <span data-ttu-id="decb8-436">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-436">no</span></span>           |
| <span data-ttu-id="decb8-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="decb8-437">msdyn_start</span></span>                  | <span data-ttu-id="decb8-438">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-438">no</span></span>             | <span data-ttu-id="decb8-439">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-439">no</span></span>           |
| <span data-ttu-id="decb8-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="decb8-440">msdyn_taskid</span></span>                 | <span data-ttu-id="decb8-441">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-441">no</span></span>             | <span data-ttu-id="decb8-442">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-442">no</span></span>           |
| <span data-ttu-id="decb8-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="decb8-443">msdyn_taskidname</span></span>             | <span data-ttu-id="decb8-444">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-444">no</span></span>             | <span data-ttu-id="decb8-445">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-445">no</span></span>           |
| <span data-ttu-id="decb8-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="decb8-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="decb8-447">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-447">no</span></span>             | <span data-ttu-id="decb8-448">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="decb8-449">Proje takımı üyesi</span><span class="sxs-lookup"><span data-stu-id="decb8-449">Project team member</span></span>

| <span data-ttu-id="decb8-450">**Mantıksal ad**</span><span class="sxs-lookup"><span data-stu-id="decb8-450">**Logical name**</span></span>                                 | <span data-ttu-id="decb8-451">**Oluşturabilir**</span><span class="sxs-lookup"><span data-stu-id="decb8-451">**Can create**</span></span> | <span data-ttu-id="decb8-452">**Düzenleyebilir**</span><span class="sxs-lookup"><span data-stu-id="decb8-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="decb8-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="decb8-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="decb8-454">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-454">no</span></span>             | <span data-ttu-id="decb8-455">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-455">no</span></span>           |
| <span data-ttu-id="decb8-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="decb8-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="decb8-457">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-457">no</span></span>             | <span data-ttu-id="decb8-458">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-458">no</span></span>           |
| <span data-ttu-id="decb8-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="decb8-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="decb8-460">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-460">no</span></span>             | <span data-ttu-id="decb8-461">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-461">no</span></span>           |
| <span data-ttu-id="decb8-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="decb8-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="decb8-463">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-463">no</span></span>             | <span data-ttu-id="decb8-464">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-464">no</span></span>           |
| <span data-ttu-id="decb8-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="decb8-465">msdyn_effort</span></span>                                     | <span data-ttu-id="decb8-466">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-466">no</span></span>             | <span data-ttu-id="decb8-467">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-467">no</span></span>           |
| <span data-ttu-id="decb8-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="decb8-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="decb8-469">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-469">no</span></span>             | <span data-ttu-id="decb8-470">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-470">no</span></span>           |
| <span data-ttu-id="decb8-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="decb8-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="decb8-472">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-472">no</span></span>             | <span data-ttu-id="decb8-473">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-473">no</span></span>           |
| <span data-ttu-id="decb8-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="decb8-474">msdyn_finish</span></span>                                     | <span data-ttu-id="decb8-475">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-475">no</span></span>             | <span data-ttu-id="decb8-476">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-476">no</span></span>           |
| <span data-ttu-id="decb8-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="decb8-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="decb8-478">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-478">no</span></span>             | <span data-ttu-id="decb8-479">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-479">no</span></span>           |
| <span data-ttu-id="decb8-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="decb8-480">msdyn_hours</span></span>                                      | <span data-ttu-id="decb8-481">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-481">no</span></span>             | <span data-ttu-id="decb8-482">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-482">no</span></span>           |
| <span data-ttu-id="decb8-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="decb8-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="decb8-484">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-484">no</span></span>             | <span data-ttu-id="decb8-485">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-485">no</span></span>           |
| <span data-ttu-id="decb8-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="decb8-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="decb8-487">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-487">no</span></span>             | <span data-ttu-id="decb8-488">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-488">no</span></span>           |
| <span data-ttu-id="decb8-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="decb8-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="decb8-490">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-490">no</span></span>             | <span data-ttu-id="decb8-491">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-491">no</span></span>           |
| <span data-ttu-id="decb8-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="decb8-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="decb8-493">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-493">no</span></span>             | <span data-ttu-id="decb8-494">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-494">no</span></span>           |
| <span data-ttu-id="decb8-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="decb8-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="decb8-496">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-496">no</span></span>             | <span data-ttu-id="decb8-497">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-497">no</span></span>           |
| <span data-ttu-id="decb8-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="decb8-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="decb8-499">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-499">no</span></span>             | <span data-ttu-id="decb8-500">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-500">no</span></span>           |
| <span data-ttu-id="decb8-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="decb8-501">msdyn_start</span></span>                                      | <span data-ttu-id="decb8-502">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-502">no</span></span>             | <span data-ttu-id="decb8-503">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="decb8-504">Project</span><span class="sxs-lookup"><span data-stu-id="decb8-504">Project</span></span>

| <span data-ttu-id="decb8-505">**Mantıksal ad**</span><span class="sxs-lookup"><span data-stu-id="decb8-505">**Logical name**</span></span>                       | <span data-ttu-id="decb8-506">**Oluşturabilir**</span><span class="sxs-lookup"><span data-stu-id="decb8-506">**Can create**</span></span> | <span data-ttu-id="decb8-507">**Düzenleyebilir**</span><span class="sxs-lookup"><span data-stu-id="decb8-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="decb8-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="decb8-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="decb8-509">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-509">no</span></span>             | <span data-ttu-id="decb8-510">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-510">no</span></span>           |
| <span data-ttu-id="decb8-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="decb8-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="decb8-512">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-512">no</span></span>             | <span data-ttu-id="decb8-513">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-513">no</span></span>           |
| <span data-ttu-id="decb8-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="decb8-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="decb8-515">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-515">no</span></span>             | <span data-ttu-id="decb8-516">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-516">no</span></span>           |
| <span data-ttu-id="decb8-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="decb8-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="decb8-518">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-518">no</span></span>             | <span data-ttu-id="decb8-519">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-519">no</span></span>           |
| <span data-ttu-id="decb8-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="decb8-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="decb8-521">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-521">no</span></span>             | <span data-ttu-id="decb8-522">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-522">no</span></span>           |
| <span data-ttu-id="decb8-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="decb8-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="decb8-524">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-524">no</span></span>             | <span data-ttu-id="decb8-525">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-525">no</span></span>           |
| <span data-ttu-id="decb8-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="decb8-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="decb8-527">evet</span><span class="sxs-lookup"><span data-stu-id="decb8-527">yes</span></span>            | <span data-ttu-id="decb8-528">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-528">no</span></span>           |
| <span data-ttu-id="decb8-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="decb8-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="decb8-530">evet</span><span class="sxs-lookup"><span data-stu-id="decb8-530">yes</span></span>            | <span data-ttu-id="decb8-531">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-531">no</span></span>           |
| <span data-ttu-id="decb8-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="decb8-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="decb8-533">evet</span><span class="sxs-lookup"><span data-stu-id="decb8-533">yes</span></span>            | <span data-ttu-id="decb8-534">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-534">no</span></span>           |
| <span data-ttu-id="decb8-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="decb8-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="decb8-536">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-536">no</span></span>             | <span data-ttu-id="decb8-537">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-537">no</span></span>           |
| <span data-ttu-id="decb8-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="decb8-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="decb8-539">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-539">no</span></span>             | <span data-ttu-id="decb8-540">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-540">no</span></span>           |
| <span data-ttu-id="decb8-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="decb8-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="decb8-542">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-542">no</span></span>             | <span data-ttu-id="decb8-543">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-543">no</span></span>           |
| <span data-ttu-id="decb8-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="decb8-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="decb8-545">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-545">no</span></span>             | <span data-ttu-id="decb8-546">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-546">no</span></span>           |
| <span data-ttu-id="decb8-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="decb8-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="decb8-548">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-548">no</span></span>             | <span data-ttu-id="decb8-549">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-549">no</span></span>           |
| <span data-ttu-id="decb8-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="decb8-550">msdyn_duration</span></span>                         | <span data-ttu-id="decb8-551">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-551">no</span></span>             | <span data-ttu-id="decb8-552">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-552">no</span></span>           |
| <span data-ttu-id="decb8-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="decb8-553">msdyn_effort</span></span>                           | <span data-ttu-id="decb8-554">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-554">no</span></span>             | <span data-ttu-id="decb8-555">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-555">no</span></span>           |
| <span data-ttu-id="decb8-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="decb8-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="decb8-557">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-557">no</span></span>             | <span data-ttu-id="decb8-558">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-558">no</span></span>           |
| <span data-ttu-id="decb8-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="decb8-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="decb8-560">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-560">no</span></span>             | <span data-ttu-id="decb8-561">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-561">no</span></span>           |
| <span data-ttu-id="decb8-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="decb8-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="decb8-563">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-563">no</span></span>             | <span data-ttu-id="decb8-564">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-564">no</span></span>           |
| <span data-ttu-id="decb8-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="decb8-565">msdyn_finish</span></span>                           | <span data-ttu-id="decb8-566">evet</span><span class="sxs-lookup"><span data-stu-id="decb8-566">yes</span></span>            | <span data-ttu-id="decb8-567">evet</span><span class="sxs-lookup"><span data-stu-id="decb8-567">yes</span></span>          |
| <span data-ttu-id="decb8-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="decb8-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="decb8-569">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-569">no</span></span>             | <span data-ttu-id="decb8-570">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-570">no</span></span>           |
| <span data-ttu-id="decb8-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="decb8-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="decb8-572">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-572">no</span></span>             | <span data-ttu-id="decb8-573">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-573">no</span></span>           |
| <span data-ttu-id="decb8-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="decb8-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="decb8-575">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-575">no</span></span>             | <span data-ttu-id="decb8-576">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-576">no</span></span>           |
| <span data-ttu-id="decb8-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="decb8-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="decb8-578">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-578">no</span></span>             | <span data-ttu-id="decb8-579">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-579">no</span></span>           |
| <span data-ttu-id="decb8-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="decb8-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="decb8-581">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-581">no</span></span>             | <span data-ttu-id="decb8-582">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-582">no</span></span>           |
| <span data-ttu-id="decb8-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="decb8-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="decb8-584">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-584">no</span></span>             | <span data-ttu-id="decb8-585">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-585">no</span></span>           |
| <span data-ttu-id="decb8-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="decb8-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="decb8-587">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-587">no</span></span>             | <span data-ttu-id="decb8-588">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-588">no</span></span>           |
| <span data-ttu-id="decb8-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="decb8-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="decb8-590">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-590">no</span></span>             | <span data-ttu-id="decb8-591">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-591">no</span></span>           |
| <span data-ttu-id="decb8-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="decb8-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="decb8-593">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-593">no</span></span>             | <span data-ttu-id="decb8-594">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-594">no</span></span>           |
| <span data-ttu-id="decb8-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="decb8-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="decb8-596">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-596">no</span></span>             | <span data-ttu-id="decb8-597">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-597">no</span></span>           |
| <span data-ttu-id="decb8-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="decb8-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="decb8-599">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-599">no</span></span>             | <span data-ttu-id="decb8-600">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-600">no</span></span>           |
| <span data-ttu-id="decb8-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="decb8-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="decb8-602">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-602">no</span></span>             | <span data-ttu-id="decb8-603">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-603">no</span></span>           |
| <span data-ttu-id="decb8-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="decb8-604">msdyn_progress</span></span>                         | <span data-ttu-id="decb8-605">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-605">no</span></span>             | <span data-ttu-id="decb8-606">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-606">no</span></span>           |
| <span data-ttu-id="decb8-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="decb8-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="decb8-608">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-608">no</span></span>             | <span data-ttu-id="decb8-609">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-609">no</span></span>           |
| <span data-ttu-id="decb8-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="decb8-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="decb8-611">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-611">no</span></span>             | <span data-ttu-id="decb8-612">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-612">no</span></span>           |
| <span data-ttu-id="decb8-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="decb8-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="decb8-614">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-614">no</span></span>             | <span data-ttu-id="decb8-615">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-615">no</span></span>           |
| <span data-ttu-id="decb8-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="decb8-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="decb8-617">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-617">no</span></span>             | <span data-ttu-id="decb8-618">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-618">no</span></span>           |
| <span data-ttu-id="decb8-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="decb8-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="decb8-620">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-620">no</span></span>             | <span data-ttu-id="decb8-621">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-621">no</span></span>           |
| <span data-ttu-id="decb8-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="decb8-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="decb8-623">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-623">no</span></span>             | <span data-ttu-id="decb8-624">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-624">no</span></span>           |
| <span data-ttu-id="decb8-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="decb8-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="decb8-626">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-626">no</span></span>             | <span data-ttu-id="decb8-627">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-627">no</span></span>           |
| <span data-ttu-id="decb8-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="decb8-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="decb8-629">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-629">no</span></span>             | <span data-ttu-id="decb8-630">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-630">no</span></span>           |
| <span data-ttu-id="decb8-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="decb8-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="decb8-632">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-632">no</span></span>             | <span data-ttu-id="decb8-633">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-633">no</span></span>           |
| <span data-ttu-id="decb8-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="decb8-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="decb8-635">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-635">no</span></span>             | <span data-ttu-id="decb8-636">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-636">no</span></span>           |
| <span data-ttu-id="decb8-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="decb8-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="decb8-638">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-638">no</span></span>             | <span data-ttu-id="decb8-639">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-639">no</span></span>           |
| <span data-ttu-id="decb8-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="decb8-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="decb8-641">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-641">no</span></span>             | <span data-ttu-id="decb8-642">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-642">no</span></span>           |
| <span data-ttu-id="decb8-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="decb8-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="decb8-644">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-644">no</span></span>             | <span data-ttu-id="decb8-645">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-645">no</span></span>           |
| <span data-ttu-id="decb8-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="decb8-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="decb8-647">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-647">no</span></span>             | <span data-ttu-id="decb8-648">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-648">no</span></span>           |
| <span data-ttu-id="decb8-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="decb8-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="decb8-650">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-650">no</span></span>             | <span data-ttu-id="decb8-651">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-651">no</span></span>           |
| <span data-ttu-id="decb8-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="decb8-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="decb8-653">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-653">no</span></span>             | <span data-ttu-id="decb8-654">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-654">no</span></span>           |
| <span data-ttu-id="decb8-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="decb8-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="decb8-656">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-656">no</span></span>             | <span data-ttu-id="decb8-657">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-657">no</span></span>           |
| <span data-ttu-id="decb8-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="decb8-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="decb8-659">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-659">no</span></span>             | <span data-ttu-id="decb8-660">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-660">no</span></span>           |
| <span data-ttu-id="decb8-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="decb8-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="decb8-662">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-662">no</span></span>             | <span data-ttu-id="decb8-663">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-663">no</span></span>           |
| <span data-ttu-id="decb8-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="decb8-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="decb8-665">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-665">no</span></span>             | <span data-ttu-id="decb8-666">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-666">no</span></span>           |
| <span data-ttu-id="decb8-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="decb8-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="decb8-668">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-668">no</span></span>             | <span data-ttu-id="decb8-669">hayır</span><span class="sxs-lookup"><span data-stu-id="decb8-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="decb8-670">Sınırlamalar ve bilinen sorunlar</span><span class="sxs-lookup"><span data-stu-id="decb8-670">Limitations and known issues</span></span>
<span data-ttu-id="decb8-671">Aşağıda, sınırlamalar ve bilinen sorunların bir listesi yer almaktadır:</span><span class="sxs-lookup"><span data-stu-id="decb8-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="decb8-672">Zamanlama API'leri yalnızca **Microsoft Proje Lisansı olan kullanıcılar** tarafından kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="decb8-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="decb8-673">Şu kullanıcılar tarafından kullanılamaz:</span><span class="sxs-lookup"><span data-stu-id="decb8-673">They can't be used by:</span></span>
    - <span data-ttu-id="decb8-674">Uygulama kullanıcıları</span><span class="sxs-lookup"><span data-stu-id="decb8-674">Application users</span></span>
    - <span data-ttu-id="decb8-675">Sistem kullanıcıları</span><span class="sxs-lookup"><span data-stu-id="decb8-675">System users</span></span>
    - <span data-ttu-id="decb8-676">Tümleştirme kullanıcıları</span><span class="sxs-lookup"><span data-stu-id="decb8-676">Integration users</span></span>
    - <span data-ttu-id="decb8-677">Gerekli lisansa sahip olmayan diğer kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="decb8-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="decb8-678">Her bir **OperationSet** yalnızca en fazla 100 işlem içerebilir.</span><span class="sxs-lookup"><span data-stu-id="decb8-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="decb8-679">Her bir kullanıcının açık en fazla 10 **OperationSet**'i olabilir.</span><span class="sxs-lookup"><span data-stu-id="decb8-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="decb8-680">Project Operations şu anda bir proje üzerinde en fazla 500 toplam görevi desteklemektedir.</span><span class="sxs-lookup"><span data-stu-id="decb8-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="decb8-681">**OperationSet** hata durumu ve hata günlükleri şu anda kullanılamıyor.</span><span class="sxs-lookup"><span data-stu-id="decb8-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="decb8-682">Zamanlama API'leri Genel önizlemededir.</span><span class="sxs-lookup"><span data-stu-id="decb8-682">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="decb8-683">Bu API'lerin Üretim ortamlarında kullanımı Microsoft tarafından desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="decb8-683">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>
- [<span data-ttu-id="decb8-684">Projelerde ve görevlerde sınırları ve sınırları</span><span class="sxs-lookup"><span data-stu-id="decb8-684">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="decb8-685">Hata işleme</span><span class="sxs-lookup"><span data-stu-id="decb8-685">Error handling</span></span>

   - <span data-ttu-id="decb8-686">İşlem kümelerinden oluşturulan hataları gözden geçirmek için **ayarlar** \> **Zamanlama tümleştirme** \> **işlemleri kümeleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="decb8-686">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="decb8-687">Proje zamanlama hizmetinden oluşturulan hataları gözden geçirmek için **Ayarlar** \> **zamanlama tümleştirme** \> **PSS hata günlükleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="decb8-687">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="decb8-688">Örnek senaryo</span><span class="sxs-lookup"><span data-stu-id="decb8-688">Sample scenario</span></span>

<span data-ttu-id="decb8-689">Bu senaryoda; bir proje, bir takım üyesi, dört görev ve iki kaynak ataması oluşturacaksınız.</span><span class="sxs-lookup"><span data-stu-id="decb8-689">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="decb8-690">Sonra da tek bir görevi güncelleştirecek, projeyi güncelleştirecek, tek bir görevi silecek, bir kaynak atamasını silecek ve bir görev bağımlılığı oluşturacaksınız.</span><span class="sxs-lookup"><span data-stu-id="decb8-690">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```csharp
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
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="decb8-691">Ek örnekler</span><span class="sxs-lookup"><span data-stu-id="decb8-691">Additional samples</span></span>

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
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
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
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
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
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
/// </summary>
/// <param name="operationSetId">operationSet id</param>
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
/// <param name="operationSetId">operationSet id</param>
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
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
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
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
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
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
