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
ms.openlocfilehash: 87696b41db20e9ec70270c850d9acfe05df8cd84
ms.sourcegitcommit: d5004acb6f1c257b30063c873896fdea92191e3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/22/2021
ms.locfileid: "5045033"
---
# <a name="develop-project-templates-with-copy-project"></a>Proje Kopyalama ile proje şablonları geliştirme

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations, proje kopyalama ve atamaları rolü temsil eden genel kaynaklara döndürme yeteneğini destekler. Müşteriler bu işlevi temel proje şablonları oluşturmak için kullanabilir.

**Projeyi Kopyala** seçeneğini belirlediğinizde , hedef projenin durumu güncelleştirilir. kopyalama eyleminin ne zaman tamamlandığını belirlemek için **durum açıklaması** kullanın. **Kopyalama projesi**'ni seçmek, hedef proje varlığında bir hedef tarih algılanmazsa projenin başlangıç tarihini geçerli başlangıç tarihine güncelleştirir.

## <a name="copy-project-custom-action"></a>Proje özel eylemini Kopyala 

### <a name="name"></a>Veri Akışı Adı 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>Giriş parametreleri
Üç giriş parametresi vardır:

| Parametre          | Tür   | Değerler                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | String | **{"removeNamedResources":true}** veya **{"clearTeamsAndAssignments":true}** |
| SourceProject      | Varlık Başvurusu | Kaynak Proje |
| Hedef             | Varlık Başvurusu | Hedef Proje |


- **{"clearTeamsAndAssignments":true}**: Web için Project'in varsayılan davranışı ve tüm atamaları ve takım üyelerini kaldırır.
- **{"removeNamedResources":true}** Project Operations için varsayılan davranışı doğrudur ve atamaları genel kaynaklara geri döndürür.

Eylemlerde varsayılanlar hakkında daha fazla bilgi için bkz. [web API'si eylemleri kullanma](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>Kopyalanacak alanları belirt 
Eylem çağrıldığında proje kopyalanırken kopyalanacak alanları belirlemek için proje görünümünde **Proje Kopyala**, **Proje Sütunlarını Kopyala** görünür.


### <a name="example"></a>Örnek
Aşağıdaki örnekte, **removeNamedResources** parametre kümesiyle **CopyProject** özel eyleminin nasıl çağrılacağı gösterilmektedir.
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
