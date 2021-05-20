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
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Zamanlama varlıklarıyla işlemler gerçekleştirmek için Zamanlama API'lerini kullanma

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

> [!IMPORTANT] 
> Bu konuda açıklanan bazı veya tüm işlevler, bir önizleme sürümü kapsamındadır. İçerik ve işlevsellik değiştirilebilir. 

## <a name="scheduling-entities"></a>Zamanlama varlıkları

Zamanlama API'leri, **Zamanlama Varlıkları**'yla oluşturma, güncelleştirme ve silme işlemlerini gerçekleştirmeye olanak tanır. Bu varlıklar, webe yönelik projelerde Zamanlama altyapısı üzerinden yönetilir. Önceki Dynamics 365 Project Operations sürümlerinde **Zamanlama varlıklarıyla** oluşturma, güncelleştirme ve silme işlemleri kısıtlanmıştı.

Aşağıdaki tabloda, **Zamanlama varlıkları**'nın tam bir listesi verilmiştir.

| Varlık adı  | Varlık mantıksal adı |
| --- | --- |
| Project | msdyn_project |
| Proje Görevi  | msdyn_projecttask  |
| Proje Görevi Bağımlılığı  | msdyn_projecttaskdependency  |
| Kaynak Atama | msdyn_resourceassignment |
| Proje Demeti  | msdyn_projectbucket |
| Proje Takımı Üyesi | msdyn_projectteam |

## <a name="operationset"></a>OperationSet

OperationSet, bir hareket içinde işlenmesi gereken, zamanlamayı etkileyen birkaç isteğin işlenmesi gerektiğinde kullanılabilen bir çalışma birimi düzenidir.

## <a name="schedule-apis"></a>Zamanlama API'leri

Aşağıda, mevcut Zamanlama API'lerinin bir listesi verilmiştir.

- **msdyn_CreateProjectV1**: Bu API, proje oluşturmak için kullanılabilir. Proje ve varsayılan proje demeti hemen oluşturulur.
- **msdyn_CreateTeamMemberV1**: Bu API, proje takımı üyesi oluşturmak için kullanılabilir. Takım üyesi kaydı hemen oluşturulur.
- **msdyn_CreateOperationSetV1**: Bu API, bir hareket içinde gerçekleştirilmesi gereken çok sayıda isteği zamanlamak için kullanılabilir.
- **msdyn_PSSCreateV1**: Bu API, bir varlık oluşturmak için kullanılabilir. Varlık, oluşturma işlemini destekleyen Zamanlama varlıklarından herhangi biri olabilir.
- **msdyn_PSSUpdateV1**: Bu API, bir varlık güncelleştirmek için kullanılabilir. Varlık, güncelleştirme işlemini destekleyen Zamanlama varlıklarından herhangi biri olabilir.
- **msdyn_PSSDeleteV1**: Bu API, bir varlığı silmek için kullanılabilir. Varlık, silme işlemini destekleyen Zamanlama varlıklarından herhangi biri olabilir.
- **msdyn_ExecuteOperationSetV1**: Bu API, bir işlem kümesindeki tüm işlemleri yürütmek için kullanılır.

## <a name="using-schedule-apis-with-operationset"></a>Zamanlama API'lerini OperationSet ile kullanma

Hem **CreateProjectV1** hem de **CreateTeamMemberV1** içeren kayıtlar hemen oluşturulduğundan, bu API'ler doğrudan **OperationSet** içinde kullanılamaz. Ancak API'yi kullanarak gerekli kayıtları oluşturup bir **OperationSet** oluşturabilir ve ardından **OperationSet** içinde bu önceden oluşturulmuş kayıtları kullanabilirsiniz.

## <a name="supported-operations"></a>Desteklenen işlemler

| Zamanlama varlığı | Oluştur | Güncelleştirme | Delete | Dikkat edilmesi gereken önemli hususlar |
| --- | --- | --- | --- | --- |
Proje görevi | Evet | Evet | Evet | Hiçbiri |
| Proje görevi bağımlılığı | Evet | Evet | | Proje görev bağımlılığı kayıtları güncelleştirilmemiş. Bunun yerine, eski bir kayıt silinebilir ve yeni bir kayıt oluşturulabilir. |
| Kaynak atama | Evet | Evet | | Şu alanlara sahip işlemler desteklenmez: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** ve **PlannedWork**. Kaynak atama kayıtları güncelleştirilmemiş. Bunun yerine, eski kayıt silinebilir ve yeni bir kayıt oluşturulabilir. |
| Proje demeti | Yok | Yok | Yok | Varsayılan demet, **CreateProjectV1** API kullanılarak oluşturulmuş. |
| Proje takımı üyesi | Evet | Evet | Evet | Oluşturma işlemi için **CreateTeamMemberV1** API'sini kullanın. |
| Project | Evet | Evet | Yok | Şu alanlara sahip işlemler desteklenmez: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** ve **Duration**. |

