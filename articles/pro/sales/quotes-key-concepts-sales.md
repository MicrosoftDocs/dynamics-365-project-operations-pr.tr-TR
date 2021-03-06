---
title: Proje teklifi temel kavramları
description: Bu konuda, Project Operations'ta proje tekliflerinin kullanılması hakkında bilgiler sağlanmaktadır.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 64d2fd9bab9452d71e8cd194fbab70edadf00b93
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896305"
---
# <a name="project-quote-key-concepts"></a>Proje teklifi temel kavramları

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_


Dynamics 365 Project Operations'ta proje tekliflerini kullanmaya başlamadan önce dikkat edilecek temel kavramlar aşağıda verilmiştir:

## <a name="contracting-unit"></a>Sözleşme birimi

Sözleşme birimi, proje teslimatının sahibi olan bölümü veya uygulamayı temsil eder. Her sözleşme birimi için kaynak maliyetlerini ayarlayabilirsiniz. Sözleşme biriminde bir kaynak için kaynak maliyetini belirttiğinizde, bu sözleşme biriminin veya kuruluş içindeki diğer bölümlerin veya uygulamaların ödünç aldığı kaynaklar için de farklı maliyet oranları ayarlayabilirsiniz. Bunlar transfer fiyatları, kaynak ödünç alma veya değişim fiyatları olarak adlandırılır. Diğer bölümlerden kaynak ödünç alma maliyetini ayarladığınızda, bu maliyet oranlarını ödünç veren bölümün para birimi cinsinden ayarlamayı da seçebilirsiniz.

## <a name="cost-currency"></a>Maliyet para birimi

Project Operations'taki maliyet para birimi, maliyetlerin raporlandığı para birimidir. Bu para birimi; teklif, sözleşme ve projenin **Sözleşme birimi** alanına iliştirilmiş para biriminden alınır. Maliyetler bir projeye göre herhangi bir para birimine kaydedilebilir. Ancak maliyetlerin kaydedildiği para birimi, projenin maliyet para birimine dönüştürülür.

CDS platformundaki döviz kurları güncel olamadığından, ekrandaki toplam maliyetler para birimi döviz kurlarını güncelleştirdiğinizde zaman içinde değişebilir. Bununla birlikte, tutarlar oluştukları para birimi cinsinden saklandığından, veritabanına kaydedilen maliyetler değişmez.

## <a name="sales-currency"></a>Satış para birimi

Project Operations'taki satış para birimi, tahmini ve gerçek satış tutarlarının kaydedildiği ve gösterildiği para birimidir. Aynı zamanda, müşterinin anlaşma için faturalandığı para birimidir. Proje teklifinde, satış para birimi varsayılan olarak müşteri veya firma kaydındaki değere ayarlanır ve teklif oluşturulduğunda değiştirilebilir. Teklif kaydedildikten sonra, satış para birimi değiştirilemez. Ürün ve proje fiyat listelerinin varsayılan değeri teklifin satış para birimine göre ayarlanır.

Maliyetlerin aksine, satış değerleri yalnızca Satış para birimi cinsinden kaydedilebilir.

## <a name="billing-method"></a>Faturalama yöntemi

Projelerin genellikle sabit ücretli ve tüketim tabanlı sözleşme modelleri vardır. Bu, Project Operations'ta **Faturalama Yöntemi** olarak temsil edilir. Zaman ve malzeme ve sabit fiyat olmak üzere iki değeri vardır.

- **Zaman ve malzeme:** Bu, oluşan her maliyetin karşılığında bir gelir olan tüketim tabanlı bir sözleşme modelidir. Daha fazla maliyet oluşacağını tahmin ederseniz veya daha fazla maliyet oluşursa ilgili tahmini ve gerçek satışlar da artar. Bu faturalama yöntemine sahip teklif satırlarında aşılamaz limitler belirtebilirsiniz. Bu, gerçek gelir için tavan değeri belirler. Tahmini gelir aşılamaz limitlerden etkilenmez.
- **Sabit fiyat:** Bu, satış değerlerinin oluşan maliyetlerden bağımsız olacağını belirten sabit fiyatlı bir sözleşme modelidir. Satış değeri sabittir ve daha fazla maliyet tahmini ya da gerçekleşmesi olduğunda değişmez.

