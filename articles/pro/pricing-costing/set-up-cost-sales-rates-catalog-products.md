---
title: Katalog ürünleri için maliyet ve satış oranlarını ayarlama
description: Bu konu, bir ürün kataloğundaki maddeler için maliyet ve satış oranlarının nasıl ayarlanacağı hakkında bilgi sağlar.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5178a9143536bf4b2573403125325017861cdd5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086391"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products"></a>Katalog ürünleri için maliyet ve satış oranlarını ayarlama

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_


Dynamics 365 Project Operations'da ürün kataloğu öğeleri için fiyatlandırma ayarlanması, Dynamics 365 Sales ile aynı olur.

Ürünler Project Operations projelerinde tahmin veya kullanılabilir olması gerektiğinden, teklifler ve sözleşmeler için proje fiyatı listelerinde ürün kataloğu fiyatlarını ayarlamaya gerek yoktur.

Ürün katalogu fiyatları bir teklifin, sözleşmenin veya firmanın **ürün fiyatı** alanında ayarlanmalıdır. Bu varlıklar için proje fiyat listelerinde ürün kataloğu fiyatları ayarlamayın. Proje fiyat listeleri proje Işlemlerine özeldir. Fiyat listelerini tekliften sözleşmeye kopyalayan, uygulamaya özgü iş mantığı vardır. Sonuç, sözleşmeye özel proje fiyatı listesidir. Teklifteki proje fiyat listesi çok büyük olursa, kopyalama işlemi teklif kazanma işlemini erteleyebilir. Ürün Fiyatı listeleri, sözleşmelerde özel fiyat listeleri oluşturmak için kopyalanmaz. Bu, ürün fiyatı listelerinin teklif kazanma işleminin performansını etkilemediği anlamına gelir.
