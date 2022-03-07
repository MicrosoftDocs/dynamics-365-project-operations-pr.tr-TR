---
title: Proje tabanlı sözleşme satırı tahmini - lite
description: Bu konu proje tabanlı bir sözleşme satırını tahmin etme hakkında bilgi sağlar.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 747a1abe5630cac3dc074eba3a469d8d858c5ef244b59e26921e35afa61645df
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999115"
---
# <a name="estimate-a-projectbased-contract-line---lite"></a>Proje tabanlı sözleşme satırı tahmini - lite

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Dynamics 365 Project Operations'ta proje tabanlı bir sözleşme satırı, sözleşme satırını teslim etmek için ilgili çalışmanın maliyet ve potansiyel gelirini tahmin etmenize yardımcı olan ayrıntılar içerir.

Proje tabanlı bir sözleşme satırını tahmin etmek için Proje tabanlı **sözleşme satırındaki** **Sözleşme satırı Ayrıntıları** sekmesine gidin.  Proje tabanlı bir sözleşme satırında tahmin oluşturmanın iki yolu vardır:

   - Sözleşme satırı ayrıntılarını el ile ekleyerek doğrudan sözleşme satırında bir tahmin oluşturun.
   - Bir proje ve proje planı oluşturun ve ardından projeyi ve görevleri projenin sözleşme satırıyla ilişkilendirin. Bu, sözleşme satırında yer alan bileşenlere dayalı olarak, proje planı tahminini sözleşme satırına içe aktarmaka için kullanılacak süreci sağlar.

## <a name="create-an-estimation-directly-on-a-projectbased-contract-line"></a>Proje tabanlı sözleşme satırında doğrudan tahmin oluşturma

Doğrudan proje tabanlı sözleşme satırında tahmin oluşturmak için aşağıdaki adımları izleyin:

1. Sözleşme satırına gidin ve **sözleşme satırı ayrıntıları** sekmesini seçin. Bu sekmede oluşturduğunuz satırlar özetlenir ve Bu **sözleşme satırı** için **anlaşmalı değer** olarak görüntülenir. 
2. **Sözleşme Satırı Ayrıntıları** alt ızgarasında, **Yeni Sözleşme Satırı Ayrıntısı**'nı seçin. Hızlı oluşturma kaydırıcısı açılır. **Sözleşme Satırı Ayrıntıları** sayfasında, aşağıdaki alanlar bulunur.

