---
title: Özel alanları fiyatlandırma boyutları olarak ayarlama
description: Bu konuda, özel fiyatlandırma boyutlarının ayarlanması hakkında bilgi verilmektedir.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/20/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 7576f73240a7366175d7be39815583a5c9cf7187
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150377"
---
# <a name="setting-up-custom-fields-as-pricing-dimensions"></a>Özel alanları fiyatlandırma boyutları olarak ayarlama 

[!include [banner](../includes/psa-now-project-operations.md)]

Başlamadan önce, bu konunun [Özel alanlar ve varlıklar oluşturma](create-custom-fields-entities.md) ve [Fiyat ayarı ve işlem tabanlı varlıklara özel alanlar ekleme](field-references.md) konu başlıklarındaki yordamları tamamladığınızı varsaydığını bilmeniz gerekir. Bu yordamları tamamlamadıysanız geri dönüp tamamlayın ve ardından bu konuya geri dönün. 

Bu konuda, özel fiyatlandırma boyutlarının ayarlanması hakkında bilgi verilmektedir. Project Service web arabiriminde **Parametreler** sayfasındaki **Tutar Tabanlı Fiyatlandırma Boyutları** sekmesi fiyatlandırma boyutu varlıklarındaki kayıtları gösterir. Varsayılan olarak Project Service kurulumu bu sekmede ızgarasında 2 satır oluşturur:

- **msdyn_resourcecategory** (Rol)
- **msdyn_OrganizationalUnit** (Kuruluş Birimi)

> [!IMPORTANT]
> Bu satırları silmeyin. Ancak bu satırlara ihtiyacınız yoksa, **Maliyet için Geçerli**, **Satış için Geçerli** ve **Satın Alma için Geçerli** seçeneklerini **Hayır** olarak ayarlayarak belirli bir bağlamda geçersiz duruma getirebilirsiniz. Bu öznitelik değerlerinin **Hayır** olarak ayarlanması alanın bir fiyatlandırma boyutu olmamasıyla aynı etkiye sahiptir.

Bir alanın fiyatlandırma boyutu olması için:

- **Rol Fiyatı** ve **Rol Fiyatı kar payı** varlıklarında bir alan olarak oluşturulmalıdır. Bunun nasıl yapılacağı hakkında daha fazla bilgi için [Fiyat ayarı ve işlem tabanlı varlıklara özel alanlar ekleme](field-references.md) bölümüne bakın.
- **Fiyatlandırma Boyutu** tablosunda bir satır olarak oluşturulmalıdır. Örneğin, fiyatlandırma boyutu satırlarını aşağıdaki grafikte gösterildiği şekilde ekleyin. 

![Tutar Tabanlı Fiyatlandırma Boyutu Satırları](media/Amt-based-PD.png)

Kaynak Çalışma saatlerinin (**msdyn_resourceworkhours**) kar payı tabanlı bir boyut olarak eklendiğini ve **Kar Payı Tabanlı Fiyatlandırma Boyutu** sekmesinde ızgara olarak eklendiğini unutmayın.

![Kar Payı Tabanlı Fiyatlandırma Boyutu Satırları](media/Markup-based-PD.png)

> [!IMPORTANT]
> Bu tablodaki var olan veya yeni, tüm fiyat boyutu verileri ancak önbellek yenilendikten sonra Project Service fiyatlandırma iş mantığına yansıtılır. Önbellek yenileme işlemi 10 dakika kadar sürebilir. Fiyatlandırma Boyutu verilerinde yapılan değişiklikler sonucunda fiyat varsayılan mantığındaki değişiklikleri görmek için bu sürenin geçmesini bekleyin.


## <a name="attributes-of-the-pricing-dimensions-table"></a>Fiyatlandırma Boyutları Öznitelikleri tablosu
Aşağıdaki bölümlerde **Fiyatlandırma Boyutları** tablosundaki farklı öznitelikler hakkında bilgi sağlanmaktadır.

### <a name="pricing-dimension-name"></a>Fiyatlandırma Boyutu Adı
Bu değer özel fiyatlandırma boyutlarının **Rol Fiyatı** tablosuna eklenen alanın şema adıyla aynı olmalıdır. **Rol Fiyatı** tablosuna alan hakkında daha fazla bilgi için [Fiyat ayarı ve işlem tabanlı varlıklara özel alanlar ekleme](field-references.md) bölümüne bakın.

