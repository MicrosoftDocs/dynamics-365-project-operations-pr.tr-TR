---
title: Proje teklifiyle ilgili özet bilgiler (Sales)
description: Bu konuda, proje tekliflerine uygulayan ve bu teklifleri etkileyen bilgiler ve ayarlar hakkında bilgiler sağlanmaktadır. (Sales)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d050258ae457bb4392d5fa761442cfc7a444feb0
ms.sourcegitcommit: f6509f7d50de4d4ebb92c1bf2cfcdf09f17458eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/06/2020
ms.locfileid: "3966881"
---
# <a name="summary-information-on-a-project-quote-sales"></a>Proje teklifiyle ilgili özet bilgiler (Sales)

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Bu makalede, bir proje teklifi için geçerli olan bilgiler açıklanmaktadır. Bu, tüm teklif satırlarını etkileyen ayarları ve proje teklifinin KPI'larını yönlendiren tüm satır öğelerinde özetlenen teklifle ilgili bilgileri içerir.

Aşağıdaki tabloda Dynamics 365 Project Operations için benzersiz olan veya Dynamics 365 Sales tekliflerine göre bazı önemli değişiklikleri olan bir proje teklifinde özet bilgi alanları listelenmiştir.

| **Alan** | **Konum** | **İlgi, amaç ve kılavuz** | **Aşağı yönlü etki** |
| --- | --- | --- | --- |
| Tür | Özet sekmesi (gizli) | Bu seçenek kümesi alanında aşağıdaki seçenekler karma olarak bulunur:</br>- İş tabanlı (yalnızca Project Operations yüklendiğinde kullanılabilir)</br>- Öğe tabanlı (yalnızca Project Operations ve Sales yüklendiğinde kullanılabilir)</br>- Servis bakımı tabanlı (Dynamics 365 Field Service yüklendiğinde kullanılabilir) | Project Operations uygulamasını kullandığınızda, bu alanın değeri otomatik olarak **İş tabanlı** seçeneğine ayarlanır. Bu, teklifi proje tabanlı teklif olarak sınıflandırır. Projeye özgü tüm uzantıları ve işlevleri etkinleştirmek için bir teklifin proje tabanlı olması gerekir. |
| Potansiyel Müşteri | Özet sekmesi | Müşterinin şirket veya firma kaydına başvuru. Teklif bir fırsattan oluşturulduğunda, bu alan fırsattaki ilgili alandan kopyalanır. | Proje teklifindeki para birimi, müşterinin para birimine göre varsayılan olarak ayarlanır. Ancak bu, teklif kaydedilmeden önce değiştirilebilir. |
| Firma Yöneticisi | Özet sekmesi | Bu anlaşma için firma Yöneticisinin adı. Teklif bir fırsattan oluşturulduğunda, bu alan fırsattaki ilgili alandan kopyalanır. | Firma yöneticisi, bu projenin tamamlanmasından sonra müşteriyle ilişkiyi yönetmekten sorumludur. Firma yöneticisine bağlı olan ayrılabilir kaynak kaydına göre, sözleşme yapan birim, varsayılan olarak proje teklifindeki birimdir. |
| Sözleşme Birimi | Özet sekmesi | Bu teklifle ilişkili projenin veya projelerin tesliminden sorumlu olan kuruluş birimi. Teklif bir fırsattan oluşturulduğunda, bu alan fırsattaki ilgili alandan kopyalanır. | Sözleşme yapan birim, şirketin anlaşma kapatıldıktan sonra projeleri yürüten bölümüdür. Sözleşme yapan her biriminin bir para birimi vardır ve bu para birimi, projenin yürütülmesi sırasında oluşan tahmini ve gerçek maliyetleri raporlamak için kullanılır. |
| Ürün fiyat listesi | Özet sekmesi | Bu, ürün tabanlı teklif satırlarındaki varsayılan fiyatları ayarlamak için kullanılan fiyat listesidir. Bu alandaki seçenek listesi, fiyat listesi para biriminin teklifteki para birimiyle eşleştiği fiyat listelerinin bir listesini gösterir. Teklif bir fırsattan oluşturulduğunda, bu alan fırsattaki ilgili alandan kopyalanır. Fırsattaki bu alan, varsayılan olarak firma kaydından alınır ancak değiştirilebilir. | Teklif kazanıldığında, alan değeri oluşturulan proje sözleşmesine kopyalanır. |
| Para birimi | Özet sekmesi | Bu alan, bu anlaşmanın değerini bildirmek için kullanılan para birimini gösterir. Aynı zamanda, anlaşma kazanıldığında müşterinin faturalanacağı para birimidir. Teklif bir fırsattan oluşturulduğunda, bu alan fırsattaki ilgili alandan kopyalanır. Fırsattaki bu alan, varsayılan olarak firma kaydından alınır ancak kullanıcı tarafından değiştirilebilir. | Bu alan, teklif kaydedildikten sonra düzenlenemez. Bu, teklifteki ürün ve proje fiyat listelerini varsayılan yapmak için kullanılır. Teklifteki para birimi, fiyat listesindeki para birimini eşleştirmek için kullanılır. |
| Aşılamaz limit | Özet sekmesi | Bu, müşterinin bu anlaşma için kabul ettiği son değer üzerinden anlaşılan tavanı gösterir. | Bu tavan, uygulama sırasında değerlendirilir ve bu anlaşmayla ilişkili tüm satır öğeleri ve projeler için geçerlidir. |
| Talep edilen teslim tarihi | Özet sekmesi | Teklif bir fırsattan oluşturulduğunda, bu alan fırsattaki ilgili alandan kopyalanır. | Bu tarih, fatura zamanlaması oluştururken bitiş tarihi olarak kullanılır. |

Aşağıda, Project Operations için benzersiz olan ve Sales tekliflerine göre bazı önemli değişiklikleri olan bir proje teklifinde kullanılabilen sekmeler ve KPI'lar verilmiştir:

| **Alan** | **Konum** | **İlgi, amaç ve kılavuz** |
| --- | --- | --- |
| Karlılık analizi | Teklif sekmesi | Sekme aşağıdaki ölçümleri gösterir:</br>- Toplam borçlandırılabilir maliyet</br></br>- Toplam borçlandırılamaz maliyet</br>- Toplam gelir</br>- Toplam gelir (taban)</br>- Brüt kar</br>- Düzeltilen brüt kar|
| Müşteri Beklentileriyle Karşılaştırma | Teklif sekmesi | Bu sekme aşağıdaki ölçümleri gösterir:</br>- Tahmini tamamlanma zamanı</br>- İstenen tamamlanma</br>- Müşteri bütçesi</br>- Teklif değeri |
| Teklif analizi | Teklif sekmesi | Bu sekmede bir proje teklifi için aşağıdaki başlıca KPI'lar özetlenmiştir</br>- Bütçe ve zamanlama için müşteri beklentileri karşılaştırması</br>- Brüt kar</br>- Düzeltilen brüt kar |
