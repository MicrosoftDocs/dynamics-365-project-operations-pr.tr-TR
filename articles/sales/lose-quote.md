---
title: Proje tabanlı teklifleri kopyalama
description: Bu konuda, Project Operations'ta proje tabanlı tekliflerin kopyalanması hakkında bilgiler sağlanmaktadır.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d7234958d542dec4cba55cb0516f1222937389e1
ms.sourcegitcommit: f255b2cbf290973ce62fe2c1c121bd1df15a7392
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/01/2020
ms.locfileid: "3928617"
---
# <a name="copy-project-based-quotes"></a>Proje tabanlı teklifleri kopyalama

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Var olanı kopyalayarak kolayca yeni bir Proje teklifi oluşturabilirsiniz. 

- Proje teklifini kopyalamak için **Proje Teklifleri** liste sayfasında veya **Proje Teklifi** ayrıntıları sayfasında kopyalamak istediğiniz Proje teklifini seçin ve ardından **Kopyala** seçeneğini belirleyin.

Bu, kopyanın parametrelerini girebileceğiniz bir iletişim sayfası açar. Aşağıdaki tabloda iletişim sayfasına dahil edilen alanlar listelenmektedir. Seçtiğiniz değerlere bağlı olarak kopyalama işlemi değişebilir.

| **Alan** | **İlgi, amaç ve kılavuz** | **Aşağı yönlü etki** |
| --- | --- | --- |
| Başlık | Hedef teklifin ilgili konusunu veya adını girin. İletişim kutusu açıldığında sistem bunu **-kopya** ifadesi eklenmiş olarak kaynak teklifin konu kısmı olarak ayarlar. | |
| Potansiyel Müşteri | Müşterinin şirket veya firma kaydına başvuru. İletişim kutusu açıldığında sistem bunu kaynak teklifindeki firma olarak ayarlar. | Bu alan, teklifteki birincil müşteridir. |
| Sözleşme Birimi | Bu anlaşmayla ilişkili projelerin tesliminden sorumlu olan kuruluş birimi.
İletişim kutusu açıldığında sistem bunu kaynak teklifindeki sözleşme birimi olarak ayarlar. | Sözleşme birimi, şirketin anlaşma kapatıldıktan sonra projeleri yürüten bölümüdür. Sözleşme yapan her biriminin bir para birimi vardır. Para birimi, projenin yürütülmesi sırasında oluşan tahmini ve gerçek maliyetleri bildirmek için kullanılır. |
| Para birimi | Bu, anlaşmanın işlem gördüğü para birimidir. İletişim kutusu açıldığında sistem bunu kaynak teklifindeki para birimi olarak ayarlar. Bu değiştirilebilir ve değiştirilirse **Fiyatlandırmayı Kopyala** alanı her zaman **Hayır** olarak ayarlanır. Bunun nedeni, kaynak teklifindeki fiyat listelerinin artık geçerli olmamasıdır. | Para birimi, bir fiyat listesini varsayılan olarak belirlemek, teklif üzerine bir mali tahmin oluşturmak ve sonunda anlaşma kazanıldığında müşteriye fatura kesmek için kullanılır. |
| Talep Edilen Teslim Tarihi | Bu, müşteri tarafından talep edilen teslim tarihidir. | Bu, belirli bir sıklıkta faturalama tarihleri oluştururken bitiş tarihi olarak kullanılır. |
| Fiyatlandırmayı kopyala | Evet/Hayır değeri, teklif üzerindeki fiyatlandırmanın kaynak teklifinden kopyalanması gerekip gerekmediğini gösterir. | **Evet** seçilirse proje fiyat listesi ve ürün fiyat listesi başvuruları kaynak tekliften hedef teklife kopyalanır. **Hayır** seçilirse fiyat listeleri, firma veya proje parametrelerinde ayarlanan en son fiyat listelerine göre yeniden varsayılan hale getirilir. |

İletişim sayfasında **Tamam**'ı seçtiğinizde sistem, iletişim kutusunda seçilen parametrelere göre proje teklifinin bir kopyasını oluşturur. Yeni proje teklifi açılır. 

> [!NOTE]
> Aşağıdaki bilgiler Kaynak'tan Hedef teklife kopyalanmaz:
>
> - Fatura zamanlamaları
> - Teklif ve teklif satırı müşterileri
> - Proje bazlı teklif satırlarında proje başvurusu (Müşteri bütçe bilgileri)
>
>Bu bilgiler tekliflere özgü olduğu için bu alanlar ve kayıtlar kopyalanmaz. Projeler ve ürünler için teklif satırları, teklif satırı ayrıntılarına ilişkin tahminler ve teklif düzeyinde aşılmaz değerler kopyalanır. Varsayılan fiyat ve maliyet oranları **Parametreleri kopyala** iletişim sayfasında seçilen **Fiyatlandırmayı kopyala** seçeneğine bağlıdır.
