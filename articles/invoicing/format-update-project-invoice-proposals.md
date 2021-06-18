---
title: Proje faturası tekliflerini yönetme
description: Bu konuda, kaynağı/stoku tutulmayanları temel alan senaryolar için Project Operations ile müşteriye yönelik faturaların işlenmesi hakkında ayrıntılar sağlanmaktadır.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7e6d060c1cca08f86e2d04ca96c9315a17316d11
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001495"
---
# <a name="manage-project-invoice-proposals"></a>Proje faturası tekliflerini yönetme

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Aşağıdaki iki koşul karşılandığında proje faturası teklifleri, faturalama departmanınız tarafından işlenebilir:

  - Proje yöneticisi Microsoft Dataverse'teki proforma faturayı onaylar.
  - Proforma faturaya dahil edilen faturalanmayan tüm süre ve malzeme satış işlemleri, Dynamics 365 **Project Operations Entegrasyon** günlüğü kullanılarak deftere kaydedilir.

Dynamics 365 Finance'te proje faturası teklifini tamamlamak için aşağıdaki adımları kullanın.

1. Süre ve malzeme işlemleri için ödeme bilgilerini inceleyin ve **Project Operations Entegrasyon** günlüğünü deftere kaydedin.
2. Sabit fiyatlı faturalama kilometre taşları için ödeme bilgilerini inceleyin.
3. Proje faturası teklifini inceleyin ve biçimlendirin.
4. Proje faturalarını deftere kaydedin ve yazdırın.

## <a name="manage-billing-information-in-the-project-operations-integration-journal"></a>Project Operations Entegrasyon günlüğündeki ödeme bilgilerini yönetme

