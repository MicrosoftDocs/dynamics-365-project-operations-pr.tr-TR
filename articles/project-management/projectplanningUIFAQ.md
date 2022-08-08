---
title: Görev ızgarasında çalışma sorunlarını giderme
description: Bu makalede, Görev kılavuzunda çalışırken bilinmesi gereken sorun giderme bilgileri yer alır.
author: ruhercul
ms.date: 07/22/2022
ms.topic: article
ms.product: ''
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 208ed55abf4cdf0ad2b035bd923e183ff3cae660
ms.sourcegitcommit: e91136d3335ee03db660529eccacd48907774453
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/22/2022
ms.locfileid: "9188256"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Görev ızgarasında çalışma sorunlarını giderme 


_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayan öğeleri temel alan senaryolar için Project Operations, Lite dağıtımı: anlaşmadan proforma faturaya, Project for the web_

Dynamics 365 Project Operations tarafından kullanılan Görev ızgarası Microsoft Dataverse içinde barındırılan bir iframe'dir. Bu kullanımın sonucu olarak, kimlik doğrulamanın ve yetkilendirmenin doğru şekilde çalışmasının sağlanması için belirli gereksinimler karşılanmalıdır. Bu makale, iş kırılım yapısında (İKY) kılavuzu işleme veya görevleri yönetme yeteneğini etkileyebilecek genel sorunları açıklar.

Genel sorunlar arasında şunlar bulunur:

- Görev ızgarasındaki **Görev** sekmesi boştur.
- Projeyi açtığınızda, proje yüklenmez ve kullanıcı arabirimi (UI) değiştiricide takılı kalır.
- **Project for the Web** için ayrıcalıkların yönetilmesi.
- Bir görev oluşturduğunuzda, güncelleştirdiğinizde veya sildiğinizde değişiklikler kaydedilmez.

## <a name="issue-the-task-tab-is-empty"></a>Sorun: Görev sekmesi boş

### <a name="mitigation-1-enable-cookies"></a>Çözüm 1: Tanımlama bilgilerini etkinleştirin

Project Operations, iş kırılım yapısının işlenmesi için üçüncü taraf tanımlama bilgilerinin etkinleştirilmesini gerektirir. Üçüncü taraf tanımlama bilgileri etkinleştirilmediğinde, **Proje** sayfasında **Görevler** sekmesini seçtiğinizde görevler yerine boş bir sayfa görürsünüz.

Microsoft Edge veya Google Chrome tarayıcıları için aşağıdaki yordamlarda, üçüncü taraf tanımlama bilgilerini etkinleştirmek üzere tarayıcı ayarınızı nasıl güncelleştirebileceğinizi açıklanmaktadır.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Edge tarayıcınızı açın.
2. Sağ üst köşede **üç nokta**'yı (...) ve ardından **Ayarlar**'ı seçin.
3. **Tanımlama bilgileri ve site izinleri** altında, **Tanımlama bilgileri ve site verileri**'ni seçin.
4. **Üçüncü taraf tanımlama bilgileri**'ni kapatın.
5. Tarayıcınızı yenileyin. 

#### <a name="google-chrome"></a>Google Chrome

1. Chrome tarayıcınızı açın.
2. Sağ üst köşede, üç dikey noktayı ve ardından **Ayarlar**'ı seçin.
3. **Gizlilik ve güvenlik** altında, **Çerezler ve diğer site verileri**'ni seçin.
4. **Tüm çerezlere izin ver**'i seçin.
5. Tarayıcınızı yenileyin. 

> [!NOTE]
> Üçüncü taraf tanımlama bilgilerini engellerseniz diğer sitelerden gelen tüm tanımlama bilgileri ve site verileri (siteye özel durumlar listenizde izin verilse bile) engellenir.

### <a name="mitigation-2-validate-the-pex-endpoint-has-been-correctly-configured"></a>Çözüm 2: PEX uç noktasının doğru şekilde yapılandırıldığını doğrulayın

