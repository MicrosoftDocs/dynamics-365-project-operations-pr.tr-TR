---
title: Proje tabanlı sözleşme satırını tahmin etme
description: Bu makalede, proje sözleşme satırında tahminler hakkında bilgiler sağlanmaktadır.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 633ad3130a28d75ad10b81e03a883e0a732b1ba8
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825237"
---
# <a name="estimate-a-project-based-contract-line"></a>Proje tabanlı sözleşme satırını tahmin etme

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_ 

Dynamics 365 Project Operations'ta proje tabanlı bir sözleşme satırı, sözleşme satırını teslim etmek için ilgili çalışmanın maliyet ve potansiyel gelirini tahmin etmenize yardımcı olan ayrıntılar içerir.

Proje tabanlı bir sözleşme satırını tahmin etmek için Proje tabanlı **sözleşme satırındaki** **Sözleşme satırı Ayrıntıları** sekmesine gidin.  Proje tabanlı bir sözleşme satırında tahmin oluşturmanın iki yolu vardır:

   - Sözleşme satırı ayrıntılarını el ile ekleyerek doğrudan sözleşme satırında bir tahmin oluşturun.
   - Bir proje ve proje planı oluşturun ve ardından projeyi ve görevleri projenin sözleşme satırıyla ilişkilendirin. Bu, sözleşme satırında yer alan bileşenlere dayalı olarak, proje planı tahminini sözleşme satırına içe aktarmaka için kullanılacak süreci sağlar.

## <a name="create-an-estimate-directly-on-a-project-contract-line"></a>Doğrudan proje sözleşme satırında tahmin oluşturma

Doğrudan proje sözleşme satırında tahmin oluşturmak için aşağıdaki adımları izleyin:

1. Sözleşme satırına gidin ve **sözleşme satırı ayrıntıları** sekmesini seçin. Bu sekmede oluşturduğunuz satırlar özetlenir ve Bu **sözleşme satırı** için **anlaşmalı değer** olarak görüntülenir. 
2. **Sözleşme Satırı Ayrıntıları** alt ızgarasında, **Yeni Sözleşme Satırı Ayrıntısı**'nı seçin. Hızlı oluşturma kaydırıcısı açılır. **Sözleşme Satırı Ayrıntıları** sayfasında, aşağıdaki alanlar bulunur.