Dataverse'te oluşturulan proje gerçek değerleri Proje muhasebecisi tarafından Finance'te incelenir ve deftere kaydedilir. Entegrasyon günlüğüyle çalışma hakkında daha fazla bilgi için bkz. [Project Operations'ta Entegrasyon günlüğü](../project-accounting/project-operations-integration-journal.md).

Maliyet gerçek değerleri ve faturalanmamış satış gerçek değerleri, Entegrasyon günlüğüne ayrı satırlar olarak eklenir:

  - Gerçek maliyetteki birim maliyet fiyatı ve maliyet tutarı varsayılan olarak Dataverse'teki proje gerçek maliyet işleminden farklıdır.
  - Faturalanmamış satış işleminde birim satış fiyatı ve satış tutarı, varsayılan olarak Dataverse'teki faturalanmamış proje gerçek satış işleminden farklıdır.

### <a name="billing-sales-tax"></a>Faturalama satış vergisi

Faturalama için satış vergisi hesaplaması, **Project Operations Entegrasyon** günlüğü satırındaki bir faturalanmamış satış kaydındaki **Faturalama satış vergisi grubu** ve **Faturalama öğesi satış vergisi grubu** alan birleşimiyle belirlenir. Sistem, bu alan değerlerini **Proje yönetimi ve muhasebe parametreleri** sayfasındaki **Mali Bilgiler** sekmesindeki ayarlara göre varsayılan olarak ayarlar.

- **Satış vergisi grubu yöntemi**, faturalama satış vergisi grubunun varsayılan mantığını belirler:
  
  - **Proje**: Faturalama satış vergisi grubunu her zaman varsayılan olarak projeden alır. **Tüm Projeler** sayfasında **Varsayılan hesaplamayı göster**'i seçerek bir projedeki varsayılan faturalama satış vergisi grubunu inceleyebilir veya değiştirebilirsiniz.
  - **Proje sözleşmesi**: Faturalama satış vergisi grubunu her zaman varsayılan olarak proje sözleşmesinden alır. **Proje sözleşmeleri** sayfasında **Varsayılan hesaplamayı göster**'i seçerek bir proje sözleşmesindeki varsayılan faturalama satış vergisi grubunu inceleyebilir veya değiştirebilirsiniz.
  - **Müşteri**: Faturalama satış vergisi grubunu her zaman varsayılan olarak müşteriden alır.
  - **Arama**: Yukarıdaki tüm varlıklarda arama yapar ve kullanılabilir ilk değeri seçer. Arama **Proje** varlığı ile başlar, ardından **Proje sözleşmesi** varlığı ile devam eder ve son olarak **Müşteri** varlığı ile yapılır.

- **Öğe satış vergisi grubu yöntemi**, faturalama öğesi satış vergisi grubunun varsayılan mantığını belirler:
  
  - Süre, gider ve ücret işlem türleri için faturalama öğesi satış vergisi grubunu her zaman varsayılan olarak **Proje kategorisi** varlığından alır.
  - Malzeme işlem türleri için faturalama öğesi satış vergisi grubunu varsayılan olarak **Proje yönetimi ve muhasebe parametreleri**'ndeki **Öğe satış vergisi grubu yöntemi**'nden alır. Öğe numarası, öğe satış vergisi grubunu varsayılan olarak **Serbest bırakılan ürün** varlığından alır. Kategori, öğe satış vergisi grubunu varsayılan olarak **Proje kategorisi** varlığından alır.

### <a name="financial-dimensions"></a>Mali boyutlar

**Project Operations Entegrasyonu** günlüğündeki faturalanmamış satış kayıtları için mali boyutlar varsayılan olarak **Proje** varlığından alınır. Mali boyutlar, **Tutarları Dağıt** seçilerek incelenebilir ve ayarlanabilir. Entegrasyon günlüğü gönderildikten sonra ancak Proforma fatura onaylanmadan önce faturalanmamış satış kayıtlarının mali boyutlarını değiştirmeniz gerekirse **Tüm Projeler** > **Yönet** > **Deftere nakledilmiş hareketler**'e gidin, işlemi seçin ve ardından **İşlem** > **Muhasebeyi ayarla**'yı seçin.

### <a name="exchange-rates"></a>Döviz kurları

Dataverse'teki faturalanmamış işlem para birimi, Finance'te işlem para birimi olarak kullanılır ve Finance'te tanımlanmış döviz kurlarını kullanılarak şirketin muhasebe para birimine dönüştürülür.


## <a name="manage-the-financial-attributes-of-billing-milestones"></a>Faturalama kilometre taşlarına ait mali öznitelikleri yönetme 

Sabit fiyatlı fatura yöntemini kullanan proje sözleşmesi satırları, [Sabit fiyatlı kilometre taşları](../sales/invoice-schedules-contract-line.md#create-a-fixed-price-invoice-schedule-for-a-contract-line) aracılığıyla faturalanır. Proje muhasebecisi, **Proje yönetimi ve muhasebe** > **Tüm projeler** > **Yönet** > **Hesap işlemleri**'ne giderek Finance'teki faturalama kilometre taşlarını inceleyebilir.

### <a name="billing-sales-tax"></a>Faturalama satış vergisi

Dataverse'te yeni bir faturalama kilometre taşı oluşturulduğunda, **Satış vergisi grubu** ve **Öğe satış vergisi grubu** değerleri varsayılan olarak ayarlardan alınır. Sistem, bu alanlar için değerleri varsayılan olarak **Proje yönetimi ve muhasebe parametreleri** sayfasındaki **Mali Bilgiler** sekmesindeki ayarlara göre belirler.

- **Satış vergisi grubu yöntemi**, **Faturalama satış vergisi grubu**'nun varsayılan mantığını belirler:

    - **Proje**: Faturalama satış vergisi grubunu her zaman varsayılan olarak projeden alır. **Tüm Projeler** sayfasında **Varsayılan hesaplamayı göster**'i seçerek bir projedeki varsayılan satış vergisi grubunu inceleyebilir veya değiştirebilirsiniz.
    - **Proje sözleşmesi**: Faturalama satış vergisi grubunu her zaman varsayılan olarak proje sözleşmesinden alır. **Proje sözleşmeleri** sayfasında **Varsayılan hesaplamayı göster**'i seçerek bir proje sözleşmesindeki varsayılan satış vergisi grubunu inceleyebilir veya değiştirebilirsiniz.
    - **Müşteri**: Faturalama satış vergisi grubunu her zaman varsayılan olarak müşteriden alır.
    - **Arama**: Bu listedeki tüm varlıklarda arama yapar ve kullanılabilir ilk değeri seçer. Arama **Proje** varlığı ile başlar, ardından **Proje sözleşmesi** varlığı ile devam eder ve ardından **Müşteri** varlığı ile yapılır.

- **Sabit fiyatlı kilometre taşı öğesi satış vergisi grubu**, Fatura kilometre taşı için **madde satış vergisi grubu** alanında varsayılan değer olarak kullanılır. Muhasebeci, **hesaba mahsup işlemler** sayfasında bu değeri gözden geçirebilir ve değiştirebilirler. Sistem, Proje Fatura teklif satırı oluştururken bu değeri mahsup hareketten kullanır.
 

### <a name="financial-dimensions"></a>Mali boyutlar

Sabit fiyatlı faturalama kilometre taşlarının varsayılan mali boyutları, Proje sözleşmesi satırlarında ayarlanır. **Proje sözleşmeleri** > **Varsayılan hesaplamayı göster**'e gidin ve **Sözleşme satırları** sekmesinde, **fiyat sözleşmesi satırı**'nı seçin, ardından varsayılan olarak kullanmak istediğiniz mali boyut değerlerini belirleyin.

Proje muhasebecisi, proje faturası teklifi oluşturuluncaya kadar fatura kilometre taşlarındaki satış vergisi ve mali boyut bilgilerini düzenleyebilir.


## <a name="create-project-invoice-proposals"></a>Proje faturası teklifleri oluşturma

**Proje faturaları** > **Proje faturası teklifleri**'ne giderek **Proje yönetimi ve muhasebe** modülünde proje faturası teklifleri incelenebilir.

Proforma fatura Dataverse'te onaylandığında Proje faturası teklif başlığı, Finance'te oluşturulur. Daha kolay mutabakat sağlamak için sistem Finance'teki Proje faturası teklifi numarasını, Dataverse'teki Proforma fatura kimliği ile aynı sayıya ayarlar. Proforma faturaların oluşturuldukları sırayla onaylanmaları gerekmediğinden, Finance'teki Proje faturası teklif numarası sırasında daha düşük ve daha yüksek sayılara yapılacak değişikliklere izin verilmelidir. Aşağıdaki adımları kullanarak numara sıralarını yapılandırın:

1. Finance'te **Kuruluş Yönetimi** > **Numara serileri** > **numara serileri**'ne gidin.
2. **Alan** filtresinde, **Projeler**'i seçin.
3. **Başvuru** filtresinde, **Fatura teklifi**'ni seçin.
4. Project Operations Dataverse entegrasyonu etkinleştirilmiş her tüzel kişiliği filtrelemek için **Şirket** alanını kullanın.
5. **Numara Serisi ayrıntıları**'nı açın ve **Genel** sekmesinde aşağıdakileri ayarlayın:

    - **Kullanıcı değişikliklerine izin ver: Daha küçük bir sayıya** = **Evet**
    - **Kullanıcı değişikliklerine izin ver: Daha büyük bir sayıya** = **Evet**

Proje faturası teklif satırları sistem tarafından dönemsel işlem **Hazırlama tablosundan alma** (**Proje yönetimi ve muhasebe** > **Dönemsel** > **Project Operations entegrasyonu** > **Hazırlama tablosundan alma**) kullanılarak eklenir. Bu işlem el ile veya bir periyodik zamanlama kullanarak yapılabilir. Tüm satırlar faturalanmaya hazır oluncaya kadar sistem fatura teklif belgesine satır eklemez. Süre ve malzeme işlemleri yalnızca **Project Operations Entegrasyon** günlüğü kullanılarak deftere kaydedildiğinde faturalanmaya hazır olur.

## <a name="format-and-print-invoice-proposals"></a>Fatura tekliflerini biçimlendirme ve yazdırma

Proje muhasebecisi, **Fatura teklifini biçimlendirme** sayfasını ve yazdırma yönetimi özelliklerini kullanarak bir proje faturası çıktısını özelleştirebilir.

### <a name="format-invoice-proposals"></a>Fatura tekliflerini biçimlendirme

**Fatura tekliflerini biçimlendirme** sayfası, özel gruplandırma işlemlerinin müşteri projesi faturasında görüntülenmesine izin verir.

1. **Proje faturası teklifi** sayfasında, **Yazdır** > **Fatura teklifini biçimlendir**'i seçin.
2. Proje faturası çıktısı için yeni bir gruplama oluşturmak üzere **Yeni**'yi seçin.
3. **Ayrıntı/Özet** alanında, bu gruplama için seçenekleri belirleyin:

    - Müşteri faturasının işlem ayrıntılarını yazdırmak için **Ayrıntı**'yı seçin.
    - Müşteri faturasının işlem özetini yazdırmak için **Özet**'i seçin.

> [!NOTE]
> **Fatura teklifini biçimlendirme** sayfasındaki **Ayrıntı/Özet** alanındaki seçim, **Fatura teklifleri** sayfasındaki **Fatura biçimi** alanında ayrıntılı bir fatura veya özet bir fatura yazdırmak için belirlenen seçeneği geçersiz kılar.

- **Kullanılabilir işlemler** sekmesinde bu bölüme eklenecek işlem satırlarını seçin ve bunları **Seçili işlemler** sekmesine taşımak için **İşlemleri dahil et**'i seçin.
- Bölümlerin sırasını değiştirmek için **Yukarı taşı** ve **Aşağı taşı**'yı seçin.
- Biçimlendirilmiş faturayı önizlemek için **Baskı önizleme**'yi seçin.

### <a name="print-management"></a>Yazdırma yönetimi

Yazdırma yönetimi, fatura için yazdırmak, hedefleri belirtmek ve alt bilgi metnini özelleştirmek için farklı rapor dosyaları kullanır. Yazdırma yönetimi modül düzeyinde ayarlanabilir ancak bu ayarlar belirli bir müşteri, sözleşme veya fatura teklifi için geçersiz kılınabilir. Bu işleve **Proje faturası teklifi** sayfasında erişmek için **Yazdır** > **Yazdırma yönetimi**'ni seçin.

Yazdırma yönetimi ayarı bir ağaç görünümü olarak görüntülenir. Burada her düğüm düzeyi, ayarlanacak kullanılabilir belgeleri görüntüler. Özel çıktıları modül, müşteri, sözleşme veya fatura teklifi belge düzeyinde atayabilirsiniz. Özgün belge çıktısında değişiklik yapmak için istediğiniz düğümü genişletin ve **Özgün öğe**'yi seçin. **Rapor biçimi** alanında, yazdırmak için kullanılacak rapor biçimini seçin. [İş Belgesi Yönetimi Çerçevesi](/dynamics365/fin-ops-core/dev-itpro/analytics/er-business-document-management)'ni kullanarak özel rapor biçimleri kullanabilirsiniz.

## <a name="post-invoice-proposals"></a>Fatura tekliflerini deftere nakletme

Fatura incelenip düzenlendikten ve fatura teklifi satırları tatmin edici hale geldikten sonra, fatura toplamlarını ve satış vergisini kontrol edin. **Ayrıntılar** grubunda, **Toplamlar**'ı seçin ve ardından faturayı göndermek için **Deftere Naklet**'i seçin.

Faturayı deftere nakletmeden önce görüntülemek için **Deftere Nakletme** onay kutusunu temizleyin. **Proforma**, örnek bir fatura olduğunu belirtmek için faturaya yazdırılır. Faturayı yazdırmak için **Faturayı yazdır** onay kutusunu işaretleyin.

**Fatura teklifi** sayfasına ek olarak, fatura teklifleri ayrıca **Fatura tekliflerini deftere naklet** dönemsel işi çalıştırılarak da deftere nakledilebilir. Bu işi bulmak için **Proje yönetimi ve muhasebe** > **Dönemsel** > **Proje faturaları** > **Fatura tekliflerini deftere naklet**'e gidin.

Bu sayfada deftere nakledilmeye hazır olan tüm fatura teklifleri gösterilir. **Toplu İş**'i seçerek Fatura tekliflerini deftere nakletmeyi zamanlayabilirsiniz. **Toplu işleme parametresi**'ni **Evet** olarak ayarlayın ve **Yineleme**'yi seçerek toplu işlemenin yinelemesini ayarlayın.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