Project Operations bir proje parametresinin PEX Uç Noktası'na başvurmasını gerektirir. Bu uç nokta, iş kırılım yapısını işlemek için kullanılan hizmetle iletişim kurmak için gereklidir. Parametre etkinleştirilmemişse "Proje parametresi geçerli değil" hatasını alırsınız. PEX uç noktasını güncelleştirmek için aşağıdaki adımları izleyin.

1. **PEX Uç Nokta** alanını **Proje Parametreleri** sayfasına ekleyin.
2. Kullandığınız ürün türünü tanımlayın. Bu değer PEX uç nokta ayarlandığında kullanılır. Alma işleminde, ürün türü PEX uç nokta zaten tanımlanmıştır. Bu değeri koru.
3. Alanı şu değerle güncelleştirin: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=<id>&type=2`. Aşağıdaki tabloda, ürün türüne göre kullanılması gereken tür parametresi verilmiştir.

      | **Ürün türü**                     | **Parametre yazın** |
      |--------------------------------------|--------------------|
      | Varsayılan kuruluşta Project for the Web   | type=0             |
      | CDS adlı kuruluşta Project for the Web | type=1             |
      | Project Operations                   | type=2             |

4. Alanı **Proje parametreleri** sayfasından kaldırın.

### <a name="mitigation-3-sign-in-to-projectmicrosoftcom"></a>Azaltma 3: project.microsoft.com adresinde oturum açın

Tarayıcınızda yeni bir sekme açın, project.microsoft.com adresine gidin ve Project Operations'a erişmek için kullandığınız kullanıcı rolünü kullanarak oturum açın. Bir Microsoft ürününde tarayıcıda yalnızca bir Kullanıcı oturum açması önemlidir. Aşağıdaki şekilde gösterildiği gibi, "login.microsoftonline.com bağlanmayı reddetti" hata iletisi çoğu zaman birden çok kullanıcı oturum açtığında oluşur.

![İki kullanıcının oturum açtığını gösteren bir firma oturum açma sayfası seçin.](media/MULTIPLE_USERS_LOGGED_IN.png)

## <a name="issue-the-project-doesnt-load-and-the-ui-is-stuck-on-the-spinner"></a>Sorun: Proje yüklenmedi ve Kullanıcı arabirimi değer değiştiricide takılı kaldı

Kimlik doğrulama amacıyla, Görev ızgarasının yüklenmesi için açılır pencereler etkinleştirilmelidir. Açılır pencereler etkinleştirilmemişse, ekran yükleme değiştiricisinde takılı kalır. Aşağıdaki grafikte, adres çubuğunda engellenen bir açılan liste etiketine sahip olan ve değiştiricinin sayfayı yüklemeye çalışırken takılmasına neden olan URL gösterilir. 

   ![Takılı değiştirici ve açılır pencere engeli.](media/popupsblocked.png)

### <a name="mitigation-1-enable-pop-ups"></a>Çözüm 1: Açılır pencereleri etkinleştirin

Projeniz değiştiricide takılı kaldıysa, açılır pencereler etkin olmayabilir.

#### <a name="microsoft-edge"></a>Microsoft Edge

Edge tarayıcınızda açılır pencereleri etkinleştirmek için iki yol vardır.

1. Edge tarayıcınızda, tarayıcının sağ üst köşesindeki bildirimi seçin.
2. Belirtilen Dataverse ortamından **Açılır pencerelere ve yeniden yönlendirmelere her zaman izin ver**'i seçin.
 
     ![Engellenen pencereyi açar.](media/enablepopups.png)

Alternatif olarak, aşağıdaki adımları uygulayabilirsiniz.

1. Edge tarayıcınızı açın.
2. Sağ üst köşede, **üç noktayı** (...) seçin ve sonra **Ayarlar** > **Site izinleri** > **Açılır pencereler ve yeniden yönlendirmeler**'i seçin.
3. Açılır pencereleri engellemek için **Açılır pencereler ve yeniden yönlendirmeler** ayarını kapalı olarak değiştirin veya cihazınızda açılır pencerelere izin vermek için Açık seçeneğine geçiş yapın.
4. Açılır pencereleri etkinleştirdikten sonra tarayıcınızı yenileyin. 

#### <a name="google-chrome"></a>Google Chrome
1. Chrome tarayıcınızı açın.
2. Açılır pencerelerin engellendiği bir sayfaya gidin.
3. Adres çubuğunda **Açılır pencere engellendi**'yi seçin.
4. Görmek istediğiniz açılır pencerenin bağlantısını seçin.
5. Açılır pencereleri etkinleştirdikten sonra tarayıcınızı yenileyin. 

> [!NOTE]
> Sitedeki açılır pencereleri her zaman görmek için **[site] adresinden açılır pencerelere ve yeniden yönlendirmelere her zaman izin ver**'i ve ardından **Bitti**'yi seçin.

## <a name="issue-3-administration-of-privileges-for-project-for-the-web"></a>Sorun 3: Project for the Web için ayrıcalıkların yönetilmesi

Project Operations harici bir zamanlama hizmetine dayanır. Hizmet, bir kullanıcıya İKY ile ilgili varlıkları okuma ve yazma izni veren birden fazla atanmış rol olmasını gerektirir. Bu varlıklar proje görevlerini, kaynak atamalarını ve görev bağımlılıklarını içerir. Bir kullanıcı, **Görevler** sekmesine gittiğinde İKY'yi işleyemiyorsa bunun nedeni **Project Operations** için **Projenin** etkinleştirilmemiş olması olabilir. Kullanıcı, bir güvenlik rolü hatası veya erişim reddiyle ilgili bir hata alabilir.

### <a name="mitigation-1-validate-the-application-user-and-end-user-security-roles"></a>Çözüm 1: Uygulama kullanıcısını ve son kullanıcı güvenlik rollerini doğrulayın

1. **Ayar** > **Güvenlik** > **Kullanıcılar** > **Uygulama Kullanıcıları**'na gidin.  

   ![Uygulama okuyucu.](media/applicationuser.jpg)
   
2. Doğrulanacak uygulama kullanıcısı kaydına çift tıklayın:

     - Kullanıcının projeye erişimi vardır. Bunu, kullanıcının **Proje Yöneticisi** güvenlik rolüne sahip olduğunu doğrulayarak yapabilirsiniz.
     - Microsoft Project uygulaması kullanıcısı var ve doğru yapılandırılmış.
 
3. Bu kullanıcı yoksa, yeni bir kullanıcı kaydı oluşturun. 
4. **Yeni Kullanıcılar**'ı seçin, giriş formunu **Uygulama Kullanıcısı** olarak değiştirin ve **Uygulama Kimliğini** ekleyin.

   ![Uygulama kullanıcısı ayrıntıları.](media/applicationuserdetails.jpg)


## <a name="issue-4-changes-arent-saved-when-you-create-update-or-delete-a-task"></a>Sorun 4: Bir görev oluşturduğunuzda, güncelleştirdiğinizde veya sildiğinizde değişiklikler kaydedilmiyor

İKY'de bir veya daha fazla güncelleştirme yaptığınızda, değişiklikler başarısız oluyor ve kaydedilmiyor. Zamanlama ızgarasında "Yaptığınız son değişiklik kaydedilemedi" iletisiyle bir hata oluşur.

### <a name="mitigation-1-validate-the-license-assignment"></a>Çözüm 1: Lisans atamasını doğrulayın

1. Kullanıcıya doğru lisansın atandığını ve lisansın hizmet planları ayrıntılarında hizmetin etkinleştirildiğini doğrulayın.  
2. Kullanıcının **project.microsoft.com** adresini açabildiğini doğrulayın.
    
### <a name="mitigation-2-validation-configuration-of-the-project-application-user"></a>Çözüm 2: Proje uygulaması kullanıcısının doğrulama yapılandırması
1. Proje uygulaması kullanıcısının oluşturulduğunu doğrulayın.
2. Aşağıdaki güvenlik rollerini kullanıcıya uygulayın:
  
  - Dataverse Kullanıcısı veya Temel Kullanıcı
  - Project Operations Sistemi
  - Proje Sistemi
  - Project Operations Çift Yazma Sistemi. Bu rol, Project Operations'ın kaynak/stoğu tutulmayan öğeleri temel alan dağıtımı için gereklidir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
