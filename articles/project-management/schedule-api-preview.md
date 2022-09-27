---
title: Zamanlama varlıkları ile işlemler gerçekleştirmek için Proje zamanlama API'lerini kullanma
description: Bu makalede proje zamanlama API'lerinin kullanımına yönelik bilgiler ve örnekler sağlanmaktadır.
author: sigitac
ms.date: 01/13/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 159d395efff98f2af780e5ed1e5ab3d6483cba89
ms.sourcegitcommit: b1c26ea57be721c5b0b1a33f2de0380ad102648f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/20/2022
ms.locfileid: "9541149"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Zamanlama varlıkları ile işlemler gerçekleştirmek için Proje zamanlama API'lerini kullanma

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_


**Zamanlama varlıkları**

Proje zamanlaması API'leri **Zamanlama varlıklarıyla** oluşturma, güncelleştirme ve silme işlemleri gerçekleştirme olanağı sunar. Bu varlıklar, webe yönelik projelerde Zamanlama altyapısı üzerinden yönetilir. Önceki Dynamics 365 Project Operations sürümlerinde **Zamanlama varlıklarıyla** oluşturma, güncelleştirme ve silme işlemleri kısıtlanmıştı.

Aşağıdaki tabloda Proje zamanlama varlıklarının tam listesi verilmiştir.

| **Varlık adı**         | **Varlık mantıksal adı**     |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Proje Görevi            | msdyn_projecttask           |
| Proje Görevi Bağımlılığı | msdyn_projecttaskdependency |
| Kaynak Atama     | msdyn_resourceassignment    |
| Proje Demeti          | msdyn_projectbucket         |
| Proje Takımı Üyesi     | msdyn_projectteam           |
| Proje Denetim Listeleri      | msdyn_projectchecklist      |
| Proje Etiketi           | msdyn_projectlabel          |
| Etiketlenecek Proje Görevi   | msdyn_projecttasktolabel    |
| Proje Sprint'i          | msdyn_projectsprint         |

**OperationSet**

OperationSet, bir hareket içinde işlenmesi gereken, zamanlamayı etkileyen birkaç isteğin işlenmesi gerektiğinde kullanılabilen bir çalışma birimi düzenidir.

**Proje zamanlama API'leri**

Aşağıda geçerli Proje zamanlama API'lerinin listesi yer almaktadır.

| **API**                                 | Tanım                                                                                                                       |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| **msdyn_CreateProjectV1**               | Bu API, proje oluşturmak için kullanılır. Proje ve varsayılan proje paketi hemen oluşturulur.                         |
| **msdyn_CreateTeamMemberV1**            | Bu API, proje takım üyesi oluşturmak için kullanılır. Takım üyesi kaydı hemen oluşturulur.                                  |
| **msdyn_CreateOperationSetV1**          | Bu API, bir hareket içinde gerçekleştirilmesi gereken çok sayıda isteği zamanlamak için kullanılır.                                        |
| **msdyn_PssCreateV1**                   | Bu API, varlık oluşturmak için kullanılır. Varlık, oluşturma işlemini destekleyen Proje zamanlama varlıklarından herhangi biri olabilir. |
| **msdyn_PssUpdateV1**                   | Bu API, varlık güncelleştirmek için kullanılır. Varlık, güncelleştirme işlemini destekleyen Proje zamanlama varlıklarından herhangi biri olabilir  |
| **msdyn_PssDeleteV1**                   | Bu API, varlık silmek için kullanılır. Varlık, silme işlemini destekleyen Proje zamanlama varlıklarından herhangi biri olabilir. |
| **msdyn_ExecuteOperationSetV1**         | Bu API, bir işlem kümesindeki tüm işlemleri yürütmek için kullanılır.                                                 |
| **msdyn_PssUpdateResourceAssignmentV1** | Bu API, Kaynak Atamasının planlanan çalışma sınırını güncelleştirmek için kullanılır.                                                        |



**OperationSet ile Proje zamanlama API'lerini kullanma**

Hem **CreateProjectV1** hem de **CreateTeamMemberV1** içeren kayıtlar hemen oluşturulduğundan, bu API'ler doğrudan **OperationSet** içinde kullanılamaz. Ancak API'yi kullanarak gerekli kayıtları oluşturup bir **OperationSet** oluşturabilir ve ardından **OperationSet** içinde bu önceden oluşturulmuş kayıtları kullanabilirsiniz.

**Desteklenen işlemler**

