---
title: Kaynak yönetimi modlarına genel bakış
description: Bu konuda, Dynamics 365 Project Operations içindeki Kaynak yönetimi özellikleri hakkında bilgiler sağlanmaktadır.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 73ba6190e2e366f22372102d14d26f6d71ba0bc1
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4118542"
---
# <a name="resource-management-modes-overview"></a>Kaynak yönetimi modlarına genel bakış

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_


Dynamics 365 Project Operations genel ayırma akışını yürütebilmenizi sağlayan iki modu destekler. Yönetim modu, proje parametresi olarak tanımlanır ve işinizde değişiklik gerekiyorsa değiştirilebilir.    

## <a name="central-mode"></a>Merkezi mod
Merkezi mod, kaynakların projelere tahsisatını merkezileştiren kuruluşlara Proje yöneticilerinin proje düzeyinde kaynak gereksinimlerini tanımlayabilmesini sağlamak için bir yol sunar. Kaynak gereksinimlerinin yerine getirilmesi görevi Kaynak yöneticisine verilir. Proje yöneticileri, Kaynak yöneticisinin önerdiği kaynakları kabul edebilir veya reddedebilir.

![Merkezi Mod](./media/resource-management-central.png)

Merkezi modda kaynakları yönetmek için bkz:

- [Göreve genel ayrılabilir kaynaklar atama ve kaynak gereksinimleri oluşturma](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Kaynak gereksinimlerinden adlandırılmış kaynaklar ayırma](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [Kaynak isteği gönderme](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [Kaynak isteğini karşılama](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [Kaynak isteğinden bir önerilen proje kaynağını kabul etme veya reddetme](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Karma mod
Karma mod, kaynakların tahsisatında esneklik isteyen kuruluşlarda Proje yöneticilerinin ve Kaynak yöneticilerinin kaynakları ayırabilmelerini sağlar.

![Karma Mod](./media/resource-management-hybrid.png)

Desteklenen Merkezi mod işlemine ek olarak, Karma modda desteklenen diğer tüm ayırma akışlarını yönetmek için aşağıdaki konulara bakın:

Kaynağı doğrudan bir projeye ayırma:
- [Proje takımına adlandırılmış ayrılabilir kaynaklar ayırma ve görevler atama](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

Kaynak gereksinimden bir kaynak ayırma:
- [Göreve genel ayrılabilir kaynaklar atama ve kaynak gereksinimleri oluşturma](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Kaynak gereksinimlerinden adlandırılmış kaynaklar ayırma](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
