---
title: Özel alanları fiyatlandırma boyutları olarak ayarlama
description: Bu konuda, özel alanları kullanarak fiyatlandırma boyutlarının ayarlanması hakkında bilgi verilmektedir.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 67e891d8576cd92f48466929fc53fe8a4203d72d
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119442"
---
# <a name="set-up-custom-fields-as-pricing-dimensions"></a>Özel alanları fiyatlandırma boyutları olarak ayarlama

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Başlamadan önce, bu konunun [Özel alanlar ve varlıklar oluşturma](create-custom-fields-entities-pricing-dimensions.md) ve [Fiyat ayarı ve işlem tabanlı varlıklara gerekli özel alanlar ekleme](add-custom-fields-price-setup-transactional-entities.md) konu başlıklarındaki yordamları tamamladığınızı varsaydığını bilmeniz gerekir. Bu yordamları tamamlamadıysanız geri dönüp tamamlayın ve ardından bu konuya geri dönün. 

Bu konuda, özel fiyatlandırma boyutlarının ayarlanması hakkında bilgi verilmektedir. **Parametreler** sayfasındaki **Tutar Tabanlı Fiyatlandırma Boyutları** sekmesinde, fiyatlandırma boyutları varlıklarındaki kayıtları gösteren sekmedeki ızgarayı not edin. Varsayılan olarak, bu sekmedeki ızgarada iki satır vardır:

- **msdyn_resourcecategory** (Rol)
- **msdyn_OrganizationalUnit** (Kuruluş Birimi)

> [!IMPORTANT]
> Bu satırları silmeyin. Ancak bu satırlara ihtiyacınız yoksa, **Maliyet için Geçerli**, **Satış için Geçerli** ve **Satın Alma için Geçerli** seçeneklerini **Hayır** olarak ayarlayarak belirli bir bağlamda geçersiz duruma getirebilirsiniz. Bu öznitelik değerlerinin **Hayır** olarak ayarlanması alanın bir fiyatlandırma boyutu olmamasıyla aynı etkiye sahiptir.

Bir alanın fiyatlandırma boyutu olması için:

- **Rol Fiyatı** ve **Rol Fiyatı kar payı** varlıklarında bir alan olarak oluşturulmalıdır. Bunun nasıl yapılacağı hakkında daha fazla bilgi için [Fiyat ayarı ve işlem tabanlı varlıklara özel alanlar ekleme](add-custom-fields-price-setup-transactional-entities.md) bölümüne bakın.
- **Fiyatlandırma Boyutu** tablosunda bir satır olarak oluşturulmalıdır. Örneğin, fiyatlandırma boyutu satırlarını aşağıdaki grafikte gösterildiği şekilde ekleyin. 

Kaynak Çalışma saatlerinin (**msdyn_resourceworkhours**) kar payı tabanlı bir boyut olarak eklenir ve **Kar Payı Tabanlı Fiyatlandırma Boyutu** sekmesinde ızgara olarak eklenir.

> [!IMPORTANT]
> Bu tablodaki var olan veya yeni, tüm fiyat boyutu verileri ancak önbellek yenilendikten sonra fiyatlandırma iş mantığına yansıtılır. Önbellek yenileme işlemi 10 dakika kadar sürebilir. Fiyatlandırma Boyutu verilerinde yapılan değişiklikler sonucunda fiyat varsayılan mantığındaki değişiklikleri görmek için bu sürenin geçmesini bekleyin.


## <a name="attributes-of-the-pricing-dimensions-table"></a>Fiyatlandırma Boyutları Öznitelikleri tablosu
Aşağıdaki bölümlerde **Fiyatlandırma Boyutları** tablosundaki farklı öznitelikler hakkında bilgi sağlanmaktadır.

### <a name="pricing-dimension-name"></a>Fiyatlandırma Boyutu Adı
Bu değer özel fiyatlandırma boyutlarının **Rol Fiyatı** tablosuna eklenen alanın şema adıyla aynı olmalıdır. **Rol Fiyatı** tablosuna alan hakkında daha fazla bilgi için [Fiyat ayarı ve işlem tabanlı varlıklara özel alanlar ekleme](add-custom-fields-price-setup-transactional-entities.md) bölümüne bakın.

