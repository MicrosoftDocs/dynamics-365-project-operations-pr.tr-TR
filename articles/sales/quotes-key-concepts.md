---
title: Proje tabanlı tekliflere özel kavramlar
description: Bu makalede, Microsoft Dynamics 365 Project Operations'ta proje teklifleri hakkında bilgiler yer almaktadır.
author: rumant
ms.date: 12/02/2022
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 89867cfbe92f47d58b16da40b62d3d9dd6a15b64
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824376"
---
# <a name="concepts-unique-to-project-based-quotes"></a>Proje tabanlı tekliflere özel kavramlar

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Microsoft Dynamics 365 Project Operations'ta proje tekliflerini kullanmaya başlamadan önce aşağıdaki temel kavramları bilmeniz gerekir:

## <a name="owning-company"></a>Sahibi olan şirket

Sahibi olan şirket, proje tesliminin sahibi olan tüzel kişiliği ifade eder. Teklifteki müşteri, finans ve operasyon uygulamalarında bu tüzel kişilikte geçerli bir müşteri olmalıdır. Sahibi olan şirketin para birimi ve proje tabanlı teklifte seçilen sözleşmeli biriminin para birimi eşleşmelidir.

## <a name="contracting-unit"></a>Sözleşme birimi

Sözleşmeli birim, proje teslimatının sahibi olan bölümü veya uygulamayı temsil eder. Her sözleşme birimi için kaynak maliyetlerini ayarlayabilirsiniz. Sözleşme biriminde bir kaynak için kaynak maliyetlerini belirttiğinizde, sözleşmeli birimin veya kuruluş içindeki diğer bölümlerin veya uygulamaların ödünç aldığı kaynaklar için farklı maliyet oranları ayarlayabilirsiniz. Bu maliyet oranları transfer fiyatları, kaynak ödünç alma veya değişim fiyatları olarak adlandırılır. Diğer bölümlerden kaynak ödünç alma maliyetini ayarladığınızda, bu maliyet oranlarını ödünç veren bölümün para birimi cinsinden ayarlayabilirsiniz.

## <a name="cost-currency"></a>Maliyet para birimi

Project Operations'taki maliyet para birimi, maliyetlerin raporlandığı para birimidir. Bu para birimi; teklif, sözleşme ve projenin **Sözleşme birimi** alanına iliştirilmiş para biriminden alınır. Maliyetler bir projeye göre herhangi bir para biriminde kaydedilebilir. Ancak maliyetlerin kaydedildiği para birimi, projenin maliyet para birimine dönüştürülür.

Dataverse platformundaki döviz kurları güncel olamadığından, ekrandaki toplam maliyetler para birimi döviz kurlarını güncelleştirdiğinizde zaman içinde değişebilir. Bununla birlikte, tutarlar oluştukları para birimi cinsinden saklandığından, veritabanına kaydedilen maliyetler değişmez.

## <a name="sales-currency"></a>Satış para birimi

Project Operations'taki satış para birimi, tahmini ve gerçek satış tutarlarının kaydedildiği ve gösterildiği para birimidir. Aynı zamanda, müşterinin anlaşma için faturalandığı para birimidir. Proje teklifi için, varsayılan satış para birimi müşteri veya firma kaydındaki değerden ayarlanır ve teklif oluşturulduğunda değiştirilebilir. Bununla birlikte satış para birimi teklif kaydedildikten sonra değiştirilemez. Varsayılan ürün ve proje fiyat listeleri teklifin satış para birimine göre ayarlanır.

Maliyetlerin aksine, satış değerleri **yalnızca** Satış para birimi cinsinden kaydedilebilir.

## <a name="billing-method"></a>Faturalama yöntemi

Projelerin genellikle sabit ücretli ve tüketim tabanlı sözleşme modelleri vardır. Project Operations'ta, projenin sözleşme modeli faturalandırma yöntemiyle temsil edilir. Faturalama yönteminde iki değer vardır: zaman ve malzeme ve sabit fiyat.

- **Zaman ve malzeme:** Oluşan her maliyetin karşılığında bir gelir olan tüketim tabanlı bir sözleşme modelidir. Daha fazla maliyet oluşacağını tahmin ederseniz veya daha fazla maliyet oluşursa ilgili tahmini ve gerçek satışlar da artar. Bu faturalama yöntemine sahip teklif satırlarında aşılamaz limitler belirtebilirsiniz. Bu şekilde, fiili geliri geçebilirsiniz. Tahmini gelir aşılamaz limitlerden etkilenmez.
- **Sabit Fiyat:** Satış değerlerinin oluşan maliyetlerden bağımsız olduğu sabit fiyatlı bir sözleşme modelidir. Satış değeri sabittir ve daha fazla maliyet tahmini ya da gerçekleşmesi olduğunda değişmez.

## <a name="project-price-lists"></a>Proje fiyat listeleri

