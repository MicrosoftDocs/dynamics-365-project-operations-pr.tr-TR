---
title: Ürünler için alt sözleşme satırları
description: Bu konu, ürünler için alt sözleşme satırlarının nasıl kaydedileceğini ve satıcılardan yapılan ürün satın alımları kaydetmek için çeşitli alanların nasıl kullanacağını açıklar.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c0ddc39638ae9830eacc57f3e1def75aa36e6553
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323710"
---
# <a name="subcontract-lines-for-products"></a>Ürünler için alt sözleşme satırları

[!include [banner](../../includes/dataverse-preview.md)]

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Dynamics 365 Project Operations'daki bir alt sözleşmede ürünler için bir alt sözleşme satırı bulunabilir. Bu satırlar, Proje Yöneticisinin daha sonra proje görevlerinde kullanılmak üzere satıcılardan ürün satın almasına olanak verir.

Project Operations'da ürünler için bir alt sözleşme satırı oluşturmak üzere aşağıdaki adımları uygulayın.

1. Gezinti sayfasında, **Alt sözleşmeler**'i seçin ve çalışmak istediğiniz bir alt sözleşmeyi açın. 
2. **Alt Sözleşme Satırları** sekmesinde yeni bir alt sözleşme satırı oluşturmak için **+ Yeni**'yi seçin.
3. **Hızlı Oluştur** sayfasında, **İşlem Sınıfı** alanında, **Malzeme**'yi seçin ve gerekli alan bilgilerini girin veya seçin. 
4. **Kaydet**'i seçin.

Aşağıdaki tabloda, ürün satınalma ile ilgili olan **Alt sözleşme satırı ayrıntıları** ve **Hızlı oluştur** sayfasındaki alanlarla ilgili bilgiler yer almaktadır.

| Alan | Açıklama |
| ----- | ----------- |
| Adı | Alt sözleşme satırının adı. |
| Açıklama | Alt sözleşme satırında sipariş edilen ürünlerle ilgili kısa bir açıklama. |
| Hat Türü | Bu alan değeri varsayılan olarak **Miktar tabanlı** olarak ayarlanır. |
| Faturalama Yöntemi |  Alt sözleşme satırının faturalama yöntemi. Sabit fiyatlı faturalama yöntemleri için kilometre taşı tabanlı fatura zamanlaması kullanılabilir. |
| İşlem Sınıfı | Bu alan değeri varsayılan olarak **Zaman** olarak ayarlanır. Ürün satın alma için alt sözleşme satırları oluşturmak üzere **İşlem sınıfı** alanında **Malzeme** seçeneğini belirleyin. Bu seçim, alt sözleşme satırının projelerde kullanılacak ürün satın alımını kaydetmek için kullanıldığını gösterir. |
| Ürün Seçin | Satın alınan ürün, ürün kataloğunda tutuluyorsa veya serbest eklenen ürünse seçin. |
| Ürün | Katalogdan etkin bir ürün seçin. Bu alan yalnızca **Ürün Seç** **Mevcut** olarak ayarlandığında kullanılabilir. |
| Serbest Ürün | Serbest eklenen ürünün adını girin. Bu alan yalnızca **Ürün Seç** **Serbest eklenen** olarak ayarlandığında kullanılabilir.  |
| Talep Edilen Teslimat Tarihi | Ürünler için gerekli teslim tarihini seçin. Bu tarih, alt sözleşmeye eklenen proje fiyat listelerinden bir proje fiyat listesi seçmek için de kullanılır. Alt sözleşme satırındaki ürünün maliyeti daha sonra varsayılan olarak bu fiyat listesinden alınır. |
| Sözleşmedeki teslim tarihi | Sözleşmede ürünün teslimi için mutabık kalınan tarihi seçin.  |
| Sipariş Edilen Miktar | Satıcıdan satın alınan ürünün miktarını girin. Proje Yöneticisi bu miktardan fazla ürün çekerse bir uyarı oluşur. |
| Birim Grubu | Bu değer yalnızca katalog ürünleri için varsayılan olarak kullanılır. Hem **Ürün** hem de **İstenen teslim tarihi** seçildiğinde, sistem teslimat tarihine göre uygun fiyat listesini seçer. İlgili fiyat listesi kalemleri, eşleşen ürün için sorgulanır. birim ve birim grubu değerleri varsayılanı fiyat listesi öğesi kaydındaki kurulumdan ayarlanır. |
| Birim | Bu değer varsayılanı, fiyat listesi kalemi kaydındaki birim ayarından ayarlanır. Bunu gerektiği gibi başka bir birimle değiştirebilirsiniz. Ürün ve birim birleşimi, mevcut katalog ürünleri için alt sözleşme satırındaki birim fiyatı varsayılanı olarak kullanır. |
| Birim Fiyatı | Birim fiyatı varsayılan değeri, bir alt sözleşme satırının istenen teslim tarihi için geçerli olan proje fiyat listesiyle ilgili fiyat listesi kalemlerinden ürün ve birim bileşimi kullanılarak belirlenir.  |
| Alt Toplam | Bu salt okunur alan, her iki alana da değer girildiyse, Miktar x Birim fiyat olarak hesaplanır. **Miktar** alanı, **Birim Fiyat** alanı veya her ikisi de boşsa, el ile bir değer girebilirsiniz.  |
| Satış Vergisi | Satış vergisi değerini girin. |
| Toplam Tutar | Bu hesaplanan alan, vergiler dahil edildikten sonra alt sözleşme toplam tutarını gösterir. Bu alandaki değer, alt toplam + vergi olarak hesaplanır. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
