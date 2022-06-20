---
title: Gider mobil uygulaması
description: Bu makale, Gider yönetimi mobil çalışma alanı hakkında bilgi sağlar.
author: suvaidya
ms.date: 11/15/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1ba7ccae04fbb02252e3ceb01f123ce1e85375b7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930250"
---
# <a name="mobile-expense-app"></a>Gider mobil uygulaması

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Bu makale, **Gider yönetimi** mobil çalışma alanı hakkında bilgi sağlar. Bu çalışma alanı, kullanıcıların bir gider raporuna daha sonra ekleyebilmeleri için bir makbuzun resmini çekerek yüklemesine olanak sağlar. Ayrıca, kullanıcılar iliştirilen bir makbuzu kullanarak da hızlı bir şekilde gider satırı oluşturabilir ve gider raporlarını oluşturabilir ve yönetebilir. Ayrıca, onaylayanlar **Gider yönetimi** mobil çalışma alanını kendilerine atanan gider raporlarını görüntülemek için kullanabilir ve bu gider raporlarını onaylayabilir veya reddedebilir.

Bu mobil çalışma alanı, Dynamics 365 Unified Ops mobil uygulaması birlikte kullanılmak üzere tasarlanmıştır.

Çoğu kuruluşta, çalışanın geri ödeme almak için teslim ettiği, seyahat veya iş ile ilgili gider raporuna makbuzun bir kopyasını iliştirmesi gerekir. **Gider yönetimi** mobil çalışma alanı, kullanıcıların seçtikleri mobil cihazda bir makbuza ait fotoğrafı ekleyerek hızla yeni gider satırları oluşturmalarına olanak sağlar. Alternatif olarak, kullanıcılar bir makbuzun fotoğrafını çekebilir ve sonra bunu daha sonra gider raporuna ekleyebilir. Ayrıca çalışanlar kendi gider raporlarını oluşturabilir ve yönetebilir ve ardından mobil aygıtlarını kullanarak onay ve geri ödeme için bunları teslim edebilir.

**Gider yönetimi** mobil çalışma alanı özellikle kullanıcıların şu görevleri gerçekleştirmesini sağlar:

- Makbuzun fotoğrafını çekin. Makbuz fotoğrafını karşıya yükleyin ve bir gider raporuna daha sonra iliştirin.
- Dosyayı resmi çekilen bir makbuz olarak karşıya yükleyin. Daha sonra bu dosyayı bir gider raporuna ekleyebilirsiniz.
- Eklenen bir makbuzu kullanarak yeni bir gider satırı oluşturun. Daha sonra satır maddesini bir gider raporuna ekleyebilir, onay ve geri ödeme için gönderebilirsiniz.

Şunları yapmak için de kullanabilirsiniz:

- Yeni bir gider raporu oluşturun.
- Kredi kartı hareketleri ile önceden oluşturulan diğer giderleri bir gider raporuna iliştirin.
- Gider raporu için yeni giderler oluşturun.
- Gider raporu için herhangi bir masrafa ait makbuzun fotoğrafını çekerek veya resmi çekilmiş bir makbuz dosyası şeklinde yükleyerek bir makbuz ekleyin.
- Şirketin gider ilkelerine bağlı olarak, bir gidere konuklar listesini ekleyin.
- Şirketin gider ilkesine bağlı olarak giderlerin dökümünü alın.
- Onay ve geri ödeme için bir gider raporunu gönderin.
- Atanmış bir onaylayan olduğunuz gider raporlarını onaylayın veya reddedin.

## <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Dynamics 365 Finance kullanımınızla ilgili ön koşullar

Finans kuruluşunuz için dağıtılmışsa, sistem yöneticisinin **Gider yönetimi** mobil çalışma alanını yayımlaması gerekir. 

## <a name="download-and-install-the-dynamics-365-unified-ops-mobile-app"></a>Dynamics 365 Unified Ops mobil uygulamasını karşıdan yükleme ve kurma
Dynamics 365 Unified Ops mobil uygulamasını karşıdan yükleyin ve kurun:

