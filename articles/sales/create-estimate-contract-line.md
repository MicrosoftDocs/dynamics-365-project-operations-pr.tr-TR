---
title: Proje tabanlı sözleşme satırını tahmin etme
description: Bu konu proje tabanlı bir sözleşme satırını tahmin etme hakkında bilgi sağlar.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cdc8984e080d995e3a0b667fe662291b499235b2
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278532"
---
# <a name="estimate-a-projectbased-contract-line"></a>Proje tabanlı sözleşme satırını tahmin etme

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_ 

Dynamics 365 Project Operations'ta proje tabanlı bir sözleşme satırı, sözleşme satırını teslim etmek için ilgili çalışmanın maliyet ve potansiyel gelirini tahmin etmenize yardımcı olan ayrıntılar içerir.

Proje tabanlı bir sözleşme satırını tahmin etmek için Proje tabanlı **sözleşme satırındaki** **Sözleşme satırı Ayrıntıları** sekmesine gidin.  Proje tabanlı bir sözleşme satırında tahmin oluşturmanın iki yolu vardır:

   - Sözleşme satırı ayrıntılarını el ile ekleyerek doğrudan sözleşme satırında bir tahmin oluşturun.
   - Bir proje ve proje planı oluşturun ve ardından projeyi ve görevleri projenin sözleşme satırıyla ilişkilendirin. Bu, sözleşme satırında yer alan bileşenlere dayalı olarak, proje planı tahminini sözleşme satırına içe aktarmaka için kullanılacak süreci sağlar.

## <a name="create-an-estimate-directly-on-a-projectbased-contract-line"></a>Proje tabanlı sözleşme satırında doğrudan tahmin oluşturma

1. Sözleşme satırına gidin ve **sözleşme satırı ayrıntıları** sekmesini seçin. Bu sekmede oluşturduğunuz satırlar özetlenir ve Bu **sözleşme satırı** için **anlaşmalı değer** olarak görüntülenir. 
2. **Sözleşme satırı ayrıntıları** alt ızgarasında, **+ yeni sözleşme satırı ayrıntısı**'nı seçin. Hızlı oluşturma kaydırıcısı açılır. **Sözleşme satırı ayrıntıları** formunda aşağıdaki alanlar kullanılabilir:

| Alan | Konum | Veri Akışı Açıklaması | Aşağı yönlü etki |
| --- | --- | --- | --- |
| **Açıklama** | **Hızlı Oluştur** | Belirli bir tahminin açıklaması. | Bu alan, otomatik olarak oluşturulan maliyetlerin ilgili sözleşme satırı ayrıntılarını varsayılan olarak belirler. |
| **İşlem Sınıfı** | **Hızlı Oluştur** | Bu açılan liste, Proje tabanlı sözleşme satırının **Genel** sekmesinde yer alan bir hareket sınıfları listesidir. | Bu alan, otomatik olarak oluşturulan maliyetlerin ilgili sözleşme satırı ayrıntılarını varsayılan olarak belirler. |
| **Rol** | **Hızlı Oluştur** | Bu işi gerçekleştiren veya bu gideri ortaya alan kişinin rolü. | Bu alan, otomatik olarak oluşturulan maliyetlerin ilgili sözleşme satırı ayrıntılarını varsayılan olarak belirler. |
| **Kategori** | **Hızlı Oluştur** | İş veya gider kategorisi. | Bu alan, otomatik olarak oluşturulan maliyetlerin ilgili sözleşme satırı ayrıntılarını varsayılan olarak belirler. |
| **Başlangıç Tarihi** | **Hızlı Oluştur** | İşin başlangıç tarihi. | Bu alan, otomatik olarak oluşturulan maliyetlerin ilgili sözleşme satırı ayrıntılarını varsayılan olarak belirler. |
| **Bitiş Tarihi** | **Hızlı Oluştur** | İşin bitiş tarihi. | Bu alan, otomatik olarak oluşturulan maliyetlerin ilgili sözleşme satırı ayrıntılarını varsayılan olarak belirler. |
| **Kaynak Atayan Şirket** | **Hızlı Oluştur** | Bu maliyeti ortaya alan ve üzerinde çalışmak üzere kaynağı sağlayan kaynak veya tüzel kişilimcilik şirketi. | Bu alan, otomatik olarak oluşturulan maliyetlerin ilgili sözleşme satırı ayrıntılarını varsayılan olarak belirler. Bu alan, maliyet fiyatı alma işleminde de kullanılır. |
| **Kaynak Belirleme Birimi** | **Hızlı Oluştur** | Bu maliyeti yeniden veren ve kaynağın üzerinde çalışmasını sağlamak için kaynağı provies kaynak birim. | Bu alan, otomatik olarak oluşturulan maliyetlerin ilgili sözleşme satırı ayrıntılarını varsayılan olarak belirler. Bu alan, maliyet fiyatı alma işleminde de kullanılır. |
| **Birim zamanlaması** | **Hızlı oluştur** | Çalışmanın veya giderin birim grubu. Birimler, bir birim zamanlamasına veya birim grubuna aittir. Örneğin, *mil* ve *kilometre (KMS)* mesafeyi açıklayan bir birim grubuna ait birimlerdir. | Bu alan, otomatik olarak oluşturulan maliyetlerin ilgili sözleşme satırı ayrıntılarını varsayılan olarak belirler. |
| **Birim** | **Hızlı Oluştur** | Çalışmanın veya giderin birimi. | Bu alan, otomatik olarak oluşturulan maliyetlerin ilgili sözleşme satırı ayrıntılarını varsayılan olarak belirler. |
| **Miktar** | **Hızlı Oluştur** | Çalışmanın veya giderin miktarı. | Bu alan, otomatik olarak oluşturulan maliyetlerin ilgili sözleşme satırı ayrıntılarını varsayılan olarak belirler. |
| **Birim fiyatı** | **Hızlı Oluştur** | Çalışmayı gerçekleştiren rolün fatura kuru veya gider kategorisinin satış fiyatı. Bu alan, başlangıç tarihinde geçerli olan proje fiyat listesinde rol ve kaynak birimi birleşimine göre **Zaman** için varsayılan değerdir. Giderler için bu alanın varsayılan ayarı, proje fiyat listesindeki, başlangıç tarihi için geçerli olan hareket kategorisine yönelik fiyat kurulumundan alınır. İşlem kategorisi için fiyatlandırma yöntemi, **birim başına fiyat** değilse varsayılan değer yoktur ve bu alan boş bırakılır. | Çalışmayı gerçekleştiren rolün maliyet kuru veya gider kategorisinin birim başına maliyeti. Bu alan, Başlangıç tarihi için geçerli olan sözleşme birimine iliştirilmiş maliyet fiyatı listesinin rol fiyatı satırındaki **zamana bağlı role** ve kaynak birim birleşimine göre farklılık gösterir. Giderler için bu alanın varsayılan ayarı, başlangıç tarihi için geçerli olan sözleşme birimine ekli olan maliyet fiyat listesinin kategori fiyat satırına bağlıdır. İşlem kategorisi için fiyatlandırma yöntemi, birim başına fiyat değilse varsayılan değer yoktur ve bu alan boş bırakılır. |
| **Tahmini Vergi** | **Hızlı Oluştur** | Bu iş veya gider için tahmini vergi, kullanıcı tarafından girildiği şekilde. | Bu iş veya gider için tahmini vergi, kullanıcı tarafından girildiği şekilde. |
| **Tutar** | **Hızlı Oluştur** | **Miktar** ve **Fiyat** alanları boş bırakılmışsa, bu alandaki bu değer Kullanıcı tarafından eklenebilir. **Miktar** ve **Fiyat** doldurulmuşsa **tutar** alanı salt okunurdur ve **(miktar \* birim fiyatı) + vergi** olarak hesaplanır. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Sözleşme satırı ayrıntılarında fiyatları güncelleştir

