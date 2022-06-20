---
title: İşçilik maliyet oranlarını ayarlama
description: Bu makalede, Project Operations işçilik maliyeti için fiyatları belirleme hakkında bilgiler yer almaktadır
author: rumant
ms.date: 10/12/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 5216c0af29eb33ce664857b1f42b4a3130f02c50
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924270"
---
# <a name="set-up-labor-cost-rates"></a>İşçilik maliyet oranlarını ayarlama

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_


Her fiyat listesi, fiyat listesinin içeriği ve tarih efektiyle uyumlu bir dizi işçilik oranlarına (rol fiyatları) sahiptir.

1. Bir fiyat listesi oluşturun ve **rol fiyatı** sekmesinde, alt ızgarada **Yeni Rol**'ü seçin.
2. **Hızlı Oluştur** sayfasında rol ve organizasyon birimini seçin.
3. Diğer gerekli alan bilgilerini girin.

Aşağıdaki tablo, maliyet fiyat listesinde işçilik oranları oluştururken önemli olan alanlardan bazılarını içerir.

| Alan | Konum | Veri Akışı Açıklaması | Aşağı yönlü etki |
| --- | --- | --- | --- |
| Rol | **Genel** sekme ve **Hızlı Oluşturma** sayfaları | Maliyet oranı uygulandığı rolü seçin. | Gelen tahmindeki veya fiili rol, rolün maliyetini varsayılan olarak bu satırla eşleşecektir. |
| Kaynak Atayan Şirket | **Genel** sekme ve **Hızlı Oluşturma** sayfaları | Rolün atandığı tüzel kişiliği seçin. Örneğin, Fabrikam Hindistan'dan bir geliştirici veya Fabrikam ABD'den bir geliştirici. | Gelen tahmindeki veya fiili kaynak şirket, rolün maliyetini varsayılan olarak bu satırla eşleşecektir. |
| Kaynak Belirleme Birimi | **Genel** sekme ve **Hızlı Oluşturma** sayfaları | Bu rolün kullanılacağı yerden şirketin kuruluş birimini veya bölümünü seçin. Örneğin, Fabrikam Hindistan'ın Robotik bölümünden bir geliştirici veya Fabrikam USA'nın Yazılım bölümünden bir geliştirici. | Gelen tahmindeki veya fiili kaynak ünitesinde, rolün maliyetini varsayılan olarak bu satırla eşleşecektir. |
| Fiyat | **Genel** sekme ve **Hızlı Oluşturma** sayfaları | Rol, kaynak şirket ve kaynak birimi kombinasyonu için maliyet oranını ayarlayın. Örneğin, Fabrikam Hindistan'dan bir geliştirici 1000 INR veya Fabrikam ABD'den bir geliştirici 150 USD tutar. | Fiyat, gelen tahminin birim maliyetindeki varsayılan değer ve **zaman** hareketi için gerçek satır maliyet oranıdır. |
| Para birimi | **Genel** sekme ve **Hızlı Oluşturma** sayfaları | Varsayılan olarak, para birimi değeri maliyet fiyat listesinin üstbilgisindeki para biriminden gelir, ancak geçersiz kılınabilir. Örneğin, Fabrikam Hindistan'dan bir geliştirici 1000 INR maliyeti. Fabrikam ABD'den bir geliştirici 150 USD maliyeti. | Para birimi, gelen fiili maliyet satırının birim maliyetindeki varsayılan değer ve **zaman** hareketi için gerçek satır maliyet oranıdır. Proje tahmininde, para birimi değeri proje para birimine dönüştürülür ve tahminin Zaman aşamalı görünümünde gösterilir. |
| Birim Çizelgesi | **Genel** sekme ve **Hızlı Oluşturma** sayfaları | Birim zamanlama varsayılan olarak Zaman'a dönüştürülebilir ve zaman birimlerine göre ekspres hızlar kullanıldığından Rol fiyat varlığında değiştirilemez. | Aşağıya doğru etkisi yoktur. |
| Birim | **Genel** sekme ve **Hızlı Oluşturma** sayfaları | Varsayılan olarak, maliyet fiyat listesinin üstbilgisindeki **Zaman Birimi**'nden gelir, ancak geçersiz kılınabilir. Değer geçersiz kılınabilir. Örneğin, Fabrikam Hindistan'dan **Hindistan günü** başına bir geliştirici 1000 INR maliyeti. Fabrikam ABD'den **ABD günü** başına bir geliştirici 150 USD maliyeti. | Sistem, gelen bir tahmin veya gerçek hat üzerindeki birim başına varsayılan fiyatı hesaplamak için birim başına maliyeti hesaplamak için birim birim ve dönüşüm sistemini kullanır. Örneğin, Hindistan'dan bir geliştirici için 10 **Hindistan Günü** değerinde çalışma için bir tahmindir ve birim, **Hindistan Günü** 10 saat olarak tanımlanır. Tahmin satırı maliyetlendirildiğinde, uygulama tahmini olarak birim maliyetini şu şekilde hesaplar: 1000 INR/10 saat = 100 INR ABD Doları olarak dönüştürülüp **proje tahminleri** sayfasında birim maliyet olarak gösterilir. |

