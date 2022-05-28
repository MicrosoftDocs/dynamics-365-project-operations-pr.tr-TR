---
title: Zamanlama varlıkları ile işlemler gerçekleştirmek için Proje zamanlama API'larını kullanma
description: Bu konu Proje zamanlama API'larının kullanımına yönelik bilgiler ve örnekler sağlar.
author: sigitac
ms.date: 01/13/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: cabdf9716e4e25ed682368b99a87b3a3bf483cca
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8592072"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Zamanlama varlıkları ile işlemler gerçekleştirmek için Proje zamanlama API'larını kullanma

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_



## <a name="scheduling-entities"></a>Zamanlama varlıkları

Proje zamanlaması API'ları **Zamanlama varlıklarıyla** oluşturma, güncelleştirme ve silme işlemleri gerçekleştirme olanağı sunar. Bu varlıklar, webe yönelik projelerde Zamanlama altyapısı üzerinden yönetilir. Önceki Dynamics 365 Project Operations sürümlerinde **Zamanlama varlıklarıyla** oluşturma, güncelleştirme ve silme işlemleri kısıtlanmıştı.

Aşağıdaki tabloda Proje zamanlama varlıklarının tam listesi verilmiştir.

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

## <a name="project-schedule-apis"></a>Proje zamanlama API'ları

Aşağıda geçerli Proje zamanlama API'larının listesi yer almaktadır.

- **msdyn_CreateProjectV1**: Bu API, proje oluşturmak için kullanılabilir. Proje ve varsayılan proje paketi hemen oluşturulur.
- **msdyn_CreateTeamMemberV1**: Bu API, proje takımı üyesi oluşturmak için kullanılabilir. Takım üyesi kaydı hemen oluşturulur.
- **msdyn_CreateOperationSetV1**: Bu API, bir hareket içinde gerçekleştirilmesi gereken çok sayıda isteği zamanlamak için kullanılabilir.
- **msdyn_PSSCreateV1**: Bu API, bir varlık oluşturmak için kullanılabilir. Varlık, oluşturma işlemini destekleyen Proje zamanlama varlıklarından herhangi biri olabilir.
- **msdyn_PSSUpdateV1**: Bu API, bir varlık güncelleştirmek için kullanılabilir. Varlık, güncelleştirme işlemini destekleyen Proje zamanlama varlıklarından herhangi biri olabilir.
- **msdyn_PSSDeleteV1**: Bu API, bir varlığı silmek için kullanılabilir. Varlık, silme işlemini destekleyen Proje zamanlama varlıklarından herhangi biri olabilir.
- **msdyn_ExecuteOperationSetV1**: Bu API, bir işlem kümesindeki tüm işlemleri yürütmek için kullanılır.

## <a name="using-project-schedule-apis-with-operationset"></a>OperationSet ile Proje zamanlama API'larını kullanma

Hem **CreateProjectV1** hem de **CreateTeamMemberV1** içeren kayıtlar hemen oluşturulduğundan, bu API'ler doğrudan **OperationSet** içinde kullanılamaz. Ancak API'yi kullanarak gerekli kayıtları oluşturup bir **OperationSet** oluşturabilir ve ardından **OperationSet** içinde bu önceden oluşturulmuş kayıtları kullanabilirsiniz.

## <a name="supported-operations"></a>Desteklenen işlemler

| Zamanlama varlığı | Oluştur | Güncelleş | Silme | Dikkat edilmesi gereken önemli hususlar |
| --- | --- | --- | --- | --- |
Proje görevi | Evet | Evet | Evet | **Progress**, **EffortCompleted** ve **EffortRemaining** alanları, Project for the Web'de düzenlenebilir ancak Project Operations'ta düzenlenemez.  |
| Proje görevi bağımlılığı | Evet |  | Evet | Proje görev bağımlılığı kayıtları güncelleştirilmemiş. Bunun yerine, eski bir kayıt silinebilir ve yeni bir kayıt oluşturulabilir. |
| Kaynak atama | Evet | Evet | | Şu alanlara sahip işlemler desteklenmez: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** ve **PlannedWork**. Kaynak atama kayıtları güncelleştirilmemiş. Bunun yerine, eski kayıt silinebilir ve yeni bir kayıt oluşturulabilir. |
| Proje demeti | Evet | Evet | Evet | Varsayılan paket, **CreateProjectV1** API'sini kullanarak oluşturulur. Proje paketleri oluşturma ve silme desteği, Güncelleştirme Sürümü 16'da eklenmiştir. |
| Proje takımı üyesi | Evet | Evet | Evet | Oluşturma işlemi için **CreateTeamMemberV1** API'sini kullanın. |
| Project | Evet | Evet |  | Şu alanlara sahip işlemler desteklenmez: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** ve **Duration**. |

