---
title: Gider kategorileri için alt sözleşme satırları
description: Bu konu, gider için alt sözleşme satırlarının nasıl kaydedileceğini ve satıcılardan yapılan zaman satın alımları kaydetmek için alanların nasıl kullanacağını açıklar.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9e8e7bb66063dab6db1ac8da1753913aee0ef3fc
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323845"
---
#  <a name="subcontract-lines-for-expense-categories"></a>Gider kategorileri için alt sözleşme satırları

[!include [banner](../../includes/dataverse-preview.md)]

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Dynamics 365 Project Operations'daki bir alt sözleşmede gider kategorileri için bir satır bulunabilir. Gider kategorilerine ilişkin alt sözleşme satırları Proje Yöneticisinin, satıcılardan bir projede ücretlendirebileceği hizmet veya ürün kategorileri satın almasına olanak tanır.

Project Operations'da gider kategorileri için bir alt sözleşme satırı oluşturmak üzere aşağıdaki adımları uygulayın.

1. Gezinti bölmesinde, **Alt sözleşmeler**'i seçin ve çalışmak istediğiniz bir alt sözleşmeyi açın.
2. **Alt Sözleşme Satırları** sekmesinde yeni bir satır oluşturmak için **+ Yeni**'yi seçin.
3. **Hızlı Oluştur** sayfasında, **İşlem Sınıfı** alanında, **Gider**'i seçin ve gerekli diğer alan bilgilerini girin veya seçin.

Aşağıdaki tabloda, **Alt sözleşme satırı** ayrıntıları ve **Hızlı oluştur** sayfasındaki alanlarla ilgili bilgiler yer almaktadır.

| **Alan** |  **Açıklama** |
| ----------| ---------------- |
| Adı | Alt sözleşme satırının adı. |
| Açıklama | Alt sözleşme satırındaki satın alınan hizmet ve ürün kategorileriyle ilgili kısa bir açıklama. |
| Hat Türü | Bu alan **Miktar tabanlı** varsayılan değerine sahiptir.  |
| Faturalama Yöntemi | Alt sözleşme satırının faturalama yöntemi. Satırın faturalama yöntemine dayalı olarak, sabit fiyatlı faturalama yöntemi için kilometre taşı tabanlı bir fatura zamanlaması bulunur.  |
| İşlem Sınıfı | Bu alan **Zaman** varsayılan değerine sahiptir. Ürün satın alma için alt sözleşme satırları oluşturmak üzere **İşlem sınıfı** alanını **Gider** olarak ayarlayın. Bu sabit değer, alt sözleşme satırının projelerde kullanılacak ürün veya hizmet kategorisi satın alımını kaydetmek için kullanıldığını gösterir. |
| İşlem Kategorisi | İşlem kategorisini seçin. |
| İstenen Başlangıç | Satınalma kategorilerinin satıcıda kullanılabilir durumda olması gereken tarih. İstenen tarih, alt sözleşmeye eklenen proje fiyat listelerinden bir proje fiyat listesi seçmek için de kullanılır. Alt sözleşme satırındaki kategorinin maliyeti varsayılan olarak bu fiyat listesinden alınır. |
| İstenen Bitiş | Satınalma kategorilerinin artık gerekli olmadığı tarih. Bu tarih, Proje Yöneticisi bu alt sözleşme satırını bu tarihten sonraki tarihte olan projelerdeki belirli gider tahminleriyle ilişkilendirdiğinde bir uyarı getirir. |
| Sipariş Edilen Miktar | Satıcıdan satın alınan kategori miktarı. Proje yöneticisi satın alınan miktardan fazlasını çekerse bir uyarı oluşur.  |
| Birim Grubu | Bu alan değeri varsayılanı, seçili kategori için ayarlanan varsayılan birim grubuna göre ayarlanır. |
| Birim | Bu alan değeri varsayılanı, seçili kategori için ayarlanan varsayılan birime göre ayarlanır. Kategori ve birim birleşimi, alt sözleşme satırındaki birim fiyatı varsayılan olarak kullanır. |
| Birim Fiyatı | Birim fiyatı alanı varsayılan değeri, alt sözleşme satırının istenen başlangıç tarihi için geçerli olan proje fiyat listesiyle ilgili kategori fiyatlarındaki kategori ve birim bileşimi kullanılarak belirlenir.  |
| Alt Toplam | Bu salt okunur alan, hem miktar hem de birim fiyat değerleri girilirse miktar birim fiyatı olarak otomatik hesaplanır. Her iki alan da boşsa, bu alana el ile bir değer girebilirsiniz.  |
| Satış Vergisi | Satış vergisi tutarını girin.  |
| Toplam Tutar | Alt sözleşme satırının vergiler dahil toplam tutarı. Bu alan, alt toplam + satış vergisi olarak hesaplanır.  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
