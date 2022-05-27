---
title: Katalog ürünleri için maliyet ve satış oranlarını ayarlama -lite
description: Bu konu, bir ürün kataloğundaki maddeler için maliyet ve satış oranlarının nasıl ayarlanacağı hakkında bilgi sağlar.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 12e09d99e9832c93c3aea34ec0d4488cdf6b02fa
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576846"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Katalog ürünleri için maliyet ve satış oranlarını ayarlama -lite

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_


Dynamics 365 Project Operations uygulamasında ürün kataloğu öğeleri için fiyatlandırma ayarı, Dynamics 365 Sales ile aynıdır.

Project Operations'ta ürünler tahmin edilemez veya projelerde kullanılamaz. Bu nedenle, ürün kataloğu fiyatlarının teklifler ve sözleşmeler için proje fiyat listelerinde ayarlanması gerekmez.

Ürün kataloğu fiyatlarını ayarlamak için bir teklifin, sözleşmenin veya hesabın **Ürün Fiyatı** alanını kullanın. Proje fiyat listelerinde ürün kataloğu fiyatları ayarlamayın. Proje fiyat listeleri proje Işlemlerine özeldir. Uygulamaya özgü iş mantığı, fiyat listelerini bir tekliften bir sözleşmeye kopyalar. Sonuç, sözleşmeye özel proje fiyatı listesidir. Teklifteki proje fiyat listesi çok büyük olursa, kopyalama işlemi teklif kazanma işlemini erteleyebilir. Ürün Fiyatı listeleri, sözleşmelerde özel fiyat listeleri oluşturmak için kopyalanmaz. Kopyalama söz konusu olmadığı için teklif sürecinin performansı etkilenmez.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]