## <a name="project-price-lists"></a>Proje fiyat listeleri

Proje fiyat listeleri; zaman, gider ve projeyle ilgili diğer bileşenlerin maliyet oranlarını değil varsayılan fiyatlarını belirlemek için kullanılan fiyat listeleridir. Birden çok fiyat listesi olabilir. Her listenin, her proje teklifinin kendi tarih geçerliliği olabilir. Proje fiyat listelerinde çakışan tarih geçerliliği Project Operations'ta desteklenmez.

## <a name="product-price-lists"></a>Ürün fiyat listeleri

Ürün fiyat listeleri, teklifteki ürün tabanlı satırların maliyet oranlarını değil varsayılan fiyatlarını belirlemek için kullanılan fiyat listeleridir. Her teklif için yalnızca bir fiyat listesi vardır.

## <a name="transaction-classes"></a>İşlem sınıfları

Project Operations dört işlem sınıfı türünü destekler:

- Zaman
- Gider
- Malzeme
- Ücret

Maliyet ve satış değerleri; Zaman, Gider ve Malzeme işlem sınıflarında tahmin edilebilir ve oluşabilir. Ücret yalnızca gelir işlem sınıfına dahil olabilir.

## <a name="work-entities-and-billing-entities"></a>İş varlıkları ve faturalama varlıkları

İşi temsil eden varlıklar Projeler ve Görevlerdir. Faturayı temsil eden varlıklar Teklif satırları ve Sözleşme satırlarıdır. Farklı iş varlıklarını, Teklif veya Sözleşme satırlarıyla ilişkilendirerek faturalama seçeneklerine bağlayabilirsiniz.

## <a name="multi-customer-deals"></a>Çok müşterili anlaşmalar

Çok müşterili anlaşmalar, faturalanacak birden çok müşteri olduğunda gerçekleşir. Bu anlaşmaların yaygın örnekleri şunlardır:

- **OEM Kuruluşlar ve bunların iş ortakları:** İş ortakları ve satıcılar, bir ürünü katma değerli hizmetlerle satarlar. Bu genellikle, müşteriyle yapılan belirli bir anlaşma sırasında OEM, projenin bir kısmını finanse etmeyi teklif ettiğinde oluşan bir senaryodur. 

- **Kamu sektörü projeleri:** Yerel hükümetin birden çok bölümü bir projeyi fonlamayı kabul eder ve önceden kabul edilen paylara göre faturalandırılırlar. Örneğin, bir okul bölgesi ve şehir ya da yerel kamu dairesi, bir yüzme havuzu inşaatını fonlamayı kabul eder.

## <a name="invoice-schedules"></a>Fatura zamanlamaları

Fatura zamanlamaları, her teklif satırına özeldir ve aynı zamanda isteğe bağlıdır. Fatura zamanlamaları, belirli başlangıç ve bitiş tarihlerine ve fatura sıklığına göre oluşturulur. Fatura zamanlamaları, otomatik fatura oluşturma işlemi yapılandırıldığında sözleşme aşamasında kullanılır. Teklif aşamasında, zamanlamalar isteğe bağlıdır. Fatura zamanlamaları, **Teklif** aşamasında oluşturulduğunda, bir proje teklifi kazanıldığında oluşturulan proje sözleşmesine kopyalanır.

## <a name="changes-from-dynamics-365-sales-quote"></a>Dynamics 365 Sales teklifinden farkları:

Project Operations teklifleri, Dynamics 365 Sales tekliflerini temel alarak oluşturulur. Ancak işlevselliğinde bilmeniz gereken bazı önemli farklılıklar bulunmaktadır:

- **Düzelt** ve **Etkinleştir** eylemleri desteklenmez.
- Project Operations tekliflerinde iki farklı satır türü vardır. Bunlardan biri projeler, diğeri de ürünler içindir.
- Project Operations teklifleri kendi biçim ve kullanıcı arabirimi öğelerine, iş kurallarına, eklentilerdeki iş mantığına ve Sales tekliflerine göre benzersiz kılan istemci tarafı komut dosyalarına sahiptir.

Bu nedenlerle, bir Sales teklifiyle Project Operations teklifini birbirinin yerine kullanmanız önerilmez.
