---
title: Fiyat ayarı ve geçiş varlıklarına özel alanlar ekleme
description: Bu konu varlıklara, formlara ve görünümlere gerekli özel alan başvurularının nasıl ekleneceği hakkında bilgi sağlar.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a7268eb33c80f5e35d2ef21a8f4c7ed7ba322e27
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000595"
---
# <a name="add-required-custom-fields-to-price-setup-and-transactional-entities"></a>Fiyat ayarı ve geçiş varlıklarına özel alanlar ekleme

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Bu konu, [Fiyatlandırma boyutu olarak kullanılmak üzere özel alanlar ve varlıklar oluşturma](create-custom-fields-entities-pricing-dimensions.md) konusundaki yordamları tamamladığınızı varsayar. Bu yordamları tamamlamadıysanız geri dönüp tamamlayın ve ardından bu konuya geri dönün. 

Bu konuda yordamlar, gerekli özel alan başvurularının varlıklara ve form ve görünüm gibi kullanıcı arabirimi (UI) öğelerine nasıl ekleneceğini gösterir.

## <a name="add-custom-pricing-dimension-fields"></a>Özel fiyatlandırma boyutu alanları ekleme 
Özel alanlar ve varlıklar oluşturulduktan sonra, sonraki adım başvuru alanları oluşturarak Fiyat ayarı ve işlem varlıklarının herhangi bir özel varlık veya seçenek kümesiyle uyumlu hale getirmektir. Fiyatlandırma boyutları listesinin seçenek kümesi boyutlarına ya da varlık boyutlarına veya her ikisine sahip olmasına bağlı olarak, yalnızca **Seçenek kümesi tabanlı özel fiyatlandırma boyutları**'ndaki veya **Varlık tabanlı özel fiyatlandırma boyutları**'ndaki veya her ikisindeki adımları izleyin.

### <a name="option-set-based-custom-pricing-dimensions"></a>Seçenek kümesi tabanlı özel fiyatlandırma boyutları
Özel bir fiyatlandırma boyutu seçenek kümesi tabanlı ise, temel varlıklara bir alan olarak ekleyin. Aşağıdaki yordamda **Kaynak Çalışma Konumu** ve **Kaynak Çalışma Saatleri** seçenek kümesi tabanlı fiyatlandırma boyutları olarak kullanılır. Bunların öncelikle **Rol fiyatı** ve **Rol Fiyatı Sair Gideri** fiyatlandırma varlıklarına alan olarak eklenmesi gerekir.

1. Proje Operations'da, **Ayarlar** > **Çözümler**'i seçin ve **\<your organization name> fiyatlandırma boyutları** ayarını çift tıklayın. 
2. Çözüm Gezgininde, sol gezinti bölmesinde **Varlıklar > Rol Fiyatı**'nı seçin.
3. **Rol Fiyatı** varlığını genişletin ve **Alanlar**'ı seçin.
4. **Kaynak Çalışma Konumu** konumu adlı yeni bir alan oluşturmak ve alan türü olarak **Seçenek kümesi**'ni seçmek için **Yeni**'yi seçin. 
5. **Varolan bir seçenek kümesini kullan**'ı, **Kaynak Çalışma Konumu** seçenek kümesini seçin ve ardından **Kaydet**'i seçin.
6. Bu alanı **Rol Fiyatı Kar Payı** varlığına eklemek için 1-5 arasındaki adımları yineleyin. 
7. **Kaynak Çalışma Saatleri** seçenek kümesi için 1-5 arasındaki adımları yineleyin.

> [!IMPORTANT]
> Birden çok varlığa bir alan eklediğinizde, tüm varlıklar üzerinde aynı alan adını kullanın. 

> ![Kaynak Çalışma Konumunu Rol Fiyatına ekleme](media/RWL-Field.png)

Bir projeyle ilgili satış ve tahmin aşamalarında, **Normal saatler** ve **Fazla mesai saatleri**'nde **Yerel** ve **Yerinde** çalışmanın tamamlanması için gereken iş çabası tahminleri, Teklif/Projenin değerini tahmin etmek için kullanılır. **Kaynak çalışma konumu** ve **Kaynak çalışma saatleri** alanları **Teklif Satırı Ayrıntısı**, **Sözleşme satırı ayrıntısı**, **Proje takımı üyesi** ve **Tahmin satırı** tahmin varlıklarına eklenir.

