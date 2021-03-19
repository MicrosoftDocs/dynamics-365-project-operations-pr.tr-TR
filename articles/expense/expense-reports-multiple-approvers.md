---
title: Gider raporları ve birden çok onaylayan
description: Bu konu birden çok kişi tarafından onay gerektiren gider raporları hakkında bilgi sağlar.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9b9826c89e9deb870adb053f82bd049906f56052
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276552"
---
# <a name="expense-reports-and-multiple-approvers"></a>Gider raporları ve birden çok onaylayan

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Kuruluşunuzun gider onay ilkelerine bağlı olarak, bir veya birden çok kişinin gönderilen gider raporunu onaylaması gerekebilir. Gider raporu onayı için iş akışı işlemi ayarladığınızda, gider raporunu bir veya daha fazla onaylayana yönelik görevleri veya adımları içeren iş akışı öğeleri ekleyebilirsiniz. Örneğin, tüm gider raporlarının raporu gönderen çalışanın yöneticisi ve borç hesapları koordinatörü olacak şekilde iki ayrı kişi tarafından onaylanmasını şart koşabilirsiniz.

Gider raporunu birden çok onaylayan bulunması gerektiğine karar verdiğinizde, iş akışı öğelerini aşağıdaki yollardan biriyle ekleyebilirsiniz:

- Tek adım içeren bir onay öğesi ekleyin. Örneğin, adım bir kullanıcı grubuna bir gider raporu atanmasını ve kullanıcı grubu üyelerinin yüzde 50'sinin onayını gerektirebilir.
- Birden çok adım içeren bir onay öğesi ekleyin. Örneğin, onay öğesi aşağıdaki adımları içerebilir:

    1. Gider raporunu gönderen çalışanın yöneticisi onaylar.
    2. Borç hesapları görevlisi makbuzları ve gider raporu maddelerini doğrular.
    3. Bütçe sahibi gider raporunu onaylar.

- Her biri bir adım olan birden fazla onay öğesi ekleyin. Örneğin, aşağıdaki adımların her biri için ayrı bir onay öğesi ekleyebilirsiniz:

    1. Çalışanın yöneticisi gider raporunu onaylar.
    2. Bütçe sahibi gider raporunu onaylar.


[!INCLUDE[footer-include](../includes/footer-banner.md)]