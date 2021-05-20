---
title: Proje Kopyalama ile proje şablonları geliştirme
description: Bu konu, proje özel eylemini kullanarak proje şablonlarının nasıl oluşturulacağı hakkında bilgiler sağlar.
author: stsporen
manager: Annbe
ms.date: 01/21/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cc17df0c73b276048f7c4b04bd9dc6644e828dc0
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949838"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="3c23f-103">Proje Kopyalama ile proje şablonları geliştirme</span><span class="sxs-lookup"><span data-stu-id="3c23f-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="3c23f-104">_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="3c23f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="3c23f-105">Dynamics 365 Project Operations, proje kopyalama ve atamaları rolü temsil eden genel kaynaklara döndürme yeteneğini destekler.</span><span class="sxs-lookup"><span data-stu-id="3c23f-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="3c23f-106">Müşteriler bu işlevi temel proje şablonları oluşturmak için kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="3c23f-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="3c23f-107">**Projeyi Kopyala** seçeneğini belirlediğinizde , hedef projenin durumu güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="3c23f-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="3c23f-108">kopyalama eyleminin ne zaman tamamlandığını belirlemek için **durum açıklaması** kullanın.</span><span class="sxs-lookup"><span data-stu-id="3c23f-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="3c23f-109">**Kopyalama projesi**'ni seçmek, hedef proje varlığında bir hedef tarih algılanmazsa projenin başlangıç tarihini geçerli başlangıç tarihine güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3c23f-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="3c23f-110">Proje özel eylemini Kopyala</span><span class="sxs-lookup"><span data-stu-id="3c23f-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="3c23f-111">Veri Akışı Adı</span><span class="sxs-lookup"><span data-stu-id="3c23f-111">Name</span></span> 

<span data-ttu-id="3c23f-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="3c23f-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="3c23f-113">Giriş parametreleri</span><span class="sxs-lookup"><span data-stu-id="3c23f-113">Input parameters</span></span>
<span data-ttu-id="3c23f-114">Üç giriş parametresi vardır:</span><span class="sxs-lookup"><span data-stu-id="3c23f-114">There are three input parameters:</span></span>

| <span data-ttu-id="3c23f-115">Parametre</span><span class="sxs-lookup"><span data-stu-id="3c23f-115">Parameter</span></span>          | <span data-ttu-id="3c23f-116">Tür</span><span class="sxs-lookup"><span data-stu-id="3c23f-116">Type</span></span>   | <span data-ttu-id="3c23f-117">Değerler</span><span class="sxs-lookup"><span data-stu-id="3c23f-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="3c23f-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="3c23f-118">ProjectCopyOption</span></span>  | <span data-ttu-id="3c23f-119">String</span><span class="sxs-lookup"><span data-stu-id="3c23f-119">String</span></span> | <span data-ttu-id="3c23f-120">**{"removeNamedResources":true}** veya **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="3c23f-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="3c23f-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="3c23f-121">SourceProject</span></span>      | <span data-ttu-id="3c23f-122">Varlık Başvurusu</span><span class="sxs-lookup"><span data-stu-id="3c23f-122">Entity Reference</span></span> | <span data-ttu-id="3c23f-123">Kaynak Proje</span><span class="sxs-lookup"><span data-stu-id="3c23f-123">Source Project</span></span> |
| <span data-ttu-id="3c23f-124">Hedef</span><span class="sxs-lookup"><span data-stu-id="3c23f-124">Target</span></span>             | <span data-ttu-id="3c23f-125">Varlık Başvurusu</span><span class="sxs-lookup"><span data-stu-id="3c23f-125">Entity Reference</span></span> | <span data-ttu-id="3c23f-126">Hedef Proje</span><span class="sxs-lookup"><span data-stu-id="3c23f-126">Target Project</span></span> |


- <span data-ttu-id="3c23f-127">**{"clearTeamsAndAssignments":true}**: Web için Project'in varsayılan davranışı ve tüm atamaları ve takım üyelerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3c23f-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="3c23f-128">**{"removeNamedResources":true}** Project Operations için varsayılan davranışı doğrudur ve atamaları genel kaynaklara geri döndürür.</span><span class="sxs-lookup"><span data-stu-id="3c23f-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="3c23f-129">Eylemlerde varsayılanlar hakkında daha fazla bilgi için bkz. [web API'si eylemleri kullanma](/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="3c23f-129">For more defaults on actions, see [Use Web API actions](/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="3c23f-130">Kopyalanacak alanları belirt</span><span class="sxs-lookup"><span data-stu-id="3c23f-130">Specify fields to copy</span></span> 
<span data-ttu-id="3c23f-131">Eylem çağrıldığında proje kopyalanırken kopyalanacak alanları belirlemek için proje görünümünde **Proje Kopyala**, **Proje Sütunlarını Kopyala** görünür.</span><span class="sxs-lookup"><span data-stu-id="3c23f-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>


### <a name="example"></a><span data-ttu-id="3c23f-132">Örnek</span><span class="sxs-lookup"><span data-stu-id="3c23f-132">Example</span></span>
<span data-ttu-id="3c23f-133">Aşağıdaki örnekte, **removeNamedResources** parametre kümesiyle **CopyProject** özel eyleminin nasıl çağrılacağı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="3c23f-133">The following example shows how to call the **CopyProject** custom action with the **removeNamedResources** parameter set.</span></span>
```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    [DataContract]
    public class ProjectCopyOption
    {
        /// <summary>
        /// Clear teams and assignments.
        /// </summary>
        [DataMember(Name = "clearTeamsAndAssignments")]
        public bool ClearTeamsAndAssignments { get; set; }

        /// <summary>
        /// Replace named resource with generic resource.
        /// </summary>
        [DataMember(Name = "removeNamedResources")]
        public bool ReplaceNamedResources { get; set; }
    }

    public class CopyProjectSample
    {
        private IOrganizationService organizationService;

        public CopyProjectSample(IOrganizationService organizationService)
        {
            this.organizationService = organizationService;
        }

        public void SampleRun()
        {
            // Example source project GUID
            Guid sourceProjectId = new Guid("11111111-1111-1111-1111-111111111111");
            var sourceProject = new Entity("msdyn_project", sourceProjectId);

            Entity targetProject = new Entity("msdyn_project");
            targetProject["msdyn_subject"] = "Example Project";
            targetProject.Id = organizationService.Create(targetProject);

            ProjectCopyOption copyOption = new ProjectCopyOption();
            copyOption.ReplaceNamedResources = true;

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, ProjectCopyOption projectCopyOption)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV2");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;
            req["ProjectCopyOption"] = JsonConvert.SerializeObject(projectCopyOption);
            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```


[!INCLUDE[footer-include](../includes/footer-banner.md)]