---
title: Kaynak yönetimi modlarına genel bakış
description: Bu konuda, Dynamics 365 Project Operations'ta Kaynak yönetimi özelliği hakkında bilgiler sağlanmaktadır.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.custom: intro-internal
ms.openlocfilehash: 41265534661e51565bf31105ef69cec9b3b181c3
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/07/2021
ms.locfileid: "6367915"
---
# <a name="resource-management-modes-overview"></a>Kaynak yönetimi modlarına genel bakış

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_


Dynamics 365 Project Operations, genel ayırma akışını yürütmeniz için iki modu destekler. Yönetim modu, proje parametresi olarak tanımlanır ve işinizde değişiklik gerekiyorsa değiştirilebilir.    

## <a name="central-mode"></a>Merkezi mod
Merkezi mod, kaynakların projelere tahsisatını merkezileştiren kuruluşlara Proje yöneticilerinin proje düzeyinde kaynak gereksinimlerini tanımlayabilmesini sağlamak için bir yol sunar. Kaynak gereksinimlerinin yerine getirilmesi görevi Kaynak yöneticisine verilir. Proje yöneticileri, Kaynak yöneticisinin önerdiği kaynakları kabul edebilir veya reddedebilir.

![Merkezi Mod](./media/resource-management-central.png)

Merkezi modda kaynakları yönetmek için bkz:

- [Göreve genel ayrılabilir kaynaklar atama ve kaynak gereksinimleri oluşturma](/dynamics365/project-service/assign-generic-bookable-resource)
- [Kaynak gereksinimlerinden adlandırılmış kaynaklar ayırma](/dynamics365/project-service/book-named-resource)
- [Kaynak isteği gönderme](/dynamics365/project-service/submit-resource-request)
- [Kaynak isteğini karşılama](/dynamics365/project-service/resource-management-fulfill-requests)
- [Kaynak isteğinden bir önerilen proje kaynağını kabul etme veya reddetme](/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Karma mod
Karma mod, kaynakların tahsisatında esneklik isteyen kuruluşlarda Proje yöneticilerinin ve Kaynak yöneticilerinin kaynakları ayırabilmelerini sağlar.

![Karma Mod](./media/resource-management-hybrid.png)

Desteklenen Merkezi mod işlemine ek olarak, Karma modda desteklenen diğer tüm ayırma akışlarını yönetmek için aşağıdaki konulara bakın:

Kaynağı doğrudan bir projeye ayırma:
- [Proje takımına adlandırılmış ayrılabilir kaynaklar ayırma ve görevler atama](/dynamics365/project-service/assign-named-bookable-resource)

Kaynak gereksinimden bir kaynak ayırma:
- [Göreve genel ayrılabilir kaynaklar atama ve kaynak gereksinimleri oluşturma](/dynamics365/project-service/assign-generic-bookable-resource)
- [Kaynak gereksinimlerinden adlandırılmış kaynaklar ayırma](/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]