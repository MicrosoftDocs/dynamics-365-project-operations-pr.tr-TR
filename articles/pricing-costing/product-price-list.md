---
title: Ürün fiyat listeleri
description: Bu konu, proje teklifleri ve sözleşmeler için kullanılan katalog fiyatındaki fiyat listeleriyle ilgili bilgi sağlar.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 4feb7638dd7b6826e575d83457ae7f74ef6793bf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593268"
---
# <a name="product-price-lists"></a>Ürün fiyat listeleri

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

 Project Operations'taki **Ürün fiyatı listeleri** ve ilgili fiyat listesi maddesi varlıkları, ürün tabanlı teklif ve sözleşme satırlarındaki fiyatlandırma ürünleri için işlevselliği destekler. Projelerde kullanılan ürünlerinde, fiyat listesi maddesi kaydetme işlemini kullanılan proje fiyat listeleri için gerçekleştirir. 

Ürünler, ürün kataloğunda varsayılan maliyet ve fiyat listelerine sahip olacak şekilde ayarlanmalıdır. Varsayılan maliyet ve liste fiyatlarını yapılandırmak için liste fiyatı, standart maliyet ve geçerli maliyeti kullanın. Varsayılan liste fiyatları yalnızca, bir teklif satırında veya proje sözleşmesi satırında, yalnızca siste, teklif veya proje sözleşmesiyle ilgili ürün fiyatı listesinde bu ürün için bir fiyat listesi satırı bulamazsa kullanılır.

Ürün kataloğu satırlarının maliyet fiyatı teklifler arasında değiştirilebilir. Maliyetleri doğru şekilde izlemezseniz, proje görevlendirmelerinde operasyon karlarını belirleyemeyeceğiniz için bu özellik önemlidir. Varsayılan olarak ürünün standart maliyeti maliyet fiyatı olarak kullanılır. Ancak, bu teklif için farklı bir maliyet fiyatı varsa, teklif satırındaki varsayılan maliyet fiyatı güncelleştirilebilir.

## <a name="price-list-items"></a>Fiyat listesi öğeleri

Ürün kataloğundaki ürünleri farklı fiyat listelerine ekleyebilirsiniz. Ürünlerin fiyat listesi satırları her zaman belirli bir birime başvuruda bulunur. Fiyat listesi öğelerindeki bir ürünün fiyatlandırması para birimi tutarı olarak yapılandırılabilir. Bunun yerine liste fiyatı, geçerli maliyet veya standart maliyetin bir işlevi olarak da yapılandırılabilir.

Ürün fiyatları liste fiyatı, standart maliyet veya geçerli maliyet işlevi olarak yapılandırıldığında, fiyatlandırma işlevi çeşitli yuvarlama seçeneklerini destekler. Birden çok fiyatlandırma yönteminden ve yuvarlama seçeneğinden yararlanmaya ek olarak, indirim listelerini fiyat listesi öğeleriyle ilişkilendirebilirsiniz. 

 
## <a name="default-product-price-list"></a>Varsayılan ürün fiyat listesi
Her müşteri kaydı, müşterinin para birimiyle eşleşen bir fiyat listesi belirtebileceğiniz bir **Varsayılan Fiyat Listesi** alanına sahiptir. Bu alana otomatik olarak bir varsayılan değer girilmez. Belirli bir müşteriyle özel bir fiyatlandırma anlaşması varsa, bu alanı kullanarak bir fiyat listesini bu müşteriyle ilişkilendirebilirsiniz.

Fırsat, Teklif ve Proje Sözleşmesi varlıkları varsayılan ürün fiyatı listelerini girmek için aşağıdaki sırayı kullanır. Aynı sıra proje fiyat listeleri için de kullanılır.

1.  Teklif
2.  Fırsat
3.  Müşteri
4.  Genel ayarlar 

Varsayılan olarak, teklif satırındaki **Ürün** alanı, teklifin ürün fiyatı listesindeki tüm etkin ürünleri listeler. Ürün devre dışı bırakılmışsa veya bir taslak ürünse, fiyat listesinde olsa bile listelenmez. 

Ürün kataloğu satırları, proje sözleşmesi için oluşturulan ilk faturaya fatura satırları olarak eklenir. Bir taslak faturada, bu fatura satırları silinebilir. Bu durumda, satırlar faturalanıncaya veya fatura müşteriye gönderilene kadar bir sonraki faturada görüntülenir. Ürün fatura satırındaki kısmi bir miktarı faturalayamazsınız. Proje sözleşmesindeki ürün satırları faturalandığında, fiili değerler oluşturulur. Ancak, bu fiili değerler ilgili proje varlığına bağlanmaz. Başka bir deyişle, ürün tabanlı proje sözleşme satırları proje tabanlı kullanımdan bağımsızdır. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
