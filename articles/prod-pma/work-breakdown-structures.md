---
title: İş kırılım yapısına genel bakış
description: iş kırılım yapısı (İKY), proje için yapılacak işin bir açıklamasıdır. Proje takımının iş kompozisyonunu ve her bir bileşenin veya görevin boyut, maliyet ve süresini anlamaya yönelik oluşturulan bir görev hiyerarşisidir.
author: Yowelle
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWorkBreakdownStructure
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23861
ms.assetid: 241a0464-0056-4a69-b468-0afbe2d5f3ae
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9d0cfcc27c69695fc6fe897e798b2831528833e6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086299"
---
# <a name="work-breakdown-structures-overview"></a>İş kırılım yapısına genel bakış

[!include [banner](../includes/banner.md)]

iş kırılım yapısı (İKY), proje için yapılacak işin bir açıklamasıdır. Proje takımının iş kompozisyonunu ve her bir bileşenin veya görevin boyut, maliyet ve süresini anlamaya yönelik oluşturulan bir görev hiyerarşisidir. İKY'nin üç önemli amacı vardır:

-   Görevlerdeki işin kırılımını ve komposizyonunu açıklama.
-   Projedeki işin zamanlanması
-   Her görevin maliyetini tahmin etme.

Bir İKY'deki ayrıntı derecesi, tahminler için gereken doğruluk düzeyine ve bu tahminlere yönelik gerekli izleme düzeyine bağlıdır. Zamanlama ve maliyetle ilgili kaymalara karşı çok az toleransı olan projelerde genellikle daha ayrıntılı bir İKY ve İKY'ye göre işin ilerleyişinin ve maliyetinin titiz şekilde takip edilmesi gerekir. Bu tür bir projeler, inşaat ve mühendislik endüstrilerinde yaygındır. 

Buna karşılık, medya ve reklam, yazılım ve BT altyapısı gibi endüstrilerdeki projeler ise başka türlüdür. Verimlilik görevi yapan kişilerin deneyim ve yetkinliğine göre değişir. Bu nedenle, söz konusu endüstrilerde projenin ayrıntılı ilerleyişini takip etmekten ziyade projenin boyutunu kestirmek için İKY kullanılır. 

İKY hazırlamak genellikle uzun süren ve çok çeşitli insanlardan işbirliği ve bilgi gerektiren yoğun bir işlemdir. Bu konuda, tahmin ve izleme gereksinimlerinizi karşılamak için İKY geliştirmelerini nasıl kullanabileceğiniz açıklanır.

## <a name="prerequisites-for-creating-a-wbs"></a>İKY oluşturmaya ilişkin önkoşullar
İKY oluşturmak için bir çalışma zamanlaması oluşturup çalışma maliyetini tahmin edebilmeniz gerekir.

### <a name="prerequisites-for-creating-a-work-schedule"></a>Çalışma zamanlaması oluşturmak için ön koşullar

İKY özelliklerinin bütün zamanlama yeteneklerini kullanmak için aşağıdaki ayarı gerçekleştirin:

1.  Varsayılan bir takvim ve proje takvimi ayarlayın:
    1.  **Proje yönetimi ve muhasebe** &gt; **Kurulum** &gt; **Proje yönetimi ve muhasebe parametreleri** &gt; **Zamanlama** bölümünü tıklayın. **Varsayılan çalışma takvimi** alanından, varsayılan bir takvim belirtin. Bu, oluşturulan her yeni proje için varsayılan çalışma takvimi olur.
    2.  Belirli bir proje için varsayılan takvimi değiştirebilirsiniz. Projenin ayrıntılar sayfasını tıklayın ve **Proje ekibi ve zamanlama** hızlı sekmesinde, başka bir takvim seçerek **Zamanlama takvimi** alanını güncelleştirin.

2.  Standart çalışma günlerini ve çalışma saatlerini ayarlayın. Projeniz için çalışma takvimi olarak ayarladığınız takvim, aşağıdaki bilgileri belirlemek için İKY'de kullanılacaktır:

-   Çalışma günleri ve tatiller
-   Bir gündeki çalışma saatlerinin sayısı

Bir takvimin çalışma günlerini ve çalışma saatlerini ayarlamak ya da yeni bir takvim oluşturmak için **Kuruluş yönetimi** &gt; **Ortak** &gt; **Takvimler** seçeneğini tıklayın.

### <a name="prerequisites-for-estimating-the-cost-of-work"></a>Çalışma maliyetini tahmin etmek için ön koşullar

