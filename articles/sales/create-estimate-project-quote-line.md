---
title: Proje teklif satırını tahmin etme
description: Bu makalede,proje teklif satırında nasıl tahmin oluşturulacağı hakkında bilgiler sağlanmaktadır.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9fd387da51da6e85e740aef529d488adcdf27c9a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912653"
---
# <a name="estimate-a-project-quote-line"></a>Proje teklif satırını tahmin etme

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Proje tabanlı teklif satırında, teklif satırını teslim etmek için mevcut işin maliyetini ve potansiyel gelirini tahmin etmeye yardımcı olan ayrıntılar bulunur.

Proje tabanlı teklif satırını tahmin etmek için teklif satırında **Teklif Satırı Ayrıntısı** sekmesini seçin. Proje tabanlı teklif satırında tahmin oluşturmanın iki yolu vardır:

   - Teklif satırı ayrıntılarını kullanarak teklif satırında elle doğrudan teklif oluşturun. 
   - Bir proje ve proje planı oluşturun ve ardından projeyi ve projedeki görevleri teklif satırıyla ilişkilendirin. Proje planındaki tahminleri sağladığınız bilgilere göre teklif satırında içeri aktarma işlemi etkinleştirilir.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Proje tabanlı teklif satırında doğrudan tahminler oluşturma

Doğrudan proje tabanlı teklif satırında tahminler oluşturmak için aşağıdaki adımları izleyin:

1. Proje tabanlı teklif satırında bir tahmin oluşturmak için **Teklif Satırı Ayrıntısı** sekmesini seçin. Bu sekmede oluşturduğunuz satır öğesi, bu teklif satırının teklif değerini özetler. 
2. Teklif satırı ayrıntıları oluşturmak için **Teklif Satırı Ayrıntıları** alt ızgarasında **Yeni Teklif Satırı Ayrıntısı**'nı seçin. Hızlı oluşturma kaydırıcısı açılır. **Teklif Satırı** sayfasında aşağıdaki alanlar yer alır.

| **Alan** | **Location** | **Açıklama** | **Aşağı yönlü etki** |
| --- | --- | --- | --- |
| Açıklama | Hızlı oluştur | Belirli bir tahminin açıklaması. | Bu değer, otomatik olarak oluşturulan maliyet için ilgili teklif satırı detaylarına varsayılan olarak alınır. |
| İşlem Sınıfı | Hızlı oluştur | Bu açılan listede, proje tabanlı teklif satırının **Genel** sekmesine dahil edilen işlem sınıfları sağlanır.  | Bu değer, otomatik olarak oluşturulan maliyet için ilgili teklif satırı detaylarına varsayılan olarak alınır. |
| Ürün Seç | Hızlı oluştur | Hareket sınıfı **Malzeme** olduğunda geçerlidir. Bu tahmin satırının, **Varolan** (katalog) bir ürün için mi **Serbest** bir ürün için mi olduğunu belirleyebilirsiniz. | Bu değer, otomatik olarak oluşturulan maliyet için ilgili teklif satırı detaylarına varsayılan olarak alınır. |
| Ürün | Hızlı oluştur | Ürün kataloğundan ürün kimliği. Bu alan, yalnızca **Ürün Seç** alanında **Varolan** öğesini seçtiğinizde etkinleştirilir. Kimlik, teklifteki proje fiyat listesinden satış fiyatını almak için kullanılır. | Bu değer, otomatik olarak oluşturulan maliyet için ilgili teklif satırı detaylarına varsayılan olarak alınır. |
| Serbest Eklenen Ürün | Hızlı oluştur | Ürün adını yazmak için bir metin kutusu. Bu alan, yalnızca **Ürün Seç** alanında **Serbest** öğesini seçtiğinizde etkinleştirilir.| Bu değer, otomatik olarak oluşturulan maliyet için ilgili teklif satırı detaylarına varsayılan olarak alınır. |
| Rol | Hızlı oluştur | Bu çalışmayı gerçekleştirecek veya bu gideri karşılayacak kişinin rolü. | Bu değer, otomatik olarak oluşturulan maliyet için ilgili teklif satırı detaylarına varsayılan olarak alınır. |
| Kategori | Hızlı oluştur | İş veya gider kategorisi. | Bu değer, otomatik olarak oluşturulan maliyet için ilgili teklif satırı detaylarına varsayılan olarak alınır. |
| Başlangıç Tarihi | Hızlı oluştur | İşin başlangıç tarihi. | Bu alan, otomatik olarak oluşturulan maliyet için teklif satırı ayrıntılarına varsayılan olarak alınır. |
| Bitiş Tarihi | Hızlı oluştur | İşin bitiş tarihi. | Bu alan, otomatik olarak oluşturulan maliyet için teklif satırı ayrıntılarına varsayılan olarak alınır. |
| Kaynak Atayan Şirket | Hızlı Oluştur | Bu maliyeti karşılayan ve üzerinde çalışılması için kaynağı sağlayan kaynak atayan şirket veya tüzel kişilik. | Değer, otomatik olarak oluşturulan ve maliyet fiyatı almada kullanılan maliyet için ilgili teklif satırı detaylarına varsayılan olarak alınır. |
| Kaynak Belirleme Birimi | Hızlı oluştur | Bu maliyeti karşılayan ve üzerinde çalışılması için kaynağı sağlayan kaynak birimi. | Bu değer, otomatik olarak oluşturulan ve maliyet fiyatı almada kullanılan maliyet için ilgili teklif satırı detaylarına varsayılan olarak alınır. |
| Birim zamanlaması | Hızlı oluştur | İş, ürün veya giderin birim grubu. Birimler, bir birim zamanlamasına veya birim grubuna aittir. Örneğin, mil ve kilometre mesafeyi açıklayan bir birim grubuna ait birimlerdir. | Bu değer, otomatik olarak oluşturulan maliyet için ilgili teklif satırı detaylarına varsayılan olarak alınır. |
| Birim | Hızlı oluştur | İş, ürün veya giderin birimi. | Bu değer, otomatik olarak oluşturulan maliyet için ilgili teklif satırı detaylarına varsayılan olarak alınır. |
| Miktar | Hızlı oluştur | İş, ürün veya giderin miktarı. | Bu değer, otomatik olarak oluşturulan maliyet için ilgili teklif satırı detaylarına varsayılan olarak alınır. |
| Birim fiyatı | Hızlı Oluştur |Çalışmayı gerçekleştiren rolün fatura oranı, ürünün birim fiyatı veya ürün ya da gider kategorisinin satış fiyatı. **Zaman** için varsayılan, başlangıç tarihi için geçerli proje fiyatı listesinin rol fiyatı satırında bulunan fiyatlandırma boyutu değerlerinin birleşimine dayanır. **Giderler** için bu alanın varsayılan ayarı, proje fiyat listesindeki, başlangıç tarihi için geçerli olan hareket kategorisine yönelik fiyat kurulumundan alınır. İşlem kategorisi için fiyatlandırma yöntemi, birim başına fiyat değilse varsayılan değer yoktur ve bu alan boş bırakılır. Ürünler için bu alanın varsayılanı, başlangıç tarihi için geçerli proje fiyat listesindeki **Fiyat listesi maddesi** satırına dayanır.| Çalışmayı gerçekleştiren rolün maliyet oranı, gider kategorisinin birim başına maliyeti veya ürünün birim maliyeti. **Zaman** için varsayılan, başlangıç tarihi için geçerli sözleşme birimine eklenmiş maliyet fiyat listesinin rol fiyatı satırında bulunan fiyatlandırma boyutu değerlerinin birleşimine dayanır. Giderler varsayılan, başlangıç tarihi için geçerli sözleşme birimine eklenmiş masraf fiyat listesinin kategori fiyat satırına dayanır. Hareket kategorisinin fiyatlandırma yöntemi birim başına fiyat değilse varsayılan olmaz ve bu alan boş bırakılır. Ürünler için bu alanın varsayılanı, başlangıç tarihi için geçerli sözleşme birimine eklenmiş masraf fiyat listesinin **Fiyat listesi maddesi** satırına dayanır.|
| Tahmini Vergi | Hızlı oluştur | Bu iş veya gider için tahmini vergiyi el ile girebilirsiniz. | Bu alanda aşağı yönlü etki yoktur. |
| Miktar | Hızlı oluştur | **Miktar** ve **Fiyat** alanları boş bırakılırsa bilgileri bu alana el ile girebilirsiniz. Bu alanlar boş değilse bu alan salt okunur hale gelir ve (Miktar \* Birim fiyat) + Vergi olarak hesaplanır. | Bu alanda aşağı yönlü etki yoktur. |