1. Proje Operations'da, **Ayarlar** > **Çözümler**'i seçin ve ardından **\<your organization name> fiyatlandırma boyutları** ayarını çift tıklayın. 
2. Çözüm Gezgininde, sol gezinti bölmesinde **Varlıklar > Teklif Satırı Ayrıntısı**'nı seçin.
3. **Teklif satırı ayrıntısı** varlığını genişletin ve **Alanlar**'ı seçin.
4. **Kaynak Çalışma Konumu** konumu adlı yeni bir alan oluşturmak ve alan türünü **Seçenek kümesi** seçmek için **Yeni**'yi seçin. 
5. **Varolan bir seçenek kümesini kullan**'ı ve **Kaynak Çalışma Konumu**'nu seçin ve ardından **Kaydet**'i seçin.
6. Bu alana **Proje sözleşmesi satır ayrıntısı**, **Proje takımı üyesi** ve **Tahmin satırı** varlıklarına eklemek için 1-5 arasındaki adımları yineleyin.
7. **Kaynak Çalışma Saatleri** seçenek kümesi için 1-6 arasındaki adımları yineleyin. 

> ![Kaynak Çalışma Konumunu Tahmin Satırına ekleme](media/RWL-Default-Value.png)

Teslimat ve faturalama için tamamlanmış işin Proje Fiili Değerlerinde **Yerel** mi yoksa **Yerinde** mi gerçekleştirildiğini ve **Normal saatler** veya **Fazla mesai** sırasında mı tamamlandığını belirlemek için doğru olarak fiyatlandırılması gerekir. **Kaynak Çalışma Konumu** ve **Kaynak Çalışma Saatleri** alanlarının **Zaman girişi**, **Fiili değer**, **Fatura Satırı Ayrıntısı** ve **Yevmiye defteri satırı** varlıklarına eklenmesi gerekir.

1. **Ayarlar** > **Çözümler**'i seçin ve ardından **\<your organization name> fiyatlandırma boyutları** ayarını çift tıklayın.
2. Çözüm Gezgininde, sol gezinti bölmesinde **Varlıklar > Zaman Girişi**'ni seçin.
3. **Teklif satırı ayrıntısı** varlığını genişletin ve ardından **Alanlar**'ı seçin.
4. **Kaynak Çalışma Konumu** konumu adlı yeni bir alan oluşturmak ve alan türü olarak **Seçenek kümesi**'ni seçmek için **Yeni**'yi seçin. 
5. **Varolan bir seçenek kümesini kullan**'ı, **Kaynak Çalışma Konumu** seçenek kümesini seçin ve ardından **Kaydet**'i seçin.
6. Bu alanı **Fiili değer**, **Fatura satırı ayrıntısı** ve **Yevmiye defteri satırı** varlıklarına eklemek için 1-5 arasındaki adımları yineleyin.
7. **Kaynak Çalışma Saatleri** seçenek kümesi için 1-6 arasındaki adımları yineleyin. 

> ![Kaynak Çalışma Konumunu Zaman Girişine ekleme](media/RWL-time-entry.png)

Bu, seçenek kümesi tabanlı özel boyutlar için gerekli şema değişikliklerini tamamlar.

## <a name="entity-based-custom-pricing-dimensions"></a>Varlık tabanlı özel fiyatlandırma boyutları

Özel fiyatlandırma boyutu bir varlık olduğunda, boyut varlığı ile temel varlıklar arasına 1:N ilişkileri eklersiniz. Yukarıdaki Standart Başlık örneğini kullanarak, her çalışana standart bir başlık atanması beklenir. Sonuç olarak, Standart Başlıktan Ayrılabilir Kaynağa 1:N ilişkisine veya Ayrılabilir Kaynaktan Standart Başlığa oluşturulmuşsa N:1 ilişkisine gereksinim duyarsınız.

1. Proje Operations'da, **Ayarlar** > **Çözümler**'i seçin ve ardından **\<your organization name> fiyatlandırma boyutları** ayarını çift tıklayın. 
2. Çözüm Gezgininde, sol gezinti bölmesinde **Varlıklar > Standart Başlık**'ı seçin.
3. **Standart Başlık** varlığını genişletin ve **1:N İlişkileri**'ni seçin.
4. **Standart Başlıktan Ayrılabilir Kaynağa** adlı yeni bir 1:N ilişkisi oluşturmak için **Yeni**'yi seçin. Gerekli bilgileri girin ve ardından **Kaydet**'i seçin.