| **Zamanlama varlığı**   | **Oluştur** | **Update** | **Silme** | **Dikkat edilmesi gereken önemli hususlar**                                                                                                                                                                                                                                                                                                                            |
|-------------------------|------------|------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Proje görevi            | Evet        | Evet        | Evet        | **Progress**, **EffortCompleted** ve **EffortRemaining** alanları, Project for the Web'de düzenlenebilir ancak Project Operations'ta düzenlenemez.                                                                                                                                                                                             |
| Proje görevi bağımlılığı | Evet        | Hayı         | Evet        | Proje görev bağımlılığı kayıtları güncelleştirilmemiş. Bunun yerine, eski bir kayıt silinebilir ve yeni bir kayıt oluşturulabilir.                                                                                                                                                                                                                                 |
| Kaynak atama     | Evet        | Evet\*      | Evet        | Şu alanlara sahip işlemler desteklenmez: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** ve **PlannedWork**. Kaynak atama kayıtları güncelleştirilmemiş. Bunun yerine, eski kayıt silinebilir ve yeni bir kayıt oluşturulabilir. Kaynak Atama sınırlarını güncelleştirmek için ayrı bir API sağlanmıştır. |
| Proje demeti          | Evet        | Evet        | Evet        | Varsayılan paket, **CreateProjectV1** API'sini kullanarak oluşturulur. Proje paketleri oluşturma ve silme desteği, Güncelleştirme Sürümü 16'da eklenmiştir.                                                                                                                                                                                                   |
| Proje takımı üyesi     | Evet        | Evet        | Evet        | Oluşturma işlemi için **CreateTeamMemberV1** API'sini kullanın.                                                                                                                                                                                                                                                                                           |
| Project                 | Evet        | Evet        |            | Şu alanlara sahip işlemler desteklenmez: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** ve **Duration**.                                                                                       |
| Proje Denetim Listeleri      | Evet        | Evet        | Evet        |                                                                                                                                                                                                                                                                                                                                                         |
| Proje Etiketi           | Hayı         | Evet        | Hayı         | Etiket adları değiştirilebilir. Bu özellik, yalnızca Project for the Web için kullanılabilir                                                                                                                                                                                                                                                                      |
| Etiketlenecek Proje Görevi   | Evet        | Hayı         | Evet        | Bu özellik, yalnızca Project for the Web için kullanılabilir                                                                                                                                                                                                                                                                                                  |
| Proje Sprint'i          | Evet        | Evet        | Evet        | **Başlangıç** alanındaki tarih, **Bitiş** alanındaki tarihten daha erken bir zaman olmalıdır. Aynı projenin sprint'leri birbiriyle çakışamaz. Bu özellik, yalnızca Project for the Web için kullanılabilir                                                                                                                                                                    |




Kimlik özelliği isteğe bağlıdır. Sağlanmışsa, sistem bunu kullanmayı dener ve kullanılamaz ise bir özel durum oluşturur. Sağlanmazsa, sistem bunu oluşturacaktır.

**Sınırlamalar ve bilinen sorunlar**

Aşağıda, sınırlamalar ve bilinen sorunların bir listesi yer almaktadır:

-   Proje Zamanlama API'leri yalnızca **Microsoft Project Lisansı olan kullanıcılar** tarafından kullanılabilir. Şu kullanıcılar tarafından kullanılamaz:
    -   Uygulama kullanıcıları
    -   Sistem kullanıcıları
    -   Tümleştirme kullanıcıları
    -   Gerekli lisansa sahip olmayan diğer kullanıcılar
-   Her bir **OperationSet** yalnızca en fazla 100 işlem içerebilir.
-   Her bir kullanıcının açık en fazla 10 **OperationSet**'i olabilir.
-   Project Operations şu anda bir proje üzerinde en fazla 500 toplam görevi desteklemektedir.
-   Her Güncelleştirme Kaynak Ataması Sınır işlemi, tek bir işlem olarak sayılır.
-   Her bir güncelleştirilmiş sınır listesinde en fazla 100 zaman dilimi bulunabilir.
-   **OperationSet** hata durumu ve hata günlükleri şu anda kullanılamıyor.
-   Proje başına en fazla 400 sprint bulunur.
-   [Proje ve görevlerde sınır ve kısıtlamalar](/project-for-the-web/project-for-the-web-limits-and-boundaries).
-   Etiketler, şu an için yalnızca Project for the Web için kullanılabilir.

**Hata işleme**

-   İşlem kümelerinden oluşturulan hataları gözden geçirmek için **ayarlar** \> **Zamanlama tümleştirme** \> **işlemleri kümeleri**'ne gidin.
-   Proje zamanlama hizmetinden oluşturulan hataları gözden geçirmek için **Ayarlar** \> **Zamanlama tümleştirmesi** \> **PSS Hata günlükleri**'ne gidin.

**Kaynak Atama Sınırlarını Düzenleme**

Varlık güncelleştiren diğer proje zamanlama API'lerinin aksine, kaynak ataması sınır API'si yalnızca tek bir varlık (msydn_resourceassignment) üzerindeki tek bir varlığın (msdyn_plannedwork) güncelleştirmelerinden sorumludur.

Zamanlama modunun aşağıdaki gibi olduğunu varsayalım:

-   **sabit birimler**
-   proje takvimi; Pazartesi, Salı, Perşembe, Cuma (ÇARŞAMBA GÜNÜ YOK) günleri 9-17 saatleri arasındadır (9-17pst)
-   kaynak takvimi ise Pazartesi'den Cuma'ya 9-13 PST saatleri arasındadır

Bu atama, günde dört saat olmak üzere bir haftalıktır. Bunun nedeni, kaynak takviminin 9-13 PST arasında, yani günde dört saat olmasıdır.

| &nbsp;     | Görev | Başlangıç Tarihi | Bitiş Tarihi  | Miktar | 13/6/2022 | 14/6/2022 | 15/6/2022 | 16/6/2022 | 17/6/2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-13 çalışanı |  T1  | 13/6/2022  | 17/6/2022 | 20       | 4         | 4         | 4         | 4         | 4         |

Örneğin, çalışanın bu haftanın her günü yalnızca üç saat çalışmasını ve diğer görevler için bir saat kullanmasını istiyorsanız:

#### <a name="updatedcontours-sample-payload"></a>UpdatedContours örnek yükü:

```json
[{

"minutes":900.0,

"start":"2022-06-13T00:00:00-07:00",

"end":"2022-06-18T00:00:00-07:00"

}]
```

Güncelleştirme Sınırı Zamanlama API'ı çalıştırıldıktan sonra atama bu şekildedir.

| &nbsp;     | Görev | Başlangıç Tarihi | Bitiş Tarihi  | Miktar | 13/6/2022 | 14/6/2022 | 15/6/2022 | 16/6/2022 | 17/6/2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-13 çalışanı | T1   | 13/6/2022  | 17/6/2022 | 15       | 3         | 3         | 3         | 3         | 3         |


**Örnek senaryo**

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

** Ek örnekler

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
