---
title: Zaman girişlerini uzatma
description: Bu konuda, geliştiricilerin zaman girişi denetimini nasıl uzatacağı hakkında bilgiler sağlanmaktadır.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 93f411ad7c86beefcc35e7799a03987dacdcd62b
ms.sourcegitcommit: 5a29adce48133e09f051929e8544d6c2c93c025d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/02/2020
ms.locfileid: "3930904"
---
# <a name="extending-time-entries"></a>Zaman girişlerini uzatma

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Dynamics 365 Project Operations, uzatılabilir zaman girişi özel denetimi içerir. Bu denetim aşağıdaki özellikleri içerir:

- Zamanı bir haftaya yatay olarak girme
- Gün, satır veya haftaya göre toplamlar
- Satırları veya haftaları kopyalama
- SS:dd veya SS.ss ile zaman girişi (otomatik olarak SS.ss biçimine dönüştürülür)
- Atamalar, ayırmalar veya randevulardan içeri aktarma

Zaman girişlerini uzatma işlemi iki alanda yapılabilir:
- [Kendi kullanımınız için özel zaman girişleri ekleme](#add)
- [Haftalık Zaman Girişi denetimini özelleştirme](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Kendi kullanımınız için özel zaman girişleri ekleyin.

Zaman girişleri, birden çok senaryo için kullanılmak üzere tasarlanmış temel bir varlıktır. Nisan Dalga 1 2020'de, bir **Ayarlar** varlığı ve yeni bir **Zaman Girişi Kullanıcısı** güvenlik rolü sağlayan TESA temel çözümü eklenmiştir. **msdyn_duration** ile doğrudan ilişkili olan yeni **msdyn_start** ve **msdyn_end** alanları da eklenmiştir. Yeni varlık, güvenlik rolü ve alanlar, zamana birden çok ürün içinde daha birleşik bir yaklaşıma olanak tanır.


### <a name="time-source-entity"></a>Zaman Kaynak Varlığı
| Alan | Veri Akışı Açıklaması | 
|-------|------------|
| Veri Akışı Adı  | Zaman girişi oluşturma sırasında seçim değeri olarak kullanılan Zaman Kaynağı girişinin adı. |
| Varsayılan Zaman Kaynağı [Zaman Kaynağı: isdefault] | Varsayılan olarak, varsayılan zaman kaynağında yalnızca bir Zaman Kaynağı işaretlenebilir. Bu beceri, zaman kaynağı belirtilmediğinde girişlerin bir zaman kaynağını varsayılan olarak ayarlamasını sağlar. |
|Zaman Kaynağı Türü [Zaman Kaynağı: sourcetype] | Kaynak türü, zaman kaynağının bir uygulamayla ilişkilendirilmesine olanak veren bir seçenektir (Zaman Girişi Kaynak Türü). Ek uygulamalar eklendikçe, bu seçenek kümesine başka değerler de eklenecektir. Microsoft'un 190.000.000'den büyük değerleri depoladığını unutmayın.|


### <a name="time-entries-and-the-time-source-entity"></a>Zaman girişleri ve Zaman Kaynağı Varlığı
Her zaman girişi bir zaman kaynağı kaydıyla ilişkilendirilir. Bu kayıt, zaman girişini işleyecek uygulamaları belirler.

Zaman girişleri her zaman başlangıç, bitiş ve sürenin bağlantılı olduğu tek bir bitişik zaman bloğu halindedir.

Mantık aşağıdaki durumlarda zaman girişi kaydını otomatik olarak güncelleştirir:

- Aşağıdaki üç alandan ikisi sağlanmışsa üçüncüsü otomatik olarak hesaplanır 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- **msdyn_start** ve **msdyn_end** alanları saat dilimini algılar.
- Yalnızca **msdyn_date** ve **msdyn_duration** belirtilmiş olarak oluşturulan zaman girişleri gece yarısı başlar ve **msdyn_start** ve **msdyn_end** buna uygun şekilde güncelleştirilir.

#### <a name="time-entry-types"></a>Zaman girişi türleri

Zaman girişi kayıtlarının, ilişkili uygulamanın gönderme akışında davranışı tanımlayan ilişkilendirilmiş bir türü vardır.

|Etiket | Value|
|-----|-----|
|Molada   |192,355,000|
|Seyahat | 192,355,001|
|Fazla Mesai   | 192,354,320|
|İş   | 192,350,000|
|Devamsızlık    | 192,350,001|
|Tatil   | 192,350,002|



## <a name="customize-the-weekly-time-entry-control"></a><a name="customize"></a>Haftalık Zaman Girişi denetimini özelleştirme
Geliştiriciler başka varlıklara daha fazla alan ve arama ekleyebilir ve iş senaryolarını destekleyen özel iş kuralları uygulayabilir.

### <a name="add-custom-fields-with-lookups-to-other-entities"></a>Başka varlıklara aramaları olan özel alanlar ekleme
Haftalık zaman girişi ızgarasına özel bir alan eklemenin üç ana adımı vardır.

- Özel alanı hızlı oluşturma iletişim kutusuna ekleyin.
- Özel alanı göstermek üzere ızgarayı yapılandırın.
- Özel alanı, satır düzenleme görev akışına veya hücre düzenleme görev akışına ekleyin.

Ayrıca yeni alanın satır veya hücre düzenleme görev akışında gerekli doğrulamalara sahip olduğundan emin olmanız gerekir. Bu adımın parçası olarak, zaman girişi durumuna göre alanı kilitlemeniz gerekir.

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Özel alanı hızlı oluşturma iletişim kutusuna ekleme
Özel alanı **Zaman Girişi Oluştur Hızlı Oluşturma** iletişim kutusuna eklemeniz gerekir. Daha sonra kullanıcılar zaman girişleri eklediklerinde, **Yeni** seçeneğini belirleyerek bir değer girebilirler.

#### <a name="configure-the-grid-to-show-the-custom-field"></a>Özel alanı göstermek üzere ızgarayı yapılandırma
Haftalık zaman girişi ızgarasına özel bir alan eklemenin iki yolu vardır:

  - Görünümü özelleştirme ve özel alan ekleme
  - Yeni bir varsayılan özel zaman girişi oluşturma 


**Görünümü özelleştirme ve özel alan ekleme**

**Haftalık Zaman Girişlerim** görünümünü özelleştirebilir ve özel alanı buna ekleyebilirsiniz. Görünümde bu özellikleri düzenleyerek ızgaradaki özel alanın konumunu ve boyutunu seçebilirsiniz.

**Yeni bir varsayılan özel zaman girişi oluşturma** 

Bu görünüm, ızgarada bulunmasını istediğiniz sütunlara ek olarak **Açıklama** ve **Harici Yorumlar** alanlarını içermelidir. 

1. Görünümde bu özellikleri düzenleyerek ızgaranın konumunu, boyutunu ve varsayılan sıralama düzenini seçin. 
2. Bu görünümün özel denetimini **Zaman Girişi Izgarası** denetimi olacak şekilde yapılandırın. 
3. Bu denetimi görünüme ekleyin ve web, telefon ve tablet için seçin. 
4. Haftalık zaman girişi ızgarası için parametreleri yapılandırın. **Başlangıç Tarihi** alanını **msdyn_date** olarak, **Süre** alanını **msdyn_duration** olarak ve **Durum** alanını **msdyn_entrystatus** olarak ayarlayın. 
5. Varsayılan görünüm için, **Salt Okunur Durum Listesi** alanı **192350002,192350003,192350004** olarak, **Satır Düzenleme Görev Akışı** alanı **msdyn_timeentryrowedit** olarak ve **Hücre Düzenleme Görev Akışı** alanı **msdyn_timeentryedit** olarak ayarlanır. 
6. Bu alanları salt okunur durumları eklemek veya kaldırmak ya da satır veya hücreyi düzenlemek için farklı bir görev tabanlı deneyim (TBX) kullanmak üzere özelleştirebilirsiniz. Bu alanlar, bir statik değere bağlanmalıdır.


> [!NOTE] 
> Her iki seçenek de **Proje** ve **Proje Görevi** varlıklarındaki bazı kullanıma hazır filtreleri kaldırır, böylece varlıkların tüm arama görünümleri görülebilir. Yalnıza kullanıma hazır, ilgili arama görünümleri görünür.
Özel alan için uygun görev akışını belirlemeniz gerekir. Alanı ızgaraya eklediyseniz büyük olasılıkla, zaman girişleri satırının tamamı için geçerli olan alanlarda kullanılan satır düzenleme görev akışına gitmesi gerekir. Özel alan, **Bitiş saati** özel alanı gibi benzersiz bir günlük değere sahipse hücre düzenleme görev akışına gitmelidir.

Görev akışına özel alan eklemek için bir **Alan** öğesini sayfada uygun konuma sürükleyin ve ardından alan özelliklerini ayarlayın. **Kaynak** özelliğini **Zaman Girişi** olarak ve **Veri Alanı** özelliğini özel alan olarak ayarlayın. **Alan** özelliği, TBX sayfasında görünen adı belirtir. Alanda yaptığınız değişiklikleri kaydetmek için **Uygula**'yı ve ardından sayfada yaptığınız değişiklikleri kaydetmek için de **Güncelleştir**'i seçin.

Bunun yerine yeni bir özel TBX sayfası kullanmak için yeni bir işlem oluşturun. Kategoriyi **İş Süreci Akışı** olarak, varlığı **Zaman Girişi** olarak ve iş süreci akışı türünü **Süreci görev akışı olarak çalıştır** olarak ayarlayın. **Özellikler**altında, **Sayfa Adı** özelliği sayfanın görünen adı olarak ayarlanmalıdır. Tüm ilgili alanları TBX sayfasına ekleyin. İşlemi kaydedin ve etkinleştirin, ardından işlemde ilgili görev akışının özel denetim özelliğini **Ad** değerine güncelleştirin.

### <a name="add-new-option-set-values"></a>Yeni seçenek kümesi değerleri ekleme
Kullanıma hazır bir alana seçenek kümesi ayarları eklemek için alanın düzenleme sayfasını açın ve **Tür**altında, seçenek kümesinin yanındaki **Düzenle** öğesini seçin. Ardından, özel bir etiket ve renk bulunan yeni bir seçenek ekleyin. Yeni bir zaman girişi durumu eklemek isterseniz kullanıma hazır alan **Durum** değil **Giriş Durumu** olarak adlandırılır.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Yeni zaman girişi durumunu salt okunur olarak belirleme
Yeni zaman girişi durumunu salt okunur olarak belirlemek üzere yeni zaman girişi değerini **Salt Okunur Durum Listesi** özelliğine ekleyin. Zaman girişi ızgarasının düzenlenebilir kısmı yeni durumun bulunduğu satırlar için kilitlenir.
Ardından **Zaman Girişi Satır Düzenlemesi** ve **Zaman Girişi Düzenlemesi** TBX sayfalarındaki tüm alanları kilitlemek üzere iş kuralları ekleyin. Sayfanın iş süreci akışı düzenleyicisini açıp **İş Kuralları** öğesini seçerek bu sayfaların iş kurallarına erişebilirsiniz. Varolan iş kurallarındaki koşula yeni durumu ekleyebilir veya yeni durum için yeni bir iş kuralı ekleyebilirsiniz.

### <a name="add-custom-validation-rules"></a>Özel doğrulama kuralları ekleme
Haftalık zaman girişi ızgarası deneyimi için ekleyebileceğiniz iki tür doğrulama kuralı vardır:

- Hızlı oluşturma iletişim kutuları ve TBX sayfalarında çalışan istemci tarafı iş kuralları.
- Tüm zaman girişi güncelleştirmelerine uygulanan sunucu tarafı eklenti doğrulamaları.

#### <a name="business-rules"></a>İş Kuralları
Alanları kilitlemek ve kilitlerini açmak, alanlara varsayılan değerler girmek ve yalnızca geçerli zaman girişi kaydında bilgi gerektiren doğrulamaları tanımlamak için iş kurallarını kullanın. Sayfanın iş süreci akışı düzenleyicisini açıp **İş Kuralları** öğesini seçerek bir TBX sayfasının iş kurallarına erişebilirsiniz. Ardından varolan iş kurallarını düzenleyebilir veya yeni bir iş kuralı ekleyebilirsiniz. Daha da özelleştirilmiş doğrulamalar için JavaScript'i çalıştırmak üzere bir iş kuralı kullanabilirsiniz.

#### <a name="plug-in-validations"></a>Eklenti doğrulamaları
Tek bir zaman girişi kaydında kullanılabilir olandan daha fazla bağlam gerektiren doğrulamalar veya kılavuzdaki satır içi güncelleştirmeler üzerinde çalıştırmak istediğiniz doğrulamalar için eklenti doğrulamalarını kullanmanız gerekir. Doğrulamayı tamamlamak için **Zaman Girişi** varlığında özel bir eklenti oluşturun.
