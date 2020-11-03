---
title: Onaylanan zaman veya gider girişlerini geri çekme
description: Bu konu, önceden onaylanmış bir zaman veya gider hareketini geri çekme hakkında bilgi sağlar.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 7bacd70881a6c463cc449a365173da5338a3d3fc
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086371"
---
# <a name="recall-approved-time-or-expense-entries"></a>Onaylanan zaman veya gider girişlerini geri çekme

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Zaman veya gider girişi yapan bir proje takımı üyesi veya başka bir kişi bu zaman ya da gider girişini onaylandıktan sonra geri çekebilir. Onaylanmış bir zaman veya gider girişini geri çekme işleminin iki adımı vardır:

1. Gönderen bir geri çekme isteğinde bulunur.
2. Onaylayan geri çekme işlemini onaylar.

## <a name="request-a-recall"></a>Geri çekme isteğinde bulunma

Onaylanan bir zaman veya gider girişini geri çekmek için aşağıdaki adımları izleyin.

1. Zaman girişleri için, **Projeler** \> **Çalışmam** \> **Zaman Girişi** öğesine gidin.

    –veya–

    Gider girişleri için, **Projeler** \> **Çalışmam** \> **Giderler** öğesine gidin.

2. Zaman girişlerinde, bir projenin ve bir görevin belirli bir birleşimiyle ilgili tüm zaman girişlerini seçin. Alternatif olarak, ızgaradan belirli bir proje için belirli bir tarihte zamana ait hücreyi seçin.

    –veya–

    Gider girişleri için, geri çekmek istediğiniz gider girişinin satırını seçin.

3. **Geri çek** 'i seçin. Bir onay iletişim kutusu görüntülenir. Seçilen zaman ve gider girişleri önceden onaylandıysa, geri çekme için bir neden girmeniz istenir.
4. Geri çekme için bir neden girin ve ardından işlemi onaylamak için **Tamam** 'ı seçin. Sistem, girişleri onaylayan kişiye geri çekmeyi onaylaması için bir istek gönderir.

> [!NOTE]
> Onaylanan zaman ve gider girişleri geri çekilebilse de onaylanan bir zaman veya gider müşteriye zaten faturalanmışsa, geri çekme isteği oluşturulamaz. Geri çekme isteği oluşturmaya çalışan bir kullanıcı, zaman veya giderin zaten faturalandığı için geri çekilemeyeceğini belirten bir ileti alır.

## <a name="approve-or-reject-a-recall-request"></a>Geri çekme isteğini onaylama veya reddetme

Geri çekme isteğini onaylamak veya reddetmek için şu adımları izleyin.

1. **Projeler** \> **İşlerim** \> **Onaylar** 'a gidin.
2. **Onaylar** listesi sayfasında, görünümü **Onay için İstekleri Geri Çek** olarak değiştirin. Gönderilen geri çekme isteklerinin listesi gösterilir.
3. Bir veya daha fazla giriş seçin ve ardından **Onayla** veya **Reddet** seçeneğini belirleyin.
4. **Onayla** 'yı seçtiyseniz, onayın etkisini açıklayan bir uyarı iletisi alırsınız. İşlemi onaylamak için **Tamam** 'ı seçin. Geri çekme isteği onaylanır.

    –veya–

    **Reddet** 'i seçtiyseniz, geri çekme isteği reddedilir.

> [!NOTE]
> Bir geri çekme isteğinde olduğu gibi geri çekme onaylandığında da sistem zaman veya gider girişlerindeki faturalama etkinliğini denetler. Giriş zaten faturalanmışsa veya bir taslak faturadaysa, onaylayan giriş zaten faturalandırıldığından zaman veya gider girişini geri çekme isteğinin onaylanamayacağını belirten bir hata iletisi alır.

## <a name="impact-of-a-recall-request"></a>Geri çekme isteğinin etkisi

Bir onay geri çekildiğinde işlemsel ve finansal bir etkisi olur.

### <a name="operational-impact"></a>İşlemsel etki

Bir geri çekme isteği onaylanırsa, onay kaydı **Reddedildi** olarak işaretlenir. Girişin durumu, bir zaman girişi veya gider girişi olmasına bağlı olarak **İade Edildi** veya **Reddedildi** olarak değiştirilir.

Proje takımı üyesi girişleri görüntüleyebilir, düzenleyebilir ve ardından yeniden gönderebilir veya girişleri tamamen silebilir.

Geri çekme isteği reddedilirse, girişin durumu **Onaylandı** olarak kalır ve giriş proje takımı üyesi veya projenin onaylayanı tarafından düzenlenemez.

### <a name="financial-impact"></a>Finansal etki

Bir geri çekme isteği onaylanırsa maliyet ve satışlar için karşılık gelen gerçek tutarlar aşağıdaki şekilde güncelleştirilir:

- **Düzeltme Durumu** alanı **Düzeltildi** olarak güncelleştirilir.
- **Faturalama Durumu** alanı **İptal Edildi** olarak güncelleştirilir.

Ardından, Fiili değerler tablosunda ters işlem girişleri oluşturulur. Ters işlem girişleri oluşturmak için sistem özgün fiili değerleri alan değerlerinin üzerine kopyalar. Kopyalanmayan tek değer miktar değerleridir. Bunun yerine bu değerler tersine çevrilir. **Maliyet** ve **Faturalanmamaış Satış** fiili değerleri için tersine çevrilmiş fiili değerler oluşturulur. Geri çevrilen gerçek tutarlardaki **Düzeltme Durumu** alanı **Düzeltilemez** olarak, **Faturalama durumu** alanı da **İptal Edildi** olarak ayarlanır. Bu değişiklikler nedeniyle, projedeki kaydedilmiş harcama ve gelir biriktirme listesi, bu gerçek tutarların temsil ettiği tutarları açıklamaz.

Geri çekme isteği reddedilirse, proje üzerinde finansal etkisi olmaz.

## <a name="changes-to-time-entry-records"></a>Zaman girişi kayıtlarında değişiklikler

Aşağıdaki çizim, geri çekildiklerinde onaylanan zaman girişlerinde gerçekleşen değişiklikleri gösterir.

![Zaman Girişi durum geçişleri](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a>Gider girişi kayıtlarında değişiklikler

Aşağıdaki çizim, geri çekildiklerinde onaylanan gider girişlerinde gerçekleşen değişiklikleri gösterir.

![Gider Girişi durum geçişleri](media/ExpenseEntryStateTransitions.png)
