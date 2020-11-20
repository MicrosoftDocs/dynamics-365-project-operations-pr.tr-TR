---
title: Proje sözleşme ayarları
description: Bu konu, sözleşme satırlarını etkileyen alanlar hakkında ve tüm satır maddeleri boyunca özetlenen sözleşmeyle ilgili bilgiler için bilgi sağlar.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2f29e396f8d30a5c5648b5c9937f1f20fbf72e89
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181167"
---
# <a name="project-contract-settings"></a>Proje sözleşme ayarları

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Bu konu, tüm sözleşme satırlarını etkileyen ayarlar da dahil olmak üzere tüm proje sözleşmesi için uygulanan alanlar hakkında bilgi sağlar. Tüm satır öğeleri boyunca özetlenen sözleşmeyle ilgili bilgileri, proje sözleşmesinin sürücü KPI 'Ları olarak da içerir.

Aşağıdaki tabloda Dynamics 365 Project Operations için benzersiz olan veya Dynamics 365 Sales'taki satış siparişlerine göre bazı önemli değişiklikleri olan bir proje teklifinde alanları listelenmiştir.

| Alan | Konum | Veri Akışı Açıklaması | Aşağı yönlü etki |
| --- | --- | --- | --- |
| Tür | **Özet** sekmesi (gizli) | Bu seçenek kümesi alanında aşağıdaki seçenekler karma olarak bulunur:</br>- **İş tabanlı** (yalnızca Project Operations yüklendiğinde kullanılabilir)</br>- **Öğe tabanlı** (yalnızca Project Operations ve Sales yüklendiğinde kullanılabilir)</br>- **Servis bakımı tabanlı** (Dynamics 365 Field Service yüklendiğinde kullanılabilir) | Project Operations, bu alanın değeri **çalışma tabanlı** olarak varsayılan olur ve sözleşmeyi proje tabanlı bir sözleşme olarak sınıflandırır. Projeye özgü tüm uzantıları ve işlevleri etkinleştirmek için bir projenin proje tabanlı olması gerekir. |
| Sahibi Olan Şirket | **Özet** sekmesi | Bu proje sözleşmesiyle ilişkili projelerden tahakkuk eden maliyetleri ve geliri hesaplayacak tüzel kişilik. Sözleşme, bir tekliften oluşturulduğunda, bu alan teklif kaydındaki ilgili alandan kopyalanır. | Sahibi olan şirket, Project Operations'ın **Proje yönetimi ve muhasebe** modülündeki tüzel kişilik kavramına eşittir. Bu projeden tahakkuk eden tüm maliyetler ve gelir, sahibi olan şirketin Genel muhasebesinde hesaplanır. |
| Müşteri | **Özet** sekmesi | Müşterinin şirket veya firma kaydına başvuru. Sözleşme, bir tekliften oluşturulduğunda, bu alan teklif kaydındaki ilgili alandan kopyalanır. | Proje sözleşmesindeki para birimi, müşterinin para birimine göre varsayılan olarak ayarlanır. Para birimi, sözleşme kaydedilmeden önce değiştirilebilir. |
| Firma Yöneticisi | **Özet** sekmesi | Bu anlaşma için firma Yöneticisinin adı. Sözleşme, bir tekliften oluşturulduğunda, bu alan teklif kaydındaki ilgili alandan kopyalanır. | Firma yöneticisi, bu projenin tamamlanmasından sonra müşteriyle ilişkiyi yönetmekten sorumludur. Firma yöneticisine bağlı olan ayrılabilir kaynak kaydına göre, sözleşme yapan birim, varsayılan olarak proje teklifindeki birimdir. |
| Sözleşme Birimi | **Özet** sekmesi | Bu sözleşmeyle ilişkili projelerin tesliminden sorumlu olan kuruluş birimi. Sözleşme, bir tekliften oluşturulduğunda, bu alan teklif kaydındaki ilgili alandan kopyalanır. | Sözleşme birimi, şirketin sonra projeleri yürüten bölümüdür. Sözleşme yapan her biriminin bir para birimi vardır ve bu para birimi, proje sırasında oluşan tahmini ve gerçek maliyetleri bildirmek için kullanılır. |
| Ürün Fiyat Listesi | **Özet** sekmesi | Bu, ürün tabanlı sözleşme satırlarındaki varsayılan fiyatları ayarlamak için kullanılan fiyat listesidir. Bu alandaki seçenek listesi, fiyat listesi para biriminin sözleşmedeki para birimiyle eşleştiği fiyat listelerinin bir listesini gösterir. Sözleşme, bir tekliften oluşturulduğunda, bu alan teklif kaydındaki ilgili alandan kopyalanır. Proje sözleşmesinde bu alan, varsayılan olarak firma kaydından alınır ancak değiştirilebilir. | Bu alanda aşağı yönlü ilgi yoktur. |
| Para birimi | **Özet** sekmesi | Bu anlaşmayı ve müşterinin faturalandığı para birimini raporlamak için kullanılan para birimi. Sözleşme, bir tekliften oluşturulduğunda, bu alan teklif kaydındaki ilgili alandan kopyalanır. Proje sözleşmesinde bu alan, varsayılan olarak firma kaydından alınır ancak değiştirilebilir. | Bu alan, sözleşme kaydedildikten sonra düzenlenemez. Bu alan, sözleşmedeki ürün ve proje fiyat listelerini varsayılan yapmak için kullanılır. Sözleşmedeki para birimi, fiyat listesindeki para birimini eşleştirmek için kullanılır. |
| Aşılamaz Limit | **Özet** sekmesi | Bu alan, müşterinin bu anlaşma için kabul ettiği son değer üzerinden anlaşılan tavanı gösterir. | Bu tavan, uygulama sırasında değerlendirilir ve bu anlaşmayla ilişkili tüm satır öğeleri ve projeler için geçerlidir. |
| Talep Edilen Teslimat Tarihi | **Özet** sekmesi | Sözleşme, bir sözleşme oluşturulduğunda, bu alan sözleşme kaydındaki ilgili alandan kopyalanır. | Bu tarih, fatura zamanlaması oluştururken bitiş tarihi olarak kullanılır. |