Bu API'ler özel alanlar içeren varlık nesneleriyle çağrılabilir.

Kimlik özelliği isteğe bağlıdır. Sağlanmışsa, sistem bunu kullanmayı dener ve kullanılamaz ise bir özel durum oluşturur. Sağlanmazsa, sistem bunu oluşturacaktır.

## <a name="restricted-fields"></a>Sınırlandırılmış alanlar

Aşağıdaki tablolarda, **oluşturma** ve **düzenleme** için kısıtlanan alanlar tanımlanır.

### <a name="project-task"></a>Proje görevi

| **Mantıksal ad**                       | **Oluşturabilir** | **Düzenleyebilir**     |
|----------------------------------------|----------------|------------------|
| msdyn_actualcost                       | hayır             | hayır               |
| msdyn_actualcost_base                  | hayır             | hayır               |
| msdyn_actualend                        | hayır             | hayır               |
| msdyn_actualsales                      | hayır             | hayır               |
| msdyn_actualsales_base                 | hayır             | hayır               |
| msdyn_actualstart                      | hayır             | hayır               |
| msdyn_costatcompleteestimate           | hayır             | hayır               |
| msdyn_costatcompleteestimate_base      | hayır             | hayır               |
| msdyn_costconsumptionpercentage        | hayır             | hayır               |
| msdyn_effortcompleted                  | hayır             | hayır               |
| msdyn_effortestimateatcomplete         | hayır             | hayır               |
| msdyn_iscritical                       | hayır             | hayır               |
| msdyn_iscriticalname                   | hayır             | hayır               |
| msdyn_ismanual                         | hayır             | hayır               |
| msdyn_ismanualname                     | hayır             | hayır               |
| msdyn_ismilestone                      | hayır             | hayır               |
| msdyn_ismilestonename                  | hayır             | hayır               |
| msdyn_LinkStatus                       | hayır             | hayır               |
| msdyn_linkstatusname                   | hayır             | hayır               |
| msdyn_msprojectclientid                | hayır             | hayır               |
| msdyn_plannedcost                      | hayır             | hayır               |
| msdyn_plannedcost_base                 | hayır             | hayır               |
| msdyn_plannedsales                     | hayır             | hayır               |
| msdyn_plannedsales_base                | hayır             | hayır               |
| msdyn_pluginprocessingdata             | hayır             | hayır               |
| msdyn_progress                         | hayır             | hayır (P4W için evet) |
| msdyn_remainingcost                    | hayır             | hayır               |
| msdyn_remainingcost_base               | hayır             | hayır               |
| msdyn_remainingsales                   | hayır             | hayır               |
| msdyn_remainingsales_base              | hayır             | hayır               |
| msdyn_requestedhours                   | hayır             | hayır               |
| msdyn_resourcecategory                 | hayır             | hayır               |
| msdyn_resourcecategoryname             | hayır             | hayır               |
| msdyn_resourceorganizationalunitid     | hayır             | hayır               |
| msdyn_resourceorganizationalunitidname | hayır             | hayır               |
| msdyn_salesconsumptionpercentage       | hayır             | hayır               |
| msdyn_salesestimateatcomplete          | hayır             | hayır               |
| msdyn_salesestimateatcomplete_base     | hayır             | hayır               |
| msdyn_salesvariance                    | hayır             | hayır               |
| msdyn_salesvariance_base               | hayır             | hayır               |
| msdyn_scheduleddurationminutes         | hayır             | hayır               |
| msdyn_scheduledend                     | hayır             | hayır               |
| msdyn_scheduledstart                   | hayır             | hayır               |
| msdyn_schedulevariance                 | hayır             | hayır               |
| msdyn_skipupdateestimateline           | hayır             | hayır               |
| msdyn_skipupdateestimatelinename       | hayır             | hayır               |
| msdyn_summary                          | hayır             | hayır               |
| msdyn_varianceofcost                   | hayır             | hayır               |
| msdyn_varianceofcost_base              | hayır             | hayır               |

### <a name="project-task-dependency"></a>Proje görevi bağımlılığı

