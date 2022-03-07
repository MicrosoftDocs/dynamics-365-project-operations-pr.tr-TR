---
title: Gider yönetimi iş akışı
description: Bu konu, Microsoft Dynamics 365 Finance'ta iş akışı sistemini nasıl kullanabileceğinizi ve gider yönetiminde gider raporlarına yönelik bir gözden geçirme işlemi ayarlamanıza açıklanmaktadır.
author: ShylaThompson
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7c2a2cae435342139f32d1bb5d38d68acd920453f5e6f6551e1f6d57967d8053
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001320"
---
# <a name="expense-management-workflow"></a>Gider yönetimi iş akışı

İş akışı sistemini nasıl kullanabileceğinizi ve gider yönetiminde gider raporlarına yönelik bir gözden geçirme işlemi ayarlamanıza açıklanmaktadır. Gider raporlarını kimlerin onayladığına karar vermek için aşağıdaki ölçütleri kullanan bir iş akışı ayarlayabilirsiniz:

- Çalışan raporlama hiyerarşisi ve önceden tanımlanmış onay sınırları
- Geçici onaylayanları ve son onaylayanı destekleyen çok düzeyli onay
- Mali Boyutlar ve proje sorumluluğu
- Belirli kullanıcılar veya Kullanıcı gruplarına atama

Gider raporları, seyahat talepleri, nakit avanslar ve katma değerli vergi (KDV) kurtarması için iş akışı onayları oluşturulabilir.

**Örnek**

Aşağıdaki işlem, gider raporu için gider yönetimi iş akışına bir örnektir.

1. Bir çalışan bir gider raporu oluşturur ve kaydeder.
2. Çalışan, onay için gider raporu gönderir. Onaylayan, iş akışı ayarlanırken tanımlanan kurallara göre tanımlanır.
3. Onaylayan, bir gider raporunun onaya hazır olduğunu bildiren bir bildirim alır. Onaylayan, gider raporunu inceler ve aşağıdaki koşulların karşılandığını doğrular:

    - Giderler herhangi bir gider ilkesini ihlal etmeyin. Bir gider bir ilkeyi ihlal ederse, onaylayan, gider raporunun geçerli bir iş doğrulaması içerdiğini doğrular.
    - Elektronik girişler gider raporuna iliştirilir.

4. Onaylayan gider raporunu onaylar.
5. Gider raporu, deftere nakil için borç hesapları Koordinatörü 'ne atanır.
6. Otomatik nakil yapılandırılmış olup olmamasına bağlı olarak aşağıdaki adımlardan biri oluşur:

    - Otomatik nakil yapılandırılırsa, gider raporu ödeme için işlenir ve gider raporunun durumu güncelleştirilir.
    - Otomatik deftere nakil yapılandırılmazsa borç hesapları Düzenleyicisi tüm özgün makbuzların gönderildiğini ve makbuzların gider raporundaki giderlerle hizalandığını doğrular. Gider raporuna girilen tüm vergi kodlarının aynı zamanda doğru olarak doğrulanması gerekir.

Bu gereksinimler doğrulandıktan sonra, gider raporu deftere nakledilir.

Gider raporu deftere nakledildikten sonra, gider raporu için ödeme yetkilidir ve çalışana geri ödeme yapılır.


[!INCLUDE[footer-include](../includes/footer-banner.md)]