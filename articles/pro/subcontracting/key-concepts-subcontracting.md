---
title: Alt sözleşme temel kavramları
description: Bu konu, Microsoft Dynamics 365 Project Operations'ta taşeronluk için geçerli olan bazı anahtar kavramları açıklar.
author: rumant
ms.date: 08/03/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 01d2e57b99015c346be15e3504440c14cb9a54e24215c0b1c052c5112f4b940a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994300"
---
# <a name="key-concepts-in-subcontracting"></a>Alt sözleşme temel kavramları

[!include [banner](../../includes/dataverse-preview.md)]

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Konu, Microsoft Dynamics 365 Project Operations'ta taşeronluk işlevini kullanmaya başlamadan önce dikkat edilmesi gereken bazı anahtar kavramları açıklar.

## <a name="contracting-unit-on-the-subcontract"></a>Taşeronda sözleşme birimi

Sözleşme birimi, nihai projenin teslimine sahip olan bölümü veya uygulamayı temsil eder. Sözleşme birimi aynı zamanda satıcıyla sözleşme ilişkisine giren bölümdür.

## <a name="purchase-currency"></a>Satın alma para birimi

Project Operations'ta, satın alma para birimi taşeronun oluşturulduğu para birimidir. Aynı zamanda bir projedeki taşeron maliyetlerinin kaydedildiği para birimidir. Satınalma para birimi proje para biriminden farklı olabilir ve proje para birimi de satış para biriminden farklı olabilir.

## <a name="billing-methods-on-subcontract-lines"></a>Taşeron satırlarındaki faturalama yöntemleri

Projeler için genellikle sabit ücret ve tüketime dayalı sözleşme modelleri vardır. Project Operations, satış ve satınalma bağlamlarında bu faturalama yöntemlerini destekler. Bir satın alma işlemi için faturalama yöntemleri aşağıdaki şekilde çalışır:

- **Zaman ve Malzeme** – Bir taşeron hattı **Zaman ve Malzeme** faturalandırma yöntemini kullandığında, taşeronlar bu proje üzerinde çalışırken ve zaman kaydettikçe zaman maliyeti projeye kaydedilir. Taşeronlardan gelen bu maliyet hareketleri daha sonra satıcı faturalarındaki satır maddeleri ile eşleştirilir. Bu modelde, Project Operations'ta kullanan proje yöneticileri, satıcı fatura satırlarını kaydedilen ve onaylanan taşeron süresiyle eşleştirebilir ve doğrulayabilir. Doğrulama tamamlandıktan sonra, onaydan sonra kaydedilen önceki maliyet fiili değerleri tersine çevrilir ve projede satıcı faturasını temel alan yeni maliyet fiili değerleri oluşturulur.
- **Sabit Fiyat** – Bu sabit ücretli sözleşme modelinde, satıcı faturaları sabit kilometre taşlarını temel alır. Ancak, taşeron kaynakları da zamanı bildirebilir. Saat daha sonra proje yöneticisi tarafından gözden geçirilip onaylanır. Onaylandığında, Project Operations projede geçici maliyet fiili değerleri oluşturur. Satıcı bir kilometre taşı için fatura gönderdikten sonra, proje yöneticisi daha önce kaydedilmiş maliyet fiili değerleriyle kilometre taşını eşleştirebilir. Doğrulama tamamlandığında, maliyet fiili değerleri tersine çevrilir ve kilometre taşı tabanlı maliyet kaydedilir.

## <a name="project-price-lists-on-subcontracts"></a>Alt sözleşmelerindeki proje fiyat listeleri

Proje fiyat listeleri, zaman, gider ve projeyle ilgili diğer bileşenler için satınalma fiyatlarını ayarlamak için kullanılan fiyat listeleridir. Her biri Project Operations'ta kendi geçerlilik düzeyine sahip olabilecek birden fazla fiyat listesi olabilir. Project Operations, bir taşeron için proje fiyat listelerinde çakışan geçerlilik tarihlerini desteklemez.

## <a name="transaction-classes-on-subcontracts"></a>Taşeronlardaki hareket sınıfları

Project Operations dört işlem sınıfı türünü destekler:

- Zaman
- Gider
- Malzeme
- Ücret

Satınalma maliyetleri yalnızca **Zaman**, **Gider** ve **Malzeme** hareket sınıflarında tahmin edilebilir ve tahakkuk edebilir. **Ücret** yalnızca gelire özel bir işlem sınıfıdır ve satın alma içeriğinde kullanılamaz.

## <a name="purchase-pricing-dimensions"></a>Satın alma fiyatlandırma boyutları

Fiyatlandırma boyutları, satınalma fiyatı kurulumu ve zaman hareketlerinde varsayılan olarak hangi özniteliklerin kullanılmayacağına karar vermenizi sağlar. Satınalma ile ilgili olarak, Project Operations satınalma fiyatı kurulumu ve temerrüde düşme için yalnızca sabit boyut kümelerini destekler. Satınalma fiyatı kurulumu ve taşeron satırlarında ve taşeron zaman hareketlerinde varsayılan olarak, öznitelikler **Rol** ve **Rezerve Edilebilir Kaynak**'tır.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
