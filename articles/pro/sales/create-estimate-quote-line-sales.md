---
title: Proje tabanlı bir teklif satırını tahmin etme
description: Bu konuda, proje tabanlı teklif satırında nasıl tahmin oluşturulacağı hakkında bilgiler sağlanmaktadır.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 20a318c9f288b08a0984f9c29dced05997622f47
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003430"
---
# <a name="estimating-a-project-based-quote-line"></a>Proje tabanlı bir teklif satırını tahmin etme

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Proje tabanlı teklif satırında, teklif satırını teslim etmek için mevcut işin maliyetini ve potansiyel gelirini tahmin etmeye yardımcı olan ayrıntılar bulunur.

Proje tabanlı teklif satırını tahmin etmek için proje tabanlı teklif satırında **Teklif Satırı Ayrıntısı** sekmesini seçin. Proje tabanlı teklif satırında bir tahmin oluşturmanın iki yolu vardır:

- Teklif satırı ayrıntılarını kullanarak teklif satırında elle doğrudan teklif oluşturun. 
- Bir proje ve proje planı oluşturun ve ardından projeyi ve projedeki görevleri teklif satırıyla ilişkilendirin. Proje planındaki tahminleri sağladığınız bilgilere göre teklif satırında içeri aktarma işlemi etkinleştirilir.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Proje tabanlı teklif satırında doğrudan tahminler oluşturma

Proje tabanlı teklif satırında bir tahmin oluşturmak için **Teklif Satırı Ayrıntısı** sekmesini seçin. Bu sekmede oluşturduğunuz satır öğesi, bu teklif satırının teklif değerini özetler. 

Teklif satırı ayrıntıları oluşturmak için **Teklif Satırı Ayrıntıları** alt ızgarasında **Yeni Teklif Satırı Ayrıntısı**'nı seçin. Hızlı oluşturma kaydırıcısı açılır. Aşağıdaki tabloda, **Teklif Satırı Ayrıntısı** sayfasındaki alanlarla ilgili ayrıntılar ve değerlerin işlevselliği nasıl etkilediğiyle ilgili bilgiler yer alır.

| **Alan** | **Location** | **Açıklama** | **Aşağı yönlü etki** |
| --- | --- | --- | --- |
| Açıklama | Hızlı oluştur | Belirli bir tahminin açıklaması. | Bu değer, otomatik olarak oluşturulan maliyet için ilgili teklif satırı detaylarına varsayılan olarak alınır. |
| İşlem Sınıfı | Hızlı oluştur | Bu açılır liste, proje tabanlı teklif satırının **Genel** sekmesinde yer alan hareket sınıflarının bir listesini sağlar.  | Bu değer, otomatik olarak oluşturulan maliyet için ilgili teklif satırı detaylarına varsayılan olarak alınır. |
| Ürün Seç | Hızlı oluştur | Hareket sınıfı **Malzeme** olduğunda geçerlidir. Bu tahmin satırının, **Varolan** (katalog) bir ürün için mi **Serbest** bir ürün için mi olduğunu belirleyebilirsiniz. | Bu değer, otomatik olarak oluşturulan maliyet için ilgili teklif satırı detaylarına varsayılan olarak alınır. |
| Ürün | Hızlı oluştur | Ürün kataloğundan ürün kimliği. Bu alan, yalnızca **Ürün Seç** alanında **Varolan** öğesi seçilmişse etkinleştirilir. Kimlik, teklifteki proje fiyat listesinden satış fiyatını almak için kullanılır. | Bu değer, otomatik olarak oluşturulan maliyet için ilgili teklif satırı detaylarına varsayılan olarak alınır. |
| Serbest Eklenen Ürün | Hızlı oluştur | Ürünün adını yazmak için bir metin kutusu. Bu alan, yalnızca **Ürün Seç** alanında **Serbest** öğesi seçilirse etkinleştirilir.| Bu değer, otomatik olarak oluşturulan maliyet için ilgili teklif satırı detaylarına varsayılan olarak alınır. |
| Rol | Hızlı oluştur | Bu çalışmayı gerçekleştirecek veya bu gideri karşılayacak kişinin rolü. | Bu değer, otomatik olarak oluşturulan maliyet için ilgili teklif satırı detaylarına varsayılan olarak alınır. |
| Kategori | Hızlı oluştur | İş veya gider kategorisi. | Bu değer, otomatik olarak oluşturulan maliyet için ilgili teklif satırı detaylarına varsayılan olarak alınır. |
| Başlangıç Tarihi | Hızlı oluştur | İşin başlangıç tarihi. | Bu alan, otomatik olarak oluşturulan maliyet için teklif satırı ayrıntılarına varsayılan olarak alınır. |
| Bitiş Tarihi | Hızlı oluştur | İşin bitiş tarihi. | Bu alan, otomatik olarak oluşturulan maliyet için teklif satırı ayrıntılarına varsayılan olarak alınır. |
| Kaynak Belirleme Birimi | Hızlı oluştur | Bu maliyeti karşılayacak ve üzerinde çalışılması için kaynağı sağlayacak kaynak birimi. | Bu değer, otomatik olarak oluşturulan ve maliyet fiyatı almada kullanılan maliyet için ilgili teklif satırı detaylarına varsayılan olarak alınır. |
| Birim zamanlaması | Hızlı oluştur | İş, ürün veya giderin birim grubu. Birimler, bir birim zamanlamasına veya birim grubuna aittir. Örneğin, mil ve kilometre mesafeyi açıklayan bir birim grubuna ait birimlerdir. | Bu değer, otomatik olarak oluşturulan maliyet için ilgili teklif satırı detaylarına varsayılan olarak alınır. |
| Birim | Hızlı oluştur | İş, ürün veya giderin birimi. | Bu değer, otomatik olarak oluşturulan maliyet için ilgili teklif satırı detaylarına varsayılan olarak alınır. |
| Miktar | Hızlı oluştur | İş, ürün veya giderin miktarı. | Bu değer, otomatik olarak oluşturulan maliyet için ilgili teklif satırı detaylarına varsayılan olarak alınır. |
| Birim fiyatı | Hızlı Oluştur |Çalışmayı gerçekleştiren rolün fatura oranı, ürünün birim fiyatı veya ürün ya da gider kategorisinin satış fiyatı. Bu alan için varsayılan, başlangıç tarihi için geçerli proje fiyatı listesinin rol fiyatı satırında bulunan fiyatlandırma boyutu değerlerinin birleşimine dayanan **Zaman**'dır. **Giderler** için bu alanın varsayılan ayarı, proje fiyat listesindeki, başlangıç tarihi için geçerli olan hareket kategorisine yönelik fiyat kurulumundan alınır. Hareket kategorisinin fiyatlandırma yöntemi birim başına fiyat değilse varsayılan olmaz ve bu alan boş bırakılır. Ürünler için varsayılan, başlangıç tarihi için geçerli proje fiyat listesindeki **Fiyat listesi maddesi** satırına dayanır.| Çalışmayı gerçekleştiren rolün maliyet oranı, gider kategorisinin birim başına maliyeti veya ürünün birim maliyeti. Bu alan için varsayılan, başlangıç tarihi için geçerli proje fiyatı listesinin rol fiyatı satırında bulunan fiyatlandırma boyutu değerlerinin birleşimine dayanan **Zaman**'dır. **Giderler** için bu alanın varsayılan ayarı, proje fiyat listesindeki, başlangıç tarihi için geçerli olan hareket kategorisine yönelik fiyat kurulumundan alınır. Hareket kategorisinin fiyatlandırma yöntemi birim başına fiyat değilse varsayılan olmaz ve bu alan boş bırakılır. Ürünler için varsayılan, başlangıç tarihi için geçerli proje fiyat listesindeki **Fiyat listesi maddesi** satırına dayanır.|
| Tahmini Vergi | Hızlı oluştur | Bu iş veya gider için tahmini vergiyi el ile girebilirsiniz. | Bu alanda aşağı yönlü etki yoktur. |
| Miktar | Hızlı oluştur | **Miktar** ve **Fiyat** alanları boş bırakılırsa bilgileri bu alana el ile girebilirsiniz. Bu alanlar boş değilse bu alan salt okunur hale gelir ve (Miktar \* Birim fiyat) + Vergi olarak hesaplanır. | Bu alanda aşağı yönlü etki yoktur. |