İKY'nin tam maliyet tahmini yeteneklerini kullanmak için çalışanlar, iş gücü kategorileri, giderler, masraflar ve malzemeler için maliyet ve satış fiyatlarını ayarlamanız gerekir.

-   İş gücü, gider ve ücret kategorilerinin maliyet ve satış fiyatlarını ayarlamak için **Proje yönetimi ve muhasebe** &gt; **Kurulum** &gt; **Fiyatlar** seçeneklerini tıklayın.
-   Maddelerin maliyet ve satış fiyatlarını ayarlamak için, Ürün bilgileri yönetimi'nde, **Yayımlanan ürün listesi** sayfasındaki her öğe için **Ticari sözleşmeler** sayfasını kullanın.

## <a name="creating-a-wbs"></a>WBS oluşturma
İKY oluşturmak üç etkinliği içerir:

1.  **İş ayrıştırma** : İşin yönetilebilen parçalara veya görevlere göre kırılımlarını oluşturma.
2.  **Çalışma zamanlaması** : görevi gerçekleştirmek için gereken zamanı tahmin etme, görevlerarası bağımlılıkları ayarlama ve görevlerin başlangıç ve bitiş tarihlerini seçme.
3.  **Maliyet tahmini** : her görev için maliyet tahmini yapma.

Aşağıdaki bölümlerde, İKY özelliklerinin bu etkinliklerin her birine nasıl yardımcı olabileceği açıklanmaktadır.

### <a name="work-decomposition"></a>İş ayrıştırma

İşin kırılımını ve ayrıştırma oluşturmak bir İKY oluşturma sürecinde genellikle ilk adımdır. İKY işlevi, iş kırılımı veya ayrıştırma için aşağıdaki temel yapıları destekler. 

**Proje kök görevi** : Proje kök görevi, projeye ait en üst düzey özet görevdir. Diğer tüm proje görevleri, bu özet görev altında oluşturulur. Kök görevin adı daima proje adına ayarlanır. Kök düğümün çalışma, tarihleri ve süresi, kök görevinin altındaki görevlerin değerlerinin özetidir. Kök düğümü özelliklerini değiştiremez veya kök düğümü silemezsiniz.

**Özet veya kapsayıcı görevler** : Özet görev, altında alt görevler veya bileşen görevler bulunan bir görevdir. Bir özet görev herhangi bir iş çalışmasına veya kendi maliyetine sahip değildir. Bunun yerine, bir özet görevin işle ilgili çalışma ve maliyeti, bileşen görevlerin işle ilgili çalışmanın ve maliyetinin toplamıdır. Bileşen görevlere ait en erken başlangıç tarihi özet görevin başlangıç tarihi olarak kullanılır ve bileşen görevlere ait en son bitiş tarihi de bitiş tarihi olarak kullanılır. Bir özet görevin adını değiştirebilir, ancak çalışma, tarih ve süre için zamanlama özelliklerini değiştiremezsiniz. Bir özet görevi silerseniz, tüm bileşen görevleri de silinir. 

**Yaprak düğüm görevleri** : Yaprak düğüm görevi, projedeki en ufak çalışma paketini gösterir. Yaprak düğümü bir tahmini çalışmaya, planlanmış kaynak sayısına ve planlanan başlangıç ve bitiş tarihi ile süreye sahiptir. 

Bir proje için bir çalışma hiyerarşisi veya ayrışım oluşturulmasını etkinleştirmek için aşağıdaki hiyerarşi işlemlerini tamamlayabilirsiniz. 

**Yeni görev** : Oluşturduğunuz yeni görevler kök düğümünün altına otomatik olarak eklenir ve göreve bir İKY numarası otomatik olarak atanır. İKY numarası görevin hiyerarşideki düzeyini temsil eder. Proje kök görev altındaki birinci düzeyde bulunan görevler için 1, 2, 3 gibi bir numaralandırma düzeni kullanılır. Birinci düzeyin altındaki görevler için 1.1, 1.2, 1.3 gibi bir numaralandırma düzeni kullanılır. Bir önceki düzeyin altına eklenen her düzey için, yeni bir noktalı sayı dizisi eklenir. 

Şu anda İKY numaralandırmasını özelleştiremezsiniz. 

**Görevi girintile** : Görevi girintilediğinizde, görev kendisinden önce gelen görevin alt öğesi olur. Yeni alt görevin İKY numarası, yeni üst görevin İKY numarasına göre otomatik olarak yeniden hesaplanır. Üst görev şimdi bir özet veya kapsayıcı görevdir ve bu nedenle bileşen görevlerinin bir toplama durumuna gelir. 

