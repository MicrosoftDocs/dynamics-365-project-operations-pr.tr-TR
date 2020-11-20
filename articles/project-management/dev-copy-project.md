---
title: Proje Kopyalama ile proje şablonları geliştirme
description: Bu konu, proje özel eylemini kullanarak proje şablonlarının nasıl oluşturulacağı hakkında bilgiler sağlar.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 0100c29873be6346614e958ef6ea0c77da2c9590
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131637"
---
# <a name="develop-project-templates-with-copy-project"></a>Proje Kopyalama ile proje şablonları geliştirme

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Dynamics 365 Project Operations bir projeyi kopyalamanın ve tüm atamaları rolü temsil eden genel kaynaklara geri döndürbilme yeteneğini destekler. Müşteriler bu işlevi temel proje şablonları oluşturmak için kullanabilir.

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