### <a name="type-of-dimension"></a>Boyut türü
İki tür fiyatlandırma boyutu vardır:
  
  - **Tutar tabanlı boyutlar**: Giriş bağlamlarından alınan boyut değerleri **Rol Fiyatı** satırındaki boyut değerleriyle eşleştirilir ve fiyat/maliyet varsayılan olarak doğrudan **Rol Fiyatı** tablosundan ayarlanır.
  - **Kar payı tabanlı boyutlar**: Bunlar fiyat/maliyet almak için aşağıdaki 3 adımlı işlemi kullanacağı boyutlardır:
 
    1. Taban fiyatı almak için giriş bağlamından kar payı tabanlı olmayan boyut değerleri Rol Fiyatı satırıyla eşleştirilir.
    2. Kar payı yüzdesi almak için giriş bağlamından tüm boyut değerleri **Rol Fiyatı Kar Payı** satırıyla eşleştirilir.
    3. İkinci adımda elde edilen kar payı yüzdesi son fiyat/maliyet değerine ulaşmak için ilk adımdaki **Rol Fiyatı** tablosundan alınan taban fiyata uygulanır.
   
   Aşağıdaki tabloda fiyat kar paylarını hesaplama gösterilmiştir.
  
| Rol        | Kuruluş Birimi    |İş Konumu      |Standart Başlık      |Kaynak Çalışma Saatleri      |  Kar Payı|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | Contoso Hindistan|Yerinde            |                    |Fazla Mesai                 |15     |
|             | Contoso Hindistan|Yerel             |                    |Fazla Mesai                 |10     |
|             | Contoso ABD   |Yerel             |                    |Fazla Mesai                 |20     |


Taban fiyatı 100 ABD Doları olan Contoso Hindistan'dan bir kaynak yerinde çalışıyorsa ve zaman girişinde 8 saat Normal ve 2 saat de fazla mesai girişi yaparsa, fiyatlandırma altyapısı 8 saat için taban fiyatı olarak 100 ABD Doları kullanarak 800 ABD Doları elde edilir. 2 saatlik fazla mesai için 100 ABD Doları değerindeki taban fiyata %15 kar payı eklenir ve 115 ABD Doları elde edilir. Toplamda maliyet 230 USD Doları kaydedilir.

### <a name="applicable-to-cost"></a>Maliyet için Geçerli 
Bu değer **Evet** olarak ayarlandığında maliyet ve kar payı oranları alınırken **Rol Fiyatı** ve **Rol Fiyatı Kar Payı** ile eşleştirmek için giriş bağlamından gelen boyut değerinin kullanılması gerektiğini gösterir.

### <a name="applicable-to-sales"></a>Satış için Geçerli
Bu değer **Evet** olarak ayarlandığında fatura ve kar payı oranları alınırken **Rol Fiyatı** ve **Rol Fiyatı Kar Payı** ile eşleştirmek için giriş bağlamından gelen boyut değerinin kullanılması gerektiğini gösterir.

### <a name="applicable-to-purchase"></a>Satın Alma için Geçerli
Bu değer **Evet** olarak ayarlandığında satınalma fiyatı alınırken **Rol Fiyatı** ve **Rol Fiyatı Kar Payı** ile eşleştirmek için giriş bağlamından gelen boyut değerinin kullanılması gerektiğini gösterir. Alt üstlenici senaryoları desteklenmez, bu nedenle bu alan kullanılmaz. 

### <a name="priority"></a>Öncelik
Boyut önceliğinin ayarlanması fiyatlandırma işlevinin giriş boyutu değerleri ve **Rol Fiyatı** veya **Rol Fiyatı Kar Payı** tablolarından alınan değerler arasında tam bir eşleşme bulamadığında bile bir fiyat üretmesine yardımcı olur. Bu senaryoda boyutları öncelik sıralarına göre ölçerek eşleşmeyen boyut değerleri için null değerler kullanılır.

- **Maliyet Önceliği**: Bir boyutun maliyet önceliği değeri maliyet fiyatları ayarıyla eşleştirilirken bu boyutun ağırlığını gösterir. **Maliyet Önceliği** değeri **Maliyet için Geçerli** olan boyutlar arasında benzersiz olmalıdır.
- **Satış Önceliği**: Bir boyutun satış önceliği değeri satış fiyatları veya fatura oranları ayarıyla eşleştirilirken bu boyutun ağırlığını gösterir. **Satış Önceliği** değeri **Satış için Geçerli** olan boyutlar arasında benzersiz olmalıdır.