> [!NOTE] 
> Girinti işleminden önce yaprak düğüm olan bir görevin altına görevleri girintilerseniz, yeni oluşturulan bu özet görev kendi tarih, çalışma ve kaynak sayısını kaybeder. Şimdi yeni bileşen görevlere ait değerlerin bir özetini kullanır. 

**Görev girintisini azalt** : Görevin girintisini azaltırsanız, görev artık üst göreve ait bir bileşen görev değildir. Bu görevin İKY numarası, görevin hiyerarşideki yeni düzeyini yansıtacak şekilde otomatik olarak yeniden hesaplanır. Bu görevin ait olduğu önceki üst görevin çalışma, maliyet ve tarihleri bu görevi içermeyecek şekilde yeniden hesaplanır. 

**Yukarı taşı ve aşağı taşı** : **Yukarı taşı** ve **Aşağı taşı** 'yı tıkladığınızda, bir üst görevin hiyerarşisi içinde konumunu değiştirirsiniz. Bir görevin konumu görevin çalışma, maliyet, tarih veya süresini etkilemez. Ancak Bu görevin İKY numarası, görevin hiyerarşideki yeni konumunu yansıtacak şekilde otomatik olarak yeniden hesaplanır.

### <a name="schedule-estimation"></a>Zamanlama tahmini

Zamanlama tahmini genellikle İKY oluşturmanın ikinci adımıdır. En iyi uygulama olarak, görevleri oluşturduktan sonra zamanlama tahminini tamamlamalısınız. Finance uygulamasında **İş kırılım yapısı** sayfasında iki bölüm vardır. Üst bölme, zamanlama tahmini için düşünülmüştür ve alt bölmede maliyet tahmini için kullanabileceğiniz **Tahmin edilen maliyet ve gelirler** sekmesi bulunur. 
**Görev bağımlılıkları** : İKY içinde, görevler arasında öncül ilişkisi oluşturabilirsiniz. Bir göreve öncül görevler atandığında, görev yalnızca tüm öncül görevler tamamlandıktan sonra başlayabilir. Görevin planlanan başlangıç tarihi, otomatik olarak tüm öncüllerinin en geç bitiş tarihine ayarlanır. 

**Görev zamanlama** : Aşağıdaki etmenler yaprak düğüm görevlerinin zamanlamasını belirler:

-   Öncüller
-   Çaba
-   Kaynak sayısı
-   Başlangıç ve bitiş tarihleri

Öncülleri olmayan bir yaprak düğüm görevinin başlangıç tarihi, otomatik olarak projenin zamanlama başlangıç tarihi olarak ayarlanır. Bir yaprak düğüm görevinin süresi her zaman kendi başlangıç ve bitiş tarihleri arasındaki iş günü sayısı olarak hesaplanır. 

*<strong><em>Zamanlama kuralları</em></strong>* Otomatik zamanlama yardımı etkinleştirildiğinde, yaprak düğüm görevlere yönelik görev zamanlaması için aşağıdaki kurallar uygulanır:

-   Görevin başlangıç ve bitiş tarihleri, projenin zamanlama takvimine bağlı olarak her zaman iş günü olmalıdır.
-   Öncüllere sahip bir görevin başlangıç tarihi otomatik olarak öncüllerinin en son bitiş tarihine ayarlanır.
-   Bir görevle ilgili çalışma, otomatik olarak aşağıdaki gibi hesaplanır:

Proje takvimindeki standart iş gününde Kişi sayısı × Süre × Saat sayısı. 

Bazı durumlarda, bu kuralların dışına çıkmak isteyebilirsiniz. Otomatik zamanlamayı, Finance'in yaprak düğüm görevlerin özelliklerini ayarlamasını veya düzeltmesini engellemek için kapatabilirsiniz. Bir göreve herhangi bir zamanlama kuralını ihlal eden bilgi girdiğinizde, bu görevle için bir zamanlama hatası simgesi gösterilir. Zamanlama hatalarının görüntülenmesini istemiyorsanız, özelliği kapatmak **Zamanlama hatalarını göster** seçeneğini tıklayın. 

> [!NOTE] 
> Otomatik zamanlama yardımının açık veya kapalı olmasına bakılmaksızın, bir özet veya kapsayıcı görevin değerleri, bileşen görevlerin değerlerinin toplamı olarak hesaplanmaya devam eder. 

**Zamanlama hatalarını düzeltme** : Otomatik zamanlama yardımı açıldığında, zamanlama hatalarının oluşma ihtimali yoktur. Ancak, otomatik zamanlama yardımını kapattıktan sonra yeniden açarsanız, zamanlama hata simgeleri İKY'de görünebilir. 

