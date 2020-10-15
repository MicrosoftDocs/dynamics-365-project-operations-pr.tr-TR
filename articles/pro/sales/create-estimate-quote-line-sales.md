---
title: Proje tabanlı bir teklif satırını tahmin etme
description: Bu konuda, proje tabanlı teklif satırında nasıl tahmin oluşturulacağı hakkında bilgiler sağlanmaktadır.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 65aee7238781ac90f603e57c6d9b0b92cabd6644
ms.sourcegitcommit: f6509f7d50de4d4ebb92c1bf2cfcdf09f17458eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/06/2020
ms.locfileid: "3966883"
---
# <a name="estimating-a-project-based-quote-line"></a>Proje tabanlı bir teklif satırını tahmin etme

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Proje tabanlı teklif satırında, teklif satırını teslim etmek için mevcut işin maliyetini ve potansiyel gelirini tahmin etmeye yardımcı olan ayrıntılar bulunur.

Proje tabanlı teklif satırını tahmin etmek için proje tabanlı teklif satırında **Teklif Satırı Ayrıntısı** sekmesini seçin. Proje tabanlı teklif satırında bir tahmin oluşturmanın iki yolu vardır:

- Teklif satırı ayrıntılarını kullanarak teklif satırında elle doğrudan teklif oluşturma 
- Bir proje ve proje planı oluşturun ve ardından projeyi ve projedeki görevleri teklif satırıyla ilişkilendirin. Proje planındaki tahminleri sağladığınız bilgilere göre teklif satırında içeri aktarma işlemi etkinleştirilir.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Proje tabanlı teklif satırında doğrudan tahminler oluşturma

Proje tabanlı teklif satırında bir tahmin oluşturmak için **Teklif Satırı Ayrıntısı** sekmesini seçin. Bu sekmede oluşturduğunuz satır öğesi, bu teklif satırının teklif değerini özetler. 

Teklif satırı ayrıntıları oluşturmak için **Teklif Satırı Ayrıntıları** alt ızgarasında **+ Yeni teklif satırı ayrıntısı**'nı seçin. Hızlı oluşturma kaydırıcısı açılır. **Teklif Satırı** formunda aşağıdaki alanlar:

| **Alan** | **Konum** | **İlgi, amaç ve kılavuz** | **Aşağı yönlü etki** |
| --- | --- | --- | --- |
| Veri Akışı Açıklaması | Hızlı oluştur | Belirli bir tahminin açıklaması. | Bu alan, otomatik olarak oluşturulan maliyetin ilgili teklif satırı ayrıntısı için varsayılan değerdir. |
| İşlem Sınıfı | Hızlı oluştur | Bu açılan listede, proje tabanlı teklif satırının **Genel** sekmesine dahil edilen işlem sınıfları sağlanır.  | Bu alan, otomatik olarak oluşturulan maliyetin ilgili teklif satırı ayrıntısı için varsayılan değerdir. |
| Rol | Hızlı oluştur | Bu işi gerçekleştirecek veya bu gideri üstlenecek kişi. | Bu alan, otomatik olarak oluşturulan maliyetin ilgili teklif satırı ayrıntısı için varsayılan değerdir. |
| Kategori | Hızlı oluştur | İş veya giderin kategorisi. | Bu alan, otomatik olarak oluşturulan maliyetin ilgili teklif satırı ayrıntısı için varsayılan değerdir. |
| Başlangıç Tarihi | Hızlı oluştur | İşin başlangıç tarihi. | Bu alan, otomatik olarak oluşturulan maliyetin ilgili teklif satırı ayrıntısı için varsayılan değerdir. |
| Bitiş Tarihi | Hızlı oluştur | İşin bitiş tarihi. | Bu alan, otomatik olarak oluşturulan maliyetin ilgili teklif satırı ayrıntısı için varsayılan değerdir. |
| Kaynak Belirleme Birimi | Hızlı oluştur | Bu maliyeti üstlenecek ve üzerinde çalışılacak kaynağı sağlayacak kaynak belirleme birimi. | Bu alan, otomatik olarak oluşturulan maliyetin ilgili teklif satırı ayrıntısı için varsayılan değerdir. Bu alan, maliyet fiyatı alma işleminde de kullanılır. |
| Birim zamanlaması | Hızlı oluştur | İş veya giderin birim grubu. Birimler, bir birim zamanlamasına veya birim grubuna aittir. Örneğin, Mil ve KM'ler, mesafeyi tanımlayan bir birim grubuna ait birimlerdir. | Bu alan, otomatik olarak oluşturulan maliyetin ilgili teklif satırı ayrıntısı için varsayılan değerdir. |
| Birim | Hızlı oluştur | İş veya giderin birimi. | Bu alan, otomatik olarak oluşturulan maliyetin ilgili teklif satırı ayrıntısı için varsayılan değerdir. |
| Miktar | Hızlı oluştur | İş veya giderin miktarı | Bu alan, otomatik olarak oluşturulan maliyetin ilgili teklif satırı ayrıntısı için varsayılan değerdir. |
| Birim fiyatı | Hızlı oluştur | İşi gerçekleştiren rolün fatura oranı veya gider kategorisinin Satış fiyatı. Bu alan, başlangıç tarihinde geçerli olan proje fiyat listesinde rol ve kaynak birimi birleşimine göre Zaman için varsayılan değerdir. Giderler için bu alan, başlangıç tarihinde geçerli olan proje fiyat listesinde işlem kategorisinin fiyat ayarında varsayılan değerdir. İşlem kategorisi için fiyatlandırma yöntemi, birim başına fiyat değilse varsayılan değer yoktur ve bu alan boş bırakılır. | İşi gerçekleştiren rolün maliyet oranı veya gider kategorisinin birim başına maliyeti. Bu alan, başlangıç tarihinde geçerli olan Teklif fiyat listesinin Sözleşme biriminin fiyatında rol ve kaynak birimi birleşimine göre Zaman için varsayılan değerdir. Giderler için bu alan, başlangıç tarihinde geçerli olan Sözleşme biriminin maliyet fiyatı listesinde işlem kategorisinin fiyat ayarında varsayılan değerdir. İşlem kategorisi için fiyatlandırma yöntemi, birim başına fiyat değilse varsayılan değer yoktur ve bu alan boş bırakılır. |
| Tahmini Vergi | Hızlı oluştur | Bu iş veya gider için tahmini vergiyi el ile girebilirsiniz. | Bu alanda aşağı yönlü etki yoktur. |
| Miktar | Hızlı oluştur | **Miktar** ve **Fiyat** alanları boş bırakılırsa bilgileri bu alana el ile girebilirsiniz. Bu alanlar boş değilse bu alan salt okunur hale gelir ve (Miktar \* Birim fiyat) + Vergi olarak hesaplanır. | Bu alanda aşağı yönlü etki yoktur. |

