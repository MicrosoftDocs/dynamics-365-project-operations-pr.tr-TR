---
title: Gider raporlarını yeniden tasarlama
description: Bu konuda, gider raporu girişi için yeniden tasarlanan ve yeniden düşünülen deneyim hakkında bilgiler sağlanmaktadır.
author: suvaidya
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 18d7407681906361f3f818225efb8510ac981d98
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122832"
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

## <a name="getting-started-video-for-new-users"></a>Yeni kullanıcılar için başlarken videosu

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE2Y7gO]

[Dynamics 365 for Finance and Operations'ta gider deneyimi](https://youtu.be/Ocy-MsTvEE0) videosu (yukarıda gösterilmektedir) YouTube'da mevcut olan [Finance and Operations çalma listesine](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) dahil edilmiştir.

## <a name="new-features"></a>Yeni özellikler

| Yeni özellik | Veri Akışı Açıklaması |
|---|----|
| Gider alanı görünürlüğü | Yeni kurulum sayfası, bir kuruluş için hangi alanların devre dışı bırakılması gerektiğini, hangi alanların gerekli olduğunu ve hangi alanların önerildiğini belirtmenize olanak tanır. |
| Gerekli alanlar | Yeni basit yapılandırma, ilke çerçevesini kullanmak zorunda kalmadan bazı alanları gerekli kılmanıza olanak tanır. |
| İsteğe bağlı alanlar | İsteğe bağlı alanlar için ikinci bir sayfa eklenir. Bu şekilde, çalışanlar alanları ayarlamak zorunda olduklarını hissetmez ancak alanlara yine de kolayca erişilebilir. |
| İliştirilmemiş makbuzları ekleme | İliştirilmemiş makbuzları gider raporuna ekleme özelliği, çalışma alanından ve gider raporunda daha fazla görünürdür. |
| İyileştirilmiş iletiler | Uyarılar veya hatalar olan gider satırlarının görünürlüğü daha iyidir. |
| İleti çubuğundaki iletilerde azalma| Bilgi günlüğü iletilerinin sayısı azaltılmıştır ve birçok durumda yinelenen iletilerin görünmesini engellemek için çalışma yapılmıştır. |
| Birlikte gruplanan ortak eylemler | Arabirim, ortak satır düzeyinde eylemlerin çoğu için yeni bir eylemler düğmesinin eklenmesi ve başlık ve diğer az kullanılan eylemler için üç nokta düğmesinin (...) eklenmesi ile temizlenmiştir. |
| Görünürlüğü artırmak için yeni çalışma alanı | Yeni bir çalışma alanı, kullanıcıların farklı alanlara geçmesine olanak tanıyan özellikleri ve bağlantıları birleştirir. |
| Gider oluşturma sırasında mevcut giderleri ve makbuzları ekleme | Gider raporları oluştururken giderlerin ve makbuzların tümünü veya içlerinden seçtiklerinizi ekleyebilirsiniz. |
| Döviz kuru hesap makinesi | Cepten yapılan birden fazla para birimli işlemler için döviz kurunu hesaplamanıza olanak tanıyan bir döviz kuru hesap makinesi. |
| Yeni gider satırları kaydetme ve ekleme | Gider satırlarını hızlıca girmenize yardımcı olmak için yeni giderleri girerken **Kaydet** ve **Yeni** düğmelerini kullanabilirsiniz. |
| Bölünmüş ve dökümü alınmış satırlar için daha iyi görünürlük | Dökümü alınmış ve bölünmüş satırlar, görünürlüğü artırmak ve hata olup olmadığını kolayca belirlemenize yardımcı olmak için doğrudan gider listesine eklenir. |
| Döküm sırasında makbuzları gösterme | Makbuzlar döküm sırasında gösterilebilir. |

Gider girişi senaryolarında ilk sürüme odaklanılır. Gider raporu inceleme veya onay senaryolarında, mevcut gider girişi sayfası kullanılmaya devam eder.

Aşağıdaki özellikler mevcut sayfada bulunur ancak henüz yeni sayfada yoktur. Bu özellikler sonraki birkaç sürümde yeniden sunulacaktır:

- Onaylar
- Borç hesabı onayları ve muhasebeyi düzenleme özelliği
- Birden çok giriş noktası
- Seyahat talebi tümleştirmesi
- Gider alanı görünürlüğü için veri varlığı
- Harcırah giderleri girişi
- Satır düzeyi iş akışı
- Geçici onaylayan desteği
- Gelişmiş döküm