Aşağıdaki KPI 'Lar bir proje sözleşmesinin **sözleşme performansı** sekmesinde kullanılabilir.

| Alan | Konum | Veri Akışı Açıklaması |
| --- | --- | --- |
| Sözleşme Değeri | Genel Sözleşme | Proje sözleşmesinin toplam değeri. |
| Faturalanan Tutar | Genel Sözleşme | Bu sözleşmeyle ilgili tüm faturalardaki tutarların toplamı. |
| Ortaya Çıkan Maliyet | Genel Sözleşme | Sözleşmeyle eşlenen tüm projelerde günlüğe kaydedilen tüm maliyet fiili değerlerinin toplamı. |
| Brüt Kar | Genel Sözleşme | Faturalanan tutar - Tahakkuk eden maliyet çapraz Tarih/faturalanan tutar |
| Beklenen Marj | Genel Sözleşme | (Sözleşme değeri - tahmini maliyetler) / Sözleşme Değertahmini maliyetler = sözleşmeyle eşlenen tüm projelerdeki tüm tahmini maliyetlerin toplamı.|
| Sözleşme Değeri | Proje tabanlı satırlar | Sözleşme satırının değeri. |
| Faturalanan Tutar | Proje tabanlı satırlar | Sabit fiyat sözleşmesi satırı için: Bu sözleşme için oluşturulan çeşitli faturalardaki bu sözleşme satırıyla karşılaştırılarak tüm faturalanan satış kilometre taşındaki tutarların toplamı. Zaman ve malzeme sözleşmesi satırı için: Bu sözleşme için oluşturulan çeşitli faturalardaki bu sözleşme satırıyla karşılaştırılarak tüm faturalanan satış ücretlendirilebilir tutarların toplamı. |
| Ortaya Çıkan Maliyet | Proje tabanlı satırlar | Sözleşmeyle eşlenen tüm projelerde günlüğe kaydedilen tüm maliyet fiili değerlerinin toplamı. |
| Brüt Kar | Proje tabanlı satırlar | (Faturalanan tutar - Tahakkuk eden maliyet çapraz Tarih) / faturalanan tutar |
| Beklenen Marj | Proje tabanlı satırlar | (Baz para birimi cinsinden sözleşme satır tutarı-baz para birimi cinsinden sözleşme satırı için tahmini maliyetler)/sözleşme satırı tutarı baz para birimi cinsinden |
| Ortaya Çıkan Maliyet | Proje tabanlı satır ayrıntısı | Saat: Bu sözleşme satırıyla eşlenen projedeki bir rol için zaman maliyet gerçeğindeki tüm zaman miktarı toplamı. Giderler: Bu sözleşme satırıyla eşlenen projedeki bir kategori için tüm gider maliyet gerçeğindeki tüm zaman miktarı toplamı. |
| Kaydedilen Miktar | Proje tabanlı satır ayrıntısı | Saat: Bu sözleşme satırıyla eşlenen projedeki bir rol için zaman maliyet gerçekindeki tüm zaman miktarı. Giderler: Bu sözleşme satırıyla eşlenen projedeki gider maliyeti fiililerindeki bu gider kategorisi için tüm miktarlar. |
| Faturalanan Tutar | Proje tabanlı satır ayrıntısı | Sabit bir fiyat sözleşmesi satırı için, bu alan ayrıntı düzeyinde boş bırakılır ve yalnızca sözleşme satırı düzeyinde gösterilir. Bir zaman ve malzeme sözleşmesi satırı için, hesaplamalar Ayrıntılar düzeyinde tamamlanır. Ayrıntılar, faturalanan tüm gelir satırlarındaki tutar 'ın Masraflandırılabilir olan bu sözleşme satırına göre toplamını gösterir. |
| Faturalanan Miktar | Proje tabanlı satır ayrıntısı | Sabit bir fiyat sözleşmesi satırı için, bu alan ayrıntı düzeyinde boş bırakılır ve yalnızca sözleşme satırı düzeyinde gösterilir. Bir zaman ve malzeme sözleşmesi satırı için, hesaplamalar zaman ve giderler için Ayrıntılar düzeyinde tamamlanır. Saat: Ayrıntılar, faturalanan tüm gelir satırlarındaki tutar 'ın Masraflandırılabilir olan bu sözleşme satırına göre toplamını gösterir. Giderler: Bu sözleşme satırıyla eşlenen projedeki gider maliyeti fiililerindeki bu gider kategorisi için tüm miktarlar. |
| Sözleşme Değeri | Ürün tabanlı satırlar | Bu ürün tabanlı sözleşme satırının sözleşme satırı değeri. |
| Faturalanan Tutar | Ürün tabanlı satırlar | Bu sözleşme için oluşturulan çeşitli faturalardaki ürün tabanlı sözleşme satırıyla karşılaştırılarak tüm fatura satırlarındaki tutarların toplamı. |
| Ortaya Çıkan Maliyet | Ürün tabanlı satırlar | Sözleşmeyle eşlenen tüm projelerde günlüğe kaydedilen tüm maliyet fiili değerlerinin toplamı. |
| Brüt Kar | Proje tabanlı satırlar | Faturalanan tutar - Tahakkuk eden maliyet çapraz Tarih/faturalanan tutar |
| Beklenen Marj | Ürün tabanlı satırlar | (Sözleşme satırı değeri-sözleşme satırı için tahmini maliyetler)/sözleşme satırı değeri |
