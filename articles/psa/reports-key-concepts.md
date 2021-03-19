---
title: Temel kavramlar
description: Bu konu, Project Service Automation'da kaynak yönetimi için temel kavramlar hakkında bilgi sağlar.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 704aadab3dd1b8b3e22ecdb15cf97cc7cbba1a23
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283347"
---
# <a name="key-concepts"></a>Temel kavramlar

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Aşağıdaki tabloda, Dynamics 365 Project Service Automation uygulamasında kullanılan temel kavramlar tanımlanır.

| Kavram                    | Tanım |
|----------------------------|------------|
| Proje takımı üyesi        | Proje takımının bir parçası olarak bir proje takımı üyesi; ayırmaları olan adlandırılmış bir kaynak, ayırmaları olmayan adlandırılmış bir kaynak veya genel bir kaynak olabilir. Genel kaynakların ayırmaları yoktur, projeye yerleşiklerdir ve projeler genelinde kapasite kısıtlamaları yoktur. |
| Proje genel kaynağı   | Adlandırılmış kaynağı bilmenizi gerektirmeden takım ve personel oluşturabileceğiniz bir proje planı sağlayan bir kaynak yer tutucusu. Proje takvimi, genel kaynağın takvimi olarak kullanılır. Genel kaynaklar bir proje takımına eklenebilir ve görevlere atanabilir. |
| Ayrılan saat sayısı               | Proje çalışmasının tamamlanmasını güvence altına almak için projede kaynak saatleri kesin ayrılmıştır. Ayrılmış saatler kaynağın toplam kapasitesini kullanır. Ayırmalar, genel kaynaklarda değil; yalnızca adlandırılmış kaynaklardadır. |
| Atanan saat sayısı             | Kaynak saatleri proje zamanlamasında görevlere atanır. Atamalar adlandırılmış veya genel kaynaklarda olabilir. Atamalar ayırmalardan bağımsız olabilir. |
| Gerekli saat sayısı             | Gerekli ancak henüz adlandırılmış bir kaynak tarafından karşılanmamış kapasite. Gerekli saatler yalnızca kaynak gereksinimleri oluşturan genel takım üyeleriyle ilgilidir. |
| Talep                     | Geçerli ve gelen iş yükü. Project Service Automation'da talep, kaynak gereksinimleri veya kaynak istekleri olarak gösterilir. |
| Kaynak gereksinimi       | Gerekli kaynaklar için gerekli saatleri, başlangıç ve bitiş tarihlerini, becerileri, coğrafyayı ve diğer fiyatlandırma boyutlarını yakalamada kullanılan bir varlık. Kaynak gereksinimleri, proje takımı üyelerinden veya tek tek oluşturulur. |
| Kaynak isteği           | Kaynak yöneticisinin karşılaması gereken kaynak gereksinimini taşımak için "zarf" olarak kullanılan bir varlık. |
| Kaynağın varsayılan rolü      | Kullanım hesaplaması için bir kaynağın gruplandırıldığı rol. Kaynağın, rol için gerekli becerilere sahip olduğu ve bu rol için hedef kullanımını karşıladığı varsayılmaktadır. |
| Kaynak kuruluş birimi | Kaynağın atandığı kuruluş birimi. |
| Sınır                    | Günlük dağılıma ayrılan görev, gereksinim veya atama saatleri. Örneğin beş günlük 40 saatlik bir görev, günde sekiz saatten beş gün şeklinde sınırlandırılabilir. |
| Mutabakat görünümü        | Her proje takımı üyesinin ayırmalarını ve atamalarını gösteren görünüm. Bu görünüm proje yöneticisinin ayırmalar ve atamalar arasındaki uyuşmazlıkların kontrolüne ve herhangi bir uyuşmazlık varsa düzeltici eylemde bulunmasına olanak sağlar. |
| Çalışma saatleri                 | Kaynak kapasitesini, çalışma saatlerini ve çalışma dışı saatleri belirlemek için kullanılan bir varlık. Bu varlık, kaynak takvimi olarak da adlandırılır. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]