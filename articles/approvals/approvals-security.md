---
title: Güvenlik ve onaylar
description: Bu makale, Microsoft Dynamics 365 Project Operations'ta onaylar ile çalışma için güvenlik kurulumu hakkında bilgi sağlar.
author: stsporen
ms.date: 08/29/2022
ms.topic: security
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 0dcadaa142bf46e4c54f160759602ac749022108
ms.sourcegitcommit: 73aff2b3c5e5b8a2254735b0b25931cbb6754c87
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709422"
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

**Proje Onaylayan Yöneticisi** güvenlik rolü, kullanıcıların ilkeleri atlamasına ve tüm projelerde bu girdilerin onaylanmasına izin verir. Bu rolün atanması, takım üyeliği gerektiren ve onaylayan olarak işaretlenmiş doğrulama mantığını atlar. **Proje** gibi ilgili tablolara, size atanan güvenlik rolleri yoluyla erişmeniz gerekir.

SYSTEM kullanıcı bağlamı, doğrulamaları Proje Onaylayan Yönetici güvenlik rolü ile aynı şekilde atlar.