> ![Standart Başlığı Ayrılabilir Kaynağa başvuru alanı olarak ekleme](media/ST-BR.png)

Standart Başlığın **Rol Fiyatı** ve **Rol Fiyatı Kar Payı** Fiyatlandırma varlıklarına da eklenmesi gerekir. Bu da **Standart Başlık** ile **Rol Fiyatı** varlıkları arasında ve **Standart Başlık** ve **Rol Fiyatı Kar payı** varlıkları arasında 1:N ilişkileri kullanılarak tamamlanır.

1. Çözüm Gezgininde, sol gezinti bölmesinde **Varlıklar > Standart Başlık**'ı seçin.
2. **Standart Başlık** varlığını genişletin ve **1:N İlişkileri**'ni seçin.
3. **Standart Başlıktan Rol Fiyatına** adlı yeni bir 1:N ilişkisi oluşturmak için **Yeni**'yi seçin. Gerekli bilgileri girin ve ardından **Kaydet**'i seçin.
4. **Standart Başlık** ve **Rol Fiyatı Kar Payı** varlıkları arasında 1:N İlişkileri oluşturmak için 1-4 arasındaki adımları yineleyin.

Projenin satış ve tahmin aşamalarında, Teklife/Projeye fiyat vermek için, her standart başlık için çalışma çabası tahminleri gerekir. Bu, Standart Başlık'tan tahmin varlıklarının her birine 1:N ilişkileri ekleneceği anlamına gelir: 

- **Teklif satırı ayrıntısı**
- **Proje Sözleşme Satırı Ayrıntısı**
- **Proje Takımı Üyesi**
- **Tahmin Satırı**

5. **Standart Başlıktan** **Teklif Satırı Ayrıntısı**, **Proje sözleşme satırı ayrıntısı**, **Proje takımı üyesi** ve **Tahmin satırı**'na ' e 1:N İlişkileri oluşturmak için 1-5 arasındaki adımları yineleyin.

> ![Standart Başlığı Tahmin Satırına başvuru alanı olarak ekleme](media/ST-Estimate-Line.png)

  Teslimat ve Faturalama aşamalarında, her bir standart başlığın tamamladığı iş Proje Fiili Değerlerinde doğru fiyatlandırılmalıdır. Bu **Standart başlıktan** **Zaman Girişi**, **Fiili Değer**, **Fatura satır ayrıntısı** ve **Yevmiye defteri satırı** varlıklarına 1:N ilişkileri olması gerektiği anlamına gelir.

6. **Standart başlıktan** **Zaman Girişi**, **Fiili Değer**, **Fatura satır ayrıntısı** ve **Yevmiye defteri satırı** varlıklarına 1:N ilişkileri oluşturmak için 1-6 arası adımları yineleyin.

> ![Standart Başlığı Zaman Girişine başvuru alanı olarak ekleme](media/ST-Mapping.png)

### <a name="set-up-dimension-value-defaulting-using-the-mappings-features-of-the-platform"></a>Platformun eşleme özelliklerini kullanarak Boyut değeri varsayılanı ayarlama
Zaman Girişi için, sistemin varsayılan olarak zaman girişini kaydeden Ayrılabilir Kaynaktan alınan Zaman Girişinde standart başlığı kullanmak yararlı olacaktır. **Ayrılabilir Kaynaktan** **Zaman girişine** 1: N ilişkisinde alan eşlemeleri eklemek için aşağıdaki adımları kullanın.

1. Çözüm Gezgininde, sol gezinti bölmesinde **Varlıklar > Standart Başlık**'ı seçin.
2. **Standart Başlık** varlığını genişletin ve **1:N İlişkileri**'ni seçin.
3. **Ayrılabilir Kaynaktan Zaman Girişine** öğesine çift tıklayın. **İlişki** sayfasında, **Alan eşlemelerini kullan**'ı seçin. 
4. **Ayrılabilir Kaynak** varlığındaki **Standart Başlık** alanı ile **Zaman Girişi** varlığındaki **Standart Başlık** referans alanı arasında yeni bir alan eşlemesi oluşturmak için **Yeni**'yi seçin. 

> ![Standart Başlığın Ayrılabilir Kaynaktan Zaman Girişine varsayılan olarak değiştirilmesine izin vermek için alan eşlemeleri ayarlama](media/ST-Mapping2.png)