| **Mantıksal ad**              | **Oluşturabilir** | **Düzenleyebilir** |
|-------------------------------|----------------|--------------|
| msdyn_linktype                | hayır             | hayır           |
| msdyn_linktypename            | hayır             | hayır           |
| msdyn_predecessortask         | evet            | hayır           |
| msdyn_predecessortaskname     | evet            | hayır           |
| msdyn_project                 | evet            | hayır           |
| msdyn_projectname             | evet            | hayır           |
| msdyn_projecttaskdependencyid | evet            | hayır           |
| msdyn_successortask           | evet            | hayır           |
| msdyn_successortaskname       | evet            | hayır           |

### <a name="resource-assignment"></a>Kaynak atama

| **Mantıksal ad**             | **Oluşturabilir** | **Düzenleyebilir** |
|------------------------------|----------------|--------------|
| msdyn_bookableresourceid     | evet            | hayır           |
| msdyn_bookableresourceidname | evet            | hayır           |
| msdyn_bookingstatusid        | hayır             | hayır           |
| msdyn_bookingstatusidname    | hayır             | hayır           |
| msdyn_committype             | hayır             | hayır           |
| msdyn_committypename         | hayır             | hayır           |
| msdyn_effort                 | hayır             | hayır           |
| msdyn_effortcompleted        | hayır             | hayır           |
| msdyn_effortremaining        | hayır             | hayır           |
| msdyn_finish                 | hayır             | hayır           |
| msdyn_plannedcost            | hayır             | hayır           |
| msdyn_plannedcost_base       | hayır             | hayır           |
| msdyn_plannedcostcontour     | hayır             | hayır           |
| msdyn_plannedsales           | hayır             | hayır           |
| msdyn_plannedsales_base      | hayır             | hayır           |
| msdyn_plannedsalescontour    | hayır             | hayır           |
| msdyn_plannedwork            | hayır             | hayır           |
| msdyn_projectid              | evet            | hayır           |
| msdyn_projectidname          | hayır             | hayır           |
| msdyn_projectteamid          | hayır             | hayır           |
| msdyn_projectteamidname      | hayır             | hayır           |
| msdyn_start                  | hayır             | hayır           |
| msdyn_taskid                 | hayır             | hayır           |
| msdyn_taskidname             | hayır             | hayır           |
| msdyn_userresourceid         | hayır             | hayır           |

### <a name="project-team-member"></a>Proje takımı üyesi

| **Mantıksal ad**                                 | **Oluşturabilir** | **Düzenleyebilir** |
|--------------------------------------------------|----------------|--------------|
| msdyn_calendarid                                 | hayır             | hayır           |
| msdyn_creategenericteammemberwithrequirementname | hayır             | hayır           |
| msdyn_deletestatus                               | hayır             | hayır           |
| msdyn_deletestatusname                           | hayır             | hayır           |
| msdyn_effort                                     | hayır             | hayır           |
| msdyn_effortcompleted                            | hayır             | hayır           |
| msdyn_effortremaining                            | hayır             | hayır           |
| msdyn_finish                                     | hayır             | hayır           |
| msdyn_hardbookedhours                            | hayır             | hayır           |
| msdyn_hours                                      | hayır             | hayır           |
| msdyn_markedfordeletiontimer                     | hayır             | hayır           |
| msdyn_markedfordeletiontimestamp                 | hayır             | hayır           |
| msdyn_msprojectclientid                          | hayır             | hayır           |
| msdyn_percentage                                 | hayır             | hayır           |
| msdyn_requiredhours                              | hayır             | hayır           |
| msdyn_softbookedhours                            | hayır             | hayır           |
| msdyn_start                                      | hayır             | hayır           |

### <a name="project"></a>Project

