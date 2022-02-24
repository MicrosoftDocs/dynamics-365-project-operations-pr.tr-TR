---
title: Gider raporunda birden çok onaylayan
description: Bu konu birden çok kişi tarafından onay gerektiren gider raporları hakkında bilgi sağlar.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0fbe1c93c5359a6be493e3c4e1b27b06dbb48002
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271737"
---
# <a name="multiple-approvers-on-an-expense-report"></a>Gider raporunda birden çok onaylayan

Kuruluşunuzun gider onay ilkelerine bağlı olarak, bir veya birden çok kişinin bir çalışan tarafından gönderilen gider raporunu onaylaması gerekebilir. Gider raporu onayı için iş akışı işlemi ayarladığınızda, gider raporunu bir veya daha fazla onaylayana yönelik görevleri veya adımları içeren iş akışı öğeleri ekleyebilirsiniz. Örneğin, tüm gider raporlarının ilk önce raporu gönderen çalışanın yöneticisi ve ardından borç hesapları koordinatörü tarafından onaylanmasını şart koşabilirsiniz.

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