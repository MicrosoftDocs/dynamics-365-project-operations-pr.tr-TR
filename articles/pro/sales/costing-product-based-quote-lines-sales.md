---
title: Ürün tabanlı teklif satırlarını maliyetlendirme
description: Bu konuda, ürün tabanlı bir teklif satırına bir maliyet fiyatı uygulama hakkında bilgiler sağlanmaktadır.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1fa7896e249abfefd3e93cba4bad789e67e14f31
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003475"
---
# <a name="costing-product-based-quote-lines"></a>Ürün tabanlı teklif satırlarını maliyetlendirme

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_


Dynamics 365 Project Operations'ta proje tabanlı teklif satırlarında bir **Maliyet Fiyatı** alanı da vardır. Bu alan, teklif satırındaki ürünün maliyet fiyatını izlemek ve aşağı yönlü karlılık hesaplamaları için kullanılır.

Katalog ürünü için ürün tabanlı bir teklif satırı oluşturulduğunda, ürün tabanlı teklif satırının maliyeti, varsayılan olarak ürün kataloğundaki **Standart Maliyet** alanından alınır. Ürün kataloğundaki standart maliyet alanı Kuruluşun temel para birimi cinsinden ayarlanır. Ürün tabanlı teklif satırındaki varsayılan birim maliyeti teklifte, satış para birimine dönüştürülür.

## <a name="unit-cost-on-a-product-based-quote-line"></a>Ürün tabanlı teklif satırındaki birim maliyet

Ürün tabanlı teklif satırında birim maliyete sahip olmanın amacı bir ürünün her satışta farklı maliyetlere sahip olabilmesine izin vermektir. Bu tipik bir senaryo değildir ancak bazen, nihai satışın müşterisine bağlı olarak ürünün maliyeti tedarikçi tarafından düşürülebilir.

Örneğin:

Fabrikam Robotics, A Datum Corporation'ın montaj hatlarına robotik kollar kuruyor. Fabrikam, kurulum hizmetleri sağlıyor ancak robotik kollar, Trey Robotics şirketinden sağlanıyor. A Datum Corporation firmasına robotik kolların kurulumu, Trey şirketinin robotik kolları için yeni bir endüstriye açılan kapıysa Trey, Fabrikam'a bu anlaşma için özel bir iskonto sunabilir.

Bu durumda Fabrikam, Robotik Kollar için ürün tabanlı teklif satırı oluşturur ve bu teklif için birim başına özel bir maliyet girer. Bu maliyet, Trey Robotik Kollarının standart maliyetinden farklıdır.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]