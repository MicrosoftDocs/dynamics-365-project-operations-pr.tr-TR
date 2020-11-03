---
title: Fiyat listelerini ayarlama
description: Bu konuda, maliyet ve satış fiyatı listelerini ayarlama hakkında bilgi verilmektedir.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 578f5641659a5d05785781afe7055fe4449cf799
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088147"
---
# <a name="set-up-price-lists"></a>Fiyat listelerini ayarlama

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Dynamics 365 Project Operations'taki fiyat listeleri oranlar kataloğunu temsil eder. Hızlı maliyet, satış ve fatura oranları oranları. Fiyat listesinin maliyet oranlarını mı, yoksa Satışlar ve fatura oranlarını ifade etmek istediğinize bağlı olarak, Fiyat listesi bağlamı **Satış** veya **maliyet** olur.

Aşağıdaki uzantılar Project Operations'a Işlemlerine özeldir ve Dynamics 365 Sales'den fiyat listelerine uygulanır.

- **Bağlam** : Bu alan, **maliyet** ve **satış** desteklenen değerlerine sahiptir. Değer, **Satın alma** desteklenmez. **Maliyet** fiyat listesi oluşturmak için içeriği maliyet olarak ayarlayın veya içeriği **Satış** fiyatı listesi için satış olarak ayarlayın. Maliyet fiyatı listeleri tahmin ve gerçek değerler kayıtlarında maliyet türüyle ilgili fiyatı çözümler. Satış fiyatı listeleri, faturalandıredilmemiş ve Faturalanan satış tiplerinin tahmini ve gerçek kayıtlarında fiyatı çözümler.
- **Zaman birimi** : Bu, Fiyat listesi için Ilgili **rol fiyatı** tablosunda fiyatın ayarlandığı varsayılan zaman birimidir.
- **Fiyat Listesi Varlığı** : Bu gizli alan, teklif veya sözleşme özgü fiyat listelerini standart olan ve genel olarak uygulanabilen farklılaştırmanıza yönelik proje işlemleri gereğidir.

## <a name="price-list-header"></a>Fiyat Listesi üst bilgisi

Aşağıdaki tabloda Project Operations için benzersiz olan bir fiyat listesinin **Genel** sekmesindeki alanlar veya satıştaki fiyat listelerinden davranış içinde belirgin değişiklikler vardır.

| Alan | Konum | İlgi, amaç ve kılavuz | Aşağı yönlü etki |
| --- | --- | --- | --- |
| Veri Akışı Adı | **Genel** sekme ve **Hızlı Oluşturma** formları | Fiyat listesi kimliği. | Fiyat listesi, bu değeri tüm liste sayfalarında ve açılan seçeneklerle gösterilir.|
| Bağlam | **Genel** sekme ve **Hızlı Oluşturma** formları | Bu alan **maliyet** veya **satış** olarak ayarlanabilir. | **Maliyet** tahminleri ve maliyet fiili değerleri için fiyatı aramak amacıyla maliyet ayarı atanan bir fiyat listesi kullanılır. Satış tahminleri ve satış fiili değerleri için fiyatı aramak amacıyla **Satış** ayarı atanan bir fiyat listesi kullanılır. Yalnızca bir müşteri, proje teklif veya proje sözleşme için yalnızca içeriği **Satış** olarak ayarı yapılmış fiyat listeleri bir proje fiyat listesine iliştirilebilir. |
| Başlangıç Tarihi | **Genel** sekme ve **Hızlı Oluşturma** formları | Fiyat listesinin geçerli olduğu dönemin başlangıç tarihi. | **Bitiş tarihi** alanıyla birlikte bu alan belirli bir tahmin veya gerçek satır için hangi fiyat listesinin geçerli olduğunu belirlemek için kullanılır. |
| Bitiş Tarihi | **Genel** sekme ve **Hızlı Oluşturma** formları | Fiyat listesinin geçerli olduğu dönemin bitiş tarihi. | **Başlanıgç tarihi** alanıyla birlikte bu alan belirli bir tahmin veya gerçek satır için hangi fiyat listesinin geçerli olduğunu belirlemek için kullanılır. |
| Para birimi | **Genel** sekme ve **Hızlı Oluşturma** formları | Bu alan, bu fiyat listesiyle ilgili her rol, kategori veya fiyat listesi öğesi satırındaki para birimini varsayılan olarak kullanır. | **Satış** fiyatı listelerinde, roller, Kategoriler veya fiyat listesi öğesi satırları bu para birimi dışındaki herhangi bir para birimi içinde oluşturulamaz. **Maliyet** fiyatı listelerinde, herhangi bir para biriminde bir rol fiyatı satırı oluşturabilirsiniz. Burada tanımlanan para birimi varsayılan olarak kullanılır. İlgili rol fiyatları olan Kullanıcı Kurulumu, herhangi bir para biriminde işçilik maliyet oranı kurulumunu etkinleştirmek için bu değeri geçersiz kılabilir. Kategori maliyet oranları ve fiyat listesi madde maliyetleri yalnızca burada tanımlanan para birimi cinsinden ayarlanabilir. |
| Zaman Birimi | **Genel** sekme ve **Hızlı Oluşturma** formları | Bu alan, bu fiyat listesiyle ilgili her rol öğesi satırındaki saat birimini varsayılan olarak kullanır. | Bu alan değeri yalnızca ilgili rol fiyatı kurulumunda kullanılır. **Maliyet** ve **Satış** fiyatı listelerinde, herhangi bir zaman biriminde bir rol fiyatı satırı oluşturabilirsiniz. Burada tanımlanan zaman birimi varsayılan olarak kullanılır. İlgili rol fiyatları olan Kullanıcı Kurulumu, herhangi bir zaman biriminde işçilik maliyet ve fatura oranı kurulumunu etkinleştirmek için bu değeri geçersiz kılabilir. |
| Veri Akışı Açıklaması | **Genel** sekme ve **Hızlı Oluşturma** formları | Bu bir metin alanıdır ve fiyat listesinin çok satırlı bir açıklamasını kullanmanıza olanak sağlar. | Bu alan, ilgili fiyat listeleri içeren çeşitli varlıklarda fiyat listesindeki **ilişkili** görünümlerde gösterilir. |
