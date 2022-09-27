---
title: Güvenlik ve onaylar
description: Bu makale, Microsoft Dynamics 365 Project Operations'ta onaylar ile çalışma için güvenlik kurulumu hakkında bilgi sağlar.
author: stsporen
ms.date: 08/29/2022
ms.topic: security
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: bc33f63f66bdcf1470e5d9386cfc3661774436fd
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/16/2022
ms.locfileid: "9525374"
---
# <a name="security-and-approvals"></a>Güvenlik ve onaylar

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Microsoft Dynamics 365 Project Operations; zaman, gider ve malzeme girişlerinin onaylanmasını sağlamak için iki güvenlik rolü kullanır:

- Projeyi Onaylayan
- Projeyi Onaylayan Yönetici

## <a name="project-approver"></a>Projeyi Onaylayan

Proje zamanı, gider ve malzeme girişlerini onaylamak için **Proje Onaylayan** güvenlik rolüne sahip olmanız gerekir. Ayrıca, **Proje** gibi ilgili ilişkili varlıklara da erişiminiz olmalıdır. Bu erişim, **Proje Yöneticisi** rolüne sahip bir kişi tarafından atanabilir. Ayrıca, projenin bir takım üyesi olmanız ve onaylayan olarak işaretlenmiş olmanız gerekir.

Proje dışı girişleri onaylamak için gönderenin yöneticisi olmanız gerekir.

## <a name="project-approver-admin"></a>Projeyi Onaylayan Yönetici

> [!NOTE]
> Proje Onaylayan Yönetici işlevini kullanabilmek için [Onay ayarları](approval-sets.md) özelliğinin etkinleştirilmesi gerekir.

**Proje Onaylayan Yöneticisi** güvenlik rolü, kullanıcıların ilkeleri atlamasına ve tüm projelerde bu girdilerin onaylanmasına izin verir. Bu rolün atanması, takım üyeliği gerektiren ve onaylayan olarak işaretlenmiş doğrulama mantığını atlar. Ayrıca, **Proje** gibi ilgili ilişkili varlıklara da erişiminiz olmalıdır. Bu erişim, **Proje Yöneticisi** rolüne sahip bir kişi tarafından atanabilir.

SYSTEM kullanıcı bağlamı, doğrulamaları Proje Onaylayan Yönetici güvenlik rolü ile aynı şekilde atlar.
