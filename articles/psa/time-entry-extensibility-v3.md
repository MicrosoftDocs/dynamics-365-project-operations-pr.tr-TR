---
title: Haftalık zaman girişini özelleştirme
description: Bu konu, bir kuruluşun uygulamalarını destekleyen özel iş kurallarının nasıl uygulanacağı hakkında bilgi sağlar.
author: stsporen
ms.custom:
- dyn365-projectservice
ms.date: 07/09/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 1cc32a1d8776f4adaa0031154aba6bd6733b7f7d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581078"
---
# <a name="customize-weekly-time-entry"></a>Haftalık zaman girişini özelleştirme 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Microsoft, Microsoft Dynamics 365 Project Service Automation sürüm 3.3'te proje kaynaklarının bir defada bir haftaya kadar hızlı şekilde zaman girmesine olanak tanıyan modern bir ızgara tanıttı. Yeni haftalık zaman girişi ızgarası, tarihe, satıra veya haftaya göre yapılan girişlerin toplamını gösterebilir. Kaynaklar, hafta içinde yapılan zaman girişlerinin kopyalarını oluşturabilir ve ayrıca önceki haftalardan toplu kopyalama gerçekleştirebilir. Sistem özelleştiriciler, alanlar ekleyerek, başka varlıklara aramalar ekleyerek ve kuruluşun uygulamalarını desteklemek için özel iş kuralları uygulayarak görünümü özelleştirebilir.

Zaman girişi ve yeni haftalık zaman ızgarasına site haritası aracılığıyla erişilir. Önceki PSA sürümlerinin parçası olan genişletilebilir olmayan özel zaman girişi deneyiminin yerini, genişletilebilir haftalık zaman girişi ızgarası ile salt okunur ızgara ve takvimdeki alternatif deneyim alır. Bu değişiklikle kullanıcılar haftalık miktarlarda zaman girebilirler.

## <a name="page-layout"></a>Sayfa düzeni
Yeni haftalık zaman girişi ızgarası, bir araç çubuğu ve **Boyutlar** ve **Süre** olmak üzere iki ana bölümden oluşan özel bir denetimdir. Araç çubuğunda, zaman girişi ızgarasının yalnızca bu özel denetimi için geçerli olan bir düğme bulunur. Buna karşılık sayfanın üst kısmındaki Eylem Bölmesinde bulunan düğmeler, zaman girişi için desteklenen üç denetim türü için geçerlidir: haftalık zaman girişi denetimi, salt okunur denetim ve takvim denetimi.

### <a name="dimensions"></a>Boyutlar
**Boyutlar** bölümünde, sütun başlıkları olarak zamanın girilebileceği tüm boyutlar gösterilir. Aşağıdaki boyutlar kullanıma hazır şekilde desteklenir:

- Proje
- Proje Görevi
- Rol
- Tür
- Giriş Durumu

**Boyutlar** bölümü satır içi düzenlemeye izin vermez. Bu bölüm, özel alanların haftalık zamana girişi kılavuzuna eklenmesine olanak sağlayan bir görünümle desteklenir. Özel alanlar ekleme hakkında bilgi için, bu konunun ilerleyen bölümlerindeki "Genişletilebilirlik" bölümüne bakın.

### <a name="duration"></a>Süre
Süre bölümü, haftanın günlerini sütun başlıkları olarak gösterir. Bu bölüm satır içi düzenlemeye izin verir. Uygun boyutlara sahip bir zaman girişi satırı oluşturulduktan sonra kullanıcılar, bu boyutlarda harcadıkları süreyi satır içine hızlı bir şekilde girebilir.