Sözleşmeye iliştirilen proje fiyat listesindeki fiyatları veya sözleşme biriminin maliyet fiyatı listesini değiştirirseniz, değişikliği yansıtmak için her sözleşme satırı ayrıntılarında fiyatları yenileyebilirsiniz. **Sözleşme** sayfasında **Yeniden hesapla**'yı seçin. Size bu sözleşmedeki tüm sözleşme satırları için fiyatların sıfırlandığını bildiren bir uyarı açılır. Satış ve maliyet sözleşme satırı ayrıntılarının her ikisi için de fiyatları yenilemek üzere **Evet**'i seçin.

## <a name="access-contract-line-details-for-cost"></a>Maliyet erişim sözleşmesi satır ayrıntıları

**Sözleşme satırı ayrıntıları** sekmesinde, alt kılavuzun araç çubuğunda bazı eylemleri etkinleştirmek için ızgarasında bir satır seçin. Alt kılavuz araç çubuğundaki ilk eylem **Açık maliyet ayrıntısı**'dır. Bu sözleşme satırı ayrıntısı için ilgili maliyet oranını ve tutarı görmek için **Açık maliyet ayrıntısı**'nı seçin. 

> [!NOTE]
> **Maliyet** için kaynak şirketi, kaynak birim, miktar, tarih, rol veya sözleşme satırı ayrıntısı üzerinde kategori değerlerini değiştirmek **Satış** için ilgili sözleşme satırı ayrıntısının karşılık gelen değerlerini de değiştirir.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Sözleşme satırındaki para birimi maliyet ve satış ayrıntıları

**Satışlar** için sözleşme satırı ayrıntısı Proje Fiyat listesinden, sözleşme satırı ayrıntısı başlangıç tarihi için geçerli olan varsayılan para birimini ayarlar.

**Maliyet** için sözleşme satırı ayrıntısı sözleşmenin sözleşme birimi Fiyat listesinden, **Maliyet** için sözleşme satırı ayrıntısı başlangıç tarihi için geçerli olan varsayılan para birimini ayarlar.

Karlılık hesaplamaları, **Maliyet** ve **Satış** için sözleşme satırı ayrıntılarının tutarlarını, sözleşmenin genel gerçek ve tahmini kenar boşluklarını raporlamak için ortamın temel para birimine dönüştürür.

> [!NOTE]
> Para birimi yuvarlama hataları ve değişen kenar boşlukları, etkili Döviz kurları olmadığı için oluşabilir. Bu hesaplamaları yalnızca proje sözleşmelerinde, Döviz kurları tarihinin yuvarlanması ve kullanımı için daha yüksek hassasiyet gerektiren gerçek bir yasal veya başka bir raporlama için kullanın.


[!INCLUDE[footer-include](../includes/footer-banner.md)]