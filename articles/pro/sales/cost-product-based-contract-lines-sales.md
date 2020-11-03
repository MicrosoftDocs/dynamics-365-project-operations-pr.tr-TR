---
title: Ürün tabanlı sözleşme satırlarını maliyetlendirme
description: Bu konu oluşturma hakkında bilgi sağlar
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7dfb9425174dddee52f9ee64f7a963e48a6bca70
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/20/2020
ms.locfileid: "4086555"
---
# <a name="costing-product-based-contract-lines"></a>Ürün tabanlı sözleşme satırlarını maliyetlendirme

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_


Dynamics 365 Project Operations'ta ürün tabanlı sözleşme satırları, ürünün akış yönündeki karlılık hesaplamaları için maliyet fiyatını depolayan **Maliyet fiyatı** alanını içerir.

Katalog ürünü için ürün tabanlı bir sözleşme satırı oluşturulduğunda, ürün tabanlı sözleşme satırının maliyeti, varsayılan olarak ürün kataloğundaki **Standart Maliyet** alanından alınır. Ürün kataloğundaki **standart maliyet** alanı Kuruluşun temel para birimi cinsinden ayarlanır. Birim maliyet, sözleşme satırında varsayılan olarak kullanıldığında, sözleşmedeki satış para birimine dönüştürülür.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Ürün tabanlı sözleşme satırındaki birim maliyet

Ürün tabanlı sözleşme satırında birim maliyete sahip olmanın amacı bir ürünün her satışta farklı maliyetlere sahip olabilmesine izin vermektir. Her zaman gerekli olmasa da, ürün maliyetine tedarikçiye göre iskonto uygulanabilecek belirli senaryolar vardır. Aşağıdaki senaryoyu inceleyin:

Fabrikam Robotics, A Datum Corporation'ın montaj hatlarına robotik kollar kuruyor. Fabrikam, kurulum hizmetleri sağlıyor ancak robotik kollar, Trey Research şirketinden sağlanıyor. Adatum Corporation firmasına robotik kolların kurulumu, Trey Research şirketi yeni bir endüstriye açılan kapıysa Trey, Fabrikam'a bu anlaşma için özel bir iskonto sunabilir. Bu durumda, Fabrikam, bu sözleşmenin birim maliyetini, Trey Research'den alınan Robot kolları standart maliyetinden farklı bir şekilde robot bir şekilde ve bir dizi maliyet için ürün tabanlı bir sözleşme satırı halinde oluşturur.