**Göreve göre zamanlama hatalarını düzeltme** : Belirli bir görevde zamanlama hatası simgesini çift tıkladığınızda, bir iletişim kutusu o görev için tüm zamanlama hatalarını görüntüler. Görev için hangi zamanlama hatalarının düzeltileceğine karar verebilirsiniz. 

**Tüm zamanlama hatalarının giderilmesi:** Finance'in İKY'deki tüm zamanlama hatalarını düzeltmesini istiyorsanız, Eylem Bölmesi'nde **Tüm zamanlama uyuşmazlıklarını düzelt** 'i tıklayın. 

> [!NOTE] 
> Bu özellik, İKY'de belirgin değişikliklere neden olabilir. Hatalar aşağıdaki sırada düzeltilir:

1.  Tüm görevlerdeki tahmini çalışma, proje takviminde tanımlanan kapasiteye eşit olacak şekilde değiştirilir.
2.  Her görevin başlangıç tarihi, görevin tüm öncül görevleri tamamlandıktan sonra başlayacak şekilde değiştirilir.
3.  Öncül görevlerin başlangıç tarihlerindeki boşlukları kaldırmak için her görevin başlangıç tarihi değiştirilir.

### <a name="cost-estimation"></a>Maliyet tahmini

Bu belgede daha önce belirtildiği gibi, **Iş kırılım yapısı** sayfasının alt bölmesindeki **Tahmini maliyetler ve gelirler** sekmesini kullanarak her bir yaprak düğüm görevinin maliyet tahmini miktarını girersiniz. 

> [!NOTE] 
> Bir özet veya kapsayıcı görevin maliyet tahmini üzerinde değişiklik yapamazsınız. Bir özet görevinin maliyet tahmini, yaprak düğümü görevlerinin maliyet tahmini toplamına eşittir. Her görevin tahmini toplam maliyeti, aşağıdaki hareket türleri için tahmini maliyet tutarlarının toplamı olarak hesaplanır:

-   İşçilik
-   Madde veya malzeme
-   Giderler

**Ücret** hareket türü, ücret tabanlı geliri tahmin etmek için kullanılır. Bu hareket türünün maliyet bileşeni yoktur ve bu nedenle maliyet tahmini yapıldığında dikkate alınmaz. 

Bir **Mahsup** hareket türü, sözleşme yapılan satış değerlerini sabit değerli proje türünde kaydetmek için kullanılır. Bu hareket türü de maliyet tahmini olduğunda da dikkate edilmez. 

Her göreve ait iş gücü, malzeme ve giderlerin maliyetlerini tahmin ettiğinizde, tahmini maliyete bir proje kategorisi atamanız gerekir. 

**İş gücü maliyetlerini tahmin etme** : Her yaprak düğüm görevi için saat olarak işle ilgili çalışmayı ve varsayılan kategoriyi atarsınız. Bu nedenle, bir görev için bir zamanlama ayarladığınızda, göreve yönelik iş gücü maliyet tahmini otomatik olarak iş gücüne ait varsayılan kategoriye eklenir. Bu maliyet tahmini, görevin **Satır ayrıntıları** kılavuzundaki **Tahmini maliyetler ve gelir** sekmesinde görüntülenir. Daha fazla iş gücü maliyet tahmini gerektiğinde, bu sekmeden ekleyebilirsiniz. İş gücü maliyeti tahminindeki saatleri arttırırsanız veya azaltırsanız, görevin zamanlaması otomatik olarak yeniden hesaplanır. 

**Gider ve malzeme maliyetleri tahmin etme** : **Tahmini maliyetler ve gelir** sekmesi, tahmin yapılması gerektiğinde, bir görev için gider ve malzeme maliyetlerini tahmin etmenize olanak sağlar. 

Her iş gücü ve gider tahmini satırının maliyet ve satış fiyatı **Proje yönetimi ve muhasebe** &gt; **Kurulum** &gt; **Fiyatlandırma** bölümündeki fiyatlandırma tablolarındaki her bir kategori için tanımlanan kuruluma dayanır. Maddeler için maliyet ve satış fiyatları varsayılan olarak Ürün bilgileri yönetimi'nde, **Yayımlanan ürün listesi** sayfasındaki madde veya ticari sözleşmelerden eklenir.

## <a name="tracking-progress-on-the-wbs"></a>İKY'de ilerlemeyi izleme
Bazı endüstriler, bir projenin ilerleyişini en alt düzeyde İKY üzerinden izlerken diğerleri İKY üzerinde daha yüksek düzeyde ilerlemeyi izler. Bu bölümde, proje gereksinimleriniz için İKY izlemeyi nasıl kullanabileceğiniz açıklanmaktadır. 

