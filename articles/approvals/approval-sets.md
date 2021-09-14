---
title: Onay kümeleri
description: Bu konuda onay kümeleri, istekler ve bu işlemlerin alt kümeleri ile nasıl çalışılacağı açıklanmaktadır.
author: stsporen
manager: tfehr
ms.date: 08/10/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 1d9333033eb2b03966c6531d0fd6ad5b878acd93
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323260"
---
# <a name="approval-sets"></a>Onay kümeleri

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Onay kümeleri, onaylama isteklerini işlemlerin daha küçük alt kümeleri olarak gruplandırır. Bu gruplandırma, onayların projeye göre belirli bir sırada işlenmesine ve yeniden denemeye ve sıralamaya olanak tanır. Onay isteklerinin bir arada gruplandırılması, büyük hacimli onaylar için onay işleminin güvenilirliğini ve izlenebilirliğini artırır.

Onay kümeleri, ilgili kayıtların genel işlenme durumunu belirtir. Onay kaydı bir onay kümesi kullanılarak işlendiğinde, kayıt **Gönderildi** durumundan **Onaylandı** durumuna geçer ve artık onay kümesiyle bağlantılı olmaz. Bir kayıt onaylanmak üzere gönderildiğinde başarısız olursa, kayıt **Gönderildi** durumunda kalır ve onay kümesi başarısız olarak işaretlenir. Onay kümesi, hatanın hata mesajını günlüğe kaydeder.

## <a name="processing-approvals-and-approval-sets"></a>Onayları ve onay kümelerini işleme
İşlenmek üzere kuyruğa alınmış onaylar, **İşlenen Onaylar** görünümünde görünür. Sistem tüm girişleri birden çok kez zaman uyumsuz olarak işler (önceki girişimler başarısız olursa bir onayı yeniden denemek dahil).

**Onay Kümesi Yaşam Süresi** alanı, başarısız olarak işaretlenmeden önce kümeyi işlemek için kalan deneme sayısını kaydeder.

## <a name="failed-approvals-and-approval-sets"></a>Başarısız onaylar ve onay kümeleri
**Başarısız Onaylar** görünümü, kullanıcı müdahalesi gerektiren tüm onayları listeler. Başarısızlığın nedenini belirlemek için ilgili onay kümesi günlüklerini açın.
**Yeniden dene**'yi seçtiğinizde onay kümesi ömür sayısına ekleme yapılır, onay kümesi tekrar **İşleniyor** durumuna taşınır ve kalan kayıtları işlenmeye çalışılır.

## <a name="configure-approval-sets"></a>Onay kümelerini yapılandırma

### <a name="enable-the-approval-sets-feature"></a>Onay kümeleri özelliğini etkinleştirme
Onay kümeleri özelliğini etkinleştirmeden önce, işlenmekte olan onay olmadığını doğrulayın.

- **Proje parametreleri** sayfasına gidin ve **Özellik Kontrolü** > **Modern Onayları Etkinleştir** seçeneğini belirleyin.

### <a name="turn-off-the-approval-sets-feature"></a>Onay kümeleri özelliğini devre dışı bırakma
Onay kümeleri özelliğini devre dışı bırakmadan önce, işlenmekte olan onay olmadığını doğrulayın.

- **Proje Parametreleri** sayfasına gidin ve **Özellik Kontrolü** > **Modern Onayları Devre Dışı Bırak** seçeneğini belirleyin.

### <a name="configuring-the-asynchronous-threshold"></a>Zaman uyumsuz eşiği yapılandırma 
Onay kümeleri oluşturulduğunda, onay için seçilen kayıt sayısı belirtilen eşiği aştığında, işlem arka plana gider. Onay işleminin zaman uyumlu mu zaman uyumsuz mu çalıştırılması gerektiğini belirlemek için **Zaman Uyumsuz Eşik** alanını kullanın. Aşağıdaki değerlerden birini seçin:

  - Sıfır: Tüm istekler zaman uyumsuz olarak işlenmelidir. 
  - Sıfırdan büyük sayılar: Onaylar, yalnızca gönderilen onay sayısı bu değeri aştığında zaman uyumsuz olarak işlenir.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
