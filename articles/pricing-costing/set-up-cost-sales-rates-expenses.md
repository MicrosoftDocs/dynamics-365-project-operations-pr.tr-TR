---
title: Giderler için maliyet ve satış oranlarını ayarlama
description: Bu konu, işlem ve gider kategorileri için maliyet ve satış oranlarının nasıl ayarlanacağı hakkında bilgi sağlar.
author: rumant
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 34e3c24ae1aa999954af9b347633820d265ac0c3
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877244"
---
# <a name="set-up-cost-and-sales-rates-for-expenses"></a>Giderler için maliyet ve satış oranlarını ayarlama

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Dynamics 365 Project Operations'ta işlem kategorileri için maliyeti ve satış fiyatlarını ayarlayabilirsiniz. Maliyet ve satış fiyatları giderler için tasarlandığından, bunları içeren her bir hareket kategorisi de masraf kategorisi olarak ayarlanmalıdır. Bu ayarlar, akış yönündeki işlevsellik için doğruluk sağlar. Hareket kategorilerinin maliyet ve satış fiyatları yalnızca tek bir para birimi cinsinden listelenebilir ve bu, Fiyat listesi başlığında para birimi olması gerekir.

Hareket kategorileri için maliyet ve satış oranları ayarlamak üzere aşağıdaki adımları izleyin. 

1. **Satış** > **Müşteriler** > **Fiyat Listeleri**'ne gidin.
2. Yeni fiyat listesi oluşturmak için **Yeni**'yi seçin. 
3. **Kategori fiyatları**'nın alt ızgara menüsünde, **Yeni Kategori Fiyatı**'nı seçin. 
4. **Hızlı kayıt** sayfasında, için yeni fiyatı oluşturacağınız hareket kategorisini ve birimi girin.

Aşağıdaki tabloda, **genel** sekmesindeki alanlar ve bir satış fiyatı listesinde rol fiyatları oluştururken aklınızda bulundurmanız gereken bir rol fiyatı satırının **hızlı kayıt** bölmesi yer almaktadır:

| Alan | Konum | Veri Akışı Açıklaması | Aşağı yönlü etki |
| --- | --- | --- | --- |
| İşlem Kategorisi | **Genel** sekme ve **Hızlı Oluşturma** sayfaları | Satış veya maliyet fiyatı oluşturduğunuz hareket kategorisini seçin. | Gelen tahmindeki veya Gİder için fiilindeki işlem kategorisi, işlem kategorisinin maliyetini varsayılan olarak bu satırla eşleşecektir. |
| Birim Çizelgesi | **Genel** sekme ve **Hızlı Oluşturma** sayfaları | Birim çizelgesi, işlem kategorisinin birim iş çizelgesinin varsayılan değerlerini alır. | Bu alanda aşağı yönlü etki yoktur. |
| Birim | **Genel** sekme ve **Hızlı Oluşturma** sayfaları | Oranların ayarlandığı birimi seçin. | Gelen tahminin veya gerçekteki birim, bu satırdaki birimle varsayılan olarak masraf tahmininin veya gerçek oranla karşılaştırmalı olarak eşleştirilir. |
| Fiyatlandırma Yöntemi | **Genel** sekme ve **Hızlı Oluşturma** sayfaları | **Fiyatlandırma yöntemi** alanının olası değerleri, **birim başına fiyat**, **maliyet** ve **maliyet üzerinden biçimlendirme**'dir. | Fiyat ayarı sırasında, **birim başına fiyatı** seçmek, Kategori fiyat satırındaki **yüzde** alanını kilitler. **Maliyet** seçilirse, **Fiyat** ve **yüzde** alanları satış fiyatı listesinde kilitlidir. **Maliyet üzerinden işaretlemeyi** seçmek , satış fiyatı listesindeki **Fiyat** alanını kilitler. Gelen gerçek bir satırda gider için **maliyet** veya **Maliyet fiyatlandırma yöntemi** üzerinde işaretleme, karşılık gelen faturalandırmayan satış satırıyla, gerçek maliyet üzerindeki fiyata eşit olan veya fiyat üzerinden bir işaretleme olarak hesaplanan bir fiyatı atamatır. |
| Fiyat | **Genel** sekme ve **Hızlı Oluşturma** sayfaları | Hareket kategorisi ve birim birleşimi için birim başına oran ayarlayın. Örneğin, harcırah oranı her mil ve 8 USD için 10 USD. | Kilometre ücreti, gelen tahminin birim maliyetindeki varsayılan değer ve zaman hareketi için gerçek satır maliyet oranıdır.|
| Yüzde | **Genel** sekme ve **Hızlı Oluşturma** sayfaları | Hareket kategorisi ve birim birleşimi için maliyet üzerinden yüzde ayarlayın. Örneğin, Airfare satış kuru, tahakkuk eden Airfare gideri maliyeti üzerinden yüzde 10'a kadar olarak işaretlenmelidir. | Maliyet üzerindeki kar payı yüzdesini girin. Bu alan yalnızca seçilen fiyat hesaplama yöntemi **Maliyet üzerinden kar payı** olduğunda kullanılabilir. |
| Para birimi | **Genel** sekme ve **Hızlı Oluşturma** sayfaları | Varsayılan olarak, para birimi değeri satış fiyat listesi üst bilgisindeki para biriminden gelir. Hareket kategorisi fiyatlandırması için para birimi geçersiz kılınamaz. | Bu para birimi, gelen tahminin birim maliyetindeki varsayılan değer ve zaman hareketi için gerçek satır maliyet oranıdır. |

