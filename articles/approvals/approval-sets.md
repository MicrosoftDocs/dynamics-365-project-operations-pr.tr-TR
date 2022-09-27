---
title: Onay kümeleri
description: Bu makalede, onay kümeleri, istekler ve bu operasyonların alt kümeleri ile nasıl çalışılacağı açıklanmaktadır.
author: stsporen
ms.date: 02/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: ca205073edbce2b399aab3ae273d635c8af96765
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524941"
---
# <a name="approval-sets"></a>Onay kümeleri

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Onay kümeleri, onaylama isteklerini işlemlerin daha küçük alt kümeleri olarak gruplandırır. Bu gruplandırma, onayların projeye göre belirli bir sırada işlenmesine ve yeniden denemeye ve sıralamaya olanak tanır. Onay isteklerinin bir arada gruplandırılması, büyük hacimli onaylar için onay işleminin güvenilirliğini ve izlenebilirliğini artırır.

Onay kümeleri, ilgili kayıtların genel işlenme durumunu belirtir. Onay kaydı bir onay kümesi kullanılarak işlendiğinde, kayıt **Gönderildi** durumundan **Onaylandı** durumuna geçer ve artık onay kümesiyle bağlantılı olmaz. Bir kayıt onaylanmak üzere gönderildiğinde başarısız olursa, kayıt **Gönderildi** durumunda kalır ve onay kümesi başarısız olarak işaretlenir. Onay kümesi, hatanın hata mesajını günlüğe kaydeder.

## <a name="processing-approvals-and-approval-sets"></a>Onayları ve onay kümelerini işleme
İşlenmek üzere kuyruğa alınmış onaylar, **İşlenen Onaylar** görünümünde görünür. Sistem tüm girişleri birden çok kez zaman uyumsuz olarak işler (önceki girişimler başarısız olursa bir onayı yeniden denemek dahil).

**Onay Kümesi Yaşam Süresi** alanı, başarısız olarak işaretlenmeden önce kümeyi işlemek için kalan deneme sayısını kaydeder.

Onay kümeleri **Project Service - Proje Onay Kümelerini Tekrar Tekrar Zamanla** olarak adlandırılan bir **Bulut Akışı**'na göre periyodik etkinleştirme aracılığıyla işlenir. Bu **Project Operations** olarak adlandırılan **Çözüm**'de bulunur. 

Aşağıdaki adımları tamamlayarak akışın etkinleştirildiğinden emin olun.

1. Yönetici olarak [flow.microsoft.com](https://powerautomate.microsoft.com) adresinde oturum açın.
2. Sağ üst köşede, Dynamics 365 Project Operations için kullandığınız ortama geçiş yapın.
3. Ortama yüklenen çözümleri listelemek için **Çözümler**'i seçin.
4. Çözüm listesinde **Project Operations**'ı seçin.
5. **Tümü** filtresini **Bulut Akışları** olarak değiştirin.
6. **Project Service - Proje Onay Kümelerini Tekrar Tekrar Zamanla** akışının **Açık** olarak ayarlandığını doğrulayın. Ayarlanmadıysa akışı seçin ve ardından **Aç** seçeneğini belirleyin.
7. Project Operations Dataverse ortamınızdaki **Ayarlar** alanında **Sistem İşleri** listesini inceleyerek işlemenin her beş dakikada bir gerçekleştiğini doğrulayın.

## <a name="failed-approvals-and-approval-sets"></a>Başarısız onaylar ve onay kümeleri
**Başarısız Onaylar** görünümü, kullanıcı müdahalesi gerektiren tüm onayları listeler. Başarısızlığın nedenini belirlemek için ilgili onay kümesi günlüklerini açın.
**Yeniden dene**'yi seçtiğinizde onay kümesi ömür sayısına ekleme yapılır, onay kümesi tekrar **İşleniyor** durumuna taşınır ve kalan kayıtları işlenmeye çalışılır.

## <a name="configure-approval-sets"></a>Onay kümelerini yapılandırma

### <a name="enable-the-approval-sets-feature"></a>Onay kümeleri özelliğini etkinleştirme
Onay kümeleri özelliğini etkinleştirmeden önce, işlenmekte olan onay olmadığını doğrulayın. Bu özellik etkinleştirildikten sonra, devre dışı bırakılamaz.

- **Proje parametreleri** sayfasına gidin ve **Özellik Kontrolü** > **Modern Onayları Etkinleştir** seçeneğini belirleyin.

### <a name="configuring-the-asynchronous-threshold"></a>Zaman uyumsuz eşiği yapılandırma 
Onay kümeleri oluşturulduğunda, onay için seçilen kayıt sayısı belirtilen eşiği aştığında, işlem arka plana gider. Onay işleminin zaman uyumlu mu zaman uyumsuz mu çalıştırılması gerektiğini belirlemek için **Zaman Uyumsuz Eşik** alanını kullanın. Aşağıdaki değerlerden birini seçin:

  - Sıfır: Tüm istekler zaman uyumsuz olarak işlenmelidir. 
  - Sıfırdan büyük sayılar: Onaylar, yalnızca gönderilen onay sayısı bu değeri aştığında zaman uyumsuz olarak işlenir.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