## <a name="update-prices-on-quote-line-details"></a>Teklif satırı ayrıntılarında fiyatları güncelleştirme

Teklife ekli proje fiyat listesinde veya sözleşme biriminin maliyet fiyatı listesinde fiyatları değiştirdiyseniz bu değişikliği yansıtmak üzere tek tek teklif satırı ayrıntılarındaki fiyatları yenilemek için **Teklif** sayfasında **Yeniden Hesapla** seçeneğini belirleyebilirsiniz. **Yeniden Hesapla** seçeneğini belirlediğinizde, bu teklifteki tüm teklif satırları için teklif satırı ayrıntılarındaki fiyatların sıfırlanacağını bildiren bir uyarı oluşur. Satış ve maliyet teklif satırı ayrıntıları için fiyatları yenilemek üzere **Evet**'i seçin.

## <a name="access-quote-line-details-for-cost"></a>Maliyet için teklif satırı ayrıntılarına erişme

**Teklif Satırı Ayrıntıları** sekmesinde, alt ızgaranın araç çubuğunda bazı eylemleri etkinleştirmek için ızgarada bir satır seçin. Teklif satırı ayrıntısı seçildiğinde alt ızgara araç çubuğundaki ilk eylem **Maliyet Ayrıntısını Aç** seçeneğidir. Bu teklif satırı için ilgili maliyet oranını ve tutarı görmek üzere **Maliyet Ayrıntısını Aç**'ı seçin.

> [!NOTE]
> Maliyet için teklif satırı ayrıntısında kaynak birimi, miktar, tarihler, rol veya kategori değerlerinin değiştirilmesi, satışlar için teklif satırı ayrıntılarında karşılık gelen değerleri değiştirir.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Maliyet ve satışlar için teklif satırı ayrıntılarında para birimi

Teklif satırı ayrıntısının başlangıç tarihinde geçerli olan proje fiyat listesinden satış varsayılan değerleri için teklif satırı ayrıntısındaki para birimi.

Maliyet için teklif satırı ayrıntısının başlangıç tarihinde geçerli olan teklifin sözleşme biriminin fiyat listesinde maliyet varsayılan değerleri için teklif satırı ayrıntısındaki para birimi.

Karlılık hesaplamaları, teklifte genel tahmini kar marjını raporlamak üzere maliyet ve satışlar için teklif satırı ayrıntılarındaki tutarı ortamın temel para birimine dönüştürür.

Bu, güncel döviz kurlarının bulunmaması nedeniyle para birimi yuvarlama hatalarına ve değişen kar marjlarına neden olabilir. Bu hesaplamaları, Proje tekliflerinde yalnızca yaklaşık değerler olarak kullanın ve daha yüksek yuvarlama duyarlılığı ve güncel döviz kurlarının bilinmesini gerektiren gerçek yasal veya diğer raporları kullanmayın.
