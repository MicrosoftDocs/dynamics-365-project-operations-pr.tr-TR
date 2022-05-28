---
title: Önceden onaylanan girişleri geri çekme
description: Bu konu, proje ekibi üyelerinin önceden gönderilen ve onaylanmış zaman, masraf ve malzeme kullanımı kayıtlarını nasıl geri çekeceğini ve proje yöneticisinin geri çekme isteklerini nasıl onaylayacağını veya reddedeceğini açıklamaktadır.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 18796e803ff73806aaa60b453048ee3160406b40
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586598"
---
# <a name="recall-previously-approved-entries"></a>Önceden onaylanan girişleri geri çekme

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Zaman, gider veya malzeme kullanımı girişi yapan proje takımı üyeleri, bu girişi onaylandıktan sonra geri çekebilir. Geri çekme süreci iki ana adımdan oluşur:

1. Gönderen, geri çekme isteğinde bulunur.
2. Onaylayan, geri çekme isteğini onaylar.

## <a name="request-a-recall"></a>Geri çekme isteğinde bulunma

Onaylanan bir zaman veya malzeme kullanımı girişini geri çekmek için aşağıdaki adımları izleyin.

1. Geri çekmek istediğiniz girişin türüne bağlı olarak şu adımlardan birini izleyin:

    - Zaman girişlerinde **Projeler** \> **Çalışmam** \> **Zaman Girişi**'ne gidin ve belirli bir proje ve görev kombinasyonu için tüm zaman girişlerini seçin. Alternatif olarak, kılavuzdan belirli bir proje için belirli bir tarihte zamana ait hücreyi seçin.
    - Gider girişlerinde **Projeler** \> **Çalışmam** \> **Giderler**'e gidin ve geri çekilecek gider girişinin satırını seçin.
    - Malzeme kullanımı girişleri için **Projeler** \> **Çalışmam** \> **Malzeme Kullanım Günlüğü**'ne gidin ve geri çekilecek malzeme kullanımı girişinin satırını seçin.

2. **Geri çek**'i seçin. Bir onay iletişim kutusu görüntülenir. Seçilen zaman, gider ya da malzeme kullanımı girişleri önceden onaylandıysa geri çekme için bir neden girmeniz istenir.
3. Geri çekme için neden girin ve ardından işlemi onaylamak için **Tamam**'ı seçin. Sistem, girişleri onaylayan kişiye geri çekmeyi onaylaması için istek gönderir.

> [!IMPORTANT]
> Önceden onaylanarak müşteriye faturalandırılmış zaman, gider ve malzeme kullanımı girişleri için geri çekme isteği oluşturamazsınız. Geri çekme isteği oluşturmaya çalıştığınızda zaman, gider veya malzeme kullanımı girişinin çoktan faturalandığı için geri çekilemeyeceğini belirten bir ileti alırsınız. Bu durumda, yalnızca özgün faturada müşteriye tam kredi verilmesi veya iade yapılması için düzeltme faturası kullanıldıysa girişi geri çekme isteğinde bulunabilirsiniz.

## <a name="approve-or-reject-a-recall-request"></a>Geri çekme isteğini onaylama veya reddetme

Geri çekme isteğini onaylamak veya reddetmek için şu adımları izleyin.

1. **Projeler** \> **İşlerim** \> **Onaylar**'a gidin.
2. **Onaylar** listesi sayfasında, görünümü **Onay için İstekleri Geri Çek** olarak değiştirin. Gönderilen geri çekme isteklerinin listesi gösterilir.
3. Bir veya daha fazla giriş seçin ve ardından **Onayla** veya **Reddet** seçeneğini belirleyin.
4. **Onayla**'yı seçtiyseniz, onayın etkisini açıklayan bir uyarı iletisi alırsınız. İşlemi onaylamak için **Tamam**'ı seçin. Geri çekme isteği onaylanır.

    –veya–

    **Reddet**'i seçtiyseniz, geri çekme isteği reddedilir.

> [!IMPORTANT]
> Geri çekme, isteğinde olduğu gibi onaylandığında da sistem, zaman, gider veya malzeme kullanımı girişlerindeki faturalandırma etkinliğini denetler. Giriş zaten faturalanmışsa veya taslak fatura halindeyse onaylayan, faturalandırılmış olması nedeniyle zaman veya giderin geri çekme için onaylanamayacağını belirten bir hata iletisi alır. Bu durumda onaylayıcı, yalnızca özgün faturada müşteriye tam kredi verilmesi veya iade yapılması için düzeltme faturası kullanıldıysa geri çekmeyi onaylayabilir.

## <a name="impact-of-a-recall-request"></a>Geri çekme isteğinin etkisi

Geri çekilen onayların operasyonel ve finansal etkileri bulunur.

### <a name="operational-impact"></a>Operasyonel etki

Geri çekme isteği onaylandığında onay kaydı **Reddedildi** olarak işaretlenir. Girişin durumu; zaman, gider veya malzeme kullanımı girişi olmasına bağlı olarak **İade Edildi** veya **Reddedildi** olarak değiştirilir.

Proje takımı üyeleri, girişleri görüntüleyebilir, düzenleyebilir ve ardından yeniden gönderebilir veya girişleri tamamen silebilir.

Geri çekme isteği reddedilirse, girişin durumu **Onaylandı** olarak kalır ve giriş proje takımı üyesi veya projenin onaylayanı tarafından düzenlenemez.

### <a name="financial-impact"></a>Finansal etki

Geri çekme isteği onaylandığında maliyet ve satışlara karşılık gelen gerçek tutarlar aşağıdaki şekilde güncelleştirilir:

- **Düzeltme Durumu** alanı **Düzeltildi** olarak güncelleştirilir.
- **Faturalama Durumu** alanı **İptal Edildi** olarak güncelleştirilir.

Ardından, Gerçek değerler tablosunda ters işlem girişleri oluşturulur. Ters işlem girişleri oluşturmak için sistem özgün gerçek değerleri alan değerlerinin üzerine kopyalar. Kopyalanmayan tek değer miktar değerleridir. Bunun yerine bu değerler tersine çevrilir. **Maliyet** ve **Faturalanmamaış Satış** gerçek değerleri için tersine çevrilmiş gerçek değerler oluşturulur. Geri çevrilen gerçek tutarlardaki **Düzeltme Durumu** alanı **Düzeltilemez** olarak, **Faturalama durumu** alanı da **İptal Edildi** olarak ayarlanır. Bu değişiklikler nedeniyle, projedeki kaydedilmiş harcama ve gelir biriktirme listesi, bu gerçek tutarların temsil ettiği tutarları açıklamaz.

Geri çekme isteği reddedilirse, proje üzerinde finansal etkisi olmaz.

## <a name="changes-to-time-entry-records"></a>Zaman girişi kayıtlarında değişiklikler

Aşağıdaki çizim, geri çekildiklerinde onaylanan zaman girişlerinde ve bunlara karşılık gelen onay kayıtlarında gerçekleşen değişiklikleri gösterir.

![Zaman girişi durum geçişleri.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-and-material-usage-entry-records"></a>Gider ve malzeme kullanımı kayıtlarında değişiklikler

Aşağıdaki çizim, geri çekildiklerinde onaylanan gider ve malzeme kullanımı girişlerinde ve bunlara karşılık gelen onay kayıtlarında gerçekleşen değişiklikleri gösterir.

![Gider girişi durum geçişleri.](media/ExpenseEntryStateTransitions.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