Bu API'ler özel alanlar içeren varlık nesneleriyle çağrılabilir.

Kimlik özelliği isteğe bağlıdır. Sağlanmışsa, sistem bunu kullanmayı dener ve kullanılamaz ise bir özel durum oluşturur. Sağlanmazsa, sistem bunu oluşturacaktır.

## <a name="restricted-fields"></a>Sınırlandırılmış alanlar

Aşağıdaki tablolarda, **Oluşturma** ve **Düzenleme** için kısıtlanan alanlar tanımlanır.

### <a name="project-task"></a>Proje görevi

| Mantıksal ad                           | Oluşturabilir     | Düzenleyebilir         |
|----------------------------------------|----------------|------------------|
| msdyn_actualcost                       | No             | No               |
| msdyn_actualcost_base                  | No             | No               |
| msdyn_actualend                        | No             | No               |
| msdyn_actualsales                      | No             | No               |
| msdyn_actualsales_base                 | No             | No               |
| msdyn_actualstart                      | No             | No               |
| msdyn_costatcompleteestimate           | No             | No               |
| msdyn_costatcompleteestimate_base      | No             | No               |
| msdyn_costconsumptionpercentage        | No             | No               |
| msdyn_effortcompleted                  | Hayır (Proje için evet)             | Hayır (Proje için evet)               |
| msdyn_effortremaining                  | Hayır (Proje için evet)              | Hayır (Proje için evet)                |
| msdyn_effortestimateatcomplete         | No             | No               |
| msdyn_iscritical                       | No             | No               |
| msdyn_iscriticalname                   | No             | No               |
| msdyn_ismanual                         | No             | No               |
| msdyn_ismanualname                     | No             | No               |
| msdyn_ismilestone                      | No             | No               |
| msdyn_ismilestonename                  | No             | No               |
| msdyn_LinkStatus                       | No             | No               |
| msdyn_linkstatusname                   | No             | No               |
| msdyn_msprojectclientid                | No             | No               |
| msdyn_plannedcost                      | No             | No               |
| msdyn_plannedcost_base                 | No             | No               |
| msdyn_plannedsales                     | No             | No               |
| msdyn_plannedsales_base                | No             | No               |
| msdyn_pluginprocessingdata             | No             | No               |
| msdyn_progress                         | Hayır (Proje için evet)             | Hayır (Proje için evet) |
| msdyn_remainingcost                    | No             | No               |
| msdyn_remainingcost_base               | No             | No               |
| msdyn_remainingsales                   | No             | No               |
| msdyn_remainingsales_base              | No             | No               |
| msdyn_requestedhours                   | No             | No               |
| msdyn_resourcecategory                 | No             | No               |
| msdyn_resourcecategoryname             | No             | No               |
| msdyn_resourceorganizationalunitid     | No             | No               |
| msdyn_resourceorganizationalunitidname | No             | No               |
| msdyn_salesconsumptionpercentage       | No             | No               |
| msdyn_salesestimateatcomplete          | No             | No               |
| msdyn_salesestimateatcomplete_base     | No             | No               |
| msdyn_salesvariance                    | No             | No               |
| msdyn_salesvariance_base               | No             | No               |
| msdyn_scheduleddurationminutes         | No             | No               |
| msdyn_scheduledend                     | No             | No               |
| msdyn_scheduledstart                   | No             | No               |
| msdyn_schedulevariance                 | No             | No               |
| msdyn_skipupdateestimateline           | No             | No               |
| msdyn_skipupdateestimatelinename       | No             | No               |
| msdyn_summary                          | No             | No               |
| msdyn_varianceofcost                   | No             | No               |
| msdyn_varianceofcost_base              | No             | No               |

