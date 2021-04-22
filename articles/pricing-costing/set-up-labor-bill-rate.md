---
title: İşçilik fatura oranlarını ayarlama
description: Bu konuda Project Operations'ta iş gücü faturalandırma fiyatlarını ayarlama hakkında bilgi sağlanır.
author: rumant
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f0267fce673bbd0080022a8abf2dd0020cc8b662
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877424"
---
# <a name="set-up-labor-bill-rates"></a>İşçilik fatura oranlarını ayarlama

**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations

Her fiyat listesi, fiyat listesinin içeriği ve tarih efektiyle uyumlu bir dizi işçilik oranlarına (rol fiyatları) sahiptir. Dynamics 365 Project Operations'ta zaman için fatura oranları yalnızca tek bir para biriminde ayarlanabilir ve bu, Fiyat listesi başlığındaki para birimidir.

1. Bir satış fiyatı listesinin işçilik fatura oranlarını ayarlamak için **Satış** > **Müşteriler** > **Fiyat Listeleri**'ne gidin yeni bir fiyat listesi oluşturmak için **Yeni**'yi seçin. 
2. **Rol Fiyatlar** sekmesinde, alt ızgarada **Yeni Rol Fiyatı**'nı seçin. 
3. **Hızlı kayıt** bölmesinde, fatura oranı ayarlamanız gereken rolü ve organizasyon birimi bileşimini girin.

   Aşağıdaki tabloda, **genel** sekmesindeki alanlar ve bir satış fiyatı listesinde rol fiyatları oluştururken aklınızda bulundurmanız gereken bir rol fiyatı satırının **hızlı kayıt** bölmesi yer almaktadır:

    | Alan | Konum | Veri Akışı Açıklaması | Aşağı yönlü etki |
    | --- | --- | --- | --- |
    | Rol | **Genel** sekme ve **Hızlı Oluşturma** bölme | Fatura sıklığını ayarladığınız rolü seçin. | Gelen tahmindeki veya fiili rol, rolün maliyetini varsayılan olarak bu satırla eşleşecektir. |
    | Kaynak Atayan Şirket | **Genel** sekme ve **Hızlı Oluşturma** bölme | Rolün atandığı şirket veya tüzel kişiliği seçin. Örneğin, Fabrikam Hindistan'dan bir geliştirici veya Fabrikam ABD'den bir geliştirici. | Gelen tahmindeki veya fiili kaynak şirket, rolün faturasını varsayılan olarak bu satırla eşleşecektir. |
    | Kaynak Belirleme Birimi | **Genel** sekme ve **Hızlı Oluşturma** bölme | Bu rolün kullanılacağı yerden şirketin kuruluş birimini veya bölümünü seçin. Örneğin, Fabrikam Hindistan'ın Robotik bölümünden bir geliştirici veya Fabrikam USA'nın Yazılım bölümünden bir geliştirici. | Gelen tahmindeki veya fiili kaynak ünite, rolün faturasını varsayılan olarak bu satırla eşleşecektir. |
    | Fiyat | **Genel** sekme ve **Hızlı Oluşturma** bölme | Rol, kaynak şirket ve kaynak birimi kombinasyonu için fatura oranını ayarlayın. Örneğin, Fabrikam Hindistan'daki bir geliştiricinin ürün reçetesi oranı bir 100 USD veya Fabrikam ABD'deki bir ürün reçetesi 150 USD fatura puan oranına sahiptir. | Bu fiyat, gelen tahminin birim maliyetindeki varsayılan değer ve zaman hareketi için gerçek satır maliyet oranıdır. |
    | Para birimi | **Genel** sekme ve **Hızlı Oluşturma** bölme| Varsayılan olarak, para birimi değeri satış fiyat listesi üst bilgisindeki para biriminden gelir. Bir satış fiyatı listesinde, para birimi geçersiz kılınamaz. | Bu para birimi, gelen tahminin birim maliyetindeki varsayılan değer ve zaman hareketi için gerçek satır maliyet oranıdır. |
    | Birim Çizelgesi | **Genel** sekme ve **Hızlı Oluşturma** bölme | Birim zamanlama varsayılan olarak Zaman'a dönüştürülebilir ve zaman birimlerine göre ekspres hızlar kullanıldığından Rol fiyat varlığında değiştirilemez. | Bu alanda aşağı yönlü etki yoktur. |
    | Birim | **Genel** sekme ve **Hızlı Oluşturma** bölme | Maliyet fiyat listesinin üstbilgisindeki **Zaman Birimi**'nden gelir, ancak geçersiz kılınabilir. Değer geçersiz kılınabilir. Örneğin, Fabrikam Hindistan'dan **Hindistan günü** başına bir geliştirici 1000 USD maliyeti. Fabrikam ABD 'deki geliştirici bir **ABD gün** başına 1500 USD fatura hızına sahiptir. | Gelen tahmin veya gerçek satırdaki birim başına fiyt varsayılanlarında sistem, gelen birim başına varsayılan fiyatı hesaplamak için birim başına maliyeti hesaplamak için birim birim ve dönüşüm sistemini kullanır. Örneğin, Hindistan'dan bir geliştirici için 10 **Hindistan Günü** değerinde çalışma için bir tahmindir ve birim, Hindistan Günü 10 saat olarak tanımlanır. Satırı tahmin eden fiyatlandırma yaparken, uygulama tahmindeki birim fiyatı 1000 USD/10 saat = saat başına 100 USD olarak hesaplar. |