## <a name="pricing-methods-for-expenses"></a>Giderler için fiyatlandırma yöntemleri

Yalnızca gider fiyatlandırma bağlamında ilgili kategori fiyatlarını ayarladığınızda, aşağıdaki üç fiyatlandırma yönteminden birini kullanabilirsiniz:

- **Birim fiyatı**
- **Maliyette**
- **Maliyet üzerinde kar payı**

### <a name="price-per-unit"></a>Birim fiyatı
Bu fiyatlandırma yöntemi bir satış fiyatı listesine bağlantılandırılmış bir kategori fiyat satırında seçildiğinde, hem tahmin, hem de gerçek değer olarak kategori ve birim kombinasyonunun varsayılan değerleri hesaplanır. Tahmin, giderler için proje tahmini satırları anlamına gelir, teklif satır ayrıntısı ve giderler için sözleşme satırı ayrıntısı.

### <a name="at-cost"></a>Maliyette
Bu fiyatlandırma yöntemi bir satış fiyatı listesine bağlantılandırılmış bir kategori fiyat satırında seçildiğinde, hem tahmin, hem de gerçek değer olarak kategori ve birim kombinasyonunun varsayılan değerleri hesaplanır. Örneğin, masraf hareket sınıfı için faturalandıralınmamış satış fiili değerleri. Birim Fiyat, bu masraf için gerçek maliyet üzerindeki birim fiyattan alınan faturalandırılmyan satışlar fiili değeri üzerinde ayarlanır. Maliyeti temel alan Fiyat varsayılanı, giderler için proje tahminlerine veya gider için teklif satırı ve sözleşme satırı ayrıntılarına yapılmaz.

### <a name="markup-over-cost"></a>Maliyet üzerinde kar payı
Bu fiyatlandırma yöntemi bir satış fiyatı listesine bağlantılandırılmış bir kategori fiyat satırında seçildiğinde, hem tahmin, hem de gerçek değer olarak kategori ve birim kombinasyonunun varsayılan değerleri hesaplanır. Örneğin, masraf hareket sınıfı için faturalandıralınmamış satış fiili değerleri. Bu birim fiyat, faturalanan satış fiili değerinin, tanımlanan biçimlendirme yüzdesi uygulandıktan sonra bu masraf için fiili maliyet üzerindeki birim fiyattan hesaplanan bir değere ayarlanmıştır. Maliyeti temel alan Fiyat varsayılanı, giderler için proje tahminlerine veya gider için teklif satırı ve sözleşme satırı ayrıntılarına yapılmaz.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