## <a name="update-prices-on-quote-line-details"></a>Teklif satırı ayrıntılarında fiyatları güncelleştirme

Teklifle ilişkili proje fiyat listesindeki veya sözleşme biriminin maliyet fiyatı listesindeki fiyatları değiştirdiyseniz bu değişikliği yansıtmak üzere her bir teklif satırı ayrıntılarında fiyatları yenilemek için **Teklif** sayfasında **Yeniden hesapla**'yı seçebilirsiniz. **Yeniden hesapla**'yı seçtiğinizde, bu teklifteki tüm teklif satırlarıyla ilgili teklif satırı ayrıntılarının sıfırlanacağını bildiren bir uyarı görüntülenir. Satış ve maliyet teklif satırı ayrıntıları için fiyatları yenilemek üzere **Evet**'i seçin.

## <a name="access-quote-line-details-for-cost"></a>Maliyet için teklif satırı ayrıntılarına erişme

**Teklif satırı ayrıntıları** sekmesinde, alt kılavuzun araç çubuğunda bazı eylemleri etkinleştirmek için ızgarasında bir satır seçin. Teklif satırı ayrıntısı seçildiğinde alt ızgara araç çubuğundaki ilk eylem **Açık maliyet ayrıntısı** olur. Bu teklif satırı için ilgili maliyet oranını ve tutarı görmek üzere **Maliyet Ayrıntısını Aç**'ı seçin.

> [!NOTE]
> Maliyet için teklif satırı ayrıntısında kaynak birimi, miktar, tarihler, rol veya kategori değerlerinin değiştirilmesi, satışlar için teklif satırı ayrıntılarında karşılık gelen değerleri değiştirir.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Maliyet ve satışlar için teklif satırı ayrıntılarında para birimi

Teklif satırı ayrıntısının başlangıç tarihinde geçerli olan proje fiyat listesinden satış varsayılan değerleri için teklif satırı ayrıntısındaki para birimi.

Maliyet için teklif satırı ayrıntısının başlangıç tarihinde geçerli olan teklifin sözleşme biriminin fiyat listesinde maliyet varsayılan değerleri için teklif satırı ayrıntısındaki para birimi.

Karlılık hesaplamaları, teklifte genel tahmini kar marjını raporlamak üzere maliyet ve satışlar için teklif satırı ayrıntılarındaki tutarı ortamın temel para birimine dönüştürür.

> [!DİKKAT EDİN
> > Para birimi yuvarlama hataları ve değişen kenar boşlukları, etkili Döviz kurları olmadığı için oluşabilir. Bu hesaplamaları yalnızca proje sözleşmelerinde kullanın. Bunlar, yaklaşık değerler değildir veya döviz kurları için geçerlilik tarihinin yuvarlanması ve farkındalığına yönelik daha yüksek hassasiyet gerektiren gerçek bir meşru veya başka bir raporlama için değildir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