## <a name="transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions"></a>Diğer kuruluş birimlerindeki veya bölmelerin kaynak fiyatlarını aktarın veya fatura oranları ayarlayın. 

Proje tabanlı şirketler çoğu zaman projeler üzerinde çalışmak için farklı yasal varlıklardan ve yasal varlıktaki farklı bölmelerin çalışanlarını kullanırlar. Bir proje tek bir tüzel kişi tarafından yürütülebilir, ancak proje üzerinde çalışan çalışanlar veya danışmanlar aynı tüzel kişiden veya farklı bir tüzel kişiden gelebilir veya her ikisinin bir kombinasyonu olabilir. Proje ayrıca farklı yasal varlıklar ve bölmelerin bir bileşiminden da oluşturulabilir. Project Operations'nde, projenin teslimine sahip tüzel kişi **Sahibi Şirket**, teslimin sahibi ise **Yüklenici Birimdir**. Kaynak sağlayan diğer tüm tüzel kişiler **Kaynak şirketleri** ve kaynak sağlayan bölümler **Kaynak üniteler**'dir. Dünyanın çeşitli coğrafi ve işçilik pazarlarının işçilik maliyetlerindeki farklılıklar nedeniyle, işçilik için fatura oranları farklı coğrafi bölgeler için de farklı şekilde ayarlanmıştır.

Örneğin, bir ABD projesinde çalışan Fabrikam Hindistan'ın Robotik bölümünden geliştirici, saat başına 100 USD oranına göre faturalandırılmasını ister. ABD projesi üzerinde çalışan fabrikam ABD'nin robotik bölümü geliştirici bir saatte 150 USD faturalanalır. 

### <a name="example-set-up-a-bill-rate"></a>Örnek: Fatura oranı ayarlama 

1. *Fabrikam ABD fatura oranları* adında bir satış fiyatı listesi oluşturun ve bu tarihi verimlilik olarak ayarlayın.
2. Satış fiyat listesi formuna aşağıdaki bilgileri girin:

    | Rol | Kaynak atayan şirket | Kaynak belirleme birimi | Fatura oranı |
    | --- | --- | --- | --- |
    | Geliştirici | Fabrikam India | Fabrikam Hindistan-Robotik | 100 ABD doları |
    | Geliştirici | Fabrikam Filipinler | Fabrikam Filipinler-Robotik | $90 |
    | Geliştirici | Fabrikam ABD | Fabrikam ABD-Robotik | $150 |

3. Proje sözleşmesinin proje fiyat listesine veya belirli bir hesaba satış fiyatı listesini **Fabrikam ABD fatura fiyatları** iliştirin.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