| **Mantıksal ad**                       | **Oluşturabilir** | **Düzenleyebilir** |
|----------------------------------------|----------------|--------------|
| msdyn_actualexpensecost                | hayır             | hayır           |
| msdyn_actualexpensecost_base           | hayır             | hayır           |
| msdyn_actuallaborcost                  | hayır             | hayır           |
| msdyn_actuallaborcost_base             | hayır             | hayır           |
| msdyn_actualsales                      | hayır             | hayır           |
| msdyn_actualsales_base                 | hayır             | hayır           |
| msdyn_contractlineproject              | evet            | hayır           |
| msdyn_contractorganizationalunitid     | evet            | hayır           |
| msdyn_contractorganizationalunitidname | evet            | hayır           |
| msdyn_costconsumption                  | hayır             | hayır           |
| msdyn_costestimateatcomplete           | hayır             | hayır           |
| msdyn_costestimateatcomplete_base      | hayır             | hayır           |
| msdyn_costvariance                     | hayır             | hayır           |
| msdyn_costvariance_base                | hayır             | hayır           |
| msdyn_duration                         | hayır             | hayır           |
| msdyn_effort                           | hayır             | hayır           |
| msdyn_effortcompleted                  | hayır             | hayır           |
| msdyn_effortestimateatcompleteeac      | hayır             | hayır           |
| msdyn_effortremaining                  | hayır             | hayır           |
| msdyn_finish                           | evet            | evet          |
| msdyn_globalrevisiontoken              | hayır             | hayır           |
| msdyn_islinkedtomsprojectclient        | hayır             | hayır           |
| msdyn_islinkedtomsprojectclientname    | hayır             | hayır           |
| msdyn_linkeddocumenturl                | hayır             | hayır           |
| msdyn_msprojectdocument                | hayır             | hayır           |
| msdyn_msprojectdocumentname            | hayır             | hayır           |
| msdyn_plannedexpensecost               | hayır             | hayır           |
| msdyn_plannedexpensecost_base          | hayır             | hayır           |
| msdyn_plannedlaborcost                 | hayır             | hayır           |
| msdyn_plannedlaborcost_base            | hayır             | hayır           |
| msdyn_plannedsales                     | hayır             | hayır           |
| msdyn_plannedsales_base                | hayır             | hayır           |
| msdyn_progress                         | hayır             | hayır           |
| msdyn_remainingcost                    | hayır             | hayır           |
| msdyn_remainingcost_base               | hayır             | hayır           |
| msdyn_remainingsales                   | hayır             | hayır           |
| msdyn_remainingsales_base              | hayır             | hayır           |
| msdyn_replaylogheader                  | hayır             | hayır           |
| msdyn_salesconsumption                 | hayır             | hayır           |
| msdyn_salesestimateatcompleteeac       | hayır             | hayır           |
| msdyn_salesestimateatcompleteeac_base  | hayır             | hayır           |
| msdyn_salesvariance                    | hayır             | hayır           |
| msdyn_salesvariance_base               | hayır             | hayır           |
| msdyn_scheduleperformance              | hayır             | hayır           |
| msdyn_scheduleperformancename          | hayır             | hayır           |
| msdyn_schedulevariance                 | hayır             | hayır           |
| msdyn_taskearlieststart                | hayır             | hayır           |
| msdyn_teamsize                         | hayır             | hayır           |
| msdyn_teamsize_date                    | hayır             | hayır           |
| msdyn_teamsize_state                   | hayır             | hayır           |
| msdyn_totalactualcost                  | hayır             | hayır           |
| msdyn_totalactualcost_base             | hayır             | hayır           |
| msdyn_totalplannedcost                 | hayır             | hayır           |
| msdyn_totalplannedcost_base            | hayır             | hayır           |


## <a name="limitations-and-known-issues"></a>Sınırlamalar ve bilinen sorunlar
Aşağıda, sınırlamalar ve bilinen sorunların bir listesi yer almaktadır:

- Zamanlama API'leri yalnızca **Microsoft Proje Lisansı olan kullanıcılar** tarafından kullanılabilir. Şu kullanıcılar tarafından kullanılamaz:
    - Uygulama kullanıcıları
    - Sistem kullanıcıları
    - Tümleştirme kullanıcıları
    - Gerekli lisansa sahip olmayan diğer kullanıcılar
- Her bir **OperationSet** yalnızca en fazla 100 işlem içerebilir.
- Her bir kullanıcının açık en fazla 10 **OperationSet**'i olabilir.
- Project Operations şu anda bir proje üzerinde en fazla 500 toplam görevi desteklemektedir.
- **OperationSet** hata durumu ve hata günlükleri şu anda kullanılamıyor.
- Zamanlama API'leri Genel önizlemededir. Bu API'lerin Üretim ortamlarında kullanımı Microsoft tarafından desteklenmez.
- [Projelerde ve görevlerde sınırları ve sınırları](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a>Hata işleme

   - İşlem kümelerinden oluşturulan hataları gözden geçirmek için **ayarlar** \> **Zamanlama tümleştirme** \> **işlemleri kümeleri**'ne gidin.
   - Proje zamanlama hizmetinden oluşturulan hataları gözden geçirmek için **Ayarlar** \> **zamanlama tümleştirme** \> **PSS hata günlükleri**'ne gidin.

## <a name="sample-scenario"></a>Örnek senaryo

Bu senaryoda; bir proje, bir takım üyesi, dört görev ve iki kaynak ataması oluşturacaksınız. Sonra da tek bir görevi güncelleştirecek, projeyi güncelleştirecek, tek bir görevi silecek, bir kaynak atamasını silecek ve bir görev bağımlılığı oluşturacaksınız.

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

## <a name="additional-samples"></a>Ek örnekler

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
