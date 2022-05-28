---
title: Ürün tabanlı sözleşme satırlarını maliyetlendirin - lite
description: Bu konu oluşturma hakkında bilgi sağlar
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3def4c330dc9aadbf5ff806ef7682fbfd1072e4b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599294"
---
# <a name="cost-product-based-contract-lines---lite"></a>Ürün tabanlı sözleşme satırlarını maliyetlendirin - lite

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_


Dynamics 365 Project Operations uygulamasındaki ürün tabanlı sözleşme satırları, satış sonrası karlılık hesaplamaları için ürünün maliyet fiyatını depolayan **Maliyet Fiyatı** alanını içerir.

Katalog ürünü için ürün tabanlı sözleşme satırı oluşturulduğunda, satırın maliyeti varsayılan olarak ürün kataloğundaki **Standart Maliyet** alanından alınır. Ürün kataloğundaki **standart maliyet** alanı Kuruluşun temel para birimi cinsinden ayarlanır. Birim maliyet, sözleşme satırında varsayılan olarak kullanıldığında, sözleşmedeki satış para birimine dönüştürülür.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Ürün tabanlı sözleşme satırındaki birim maliyet

Ürün tabanlı sözleşme satırında birim maliyete sahip olmanın amacı bir ürünün her satışta farklı maliyetlere sahip olabilmesine izin vermektir. Her zaman gerekli olmasa da, ürün maliyetine tedarikçiye göre iskonto uygulanabilecek belirli senaryolar vardır. Aşağıdaki senaryoyu inceleyin:

Fabrikam Robotics, A Datum Corporation'ın montaj hatlarına robotik kollar kuruyor. Fabrikam, kurulum hizmetleri sağlar ancak robotik kollar Trey Research'tendir. Adatum Corporation firmasına robotik kolların kurulumu, Trey Research şirketi yeni bir endüstriye açılan kapıysa Trey, Fabrikam'a bu anlaşma için özel bir iskonto sunabilir. Bu durumda Fabrikam, Robotic Arms için bir ürün tabanlı sözleşme satırı oluşturur. Bu sözleşme için birim başına maliyet girilir. Maliyet, Trey Research'ün robotik kollarının maliyetinden farklıdır.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]