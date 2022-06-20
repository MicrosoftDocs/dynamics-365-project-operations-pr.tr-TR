---
title: Avanslar ve elde tutulan tutar tabanlı sözleşmeler
description: Bu makalede, Project Operations'ta elde tutulan tutar temelli sözleşme modelleri ve avanslar hakkında bilgiler sağlanmaktadır.
author: rumant
ms.date: 10/20/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 201dd1651b12614930f6a2c294156b31deceab0b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932504"
---
# <a name="advances-and-retainer-based-contracts"></a>Avanslar ve elde tutulan tutar tabanlı sözleşmeler


_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Dynamics 365 Project Operations, elde tutulan tutar tabanlı sözleşmeleri destekler. Elde kalan tabanlı bir sözleşme, müşterinin bir proje süresi boyunca faturalandığı, anlaştığınız eşit dağıtılmış ödemeler kümesidir. Bu sözleşme türü genellikle müşteriye tahmin edilebilir bir fatura ve ödeme zamanlaması vermek için gereksinim duyan zaman ve malzeme veya tüketim tabanlı faturalama modelleri için kullanılır. Her döneme tahakkuk edilen gelir geliri, dönemin başlangıcındaki müşteriden alınan ödemeye göre mutabakat yapılır. Saat ve malzeme faturalama modelinin kavramıyla uyumlu olarak, her dönemde tahakkuk edilen gelir değerleri, tahakkuk eden maliyetlere göre farklılık gösterebilir. Tahakkuk eden gelir dönemin başlangıcında alınan tutardan daha fazla ise, proje teslim şirketi aşağıdakileri sağlayabilir:

- Yalnızca fazlası için müşteriyi faturalayın. 
- Gelirin mutabakatını bir sonraki faturalama dönemine erteleyin ve kalan mutabakata getirilmemiş gelir için projenin sonundaki bir son fatura yapın.

Project Operations'ta elde kalan tabanlı bir model ve sabit fiyatlı sözleşme modeli arasındaki temel fark sabit fiyatlı sözleşme modelinde, fatura tutarının bağlantılı veya tahakkuk eden maliyetlere bağlı olmasıdır. Faturalama, bu döneme ait tahakkuk eden maliyetlere hizalanmış kilometre taşına dayalı bir yaklaşım izler. Elde kalan tabanlı bir sözleşmede, faturalanabileceği gelir, sözleşme satırındaki faturalama yöntemine göre kaydedilir. Faturalama yöntemi zaman ve malzeme olduğunda, elenebilir gelir fatura verilen herhangi bir dönemde tahakkuk eden maliyetlere bağlıdır ve dönem ile döneme farklı olabilir. Ancak müşteri yalnızca periyodik elde kalan tutar için faturalandırılır. Sistem, dönem sonunda faturaalabilir geliri, dönemin başında için müşteriye fatura edilmiş olan tutara karşı mutabık kılmak üzere dönemin sonundaki başka bir faturayı kullanır.

Bu yöntemin avantajı, müşterinin maliyetlerinin, tipik bir zaman ve malzeme modelinden farklı olarak, elde tutulan zamanlamasında tahmin edilebilir hale gelmesine sahip olmasıdır. Projeyi teslim eden kuruluşun, bir sabit fiyat modelinin izin verdiğinden önce, kapsamdaki her artış nedeniyle, tahakkuk eden maliyetleri kurtarmanın riskiyle ilgili bazı odalar da vardır.

Dönemsel elde tutulan tabanlı bir zamanlamanın yanı sıra, Project Operations bir müşteriden bir kerelik bir avans kaydedebilir ve farklı proje maliyeti bileşenleriyle ilgili olarak mutabakat yapabilir.

Project OPerations'taki elde tutulan müşteriye faturalanana kadar kullanılamaz. Bu, avanslar ve elde tutulanlar için alt ızgarada yer alan aşağıdaki alanlarla gösterilir.

| Alan | Veri Akışı Açıklaması | Aşağı yönlü etki |
| --- | --- | --- |
| Kullanılabilir Tutar | Elde tutulan veya öncelikli kayıtta kullanılmak üzere kullanılabilir olan tutar. | Avans veya elde tutulan faturalanıncaya kadar bu kullanılabilir durumda değil, kullanılabilir tutar sıfır olacaktır. |
| Kullanılan Tutar | Elde tutulan veya öncelikli kayıtta kullanılmak üzere kullanılabilir olan tutar. | Avans veya elde tutulan, önceden kullanılmış veya tüketildiği bir bölümü olan gerçek maliyetlere sahip bir faturada kısmen mutabakat yapılabilir. Gelecekteki veya elde tutulan tutarının kalan kısmı fiili maliyetlerle gelecekte mutabık kılmak için kullanılabilir. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]