## <a name="transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity"></a>Bölümünüz veya tüzel kişiliğiniz dışındaki kaynaklar için fiyatlandırma ve maliyet aktarımı

Proje tabanlı şirketlerin, projelerde çalışmak için şirketin farklı yerlerinden çalışanları kullanmaları için. Bir proje tek bir tüzel kişi tarafından yürütülebilir, ancak proje üzerinde çalışan çalışanlar veya danışmanlar aynı tüzel kişiden veya farklı bir tüzel kişiden gelebilir veya her ikisinin bir kombinasyonu olabilir. Dynamics 365 Project Operations'te, projenin teslimatına sahip tüzel kişilik **Sahibi Olan Şirket**'tir ve teslimata sahip bölüm **Sözleşme Birimi**'dir. Kaynak sağlayan diğer tüzel kişiler **Kaynak şirketleri** ve kaynak sağlayan bölümler **Kaynak üniteler**'dir. Çoğu ülkede, şirketlerin kaynak tüzel kişi veya bölüm sağlamak için, kaynak kullanımı için sahibi şirket ve sözleşme birimi ücret gereklidir.

Örneğin, Fabrikam şirketi, Fabrikam Hindistan-Robotik'in Fabrikam ABD-Robotik veya Fabrikam İngiltere-Robotik ile bir maliyet oranı kartı üzerinde anlaşma sağladığından emin olmalıdır.

Fabrikam Hindistan-Robotik'ten bir geliştirici, Fabrikam ABD-Robotics'e ödünç verildiğinde $100 ve Fabrikam U-Robotik'e ödünç verildiğinde $150 ücrete ular.

### <a name="set-up-costs-for-outside-resources"></a>Dış kaynaklar için maliyetleri ayarlama

1. Fabrikam *ABD-Robotik maliyet oranları* adlı bir maliyet fiyat listesi oluşturun ve bir tarih etkin aralığı ayarlayın.
2. Maliyet fiyat listesinde, aşağıdaki tablodaki bilgileri kullanarak fiyatları ayarlayın. 

| Rol | Kaynak Atayan Şirket | Kaynak Belirleme Birimi | Maliyet oranı |
| --- | --- | --- | --- |
| Geliştirici | Fabrikam India | Fabrikam Hindistan-Robotik | 100 ABD doları |
| Geliştirici | Fabrikam Filipinler | Fabrikam Filipinler-Robotik | $90 |
| Geliştirici | Fabrikam ABD | Fabrikam ABD-Robotik | $150 |

3. Bu maliyet fiyat listesini Fabrikam US-Robotics organizasyon birimine ekleyin.

### <a name="set-up-transfer-pricing-for-a-resource-in-the-appropriate-currency"></a>Uygun para birimindeki bir kaynak için transfer fiyatlandırması ayarlama 

Proje Operations'nde, kaynak fiyatlandırması herhangi bir para biriminde ayarlanabilir. Para birimi, fiyat listesi üstbilgisindekine göre varsayılandır, ancak değiştirilebilir.

Transfer fiyatı ayarı örneği kullanılarak bilgiler şu şekilde değiştirilebilir:

Fabrikam şirketi, Fabrikam Hindistan-Robotik'in Fabrikam ABD-Robotik veya Fabrikam İngiltere-Robotik ile bir maliyet oranı kartı üzerinde anlaşma sağladığından emin olmalıdır.

Fabrikam Hindistan-Robotik'ten bir geliştirici, Fabrikam ABD-Robotics'e ödünç verildiğinde $5000 ve Fabrikam U-Robotik'e ödünç verildiğinde $5500 ücrete ular.

Fabrikam US-Robotics'in maliyet fiyat listesinde maliyet oranları şu şekilde ifade edilebilir:

| Rol | Kaynak Atayan Şirket | Maliyet |
| --- | --- | --- |
| Geliştirici | Fabrikam India | 5000 INR |
| Geliştirici | Fabrikam ABD | 115 USD |

Fabrikam US-Robotics'in maliyet fiyat listesinde maliyet oranları şu şekilde ifade edilebilir:

| Rol | Kaynak atayan şirket | Maliyet |
| --- | --- | --- |
| Geliştirici | Fabrikam India | 5500 INR |
| Geliştirici | Fabrikam İngiltere | 115 GBP |

Maliyet fiyat listesi birden çok para biriminde işçilik oranları sağlayabilir. Proje üzerinde bir maliyet tahmini oluştururken, Project Operations bu maliyet oranlarını proje para birimine dönüştürür ve kullanıcıya görüntüler. Bir zaman girişi onaylandığında ve bir maliyet fiili oluşturulduğunda, maliyet fiili, maliyet fiyat listesindeki eşleşen rol fiyat satırının para birimi cinsinden fiyatlandırılır. Tek bir projedeki zaman ait maliyet fiili, birden çok para birimine kaydedilebilir. Ancak, proje düzeyindeki gerçek işçilik maliyetlerini oluştururken veya özetlediğinizde, proje Işlemleri tüm işçilik maliyet tutarlarını kullanıcının görüntüleyebileceği proje para birimine dönüştürür.


[!INCLUDE[footer-include](../includes/footer-banner.md)]