| Alan | Location | Açıklama | Aşağı yönlü etki |
| --- | --- | --- | --- |
| **Açıklama** | **Hızlı Oluştur** | Belirli bir tahminin açıklaması. | Bu değer, otomatik olarak oluşturulan maliyet için ilgili sözleşme satırı detaylarına varsayılan olarak alınır. |
| **İşlem Sınıfı** | **Hızlı Oluştur** | Bu, proje temelli sözleşme satırının **Genel** sekmesinde yer alan hareket sınıflarının bir listesidir. | Bu değer, otomatik olarak oluşturulan maliyet için ilgili sözleşme satırı detaylarına varsayılan olarak alınır. |
| **Ürün Seç** | **Hızlı oluştur** | Hareket sınıfı **Malzeme** olduğunda geçerlidir. Bu tahmin satırının, **Varolan** (katalog) bir ürün için mi **Serbest** bir ürün için mi olduğunu belirleyebilirsiniz. | Bu değer, otomatik olarak oluşturulan maliyet için ilgili sözleşme satırı detaylarına varsayılan olarak alınır. |
| **Ürün** | **Hızlı oluştur** | Ürün kataloğundan ürün kimliği. Bu alan, yalnızca **Ürün Seç** alanında **Varolan ürün** öğesini seçtiğinizde etkinleştirilir. Kimlik, sözleşmedeki proje fiyat listesinden satış fiyatını almak için kullanılır. | Bu değer, otomatik olarak oluşturulan maliyet için ilgili sözleşme satırı detaylarına varsayılan olarak alınır. |
| **Serbest Ürün** | **Hızlı oluştur** | Ürün adını girmek için bir metin alanı. Bu alan, yalnızca **Ürün Seç** alanında **Serbest** öğesini seçtiğinizde etkinleştirilir.| Bu değer, otomatik olarak oluşturulan maliyet için ilgili sözleşme satırı detaylarına varsayılan olarak alınır. |
| **Rol** | **Hızlı Oluştur** | Bu işi gerçekleştiren veya bu gideri ortaya alan kişinin rolü. | Bu değer, otomatik olarak oluşturulan maliyet için ilgili sözleşme satırı detaylarına varsayılan olarak alınır.|
| **Kategori** | **Hızlı Oluştur** | İş veya gider kategorisi. |Bu değer, otomatik olarak oluşturulan maliyet için ilgili sözleşme satırı detaylarına varsayılan olarak alınır.|
| **Başlangıç Tarihi** | **Hızlı Oluştur** | İşin başlangıç tarihi. | Bu değer, otomatik olarak oluşturulan maliyet için ilgili sözleşme satırı detaylarına varsayılan olarak alınır. |
| **Bitiş Tarihi** | **Hızlı Oluştur** | İşin bitiş tarihi. | Bu değer, otomatik olarak oluşturulan maliyet için ilgili sözleşme satırı detaylarına varsayılan olarak alınır. |
| **Kaynak Belirleme Birimi** | **Hızlı Oluştur** | Bu maliyeti karşılayan ve üzerinde çalışılması için kaynağı sağlayan kaynak birimi. |Bu değer, otomatik olarak oluşturulan ve maliyet fiyatı almada kullanılan maliyet için ilgili sözleşme satırı detaylarına varsayılan olarak alınır. |
| **Birim zamanlaması** | **Hızlı oluştur** | İş, ürün veya giderin birim grubu. Birimler, bir birim zamanlamasına veya birim grubuna aittir. Örneğin, *mil* ve *kilometre (kms)* mesafeyi açıklayan bir birim grubuna ait birimlerdir. | Bu değer, otomatik olarak oluşturulan maliyet için ilgili sözleşme satırı detaylarına varsayılan olarak alınır. |
| **Birim** | **Hızlı Oluştur** | İş, ürün veya giderin birimi. | Bu değer, otomatik olarak oluşturulan maliyet için ilgili sözleşme satırı detaylarına varsayılan olarak alınır. |
| **Miktar** | **Hızlı Oluştur** | İş, ürün veya giderin miktarı. | Bu değer, otomatik olarak oluşturulan maliyet için ilgili sözleşme satırı detaylarına varsayılan olarak alınır. |
| **Birim fiyatı** | **Hızlı Oluştur** | Çalışmayı gerçekleştiren rolün fatura oranı, ürünün birim fiyatı veya ürün ya da gider kategorisinin satış fiyatı. Bu alanın varsayılanı, başlangıç tarihi için geçerli proje fiyatı listesinin rol fiyatı satırında bulunan fiyatlandırma boyutu değerlerinin birleşimine dayanan **Zaman**'dır. **Giderler** için bu alanın varsayılan ayarı, proje fiyat listesindeki, başlangıç tarihi için geçerli olan hareket kategorisine yönelik fiyat kurulumundan alınır. İşlem kategorisi için fiyatlandırma yöntemi, **birim başına fiyat** değilse varsayılan değer yoktur ve bu alan boş bırakılır. Ürünler için bu alanın varsayılanı, başlangıç tarihi için geçerli proje fiyat listesindeki **Fiyat listesi maddesi** satırına dayanır.| Çalışmayı gerçekleştiren rolün maliyet oranı, gider kategorisinin birim başına maliyeti veya ürünün birim maliyeti. Bu alanın varsayılanı, başlangıç tarihi için geçerli sözleşme birimine eklenmiş maliyet fiyat listesinin rol fiyatı satırında bulunan fiyatlandırma boyutu değerlerinin birleşimine dayanan **Zaman**'dır. Giderler için bu alanın varsayılan ayarı, başlangıç tarihi için geçerli olan sözleşme birimine ekli olan maliyet fiyat listesinin kategori fiyat satırına bağlıdır. İşlem kategorisi için fiyatlandırma yöntemi, birim başına fiyat değilse varsayılan değer yoktur ve bu alan boş bırakılır. Ürünler için bu alanın varsayılanı, başlangıç tarihi için geçerli sözleşme birimine eklenmiş masraf fiyat listesinin **Fiyat listesi maddesi** satırına dayanır.|
| **Tahmini Vergi** | **Hızlı Oluştur** | Bu iş veya gider için tahmini vergi. | Bu iş veya gider için tahmini vergi. |
| **Miktar** | **Hızlı Oluştur** | Bu alandaki değeri, **Miktar** ve **Fiyat** alanları boş bırakılmışsa ekleyebilirsiniz. **Miktar** ve **Fiyat** doldurulmuşsa **tutar** alanı salt okunurdur ve **(miktar \* birim fiyatı) + vergi** olarak hesaplanır. | &nbsp; |

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