## <a name="create-a-new-time-entry"></a>Yeni zaman girişi oluşturma
Zaman girişi ızgarasında yeni bir zaman girişi oluşturmak için **Yeni** öğesini seçin. **Zaman Girişi Hızlı Oluşturma** iletişim kutusu görüntülenir. Bu iletişim kutusunda, kullanıcılar zaman girişi tarihini seçebilir ve ardından **Proje**, **Proje Görevi**, **Rol** ve **Süre** boyutları için dakika, saat veya gün cinsinden sayı ile birlikte **h**, **m** veya **d** yazarak veri girebilirler. Kullanıcılar zaman girişi için harici olarak paylaşılabilecek bir açıklama ve yorum da girebilir. Kullanıcılar yaptıkları değişiklikleri kaydettiklerinde boyutlara göre girdikleri değerler **Boyutlar** bölümünde görüntülenir. **Süre** alanına girdikleri süre bilgileri, zaman girişinin oluşturulduğu tarihte görüntülenir.

Arama alanları, sistem görünümleriyle desteklenir. Örneğin, kullanıcı bir proje girdikten sonra **Proje Görevi** alanı varsayılan olarak **Kopyalama** görünümüne ayarlanır. Kullanıcıya atanmamış görevler için zaman girişleri oluşturmak üzere arama iletişim kutusunda **Görünümü Değiştir** öğesini ve ardından **Tüm Etkin Proje Görevleri** görünümünü seçin.

## <a name="edit-a-time-entry"></a>Zaman girişini düzenleme
Zaman girişi sayfasında **Açıklama** ve **Harici Yorumlar** gibi bazı alanların ayrıntıları haftalık zaman girişi ızgarasında gösterilmez. Bunun yerine, süre hücrelerinde bu ek ayrıntıların olduğu küçük bir üçgen gösterge görüntülenir. Hücreyi seçin ve ardından **Hızlı Düzenleme** panelindeki verileri görüntülemek için **Ayrıntıları Düzenle** öğesini seçin. Haftalık zaman girişi ızgarasının parçası olmayan belirli bir zaman girişinin ayrıntılarını düzenlemek veya güncelleştirmek için kullanıcıların **Hızlı Düzenleme** bölmesini açması gerekir.

## <a name="copy-a-time-entry-row"></a>Zaman girişi satırını kopyalama
İlk zaman girişi satırı oluşturulduktan sonra kullanıcılar, tüm satırı yeni bir satıra kopyalamak **Satırı kopyala** öğesini seçebilirler. Satır bu şekilde kopyalandığında boyutlar ve süreler de kopyalanır. Kullanıcılar **Süre** bölümünde boyut değerlerini ve süreleri satır içi güncelleştirmek için **Satırı düzenle** öğesini de seçebilirler.

## <a name="open-a-time-entry"></a>Zaman girişi açma
Haftalık zaman girişi ızgarası, en belirgin alanlarda en iyi ve hızlı girişi desteklemek için seçilen boyutların ve sürelerin bir alt kümesini gösterir. Tek bir zaman girişinin tüm ayrıntıları görüntülemek için **Girişi Düzenle** altındaki **Aç** öğesini seçin.

## <a name="submit-a-time-entry"></a>Zaman girişi gönderme
Kullanıcılar bir hücre bloğunu veya bir zaman girişi satırının tamamını ve ardından **Gönder** öğesini seçerek tek bir zaman girişi veya bir zaman girişi grubu gönderebilirler. Gönderilen zaman girişleri, onaylayanların **Onay** sayfasında onay bekleyen girişler olarak görüntülenir. Zaman girişleri başarıyla gönderildikten sonra düzenlenemezler.

## <a name="recall-a-time-entry"></a>Zaman girişini geri çekme
Gönderdiğiniz zaman girişlerini geri çekebilirsiniz. Tek bir zaman girişini, bir zaman girişi bloğunu veya bir zaman girişi satırının tamamını geri çekebilirsiniz. Geri çekilen zaman girişleri, kaynakları düzenlemek için kullanılabilir.

