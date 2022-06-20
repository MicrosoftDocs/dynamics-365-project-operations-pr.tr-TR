---
title: Örnek verileri yükleme
description: Bu makale, Project Service Automation'da örnek veri kurma hakkında bilgiler sağlar.
ms.custom: dyn365-projectservice
ms.date: 11/08/2018
ms.reviewer: johnmichalak
ms.suite: ''
applies_to: Dynamics 365 Project Service Automation
author: ruhercul
ms.author: ruhercul
search.audienceType: IT Pro, Developer
search.app: ''
ms.openlocfilehash: 8fb3854c139125abbf499622d048e2ff0791516a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926800"
---
# <a name="sample-data-installation-for-the-project-service-application"></a>Project Service uygulaması için örnek veri kurulumu

[!include [banner](../includes/psa-now-project-operations.md)]

Microsoft, kendi tanıtım ortamlarınızı oluşturmanıza yardımcı olmak için uygulamalarınızın özelliklerini gösteren indirilebilir örnek veri paketleri sağlar. Örnek veri paketi için iki tür vardır:
- başvuru/verileri Kurulumu
- demo veri (iş emirleri ve projeler gibi referans/kurulum ve işlem verisi)

Örnek **referans** veri paketleri üç farklı pakette indirilebilir, böylece veriyi yalnızca Project Service çin yükleyebilir veya yalnızca Field Service için yükleyebilirsiniz, veya örnek veriyi her iki uygulama için de aynı anda yükleyebilirsiniz.

Örnek kurulum/referans veri paketleri şunlardır:

- [**V902PSMasterData** - sadece Project Service sürüm 3.x](https://go.microsoft.com/fwlink/?linkid=2026540&clcid=0x409)

- [**V902FSMasterData** - sadece Field Service sürüm 8.x](https://go.microsoft.com/fwlink/?linkid=2026536&clcid=0x409)

- [**V902FPSMasterData** - Field Service 8.x ve Project Service 3.x](https://go.microsoft.com/fwlink/?linkid=2026041&clcid=0x409)

En güncel **demo** veri paketi şudur:

 - [**FPSDemoData** - Field Service 8.x ve Project Service 3.x](https://aka.ms/fpsdemodatapackage)

   Kurulum talimatları kullanıcılar arasında bir miktar farklılık gösterir ve geri kalanını önceki [**blog gönderisinde**](https://aka.ms/fpsdemodatablog) belirtildiği gibi oluşturabilir ve yapılandırabilirsiniz. Bu paket, daha az gösteri veri kümesi sunar ve yüklemek için yaklaşık 3 saat sürer.

Bu örnek veri paketleri yalnızca İngilizce dilinde kullanılabilir.

> [!IMPORTANT]
> **Örnek verileri kaldırmanın bir yolu yoktur.** Bu paketleri yalnızca gösterim, değerlendirme, eğitim veya test sistemlerinde yüklemeniz gerekir. Ayrıca tek başına bir paket kurmanın ve daha sonra başka bir tek başına paket kurmanın desteklenmediğini unutmayın. (Diğer bir deyişle, **FSMasterData** ardından **PSMasterData** yüklemesi veya tam tersi bir yükleme yapamazsınız.) Gelecekte herhangi bir noktada her iki uygulama için örnek veri ihtiyacınız olacağını düşünüyorsanız **v902FPSMasterData** paketini yüklemelisiniz.

Örnek veri paketlerinden birini yüklediğinizde yükleme işlemi aşağıdaki eylemleri gerçekleştirir:

- Project Service, Field Service veya (varsa) her iki uygulamayı kullanmak için varsayılan parametreler oluşturur ya da ayarlar.

- Önemli özellikleri göstermek üzere, ayrılabilir kaynaklar, uygulamaya özgü roller, satış ve maliyet fiyat listeleri, kuruluş birimleri, satış süreci kayıtları ve diğer varlıklar gibi uygulamalar için örnek verileri içeri aktarır.  

Çalışma **demo verileri** paket iş emirleri ve projeler gibi yukarıdaki ve ek işlem verileri alın.

Örnek verilerle hangi özellikleri gösterebileceğinizi mi merak ediyorsunuz? [Teknik notlar](#technical-notes) altında, aşağıdaki Fabrikam Robotics kurgusal senaryosuna bakın.

Bu örnek veri paketlerini yükleme hakkında sorularınız varsa bize [fpsdemodata@microsoft.com adresinden bir e-posta gönderin](mailto:fpsdemodata@microsoft.com).

## <a name="requirements"></a>Gereksinimler

Yükleme protokolünde hedef kurulumunuz (kuruluş) hakkında aşağıdakiler varsayılmaktadır:

- Temel dil İngilizcedir ve temel para birimi ABD dolarıdır (ABD doları,$)

- Kuruluşta mevcut Project Service veya Field Service verileri yoktur ya da kuruluş sadece herhangi bir yeni kuruluşla gelen iskelet varsayılan verilere sahiptir.

- İş uygulamasının doğru sürümü zaten yüklüdür:
       
    - **FPSDemoData veya v902FPSMasterData için:** Kuruluşta Field Service sürüm 8.x ve Project Service sürüm 3.x yüklüdür.

    - **v902PSMasterData için:** Kuruluşta Project Service sürüm 3.x yüklüdür.

    - **v902FSMasterData için:** Kuruluşta Field Service sürüm 8.x yüklüdür.

> [!NOTE]
> Örnek verileri zaten bu verilerin bulunduğu mevcut bir Project Service ve Field Service deneme sürümüne veya demo ortamına yüklemeniz gerekirse (önerilmez), yükleyici tarafından gerçekleştirilen güvenlik ön denetimlerini askıya almanız gerekir. Daha fazla bilgi için aşağıdaki teknik notlara bakın.

## <a name="prepare-for-installation"></a>Yükleme için hazırlama

Yükleyiciyi Windows'un güncel bir sürümüne (tercihen Windows 10) sahip bir bilgisayarda çalıştırmanız gerekir.

Bilgisayar için bir ağa bağlı kalmayı ve yükleme için **kurulum/referans verisi** için **1 saate** kadar çalıştırılmasını planlamalısınız. (Normal kurulum yaklaşık 30 dakika sürer **FPSMasterData**, her iki uygulaması için örnek verileri içerir.) İçin **FPSDemoData**, geçici bir çözüm yükleme sürecek **3 saat**.

Bilgisayarda ekran koruyucu işlevinin kapatılmış olması gerekir. Aksi durumda, ekran koruyucu devreye girdiğinde (siz oturumunuzu bu süreçte etkin tutmadıkça) yükleme için oturum kimlik bilgileri kaybolabilir.

> [!div class="mx-imgBorder"]
> ![Ekran koruyucu kapalı durumdayken ekran koruyucu ayarlarının ekran görüntüsü.](media/sample-data-1.png)

## <a name="download-and-unpack"></a>İndirme ve paketi açma

Project Service ve Field Service örnek veri yükleyicisi, kendiliğinden açılan bir yürütülebilir dosya olarak dağıtılır. Dosya adları, örnek veri paketine bağlı olarak değişiklik gösterebilir. Ancak aksi durumda adımlar, yüklediğiniz paket ne olursa olsun aynıdır.

Paket indirildikten sonra .exe dosyasını çalıştırın ve daha sonra, sıkıştırılmış zip dosyasını açmak için hüküm ve koşulları kabul edin. Daha sonra bu dosyanın içeriğini bilgisayarda bir klasöre çıkarmanız gerekir.

İşletim sistemi ve güvenlik ayarlarına bağlı olarak, zip dosyasını açtıktan sonra aşağıdaki adımları gerçekleştirmeniz gerekebilir:

1. **v902FPSMasterData** / **PackageDeployer_FPSDemoData** klasöründe **FPSDemoData.dll** dosyasını bulun ve dosyaya sağ tıklayın.

2. **Engellemeyi Kaldır**'ı seçin.

3. **Uygula**'yı seçin.

4. **Tamam** seçeneğini işaretleyin.


## <a name="create-or-configure-users"></a>Kullanıcıları oluşturma veya yapılandırma

**FPSDemoData** paketi altı kullanıcıya gerek duyarken **FPSMasterData** paketi, bir kullanıcı gerektirir. Doğru servis talebini, örnek veri paketine bakın.

## <a name="create-or-configure-users---setupreference-data-packages"></a>Oluşturma veya kullanıcı yapılandırma - kurulum/referans veri paketleri

**FPSMasterData** paketi, burada açıklanan ayarlarla birlikte Spencer Low adlı bir kullanıcıyla yüklemek için tasarlanmıştır. Paketi doğru şekilde yüklemek için, gelen örnek veri yapılandırmasını eşleştirmek üzere ortamınızda kullanıcılar oluşturmanız (veya geçici olarak yeniden adlandırmanız) gerekir.

Kullanıcıları oluşturmak veya yapılandırmak için **Ayarlar** > **Güvenlik** > **Kullanıcılar**'a gidin ve aşağıdakileri yapın:

1. Proje Yöneticisi ve Proje Yönetici rolleri için UserFullname="Spencer Low" ve kullanıcı adını da "spencerl" (**küçük harfli**) olarak ayarlayın.

2. **Spencer Low** kullanıcısını seçin ve ardından **Rolleri Yönet**'i seçin. **Sistem Yöneticisi** rolünü bulup seçin ve ardından Spencer Low'a tüm yönetici haklarını vermek için **Tamam**'ı seçin. Bu adım, örnek kayıtların doğru kullanıcı sahipliğiyle oluşturulduğundan emin olmak için gereklidir ve bu nedenle görünümleri doğru şekilde doldurun.

3. İndirilen paketten, varsayılan kullanıcı bağlamının e-posta adresleriyle birlikte bir veri eşleme dosyası güncelleştirmeniz gerekir. Bunu yapmak için **PkgFolder**'ı açın ve ardından Not Defteri'nde (veya Visual Studio'da ya da başka bir XML düzenleyicisinde) **ImportUserMapFile.xml** dosyasını bulun ve açın. **DefaultUserToMapTo=** alanına Spencer Low kullanıcısının e-posta adresini girin.

4. Spencer Low'u **spencerl** kullanıcı adıyla kullanmıyorsanız ek bir dosyayı daha güncelleştirmeniz gerekir. **DemoDataPreImportConfig.xml** dosyasını açın ve ardından **userstocreateandconfigure** etiketini bulun. Spencer Low kullanıcınızın kullanıcı adıyla **\<login\>** etiketini güncelleştirin. Ek ayrıntılar için aşağıdaki [Teknik notlara](#technical-notes) bakın.

## <a name="create-or-configure-users---demo-data-package"></a>Oluşturma veya yapılandırma kullanıcılar - demo veri paketi

Demo verileri paket altı kullanıcıların gerektirir. Paket doğru bir şekilde yüklemek aşağıdakileri yapın:

 1. Mevcut kullanıcıları geçici olarak gelen örnek veri yapılandırmasına eşleştirmek için oluşturun veya geçici olarak adını değiştirin **Ayarlar** > **Güvenlik** > **Kullanıcılar**.
 
    Bu rolleri yalnızca istenen tabanlı tanıtım için gereklidir.  
    - Kullanıcının tam = "David So" Field Service teknisyeni olarak   
    - Kullanıcı tam adı = "Jamie Reding" Müşteri Hizmetleri ve Field Service Dağıtıcısı olarak   
    - Kullanıcı adı = "Molly Clark" Hesap Yöneticisi olarak   
    - Kullanıcı adı = "Spencer Low" Yöntem ve Proje Yöneticisi olarak  
    - Kullanıcı adı ="Veronica Quek" Ekip Üyesi olarak   
    - Kullanıcı adı = "William Contoso"
  
2. Örnek kayıtlarını doğru şekilde almak için veri alma demo amacıyla, Yönetici rolüne yukarıda altı kullanıcılara atayın. 

3. **PkgFolder** açın ve sonra **ImportUserMapFile.xml** bulun ve açın. **Yeni=** alanlarını sisteminizde karşılık gelen kullanıcıların e-posta adreslerine güncelleştirin.

   > [!div class="mx-imgBorder"]
   > ![UserMapFile ekran görüntüsü.](media/sample-data-7.png)

4. "Spencer Low" tam adına sahip kullanıcınız **"spencerl"**'dan başka bir kullanıcı kimliğine sahipse, ek bi dosya güncelleştirmeniz gerekir. **DemoDataPreImportConfig.xml** dosyasını açın ve ardından **userstocreateandconfigure** etiketini bulun. **\<login\>** etiketini loginId olarak (büyük-küçük harf duyarlı) güncelleştirin. 

5. İlk kullanıcının takvimini (içinde **userstocreateandconfigure** etiketi) gösteri verilerinin alınması üzerindeki ayrılabilir tüm kaynaklar için çalışma saatleri doldurmak için kullanılır. **Ayarları** > **güvenlik** > **kullanıcılar**, "Spencer Low" kullanıcısını bulun ve "Çalışma saatlerini" seçeneğini açın. Seçimi varolan çalışma saatlerini düzenleyin **haftalık zamanlama başlangıçtan bitişe kadar yinelenen tüm** seçeneği. **Çalışma saatlerini Pazartesi, Cuma ve saat dilimi Pasifik Saati (ABD ve Kanada) ayarlama 8:00 - 18:00 için (9 saat)** ayarlanmış olduğundan emin olun. Bu, proje ve zamanlama tablosu beklendiği gibi gösterilmesini sağlamak için gereklidir.

**Öneri:** Örnek veri yüklemesi sırasında bir şeyler ters giderse başlangıç noktanıza dönmenizin gerektiği durumda artık kuruluşunuzun bir yedeğini oluşturmayı düşünün. Daha fazla bilgi için bkz. [Kurulumları yedekleme ve geri yükleme](/dynamics365/customer-engagement/admin/backup-restore-instances).

## <a name="run-the-package-deployer"></a>Package Deployer'nı çalıştırma

1. **PackageDeployer_FPSDemoData** VEYA **v902FPSMasterData** klasöründe **PackageDeployer.exe**'i bulun ve çalıştırın.

2. Hüküm ve koşulları kabul edin.

3. Sonraki pencerede:

   a. Dağıtım türünü **Office 365** olarak seçin.

   b. "Kullanıcıları oluşturma veya yapılandırma" bölümünde, yapılandırılan sistem yöneticisinin kullanıcı adını ve parolasını kullanın ("spencerl" kullanıcı adlı "Spencer Low").

   c. **Kullanılabilir kuruluşların listesini görüntüle** seçeneğinin işaretli olduğundan emin olun.

      > [!div class="mx-imgBorder"]
      > ![Kullanılabilir kuruluşların listesini görüntüle" seçeneğinin seçili olduğu durumda Package Deployer penceresinin ekran görüntüsü](media/sample-data-2.png)

4. Örnek verileri yüklemek istediğiniz kuruluşu seçin.

5. **Demo Veri Kurulumu** iletişim kutusunu görene kadar **İleri**'yi seçin.

   > [!div class="mx-imgBorder"]
   > ![Demo veri yükleyicisi durum penceresinin ekran görüntüsü.](media/sample-data-3.png)

6. Devam etmeden önce, örnek verileri yüklemenin bir saat kadar (normalde yaklaşık 10 dakika) sürebileceğini unutmayın. Yükleme işlemi sırasında bilgisayarın açık ve bir ağa bağlı olduğundan ve oturumunuzun etkin kaldığından emin olmanız gerekir.   

7. Hazır olduğunuzda, örnek verileri yükleme işlemini başlatmak için **İleri**'ye tıklayın. Örnek verilerin yüklenmesinin ardından **Son**'a tıklayın.

## <a name="verify-the-sample-data-installation"></a>Örnek veri yüklemesini doğrulama

Tutarlılık kontrolü için, Fabrikam Robotics kurgusal senaryosunda listelenen kayıt sayısının ve varlık türlerinin beklendiği gibi göründüğünü doğrulayın.

Örnek veriler tamamen yüklendikten sonra Spencer Low kullanıcısı olarak oturum açın ve aşağıdakileri onaylayın:

- Project Service uygulaması yüklüyse **Project Service** > **Ayarlar** > **Fiyat Listeleri**'ne gidin. Fatura oranları ve maliyet oranlarının, veri kümesinde her bir ülke/bölge için uygun para birimiyle mevcut olduğunu onaylayın.

- Project Service uygulaması yüklüyse **Universal Resource Scheduling** > **Ayarlar** > **Kuruluş Birimleri**'ne gidin. Uygun para birimli maliyet fiyatı listesinin (şehir girişleri hariç) her bir kuruluş birimiyle ilişkili olduğunu onaylayın. Herhangi bir eksik varsa bunu bulun ve doğru maliyet fiyatı listesiyle ilişkilendirin.

- Field Service uygulaması yüklüyse **Project Service** > **Ayarlar** > **Fiyat Listeleri**'ne gidin. Fatura oranları ve maliyet oranlarının mevcut olduğunu onaylayın. **Field Service** > **Ayarlar** > **Fiyat Listeleri**'ne gidin ve fatura oranları ile maliyet oranlarının, veri kümesinde her bir ülke/bölge için uygun para birimiyle mevcut olduğunu denetleyin.

  > [!div class="mx-imgBorder"]
  > ![Etkin fiyat listelerinin ekran görüntüsü.](media/sample-data-4.png)

  > [!div class="mx-imgBorder"]
  > ![Etkin kuruluş birimlerinin ekran görüntüsü.](media/sample-data-5.png)

## <a name="technical-notes"></a>Teknik notlar

Bu verilerin yüklenmesinde daha fazla teknik ayrıntı için aşağıya bakın.

### <a name="installing-sample-data-on-top-of-existing-data-not-recommended"></a>Örnek verileri mevcut verilerin üzerine yükleme (önerilmez)

Örnek verileri zaten bu verilerin bulunduğu mevcut bir Field Service veya Project Service deneme sürümü veya demo ortamı üzerine yüklemeniz gerekirse yükleyici tarafından gerçekleştirilen güvenlik ön denetimlerini askıya almanız gerekir.

Bunu yapmak için **DemoDataPreImportConfig.xml** dosyasını Not Defteri (veya başka bir XML düzenleyicisi) ile bulmak ve açmak üzere **PkgFolder** klasörüne gidin.

Aşağıdaki değeri bulun ve ardından ayarını doğru yerine yanlış olarak değiştirin:

```alias
<TerminateOnPreCheckFailure>true</TerminateOnPreCheckFailure>
```

Bu değişiklik, aşağıdakiler dahil olmak üzere yükleyicinin bazı önemli güvenlik denetimlerini atlamasına neden olur:

- Birden fazla etkin **Kuruluş Birimi** kaydının olmadığını onaylama ve ardından bunu **Fabrikam ABD** olarak yeniden adlandırma.

- Birden fazla etkin **İş Şablonu** kaydının olmadığını onaylama.

- Birden fazla etkin **Proje Parametresi** kaydının olmadığını onaylama ve ardından bu girişi **Parametreler** olarak yeniden adlandırma.

### <a name="configuration-components"></a>Yapılandırma bileşenleri

Bu içeri aktarma öncesi yapılandırma dosyasında bir dizi diğer yapılandırma bileşeni vardır. Teknik kullanıcılar için bunlardan bazıları şunlardır:

- **\<RequiredSolutions\>** önkoşul çözüm yüklemelerini ve bunların sürüm numaralarını belirtir.

- **\<InstallSampleData\>** kullanıma hazır örnek verilerin uygulamalarda yüklü olup olmadığını denetler.

    - yanlış: (kaldırılabilir olan) bu yerleşik verilerin yüklenmesini atlar

    - doğru: yerleşik verileri, FS ve PSA örnek veri yüklemesiyle eşzamanlı olarak yükler

- **\<PreImportDataCollection\>** düz dosya Veri Eşlemelerini ve ana örnek veri yüklemesinin sonrasında alınacak ilişkili Kayıtları belirtir.

- **\<EntitiesToEnableScheduling\>** Microsoft Dynamics Scheduling uygulamasında (Universal Resource Scheduling olarak da bilinir) Ayırma için hangi varlıkların etkinleştirilmesi gerektiğini belirler.

- **\<UsersToCreateAndConfigure\>** örnek verileri içeri aktarmanın yürütülmesinden önce (mevcut durumda yoksa) oluşturulacak Ayrılabilir Kaynakları belirtir. Kaynak sistem örnek veri Ayrılabilir Kaynağının, FullName ve her bir kaynağın oturum açmasında hedef sistem Ayrılabilir Kaynak kayıtlarıyla eşleştiğini lütfen unutmayın. Bu nedenle, önce bu adları kullanarak hedef sisteme örnek verileri içeri aktarmadığınız, daha sonra Etkin Kullanıcı kayıtlarının yanı sıra istediğiniz ad kümesi için Ayrılabilir Kaynakları yeniden adlandırmadığınız ve ardından son hedef sisteminize içeri aktarmak için verileri tekrar dışa aktarma (**ImportUserMapFile.xml** dosyasını Eski ve Yeni girişlere uygun şekilde güncelleştirme) yapmadığınız sürece bu ön yapılandırma dosyasındaki adları değiştirmeniz mümkün DEĞİLDİR.

- **\<PluginsToDisable\>** örnek verileri içeri aktarma sırasında devre dışı bırakılması ve ardından tekrar etkin hale getirilmesi gereken çok farklı satır öğesi eklentilerini belirtir.

### <a name="fabrikam-robotics-fictitious-scenario"></a>Fabrikam Robotics kurgusal senaryosu

Field Service ve Project Service örnek referans veri paketleri, yaklaşık 4000 kayıt ve yaklaşık 40 farklı varlığın yanı sıra **Fabrikam İmalat Ana Verileri (v3.0.0.0) çözümünü** yükler. Field Service veya Project Service için ayrı örnek veri paketleri bu uygulama için **v902FPSMasterData** örnek verilerinin bir alt kümesini içerir. **Demo verileri** paketini yüklemelerini **Fabrikam üretim Demo verileri (v3.0.0.7) çözüm** 148 varlıkları arasında yaklaşık 22.000 kayıtlarla.

Kurgusal bir şirket olan Fabrikam Robotics bir elektronik cihaz montaj hattı robotları üreticisidir ve yükleme planlama, uygulama ve sürekli bakım hizmetleri dahil olmak üzere ürün kalitesi, yenilik ve güçlü müşteri hizmetleri ile bilinir. Fabrikam, Amerika Birleşik Devletleri merkezlidir (Fabrikam ABD) ve Fransa, Hindistan, Birleşik Krallık ve İsviçre'de proje tabanlı servis operasyonları vardır.

Field Service operasyonları çoğunlukla daha büyük Seattle bölgesinde olmak üzere Amerika Birleşik Devletleri merkezlidir. Şirket, müşteri varlık performansını izlemek ve giderek daha proaktif yerinde hizmetler sunmak için Nesnelerin İnterneti (IoT) bağlantısından yararlanmaya odaklanır.

Örnek verilere yüksek düzeyde bir genel bakış aşağıdaki gibidir:

- Ortak örnek veri öğeleri (her iki uygulamada da yer alır)

    - 1 kullanıcı

    - 71 firma

    - 137 ilgili kişi

    - Çeşitli işlem türleri ve kategorileri

    - 1 ürün fiyat listesiyle birlikte 50 ürün

    - 14 fiyat/maliyet listesi

    - 3 düzeyli (derecelendirme değerli) 2 derecelendirme modelinde 31 özellik (kaynak becerileri)

- Project Service

    - 8 kuruluş birimi

    - 6 role özgü kullanım düzeyi

    - 2,8k+ rol-fiyat belirtimi

- Field Service

    - 4 bölge

    - 5 iş emri türü

    - 22 müşteri varlığı

    - Bir dizi ilişkili kaynak özelliği (9), hizmet (13) ve hizmet görevi (13) ile birlikte 9 olay türü
   
**Demo verileri** yaklaşık 179 iş emirleri, 12 projeleri ve ilişkili işlem veri paketi yükler. 

### <a name="change-the-work-hours-for-sample-resources"></a>Örnek kaynaklar için çalışma saatlerini değiştirme

Tüm ayrılabilir kaynakların varsayılan 24 çalışma saatli bir takvimi vardır.

Örnek ayrılabilir kaynaklar için çalışma saatlerini değiştirmeniz gerekirse **Universal Resource Scheduling** > **Zamanlama** > **Kaynaklar**'a gidin.

Bir kullanıcı seçin (örneğin Spencer Low) ve birden fazla kullanıcıya uygulamak istediğiniz saatler için Spencer'ın çalışma saatlerini değiştirin. **Universal Resource Scheduling** > **Ayarlar** > **Çalışma Saati Şablonları**'na gidin ve **Varsayılan İş Şablonu** kaydını düzenleyin. **Şablon Kaynağı** alanında, diğer kaynaklara uygulamak istediğiniz çalışma saatlerine sahip bir kullanıcı seçin. **Universal Resource Scheduling** > **Zamanlama** > **Kaynaklar** > **Etkin Ayrılabilir Kaynaklar**'a gidin. Değiştirmek istediğiniz kaynakları seçin ve ardından **Takvim Ayarla**'yı seçin. **İş Şablonu** açılan listesinde **Varsayılan Çalışma Saati** şablonunu veya doğru şablonlaştırılan kaynakla birlikte başka bir şablonu seçin. Zamanlama panosuna gittiğinizde, güncelleştirilmiş çalışma saatlerine sahip kaynakları artık görebilmeniz gerekir.

> [!div class="mx-imgBorder"]
> ![Etkin ayrılabilir kaynakların ekran görüntüsü.](media/sample-data-6.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]