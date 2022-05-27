---
title: Ürünler için alt sözleşme satırları
description: Bu konu, ürünler için alt sözleşme satırlarının nasıl kaydedileceğini ve satıcılardan yapılan ürün satın alımları kaydetmek için çeşitli alanların nasıl kullanacağını açıklar.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 71e4a48c3d29d7ea5b015f6c6797da60001fccff
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579097"
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

| Alan | Açıklama | İşlevsel etki|
| ----- | ----------- | ----------- |
| Adı | Tanımlamayla ile ilgili yardım için alt sözleşme satırının adı. |Bu, alt sözleşme satırlarına dayalı olarak tüm aramalarda ilk sütun olarak gösterilir.
| Açıklama | Alt sözleşme satırında sipariş edilen ürünlerle ilgili kısa bir açıklama. | Hiçbiri |
| Hat Türü | Bu alan **Miktar tabanlı** varsayılan değerine sahiptir. |Hiçbiri |
| Faturalama Yöntemi | Bu, Project Operations tarafından desteklenen iki ana sözleşme modelini temsil eden bir seçenek kümesidir: **Sabit Fiyat** ve **Zaman ve Malzeme**. | Seçilen faturalama yöntemine göre, Sabit Fiyat faturalandırma yönteminin seçildiği alt sözleşme satırları için kilometre taşı tabanlı bir fatura zamanlaması sunulur. |
| İşlem Sınıfı |Bu alan **Zaman** varsayılan değerine sahiptir. Ürün satın alma için alt sözleşme satırları oluşturmak üzere **İşlem sınıfı** alanını **Malzeme** olarak ayarlayın.  | Bu, bir alt sözleşme satırının, projelerde kullanılacak ürünlerin satın alımını kaydetmek için kullanıldığını gösterir. |
| Ürün Seçin | Satın alınan ürün, ürün kataloğunda tutuluyorsa veya serbest eklenen ürünse seçin. |Hiçbiri |
| Ürün | Katalogdan etkin bir ürün seçin. Bu alan yalnızca **Ürün Seç** **Mevcut** olarak ayarlandığında kullanılabilir. |**Ürün** ve **Birim** birleşimi varsayılan olarak kullanılır veya alt sözleşme satırının birim fiyatı için hesaplanır.
| Serbest Ürün | Serbest eklenen ürünün adını girin. Bu alan yalnızca **Ürün Seç** **Serbest eklenen** olarak ayarlandığında kullanılabilir.  |Satınalma fiyatı, serbest ürünler için otomatik olarak doldurulmaz.|
| Talep Edilen Teslimat Tarihi | Ürünler için gereken teslim tarihini girin.| Bu tarih, alt sözleşmeye eklenen proje fiyat listelerinden bir proje fiyat listesi seçmek için de kullanılır. Alt sözleşme satırındaki ürünün maliyeti daha sonra varsayılan olarak bu fiyat listesinden alınır. |
| Sözleşmedeki teslim tarihi | Ürünlerin sözleşmeyle belirlenen teslim tarihini girin.  |Hiçbiri|
| Sipariş Edilen Miktar | Satıcıdan satın alınan ürünün miktarını girin.| Bu, bir proje yöneticisi bu miktardan daha fazlasını çektiğinde uyarı göstermek için kullanılacaktır.|
| Birim Grubu | Bu değer yalnızca katalog ürünleri için varsayılan olarak kullanılır. |Hem **Ürün** hem de **İstenen teslim tarihi** seçildiğinde, sistem teslimat tarihine göre uygun fiyat listesini seçer. İlgili fiyat listesi kalemleri, eşleşen ürün için sorgulanır. birim ve birim grubu değerleri varsayılanı fiyat listesi öğesi kaydındaki kurulumdan ayarlanır. |
| Birim | Bu değer varsayılan olarak ürün fiyat listesi kalemi kaydında ayarlanan birimdir. Bunu gerektiği gibi başka bir birimle değiştirebilirsiniz.| Ürün ve birim birleşimi, mevcut katalog ürünleri için alt sözleşme satırındaki birim fiyatı varsayılanı olarak kullanır. |
| Birim Fiyatı | Birim fiyatı varsayılan değeri, bir alt sözleşme satırının istenen teslim tarihi için geçerli olan proje fiyat listesiyle ilgili fiyat listesi kalemlerinden ürün ve birim bileşimi kullanılarak belirlenir.  |Hiçbiri |
| Alt Toplam | Bu salt okunur alan, her iki alana da değer girildiyse, Miktar x Birim fiyat olarak hesaplanır. **Miktar** alanı, **Birim Fiyat** alanı veya her ikisi de boşsa, el ile bir değer girebilirsiniz.  |Hiçbiri |
| Satış Vergisi | Satış vergisi değerini girin. |Hiçbiri |
| Toplam Tutar | Bu hesaplanan alan, vergiler dahil edildikten sonra alt sözleşme toplam tutarını gösterir. Bu alandaki değer, Ara Toplam + Vergi olarak hesaplanır. |Hiçbiri |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
