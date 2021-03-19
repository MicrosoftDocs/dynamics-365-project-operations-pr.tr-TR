---
title: Katalog ürünleri için maliyet ve satış oranlarını ayarlama -lite
description: Bu konu, bir ürün kataloğundaki maddeler için maliyet ve satış oranlarının nasıl ayarlanacağı hakkında bilgi sağlar.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f0941c549cc38f0938a5819e8cb6ca9912f14790
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274482"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Katalog ürünleri için maliyet ve satış oranlarını ayarlama -lite

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_


Dynamics 365 Project Operations uygulamasında ürün kataloğu öğeleri için fiyatlandırma ayarı, Dynamics 365 Sales ile aynıdır.

Project Operations'ta ürünler tahmin edilemez veya projelerde kullanılamaz. Bu nedenle, ürün kataloğu fiyatlarının teklifler ve sözleşmeler için proje fiyat listelerinde ayarlanması gerekmez.

Ürün kataloğu fiyatlarını ayarlamak için bir teklifin, sözleşmenin veya hesabın **Ürün Fiyatı** alanını kullanın. Proje fiyat listelerinde ürün kataloğu fiyatları ayarlamayın. Proje fiyat listeleri proje Işlemlerine özeldir. Uygulamaya özgü iş mantığı, fiyat listelerini bir tekliften bir sözleşmeye kopyalar. Sonuç, sözleşmeye özel proje fiyatı listesidir. Teklifteki proje fiyat listesi çok büyük olursa, kopyalama işlemi teklif kazanma işlemini erteleyebilir. Ürün Fiyatı listeleri, sözleşmelerde özel fiyat listeleri oluşturmak için kopyalanmaz. Kopyalama söz konusu olmadığı için teklif sürecinin performansı etkilenmez.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]