---
title: İşçilik fatura oranlarını ayarlama - lite
description: Bu konuda Project Operations'ta iş gücü faturalandırma fiyatlarını ayarlama hakkında bilgi sağlanır.
author: rumant
manager: Annbe
ms.date: 10/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 733b7c83de8137aba6c084d5f03a2a4cf076a16c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274437"
---
# <a name="set-up-labor-bill-rates---lite"></a>İşçilik fatura oranlarını ayarlama - lite

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Her fiyat listesi, fiyat listesinin içeriği ve tarih efektiyle uyumlu bir dizi işçilik oranlarına (rol fiyatları) sahiptir. Dynamics 365 Project Operations'ta zaman için fatura oranları yalnızca tek bir para biriminde ayarlanabilir ve bu, Fiyat listesi başlığındaki para birimidir.

1. Bir satış fiyatı listesi için işçilik fatura tarifesinin ayarlanması için fiyat listesi başlığına dayanan bir fiyat listesi oluşturun. 
2. **Rol Fiyatlar** sekmesinde, alt kılavuzda **+ Yeni Rol Fiyatı**'nı seçin. 
3. **Hızlı kayıt** bölmesinde, fatura oranı ayarlamanız gereken rolü ve organizasyon birimi bileşimini girin.

  Aşağıdaki tabloda, **genel** sekmesindeki alanlar ve bir satış fiyatı listesinde rol fiyatları oluştururken aklınızda bulundurmanız gereken bir rol fiyatı satırının **hızlı kayıt** bölmesi yer almaktadır:

  | Alan | Konum | Veri Akışı Açıklaması | Aşağı yönlü etki |
  | --- | --- | --- | --- |
  | Rol | **Genel** sekme ve **Hızlı Oluşturma** bölme | Fatura sıklığını ayarladığınız rolü seçin. | Gelen tahmindeki veya fiili rol, rolün maliyetini varsayılan olarak bu satırla eşleşecektir. |
  | Kaynak Belirleme Birimi | **Genel** sekme ve **Hızlı Oluşturma** bölme | Bu rolün kullanılacağı yerden şirketin kuruluş birimini veya bölümünü seçin. Örneğin, Fabrikam Hindistan'ın Robotik bölümünden bir geliştirici veya Fabrikam USA'nın Yazılım bölümünden bir geliştirici. | Gelen tahmindeki veya fiili kaynak ünite, rolün faturasını varsayılan olarak bu satırla eşleşecektir. |
  | Fiyat | **Genel** sekme ve **Hızlı Oluşturma** bölme | Rol, kaynak şirket ve kaynak birimi kombinasyonu için fatura oranını ayarlayın. Örneğin, Fabrikam Hindistan'daki bir geliştiricinin ürün reçetesi oranı bir 100 USD veya Fabrikam ABD'deki bir ürün reçetesi 150 USD fatura puan oranına sahiptir. | Bu fiyat, gelen tahminin birim maliyetindeki varsayılan değer ve zaman hareketi için gerçek satır maliyet oranıdır. |
  | Para birimi | **Genel** sekme ve **Hızlı Oluşturma** bölme| Varsayılan olarak, para birimi değeri satış fiyat listesi üst bilgisindeki para biriminden gelir. Bir satış fiyatı listesinde, para birimi geçersiz kılınamaz. | Bu para birimi, gelen tahminin birim maliyetindeki varsayılan değer ve zaman hareketi için gerçek satır maliyet oranıdır. |
  | Birim Çizelgesi | **Genel** sekme ve **Hızlı Oluşturma** bölme | Birim zamanlama varsayılan olarak Zaman'a dönüştürülebilir ve zaman birimlerine göre ekspres hızlar kullanıldığından Rol fiyat varlığında değiştirilemez. | Bu alanda aşağı yönlü etki yoktur. |
  | Birim | **Genel** sekme ve **Hızlı Oluşturma** bölme | Maliyet fiyat listesinin üstbilgisindeki **Zaman Birimi**'nden gelir, ancak geçersiz kılınabilir. Değer geçersiz kılınabilir. Örneğin, Fabrikam Hindistan'dan **Hindistan günü** başına bir geliştirici 1000 USD maliyeti. Fabrikam ABD 'deki geliştirici bir **ABD gün** başına 1500 USD fatura hızına sahiptir. | Gelen tahmin veya gerçek satırdaki birim başına fiyt varsayılanlarında sistem, gelen birim başına varsayılan fiyatı hesaplamak için birim başına maliyeti hesaplamak için birim birim ve dönüşüm sistemini kullanır. Örneğin, Hindistan'dan bir geliştirici için 10 **Hindistan Günü** değerinde çalışma için bir tahmindir ve birim, Hindistan Günü 10 saat olarak tanımlanır. Satırı tahmin eden fiyatlandırma yaparken, uygulama tahmindeki birim fiyatı 1000 USD/10 saat = saat başına 100 USD olarak hesaplar. |


## <a name="transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions"></a>Diğer kuruluş birimlerindeki veya bölmelerin kaynak fiyatlarını aktarın veya fatura oranları ayarlayın. 

Proje tabanlı şirketlerin, projelerde çalışmak için şirketin farklı yerlerinden çalışanları kullanmaları için. Çalışanlar veya danışmanlar şirketin farklı bir bölümünden geldiği sırada, projeler bir bölümünden yürütülebilir. Proje ayrıca farklı bölmelerin bir bileşiminden da oluşturulabilir. Project Operations'ta projenin teslimatını sahipliğindeki şirkete, **ölçü birimi** olarak anılır. Kaynak sağlayan diğer tüm bölümler **kaynak birim** olarak adlandırılır. Dünyanın çeşitli coğrafi ve işçilik pazarlarının işçilik maliyetlerindeki farklılıklar nedeniyle, işçilik için fatura oranları farklı coğrafi bölgeler için de farklı şekilde ayarlanmıştır.

Örneğin, bir ABD projesinde çalışan fabrikam Hindistan 'dan gelen geliştirici, saat başına 100 USD oranına göre faturalandırılmasını ister. ABD projesi üzerinde çalışan fabrikam ABD 'de geliştirici bir saatte 150 USD faturalanalır.

### <a name="example-set-up-a-bill-rate"></a>Örnek: Fatura oranı ayarlama

1. *Fabrikam ABD fatura oranları* adında bir satış fiyatı listesi oluşturun ve bu tarihi verimlilik olarak ayarlayın.
2. Satış fiyat listesi formuna aşağıdaki bilgileri girin:

    | Rol | Kuruluş birimi | Fatura oranı |
    | --- | --- | --- |
    | Geliştirici | Fabrikam India | 100 ABD doları |
    | Geliştirici | Fabrikam Filipinler | $90 |
    | Geliştirici | Fabrikam ABD | $150 |

3. Proje sözleşmesinin proje fiyat listesine veya belirli bir hesaba satış fiyatı listesini **Fabrikam ABD fatura fiyatları** iliştirin.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]