Proje fiyat listeleri; zaman, gider ve projeyle ilgili diğer bileşenlerin maliyet oranlarını değil varsayılan fiyatlarını girmek için kullanılan fiyat listeleridir. Birden çok fiyat listesi olabilir. Her listenin, her proje teklifinin kendi tarih geçerliliği olabilir. Project Operations, proje fiyat listeleri için çakışan geçerlilik tarihlerini desteklemez.

## <a name="product-price-lists"></a>Ürün fiyat listeleri

Ürün fiyat listeleri, teklifteki ürün tabanlı satırların maliyet oranlarını değil varsayılan fiyatlarını girmek için kullanılan fiyat listeleridir. Her teklif için yalnızca bir fiyat listesi vardır.

## <a name="transaction-classes"></a>İşlem sınıfları

Project Operations dört işlem sınıfı türünü destekler:

- Zaman
- Gider
- Malzeme
- Ücret

Maliyet ve satış değerleri; **Zaman**, **Gider** ve **Malzeme** işlem sınıflarında tahmin edilebilir ve oluşabilir. **Ücret** yalnızca gelir işlem sınıfına dahil olabilir.

## <a name="work-entities-and-billing-entities"></a>İş varlıkları ve faturalama varlıkları

Projeler ve Görevler işi temsil eden varlıklardır. Teklif satırları ve Sözleşme satırları faturayı temsil eden varlıklardır. Farklı iş varlıklarını, Teklif satırları veya Sözleşme satırlarıyla ilişkilendirerek faturalama seçeneklerine bağlayabilirsiniz.

## <a name="multi-customer-deals"></a>Çok müşterili anlaşmalar

Çok müşterili anlaşmalar, fatura başına birden çok müşteri olduğunda gerçekleşir. Bazı tipik örnekleri aşağıda bulabilirsiniz:

- **Orijinal ekipman üreticisi (OEM) kuruluşlar ve bunların iş ortakları:** İş ortakları ve satıcılar, katma değerli hizmetler içeren bir ürün satarlar. Müşteriyle yapılan bir anlaşma sırasında OEM genellikle projenin bir kısmını finanse etmeyi teklif eder.
- **Kamu sektörü projeleri:** Yerel hükümetin birden çok bölümü bir projeyi fonlamayı kabul eder ve önceden kabul edilen paylara göre faturalandırılırlar. Örneğin, bir okul bölgesi ve şehir ya da yerel kamu dairesi, bir yüzme havuzu inşaatını fonlamayı kabul eder.

## <a name="invoice-schedules"></a>Fatura zamanlamaları

Fatura zamanlamaları, her teklif satırına özeldir ve isteğe bağlıdır. Fatura zamanlamaları, belirli başlangıç ve bitiş tarihlerine ve fatura sıklığına göre oluşturulur. Otomatik fatura oluşturma işlemi yapılandırıldığında sözleşme aşamasında kullanılırlar. Teklif aşamasında, fatura zamanlamaları isteğe bağlıdır. Fatura zamanlamaları teklif aşamasında oluşturulduğunda, bir proje teklifi kazanıldığında oluşturulan proje sözleşmesine kopyalanır.

## <a name="differences-from-dynamics-365-sales-quotes"></a>Dynamics 365 Sales tekliflerinden farkları

Project Operations teklifleri, Dynamics 365 Sales tekliflerini temel alarak oluşturulur. Ancak işlevselliğinde bilmeniz gereken bazı önemli farklılıklar bulunmaktadır:

- Project Operations teklifleri, biri projeler, diğeri ürünler için olmak üzere iki farklı türde satıra sahiptir.
- Project Operations teklifleri kendi sayfa ve kullanıcı arabirimi (UI) öğelerine, iş kurallarına, eklentilerdeki iş mantığına ve Sales tekliflerine göre benzersiz kılan istemci tarafı komut dosyalarına sahiptir.
- Sales'te tek bir satış teklifine birden fazla sipariş ekleyebilirsiniz. Project Operations'ta bir proje teklifine yalnızca bir proje sözleşmesi ekleyebilirsiniz.
- Bir satış teklifini kazandığınızda, ilgili fırsat açık kalabilir. Bir proje teklifi kazandıktan sonra, ilgili fırsat kapanır.
- Bir satış teklifi, bir proje teklifine dahil olan bazı alanları ve kavramları içermez. Alanlar arasında **Sözleşme Birimi**, **Hesap Yöneticisi** ve **Fatura İlgili Kişi Adı** bulunur.
- Satış teklifleri ve proje teklifleri seçenek kümesi tabanlı **Tür** alanıyla tanımlanır. Satış teklifi için, bu alanın değeri **Öğe-tabanlı**'dır. Proje teklifi için, değer **İş-tabanlı**'dır.

Bu farklardan dolayı, Sales ve Project Operations tekliflerini birbirinin yerine kullanmamanızı öneririz.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
