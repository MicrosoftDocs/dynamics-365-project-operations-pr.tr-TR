---
title: Gider kategorileri için alt sözleşme satırları
description: Bu makalede, nasıl masraf için taşeron satırlarının kaydı yapılacağı açıklanmakta ve alanları satıcılardan satın alma süresini kaydetmek için nasıl kullanacağınız açıklanmaktadır.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7166642abc2187a53f7019639df6f0d7124f4765
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261865"
---
#  <a name="subcontract-lines-for-expense-categories"></a>Gider kategorileri için alt sözleşme satırları

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Dynamics 365 Project Operations'daki bir alt sözleşmede gider kategorileri için bir satır bulunabilir. Gider kategorilerine ilişkin alt sözleşme satırları Proje Yöneticisinin, satıcılardan bir projede ücretlendirebileceği hizmet veya ürün kategorileri satın almasına olanak tanır.

Project Operations'da gider kategorileri için bir alt sözleşme satırı oluşturmak üzere aşağıdaki adımları uygulayın.

1. Gezinti bölmesinde, **Alt sözleşmeler**'i seçin ve çalışmak istediğiniz bir alt sözleşmeyi açın.
2. **Alt Sözleşme Satırları** sekmesinde yeni bir satır oluşturmak için **+ Yeni**'yi seçin.
3. **Hızlı Oluştur** sayfasında, **İşlem Sınıfı** alanında, **Gider**'i seçin ve gerekli diğer alan bilgilerini girin veya seçin.

Aşağıdaki tabloda, **Alt sözleşme satırı** ayrıntıları ve **Hızlı oluştur** sayfasındaki alanlarla ilgili bilgiler yer almaktadır.

| **Alan** | **Açıklama** | **İşlevsel etki** |
| --- | --- | --- |
| Adı | Tanımlamayla ile ilgili yardım için alt sözleşme satırının adı. | Bu, alt sözleşme satırlarına dayalı olarak tüm aramalarda ilk sütun olarak gösterilir. |
| Açıklama | Alt sözleşme satırında satın alınan gider kategorilerinin kısa bir açıklaması. | Hiçbiri |
|Hat Türü | Bu alan **Miktar tabanlı** varsayılan değerine sahiptir. |Hiçbiri |
| Faturalama Yöntemi | Bu, Project Operations tarafından desteklenen iki ana sözleşme modelini temsil eden bir seçenek kümesidir: **Sabit Fiyat** ve **Zaman ve Malzeme**. | Sabit Fiyat faturalandırma yöntemi seçilirse alt sözleşme satırları için kilometre taşı tabanlı bir fatura zamanlaması sunulur. |
| İşlem Sınıfı | Bu alan **Zaman** varsayılan değerine sahiptir. Ürün satın alma için alt sözleşme satırları oluşturmak üzere **İşlem sınıfı** alanını **Gider** olarak ayarlayın.  | Bu, bir alt sözleşme satırının, projelerde kullanılacak bir gider kategorisi satın alımını kaydetmek için kullanıldığını gösterir. |
| İşlem Kategorisi | Sistemdeki etkin işlem kategorilerinin bir listesini gösterir. |Hiçbiri |
| İstenen Başlangıç | Satınalma kategorilerinin satıcıdan kullanılabilir duruma gelmesi gereken tarihi girin. | İstenen başlangıç, alt sözleşmeye iliştirilen proje fiyat listelerinden bir proje fiyat listesi seçmek için kullanılır. Alt sözleşme satırındaki kategorinin maliyeti bu fiyat listesinden gelir. |
| İstenen Bitiş | Satınalma kategorilerinin artık gerekli olmayacağı tarihi girin. | Bu, bir proje yöneticisi bu alt sözleşme satırını bu tarihten sonra gerekli olan projedeki belirli gider tahminleriyle ilişkilendirdiğinde uyarı göstermek için kullanılacaktır. |
| Sipariş Edilen Miktar | Satıcıdan satın alınan kategorinin miktarı. | Bu, bir proje yöneticisi bu miktardan daha fazlasını çektiğinde uyarı göstermek için kullanılacaktır.|
| Birim Grubu | Varsayılan değer, seçili kategori için ayarlanan varsayılan birim grubuna göre belirlenir. |Hiçbiri |
| Birim | Varsayılan değer, seçili kategori için ayarlanan varsayılan birim ayarına göre belirlenir.  | **Kategori** ve **Birim** birleşimi varsayılan olarak kullanılır veya alt sözleşme satırının birim fiyatı için hesaplanır.  |
| Birim Fiyatı | Varsayılan değer, alt sözleşme satırının istenen başlangıcı için geçerli olan proje fiyat listesiyle ilgili kategori fiyatlarındaki **Kategori** ve **Birim** birleşimini kullanır. |Hiçbiri |
| Alt Toplam | Bu, miktar ve birim fiyat değerleri girildiğinde, Miktar X Birim fiyat olarak hesaplanan salt okunur bir alandır. Alanlardan biri veya her ikisi de boşsa, bu alana bir değer girebilirsiniz. |Hiçbiri |
| Satış Vergisi | Satış vergisi tutarını girin. |Hiçbiri |
| Toplam Tutar | Alt sözleşme satırının vergiler dahil toplam tutarı. Bu alan, Ara toplam + Satış vergisi olarak hesaplanır. |Hiçbiri |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