Finance'de, bir projeye ait İKY'nin üç görünümü vardır: planlama görünümü, çalışma izleme görünümü ve maliyet izleme görünümü.

### <a name="planning-view"></a>Planlama görünümü

Planlama görünümü, zamanlamanın planlanan veya temel tahminini ve maliyet bilgilerini görüntüler. Bir proje İKY'si için sürüm ve taban çizgisini izlemeye yönelik bir özellik olmasa da, bu görünümdeki değerler temel sürümü temsil etmek üzere tasarlanmıştır. Bu konudaki Zamanlama tahmini ve Maliyet tahmini bölümlerinde bu görünüm ve İKY oluşturmak için nasıl kullanılacağını açıklanır.

### <a name="effort-tracking-view"></a>Çalışma izleme görünümü

Çalışma izleme görünümü İKY'deki görevlerin ilerlemesinin izlenmesini sağlar. Bu, görevin birikmiş gerçek çalışma saatlerini planlanan çalışma saatleri ile karşılaştırır. Aşağıdaki formüller, Çalışma izleme görünümündeki değerleri sağlar:

-   İlerleme yüzdesi = Bugüne kadar harcanan gerçek çalışma süresi ÷ Görev için planlanan çalışma süresi
-   Kalan çalışma (Tahmini tamamlanma zamanı olarak da bilinir \[ETC\]) = Planlanan çalışma – Bugüne kadarki gerçek çalışma
-   Tahmini tamamlanma (EAC) = Kalan çalışma süresi + Bugüne kadar harcanan gerçek çalışma süresi
-   Öngörülen çalışma farkı = Planlanan çalışma süresi – EAC

Çalışma izleme görünümü, görevin planlanan çabaya göre daha az veya daha fazla EAC değerine sahip olmasına bağlı olarak, görevle ilgili çalışma farkının bir projeksiyonunu görüntüler:

-   EAC planlanan çalışma süresinden daha fazlaysa görevin başlangıçta planlanandan daha fazla zaman alacağı ve zamanlamanın gerisine düşeceği öngörülmektedir.
-   EAC planlanan çalışma süresinden daha azsa görevin başlangıçta planlanandan daha az zaman alacağı ve zamanlamanın önünde gideceği öngörülmektedir.

**Proje yöneticisinin çalışmayı yeniden tasarlaması** : Projenin ilerlemesini takip eden bir proje yöneticisi veya başka bir kişi görevle ilgili başlangıçtaki tahminleri gözden geçirmek zorunda kalır. Bu görev, çeşitli nedenlerle beklenenden daha hızlı veya daha yavaş ilerlemiş olabilir. Örneğin, kapsam azaltıldı veya çalışanlar başlangıçta planlanandan daha az deneyimlere sahiptir. Projeksiyonlar, projenin mevcut durumuna bağlı olarak proje yöneticisinin tahminlerle ilgili algısıdır. Genellikle taban sayılarınızı değiştirmemelisiniz, çünkü proje tabanı, projedeki tüm paydaşların hep birlikte anlaştığı projenin zamanlama ve maliyet tahminleri ile ilgili yayımlanmış belgeleri temsil eder. 

Proje yöneticilerinin görevlerdeki çalışmayı değiştirmesinin iki yolu vardır:

-   Görevdeki kalan gerçek çalışmayı güncelleştirmek için otomatik olarak ayarlanan kalan çalışmayı değiştirin.
-   Görevdeki gerçek ilerlemeyi güncelleştirmek için otomatik olarak ayarlanan ilerleme yüzdesini değiştirin.

Bu yaklaşımların ikisi de görevin ETC, EAC ve ilerleme durumu yüzdesinin yeniden hesaplanmasına ve görevde öngörülen çalışma farkına neden olur. EAC, ETC ve özet görevlerindeki ilerleme durumu yüzdesi de yeniden hesaplanır ve çalışma farkı projeksiyonu güncelleştirilir. 

**Özet görevlerde değiştirilen çalışma** : Özet veya kapsayıcı görevleri üzerindeki çalışmayı değiştirebilirsiniz. Kullanıcının, özet görevlerdeki kalan çalışma değerini veya ilerleme durumu yüzdesini kullanarak bu değerleri değiştirmesinden bağımsız olarak hesaplamalar otomatik olarak aşağıdaki sırada yapılır:

