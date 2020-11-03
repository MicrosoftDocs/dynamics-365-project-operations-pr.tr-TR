---
title: Proje tabanlı fırsat satırları (Pro)
description: Bu konuda, proje tabanlı fırsat satırları hakkında bilgiler sağlanmaktadır. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a688b9bed5a38e7b5947cbcee1e3cb8ab211e98
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086249"
---
# <a name="project-based-opportunity-lines-pro"></a>Proje tabanlı fırsat satırları (Pro)

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Proje tabanlı fırsat satırları yalnızca proje tabanlı fırsatlarda kullanılabilir. Proje tabanlı fırsat kayıtlarında **Tür** alanı **İş tabanlı** değerine ayarlanmıştır.

Proje tabanlı fırsat satırları, bir proje kullanılarak müşteriye teslim edilecek satır öğeleridir. Ancak bir proje, proje tabanlı bir fırsat satırına bağlanamaz. Fırsat genellikle bir anlaşmanın yaşam döngüsünde erken bir aşama olduğundan projeler **Teklif** aşamasından itibaren satır öğelerine bağlanabilir. Müşteriye yapılan işi teslim etmek için kullanılacak proje sayısı daha sonra, satış aşamasında verilen bir kararla belirlenir. Fırsat aşamasını müşteri için ayrı teslim bileşenlerini tanımlamak amacıyla kullanabilirsiniz. Bu bileşenleri teslim etmek için kullanılan gerçek proje sayısını etkileyen kararlar, iş hakkında daha fazla bilgi edinene kadar ertelenebilir.

Aşağıda, proje tabanlı fırsat satırındaki alanlar verilmiştir:

| **Alan** | **Konum** | **İlgi, amaç ve kılavuz** | **Aşağı yönlü etki** |
| --- | --- | --- | --- |
| Ürün Türü | Genel sekmesi (gizli) | Aşağıdaki seçeneklerden birini belirleyebilirsiniz:</br>- Proje tabanlı hizmet (yalnızca Dynamics 365 Project Operations yüklendiğinde kullanılabilir)</br>- Ürün (yalnızca Project Operations ve Dynamics 365 Sales yüklendiğinde kullanılabilir) | Fırsat üzerinde proje tabanlı satırlar ızgarasından proje tabanlı fırsat satırı oluşturduğunuzda bu alanın değeri **Proje tabanlı hizmet** olarak ayarlanır. <br> Bu değeri değiştirirseniz veya geçersiz kılarsanız proje işlevi, proje tabanlı satır öğelerinizde etkinleştirilmez. |
| Fırsat | Genel sekmesi | Bu alan salt okunurdur ve bu satır öğesinin ait olduğu üst Fırsat kaydını ifade eder. | Bu alanda aşağı yönlü etki yoktur. |
| Veri Akışı Adı | Genel sekmesi | Bu düzenlenebilir metin alanı, satır öğesine kısa bir kimlik sağlamak için kullanılabilir. | Bu fırsattan bir teklif oluşturduğunuzda bu değer teklif satırına taşınır. |
| Müşteri Bütçesi | Genel sekmesi | Bu düzenlenebilir para birimi alanı müşterinin bu satır öğesine harcayabileceği tutarı izlemek için kullanılabilir. | Bu fırsattan bir teklif oluşturduğunuzda bu değer teklif satırındaki ilgili alana taşınır. |
| Faturalama Yöntemi | Genel sekmesi | Bu düzenlenebilir alan aşağıdaki değerlere sahiptir:</br>- Zaman ve Malzeme</br>- Sabit Fiyat | Bu fırsattan bir teklif oluşturduğunuzda bu değer teklif satırındaki ilgili alana taşınır. Teklif satırı oluşturulduktan sonra, alan kilitlenir ve değiştirilemez. Bu alan değerini mümkün olduğunca doğru atayın. Teklif satırında bu alanın değerini değiştirmeniz gerekirse teklif satırını silip yeniden oluşturun. |
