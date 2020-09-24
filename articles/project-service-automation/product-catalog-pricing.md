---
title: Ürün kataloğu fiyatlandırması
description: Bu konu, ürün kataloğu fiyatlandırmasının Dynamics 365 Project Service Automation'da (PSA) çalışma şekli hakkında bilgi sağlar.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: f1a8b1af-0767-4d83-82ef-367aac7a630f
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8f296f6af9f60f40b726fddb095785dfb9831dc3
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756720"
---
# <a name="product-catalog-pricing"></a>Ürün kataloğu fiyatlandırması 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


Fiyat listeleri ve fiyat listesi öğesi varlıkları, ürün kataloğu fiyatlandırmasını destekler. Çoğu bölüm için bu işlevsellik proje teklifleri ve proje sözleşmelerindeki katalog tabanlı satırlar için kullanılır.

Proje tabanlı satırlarda, sözleşme kazanılan anlaşmayı temsil eder. Anlaşma işlemi genellikle kazanmadan önce olduğundan, teklife iliştirilen fiyatlandırma her zaman yeni bir fiyat listesine olduğu gibi kopyalanır ve sözleşmeye iliştirilen fiyattır. Bu yeni fiyat listesi sözleşmenin kapsamı dışında değiştirilemez. Bu sınırlama, ana fiyat listesinde ortaya çıkan herhangi bir fiyat değişikliği üzerinde anlaşılan bir oran kartının korunmasına yardımcı olur.

Ürünler, ürün kataloğunda varsayılan maliyet ve fiyat listelerine sahip olacak şekilde ayarlanmalıdır. Varsayılan maliyet ve liste fiyatlarını yapılandırmak için liste fiyatı, standart maliyet ve geçerli maliyeti kullanmanız gerekir. Varsayılan liste fiyatları yalnızca, bir teklif satırında veya proje sözleşmesi satırında, yalnızca siste, teklif veya proje sözleşmesiyle ilgili ürün fiyatı listesinde bu ürün için bir fiyat listesi satırı bulamazsa kullanılır.

Ürün kataloğu satırlarının maliyet fiyatı teklifler arasında değiştirilebilir. Maliyetleri doğru şekilde izlemezseniz, proje görevlendirmelerinde operasyon karlarını belirleyemeyeceğiniz için bu özellik önemlidir. Varsayılan olarak ürünün standart maliyeti maliyet fiyatı olarak kullanılır. Ancak, bu teklif için farklı bir maliyet fiyatı varsa, teklif satırındaki varsayılan maliyet fiyatı güncelleştirilebilir.

## <a name="price-list-items"></a>Fiyat listesi öğeleri

Ürün kataloğundaki ürünleri farklı fiyat listelerine ekleyebilirsiniz. Ürünlerin fiyat listesi satırları her zaman belirli bir birime başvuruda bulunur. Fiyat listesi öğelerindeki bir ürünün fiyatlandırması para birimi tutarı olarak yapılandırılabilir. Bunun yerine liste fiyatı, geçerli maliyet veya standart maliyetin bir işlevi olarak da yapılandırılabilir.

Fiyatlar fiyat listesi fiyatı, standart maliyet veya geçerli maliyet işlevi olarak yapılandırıldığında, PSA çeşitli yuvarlama seçeneklerini destekler. Birden çok fiyatlandırma yönteminden ve yuvarlama seçeneğinden yararlanmaya ek olarak, indirim listelerini fiyat listesi öğeleriyle ilişkilendirebilirsiniz. 

> ![Katalogdan ürünleri farklı fiyat listelerine ekleme](media/basic-guide-16.png)

**Proje Teklifi** sayfasında **Özel fiyatlandırma oluştur** oluştur seçeneğini belirleyerek bir teklif için yeni bir özel fiyat listesi oluşturduğunuzda, PSA fiyat listesinin bir kopyasını oluşturur ve yeni fiyat listesinin başlığındaki **Varlık** alanı **Satış Varlığı** olarak ayarlanır. Yeni fiyat listesinin adı, teklifin adı ve bir zaman damgasıyla birlikte eklenir. Özel fiyatlandırma kullanan teklifler için ek gözden geçirme ve onaylar tetiklemek için yeni fiyat listesinin adını ve teklifin adını özel iş akışlarında da kullanabilirsiniz.

 
## <a name="default-product-price-list"></a>Varsayılan ürün fiyat listesi
Her müşteri kaydı, müşterinin para birimiyle eşleşen bir fiyat listesi belirtebileceğiniz bir **Varsayılan Fiyat Listesi** alanına sahiptir. PSA'da, bu alana otomatik olarak bir varsayılan değer girilmez. Belirli bir müşteriyle özel bir fiyatlandırma anlaşması varsa, bu alanı kullanarak bir fiyat listesini bu müşteriyle ilişkilendirebilirsiniz.

Fırsat, Teklif ve Proje Sözleşmesi varlıkları varsayılan ürün fiyatı listelerini girmek için aşağıdaki sırayı kullanır. Aynı sıra proje fiyat listeleri için de kullanılır.

1.  Teklif
2.  Fırsat
3.  Müşteri
4.  PSA için genel ayarlar

Varsayılan olarak, teklif satırındaki **Ürün** alanı, teklifin ürün fiyatı listesindeki tüm etkin ürünleri listeler. Ürün devre dışı bırakılmışsa veya bir taslak ürünse, fiyat listesinde olsa bile listelenmez. 

Ürün kataloğu satırları, proje sözleşmesi için oluşturulan ilk faturaya fatura satırları olarak eklenir. Bir taslak faturada, bu fatura satırları silinebilir. Bu durumda, satırlar faturalanıncaya veya fatura müşteriye gönderilene kadar bir sonraki faturada görüntülenir. PSA'da, ürün fatura satırındaki kısmi bir miktarı faturalayamazsınız. Proje sözleşmesindeki ürün satırları faturalandığında, fiili değerler oluşturulur. Ancak, bu fiili değerler ilgili proje varlığına bağlanmaz. Başka bir deyişle, ürün tabanlı proje sözleşme satırları proje tabanlı kullanımdan bağımsızdır. PSA, projelerdeki malzeme tüketimini izlemez.