- [Android telefonlar için](https://go.microsoft.com/fwlink/?linkid=850662)
- [iPhone'lar için](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Mobil uygulamada oturum açma
1. Mobil cihazınızda uygulamayı açın.
2. Dynamics 365 URL'sini girin.
4. İlk kez oturum açtığınızda kullanıcı adınızı ve parolanızı girmeniz istenir. Kimlik bilgilerinizi girin.
5. Oturum açtıktan sonra, şirketiniz için kullanılabilir olan çalışma alanları gösterilir. Sistem yöneticisi daha sonra yeni bir çalışma alanı yayımladığında, mobil çalışma alanları listesini yenilemeniz gerekir.

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Gider yönetimi mobil çalışma alanını kullanarak bir makbuz resmi çekme

1. Mobil cihazınızda **Gider yönetimi** çalışma alanını açın.
2. **Makbuz yakala** öğesini seçin.
3. **Fotoğraf çek** veya **Görüntü Seç** öğesini belirleyin.
4. Aşağıdaki adımlardan birini uygulayın:

    - **Fotoğraf çek** öğesini seçtiyseniz, şu adımları izleyin:

        1. Mobil cihazınızdaki kameraya yönlendirilirsiniz, böylece makbuzun resmini çekebilirsiniz. 
        2. Fotoğraf çekmeyi bitirdiğinizde fotoğrafı kabul etmek için **Tamam**'ı seçin.
        3. İsteğe bağlı: Fotoğraf için bir ad ve notları girin.

    - **Görüntü seç** öğesini seçtiyseniz, şu adımları izleyin:

        1. Listeden bir görüntü seçin.
        2. İsteğe bağlı: Görüntü için bir ad ve notları girin.

5. **Bitti**'yi seçin.

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>Gider yönetimi mobil çalışma alanını kullanarak giderleri hızlıca girme

1. Mobil cihazınızda **Gider yönetimi** çalışma alanını açın.
2. **Hızlı gider girişi**'ni seçin.
3. Gider kategorisini seçin. Çevrimdışı kullanım için uygulamanıza yüklenen gider kategorileri listesi gösterilir. Varsayılan olarak, 50 öğe yüklenir, ancak geliştirici bu sayıyı değiştirebilir. Daha fazla bilgi için geliştiriciler [Mobil platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started) bölümüne başvurabilir. Kategoriniz listede yoksa, çevrimiçi arama yapmak için **Ara** seçeneğini belirleyin. Gider kategorisine göre arayın veya gider türüne göre arama yapmak için geçiş yapın.
4. Giderin hareket tarihini girin.
5. İsteğe bağlı: Giderin satıcı öğesini girin.
6. Giderin miktarını girin.
7. Giderin para birimini seçin. Çevrimdışı kullanım için uygulamanıza yüklenen para birimi kodları listesi gösterilir. Varsayılan olarak, 400 para birimi yüklüdür, ancak geliştirici bu sayıyı değiştirebilir. Daha fazla bilgi için geliştiriciler [Mobil platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started) bölümüne başvurabilir. Para biriminiz listede yoksa, çevrimiçi arama yapmak için **Ara** seçeneğini belirleyin. Para birimine göre arayın veya ada göre arama yapmak için geçiş yapın.
8. **Fotoğraf çek** veya **Görüntü Seç** öğesini belirleyin.
9. Aşağıdaki adımlardan birini uygulayın:

    - **Fotoğraf çek** öğesini seçtiğinizde mobil cihazınızdaki kameraya yönlendirilirsiniz, böylece makbuzun resmini çekebilirsiniz. Fotoğraf çekmeyi bitirdiğinizde fotoğrafı kabul etmek için **Tamam**'ı seçin.
    - **Görüntü Seç**'i seçtiyseniz , listeden bir görüntü seçin.

10. **Bitti**'yi seçin.

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace"></a>Gider yönetimi mobil çalışma alanını kullanarak gider raporunu onaylama

1. Mobil cihazınızda **Gider yönetimi** çalışma alanını açın.
2. **Gider onayları**, onaylamanız için size atanan gider raporu sayısını gösterir. Sayı her 30 dakikada bir güncelleştirilir. **Gider onayları** seçeneğini belirleyin.

    Onaylamanız için size atanan gider raporu listesi gösterilir.

3. Gider ayrıntılarını görüntülemek için bir gider raporu seçin.
4. Ayrıntılarını görüntülemek için bir gider seçin. Bir gider için gösterilen bilgiler, tüm makbuz, konuk ve döküm ayrıntılarını içerir.
5. **Gider raporu** sayfasına geri döndüğünüzde gider raporunu onaylamayı veya reddetmeyi seçin.
6. Onay eylemi için herhangi bir yorum girin.
7. **Bitti**'yi seçin.

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace"></a>Gider yönetimi mobil çalışma alanını kullanarak yeni bir gider raporu oluşturun ve onaylamaya gönderin

1. Mobil cihazınızda **Gider yönetimi** çalışma alanını açın.
2. **Gider girişi**'ni seçin.
3. **Yeni rapor**'u seçin veya listeden varolan bir gider raporu seçin.
4. Yeni gider raporları için, amacı ve elinizdeki tüm ek bilgileri girin. Bu bilgiler, gider yönetiminin şirketiniz için yapılandırılma şekline bağlı olarak değişir.
5. **Bitti**'yi seçin.
6. Kredi kartı hareketleri gibi var olan giderleri gider raporuna eklemek için **İliştir**'i seçin.
7. Listeden bir veya daha fazla gider seçin.
8. **Bitti**'yi seçin.
9. Gider raporuna yeni bir gider eklemek için **Yeni gider**'i seçin.
10. Gider kategorisini seçin. Çevrimdışı kullanım için uygulamanıza yüklenen gider kategorileri listesi gösterilir. Varsayılan olarak, 50 öğe yüklenir, ancak geliştirici bu sayıyı değiştirebilir. Daha fazla bilgi için geliştiriciler [Mobil platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started) bölümüne başvurabilir. Kategoriniz listede yoksa, çevrimiçi arama yapmak için **Ara** seçeneğini belirleyin. Gider kategorisine göre arayın veya gider türüne göre arama yapmak için geçiş yapın.
11. İsteğe bağlı: Giderin satıcı öğesini girin.
12. Giderin hareket tarihini girin.
13. Giderin miktarını girin.
14. Giderin para birimini seçin. Çevrimdışı kullanım için uygulamanıza yüklenen para birimi kodları listesi gösterilir. Varsayılan olarak, 400 para birimi yüklüdür, ancak geliştirici bu sayıyı değiştirebilir. Daha fazla bilgi için geliştiriciler [Mobil platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started) bölümüne başvurabilir. Para biriminiz listede yoksa, çevrimiçi arama yapmak için **Ara** seçeneğini belirleyin. Para birimine göre arayın veya ada göre arama yapmak için geçiş yapın.
15. **Bitti**'yi seçin.
16. Gidere daha fazla ayrıntı eklemek için, **Daha ayrıntıları ekle**'yi seçin. Kullanılabilir alanlar, şirketiniz için gider yönetiminin yapılandırmasına bağlıdır.
17. Şirket ilkesi gider için bir makbuz gerektiriyorsa, **Makbuzlar**'ı seçin ve şu adımları izleyin:

    1. **Makbuz yakala** veya **Makbuz iliştir**'i seçin.
    2. Aşağıdaki adımlardan birini uygulayın:

        - **Makbuz yakala** öğesini seçtiyseniz, şu adımları izleyin:

            1. **Fotoğraf çek** veya **Görüntü Seç** öğesini belirleyin.
            2. Aşağıdaki adımlardan birini uygulayın:

                - **Fotoğraf çek** öğesini seçtiyseniz, şu adımları izleyin:

                    1. Mobil cihazınızdaki kameraya yönlendirilirsiniz, böylece makbuzun resmini çekebilirsiniz. Fotoğraf çekmeyi bitirdiğinizde fotoğrafı kabul etmek için **Tamam**'ı seçin.
                    2. İsteğe bağlı: Fotoğraf için bir ad ve notları girin.

                - **Görüntü seç** öğesini seçtiyseniz, şu adımları izleyin:

                    1. Listeden bir görüntü seçin.
                    2. İsteğe bağlı: Görüntü için bir ad ve notları girin.

            3. **Bitti**'yi seçin.

        - **Makbuz iliştir** öğesini seçtiyseniz, şu adımları izleyin:

            1. Listeden bir veya daha fazla görüntü seçin.
            2. **Bitti**'yi seçin.

    3. Gider ayrıntılarına dönmek için **Geri** düğmesini seçin.

18. Şirket ilkesi gider için konukları gerektiriyorsa, **Konuklar**'ı seçin ve şu adımları izleyin:

    1. **Konuk**, **Önceki konuklar** veya **İş arkadaşları**'nı seçin.
    2. Aşağıdaki adımlardan birini uygulayın:

        - **Konuk** öğesini seçtiyseniz, şu adımları izleyin:

            1. Konuğun adını girin.
            2. İsteğe bağlı: Konuğun kuruluşunu ve/veya ülkesini girin.
            3. İsteğe bağlı: Konuğun unvanını girin.
            4. **Bitti**'yi seçin.

        - **Önceki konuklar** öğesini seçtiyseniz, şu adımları izleyin:

            1. Listeden bir veya daha fazla önceki konuk seçin. Çevrimdışı kullanım için uygulamanıza yüklenen önceki gider raporlarına eklediğiniz önceki konukların listesini görürsünüz. Varsayılan olarak, 50 öğe yüklenir, ancak geliştirici bu sayıyı değiştirebilir. Daha fazla bilgi için geliştiriciler [Mobil platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started) bölümüne başvurabilir. Önceki konuğunuz listede yoksa, çevrimiçi arama yapmak için **Ara** seçeneğini belirleyin. Ada göre arayın veya kuruluş, ülke veya unvana göre arama yapmak için geçiş yapın.
            2. **Bitti**'yi seçin.

        - **İş arkadaşları** öğesini seçtiyseniz, şu adımları izleyin:

            1. Listede bir veya daha fazla iş arkadaşı seçin. Çevrimdışı kullanım için uygulamanıza yüklenen iş arkadaşı listesi gösterilir. Varsayılan olarak, 50 öğe yüklenir, ancak geliştirici bu sayıyı değiştirebilir. Daha fazla bilgi için geliştiriciler [Mobil platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started) bölümüne başvurabilir. İş arkadaşlarınız listede yoksa, çevrimiçi arama yapmak için **Ara** seçeneğini belirleyin. Ada göre arayın veya şirket veya unvana göre arama yapmak için geçiş yapın.
            2. **Bitti**'yi seçin.

    3. Gider ayrıntılarına dönmek için **Geri** düğmesini seçin.

19. Şirket ilkesi giderlerin dökümünü gerektiriyorsa, **Döküm al**'ı seçin ve şu adımları izleyin:

    1. Döküm almaya başlayacağınız tarihi seçin.
    2. **Döküm ekle**'yi seçin.
    3. Gider dökümü için alt kategori seçin. Çevrimdışı kullanım için uygulamanıza yüklenen gider alt kategorilerinin listesi gösterilir. Varsayılan olarak, 50 öğe yüklenir, ancak geliştirici bu sayıyı değiştirebilir. Daha fazla bilgi için geliştiriciler [Mobil platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started) bölümüne başvurabilir. Alt kategoriniz listede yoksa, çevrimiçi arama yapmak için **Ara** seçeneğini belirleyin. Gider alt kategorisinin adına göre arayın.
    4. Döküm için hareket tutarını girin.
    5. Gerekirse hareket tarihini düzenleyin.
    6. **Bitti**'yi seçin.
    7. Seçili tarih için tüm dökümleri eklemeyi tamamlayana kadar önceki adımları tekrarlayın.
    8. Ek günler için, dökümleri sonraki güne kopyalamak için **Sonraki güne kopyala** seçeneğini belirleyebilirsiniz. Başka bir seçenek olarak, ilk tarih için yaptığınız gibi, döküm alınacak tarihi seçebilir, sonra döküm ekleyebilirsiniz.
    9. Gideri döküm ettikten sonra, gider ayrıntılarına dönmek için **Geri** düğmesini seçin.

20. **Gider raporu** sayfasına dönmek için **Geri** düğmesini seçin.
21. Tüm giderleri eklemeyi tamamlayana kadar yukarıdaki adımları tekrarlayın.
22. **Gönder**'i seçin.
23. Onaylayan için herhangi bir yorum girin.
24. **Bitti**'yi seçin.

## <a name="frequently-asked-questions"></a>Sık sorulan sorular

### <a name="why-doesnt-the-expense-mobile-app-enter-the-payment-method-by-default"></a>Gider mobil uygulaması neden varsayılan olarak ödeme yöntemini giremiyor?

Kuruluşlar, her bir gider kategorisi için **Varsayılan ödeme yöntemi** ayarını oluşturulduğu anda özelleştirebilir. Ayrıca, ödeme yöntemleri ayarladığınızda, **Varsayılan ödeme yöntemi** alanını **Yalnızca içeri aktarma** olarak ayarlayabilirsiniz.

**Yalnızca içeri aktarma** bir ödeme yöntemi için etkinleştirildiğinde, ödeme yöntemi varsayılan olarak girilmez. Bu ödeme yönteminin ayarlandığı gider kategorilerinde boş olacaktır. Bu davranış hem web deneyiminde, hem de mobil deneyimde tutarlıdır.
    
**Yalnızca içeri aktarma** bir ödeme yöntemi için etkinleştirilmemişse, bu ödeme yönteminin ayarlandığı gider kategorileri için ayarlanan değer varsayılan olarak girilir. Ancak, varsayılan değerin Gider mobil uygulamasında girilmediği bilinen bir sorun vardır. Bu sorunu çözmek için, gider raporunu kaydetmeden önce bir ödeme yöntemini el ile seçin. 

### <a name="why-cant-i-add-or-edit-financial-dimensions-in-the-expense-mobile-app"></a>Neden Gider mobil uygulamasında mali boyut ekleyemiyor veya düzenleyemiyorum?

Boyut ve dağıtım girişi desteklenmez. Bu sınırlamaya geçici bir çözüm olarak, proje veya çalışana göre varsayılan mali boyutlar ayarlayarak bu alanların mobil uygulamada varsayılan olarak ayarlanmış olmasını sağlayabilirsiniz.

### <a name="why-do-i-sometimes-see-a-synchronization-error-in-the-expense-mobile-app"></a>Neden bazen Gider mobil uygulamasında bir eşitleme hatası görüyorum?

Gider satırları ilke gereksinimlerini karşılamıyorsa ve kullanıcı ilke uyarısını dikkate almadan gider raporu gönderiyorsa mobil veriler sunucuyla eşitlenmez ve bir eşitleme hatası oluşur. Bir eşitleme hatası oluştuktan sonra gönderilen tüm gider raporları başarısız durumda kalır ve daha fazla eşitleme hatasına yol açar. Bu durumu çözmenin tek yolu eşitleme bildirimlerini el ile silmektir. Bu sorun, ilke uyarıları giderilmeden gider raporlarının gönderilmesini durdurarak ele alınır böylece eşitleme hataları önlenebilir.

### <a name="why-isnt-project-and-category-validation-correctly-reflected-in-the-expense-mobile-app"></a>Proje ve kategori doğrulaması neden Gider mobil uygulamasında doğru şekilde yansıtılmıyor?

Bu doğrulama şu anda desteklenmemektedir. Ancak destek gelecekte eklenebilir. 

### <a name="what-document-types-are-supported-in-the-expense-mobile-app"></a>Gider mobil uygulamasında hangi belge türleri desteklenir?

Gider mobil uygulaması yalnızca resimleri destekler. Şu anda PDF'leri veya diğer belgeleri desteklemez.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