Bu, varlık tabanlı özel boyutlar için gerekli şema değişikliklerini tamamlar.

##  <a name="add-custom-fields-to-forms-views-and-business-rules"></a>Formlara, görünümlere ve iş kurallarına özel alanlar ekleme

Gerekli tüm şema değişikliklerini yaptıktan sonra, sonraki adım alanları formlara ve görünümlere ekleyerek alanları Kullanıcı arabiriminde görünür hale getirmektir.

1. Formu veya görünümü açın. Sağ gezinti bölmesinde, alanı seçin ve form tuvaline sürükleyin. 
2. Bir görünümü düzenliyorsanız, sağ gezinti bölmesini kullanın, **Alan Ekle**' yi seçin ve **Alan listesi** iletişim kutusunda, gereksinim duyduğunuz alanları seçip **Tamam**'ı seçin.

Aşağıdaki tabloda, yeni alanlarla güncelleştirilmesi gereken, varlığa göre listelenen kullanıma hazır form ve görünümlerin kapsamlı bir listesi verilmektedir. Bu varlıklardaki özelleştirmelerinizde ek görünümler veya formlar varsa yeni alanları da bunlara ekleyin.

| Entity        | Yeni alana gereksinim duyan formlar   |Yeni alana gereksinim duyan görünümler      |
| ------------------------------|---------------------------------|----------------------------------|
|  Rol Fiyatı|• Bilgi |• Etkin Kaynak Kategorisi Fiyatları<br> • Kaynak Kategorisi Fiyatı İlişkili Görünümü|
|  Rol Fiyatı Kar Payı|• Bilgi|• Etkin Rol Fiyatı Kar Payı<br>• Rol Fiyatı Kar Payı İlişkili Görünümü|
|  Teklif satırı ayrıntısı|• Proje Bilgileri<br>• Hızlı Proje Oluştur|• Etkin Teklif Satırı Ayrıntısı<br>• Birleşik Teklif Satırı Ayrıntıları<br>• Teklif Satırı Ayrıntısı ilişkili görünümü|
|  Proje Sözleşme satırı ayrıntısı|• Proje Bilgileri<br>• Hızlı Proje Oluştur|• Birleşik Sözleşme Satırı Ayrıntıları<br>• Etkin Sözleşme Satırı Ayrıntıları<br>• Sözleşme Satırı Ayrıntıları İlişkili Görünümü|
|  Proje Takımı Üyesi|• Bilgi<br>• Yeni Form|• Etkin Proje Takımı Üyeleri<br>• Proje Takımı Üyeleri<br>• Proje Takımı üyeleri ilişkili görünümü|
|  Zaman Girişi|• Bilgi<br>• Zaman Girişi Oluştur|• Tarihe Göre Zaman Girişlerim<br>• Bu hafta için Zaman Girişlerim<br>• Onaylanacak zaman girişleri|
|  Yevmiye Defteri Satırı|• Bilgi<br>• Hızlı oluşturma|• Etkin yevmiye defteri satırları<br>• Yevmiye Defteri Satırı ilişkili görünümü|
|  Fatura Satırı Ayrıntısı|• Bilgi<br>• Hızlı oluşturma|• Etkin Fatura Satırı Ayrıntıları<br>• Borçlandırılabilir Fatura İşlemleri<br>• Ücretsiz Fatura İşlemleri<br>• Fatura Satırı Ayrıntısı ilişkili görünümü<br>• Borçlandırılamaz Fatura İşlemleri|
|  Gerçek|• Bilgi<br>• Etkin Gerçek Tutarlar|• Gerçek Tutar İlişkili görünümü|

Tanımladığınız öğeye bağlı olarak özel alanların iş kurallarına da eklenmesi gerekebilir. Kullanıma hazır bir örnek **Duruma göre Zaman Girişi düzenlenebilirliği** iş kuralı içindir. Bu kural, Zaman Girişi **Onaylandı** gibi düzenlenemeyen bir durumda olduğunda hangi alanların kilitlenmesi gerektiğini tanımlar. Alanların Zaman Girişi **Taslak** ve **Geri çevrildi** durumu dışında bir durumda olduğunda alanların düzenlemeye karşı kilitlenmesi için bu iş kuralına alanlar ekleyin.


[!INCLUDE[footer-include](../includes/footer-banner.md)]