## <a name="time-entry-status"></a>Zaman girişi durumu
Yeni zaman girişleri otomatik olarak **Taslak** durumu atanır. Zaman girişi gönderildiğinde durum **Gönderildi** olarak güncelleştirilir. Gönderilen bir zaman girişi onaylandığında durum **Onaylandı** olarak güncelleştirilir. Zaman girişi reddedilirse durum **Geri Çevrildi** olarak güncelleştirilir ve giriş düzeltme ve yeniden gönderim için kullanılabilir hale gelir. Yalnızca **Taslak** durumundaki zaman girişleri silinebilir.

## <a name="view-rejection-comments"></a>Reddetme yorumlarını görüntüleme
Zaman girişi onaylayan tarafından reddedildiğinde onaylayan, kaynağın reddetme nedenini anlamasına yardımcı olmak için reddetme yorumları ekleyebilir. Zaman girişinin reddetme yorumlarını görüntülemek için **Girişi aç** öğesini seçin. Reddetme yorumları zaman çizelgesinde gösterilir. Zaman çizelgesinde, kaynak girişi yeniden göndermeden önce reddetme yorumlarına yanıt verebilir.

## <a name="copy-week"></a>Haftayı kopyala
Birkaç zaman girişi oluşturulduktan sonra kullanıcılar ek zaman girişlerini toplu olarak oluşturmak için **Haftayı kopyala** öğesini seçebilirler. **Kopyala** iletişim kutusu görüntülenir. **Başlangıç Dönemi** bölümünde, zaman girişlerinin kopyalanacağı tarih aralığını tanımamak için **Başlangıç Tarihi** ve **Bitiş Tarihi** alanlarını kullanın. **Bitiş Dönemi** bölümünde, **Başlangıç Tarihi** alanında, zaman girişlerinin oluşturulduğu tarih aralığını belirtin. Ardından **Kopyala** öğesini seçin. "Bitiş" döneminde belirtilen tarih için, "başlangıç" döneminde haftanın karşılık gelen günündeki zaman girişlerinin bir kopyası oluşturulur. Örneğin, son haftanın Pazartesi gününün zaman girişi "bitiş" döneminde belirtilen haftanın Pazartesi gününe kopyalanır.

## <a name="import"></a>İçeri aktarma
Aynı temel işlem ayırmalar, atamalar ve alışverişlerden içeri aktarmak için kullanılır. Kullanıcılar, ayırmaların içeri aktarıldığı tarih aralığını belirleyebilirler. Ardından taslak zaman girişlerine kopyalanması gereken ayırmaları açıkça seçmeleri gerekir. Önceki sürümde, önerilen zaman girişleri ızgara ve takvimde görüntüleniyordu ve oturum yenilendiğinde kaybediliyordu.

## <a name="extensibility"></a>Genişletilebilirlik
### <a name="add-custom-fields-that-have-lookups-to-other-entities"></a>Başka varlıklara aramalara sahip özel alanlar ekleme
Haftalık zaman girişi ızgarasına özel bir alan eklemenin üç ana adımı vardır.

1.  Özel alanı hızlı oluşturma iletişim kutusuna ekleyin.
2.  Özel alanı göstermek üzere ızgarayı yapılandırın.
3.  Özel alanı, gerektikçe satır düzenleme görev akışına veya hücre düzenleme görev akışına ekleyin.

Ayrıca yeni alanın satır veya hücre düzenleme görev akışında gerekli doğrulamalara sahip olduğundan emin olmanız gerekir. Bu adımın parçası olarak, zaman girişi durumuna göre alanı kilitlemeniz gerekir.

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Özel alanı hızlı oluşturma iletişim kutusuna ekleme
Özel alanı Zaman Girişi Oluştur Hızlı Oluşturma iletişim kutusuna eklemeniz gerekir. böylece kullanıcılar **Yeni** düğmesini kullanarak zaman girişleri eklediklerinde bunun için bir değer girebilirler.