| Alan | Location | Açıklama | Aşağı yönlü etki |
| --- | --- | --- | --- |
| **Açıklama** | **Hızlı Oluştur** | Belirli bir tahminin açıklaması. | Bu değer, otomatik olarak oluşturulan maliyet için ilgili sözleşme satırı detaylarına varsayılan olarak alınır. |
| **İşlem Sınıfı** | **Hızlı Oluştur** | Hareket sınıflarının listesi, proje temelli sözleşme satırının **Genel** sekmesinde yer alır. | Bu değer, otomatik olarak oluşturulan maliyet için ilgili sözleşme satırı detaylarına varsayılan olarak alınır. |
| **Ürün Seç** | **Hızlı oluştur** | Hareket sınıfı **Malzeme** olduğunda geçerlidir. Bu tahmin satırının, **Varolan** (katalog) bir ürün için mi **Serbest** bir ürün için mi olduğunu belirlemek için seçim yapabilirsiniz. | Bu değer, otomatik olarak oluşturulan maliyet için ilgili sözleşme satırı detaylarına varsayılan olarak alınır. |
| **Ürün** | **Hızlı oluştur** | Ürün kataloğundan ürün kimliği. Bu alan, yalnızca **Ürün Seç** alanında **Varolan ürün** öğesini seçtiğinizde etkinleştirilir. Kimlik, sözleşmedeki proje fiyat listesinden satış fiyatını almak için kullanılır. | Bu değer, otomatik olarak oluşturulan maliyet için ilgili sözleşme satırı detaylarına varsayılan olarak alınır. |
| **Serbest Ürün** | **Hızlı oluştur** | Ürün adını girmek için bir metin alanı. Bu alan, yalnızca **Ürün Seç** alanında **Serbest** öğesini seçtiğinizde etkinleştirilir.| Bu değer, otomatik olarak oluşturulan maliyet için ilgili sözleşme satırı detaylarına varsayılan olarak alınır. |
| **Rol** | **Hızlı Oluştur** | Bu işi gerçekleştiren veya bu gideri ortaya alan kişinin rolü. | Bu değer, otomatik olarak oluşturulan maliyet için ilgili sözleşme satırı detaylarına varsayılan olarak alınır.|
| **Kategori** | **Hızlı Oluştur** | İş veya gider kategorisi. | Bu değer, otomatik olarak oluşturulan maliyet için ilgili sözleşme satırı detaylarına varsayılan olarak alınır.|
| **Başlangıç Tarihi** | **Hızlı Oluştur** | İşin başlangıç tarihi. | Bu değer, otomatik olarak oluşturulan maliyet için ilgili sözleşme satırı detaylarına varsayılan olarak alınır. |
| **Bitiş Tarihi** | **Hızlı Oluştur** | İşin bitiş tarihi. | Bu değer, otomatik olarak oluşturulan maliyet için ilgili sözleşme satırı detaylarına varsayılan olarak alınır. |
| **Kaynak Atayan Şirket** | **Hızlı Oluştur** | Bu maliyeti karşılayan ve üzerinde çalışılması için kaynağı sağlayan kaynak atayan şirket veya tüzel kişilik. | Bu değer, otomatik olarak oluşturulan ve maliyet fiyatı almada kullanılan maliyet için ilgili sözleşme satırı detaylarına varsayılan olarak alınır. |
| **Kaynak Belirleme Birimi** | **Hızlı Oluştur** | Bu maliyeti karşılayan ve üzerinde çalışılması için kaynağı sağlayan kaynak birimi. | Bu değer, otomatik olarak oluşturulan ve maliyet fiyatı almada kullanılan maliyet için ilgili sözleşme satırı detaylarına varsayılan olarak alınır. |
| **Birim zamanlaması** | **Hızlı oluştur** | İş, ürün veya giderin birim grubu. Birimler, bir birim zamanlamasına veya birim grubuna aittir. Örneğin, *mil* ve *kilometre (kms)* mesafeyi açıklayan bir birim grubuna ait birimlerdir. | Bu değer, otomatik olarak oluşturulan maliyet için ilgili sözleşme satırı detaylarına varsayılan olarak alınır. |
| **Birim** | **Hızlı Oluştur** | İş, ürün veya giderin birimi. | Bu değer, otomatik olarak oluşturulan maliyet için ilgili sözleşme satırı detaylarına varsayılan olarak alınır. |
| **Miktar** | **Hızlı Oluştur** | İş, ürün veya giderin miktarı. | Bu değer, otomatik olarak oluşturulan maliyet için ilgili sözleşme satırı detaylarına varsayılan olarak alınır. |
| **Birim fiyatı** | **Hızlı Oluştur** | Çalışmayı gerçekleştiren rolün fatura oranı, ürünün birim fiyatı veya ürün ya da gider kategorisinin satış fiyatı. **Zaman** için varsayılan, başlangıç tarihi için geçerli proje fiyatı listesinin rol fiyatı satırında bulunan fiyatlandırma boyutu değerlerinin birleşimine dayanır. **Giderler** için bu alanın varsayılanı, başlangıç tarihi için geçerli proje fiyat listesindeki hareket kategorisinin fiyat ayarlarından alınır. İşlem kategorisi için fiyatlandırma yöntemi, **birim başına fiyat** değilse varsayılan değer yoktur ve bu alan boş bırakılır. Ürünler için bu alanın varsayılanı, başlangıç tarihi için geçerli proje fiyat listesindeki **Fiyat listesi maddesi** satırına dayanır.| Çalışmayı gerçekleştiren rolün maliyet oranı, gider kategorisinin birim başına maliyeti veya ürünün birim maliyeti. **Zaman** için varsayılan, başlangıç tarihi için geçerli sözleşme birimine eklenmiş maliyet fiyat listesinin rol fiyatı satırında bulunan fiyatlandırma boyutu değerlerinin birleşimine dayanır. **Giderler** için bu alanın varsayılanı, başlangıç tarihi için geçerli sözleşme birimine eklenmiş masraf fiyat listesinin kategori fiyat satırına dayanır. İşlem kategorisi için fiyatlandırma yöntemi, birim başına fiyat değilse varsayılan değer yoktur ve bu alan boş bırakılır. Ürünler için bu alanın varsayılanı, başlangıç tarihi için geçerli sözleşme birimine eklenmiş masraf fiyat listesinin **Fiyat listesi maddesi** satırına dayanır.|
| **Tahmini Vergi** | **Hızlı Oluştur** | Bu iş veya gider için tahmini vergi, kullanıcı tarafından girildiği şekilde. | &nbsp; |
| **Miktar** | **Hızlı Oluştur** | Bu alandaki değer, **Miktar** ve **Fiyat** alanları boş bırakılmışsa eklenebilir. **Miktar** ve **Fiyat** alanları doldurulmuşsa **Tutar** alanı salt okunur olur ve **(Miktar \* Birim fiyatı) + Vergi** olarak hesaplanır. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Sözleşme satırı ayrıntılarında fiyatları güncelleştir