1.  Görevdeki EAC, ETC. ve ilerleme durumu yüzdesi hesaplanır.
2.  Yeni EAC alt görevlere, başlangıçtaki EAC'nin görevde sahip olduğu oranda dağıtılır.
3.  Her yaprak düğüm görevindeki yeni EAC hesaplanır.
4.  Kalan çalışma ve ilerleme yüzdesi, yeni EAC değerine göre, etkilenen tüm alt görevler için yeniden hesaplanır. Görevlerin çalışma farkı yeniden hesaplanır.
5.  Özet görevlerin EAC değeri de yaprak düğümlerinden yeniden hesaplanır.

Çalışma izleme görünümünde, İKY'nizi izlemek ve korumak istediğiniz düzeyi ayarlamak için **Düzeye genişlet** seçeneğine tıklayın. Her açtığınızda İKY, Çalışma izleme görünümünde o düzeye otomatik olarak genişletilir.

### <a name="cost-tracking-view"></a>Maliyet izleme görünümü

Maliyet izleme görünümü bir görev için maliyet tüketiminin izlenmesini görüntüler. Bu görünümde, bir görev için harcanan gerçek maliyet, görevin planlanan maliyetiyle karşılaştırılır. Aşağıdaki formüller, Maliyet izleme görünümündeki değerleri sağlar:

-   Tüketilen maliyetin yüzdesi = Bugüne kadarki gerçek maliyet ÷ Görev için planlanan maliyet
-   Tamamlamak için gereken maliyet (CTC) = Planlanan maliyet – Bugüne kadarki gerçek maliyet
-   Tahmini tamamlanma (EAC) = CTC + bugüne kadarki gerçek maliyet
-   Öngörülen maliyet farkı = Planlanan maliyet – EAC

Maliyet izleme görünümü, görevin planlanan maliyete göre daha az veya daha fazla EAC değerine sahip olmasına bağlı olarak, görevle ilgili maliyet farkının bir projeksiyonunu görüntüler:

-   EAC planlanan maliyetten daha fazlaysa görevin başlangıçta planlanandan daha fazla para kullanacağı ve bütçeyi aşacağı öngörülmektedir.
-   EAC planlanan maliyetten daha az ise görevin başlangıçta planlanandan daha az para kullanacağı ve bütçenin altında kalacağı öngörülmektedir.

**Proje yöneticisinin maliyeti yeniden tasarlaması** : Proje yöneticisi bir görevde başlangıçtaki maliyet tahminini düzeltmek için CTC'yi kullanmalıdır. Proje yöneticisi CTC değerini görevi gerçekleştirmek için gereken maliyete göre değiştirebilir. CTC değerini değiştirirseniz, görevin CTC, EAC ve tüketilen maliyet yüzdesi ve bir görevdeki tahmini maliyet farkı yeniden hesaplanır. EAC, ETC ve özet görevlerindeki tüketilen maliyet yüzdesi de yeniden hesaplanır ve maliyet farkı projeksiyonu güncelleştirilir. 

> [!NOTE] 
> Çalışma izleme görünümündeki bir İKY görevinin çalışmalarını düzelttiğinizde, görevin CTC, EAC, tüketilen maliyet yüzdesi ve tahmini maliyet farkı Maliyet izleme görünümünde yeniden hesaplanır. Ancak hareket tipine göre maliyet (iş gücü, malzeme veya masraf) veya proje kategorisi düzeltilmediğinden, maliyet düzeltmeleri Çalışma izleme görünümündeki değerleri etkilemez. 

**Özet görevlerde maliyetler için projeksiyon düzeltmesi** : Özet görevlerdeki maliyetleri gözden geçirebilir ve hesaplamalar otomatik olarak aşağıdaki sırada yapılır:

1.  Görev üzerinde tüketilen EAC, CTC ve maliyetin yüzdesi yeniden hesaplanır.
2.  Yeni EAC alt görevlere, özgün EAC'nin görevlerde sahip olduğu oranda dağıtılır.
3.  Her görev için yeni EAC hesaplanır.
4.  CTS ve tüketilen maliyet yüzde oranı, EAC değerine göre, etkilenen alt görevler için yeniden hesaplanır. Görevlerin maliyet farkı yeniden hesaplanır.
5.  Bu değişiklik temel alınarak tüm özet görevleri için EAC yeniden hesaplanır.

Maliyet izleme görünümünde, İKY'nizi izlemek ve korumak istediğiniz düzeyi ayarlamak için **Düzeye genişlet** seçeneğine tıklayın. Her açtığınızda İKY, Maliyet izleme görünümünde o düzeye otomatik olarak genişletilir.

### <a name="earned-value-management"></a>Kazanılan değer yönetimi