### <a name="project-task-dependency"></a>Proje görevi bağımlılığı

| Mantıksal ad                  | Oluşturabilir     | Düzenleyebilir     |
|-------------------------------|----------------|--------------|
| msdyn_linktype                | No             | No           |
| msdyn_linktypename            | No             | No           |
| msdyn_predecessortask         | Evet            | No           |
| msdyn_predecessortaskname     | Evet            | No           |
| msdyn_project                 | Evet            | No           |
| msdyn_projectname             | Evet            | No           |
| msdyn_projecttaskdependencyid | Evet            | No           |
| msdyn_successortask           | Evet            | No           |
| msdyn_successortaskname       | Evet            | No           |

### <a name="resource-assignment"></a>Kaynak atama

| Mantıksal ad                 | Oluşturabilir     | Düzenleyebilir     |
|------------------------------|----------------|--------------|
| msdyn_bookableresourceid     | Evet            | No           |
| msdyn_bookableresourceidname | Evet            | No           |
| msdyn_bookingstatusid        | No             | No           |
| msdyn_bookingstatusidname    | No             | No           |
| msdyn_committype             | No             | No           |
| msdyn_committypename         | No             | No           |
| msdyn_effort                 | No             | No           |
| msdyn_effortcompleted        | No             | No           |
| msdyn_effortremaining        | No             | No           |
| msdyn_finish                 | No             | No           |
| msdyn_plannedcost            | No             | No           |
| msdyn_plannedcost_base       | No             | No           |
| msdyn_plannedcostcontour     | No             | No           |
| msdyn_plannedsales           | No             | No           |
| msdyn_plannedsales_base      | No             | No           |
| msdyn_plannedsalescontour    | No             | No           |
| msdyn_plannedwork            | No             | No           |
| msdyn_projectid              | Evet            | No           |
| msdyn_projectidname          | No             | No           |
| msdyn_projectteamid          | No             | No           |
| msdyn_projectteamidname      | No             | No           |
| msdyn_start                  | No             | No           |
| msdyn_taskid                 | No             | No           |
| msdyn_taskidname             | No             | No           |
| msdyn_userresourceid         | No             | No           |

### <a name="project-team-member"></a>Proje takımı üyesi

| Mantıksal ad                                     | Oluşturabilir     | Düzenleyebilir     |
|--------------------------------------------------|----------------|--------------|
| msdyn_calendarid                                 | No             | No           |
| msdyn_creategenericteammemberwithrequirementname | No             | No           |
| msdyn_deletestatus                               | No             | No           |
| msdyn_deletestatusname                           | No             | No           |
| msdyn_effort                                     | No             | No           |
| msdyn_effortcompleted                            | No             | No           |
| msdyn_effortremaining                            | No             | No           |
| msdyn_finish                                     | No             | No           |
| msdyn_hardbookedhours                            | No             | No           |
| msdyn_hours                                      | No             | No           |
| msdyn_markedfordeletiontimer                     | No             | No           |
| msdyn_markedfordeletiontimestamp                 | No             | No           |
| msdyn_msprojectclientid                          | No             | No           |
| msdyn_percentage                                 | No             | No           |
| msdyn_requiredhours                              | No             | No           |
| msdyn_softbookedhours                            | No             | No           |
| msdyn_start                                      | No             | No           |

### <a name="project"></a>Project

