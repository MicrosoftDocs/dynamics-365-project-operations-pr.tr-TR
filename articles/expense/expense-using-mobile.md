---
title: Gider mobil uygulaması
description: Bu konuda, Gider yönetimi mobil çalışma alanı hakkında bilgi sağlanır.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2f274a5f0dfcfdbe8c6771fff7a636c6e93eeea9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001990"
---
# <a name="mobile-expense-app"></a>Gider mobil uygulaması

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Bu konuda, **Gider yönetimi** mobil çalışma alanı hakkında bilgi sağlanır. Bu çalışma alanı, kullanıcıların bir gider raporuna daha sonra ekleyebilmeleri için bir makbuzun resmini çekerek yüklemesine olanak sağlar. Ayrıca, kullanıcılar iliştirilen bir makbuzu kullanarak da hızlı bir şekilde gider satırı oluşturabilir ve gider raporlarını oluşturabilir ve yönetebilir. Ayrıca, onaylayanlar **Gider yönetimi** mobil çalışma alanını kendilerine atanan gider raporlarını görüntülemek için kullanabilir ve bu gider raporlarını onaylayabilir veya reddedebilir.

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

## <a name="prerequisites"></a>Ön koşullar
Kuruluşunuz için dağıtılan sürüme bağlı olarak ön koşullar farklılık gösterir.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Dynamics 365 Finance kullananlar için ön koşullar 
Finans kuruluşunuz için dağıtılmışsa, sistem yöneticisinin **Gider yönetimi** mobil çalışma alanını yayımlaması gerekir. 

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Platform güncelleştirmesi 3 veya daha sonrasını içeren 1611 sürümünü kullananlar için ön koşullar
Kuruluşunuz için platform güncelleştirmesi 3 veya daha sonraki bir sürümü bulunan 1611 sürümü dağıtılmışsa, sistem yöneticisi aşağıdaki ön koşulları tamamlamalıdır. 

<table>
<thead>
<tr class="header">
<th>Önkoşul</th>
<th>Rol</th>
<th>Veri Akışı Açıklaması</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>KB 4019015 uygulayın.</td>
<td>Sistem yöneticisi</td>
<td>KB 4019015, <strong>Gider yönetimi</strong> mobil çalışma alanını içeren bir X + + güncelleştirmesi veya meta veri düzeltmesidir. KB 4019015 uygulamak için, sistem yöneticinizin aşağıdaki adımları izlemesi gerekir.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Lifecycle Services hizmetlerinden güncelleştirmeleri indirin.</a></li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Meta veri düzeltmesini yükleyin</a>.</li>
<li><strong>ApplicationSuite</strong> ve <strong>ExpenseMobile</strong> modellerini içeren <a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">dağıtılabilir bir paket oluşturun</a> ve ardından dağıtılabilir paketi LCS'ye yükleyin.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Dağıtılabilir paketi uygulayın</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td><strong>Gider yönetimi</strong> mobil çalışma alanını yayımlayın.</td>
<td>Sistem yöneticisi</td>
<td>Bkz. <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Mobil çalışma alanı yayınlama</a>.</td>
</tr>
</tbody>
</table>

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

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Gider yönetimi mobile çalışma alanını kullanarak bir gider raporunu onaylama (Temmuz 2017 güncelleştirmesini kullanıyorsanız)

1. Mobil cihazınızda **Gider yönetimi** çalışma alanını açın.
2. **Gider onayları**, onaylamanız için size atanan gider raporu sayısını gösterir. Sayı her 30 dakikada bir güncelleştirilir. **Gider onayları** seçeneğini belirleyin.

    Onaylamanız için size atanan gider raporu listesi gösterilir.
    
3. Gider ayrıntılarını görüntülemek için bir gider raporu seçin.
4. Ayrıntılarını görüntülemek için bir gider seçin. Bir gider için gösterilen bilgiler, tüm makbuz, konuk ve döküm ayrıntılarını içerir.
5. **Gider raporu** sayfasına geri döndüğünüzde gider raporunu onaylamayı veya reddetmeyi seçin.
6. Onay eylemi için herhangi bir yorum girin.
7. **Bitti**'yi seçin.

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Gider yönetimi mobile çalışma alanını kullanarak yeni bir gider raporu oluşturma ve onaya gönderme (Temmuz 2017 güncelleştirmesini kullanıyorsanız)

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

            3.  **Bitti**'yi seçin.

        - **Makbuz iliştir** öğesini seçtiyseniz, şu adımları izleyin:

            1.  Listeden bir veya daha fazla görüntü seçin.
            2.  **Bitti**'yi seçin.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]