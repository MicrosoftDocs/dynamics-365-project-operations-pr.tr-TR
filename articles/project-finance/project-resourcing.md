---
title: Proje kaynakları
description: Bu konuda, proje kaynakları hakkında bilgi sağlanır.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9352465f83abe19097945dd34eada365cd03b8f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756572"
---
# <a name="project-resourcing"></a>Proje kaynakları

[!include [banner](../includes/banner.md)]

Bu konuda, proje kaynakları hakkında bilgi sağlanır.

Proje planlama aşaması sırasında proje yöneticileri ve kaynak yöneticilerinin yaşadığı zorluk kaynak ayırmaktır ve bu aşamada projede çalışacak doğru kaynaklara karar vermek ve ayırmak zorunda kalırlar. Dynamics 365 Finance uygulamasında projelere ait kaynakların belirlenmesi ile ilgili özellikler belirli bir görevlendirme veya görevlendirmenin bir parçası için ayrılabilen geçici kaynaklar olarak kabul edilen roller tanımlamanıza olanak sağlar. Bu tür kaynak belirleme proje yöneticileri ve kaynak yöneticileri aşağıdaki görevleri tamamlamalarına olanak sağlar:

- Kaynakları eşleştirmeyi kolaylaştıracak şekilde gerekli olan yetkinliklere sahip bir rol tanımlama.
- Ayrılmış kaynaklara göre ilk bir görevlendirme zamanlamasını tanımlamak için rolleri kullanma.
- Bir projeyle ilgili atanan rollere ve kaynaklara göre maliyetleri tahmin etme ve bir başlangıç bütçesini saptama.
- Her bir görevlendirme için gerekli kaynak ayırma sayısını tahmin etmek için rolleri kullanma.
- Projenin tam yaşam döngüsü için gerekli olan kaynak sayısını tahmin etme.
- İlk kaynak atamalarını kullanarak bir iş kırılım yapısı (İKY) taslağı oluşturma.

