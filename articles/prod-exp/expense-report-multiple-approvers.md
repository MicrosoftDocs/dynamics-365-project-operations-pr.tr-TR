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
ms.openlocfilehash: ce24b156a268f9f5aada35f9314d2d9c6607200b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086480"
---
# <a name="multiple-approvers-on-an-expense-report"></a>Gider raporunda birden çok onaylayan

[!include [banner](../includes/banner.md)]

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