#### <a name="configure-the-grid-to-show-the-custom-field"></a>Özel alanı göstermek üzere ızgarayı yapılandırma
Haftalık zaman girişi ızgarasına özel bir alan eklemenin iki yolu vardır. İlk seçenek, **Haftalık Zaman Girişlerim** görünümünü özelleştirmek ve özel alanı buna eklemektir. Görünümde bu özellikleri düzenleyerek ızgaradaki özel alanın konumunu ve boyutunu seçebilirsiniz.

İkinci seçenek, yeni bir özel zaman girişi görünümü oluşturmak ve bunu varsayılan görünüm olarak ayarlamaktır. Bu görünüm, ızgarada bulunmasını istediğiniz sütunlara ek olarak **Açıklama** ve **Harici Yorumlar** alanlarını içermelidir. Görünümde bu özellikleri düzenleyerek ızgaranın konumunu, boyutunu ve varsayılan sıralama düzenini seçebilirsiniz. Ardından bu görünümün özel denetimini **Zaman Girişi Izgarası** denetimi olacak şekilde yapılandırın. Bu denetimi görünüme ekleyin ve web, telefon ve tablet için seçin. Ardından haftalık zaman girişi ızgarası için parametreleri yapılandırın. **Başlangıç Tarihi** alanını **msdyn_date** olarak, **Süre** alanını **msdyn_duration** olarak ve **Durum** alanını **msdyn_entrystatus** olarak ayarlayın. Varsayılan görünüm için, **Salt Okunur Durum Listesi** alanı **192350002,192350003,192350004** olarak, **Satır Düzenleme Görev Akışı** alanı **msdyn_timeentryrowedit** olarak ve **Hücre Düzenleme Görev Akışı** alanı **msdyn_timeentryedit** olarak ayarlanır. Bu alanları salt okunur durumları eklemek veya kaldırmak ya da satır veya hücreyi düzenlemek için farklı bir görev tabanlı deneyim (TBX) kullanmak üzere özelleştirebilirsiniz. Bu alanlar, bir statik değere bağlanmalıdır.

#### <a name="add-the-custom-field-to-the-appropriate-edit-task-flow"></a>Özel alanı uygun düzenleme görev akışına ekleme
Düzenleme için kullanılan TBX sayfaları **İşlemler** altında bulunabilir. Varsayılan sayfalar **Project Service - Zaman Girişi Satır Düzenlemesi** ve **Project Service - Zaman Girişi Düzenlemesi**'dir.. Bu varsayılan sayfaları düzenleyebilir ya da yeni özel TBX sayfaları oluşturabilirsiniz.

> [!NOTE] 
> Her iki seçenek de **Proje** ve **Proje Görevi** varlıklarındaki bazı kullanıma hazır filtreleri kaldırır, böylece varlıkların tüm arama görünümleri görülebilir. Yalnıza kullanıma hazır, ilgili arama görünümleri görünür.

Özel alan için uygun görev akışını belirlemeniz gerekir. Alanı ızgaraya eklediyseniz büyük olasılıkla, zaman girişleri satırının tamamı için geçerli olan alanlarda kullanılan satır düzenleme görev akışına gitmesi gerekir. Özel alan, **Bitiş saati** özel alanı gibi benzersiz bir günlük değere sahipse hücre düzenleme görev akışına gitmelidir.

Görev akışına özel alan eklemek için bir **Alan** öğesini sayfada uygun konuma sürükleyin ve ardından özelliklerini ayarlayın. **Kaynak** özelliğini **Zaman Girişi** olarak ve **Veri Alanı** özelliğini özel alan olarak ayarlayın. **Alan** özelliği, TBX sayfasında görünen adı belirtir. Yaptığınız değişiklikleri alana kaydetmek için **Uygula** öğesini seçin. Ardından yaptığınız değişiklikleri sayfaya kaydetmek için **Güncelleştir** öğesini seçin.