[![Proje yaşam döngüsü](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)

Proje planlaması devam ettikçe, planlanan kaynaklar, personelli kaynaklarla değiştirilebilir. Ayrıca, proje yöneticisi herhangi bir proje aşaması sırasında dönerek kaynak ayrılmasını güncelleştirebilir.

## <a name="set-up-project-resources"></a>Proje kaynaklarını ayarlama
Bir takvim ayarlamanız ve bunu bir çalışan veya iş gücü ile ilişkilendirmeniz gerekir. Takvim, projeyi ve proje için ayrılmış kaynakların çalışma süresini zamanlamak için kullanılır. Takvim ayarı sırasında, proje yöneticileri kaynak iyileştirmesinin parçası olarak kaynak dengelemesi yapabilir. Takvim zamanlamasına bağlı olarak, kaynaklara sınırlamalar konabilir. **Takvimler** sayfasında bir takvim ayarlayabilirsiniz.

Bir çalışanı proje kaynağı olarak ayarladığınızda, kaynak ayarladığınız şirkette çalışan çalışanlar arasından seçim yapabilirsiniz. Alternatif olarak, kuruluşunuzdaki diğer şirketlerden çalışanlar seçebilirsiniz. Bu çalışanlar şirketlerarası kaynaklar olarak bilinir.

Aşağıdaki yordamlarda, bir çalışanın şirketinizdeki bir proje kaynağı olarak nasıl ayarlanacağı ve bir şirketlerarası proje kaynağının nasıl ayarlanacağı açıklanmaktadır.

### <a name="set-up-a-worker-as-a-project-resource"></a>Çalışanı proje kaynağı olarak ayarlama

1. **Çalışanlar** sayfasında, **Çalışanlar** listesinde, proje kaynağı olarak eklemekte olduğunuz çalışanı seçin ve çalışan kaydını açın.
2. Eylem bölmesinde **Proje** &gt; **Kurulum** &gt; **Proje kurulumu**'nu seçin.
3. Bir takvim seçin ve sonra sayfayı kapatın.

Ön atama türü olarak bir kaynak için varsayılan projelerini de belirtebilirsiniz. Kaynak yöneticisi veya proje yöneticisi kaynağın önceden hangi projelerde çalışacağını bildiği ön atamalar özelliği kullanılabilir. Ön atamalar, proje sponsoru ya da müşteri talebine dayanabilir. Bir projeyi önceden atamak için **Proje ata** sayfasında **Projeler** sekmesinde, **Kalan projeler** listesinden uygun projeyi seçin.

### <a name="set-up-an-intercompany-resource"></a>Şirketlerarası kaynak ayarlama

Bir çalışanı şirketlerarası kaynak olarak ayarladığınızda, ayarı hem ödünç veren şirkette, hem de ödünç alan şirkette tamamlamanız gerekir.

**Ödünç veren şirkette**

1. Finance'de, ödünç veren şirketinin seçili olduğunu doğrulayın ve ardından önceki "Çalışanı proje kaynağı olarak ayarlama" bölümündeki yordamı tamamlayın.
2. **Şirketlerarası muhasebe** sayfasında, **Yeni**'yi seçin.
3. **Tüzel kişilik kodu** alanında, ödünç veren şirketi seçin. Alanları uygun şekilde doldurun ve ardından **Kaydet**'i seçin.
4. **Transfer fiyatları** sayfasında, **Yeni**'yi seçin.
5. **Ödünç alan tüzel kişilik** alanında, uygun şirketi seçin.
6. Ödünç alan şirkete yalnızca bu bölümün başlangıcında oluşturduğunuz kaynağı vermek için, **Kaynak** alanında, oluşturduğunuz kaynağın adını seçin. Ödünç veren şirketteki tüm kaynakların ödünç alan şirket tarafından kullanılabilir olmasını sağlamak için **Kaynak** alanını boş bırakın.
7. **Proje yönetimi ve muhasebe parametreleri** sayfasında, **Şirketlerarası** sekmesinde, **Şirketlerarası kaynak planlama ve zaman çizelgelerini etkinleştir** seçeneğini **Evet** olarak ayarlayın.

**Ödünç alan şirkette**

- **Kaynaklar listesi** sayfasındaki arama filtresi alanında, ödünç veren şirket için oluşturduğunuz kaynağın adını girin ve adın ödünç alan şirketin kaynak listesine eklendiğini doğrulayın.

## <a name="manage-resource-competencies"></a>Kaynak yetkinliklerini yönetme
Kaynak yetkinlikleri kaynak yönetiminin temel bir parçasıdır. Beceri, eğitim, sertifika ve proje deneyiminin doğru şekilde dengelendiği kaynakları belirlemek için yetkinlikler temel olarak kullanılabilir. Bu bilgileri her kaynak için ayarlamanız ve düzenli aralıklarla güncelleştirmeniz gerekir. Bu şekilde, proje kaynak ataması sırasında belirli kaynak yetkinliklerinin eşleştirildiği özellikleri en üst düzeye çıkartabilir.

[![Beceriler, sertifikalar, eğitimler ve proje deneyimi ile ilgili örnekler](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)

Aşağıdaki yordamlarda, bir kaynağın bazı yetkinlik türlerinin nasıl ayarlanacağı açıklanmaktadır.

Bir çalışana ait yetkinlikleri ayarlamak üzere, İnsan kaynakları'ndaki **Çalışanlar** listesi sayfasını veya Proje yönetimi ve muhasebe modülündeki **Kaynaklar** listesi sayfasını kullanabilirsiniz. Aşağıdaki yordamlar için, İnsan kaynakları'ndaki **Çalışanlar** listesi sayfası kullanılır.

### <a name="set-up-competencies-certificates"></a>Yetkinlik ayarla: sertifikalar

1. **Çalışanlar** listesi sayfasında, çalışanın sertifika bilgilerini eklemek için bir satır seçin.
2. Eylem Bölmesi'ndeki **Çalışan** sekmesinde, **Yetkinlikler** grubunda **Sertifikalar** seçeneğini tıklayın.
3. **Yeni** seçeneğini, ardından **Sertifika türü** alanında **PMP**'yi belirleyin.
4. **Başlangıç tarihi** alanında, **1.10.2015** tarihini seçin ve **Kaydet**'i seçin.

### <a name="set-up-competencies-skills"></a>Yetkinlik ayarla: Beceriler

1. **Çalışanlar** listesi sayfasında, önceki yordamda kullandığınız çalışanın hala seçili olduğundan emin olun. Ardından Eylem Bölmesi'ndeki **Çalışan** sekmesinde, **Yetkinlikler** grubunda **Beceriler** seçeneğini tıklayın.
2. **Yeni**'yi seçin.
3. **Beceri** alanında, **Proje yönetimi**'ni seçin.
4. **Düzey** alanında, **5 Uzman** seçeneğini belirleyin.
5. **Düzey tarihi** alanında, **14.01.2014** seçeneğini belirleyin.
6. **Deneyim yılları** alanında, **10** girin.
7. **Kaydet**'i seçin ve sayfayı kapatın.

## <a name="create-a-new-project"></a>Yeni proje oluşturma
1. **Proje yönetimi** sayfasında **Yeni proje**'yi seçin ve aşağıdaki değerleri girin:

    - **Proje türü:** Zaman ve malzeme
    - **Proje adı:** XYZ Yükseltme Aşaması 2
    - **Proje grubu:** TM\_WIP
    - **Proje sözleşmesi kodu:** 00000002

2. **Proje oluştur**'u seçin.

### <a name="assign-a-resource-to-a-project"></a>Projeye kaynak atama

1. **Çalışanlar** sayfasında, **Çalışanlar** listesinde, daha önce yetkinlik ayarladığınız çalışana ait kaydı seçin ve çalışan kaydını açın.
2. Eylem Bölmesi'ndeki **Proje** sekmesinde, **Kurulum** grubunda **Projeleri ata** seçeneğini belirleyin.
3. **Kaynak doğrulama proje atamaları** sayfasında, **Projeler** sekmesinde, **Projeyi seçili projelere ekle** alanına **XYZ Yükseltme Aşama 2** projesinde filtre uygulayın.
4. **Kalan projeler** bölmesinde, bir proje seçin ve **Seçili projeler** bölmesine eklemek için ok düğmesini seçin.

Ayrıca, gereksinim duydukça bir kaynak için kategoriler de atayabilirsiniz. Kategori türü **Maliyet** ya da **Gelir** olur. Kategori türü, kuruluşunuz tarafından belirlenir. Bir kaynak için kategori atanmamışsa, Finance maliyet ve gelir için saat fiyatlarındaki varsayılan kategoriyi arar.

### <a name="set-up-project-resource-and-role-characteristics"></a>Proje kaynağı ve rol özelliklerini ayarlama

Proje yöneticisi proje için gerekli olan rolleri oluşturmak için proje kaynağı işlevselliğini kullanabilir. Kaynaklar ayrılırken teyit edilmiş kaynaklar hala bilinmiyorsa, roller kullanılabilir. Roller planlanan kaynak olarak geçici olarak ayrılabilir; böylece proje planlama aşamaları devam edebilir.

[![Rol örneği](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Senaryo:**: Contoso, onaylı proje tüzüğü olan zaman ve malzeme projesini gerçekleştirmek için işe alındı. Yardımcı proje yöneticisi hala proje kapsamını tamamlıyor. Kaynak yöneticisi şu anda yeni projede çalışmak üzere ayrılacak belirli kaynakları tanımlıyor. Projenin kritik doğası nedeniyle proje sponsoru Uzman proje yöneticisi rolünün de dahil edilmesini istedi. Proje planlaması sırasında, yardımcı proje yöneticisi kaynak bilgisine gerek duyar diye kaynak yöneticisi yeni kaynağı almalıdır ve sistemde rolü tanımlamalıdır.

Aşağıdaki adımlarda, kaynak yöneticisinin Kıdemli Proje Yöneticisi rolünü nasıl ayarlayabileceği ve bununla kaynak özelliklerini nasıl ilişkilendirebileceği gösterilmektedir. Daha sonra, rol gerekli kaynak yetkinlikleri ile eşleşen kullanılabilir kaynakları aramak için kullanılabilir.

1. **Ayar rolleri** sayfasında **Yeni**'yi seçin ve aşağıdaki değerleri girin:

    - **Rol kodu:** Kıdemli Proje Yöneticisi
    - **Açıklama:** Kıdemli Proje Yöneticisi

2. **Oluştur**'u seçin.
3. **Kıdemli Proje Yöneticisi** rolünü seçin ve **Özellikleri yapılandır**'ı seçin.
4. **Özellikler türü** alanında, **Beceri**'yi seçin.
5. **Kullanılabilir özellikler** alanına, aranacak beceriyi girin.
6. **Özellik türü** alanında, **Sertifika**'yı seçin.
7. **Kullanılabilir özellikler** alanına, aranacak sertifika türünü girin.

### <a name="assign-a-project-resource-to-a-project"></a>Projeye proje kaynağı atama

1. **Tüm projeler** sayfasında, **XYZ Yükseltme Aşama 2** projesini seçin.
2. **Proje ekibi ve zamanlama** sekmesinde **Ekle**'yi seçin.
3. **Rol** alanında, **Takım üyesi**'ni seçin.
4. **Takvimden rezerve et** seçeneğini belirleyin.
5. **Kaynak kullanılabilirliği** sayfasında **Ayarları görüntüle**'yi seçin.
6. **Görünüm ayarlarını ayarla** sayfasında, aşağıdaki değerleri girin:

    - **Tarih aralığı görünümü biçimi:** Gün
    - **Kullanılabilirlik açıklamalarını görüntüle:** Evet
    - **Kalan kapasiteyi görüntüle:** Evet

7. Kaynaklar listesinden bir kaynak seçin.
8. **Kesin rezervasyon** ve **Tam kapasite** seçeneğini belirleyin.


### <a name="assign-a-resource-to-a-default-role"></a>Kaynağa varsayılan bir rol atama

Proje veya kaynak yöneticilerinin proje için ayrılabilecek kaynaklar ile ilgili daha fazla detaya gitmesine olanak sağlamak için. Varsayılan bir rolü, var olan bir kaynakla veya yeni alınan bir kaynakla ilişkilendirebilirsiniz. Örneğin, Daniel işe alındığında, Iş analisti rolünü doldurmaya yönelik deneyim ve beceriler vardı. Kaynak yöneticisi bu rolü Daniel'in varsayılan rolü olarak atamıştır. Bu nedenle, kaynak yöneticisi, projelerde çalışabilecek iş analistleri havuzuna Daniel'i eklemiştir.

Kaynak ayırma sırasında, proje yöneticileri projelerde çalışabilecek rol kaynaklarına filtre uygulayabilir. Bu bilgiler, kaynakların karşılanması sırasında çok ölçütlü karar analizi yaparken bu bilgileri tek bir ölçüt olarak kullanabilirler. Belirli bir projeyle ilgili özel becerilere, eğitimlere ve deneyimlere sahip kaynakları aramak için filtreye başka kaynak özellikleri de ekleyebilirler.

**Senaryo:** Onaylanmış bir proje başlatıldı ve Kıdemli proje yöneticisi rolü proje planlama aşaması sırasında planlanmış bir kaynak olarak ayrıldı. Kaynak yöneticisi artık Kıdemli proje yöneticisi rolünü karşılamak için bir kaynak aldı.

1. **Kaynaklar listesi** sayfasında **Daniel Goldschmidt**'i seçin.
2. **Kaynak rolleri** sayfasında **Yeni**'yi seçin ve aşağıdaki değerleri girin:

    - **Etkin:** Geçerli tarihi girin.
    - **Süre sonu**: **Hiçbir zaman** değerini girin.
    - **Rol**: **Kıdemli Proje Yöneticisi** rolünü girin.

3. **Kaydet**'i seçin ve sayfayı kapatın.
4. **Yetkinlikler** sekmesinde, **ProjectMgmt** becerisini ve **PMP** sertifikasını ekleyin.

## <a name="set-up-role-based-pricing"></a>Rol tabanlı fiyat ayarlama
Tüm maliyet, satış ve transfer fiyatları roller için ayarlanabilir.

1. **Satış fiyatı (saat)** sayfasında, **Yeni**'yi seçin ve geçerlilik tarihini girin.
2. **Rol** sütunundan bir rol seçin.
3. **Fiyatlandırma** sütununa, seçili kaynak rolü için bir fiyat girin.

## <a name="form-a-project-team"></a>Proje ekibi oluşturma
Bir projede önceden ayarlanmış rolleri kullanmak için proje yöneticisi rolleri projeyle ilişkilendirmelidir. Bir proje için birden çok rol atanabilir. Karışıklık oluşmasını engellemek için, bu roller ayırma sırasında otomatik olarak etiketlenir. Örneğin, proje yöneticisi üç yazılım mühendisine gereksinim duyduğunda, **yazılım mühendisi 1**, **yazılım mühendisi 2** ve **yazılım mühendisi 3** olarak olan etiketlenen üç yazılım mühendisi rolü otomatik olarak oluşturulur. Rol özellikleri rol için daha önceden ayarlanmışsa, özellikler kaynak araması sırasında filtre olarak uygulanır. Aramayı daha da sadeleştirmek için, ek özellikler gerektikçe eklenebilir.

Görünüm ayarları, kaynak kullanılabilirliğinin daha iyi bir görünümünü vermek için de özelleştirilebilir. Saatlik, günlük, haftalık, aylık, üç aylık ve yıllık kullanılabilirlik seçeneklerini gösterme seçenekleri vardır. Kaynaklar üzerinde kullanılabilir ve kalan kapasiteyi gösterme seçeneği de vardır. Bu seçenek, etkinlik veya kaynak kullanılabilirliği için kullanılabilir zamanı tahmin ederken zaman yönetimi için kullanışlıdır.

Proje yöneticisi sayfada bir rol seçebilir ve gereksinime uyan bir kaynak varsa, rolü doldurmak için bir kaynak ayırmayı seçer. Kaynakların planlama aşaması sırasında bu noktada ayrılmasının zorunlu olmadığını unutmayın. İKY oluştururken, proje için rolleri personelli kaynakla değiştirebilirsiniz. Roller İKY'de personelli kaynaklarla değiştirilmişse, kaynak kurulumu proje ekibi dökümünü ve zamanlamasını otomatik olarak güncelleştirir.

[![Rollerin ve gerçek kaynakların her ikisini de içeren proje ekibi dökümü](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Proje yöneticisinin **Kalan kapasite**, **Tam kapasite**, **Kapasite yüzdesi** ve **Saatleri belirt** gibi bir projeyle ilgili kaynağı belirlemek için çeşitli seçenekleri vardır. Bu ayırma seçenekleri, kaynak atamaları değiştirilirse istediğiniz zaman iptal edilebilir. İki tür ayırma desteklenir:

- **Kesin Ayırma**: Kaynak ayırma onaylanmıştır ve belirtilen süre boyunca görevlendirmede çalışma onaylanmıştır.
- **Geçici ayırma**: Kaynak ayırma geçici olarak belirtilen süre boyunca görevlendirmede çalışacak şekilde ayarlanmıştır onaylanmıştır.

Aşağıdaki yordamda, proje ekibinin nasıl oluşturulacağı açıklanmıştır:

### <a name="create-a-project-team"></a>Proje ekibi oluşturma

1. **Tüm projeler** liste sayfasında bir proje seçin ve sonra **Düzenle**'yi seçin.
2. **Proje ekibi ve zamanlama** sekmesinde, **Zamanlama bitiş tarihi** alanına, zamanlama başlangıç tarihi artı bir ay girin. Örneğin, zamanlama başlangıç tarihi 24 Haziran 2017 (24.06.2017) ise, **24.07.2017** girin.
3. **Ekle**'yi seçin.
4. **Projeye roller ekle** bölmesinde **Rol** alanından, **Kıdemli Proje Yöneticisi**'ni seçin.
5. **Gerekli yetkinlikler** seçeneğini belirleyin.
6. **Özellikleri seç** sayfasında, Kıdemli proje yöneticisi rolü için önceden ayarladığınız özellikler varsayılan olarak seçilidir. **Tamam**'ı seçin.
7. **Projeye rol ekle** sayfasında, **Kaynak sayısı** alanına **1** girin.
8. **Kaynak** alanında, arama gerekli yetkinliklere sahibi olan tüm kaynakları gösterir. **Daniel Goldschmidt**'i seçin ve **Oluştur**'u seçin.
9. **Proje** sayfasında **Ekle**'yi seçin.
10. **Projeye roller ekle** bölmesinde **Rol** alanından, **Takım üyesi**'ni seçin. **Kaynak sayısı** alanına, **5** girin.
11. **Oluştur**'u seçin.
12. **Projeler** sayfasında **Kaynağı karşıla**'yı seçin.

## <a name="resource-capacity-synchronization"></a>Kaynağın kapasitesini eşitleme
Kaynak eşitleme işlemleri, takvim ve temel takvimle ilgili bilgilerin project kaynak zamanlamasına doğru sağlanmasına yardımcı olur. Takvim değiştirilirse, işlemler proje kaynaklarının zamanlamasında gerekli güncelleştirmeleri yapar. Bu işlemler, takvimin kaynak bilgileri önceden eşitlendiğinden performansın artırılmasına da yardımcı olur. Bu nedenle, kaynak zamanlama bilgilerinde yapılan güncelleştirmeler daha çabuk gerçekleşir. İşlemleri bir defada değil, toplu iş olarak zamanlamanız önerilir. Aksi takdirde, bilgilerin son eşitlediği tarihlerin dahil edilmesinin unutulma riski vardır. Dahil edilen tarihler kullanılmazsa, tarih eşitlemesi sırasında boşluklar oluşabilir.

![Takvim eşitlemesi](./media/projectresourcing04-1024x471.jpg)

### <a name="synchronize-resource-capacity-roll-ups"></a>Kaynağın kapasite toplamalarını eşitle

Eşitleme işlemi tüm kaynak takvimi bilgilerini eşitlemek için tasarlanmıştır. Bu bilgiler, projenin Kaynak takvimi kapasite tablosundaki herhangi bir değişiklikle ilgili temel takvim bilgilerini içerir. Projeye yeni kaynaklar eklenirse, eşitleme işlemi güncelleştirilmiş takvim bilgilerinin kullanılabilir olmasını garantilemeye yardımcı olur. Bu eşitleme, istediğiniz zaman yapılabilir.

Toplu iş seçeneğini kullanmanızı öneririz. Kapasite ayırmaların eşitlenmesi sırasında seçenekler bulunur.

1. **Proje yönetimi ve muhasebe** &gt; **Dönemlik** &gt; **Kapasite eşitlemesi** &gt; **Kaynağın kapasite toplamalarını eşitle** seçeneklerini belirleyin.
2. Aşağıdaki tabloda bulunan seçenekleri ayarlayın.

    | Seçenek      | Açıklama |
    |-------------|-------------|
    | Dönem kodu | İsteğe bağlı olarak, kaynak kapasitesi toplamasına yönelik eşitleme işleminin başlangıç ve bitiş tarihlerini ayarlamak için Genel muhasebe tarih aralığı kodunu seçin. |
    | Başlangıç tarihi  | Kaynak kapasitesi toplamasına yönelik eşitleme işleminin başlangıç tarihini girin. |
    | Bitiş tarihi    | Kaynak kapasitesi toplamasına yönelik eşitleme işleminin bitiş tarihini girin. |

[![Eşitleme işlemi](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>İKY şablonları üzerinde rolleri ayarlama
Proje yöneticileri, yeni projeler için İKY oluştururken uygulayacakları İKY şablonlarını ayarlayabilir. Proje yöneticileri, bir şablon oluştururken roller ekleyebilirler. Bir İKY şablonuna rol atamak için aşağıdaki yordamı kullanın.

1. **Proje yönetimi ve muhasebe** &gt; **Kurulum** &gt; **Projeler** &gt; **İş kırılım yapısı şablonları**'nı seçin.
2. Seçili İKY şablonu için **Ayrıntıları** seçin.
3. Listeden bir görev seçin ve **Rol** alanında göreve atanacak bir rol seçin.

### <a name="work-with-a-wbs"></a>İKY ile çalışma

Yeni bir İKY oluşturabilir veya var olan İKY şablonundan bir İKY kopyalayabilirsiniz. Proje yöneticisi, İKY'deki yeni görevlere roller atayarak kaynakları kolayca yönetebilir. Roller bir kaynak alındıktan sonra veya görev üzerinde çalışacak onaylı bir kaynak belirlendikten sonra değiştirilebilir. Bu esneklik proje yöneticilerinin aşağıdaki görevleri gerçekleştirmelerini sağlar:

- İKY iş paketleri için gereken kaynak sayısını tanımlama.
- Proje maliyetlerini tahmin etme.
- Ön bütçe belirleme.
- Rollere ve kaynaklara göre, etkinlik süresini tahmin etme.
- Kullanılabilir proje bilgilerine dayanan bazı proje yönetim planları geliştirme.

Kaynak atama işlevselliğini daha iyi kullanmak için IKY'ye ek seçenekler eklenmiştir.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Seçenek</th>
<th>Açıklama</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kaynak atamaları</td>
<td>İKY'deki görevler için atanan kaynakları, tarihleri, saat sayısını ve ayırma türünü görüntüleyin.</td>
</tr>
<tr class="even">
<td>Otomatik takım oluşturma</td>
<td>Görevle ilişkili rolleri kullanarak planlanmış kaynakları otomatik olarak ekleyin. Finance, otomatik olarak rollere dayalı çok ölçütlü karar analizini kullanarak planlanan kaynakları önerir. Roller ve çalışma (saat), bir İKY içindeki görevler için ayarlandıktan ve yapı yayımlandıktan sonra, <strong>Otomatik takım üret</strong>'i seçin. Gerekli planlanmış kaynak sayısı İKY'ye ve <strong>Proje ve ekip zamanlama</strong> sekmesine eklenir.</td>
</tr>
<tr class="odd">
<td>Kaynak (açılır liste)</td>
<td><strong>Kaynak atamasını başlat</strong> sayfasında, belirtilen süreye göre, kaynakları kesin ayırma veya geçici ayırma olarak seçebilirsiniz. Kaynak etkinliklerinin süresini görmek ve ayarlamak için görünüm ayarlarını yapabilirsiniz. Aşağıdaki seçenekleri kullanarak, iş paketi düzeyinde kaynak seçip bunları atayabilirsiniz:
<ul>
<li><strong>Kabul et</strong>: Göreve atanan kaynakta yapılan değişiklikleri onaylayın.</li>
<li><strong>İptal</strong>: Göreve atanan kaynakta yapılan değişiklikleri iptal edin.</li>
<li><strong>Otomatik olarak ata</strong>: Eşleşen bir role sahip kullanılabilir personelli kaynak otomatik olarak seçilir ve seçilen göreve atanır.</li>
</ul></td>
</tr>
</tbody>
</table>

1. **Tüm projeler** sayfasında, **XYZ Yükseltme Aşama 2** projesini seçin.
2. **Plan** &gt; **Etkinlikleri** &gt; **İş kırılım yapısı**'nı seçin.
3. Aşağıdaki düzey bir etkinlikleri İKY'ye eklemek için **Yeni**'yi seçin:

    - Başlatma
    - Planlama
    - Yürütülüyor
    - İzleme ve Denetleme
    - Kapat

4. Aşağıdaki şekilde gösterildiği gibi, tarih ve çalışma (saat) değerlerini ayarlayın.

    [![Tarih ve çalışma ayarlama](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. **Başlatma** görev satırını seçin ve **Rol** alanında, **Kıdemli Proje Yöneticisi**'ni seçin.
6. **Yayımla** öğesini seçin.
7. Aynı satırda, **Kaynak** alanında **Daniel Goldschmidt**'i seçin ve **Kabul et**'i seçin.
8. **Planlama** görev satırını seçin ve **Rol** alanında, **İş analisti**'ni seçin.
9. **Yayınla** öğesini seçin ve sonra **Otomatik takım üret** seçeneğini belirleyin.
10. Görüntülenen ileti kutusunda **Evet**'i seçin.
11. **Kaynak** alanında, değerin **İş analisti 1** olduğunu doğrulayın.
12. **İş analisti 1** kaynağı için aramayı açın ve **Kaynak atamalarını başlat**'ı seçin. Ardından görev için bir çalışan seçin.
13. **Geçici atama** &gt; **Tam kapasite** seçeneğini belirleyin.

    > [!NOTE] 
    > Belirtilen kaynağın artık 2 olduğunu bildiren bir uyarı alamazsınız, çünkü kaynak sayısı 1 olarak kalır.

14. **İş kırılım yapısı** sayfasında, İKY'deki kaynak atamasını doğrulayın ve ardından **Kaydet**'i seçin.

## <a name="resource-fulfillment-for-planned-resources"></a>Planlanan kaynaklar için kaynak karşılama
Proje yöneticisi bir proje için gerekli kaynak rolleri planlayabilir. Kaynak yöneticisi bu planlanan kaynakları **Kaynak karşılama** sayfasında bulunan istekler olarak görür ve gerçek kaynakları atayabilirler.

1. **Tüm projeler** sayfasında, **XYZ Yükseltme Aşama 2** projesini seçin.
2. **Proje**'yi seçin ve daha sonra **Düzenle** seçeneğini işaretleyin.
3. **Proje ekibi ve zamanlama** sekmesinde **Ekle**'yi seçin.
4. **Rolleri ekle** iletişim kutusunda, **Yazılım Geliştirici** rolünü seçin.
5. **Oluştur**'u seçin ve sayfayı kapatın.
6. **Kaynak karşılama** sayfasında, **XYZ Yükseltme Projesi Aşama 2** projesi için **Yazılım geliştirici 1**'i seçin.
7. Bir çalışanı ve ardından **Ata**'yı seçin.
8. **XYZ Yükseltme Projesi Aşama 2** projesi için **Yazılım geliştirici 1** satırının kaldırıldığından emin olun.
9. **Proje ekibi ve zamanlama** sekmesinde, **XYZ Yükseltme Aşama 2** projesi için, önceki adımda seçtiğiniz çalışanın **Yazılım geliştiricisi** olarak eklendiğinden emin olun.

## <a name="requests-for-project-resources"></a>Proje kaynaklarına yönelik istekler
Proje kaynak zamanlamasının işlevselliği yalnızca kaynak yöneticilerinin görevlendirmelere veya projelere yönelik personelli kaynakları dağıtmalarını sağlar. Bu işlevi etkinleştirmek için aşağıdaki görevleri gerçekleştirin veya bunların tamamlandığından emin olun:

- Numara serilerini ayarlayın.
- Proje yönetimi ve muhasebe iş akışlarını ayarlayın.
- Kaynak isteği iş akışlarını etkinleştirin.

Önceki görevler tamamlandıktan sonra, gereksinim duydukça aşağıdaki görevleri gerçekleştirebilirsiniz:

- Geçici ayrılmış personelli bir kaynaktan kaynak isteği oluşturun.
- Kaynak isteklerini izleyin.
- Kaynak isteklerini karşılayın.
- Bir İKY'den bir personelli kaynak isteyin.
- Personelli kaynak için istekte bulunmadan bir projeye kaynak ayırın.

## <a name="monitor-project-teams"></a>Proje ekiplerini izleme
1. **Tüm projeler** sayfasında, **XYZ Yükseltme Aşama 2** projesinin **Proje kodu** bağlantısını seçin.
2. **Proje ekibi ve zamanlama** hızlı sekmesinde, listelenen proje kaynaklarının doğru olduğundan emin olun.
