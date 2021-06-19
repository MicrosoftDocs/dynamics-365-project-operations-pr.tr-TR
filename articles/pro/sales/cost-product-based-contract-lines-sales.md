---
title: Ürün tabanlı sözleşme satırlarını maliyetlendirin - lite
description: Bu konu oluşturma hakkında bilgi sağlar
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9458a57863244a68359f57185325c03a46bd6569
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003565"
---
# <a name="cost-product-based-contract-lines---lite"></a>Ürün tabanlı sözleşme satırlarını maliyetlendirin - lite

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_


Dynamics 365 Project Operations uygulamasındaki ürün tabanlı sözleşme satırları, satış sonrası karlılık hesaplamaları için ürünün maliyet fiyatını depolayan **Maliyet Fiyatı** alanını içerir.

Katalog ürünü için ürün tabanlı sözleşme satırı oluşturulduğunda, satırın maliyeti varsayılan olarak ürün kataloğundaki **Standart Maliyet** alanından alınır. Ürün kataloğundaki **standart maliyet** alanı Kuruluşun temel para birimi cinsinden ayarlanır. Birim maliyet, sözleşme satırında varsayılan olarak kullanıldığında, sözleşmedeki satış para birimine dönüştürülür.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Ürün tabanlı sözleşme satırındaki birim maliyet

Ürün tabanlı sözleşme satırında birim maliyete sahip olmanın amacı bir ürünün her satışta farklı maliyetlere sahip olabilmesine izin vermektir. Her zaman gerekli olmasa da, ürün maliyetine tedarikçiye göre iskonto uygulanabilecek belirli senaryolar vardır. Aşağıdaki senaryoyu inceleyin:

Fabrikam Robotics, A Datum Corporation'ın montaj hatlarına robotik kollar kuruyor. Fabrikam, kurulum hizmetleri sağlar ancak robotik kollar Trey Research'tendir. Adatum Corporation firmasına robotik kolların kurulumu, Trey Research şirketi yeni bir endüstriye açılan kapıysa Trey, Fabrikam'a bu anlaşma için özel bir iskonto sunabilir. Bu durumda Fabrikam, Robotic Arms için bir ürün tabanlı sözleşme satırı oluşturur. Bu sözleşme için birim başına maliyet girilir. Maliyet, Trey Research'ün robotik kollarının maliyetinden farklıdır.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]