| Mantıksal ad                           | Oluşturabilir     | Düzenleyebilir     |
|----------------------------------------|----------------|--------------|
| msdyn_actualexpensecost                | No             | No           |
| msdyn_actualexpensecost_base           | No             | No           |
| msdyn_actuallaborcost                  | No             | No           |
| msdyn_actuallaborcost_base             | No             | No           |
| msdyn_actualsales                      | No             | No           |
| msdyn_actualsales_base                 | No             | No           |
| msdyn_contractlineproject              | Evet            | No           |
| msdyn_contractorganizationalunitid     | Evet            | No           |
| msdyn_contractorganizationalunitidname | Evet            | No           |
| msdyn_costconsumption                  | No             | No           |
| msdyn_costestimateatcomplete           | No             | No           |
| msdyn_costestimateatcomplete_base      | No             | No           |
| msdyn_costvariance                     | No             | No           |
| msdyn_costvariance_base                | No             | No           |
| msdyn_duration                         | No             | No           |
| msdyn_effort                           | No             | No           |
| msdyn_effortcompleted                  | No             | No           |
| msdyn_effortestimateatcompleteeac      | No             | No           |
| msdyn_effortremaining                  | No             | No           |
| msdyn_finish                           | Evet            | Evet          |
| msdyn_globalrevisiontoken              | No             | No           |
| msdyn_islinkedtomsprojectclient        | No             | No           |
| msdyn_islinkedtomsprojectclientname    | No             | No           |
| msdyn_linkeddocumenturl                | No             | No           |
| msdyn_msprojectdocument                | No             | No           |
| msdyn_msprojectdocumentname            | No             | No           |
| msdyn_plannedexpensecost               | No             | No           |
| msdyn_plannedexpensecost_base          | No             | No           |
| msdyn_plannedlaborcost                 | No             | No           |
| msdyn_plannedlaborcost_base            | No             | No           |
| msdyn_plannedsales                     | No             | No           |
| msdyn_plannedsales_base                | No             | No           |
| msdyn_progress                         | No             | No           |
| msdyn_remainingcost                    | No             | No           |
| msdyn_remainingcost_base               | No             | No           |
| msdyn_remainingsales                   | No             | No           |
| msdyn_remainingsales_base              | No             | No           |
| msdyn_replaylogheader                  | No             | No           |
| msdyn_salesconsumption                 | No             | No           |
| msdyn_salesestimateatcompleteeac       | No             | No           |
| msdyn_salesestimateatcompleteeac_base  | No             | No           |
| msdyn_salesvariance                    | No             | No           |
| msdyn_salesvariance_base               | No             | No           |
| msdyn_scheduleperformance              | No             | No           |
| msdyn_scheduleperformancename          | No             | No           |
| msdyn_schedulevariance                 | No             | No           |
| msdyn_taskearlieststart                | No             | No           |
| msdyn_teamsize                         | No             | No           |
| msdyn_teamsize_date                    | No             | No           |
| msdyn_teamsize_state                   | No             | No           |
| msdyn_totalactualcost                  | No             | No           |
| msdyn_totalactualcost_base             | No             | No           |
| msdyn_totalplannedcost                 | No             | No           |
| msdyn_totalplannedcost_base            | No             | No           |

### <a name="project-bucket"></a>Proje demeti

| Mantıksal ad          | Oluşturabilir      | Düzenleyebilir     |
|-----------------------|-----------------|--------------|
| msdyn_displayorder    | Evet             | No           |
| msdyn_name            | Evet             | Evet          |
| msdyn_project         | Evet             | No           |
| msdyn_projectbucketid | Evet             | No           |

## <a name="limitations-and-known-issues"></a>Sınırlamalar ve bilinen sorunlar
Aşağıda, sınırlamalar ve bilinen sorunların bir listesi yer almaktadır:

- Proje Zamanlama API'leri yalnızca **Microsoft Project Lisansı olan kullanıcılar** tarafından kullanılabilir. Şu kullanıcılar tarafından kullanılamaz:

    - Uygulama kullanıcıları
    - Sistem kullanıcıları
    - Tümleştirme kullanıcıları
    - Gerekli lisansa sahip olmayan diğer kullanıcılar

- Her bir **OperationSet** yalnızca en fazla 100 işlem içerebilir.
- Her bir kullanıcının açık en fazla 10 **OperationSet**'i olabilir.
- Project Operations şu anda bir proje üzerinde en fazla 500 toplam görevi desteklemektedir.
- **OperationSet** hata durumu ve hata günlükleri şu anda kullanılamıyor.
- [Projelerde ve görevlerde sınırları ve sınırları](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a>Hata işleme

- İşlem kümelerinden oluşturulan hataları gözden geçirmek için **ayarlar** \> **Zamanlama tümleştirme** \> **işlemleri kümeleri**'ne gidin.
- Proje zamanlama hizmetinden oluşturulan hataları gözden geçirmek için **Ayarlar** \> **Zamanlama tümleştirmesi** \> **PSS Hata günlükleri**'ne gidin.

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
