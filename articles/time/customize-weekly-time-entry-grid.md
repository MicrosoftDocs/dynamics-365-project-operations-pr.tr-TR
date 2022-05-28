---
title: Zaman girişlerini uzatma
description: Bu konuda, geliştiricilerin zaman girişi denetimini nasıl uzatacağı hakkında bilgiler sağlanmaktadır.
author: stsporen
ms.date: 01/27/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 6b91aecd76950d2bd37192d634c80ea98d08034e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583010"
---
# <a name="extending-time-entries"></a>Zaman girişlerini uzatma

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Dynamics 365 Project Operations, genişletilebilir bir zaman girişi özel denetimi içerir. Bu denetim aşağıdaki özellikleri içerir:

- Zamanı bir haftaya yatay olarak girme
- Gün, satır veya haftaya göre toplamlar
- Satırları veya haftaları kopyalama
- SS:dd veya SS.ss ile zaman girişi (otomatik olarak SS.ss biçimine dönüştürülür)
- Atamalar, ayırmalar veya randevulardan içeri aktarma

Zaman girişlerini uzatma işlemi iki alanda yapılabilir:
- [Kendi kullanımınız için özel zaman girişleri ekleme](#add)
- [Haftalık Zaman Girişi denetimini özelleştirme](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Kendi kullanımınız için özel zaman girişleri ekleyin

Zaman girişleri, birden çok senaryoda kullanılan temel bir varlıktır. 1 Nisan 2020'de TESA çekirdek çözümü tanıtıldı. TESA bir **Ayarlar** varlığı ve yeni bir **Zaman Girişi Kullanıcı** güvenlik rolü sağlar. **msdyn_duration** ile doğrudan ilişkili olan yeni **msdyn_start** ve **msdyn_end** alanları da eklenmiştir. Yeni varlık, güvenlik rolü ve alanlar, zamana birden çok ürün içinde daha birleşik bir yaklaşıma olanak tanır.


### <a name="time-source-entity"></a>Zaman Kaynak Varlığı
| Alan | Veri Akışı Açıklaması | 
|-------|------------|
| Veri Akışı Adı  | Zaman girişi oluşturma sırasında seçim değeri olarak kullanılan Zaman Kaynağı girişinin adı. |
| Varsayılan Zaman Kaynağı [Zaman Kaynağı: isdefault] | Varsayılan olarak, varsayılanda yalnızca bir Zaman Kaynağı işaretlenebilir. Bu, zaman kaynağı belirtilmediğinde girişlerin bir zaman kaynağını varsayılan olarak ayarlamasını sağlar. |
|Zaman Kaynağı Türü [Zaman Kaynağı: sourcetype] | Kaynak türü, zaman kaynağının bir uygulamayla ilişkilendirilmesine olanak veren bir seçenektir (Zaman Girişi Kaynak Türü). Microsoft'un 190.000.000'den büyük değerleri depolar.|


### <a name="time-entries-and-the-time-source-entity"></a>Zaman girişleri ve Zaman Kaynağı Varlığı
Her zaman girişi bir zaman kaynağı kaydıyla ilişkilendirilir. Bu kayıt, hangi uygulamaların zaman girişini işlemesi ve nasıl işlemesi gerektiğini belirler.

Zaman girişleri her zaman başlangıç, bitiş ve sürenin bağlantılı olduğu tek bir bitişik zaman bloğu halindedir.

Mantık aşağıdaki durumlarda zaman girişi kaydını otomatik olarak güncelleştirir:

- Aşağıdaki üç alandan ikisi sağlanmışsa üçüncüsü otomatik olarak hesaplanır: 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- **msdyn_start** ve **msdyn_end** alanları saat dilimine duyarlıdır.
- Yalnızca **msdyn_date** ve belirtilen **msdyn_duration** ile oluşturulan saat girişleri gece yarısı başlar. **msdyn_start** ve **msdyn_end** alanları uygun şekilde güncellenir.

#### <a name="time-entry-types"></a>Zaman girişi türleri

Zaman girişi kayıtlarının, ilişkili uygulamanın gönderme akışında davranışı tanımlayan ilişkilendirilmiş bir türü vardır.

|Etiket | Value|
|-----|-----|
|Molada   |192,355,000|
|Seyahat | 192,355,001|
|Fazla Mesai   | 192,354,320|
|İş   | 192,350,000|
|Devamsızlık    | Kategori 192,350,001|
|Tatil   | Kategori 192,350,002|


## <a name="customize-the-weekly-time-entry-control"></a><a name="customize"></a>Haftalık Zaman Girişi denetimini özelleştirme
Geliştiriciler başka varlıklara daha fazla alan ve arama ekleyebilir ve iş senaryolarını destekleyen özel iş kuralları uygulayabilir.

### <a name="add-custom-fields-with-lookups-to-other-entities"></a>Başka varlıklara aramaları olan özel alanlar ekleme
Haftalık zaman girişi ızgarasına özel bir alan eklemenin üç ana adımı vardır.

1. Özel alanı **Hızlı oluştur** iletişim kutusuna ekleyin.
2. Özel alanı göstermek üzere ızgarayı yapılandırın.
3. Özel alanı uygun şekilde **Satır düzenleme** veya **Zaman girişi düzenlemesi** sayfasına ekleyin.

Yeni alanın **Satır düzenleme** veya **Zaman girişi düzenlemesi** sayfasında gerekli doğrulamalara sahip olduğundan emin olun. Bu görevin bir parçası olarak, zaman girişinin durumuna göre alanı kilitleyin.

**Zaman girişi** ızgarasına özel bir alan ekleyip doğrudan ızgarada zaman girişleri oluşturduğunuzda, bu girişler için özel alan otomatik olarak satırla eşleşecek şekilde ayarlanır. 

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Özel alanı Hızlı oluştur iletişim kutusuna ekleme
Özel alanı **Hızlı oluştur: Zaman Girişi Oluştur** iletişim kutusuna ekleyin. Daha sonra kullanıcılar zaman girişleri eklediklerinde, **Yeni** seçeneğini belirleyerek bir değer girebilirler.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Özel alanı göstermek üzere ızgarayı yapılandırma
**Haftalık zaman girişi** ızgarasına özel alan eklemenin iki yolu vardır.

- **Haftalık Zaman Girişlerim** görünümünü özelleştirin ve buna özel alan ekleyin. Görünümdeki özellikleri düzenleyerek ızgaradaki özel alanın konumunu ve boyutunu belirtebilirsiniz.
- Yeni bir özel zaman girişi görünümü oluşturun ve bunu varsayılan görünüm olarak ayarlayın. Bu görünüm, ızgaranın içermesini istediğiniz sütunlara ek olarak **Açıklama** ve **Harici yorumlar** alanlarını içermelidir. Görünümdeki özellikleri düzenleyerek ızgaranın konumunu, boyutunu ve varsayılan sıralama düzenini belirleyebilirsiniz. Ardından bu görünümün özel denetimini **Zaman Girişi Izgarası** denetimi olacak şekilde yapılandırın. Denetimi görünüme ekleyin ve **Web**, **Telefon** ve **Tablet** için seçin. Ardından, **Haftalık zaman girişi** ızgarası için parametreleri yapılandırın. **Başlangıç tarihi** alanını **msdyn\_date** olarak ayarlayın, **Süre** alanını **msdyn\_duration** ve **Durum** alanını **msdyn\_entrystatus** olarak ayarlayın. **Salt Okunur Durum Listesi** alanı **192350002 (Onaylandı)**, **192350003 (Gönderildi)** veya **192350004 (Geri Çekme İstendi)** olarak ayarlanır.

### <a name="add-the-custom-field-to-the-appropriate-edit-page"></a>Özel alanı uygun düzenleme sayfasına ekleme
Zaman girişini veya zaman girişleri satırını düzenlemek için kullanılan sayfalar **Formlar** altında bulunabilir. Izgaradaki **Girişi düzenle** düğmesi, **Girişi düzenle** sayfasını ve **Satırı düzenle** düğmesi de **Satır düzenle** sayfasını açar. Bu sayfaları özel alanlar içerecek şekilde düzenleyebilirsiniz.

Her iki seçenek de **Proje** ve **Proje Görevi** varlıklarındaki bazı hazır filtrelemeleri kaldırır, böylece varlıklar için tüm arama görünümleri görünür olur. Yalnıza kullanıma hazır, ilgili arama görünümleri görünür.

Özel alan için uygun sayfayı belirlemelisiniz. Büyük olasılıkla, alanı ızgaraya eklediyseniz tüm zaman girdileri satırına uygulanan alanlar için kullanılan **Satır düzenleme** sayfasına gitmelidir. Özel alanın satırda her gün benzersiz bir değeri varsa (örneğin, bitiş zamanı için özel bir alansa) **Zaman girişi düzenlemesi** sayfasında görünmelidir.

Sayfaya özel alan eklemek için bir **Alan** öğesini sayfada uygun konuma sürükleyin ve ardından özelliklerini ayarlayın.

### <a name="add-new-option-set-values"></a>Yeni seçenek kümesi değerleri ekleme
Kullanıma hazır bir alana seçenek kümesi değerleri eklemek için aşağıdaki adımları izleyin.

1. Alanın düzenleme sayfasını açın ve **Tür** altında, seçenek kümesinin yanında **Düzenle**'yi seçin.
2. Özel bir etiket ve renk bulunan yeni bir seçenek ekleyin. Yeni bir zaman girişi durumu eklemek istiyorsanız kullanıma hazır alan **Giriş Durumu** olarak adlandırılır.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Yeni zaman girişi durumunu salt okunur olarak belirleme
Yeni zaman girişi durumunu salt okunur olarak belirlemek üzere yeni zaman girişi değerini **Salt Okunur Durum Listesi** özelliğine ekleyin. Etiketi değil, numarayı eklediğinizden emin olun. Zaman girişi ızgaranın düzenlenebilir kısmı artık yeni duruma sahip satırlar için kilitlenecektir. **Salt Okunur Durum Listesi** özelliğini farklı **Zaman Girişi** görünümleri için farklı şekilde ayarlamak isterseniz bir görünümün **Özel denetimler** bölümüne **Zaman girişi** ızgarasını ekleyin ve parametreleri uygun şekilde yapılandırın.

Ardından, **Satır düzenleme** ve **Zaman girişi düzenlemesi** sayfalarındaki tüm alanları kilitlemek için iş kuralları ekleyin. Bu sayfaların iş kurallarına erişmek için her sayfanın form düzenleyicisini açın ve ardından **İş kuralları**'nı seçin. Varolan iş kurallarındaki koşula yeni durumu ekleyebilir veya yeni durum için yeni bir iş kuralı ekleyebilirsiniz.

### <a name="add-custom-validation-rules"></a>Özel doğrulama kuralları ekleme
**Haftalık zaman girişi** ızgara deneyimi için iki tür doğrulama kuralı ekleyebilirsiniz:

- Sayfalarda çalışan istemci tarafı iş kuralları
- Tüm zaman giriş güncelleştirmeleri için geçerli olan sunucu tarafı eklenti doğrulamaları

#### <a name="client-side-business-rules"></a>İstemci tarafı iş kuralları
Alanları kilitlemek ve kilitlerini açmak, alanlara varsayılan değerler girmek ve yalnızca geçerli zaman girişi kaydında bilgi gerektiren doğrulamaları tanımlamak için iş kurallarını kullanın. Sayfanın iş kurallarına erişmek için form düzenleyicisini açın ve ardından **İş kuralları**'nı seçin. Ardından varolan iş kurallarını düzenleyebilir veya yeni bir iş kuralı ekleyebilirsiniz.

#### <a name="server-side-plug-in-validations"></a>Sunucu tarafı eklenti doğrulamaları
Tek seferlik giriş kaydında mevcut olandan daha fazla bağlam gerektiren doğrulamalar için eklenti doğrulamalarını kullanmalısınız. Bunları, ızgaradaki satır içi güncelleştirmelerde çalıştırmak istediğiniz doğrulamalar için de kullanmalısınız. Doğrulamaları tamamlamak için **Zaman Girişi** varlığında özel bir eklenti oluşturun.

### <a name="limits"></a>Sınırlar
Şu anda, **Zaman girişi** ızgarasının boyut sınırı 500 satırdır. 500'den fazla satır varsa, fazla satırlar gösterilmez. Bu boyut sınırını artırmanın bir yolu yoktur.

### <a name="copying-time-entries"></a>Zaman girişlerini kopyalama
Zaman girişi sırasında kopyalanması gereken alanların listesini tanımlamak için görünüm **Kopya Süresi Giriş Sütunlarını** kullanın. **Tarih** ve **Süre** gerekli alanlardır ve görünümden kaldırılmamalıdır.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
