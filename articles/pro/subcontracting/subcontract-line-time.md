---
title: Zaman için alt sözleşme satırları
description: Bu konu, zaman için alt sözleşme satırlarının nasıl kaydedileceğini ve satıcılardan satın alınan zamanın nasıl kaydedileceğini açıklar.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 10ebe0fcc86b4652ac01e28108361df1f768b61d
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323890"
---
# <a name="subcontract-lines-for-time"></a>Zaman için alt sözleşme satırları

[!include [banner](../../includes/dataverse-preview.md)]

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Dynamics 365 Project Operations'daki bir alt sözleşmede zaman için bir alt sözleşme satırı bulunabilir. Alt sözleşme zaman satırları, Proje Yöneticisinin proje görevlerine personel ve kaynak gereksinimleri sağlamak için satıcıdan kaynak zamanı satın almasına olanak tanır.

Project Operations'da zaman için bir alt sözleşme satırı oluşturmak üzere aşağıdaki adımları uygulayın.

1. Gezinti bölmesinde, **Alt sözleşmeler**'i seçin ve bir alt sözleşme açın.
2. **Alt Sözleşme Satırları** sekmesinde yeni bir alt sözleşme satırı oluşturmak için **Yeni**'yi seçin.
3. **Hızlı Oluştur** sayfasında, **İşlem Sınıfı** alanında **Zaman**'ı seçin.
4. Kalan gerekli bilgileri girin ve ardından **Kaydet**'i seçin.

  Aşağıdaki tabloda, **Alt sözleşme satırı** ve **Hızlı oluştur** sayfasındaki alanlarla ilgili bilgiler yer almaktadır.

| **Alan** | **Açıklama** |
| --- | --- |
| Adı | Alt sözleşme satırının adı. |
| Açıklama | Alt sözleşme satırında satın alınan hizmetlerle ilgili kısa bir açıklama. | 
| Hat Türü | Bu alan varsayılan değerdir.  |
| Faturalama Yöntemi | Faturalama yönetimini seçin. Başvurulan alt sözleşme satırının faturalama yöntemine dayalı olarak, Sabit Fiyatlı faturalama yöntemi için kilometre taşı tabanlı bir fatura zamanlaması kullanılabilir duruma gelir. |
| İşlem Sınıfı | Bu alan, alt yüklenici zamanını satın alma işlemini kaydetmek için alt sözleşme satırı kullanılıp kullanılmadığını gösteren bir varsayılan değerdir. |
| Rol | Zamanı satın alınan alt sözleşme kaynaklarının rolü. Alt sözleşme kaynaklarına atanan rol, satınalmanın maliyetini belirler. |
| İstenen Başlangıç | Alt yüklenici kaynaklarının çalışmaya başlayacağı tarih. İstenen tarih, alt sözleşmeye eklenen proje fiyat listelerinden bir proje fiyat listesi seçmek için de kullanılır. Alt sözleşme satırındaki rolün maliyeti daha sonra varsayılan olarak bu fiyat listesinden alınır. |
| İstenen Bitiş | Alt yüklenici kaynakları atamasının sona erdiği tarih. Bu tarih, Proje Yöneticisi bu tarihten sonra gerçekleşen kaynak gereksinimleri için bu kapasiteden çekim yaptığında uyarılar göstermek için kullanılır. |
| Sipariş Edilen Miktar | Satıcıdan satın alınan Rol saati sayısı. Bu değer, Proje Yöneticisi kaynak gereksinimleri için bu kapasiteden fazla çekim yaptığında uyarılar göstermek için kullanılır. |
| Birim Grubu | Bu alan değeri varsayılan olarak Zaman birimi grubunu kullanır ve değiştirilemez.  |
| Birim | Bu alan varsayılan olarak, Zaman birimi grubundaki temel saat birimini alır. Gün veya hafta gibi bir Zaman birimi grubu birimi satın almak için bu değeri değiştirebilirsiniz. Rol ve Birim birleşimi, alt sözleşme satırı için birim fiyatı hesaplamak üzere kullanılır. |
| Birim Fiyatı | Birim fiyatı varsayılan değeri, alt sözleşme satırının istenen bitiş tarihi için geçerli olan proje fiyat listesindeki Rol ve Birim birleşimi kullanılarak belirlenir. İlgili proje fiyat listesinde, alt sözleşme satırındaki birimden farklı bir birimde fiyat ayarlanmışsa sistem birim fiyatını hesaplamak için birim dönüşümünü kullanır. |
| Alt Toplam | Bu, hem miktar hem de birim fiyat değerleri girildiğinde otomatik olarak **Miktar x Birim fiyat** olarak hesaplanan salt okunur bir alandır. Miktar alanı, birim fiyat alanı veya her ikisi de boşsa, alana bir değer girebilirsiniz. |
| Satış Vergisi |  Satış vergisi tutarını girin. |
| Toplam Tutar | Vergiler dahil edildikten sonraki alt sözleşme satırı toplam tutarı. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