Bunun yerine yeni bir özel TBX sayfası kullanmak için yeni bir işlem oluşturun. Kategoriyi **İş Süreci Akışı** olarak, varlığı **Zaman Girişi** olarak ve iş süreci akışı türünü **Süreci görev akışı olarak çalıştır** olarak ayarlayın. **Özellikler** altında, **Sayfa Adı** özelliği sayfanın görünen adı olarak ayarlanmalıdır. Tüm ilgili alanları TBX sayfasına ekleyin. İşlemi kaydedin ve etkinleştirin, ardından işlemde ilgili görev akışının özel denetim özelliğini **Ad** değerine güncelleştirin.

### <a name="add-new-option-set-values"></a>Yeni seçenek kümesi değerleri ekleme
Kullanıma hazır bir alana seçenek kümesi ayarları eklemek için alanın düzenleme sayfasını açın ve **Tür** altında, seçenek kümesinin yanındaki **Düzenle** öğesini seçin. Ardından, özel bir etiket ve renk bulunan yeni bir seçenek ekleyin. Yeni bir zaman girişi durumu eklemek isterseniz kullanıma hazır alan **Durum** değil **Giriş Durumu** olarak adlandırılır.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Yeni zaman girişi durumunu salt okunur olarak belirleme
Yeni zaman girişi durumunu salt okunur olarak belirlemek üzere yeni zaman girişi değerini (etiket değil, sayı) **Salt Okunur Durum Listesi** özelliğine ekleyin. Zaman girişi ızgarasının düzenlenebilir kısmı yeni durumun bulunduğu satırlar için kilitlenir.
Ardından **Zaman Girişi Satır Düzenlemesi** ve **Zaman Girişi Düzenlemesi** TBX sayfalarındaki tüm alanları kilitlemek üzere iş kuralları ekleyin. Sayfanın iş süreci akışı düzenleyicisini açıp **İş Kuralları** öğesini seçerek bu sayfaların iş kurallarına erişebilirsiniz. Varolan iş kurallarındaki koşula yeni durumu ekleyebilir veya yeni durum için yeni bir iş kuralı ekleyebilirsiniz.

### <a name="add-custom-validation-rules"></a>Özel doğrulama kuralları ekleme
Haftalık zaman girişi ızgara deneyimi için ekleyebileceğiniz iki tür doğrulama kuralı vardır: •   Hızlı oluşturma iletişim kutuları ve TBX sayfalarında çalışan istemci tarafı iş kuralları •   tüm zaman girişi güncelleştirmeleri için geçerli olan sunucu tarafı eklenti doğrulamaları

#### <a name="business-rules"></a>İş kuralları
Alanları kilitlemek ve kilitlerini açmak, alanlara varsayılan değerler girmek ve yalnızca geçerli zaman girişi kaydında bilgi gerektiren doğrulamaları tanımlamak için iş kurallarını kullanın. Sayfanın iş süreci akışı düzenleyicisini açıp **İş Kuralları** öğesini seçerek bir TBX sayfasının iş kurallarına erişebilirsiniz. Ardından varolan iş kurallarını düzenleyebilir veya yeni bir iş kuralı ekleyebilirsiniz. Daha da özelleştirilmiş doğrulamalar için JavaScript'i çalıştırmak üzere bir iş kuralı kullanabilirsiniz.

#### <a name="plug-in-validations"></a>Eklenti doğrulamaları
Tek bir zaman girişi kaydında kullanılabilir olandan daha fazla bağlam gerektiren doğrulamalar veya kılavuzdaki satır içi güncelleştirmeler üzerinde çalıştırmak istediğiniz doğrulamalar için eklenti doğrulamalarını kullanmanız gerekir. Doğrulamayı tamamlamak için **Zaman Girişi** varlığında özel bir eklenti oluşturun.

> [!IMPORTANT] 
> Şu anda TBX sayfalarındaki bilinen bir sorun kullanıcıların bilgileri düzeltmesini ve bir güncelleştirme eklenti doğrulamasında başarısız olduğunda Bitti öğesini yeniden seçmelerini engellemektedir. Geçici çözüm olarak, bu durumu mümkün olduğunca fazla önlemek için iş kuralı doğrulamaları ayarlayın.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