Projenin ilerleme durumunu izlemek için kazanılan değer yöntemini (EVM) kullanabilirsiniz. Kazanılan değer ölçümlerini proje yöneticisinin Rol Merkezi'nde görüntüleyebilirsiniz. Kazanılan değer grafik bileşeni, planlanan değer ve gerçek maliyetin zaman aşamalı değerlerini gösterir. Geçerli tarihte kazanılan değer bir nokta olarak gösterilir. Kazanılan değer için zaman aşamalı veriler şu anda kullanılamıyor. 

Kazanılan değer grafiğindeki zaman aşaması, haftaya veya aya göre görüntülenir. Bu bölümde "EVM'nin üç ayağı: planlanan değer, kazanılan değer ve gerçek maliyet" açıklanmaktadır. 

**Planlanan değer** : EVM teorisinde, planlanan değer grafiğinin proje ekibinin proje üzerinde değer kazanması için planlanan oranı temsil ettiği belirtilir. 

Finance planlanan değere çizim yaparken 0:100 kazanç kuralını kullanır. Bu kuralın altında, görevin değeri bitiş tarihi itibariyle göreve nakledilir. Görev yüzde 100 tamamlanıncaya kadar hiçbir değer nakledilmez. 

Proje yönetimi ve muhasebe modülünde, yaprak düğümlerin bitiş tarihini ve planlanan maliyeti girin. Planlanan değer grafiği haftalık olarak görüntülendiğinde, planlanan değer, proje süresince tüm yaprak düğümü görevleri için haftaya göre özetlenir. 

**Kazanılan değer** : EVM teorisinde, kazanılan değer grafiğinin proje ekibinin proje üzerinde gerçekten kazandığı değer oranını temsil ettiği belirtilir. 

Finance kazanılan değere çizim yaparken 0:100 kazanç kuralını kullanır. Bu kuralın altında, görevin değeri bitiş tarihi itibariyle göreve nakledilir. Görev yüzde 100 tamamlanıncaya kadar hiçbir değer nakledilmez. 

Kazanılan değer hesaplanırken, her görevin ilerleme durumu yüzde olarak değerlendirilir. 0:100 kazanç kuralı altında, belirli bir dönemin sonunda kazanılan değer hesaplaması için yalnızca söz konusu dönemde tamamlanan görevler dikkate alınır. Projedeki kazanılan değer, grafik oluşturulduğunda tamamlanan tüm görevler için hesaplanır. 

> [!NOTE] 
> Şu anda, İKY izleme sisteminde geçmişteki ilerleme yüzdelerini her görevde saklamak için veri yapıları yoktur. Bu nedenle, kazanılan değer yalnızca küpün işlendiği saat olarak rapor edilebilir. Rol Merkezi'nde gösterilen kazanılan değer verilerini güncelleştirmek için küpü düzenli olarak işleyin. 

**Gerçek maliyet** : EVM teorisinde gerçek maliyet grafiğinin, projede harcanan para oranını temsil ettiği belirtilir. 

Bir projeye nakledilen hareketler, gerçek maliyet satırını çizmek için kullanılır. Maliyetler tarihe göre özetlenir. Bu veriler daha sonra kazanılan değer grafiğindeki gerçek maliyetleri haftaya veya aya göre grafik olarak yansıtmak için kullanılır.

### <a name="how-to-use-the-concepts-of-planned-value-earned-value-and-actual-cost"></a>Planlanan değer, kazanılan değer ve gerçek maliyet kavramlarını kullanma

**Zamanlama farkı** : Planlama sırasında, bir zaman cetveli üzerinde çalışma için bir tahmin oluşturursunuz. Bu nedenle, planlanan değer proje planlayıcılarının projede işin tamamlanacağını düşündüğü orandır. Bir proje başladıktan sonra, çalışma tamamlanır ve proje değer kazanır. Planlanan değeri kazanılmış değerle karşılaştırarak, bir projedeki çalışmanın nasıl ilerlediğini görüntüleyebilirsiniz. Bu karşılaştırmanın sonucuna, zamanlama farkı denilir. 

Bir döneme ait planlanan değer kazanılan değerden büyükse, bir projede yapılan çalışma miktarı planlanandan daha az olur. Bu nedenle proje zamanlamanın gerisindedir. Planlanan değer ve kazanılan değer parasal terimlerle ifade edildiğinden, projedeki öteleme süresi de parasal değer olarak verilir. 

Bir döneme ait planlanan değer kazanılan değerden azsa, bir projede yapılan çalışma miktarı planlanandan daha fazla olur. Bu nedenle proje zamanlamanın önündedir. Önde gidilen bu süre de parasal değer olarak verilir.