Sözleşmeye iliştirilen proje fiyat listesindeki fiyatları veya sözleşme biriminin maliyet fiyatı listesini değiştirirseniz, değişikliği yansıtmak için her sözleşme satırı ayrıntılarında fiyatları yenileyebilirsiniz. **Sözleşme** sayfasında **Yeniden hesapla**'yı seçin. Bu sözleşmedeki tüm sözleşme satırları için fiyatların sıfırlandığını bildiren bir uyarı görüntülenir. Satış ve maliyet sözleşme satırı ayrıntılarının her ikisi için de fiyatları yenilemek üzere **Evet**'i seçin.

## <a name="access-contract-line-details-for-cost"></a>Maliyet erişim sözleşmesi satır ayrıntıları

**Sözleşme satırı ayrıntıları** sekmesinde, alt kılavuzun araç çubuğunda bazı eylemleri etkinleştirmek için ızgarasında bir satır seçin. Alt kılavuz araç çubuğundaki ilk eylem **Açık maliyet ayrıntısı**'dır. Bu sözleşme satırı ayrıntısı için ilgili maliyet oranını ve tutarı görmek için **Açık maliyet ayrıntısı**'nı seçin. 

> [!NOTE]
> **Maliyet** için kaynak şirketi, kaynak birim, miktar, tarih, rol veya sözleşme satırı ayrıntısı üzerinde kategori değerlerini değiştirmek **Satış** için ilgili sözleşme satırı ayrıntısının karşılık gelen değerlerini de değiştirir.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Sözleşme satırındaki para birimi maliyet ve satış ayrıntıları

**Satışlar** için sözleşme satırı ayrıntısı Proje Fiyat listesinden, sözleşme satırı ayrıntısı başlangıç tarihi için geçerli olan varsayılan para birimini ayarlar.

**Maliyet** için sözleşme satırı ayrıntısı sözleşmenin sözleşme birimi Fiyat listesinden, **Maliyet** için sözleşme satırı ayrıntısı başlangıç tarihi için geçerli olan varsayılan para birimini ayarlar.

Karlılık hesaplamaları, **Maliyet** ve **Satış** için sözleşme satırı ayrıntılarının tutarlarını, sözleşmenin genel gerçek ve tahmini kenar boşluklarını raporlamak için ortamın temel para birimine dönüştürür.

> [!NOTE]
> Para birimi yuvarlama hataları ve değişen kenar boşlukları, etkili Döviz kurları olmadığı için oluşabilir. Bu hesaplamaları yalnızca proje sözleşmelerinde kullanın. Bunlar, yaklaşık değerler değildir veya döviz kurları için geçerlilik tarihinin yuvarlanması ve farkındalığına yönelik daha yüksek hassasiyet gerektiren gerçek bir meşru veya başka bir raporlama için değildir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