### <a name="type-of-dimension"></a>Boyut türü
İki tür fiyatlandırma boyutu vardır:
  
  - **Tutar tabanlı boyutlar**: Giriş bağlamlarından alınan boyut değerleri **Rol Fiyatı** satırındaki boyut değerleriyle eşleştirilir ve fiyat/maliyet varsayılan olarak doğrudan **Rol Fiyatı** tablosundan ayarlanır.
  - **Kar payı tabanlı boyutlar**: Bunlar Project Service'in fiyat/maliyet almak için aşağıdaki 3 adımlı işlemi kullanacağı boyutlardır
 
    1. Project Service taban fiyatı almak için giriş bağlamından kar payı tabanlı olmayan boyut değerlerini Rol Fiyatı satırıyla eşleştirir.
    2. Project Service kar payı yüzdesi almak için giriş bağlamından tüm boyut değerlerini **Rol Fiyatı Kar Payı** satırıyla eşleştirir.
    3. Project Service ikinci adımda elde edilen kar payı yüzdesini son fiyat/maliyet değerine ulaşmak için ilk adımdaki **Rol Fiyatı** tablosundan alınan taban fiyatla eşleştirir.
   
   Aşağıdaki tabloda fiyat kar paylarını hesaplama gösterilmiştir.
  
| Rol        | Kuruluş Birimi    |İş Konumu      |Standart Başlık      |Kaynak Çalışma Saatleri      |  Kar Payı|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | Contoso Hindistan|Yerinde            |                    |Fazla Mesai                 |15     |
|             | Contoso Hindistan|Yerel             |                    |Fazla Mesai                 |10     |
|             | Contoso ABD   |Yerel             |                    |Fazla Mesai                 |20     |


Taban fiyatı 100 ABD Doları olan Contoso Hindistan'dan bir kaynak yerinde çalışıyorsa ve zaman girişinde 8 saat Normal ve 2 saat de fazla mesai girişi yaparsa, Project Service fiyatlandırma altyapısı 8 saat için taban fiyatı olarak 100 ABD Doları kullanarak 800 ABD Doları elde edilir. 2 saatlik fazla mesai için 100 ABD Doları değerindeki taban fiyata %15 kar payı eklenir ve 115 ABD Doları elde edilir. Toplamda maliyet 230 USD Doları kaydedilir.

### <a name="applicable-to-cost"></a>Maliyet için Geçerli 
Bu değer **Evet** olarak ayarlandığında maliyet ve kar payı oranları alınırken **Rol Fiyatı** ve **Rol Fiyatı Kar Payı** ile eşleştirmek için giriş bağlamından gelen boyut değerinin kullanılması gerektiğini gösterir.

### <a name="applicable-to-sales"></a>Satış için Geçerli
Bu değer **Evet** olarak ayarlandığında fatura ve kar payı oranları alınırken **Rol Fiyatı** ve **Rol Fiyatı Kar Payı** ile eşleştirmek için giriş bağlamından gelen boyut değerinin kullanılması gerektiğini gösterir.

### <a name="applicable-to-purchase"></a>Satın Alma için Geçerli
Bu değer **Evet** olarak ayarlandığında satınalma fiyatı alınırken **Rol Fiyatı** ve **Rol Fiyatı Kar Payı** ile eşleştirmek için giriş bağlamından gelen boyut değerinin kullanılması gerektiğini gösterir. Şu anda Project Service alt üstlenici senaryolarını desteklemediğinden bu alan kullanılmamaktadır. 

### <a name="priority"></a>Öncelik
Boyut önceliğinin ayarlanması Project Service fiyatlandırma işlevinin giriş boyutu değerleri ve **Rol Fiyatı** veya **Rol Fiyatı Kar Payı** tablolarından alınan değerler arasında tam bir eşleşme bulamadığında bile bir fiyat üretmesine yardımcı olur. Bu senaryoda Project Service boyutları öncelik sıralarına göre ölçerek eşleşmeyen boyut değerleri için null değerler kullanır.

- **Maliyet Önceliği**: Bir boyutun maliyet önceliği değeri maliyet fiyatları ayarıyla eşleştirilirken bu boyutun ağırlığını gösterir. **Maliyet Önceliği** değeri **Maliyet için Geçerli** olan boyutlar arasında benzersiz olmalıdır.
- **Satış Önceliği**: Bir boyutun satış önceliği değeri satış fiyatları veya fatura oranları ayarıyla eşleştirilirken bu boyutun ağırlığını gösterir. **Satış Önceliği** değeri **Satış için Geçerli** olan boyutlar arasında benzersiz olmalıdır.
