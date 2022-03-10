---
title: Project Service Automation'daki onay kümeleri
description: Bu konu; onay kümesi, istekler ve bu işlemlerin alt kümeleri hakkında bilgi sağlar.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 9a7a9efbd8615f4923c6795a16c9cf98a40362b6
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323575"
---
# <a name="approval-sets-in-project-service-automation"></a>Project Service Automation'daki onay kümeleri

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Onay kümeleri, onaylama isteklerini işlemlerin daha küçük alt kümeleri olarak gruplandırır. Bu gruplandırma, onayların Projeye göre sıralı işlenmesine ve yeniden deneme ve sıralama yapılmasına olanak tanır. Gruplandırma, büyük miktarda onaylama için onay işlemenin güvenilirliğini ve izlenebilirliğini artırır.

Onay kümeleri, ilgili kayıtların genel işlenme durumunu belirtir. Onay kaydı bir onay kümesi kullanılarak işlendiğinde, kayıt **Gönderildi** durumundan **Onaylandı** durumuna taşınır ve onay kümesiyle bağlantısı kaldırılır. Bir kayıt onaylanmak üzere gönderildiğinde başarısız olursa, kayıt **Gönderildi** durumunda kalır ve onay kümesi başarısız olarak işaretlenir. Onay kümesi, hatanın hata mesajını günlüğe kaydeder.

## <a name="processing-approvals-and-approval-sets"></a>Onayları ve onay kümelerini işleme
İşlenmek üzere kuyruğa alınmış onaylar, **İşlenen Onaylar** görünümünde görünür. Sistem, önceki denemeler başarısız olduysa bir onayı yeniden denemek de dahil olmak üzere, tüm girişleri birçok defa zaman uyumsuz olarak işlemeye çalışır.

**Onay Kümesi Yaşam Süresi** alanı, başarısız olarak işaretlenmeden önce kümeyi işlemek için kalan deneme sayısını kaydeder.

## <a name="failed-approvals-and-approval-sets"></a>Başarısız onaylar ve onay kümeleri
**Başarısız Onaylar** görünümü, kullanıcı müdahalesi gerektiren tüm onayları listeler. Başarısızlığın nedenini belirlemek için ilgili onay kümesi günlüklerini açın.
**Yeniden dene**'yi seçtiğinizde onay kümesi ömür sayısına ekleme yapılır, onay kümesi tekrar **İşleniyor** durumuna taşınır ve kalan kayıtları işlenmeye çalışılır.

## <a name="configure-approval-sets"></a>Onay kümelerini yapılandırma

###  <a name="enable-the-approval-sets-feature"></a>Onay kümeleri özelliğini etkinleştirme
Onay kümeleri özelliğini etkinleştirmeden önce, işlenmekte olan onay olmadığını doğrulayın.

- **Proje parametreleri** sayfasına gidin ve **Özellik Kontrolü** > **Modern Onayları Etkinleştir** seçeneğini belirleyin.

### <a name="turn-off-the-approval-sets-feature"></a>Onay kümeleri özelliğini devre dışı bırakma
Onay kümeleri özelliğini devre dışı bırakmadan önce, işlenmekte olan onay olmadığını doğrulayın.

- **Proje Parametreleri** sayfasına gidin ve **Özellik Kontrolü** > **Modern Onayları Devre Dışı Bırak** seçeneğini belirleyin.

### <a name="configuring-the-asynchronous-threshold"></a>Zaman uyumsuz eşiği yapılandırma 
Onay kümeleri oluşturulduğunda, onay için seçilen kayıt sayısı belirtilen eşiği aştığında, işlem arka plana gider. Onay işleminin zaman uyumlu mu zaman uyumsuz mu çalıştırılması gerektiğini belirlemek için **Zaman Uyumsuz Eşik** alanını kullanın.
Geçerli değerler:

  - Sıfır: Tüm istekler zaman uyumsuz olarak işlenmelidir. 
  - Sıfırdan büyük sayılar: Onaylar, yalnızca gönderilen onay sayısı bu değeri aştığında zaman uyumsuz olarak işlenir.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
