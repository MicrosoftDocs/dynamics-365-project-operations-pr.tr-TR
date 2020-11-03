---
title: Gider raporları ve birden çok onaylayan
description: Bu konu birden çok kişi tarafından onay gerektiren gider raporları hakkında bilgi sağlar.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 548673541cee5ce598721f94415c0444995c8325
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086327"
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
