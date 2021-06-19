---
title: Katalog ürünleri için maliyet ve satış oranlarını ayarlama -lite
description: Bu konu, bir ürün kataloğundaki maddeler için maliyet ve satış oranlarının nasıl ayarlanacağı hakkında bilgi sağlar.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4995859696c844e99593139f63dffbf86a52f2f0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004367"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Katalog ürünleri için maliyet ve satış oranlarını ayarlama -lite

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_


Dynamics 365 Project Operations uygulamasında ürün kataloğu öğeleri için fiyatlandırma ayarı, Dynamics 365 Sales ile aynıdır.

Project Operations'ta ürünler tahmin edilemez veya projelerde kullanılamaz. Bu nedenle, ürün kataloğu fiyatlarının teklifler ve sözleşmeler için proje fiyat listelerinde ayarlanması gerekmez.

Ürün kataloğu fiyatlarını ayarlamak için bir teklifin, sözleşmenin veya hesabın **Ürün Fiyatı** alanını kullanın. Proje fiyat listelerinde ürün kataloğu fiyatları ayarlamayın. Proje fiyat listeleri proje Işlemlerine özeldir. Uygulamaya özgü iş mantığı, fiyat listelerini bir tekliften bir sözleşmeye kopyalar. Sonuç, sözleşmeye özel proje fiyatı listesidir. Teklifteki proje fiyat listesi çok büyük olursa, kopyalama işlemi teklif kazanma işlemini erteleyebilir. Ürün Fiyatı listeleri, sözleşmelerde özel fiyat listeleri oluşturmak için kopyalanmaz. Kopyalama söz konusu olmadığı için teklif sürecinin performansı etkilenmez.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]