## <a name="update-prices-on-quote-line-details"></a>Teklif satırı ayrıntılarında fiyatları güncelleştirme

Teklife ekli proje fiyat listesinde veya sözleşme biriminin maliyet fiyatı listesinde fiyatları değiştirdiyseniz bu değişikliği yansıtmak üzere tek tek teklif satırı ayrıntılarındaki fiyatları yenilemek için **Teklif** sayfasında **Yeniden Hesapla** seçeneğini belirleyebilirsiniz. **Yeniden hesapla**'yı seçtiğinizde, bu teklifteki tüm teklif satırlarıyla ilgili teklif satırı ayrıntılarının sıfırlanacağını bildiren bir uyarı görüntülenir. Satış ve maliyet teklif satırı ayrıntıları için fiyatları yenilemek üzere **Evet**'i seçin.

## <a name="access-quote-line-details-for-cost"></a>Maliyet için teklif satırı ayrıntılarına erişme

Maliyetin teklif satırı ayrıntılarına erişmek için aşağıdaki adımları izleyin:

1. **Teklif Satırı Ayrıntıları** sekmesinde, alt ızgaranın araç çubuğunda eylemleri etkinleştirmek için ızgarada bir satır seçin. 
2. Bu teklif satırı için ilgili maliyet oranını ve tutarı görmek üzere **Maliyet Ayrıntısını Aç**'ı seçin.

> [!NOTE]
> Maliyet için teklif satırı ayrıntısında kaynak birimi, miktar, tarihler, rol veya kategori değerlerinin değiştirilmesi, satışlar için teklif satırı ayrıntılarında karşılık gelen değerleri değiştirir.

## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Maliyet ve satışlar için teklif satırı ayrıntılarında para birimi

Satış için teklif satırı ayrıntılarındaki para birimi, varsayılan olarak teklif satırı ayrıntısının başlangıç tarihi için geçerli proje fiyat listesinden alınır.

Maliyet için teklif satırı ayrıntılarındaki para birimi, varsayılan olarak teklif satırı ayrıntısının başlangıç tarihi için geçerli teklifin sözleşme biriminin fiyat listesinden alınır.

> [!NOTE]
> Karlılık hesaplamaları, teklifte genel tahmini kar marjını raporlamak üzere maliyet ve satışlar için teklif satırı ayrıntılarındaki tutarı ortamın temel para birimine dönüştürür. Para birimi yuvarlama hataları ve değişen kenar boşlukları, etkili Döviz kurları olmadığı için oluşabilir. Bu hesaplamaları yalnızca proje tekliflerinde kullanın. Bunlar, yaklaşık değerler değildir veya döviz kurları için geçerlilik tarihinin yuvarlanması ve farkındalığına yönelik daha yüksek hassasiyet gerektiren gerçek bir meşru veya başka bir raporlama değildir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
