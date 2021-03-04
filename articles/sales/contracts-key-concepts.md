---
title: Proje Sözleşmeleri - Temel kavramlar
description: Bu konuda Project Operations'ta proje sözleşmesinin temel kavramları hakkında bilgi sağlanır.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fa00bd5b4a1179f38d5dfb63a47b39eec69c6ecf
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642162"
---
# <a name="project-contracts---key-concepts"></a>Proje Sözleşmeleri - Temel kavramlar

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Bu konu, Dynamics 365 Project Operations'ta Proje sözleşmelerini kullanmaya başlamadan önce bilmeniz gereken temel kavramları sağlar:

## <a name="owning-company"></a>Sahibi Olan Şirket

Sahibi olan şirket, Dynamics 365 Finance öğesinden Project Operations için **Proje yönetimi ve muhasebe** modülündeki tüzel kişilik kavramına eşittir. Sorumlu şirket, bir anlaşmadan tahakkuk eden maliyet ve geliri hesaba alacak tüzel kişiliği temsil eder.

## <a name="contracting-unit"></a>Sözleşme Birimi

Sözleşme birimi, proje teslimatının sahibi olan bölümü veya uygulamayı temsil eder. Her sözleşme birimi için kaynak maliyetlerini ayarlayabilirsiniz. Bir kaynağın kaynak maliyetini belirttiğiniz zaman, kaynaklar için farklı maliyet oranları da ayarlayabilirsiniz. Bu sözleşme birimi, bu kaynakları işletmedeki diğer bölüm veya uygulamalardan ödünç alarmaktadır. Kaynaklar için maliyet oranları transfer fiyatları, kaynak ödünç alma veya değişim fiyatları olarak adlandırılır. Diğer bölümlerden kaynak ödünç alma maliyet oranlarını ayarladığınızda, ödünç veren bölümün para birimi cinsini kullanın.

## <a name="cost-currency"></a>Maliyet para birimi

Maliyet para birimi, ekranda maliyetlerin raporlandığı para birimidir. Bu para birimi; Sözleşme ve projenin **Sözleşme ünitesi** alanına iliştirilmiş para biriminden alınır. Maliyetler bir projeye göre herhangi bir para birimine kaydedilebilir. Ekranda gösterildiğinde ancak maliyetlerin kaydedildiği para birimi, projenin maliyet para birimine dönüştürülür.

Common Data Service (CDS) platformundaki döviz kurları güncel olamadığından, ekrandaki toplam maliyetler para birimi döviz kurlarını güncelleştirdiğinizde zaman içinde değişebilir. Bununla birlikte, tutarlar oluştukları para birimi cinsinden saklandığından, veritabanına kaydedilen maliyetler değişmez.

## <a name="sales-currency"></a>Satış Para Birimi

Project Operations'taki satış para birimi, tahmini ve gerçek satış tutarlarının kaydedildiği ve gösterildiği para birimidir. Satış para birimi, aynı zamanda, müşterinin anlaşma için faturalandığı para birimidir. Proje sözleşmesinde, satış para birimi varsayılan olarak müşteri veya firma kaydındaki değere ayarlanır ve sözleşme oluşturulduğunda değiştirilebilir. Bir sözleşme, bir teklifin kazanıldığı gibi kapatılarak oluşturulduğunda, sözleşmedeki para birimi teklifteki para biriminden varsayılan olarak çıkar.

Sıfırdan bir proje sözleşmesi oluşturduğunuzda, **Satış Para Birimi** alanı düzenlenemez. Ürün ve proje fiyat listelerinin varsayılan değeri sözleşmedeki bu para birimine göre ayarlanır.

Maliyetlerin aksine, satış değerleri yalnızca Satış para birimi cinsinden kaydedilebilir.

## <a name="billing-method"></a>Faturalama Yöntemi

Projeler için genellikle iki sözleşme modeli türü vardır; sabit ücretli ve tüketim tabanlı. Bu modeller Project Operations'nde iki olası değere sahip faturalama yöntemleri olarak temsil edilir:

- Zaman ve Malzeme: Bu, oluşan her maliyetin karşılığında bir gelir olan tüketim tabanlı bir sözleşme modelidir. Daha fazla maliyet oluşacağını tahmin ederseniz veya daha fazla maliyet oluşursa ilgili tahmini ve gerçek satışlar da artar. Bu fatura yöntemine sahip olan sözleşme satırlarındaki, gerçek geliri geçersiz talarla ilgili olmayan limitleri belirtin. Tahmini gelir aşılamaz limitlerden etkilenmez.
- Sabit Fiyat: Bu, satış değerlerinin oluşan maliyetlerden bağımsız olacağını belirten sabit fiyatlı bir sözleşme modelidir. Satış değeri sabittir ve daha fazla maliyet tahmini ya da gerçekleşmesi olduğunda değişmez.

## <a name="project-price-lists"></a>Proje fiyat listeleri

Proje fiyat listeleri; zaman, gider ve projeyle ilgili diğer bileşenlerin maliyet oranlarını değil varsayılan fiyatlarını belirlemek için kullanılan fiyat listeleridir. Birden çok fiyat listesi olabilir. Her fiyat listesinin, her proje sözleşmesi için kendi tarih efekti vardır. Proje fiyat listelerinde çakışan tarih geçerliliği Project Operations'ta desteklenmez.

Proje teklifi kazanılarak proje sözleşmesi oluşturulduğunda, proje fiyat listeleri sözleşme adı ve tarihi dahil edilmiş olarak kopyalanır. Bu bilgilerin kopyalanması, bu proje sözleşmesindeki proje bileşenleri için özel fiyatlandırma oluşturur.

## <a name="transaction-classes"></a>İşlem sınıfları

Project Operations dört işlem sınıfı türünü destekler:

- Zaman
- Gider
- Malzeme
- Ücret

Maliyet ve satış değerleri; Zaman, Gider ve Malzeme işlem sınıflarında tahmin edilebilir ve oluşabilir. Ücret yalnızca gelir işlem sınıfına dahil olabilir.

## <a name="work-entities-and-billing-entities"></a>İş varlıkları ve faturalama varlıkları

İşi temsil eden varlıklar Projeler ve Görevlerdir. Faturayı yönlerini temsil eden varlıklar sözleşme satırlarıdır. Farklı iş varlıklarını, sözleşme satırlarıyla ilişkilendirerek faturalama seçeneklerine bağlayabilirsiniz.

## <a name="multi-customer-deals"></a>Çok müşterili anlaşmalar

Çok müşterili anlaşmalar, faturalanacak birden çok müşteri olduğunda gerçekleşir. Bu anlaşmaların yaygın örnekleri şunlardır:

- OEM Enterprises ve ortakları: Ortaklar ve satıcılar, genellikle bir müşteriyle belirli bir anlaşmayı içeren, bazı katma değerli hizmetlere sahip bir ürünü satarlar. OEM projenin bir kısmını finanse etmeyi teklif etti. 

- Kamu sektörü projeleri: Yerel hükümetin birden çok bölümü bir projeyi fonlamayı kabul eder ve önceden kabul edilen paylara göre faturalandırılırlar. Örneğin, bir okul bölgesi ve yerel kamu dairesi, bir yüzme havuzu inşaatını fonlamayı kabul eder.

## <a name="invoice-schedules"></a>Fatura zamanlamaları

Fatura zamanlamaları her sözleşme satırına özgür ve otomatik faturalamanın çalışması için gereklidir. Fatura zamanlamaları, belirli başlangıç ve bitiş tarihlerine ve fatura sıklığına göre oluşturulur. Zamanlamaları, otomatik fatura oluşturma işlemi yapılandırıldığında sözleşme aşamasında kullanılır. Bir proje sözleşmesi bir tekliften oluşturulduğunda, fatura zamanlaması tekliften proje sözleşmesine kopyalanır.

## <a name="changes-from-dynamics-365-sales-orders"></a>Dynamics 365 Sales Siparişlerinden farkları

Project Operations'daki sözleşmeler Dynamics 365 Sales'daki siparişler üzerine kurulmuştur. Ancak, işlevlerde önemli sapmalar ve farklılıklar vardır. Sözleşmeler kendi biçim ve kullanıcı arabirimi öğelerine, iş kurallarına, eklentilerdeki iş mantığına ve Siparişlere göre benzersiz kılan istemci tarafı komut dosyalarına sahiptir. Bu nedenlerden dolayı, birbirinin yerine bir Sales siparişi ve Project Operations sözleşmesi kullanmayın.


[!INCLUDE[footer-include](../includes/footer-banner.md)]