---
title: Zaman için alt sözleşme satırları
description: Bu konu, zaman için alt sözleşme satırlarının nasıl kaydedileceğini ve satıcılardan satın alınan zamanın nasıl kaydedileceğini açıklar.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c1adc1e88369e9f60548ed69b5950070d5f10c57
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595706"
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

| **Alan** | **Açıklama** | **İşlevsel etki** |
| --- | --- | --- |
| Adı | Tanımlamayla ile ilgili yardım için alt sözleşme satırının adı. | Bu, alt sözleşme satırlarına dayalı olarak tüm aramalarda ilk sütun olarak gösterilir. |
| Açıklama | Alt sözleşme satırında satın alınan hizmetlerle ilgili kısa bir açıklama. |Hiçbiri |
| Hat Türü |   Bu alan **Miktar tabanlı** varsayılan değerine sahiptir.| Hiçbiri |
| Faturalama Yöntemi | Bu, Project Operations tarafından desteklenen iki ana sözleşme modelini temsil eden bir seçenek kümesidir: **Sabit Fiyat** ve **Zaman ve Malzeme**. | Seçilen faturalama yöntemine göre, Sabit Fiyat faturalandırma yönteminin seçildiği alt sözleşme satırları için kilometre taşı tabanlı bir fatura zamanlaması sunulur. |
| İşlem Sınıfı | Varsayılan ad **Zaman** olur. | Bu, alt sözleşme satırının bir alt yüklenicinin zamanını satın almak için kullanıldığını gösterir. |
| Rol | Zamanı satın alınan alt sözleşme kaynaklarının rolünü seçin. | Alt sözleşme kaynakları tarafından gerçekleştirilen rol, satınalmanın maliyetini belirler. |
| İstenen Başlangıç | Alt yüklenici kaynaklarının çalışmaya başlayacağı tarihi girin. | Bu, alt sözleşmeye iliştirilen proje fiyat listelerinden bir proje fiyat listesi seçmek için kullanılır. Alt sözleşme satırındaki rolün maliyeti bu fiyat listesinden gelir. |
| İstenen Bitiş | Alt yüklenici kaynağı atamasının sona erdiği tarihi girin. | Bu, bir proje yöneticisi bu tarihten sonra oluşan kaynak gereksinimleri için kapasiteden çekim yaptığında uyarı göstermek için kullanılacaktır. |
| Sipariş Edilen Miktar | Satıcıdan satın alınan rol için saat sayısını girin. | Bu, bir proje yöneticisi kaynak gereksinimleri için bu kapasiteden fazla çekim yaptığında uyarı göstermek için kullanılacaktır. |
| Birim Grubu | Varsayılan değer **Zaman birimi grubu**'dur ve değiştirilemez. | Hiçbiri|
| Birim | Bu alan için varsayılan değer, **Zaman birimi grubundan** alınan saatlerin temel birimidir. Gün veya hafta gibi bir **Zaman birimi grubu** birimi satın almak için bu değeri değiştirebilirsiniz. | **Rol** ve **Birim** birleşimi varsayılan olarak kullanılır veya alt sözleşme satırının birim fiyatı için hesaplanır. |
| Birim Fiyatı | Varsayılan birim fiyat, alt sözleşme satırının **İstenen Başlangıç** tarihi için geçerli olan proje fiyat listesindeki **Rol** ve **Birim** birleşimini kullanır. | İlgili proje fiyat listesinde, alt sözleşme satırındaki birimden farklı bir birimde fiyat ayarlanmışsa sistem birim fiyatını hesaplamak için birim dönüşümünü kullanır. |
| Alt Toplam |    Bu, miktar ve birim fiyat değerleri girildiğinde, Miktar X Birim fiyat olarak hesaplanan salt okunur bir alandır. Miktar alanı, birim fiyat alanı veya her ikisi de boşsa, alana bir değer girebilirsiniz. | Hiçbiri|
| Satış Vergisi |   Satış vergisi tutarını girin. |Hiçbiri |
| Toplam Tutar | Alt sözleşme satırının vergiler dahil toplam tutarı. Bu alan, Ara toplam + Satış vergisi olarak hesaplanır.|Hiçbiri |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
