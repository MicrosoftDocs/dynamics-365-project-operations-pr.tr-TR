---
title: Proje Kopyalama ile proje şablonları geliştirme
description: Bu konu, proje özel eylemini kullanarak proje şablonlarının nasıl oluşturulacağı hakkında bilgiler sağlar.
author: stsporen
ms.date: 03/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 72aa2db7c717eeab85ada448c673bf702087baeb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590925"
---
# <a name="develop-project-templates-with-copy-project"></a>Proje Kopyalama ile proje şablonları geliştirme

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Dynamics 365 Project Operations, proje kopyalama ve atamaları rolü temsil eden genel kaynaklara döndürme yeteneğini destekler. Müşteriler bu işlevi temel proje şablonları oluşturmak için kullanabilir.

**Projeyi Kopyala** seçeneğini belirlediğinizde , hedef projenin durumu güncelleştirilir. kopyalama eyleminin ne zaman tamamlandığını belirlemek için **durum açıklaması** kullanın. **Kopyalama projesi**'ni seçmek, hedef proje varlığında bir hedef tarih algılanmazsa projenin başlangıç tarihini geçerli başlangıç tarihine güncelleştirir.

## <a name="copy-project-custom-action"></a>Proje özel eylemini Kopyala

### <a name="name"></a>Veri Akışı Adı 

msdyn\_CopyProjectV3

### <a name="input-parameters"></a>Giriş parametreleri

Üç giriş parametresi vardır:

- **ReplaceNamedResources** veya **ClearTeamsAndAssignments** – Seçeneklerden yalnızca birini belirleyin. Her iki seçeneği de belirlemeyin.

    - **\{"ReplaceNamedResources":true\}** – Project Operations için varsayılan davranış. Adlandırılmış kaynaklar, genel kaynaklarla değiştirilir.
    - **\{"ClearTeamsAndAssignments":true\}** – Project for the Web için varsayılan davranış. Tüm atamalar ve takım üyeleri kaldırılır.

- **SourceProject** – Kopyalanacak kaynak projenin varlık başvurusu. Bu parametre boş olamaz.
- **Hedef** – Kopyalanacak hedef projenin varlık başvurusu. Bu parametre boş olamaz.

Aşağıdaki tabloda üç parametrenin özeti verilmiştir.

| Parametre                | Type             | Değer                 |
|--------------------------|------------------|-----------------------|
| ReplaceNamedResources    | Boolean          | **Doğru** veya **Yanlış** |
| ClearTeamsAndAssignments | Boolean          | **Doğru** veya **Yanlış** |
| SourceProject            | Varlık Başvurusu | Kaynak proje    |
| Target                   | Varlık Başvurusu | Hedef proje    |

Eylemlerde varsayılanlar hakkında daha fazla bilgi için bkz. [web API'si eylemleri kullanma](/powerapps/developer/common-data-service/webapi/use-web-api-actions).

### <a name="validations"></a>Doğrulamalar

Aşağıdaki doğrulamalar yapılır.

1. Null özelliği, kuruluştaki her iki projenin de varlığını doğrulamak için kaynak ve hedef projeleri denetler ve alır.
2. Sistem, aşağıdaki koşulları onaylayarak hedef projenin kopyalama için geçerli olduğunu doğrular:

    - Projede (**Görevler** sekmesinin seçimi dahil) önceden oluşturulmuş bir etkinlik yoktur ve proje yeni oluşturulmuştur.
    - Bu projede önceden oluşturulmuş bir kopya yoktur, içeri aktarma istenmemiştir ve proje **Başarısız** durumunda değildir.

3. İşlem HTTP kullanılarak çağrılmaz.

## <a name="specify-fields-to-copy"></a>Kopyalanacak alanları belirt

Eylem çağrıldığında proje kopyalanırken kopyalanacak alanları belirlemek için proje görünümünde **Proje Kopyala**, **Proje Sütunlarını Kopyala** görünür.

### <a name="example"></a>Örnek

Aşağıdaki örnekte, **removeNamedResources** parametre kümesi ile **CopyProjectV3** özel eyleminin nasıl çağrılacağı gösterilmektedir.

```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

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
            targetProject["msdyn_subject"] = "Example Project - Copy";
            targetProject.Id = organizationService.Create(targetProject);

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption, true, false);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, bool replaceNamedResources = true, bool clearTeamsAndAssignments = false)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV3");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;

            if (replaceNamedResources)
            {
                req["ReplaceNamedResources"] = true;
            }
            else
            {
                req["ClearTeamsAndAssignments"] = true;
            }

            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```

[!INCLUDE[footer-include](../includes/footer-banner.md)]