**Maliyet farkı** : Kazanılan değer, çarpan olarak maliyet fiyatını kullandığından, kazanılan değer bir projede yapılacak çalışmanın maliyetini gösterir. Proje ilerledikçe hareket günlüğü o proje için gerçekte harcanan paraların kaydını sağlar. Kazanılan değeri gerçek maliyetle karşılaştırarak, kazanılan değere göre harcanan para tutarını görüntüleyebilirsiniz. Bu karşılaştırmanın sonucuna, maliyet farkı denilir. 

Bir dönem için harcanan gerçek maliyet kazanılan değerden daha büyükse, kazanılan paradan daha fazla para harcanmış demektir. Bu nedenle, proje bütçenin üzerinde olur. 

Bir dönem için harcanan gerçek maliyet kazanılan değerden daha az ise kazanılan para harcanan paradan daha çok demektir. Bu nedenle, proje bütçenin altında olur.

## <a name="wbs-templates"></a>İKY şablonları
Projeler için standart şablonlar oluşturmak üzere İKY şablonları işlevselliğini kullanabilirsiniz. Şirketinizin önerdiği projelerde çok fazla yinelenebilir iş varsa, İKY şablonu oluşturmayı düşünmelisiniz. 

Var olan bir projenin İKY'den bir İKY şablonu oluşturabilirsiniz, böylece o projeyi planlarken kazanılan bilgi ve en iyi uygulamalar gelecekte benzer projelerde yeniden kullanılabilir. Ancak bazı durumlarda, İKY'nin tamamını şablon olarak kaydetmek mantıklı olmayabilir. Bu nedenle, bir proje için İKY bölümlerinden bir şablon da oluşturabilirsiniz.

### <a name="saving-a-projects-wbs-as-a-template"></a>Projenin İKY şablonunu şablon olarak kaydetme

Bir şablon oluşturduktan sonra, onu kök düğümünün altındaki yeni bir projenin İYK'sinin içine veya proje İKY'sinde herhangi bir görevin altına alabilirsiniz.

### <a name="importing-a-wbs-template-into-a-projects-wbs"></a>İKY şablonunu bir projenin İKY'sinin içine alma

Görevleri içe aktardığınızda, şablondaki görevler, altında alındıkları görevin başlangıç tarihine göre düzenlenir. İçe alma işlemi sırasında, şablon görevlerdeki öncül İlişkiler alınan görevlerin başlangıç tarihlerini hesaplamak için kullanılır. Hedef projenin standart çalışma takvimi, içe aktarılan görevlerin bitiş tarihlerini hesaplamak için uygulanır; böylece, geçerli projenin iş takviminde tanımlanan çalışma günleri ve standart çalışma saatleri korunur. 

Tahmin satırlarındaki maliyet miktarları ve satış fiyatları, proje veya proje sözleşmesine özgü fiyatların geçerli tarihlere sahip olduğundan emin olmak için uygulanır.

### <a name="differences-between-a-projects-wbs-and-a-wbs-template"></a>Projenin İKY'si ve İKY şablonu arasındaki farklar

-   İKY şablonlarındaki görevlerin başlangıç tarihleri ve bitiş tarihleri yoktur.

Çalışılan ve çalışılmayan günler İKY şablonları için ayarlanmazlar.

-   İKY şablonları her zaman tüm projeler için varsayılan takvim olarak ayarlanmış zamanlama takvimini kullanır.

Varsayılan zamanlama takvimi yalnızca standart bir çalışma gününde saatleri bulmak için kullanılır.

-   Öncül ilişkiler İKY şablonuna kopyalanmaz.

İKY şablonlarının tarihleri olmadığından, öncülünün bitiş tarihini temel alan başlangıç tarihi mantığı gerekmez.

-   Bir İKY şablonunda görev oluşturulduğunda iş gücü maliyet tahmini satırı otomatik olarak oluşturulur. Satış fiyatı ve maliyet tutarı seçili çalışandan kopyalanır.

Gider ve madde maliyetleri, projenin İKY'sinde olduğu gibi, el ile de oluşturulabilir.

-   Aşağıdaki formülden sapmalar olduğunda zamanlama hataları görüntülenir:

Çalışma = Kaynak sayısı × Süre × Standart çalışma gününde saat sayısı 

**Tüm zamanlama hatalarını düzelt** öğesini tıklayarak bütün zamanlama hatalarını bir defada düzeltebilirsiniz. 

Başka bir seçenek olarak, zamanlama hatalarını her görevdeki uyarı simgesini tıklayarak da tek tek düzeltebilirsiniz.





[!INCLUDE[footer-include](../includes/footer-banner.md)]