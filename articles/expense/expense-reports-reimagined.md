---
title: Gider raporlarını yeniden tasarlama
description: Bu konuda, gider raporu girişi için yeniden tasarlanan ve düşünülen deneyim açıklanmaktadır.
author: suvaidya
ms.date: 03/26/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 76073d5c58398b2c296fdca05ba7bdf7f01951bb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995375"
---
# <a name="expense-reports-reimagined"></a>Gider raporlarını yeniden tasarlama

Gider raporu girişi, işlemi basitleştirmek ve raporu tamamlamak için gereken süreyi azaltmak üzere yeniden tasarlanmıştır. Yeni gider deneyiminin önemli bileşenleri şunlardır:

- Temsilcinin giderlerine erişmenize olanak tanıyan yeni gider yönetimi çalışma alanı.
- Başlık düzeyinde makbuzları daha iyi göstermek ve gider satırlarına makbuz ekleme işlemini basitleştirmek için yeni makbuz eşleştirme deneyimi.
- Daha fazla gider satırı ve ek veri sütunu görüntülemenize olanak tanıyan yeni bir salt okunur ızgara. Artık tüm dökümü alınmış ve bölünmüş satırları ana giderleriyle birlikte görebilirsiniz.
- Düzenleme giderleri için basitleştirilmiş bir bölme.
- Sorun ve nasıl çözümleneceği ile ilgili doğru bağlamı ve anlayışı sağlamak için yeniden tasarlanmış hata, uyarı ve ilke iletileri. Kullanıcıların görevlerini tamamlayabilmeleri ve sorunları giderebilmeleri için görüntülenen iletilerden birkaçını kaldırdık.
- Gerekli alanları, isteğe bağlı alanları ve dahil edilmemesi gereken alanları belirtmek için yeni bir sayfa. Bu sayfa, ayarlanması gereken alanların sayısını azaltmaya yardımcı olur.
- Tüm gider raporları için yeni bir görünüm. Böylece raporlar artık muhasebe çalışanları için tasarlanmış gibi görünmez.

Yeni deneyimi başlatmak için **Özellik yönetimi** çalışma alanını kullanarak **Gider raporlarını yeniden tasarlama** özelliğini açın. Bu özelliği açtığınızda aşağıdaki eylemler gerçekleşir:

- Var olan gider yönetimi çalışma alanı yeni çalışma alanıyla değiştirilir.
- Gider alanı görünürlüğü için yeni bir menü öğesi eklenir.
- Gider raporları için mevcut menü öğeleri (mevcut sayfa) olmaz veya gider raporu alanları kaldırılır.
- İş akışları ve onaylar sizi var olan gider raporları sayfasına götürür.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4IQFM]

## <a name="new-features"></a>Yeni özellikler

| Yeni özellik | Açıklama |
|---|----|
| Gider alanı görünürlüğü | Yeni kurulum sayfası, bir kuruluş için hangi alanların devre dışı bırakılması gerektiğini, hangi alanların gerekli olduğunu ve hangi alanların önerildiğini belirtmenize olanak tanır. |
| Gerekli alanlar | Yeni basit yapılandırma, ilke çerçevesini kullanmak zorunda kalmadan bazı alanları gerekli kılmanıza olanak tanır. |
| İsteğe bağlı alanlar | İsteğe bağlı alanlar için ikinci bir sayfa eklenir. Bu şekilde, çalışanlar alanları ayarlamak zorunda olduklarını hissetmez ancak alanlara yine de kolayca erişilebilir. |
| İliştirilmemiş makbuzları ekleme | İliştirilmemiş makbuzları gider raporuna ekleme özelliği, çalışma alanından ve gider raporunda daha fazla görünürdür. |
| İyileştirilmiş iletiler | Uyarılar veya hatalar olan gider satırlarının görünürlüğü daha iyidir. |
| İleti çubuğundaki iletilerde azalma| Bilgi günlüğü iletilerinin sayısı azaltılmıştır ve birçok durumda yinelenen iletilerin görünmesini engellemek için çalışma yapılmıştır. |
| Birlikte gruplanan ortak eylemler | Arabirim, ortak satır düzeyinde eylemlerin çoğu için yeni bir eylemler düğmesinin eklenmesi ve başlık ve diğer az kullanılan eylemler için üç nokta düğmesinin (...) eklenmesi ile temizlenmiştir. |
| Görünürlüğü artırmak için yeni çalışma alanı | Yeni bir çalışma alanı, kullanıcıların farklı alanlara geçmesine olanak tanıyan özellikleri ve bağlantıları birleştirir. |
| Gider oluşturma sırasında mevcut giderleri ve makbuzları ekleme | Gider raporları oluşturduğunuzda tüm giderleri ekleyebilir veya eklenmemiş giderleri seçebilirsiniz. Eklenmemiş giderler, kurumsal kredi kartı akışından içeri aktarılan giderler veya kullanıcı tarafından el ile oluşturulan ancak bir gider raporuna eklenmemiş giderlerdir.|
| Döviz kuru hesap makinesi | Cepten yapılan birden fazla para birimli işlemler için döviz kurunu hesaplamanıza olanak tanıyan bir döviz kuru hesap makinesi. |
| Yeni gider satırları kaydetme ve ekleme | Gider satırlarını hızlıca girmenize yardımcı olmak için yeni giderleri girerken **Kaydet** ve **Yeni** düğmelerini kullanabilirsiniz. |
| Bölünmüş ve dökümü alınmış satırlar için daha iyi görünürlük | Dökümü alınmış ve bölünmüş satırlar, görünürlüğü artırmak ve hata olup olmadığını kolayca belirlemenize yardımcı olmak için doğrudan gider listesine eklenir. |
| Döküm sırasında makbuzları gösterme | Makbuzlar döküm sırasında gösterilebilir. |
| Nakit avans seçimi | Tek bir gider işlemini karşılamak için bir veya daha fazla nakit avans seçin. |
| Nakit avans bakiyesi | Onaylanan ve ödenen nakit avanslara karşı bir gider girişi oluşturduğunuzda nakit avans bakiyesini gerçek zamanlı olarak inceleyin. |

Gider girişi senaryolarında ilk sürüme odaklanılır. Gider raporu inceleme veya onay senaryolarında, mevcut gider girişi sayfası kullanılmaya devam eder.

Yeniden Tasarlanan Gider Çalışma Alanı'nda aşağıdaki özellikler desteklenmez:

- Seyahat talebi tümleştirmesi
- Harcırah gider girişi
- Geçici onaylayan desteği
- İş akışı geçmişini görüntüleme özelliği


[!INCLUDE[footer-include](../includes/footer-banner.md)]
