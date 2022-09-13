---
title: Proje tabanlı sözleşmeleri kopyalama
description: Bu makalede, Microsoft Dynamics 365 Project Operations'ta proje sözleşmelerini kopyalama hakkında bilgiler yer almaktadır.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 21994ef6d8f6e6cdf321599d107cc80368c96ecc
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410343"
---
# <a name="copy-project-based-contracts"></a>Proje tabanlı sözleşmeleri kopyalama

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Varolan sözleşmeleri şu iki yöntemden biriyle kopyalayarak kolayca yeni proje sözleşmeleri oluşturabilirsiniz:

- **Proje Sözleşmeleri** listesi sayfasında bir proje sözleşmesi açın ve sonra **Kopyala**'yı seçin.
- **Proje Sözleşmesi** ayrıntıları sayfasında **Kopyala**'yı seçin.

Her iki durumda, kopyalanan sözleşmenin parametrelerini seçebileceğiniz iletişim kutusu görünür. İletişim kutusu aşağıdaki alanları içerir. Seçtiğiniz değerlere bağlı olarak kopyalama işlemi değişebilir.

| Alan | Tanım | Aşağı yönlü etki |
| --- | --- | --- |
| Başlık | Hedef Sözleşmenin konusunu girin. İletişim kutusu açıldığında sistem bu alanı, "kopya" ifadesi eklenmiş olarak kaynak sözleşmesinin adına ayarlar. | Bu alanda aşağı yönlü etki yoktur. |
| Customer | Müşterinin şirket veya firma kaydına başvuru. İletişim kutusu açıldığında sistem bu alanı kaynak sözleşmesindeki firma olarak ayarlar. | Bu alan, sözleşmedeki birincil müşteridir. |
| Sahibi Olan Şirket | Bu anlaşmayla ilişkili projelerin tesliminden sorumlu olan şirket. İletişim kutusu açıldığında sistem bu alanı kaynak sözleşmesindeki sahip olan şirket olarak ayarlar. | Sahip olan şirket, anlaşma yapıldıktan sonra projeyi yürüten tüzel kişilik olur. Sahip olan şirketin para birimi, sözleşme yapan birimin para birimiyle eşleşmelidir. |
| Sözleşme Birimi | Bu anlaşmayla ilişkili projelerin tesliminden sorumlu olan kuruluş birimi. İletişim kutusu açıldığında sistem bu alanı kaynak sözleşmesinin sözleşme yapan birimi olarak ayarlar. | Sözleşme yapan birim, şirketin anlaşma kapatıldıktan sonra projeleri yürüten bölümüdür. Sözleşme yapan her biriminin bir para birimi vardır. Bu para birimi, proje sırasında oluşan tahmini ve gerçek maliyetleri bildirmek için kullanılır. |
| Currency | Anlaşmanın işlem gördüğü para birimidir. İletişim kutusu açıldığında sistem, alanı kaynak sözleşmedeki para birimi olarak ayarlar. Para birimi değiştirilemiyor. Böyleyse kaynak sözleşmedeki fiyat listeleri artık alakalı olmadığından, **Kopyalama Fiyatlandırması** alanı her zaman **Hayır** olarak ayarlanır. | Bu para birimi, varsayılan fiyat listeleri için, sözleşme üzerine mali tahminler oluşturmak ve anlaşma kazanıldığında müşteriye fatura kesmek için kullanılır. |
| Talep Edilen Teslimat Tarihi | Müşteri tarafından istenen teslim tarihi. | Bu tarih, belirli bir sıklıkta faturalama tarihleri oluştururken bitiş tarihi olarak kullanılır. |
| Fiyatlandırmayı kopyala | Sözleşme üzerindeki fiyatlandırmanın kaynak sözleşmeden kopyalanması gerekip gerekmediğini gösteren bir değer. | Alan **Evet** olarak seçilirse proje fiyat listesi ve ürün fiyat listesi başvuruları kaynak sözleşmeden hedef sözleşmeye kopyalanır. **Hayır** olarak ayarlanırsa varsayılan fiyat listeleri, firma veya proje parametrelerindeki en son fiyat listelerine göre kullanılır. |

İletişim kutusunda **Tamam**'ı seçtiğinizde sistem, ayarladığınız parametre değerlerine göre sözleşmenin bir kopyasını oluşturur. Ardından yeni sözleşme açılır.

Her sözleşmeye özel olduğu için, aşağıdaki bilgiler kaynak sözleşmeden hedef sözleşmeye **kopyalanmaz**:

- Fatura zamanlamaları
- Sözleşme ve sözleşme satırı müşterileri
- Proje tabanlı sözleşme satırlarında proje başvurusu
- Müşteri bütçe bilgileri

Projeler ve ürünler için sözleşme satırları, sözleşme satırı ayrıntılarına ilişkin tahminler ve sözleşme düzeyinde aşılamaz değerler kopyalanır. Varsayılan fiyatlar ve maliyet oranlarının girişi, **Parametreleri Kopyala** iletişim kutusundaki **Fiyatlandırmayı kopyala** alanında yapılan seçime bağlıdır.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
