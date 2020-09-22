---
title: Project Service Automation sürüm 3'teki yenilikler veya değişiklikler
description: Bu konu Project Service Automation sürüm 3'teki yenilikler veya değişiklikler hakkında bilgi sağlar.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x
author: JohnPBurrows
ms.assetid: 8a4f3c98-063a-4db8-8645-06b0fbe1b5db
ms.author: john.burrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: ad0ef8cdac2990716baff27f86a5473bc0b031fe
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756638"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3"></a>Project Service Automation sürüm 3'teki yenilikler veya değişiklikler
[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Bu konu, Project Service Automation'da sürüm 2 veya sürüm 1 ile sürüm 3 arasında kullanıcı arabirimi (UI), işlevsellik ve terminoloji değişiklikleri hakkında bilgi sağlar.

## <a name="project-scheduling"></a>Proje zamanlaması
Önceki sürümlerde İş Kırılım Yapısı (İKY) olarak bilinen proje zamanlaması Zamanlama olarak yeniden adlandırılmıştır ve **Zamanlama** sekmesi tıklatılarak erişilir. 

![Proje Zamanlaması](media/psa-schedule-01.png)

Zamanlama artık modern ve erişilebilir etkileşim için yeni bir yüzeye sahiptir. Ancak temeldeki Project Service Automation zamanlama altyapısı değişmemiştir. Zamanlama ızgarasının şeridinde bulunan denetim düğmeleri, Project Service Automation'ın önceki sürümüne benzer şekilde zamanlamayla etkileşim kurmanıza olanak tanır. Zamanlamada yapılan ek değişiklikler şunları içerir:

- **Gantt grafiği** - Gantt grafiği artık mevcut değildir. Yeni bir Gannt görselleştirmesi gelecekteki bir güncelleştirmede yeniden eklenecektir.
- **Sütun başlıkları** - Sütun başlığının yanındaki aşağı göstergesini tıklatarak ızgaradaki sütun başlıklarını gizleyebilirsiniz. 
- **Sütunlar** - **Sütun ekle** öğesini tıklatarak sütunları gizleyebilirsiniz. 
- **İşlem kategorisi** - **İşlem kategorisi** araması zamanlama ızgarasına eklenmiştir ve varsayılan olarak gösterilir. 
 
## <a name="project-templates"></a>Proje şablonları
Proje şablonu işlevlerinde aşağıdaki değişiklikler yapıldı.

### <a name="create-a-project-template"></a>Bir proje şablonu oluştur 
Sürüm 3'te Project Service Automation'ın önceki sürümlerine benzer şekilde bir proje şablonu oluşturabilirsiniz. Şablon yalnızca zamanlamayı ve zamanlama yalnızca atamaları içerir ancak bunlar zorunlu değildir. Zamanlamada atamalar varsa bunlar yalnızca genel kaynaklara yönelik olabilir. Genel kaynaklar için kaynak gereksinimleri oluşturabilirsiniz ancak bunlar şablondaki gerçek kaynaklarla ayrılamaz. Şablonda bir takıma gerçek bir kaynak ayıramazsınız. 

### <a name="create-a-template-from-an-existing-template"></a>Varolan şablondan yeni bir şablon oluşturma
Project Service Automation sürüm 3'te var olan şablondan yeni bir proje şablonu oluşturduğunuzda aşağıdakiler gerçekleşir: 

- Kaynak projenin zamanlaması şablona kopyalanır. 
- Genel kaynaklar takıma kopyalanır ve tüm genel kaynak atamaları üzerine kopyalanır. Genel kaynak gereksinimleri üzerine kopyalanmaz. 

### <a name="create-a-template-from-an-existing-project"></a>Varolan projeden bir şablon oluşturma
Varolan projeden yeni bir proje şablonu oluşturduğunuzda aşağıdakiler gerçekleşir: 

- Kaynak projenin zamanlaması şablona kopyalanır. 
- Genel kaynaklar takıma kopyalanır ve tüm genel kaynak atamaları korunur. Genel kaynak gereksinimleri üzerine kopyalanmaz.    
- Atanmış veya atanmamış adlandırılan kaynaklar takımdan kaldırılır ve genel kaynaklarla değiştirilir.
- Varsa, müşteri bilgileri kaldırılır. 
- Varsa, teklifler ve sözleşmelerdeki başvurular kaldırılır. 

### <a name="create-a-project-from-a-template"></a>Şablondan bir proje oluşturun
Project Service Automation sürüm 3'te bir şablondan yeni bir proje oluşturduğunuzda aşağıdakiler gerçekleşir:

- Zamanlama, takım ve atamalar yeni projeye kopyalanır.   
- Başlangıç tarihi, kopyalama tarihi veya kullanıcı tarafından seçilen tarihtir.   
- Şablonda kaynak gereksinimleri olan genel takım üyeleri için gereksinimler otomatik olarak kopyalanmaz veya oluşturulmaz. Bunları oluşturmanız gerekir. 

## <a name="copy-a-project"></a>Proje kopyalama
Project Service Automation sürüm 3'te bir projeyi kopyaladığınızda aşağıdakiler gerçekleşir: 

- Tahmini başlangıç tarihi kopyalanır ancak değiştirilebilir.  
- Proje zamanlaması ve görevleri kopyalanır. 
- Genel kaynaklar ve bunların atamaları kopyalanır. Genel kaynakların kaynak gereksinimleri üzerine kopyalanmaz. Bunları yeniden oluşturmanız gerekir. 
- Gerçek kaynaklar ve bunların atamaları kopyalanmaz. Bunun yerine, genel kaynaklarla değiştirilir. 
- Gerçek değerler yeni projeye kopyalanmaz. 

## <a name="move-a-scheduled-project"></a>Zamanlanmış bir projeyi taşıma
Varolan projenin zamanlamasını ileriye doğru taşıdığınızda aşağıdakiler gerçekleşir: 

- Görev tarihleri, taşıma dönemine karşılık gelecek şekilde otomatik olarak taşınır. 
- Atanan genel kaynaklar atanmış olarak kalır.   
- Bunlar proje taşınmadan önce oluşturulursa genel kaynak gereksinimleri aynı kalır ve otomatik olarak yeniden oluşturulmaz. Görevin taşınması nedeniyle yeni atamaları yansıtmak için bunları yeniden oluşturmanız gerekir. 
- Gerçek kaynaklardaki atamalar, görev tarihinin taşınmasına karşılık gelecek şekilde değiştirilir. Gerçek kaynaklardaki ayırma işlemleri değişmez. Mutabakat görünümünü kullanarak ayırmaları değiştirmeniz gerekir. 
- Ayırmaları olan ancak atamaları olmayan takım kaynakları değişmez. 
- Gerçek değerler taşınmaz. 

## <a name="estimates"></a>Tahminler
Tahminler, **Kaynak atama** ve **Tahminler** olarak iki sekmeye bölünmüştür. **Kaynak atama** sekmesi, çalışma tahminlerini içerir ve görevlerin kaynak atamalarını zaman aşamalı görünümde gösterir. Tahminleri oluşturulan zamanlama altyapısını temel alarak düzenleyebilirsiniz.

![Çalışma tahminlerini ve görevlerin kaynak atamalarını gösteren kaynak atamaları sekmesi](media/resource-assignments-tab-02.png)

**Tahminler** sekmesi kaynak atamalarının maliyet ve satış tutarlarını gösterir. Tutarlar salt okunur. Maliyetlendirme ve satış fiyatlandırması artık zamanlamadaki takım üyesi atamalarından yönlendirilmektedir. Başka bir deyişle ataması olmayan bir göreviniz varsa görev, atanmamış demetin altında gösterilir. Bu ayrıca projeyle ilişkili bir müşteriniz veya sözleşmeniz/teklifiniz varsa varsayılan fiyatlandırma boyutu olan **rol** olmadan hiçbir tahmini maliyet veya satışın olmayacağı anlamına gelir. 

![Maliyet ve satış tutarlarını gösteren tahminler sekmesi](media/estimates-tab-03.png)
  
Kategori, zamanlama görünümündeki görevlerde de desteklenir. Tahminlerin zaman aşamalı görünümde kategoriye göre gruplandırılması, özellikle projenizde gider tahminleriniz de varsa daha iyi bir deneyim sunar. Gider tahminleri ayrı bir sekmede bir ızgara kullanılarak girilir. 

Gider tahminleri, **Gider tahminleri** sekmesindeki ızgaraya girilebilir. 

![Gider tahminleri ızgarasını gösteren gider tahminleri sekmesi](media/expense-estimates-tab-04.png)

## <a name="resource-management"></a>Kaynak yönetimi
Project Service Automation sürüm 3'te, yeni Birleşik İstemci Arabirimi ve ayırmalarla atamalar arasındaki ilişkide yapılan değişikliklerle genel veya gerçek kaynaklara sahip bir proje için kadro oluşturma sürüm 2 ve sürüm 1'e göre önemli ölçüde değişmiştir. Ancak hem **gerçek** hem de **genel** ayrılabilir kaynak kavramları, takım üyeleri, gereksinimler, atamalar ve ayırmalarda olduğu gibi aynı kalır.   

![Kaynak seçiciyi kullanma](media/resource-management-05.png)

### <a name="assign-a-real-bookable-resource"></a>Gerçek bir ayrılabilir kaynağı atama 
Project Service Automation sürüm 3'te, ayırma ve görev atamaları, Project Service Automation'ın önceki sürümlerindeki kadar sıkı bir şekilde iç içe geçmemiştir. Takım ızgarasını pazar içinde olduğu gibi **gerçek** bir takım üyesini ayırmak için kullanabilirsiniz.

Zamanlamadaki kaynak seçiciyi kullanarak takım görünümünde oluşturulan takım üyesini seçebilir ve bunları görevlere atayabilirsiniz. Ayırmaları geçse bile bunlara görev atamaya devam edebilirsiniz. Ayırmalarında ve atamalarında farklılıklar bulunan takım üyelerini mutabık kılmak için **Mutabakat** sekmesini kullanın.

Kaynak seçici, projenin takım üyelerini gösterir. Kaynak seçiciyi proje takımının parçası olmayan diğer ayrılabilir kaynakları aramak ve görüntülemek için de kullanabilirsiniz. Bunları bir göreve atayarak proje takımının parçası haline getirebilirsiniz. Bunları **Zamanlama panosu** veya **Mutabakat** sekmesini kullanarak ayırmanız gerekir.

### <a name="assign-a-generic-bookable-resource-on-a-task-and-project-team-and-then-fulfill-with-a-real-resource-via-schedule-board"></a>Görevde ve proje takımında genel bir ayrılabilir kaynak atayın ve ardından bunu Zamanlama panosunu kullanarak gerçek bir kaynakla gerçekleştirin 
Project Service Automation sürüm 3'te, takım oluşturma işlevi genel kaynaklar için kullanılmaz. Bunun yerine zamanlamanın kaynak hücresine genel kaynağın konum adını yazarak zamanlamadan bir genel kaynak oluşturabilir ve doğrudan atayabilirsiniz. Alternatif olarak, hücrede kaynak simgesini seçebilir ve ardından kaynak seçiciyi kullanarak oluşturmak istediğiniz genel kaynağın adını yazabilirsiniz. Bu işlem, genel kaynak takım üyesinin rolünü ve kuruluş birimini ayarlamanıza olanak tanıyan bir hızlı oluşturma panelini açar. Kaynak oluşturulduktan sonra göreve atanır ve bu genel kaynağı zamanlamadaki diğer görevlere atamaya devam edebilirsiniz.    
 
Kaynağı uygun tüm görevlere atadıktan sonra bir kaynak gereksinimi oluşturabilir ve ardından bunu **Zamanlama panosu** ile doğrudan ayırarak veya bir kaynak isteği göndererek gerçekleştirebilirsiniz. Doğrudan takım üyesi ızgarasına da genel kaynaklar ekleyebilirsiniz. 

Genel kaynaklar, kaynak gereksinimleri olmadan ve kaynak gereksinimi oluşturulana kadar projenin başlangıç/bitiş tarihleriyle proje takımına eklenir. Gereksinim oluşturmak için genel kaynağı seçin ve **Oluştur** öğesini tıklatın. Gereksinim bağlantısı şimdi görüntülenir ve gerekli saatler atanan saatlerle doldurulur. Bağlantıyı tıklatarak gereksinimi açabilir ve güncelleştirebilirsiniz.
  
Ayırma işlemi tamamlandığında ve bir adlandırılmış kaynak tarafından tamamen karşılandığında genel kaynak adlandırılmış kaynakla değiştirilir ve zamanlamadaki atama adlandırılmış kaynakla güncelleştirilir. 

Gereksinimler için önerilen kaynaklar artık ayrı bir bölüm yerine bir sekmede depolanır.

### <a name="multiple-named-resources-fulfilling-a-generic-resource"></a>Bir genel kaynağı karşılayan birden çok adlandırılmış kaynak
Bir gereksinim birden fazla kaynakla karşılandığında genel kaynak takımda kalır ve göreve atanır. Ayrılan adlandırılmış takım üyeleri, konumun parçası olarak atanmaz. Proje yöneticisi, işi gerektiği gibi gerçek kaynaklara atayabilir.  **Mutabakat** görünümü, birden çok görev ataması için birden çok kaynak arasındaki ayırmaların dökümünü sağlar. Gereksinim oluşturan bir görev paketinizin olduğu ve proje yöneticisinin bunu atamak isteme amacının tahmin edilmesinin gerektiği gibi daha karmaşık senaryolar nedeniyle bu otomatik olarak gerçekleştirilmez. Sistem amacı anlayamadığından varsayımlar amaçlanandan farklı olabilir ve yanlış veya öngörülemeyen sonuçlara neden olabilir. Öngörülebilir sonuç, proje yöneticisi **Mutabakat** görünümünü kullanarak kaynakları bilerek atayana kadar genel kaynağın atanmış kalmasıdır.

### <a name="reconciliation"></a>Mutabakat
**Mutabakat** sekmesi, her proje takımı üyesinin ayırmalarını ve tüm atamalarını gösterir. Görünüm, hücrelerde aylardan günlere kadar olan zaman noktalarını temsil edebilen saatleri gösterir. Bu görünüm, proje yöneticilerinin proje takımlarının takım üyesi ayırmalarını ve bunların atamalarını mutabık kılmasına olanak tanır. Bu, ayırmalar ve görev atamaları kesin bir şekilde eşleştirilmediğinden bir proje planlanırken daha fazla esneklik sağlamaya yardımcı olur. 

![Proje takımı üyelerinin ayırmalarını ve tüm atamalarını gösteren mutabakat sekmesi](media/resource-reconciliation-tab-06.png)

Bu görünüm her kaynak için bir takım üyesinin ayırmaları ile bunların görev atamalarının toplu değeri arasındaki farkı ele alır ve bir projedeki ayırmalar ve atamalarla ilgili oluşabilecek aşağıdaki iki farkı gösterir: 

- **Ayırma eksikliği** - Ayırma eksikliği bir kaynakta ayırmadan daha fazla atama varsa oluşur. Bu kapasite ayrılmadığından bir proje yöneticisi, eksikliği gidermek için kaynağın ayırmalarını uzatarak bu sorunu düzeltebilir. 
- **Aşırı ayırmalar** - Aşırı ayırmalar bir kaynak projeye ayrıldığında ancak görevlere atanmadığında oluşur.  Bu, örneğin, kaynak görev atamasından önce ayrılmışsa kabul edilebilir bir oluşum olabilir. Ancak diğer durumlarda kaynak atanmak üzere planlanmamış olabilir ve PM, kapasitenin başka bir projede kullanılmasını sağlamak için kaynağın ayırmalarını iptal etmeyi düşünmelidir. 

Ayırmaların bulunmadığı (ayırma eksikliği) bir kaynak için görev atamalarınız varsa toplam ayırma eksikliğini seçerek **Ayırmayı uzat** öğesini tıklatabilirsiniz. Buradan, kaynak eksikliğini ve kullanılabilirliğini ele almak için gerekli olan ayırmayı görüntüleyebilirsiniz. 
 
## <a name="time-and-expense"></a>Zaman ve gider
Bu bölüm, Project Service Automation sürüm 3'te zaman, gider ve onay değişiklikleri hakkında bilgi sağlar. Dynamics 365 Project Service Automation çözümünün parçası olarak **Zaman girişi** özelliği Birleşik Arabirim çerçevesinden yaralanmak için yenilenmiştir. Bu, tutarlı, tek tip bir kullanıcı arabirimi sunulmasını sağlar ve tüm ekran boyutlarında veya cihazlarda en iyi görüntüleme için dinamik tasarımı takip eder. 

### <a name="landing-page"></a>Giriş sayfası
Genişletilebilir olmayan özel zaman girişi deneyimi, sürüm 3'te kullanımdan kaldırıldı. Bunun yerine artık genişletilebilir ve erişilebilir yerel ızgara deneyimi bulunur. Soldaki site haritasını kullanarak zaman girişi işlevlerine erişebilirsiniz. Bu değişiklikle artık bir defada bir haftalık zaman giremezsiniz. Bunun yerine ızgaradaki her gün için bir zaman girişi oluşturmanız gerekir. Birkaç zaman girişi oluşturulduktan sonra kullanıcılar bu konuda daha sonra açıklanan **Kopyalama** işleviyle zaman girdilerini toplu olarak oluşturabilirler. 

![Zaman girişi giriş sayfası](media/time-entry-landing-page-07.png)
 
### <a name="create-new-time-entries"></a>Yeni zaman girişi oluşturma 
Zaman girişi için süreyi dakika, saat veya gün olarak girebileceğiniz bir hızlı oluşturma sayfası açmak için şeritte **Yeni** öğesini tıklatın. Bunu yapmak için miktarla birlikte h, m veya d yazmaya başlamanız yeterlidir.  

![Zaman girişini hızlı oluşturma](media/quick-create-time-entry-08.png)

Arama alanları, sistem görünümleriyle desteklenir. Örneğin, proje bilgilerini girdikten sonra **Proje görevi** alanı varsayılan olarak **Açık Proje Görevlerim** görünümüne ayarlanır. Kullanıcıya atanmamış görevler için zaman girişleri oluşturmak üzere aramada **Görünümü değiştir** öğesini tıklatın ve **Tüm Etkin proje görevleri**'ni seçin. Zaman girişi oluşturulduktan ve ızgarada gösterildikten sonra herhangi bir satır değerini doğrudan ızgarada düzenleyebilirsiniz.  

### <a name="bulk-createcopy"></a>Toplu oluşturma/kopyalama 
Birkaç zaman girişi oluşturulduktan sonra ek zaman girişlerini toplu olarak oluşturmak için kopyalama işlevini kullanabilirsiniz. **Kopyalama** iletişim kutusunu açmak için **Kopyala** öğesini tıklatın. **Başlangıç Dönemi: Başlangıç Tarihi** bölümünde, içinden zaman dilimlerinin kopyalanacağı tarih aralığını ayarlayın. **Bitiş dönemi: Başlangıç Tarihi** bölümünde, zaman girişlerinin oluşturulacağı tarihi belirtin. Zaman girişlerini **Bitiş dönemi** bölümünde belirtilen haftanın ilgili gününe kopyalamak için **Kopyala** öğesini tıklatın. Örneğin, geçen haftanın Pazartesi günü için zaman girişi **Bitiş dönemi** bölümünde belirtilen haftanın Pazartesi gününe kopyalanır. 

![Zaman girişlerini toplu olarak kopyalama](media/bulk-copy-time-entry-09.png)
 
### <a name="import-data"></a>Verileri içeri aktarın 
Atamalar ve exchange aynı arabirim düzenini takip eder ve ayırmaların içe aktarılması gerektiğinde kullanıcının başlangıç tarih aralığını belirlemesine olanak tanır. Ardından **Taslak** zaman girişlerine kopyalanması gereken ayırmaları açıkça seçmeniz gerekir. Sürüm 3'te, artık ızgara ve takvimde **Önerilen** zaman girişlerinin düzenini göremezsiniz.  

### <a name="change-in-calendar-control"></a>Takvim denetiminde değişiklik
Sürüm 3'te, özel takvim denetiminden uzaklaştık ve artık haftanın zaman girişlerini görüntülemek için UC Takvimi kullanıyoruz. Bu takvimle günü, haftayı ve ayı görüntüleyebilirsiniz. 

> [!NOTE]
> Takvimdeki sınırlama bu denetimin tek tek Takvim öğelerindeki eylemleri desteklememesidir. Örneğin, artık bir veya daha fazla takvim öğesi seçemez ve bu öğeleri gönderemez ya da silemezsiniz. Takvim öğesi tıklatıldığında ek eylemler için **Zaman girişi varlığı** sayfası açılır. 

### <a name="extensibility"></a>Genişletilebilirlik
**Özel alanlardaki veriyi yalnızca zaman ve gider girişi varlıklarında yakalama** - Zaman girişi düzenlenebilir bir ızgara, salt okunur bir ızgara ve platformdaki takvim denetimlerini kullanır. Bu denetimlerin tümü yereldir ve bu nedenle özelleştirmeleri desteklerler. Project Service Automation sürüm 3'te, ek özel alanlar ekleyebilir, arama alanlarını ayarlayabilir ve bunları özel görünümlerle yedekleyebilirsiniz. Özel alanlardaki seçili değerlere göre özel iş mantığı da ayarlayabilirsiniz.  

**Zaman ve gider girişindeki özel alanlarda veri yakalama ve bunu gönderme ve onay akışını destekleyen varlıklar aracılığıyla yayma** - Zaman girişlerinin tipik olarak işlenmesi aşağıdaki diyagramda gösterilmiştir.

![Zaman girişi işleme akışı](media/process-time-entries-10.png)

İş gereksinimleri, zaman ve gider varlıklarının özel fiyatlandırma boyutları yakalaması ve önceki grafikteki tüm varlıklar aracılığıyla özel fiyatlandırma boyutunda zamana ve giriş kaynağına göre ayarlanan değerlerin yayılması gerektiğini belirtiyorsa bkz. [Özel alanları fiyatlandırma boyutları olarak ayarlama](set-up-pricing-dimensions.md)

Zaman ve gider varlıklarının özel fiyatlandırma olmayan boyutları yakalaması ve değerleri yaymasının gerektiği iş gereksinimlerini desteklemek için fiyatlandırma boyutlarını ayarlama seçeneğini kullanabilir ve özel boyutları maliyet ya da fatura oranı olmadan fiyatlandırma boyutları olarak ifade edebilirsiniz. Başka bir senaryo, tüm varlıklarda aynı alan adını kullanarak varlıklara her birine özel bir alan eklemek olabilir. İşlem kaynağı ve işlem bağlantısı varlıklarını kullanarak gönderme/onay akışına katılan varlıklardaki kayıtları ilişkilendirmek için özel eklentiler oluşturulabilir.  

### <a name="delegate-time-and-expense-entry"></a>Temsilci süresi ve gider girişi
Common Data Service platformu, başka bir kullanıcının kimliğine bürünen bir kullanıcıyı desteklemez. Project Service Automation sürüm 3'te bu, temsilcili zaman ve gider girişi için destek olmadığı anlamına gelir. Ancak, iş ortakları ve müşteriler, sürüm 3'te temsilcili zaman girişi deneyimlerine destek sağlamak için geçici bir çözümden yararlandı. Bu, yalnızca geçici bir çözümdür ve tam bir çözüm değildir, bu nedenle sınırlamaları anlamak ve yalnızca sınırlamalar kabul edilebilirse bu yaklaşımı kullanmak önemlidir. 

> [!IMPORTANT]
> Bu bilgiler yalnızca bir iş ortağı/müşterinin özel uygulamaları için önerilen kılavuz olarak düşünülmelidir. Ürün takımı, destek kanallarımızda bu işlevler için resmi destek sunmaz.

### <a name="customization-details"></a>Özelleştirme ayrıntıları 
Özelleştirme, deneyimler oluşturmak ve düzenlemek için **Ayrılabilir kaynak** alanı eklemenize olanak tanır ve **Ayrılabilir kaynak** alanını zaman ve gider girişleri kaydedilmesi gereken başka bir kullanıcı olarak değiştirerek bir kullanıcının temsilci görevi görmesini sağlar. Aşağıdaki adımlar zaman girişi temsilcisi seçme işlemini içerir. Aynı bilgiler gider girişi temsilcisi seçme işlemi için de geçerlidir. 
 
1.  Temsilci olarak seçilen kullanıcının projelerde ve proje görevlerinde genel güvenlik erişimine sahip olduğundan emin olun. 
1.  **Zaman girişi** varlığındaki bir alan olan **Ayrılabilir kaynak**, **Hızlı oluşturma** sayfasında gösterilmediğinden bunu eklemeniz gerekir.

    -veya-

    Yalnızca kaynak için oluşturulan zaman girişlerini görüntülemek üzere özel bir görünüm oluşturun. Bu görünümü **Zaman girişleri** sayfasında, **Görünüm seçici** altında gösterilmesi için özelleştirmeleri uygulama modülü tasarımcısında yayımlayın. Proje olmayan zaman girişleri için yönetici ayarını kullanan iki eklenti bulunur:

    - PreValidateTimeEntryCreate
    - PreValidateTimeEntryUpdate
 
1. **Yönetici** alanını **Ayrılabilir kaynak** alanında atanan kullanıcının yöneticisi üzerine yazmak için yeni bir eklenti oluşturun. Aynı **Yürütme aşaması**'nı bant dışı (OOB) eklenti (doğrulama öncesi) olarak kullanın ve OOB eklentilerinden daha büyük (1'den büyük) bir **Yürütme sırası** kullanın. Bu, özel eklentinin OOB eklentilerinden sonra yürütülmesini sağlar.  
 
### <a name="end-user-experience"></a>Son kullanıcı deneyimi
1.  Hızlı oluşturma sayfasında bir zaman girişi oluştururken Proje ve Proje görevi ayrıntılarını girin ve ardından zaman girişlerinin kaydedilmesinin gerektiği **Ayrılabilir kaynak** alanındaki kullanıcıyı seçin. 
2.  Bu alan oturum açan kullanıcı için varsayılan olarak bulunur ancak kullanıcı bu alanı geçersiz kılarsa zaman girişi artık seçilen **Ayrılabilir kaynak** için oluşturulur.
3.  Bu kayıtlar için oluşturduğunuz zaman girişlerini gönderdiğinizde girişler, projede beklendiği gibi onaylayan için kuyruğa alınır. 
4.  Diğer kullanıcı için oluşturulan zaman girişlerini geri çektiğinizde zaman girişleri **Taslak** durumuna geri döner ve **Ayrılabilir Kaynak** alanı diğer kullanıcıya ayarlanır. 
5.  İsteğe bağlı olarak, diğer kullanıcı için oluşturulan zaman girişlerini filtrelemek üzere özel görünüme geçebilirsiniz. 
 
### <a name="limitations"></a>Sınırlamalar
**Kopyalama** ve **İçeri aktarma** işlevleri yalnızca oturum açan kullanıcı bağlamında çalışır. Bu, oturum açan kullanıcı için oluşturulan zaman girişlerinin ayrılabilir kaynak olarak kopyalanamayacağı veya içeri aktarılamayacağı anlamına gelir.

Bir proje için olmayan zaman girişleri yalnızca yukarıda **Özelleştirme Ayrıntıları** bölümündeki 4. adım tamamlanırsa ayrılabilir kaynak yöneticisinin onaylaması için yönlendirilir. Aksi durumda diğer kullanıcıya ait proje olmayan zaman girişleri, oturum açan kullanıcının yöneticisine yanlış yönlendirilmiş olur. 

### <a name="other-changes"></a>Diğer değişiklikler 
**Ayırmalar ve Görevler** işlevi kaldırıldı. 

## <a name="multidimensional-pricing"></a>Çok boyutlu fiyatlandırma
Esnekliği en üst düzeye çıkarmak ve farklı iş gereksinimlerini karşılamak için, Project Service Automation sürüm 3, maliyet ve fatura oranları için ayrı fiyatlandırma boyutu kümeleri uygulamasını destekler. Boyut değerleri varsayılan olarak ayarlanabilir ve ardından kaynak profili oluşturmadan zaman girişine ve proje gerçek değerlerine kadar maliyetlendirme ve fiyatlandırma işlemi üzerinden yayılır. Müşteriye özgü yapılandırma ve değişiklik veya uzantı standart özelleştirilebilirlik altyapısından yararlanır.

Project Service Automation varsayılan fiyatlandırma boyutları, rolleri ve kaynak birimleri kümesiyle birlikte gelir ve her Rol ve Kuruluş birimi birleşimi için fiyat ve maliyeti ayarlamanıza olanak tanır.

Sürüm 3'te bu kullanıma hazır alanları fiyatlandırma boyutları olarak kullanmaya devam etmek isteyen Project Service Automation müşterileri için gözlemlenebilir bir değişiklik yoktur. Project Service Automation'ı her zamanki gibi kullanmaya devam edebilirsiniz. Ancak kaynaklarınızın fiyat veya maliyeti için diğer ek öznitelikleri kullanmanız gerekiyorsa sürüm 3, kendi özel fiyatlandırma boyutlarınızı Project Service Automation'a eklemenize olanak tanır. Özel fiyatlandırma boyutlarının uzantısı karmaşık bir yapılandırma deneyimidir. 

## <a name="quotes-and-contracts"></a>Teklifler ve sözleşmeler
Project Service Automation sürüm 3'te, teklifler ve sözleşmelerin ayarları ve yönetim özellikleri değişmiştir. Aşağıdaki bölümlerde daha ayrıntılı bilgiler sağlanmaktadır.

### <a name="set-up-chargeability-options"></a>Borçlandırılabilirlik seçeneklerini ayarlama
Sürüm 1 ve 2'de teklifler ve sözleşmeler için roller ve kategorilerin borçlandırılabilirlik ayarı teklif satırı veya sözleşme satırının üst gezinti çubuğunda bulunan **Borçlandırılabilirlik** görünümü kullanılarak yapılıyordu. Bu aynı zamanda bu roller ve Gider kategorileri için fiyatları ayarlayabileceğiniz yerdi.

Sürüm 3'ten itibaren rol ve Gider kategorisine göre borçlandırılabilirlik seçeneklerinin ayarı teklif veya sözleşme satırı düzeyinde yapılır. Fiyatlandırma ayarı, Borçlandırılabilirlik ayarından ayrıdır. Üst gezinti çubuğunu kullanmak zorunda kalmadan **Borçlandırılabilirlik rolleri** ve **Borçlandırılabilirlik kategorileri** bölümlerini **Teklif satırı** ve **Sözleşme satırı** sayfalarında sekme olarak bulabilirsiniz.

![Borçlandırılabilir roller](media/chargeable-12.png)
 
Borçlandırılabilir roller ve Borçlandırılabilir kategoriler ayarı için de kullanıma hazır düzenlenebilir ızgara denetiminden yararlanılabilir. Her rol ve kategori için, Teklif Verme ve Sözleşme aşamasında fatura türü için desteklenen seçenekler önceki sürümde **Borçlandırılabilir** ve **Borçlandırılamaz** olarak değişmeden kalır. **Ücretsiz** Teklif Verme ve Sözleşme aşamasında desteklenen bir tür değildir. **Ücretsiz** yalnızca Zaman veya Gider onayı sırasında desteklenir.  
 
### <a name="create-and-edit-custom-pricing-for-a-project-service-automation-quote-and-project-contract"></a>Project Service Automation teklif ve proje sözleşmesi için özel fiyatlandırma oluşturma ve düzenleme
Sürüm 1 ve 2'de, özel teklifler ve sözleşmeler için özel fiyat listesi kullanımı **Borçlandırılabilirlik** görünümünde **Fiyatları düzenle** kullanılarak yapılıyordu. **Borçlandırılabilirlik** görünümü, teklif satırının veya sözleşme satırının en üst gezinti çubuğunda yer almaktaydı. Bu aynı zamanda roller ve gider kategorileri için borçlandırılabilirlik seçeneklerini ayarlayabileceğiniz yerdi.

Sürüm 3'ten itibaren Project Service Automation teklifinde ve Project Service Automation proje sözleşmesinde özel proje fiyat listesi oluşturma ve kullanma borçlandırılabilirlik ayarından ayrılmıştır. Project Service Automation teklifi ve Project Service Automation proje sözleşmelerinde **Proje fiyat listeleri** olarak adlandırılan yeni bir sekme bulunur. Bu sekmede, Project Service Automation teklif veya proje sözleşmesine eklenen tüm Proje fiyat listelerinin ilişkilendirilmiş bir görünümü gösterilir. Proje teklifi veya sözleşmesiyle önceden ilişkilendirilmiş varolan bir fiyat listesinden özel bir fiyat listesi oluşturmak için **Özel fiyat oluştur** öğesini tıklatın. Bu işlemle ilişkili tüm fiyat listelerinin bir kopyasını alınır ve Teklife veya sözleşmeye eklenir. Artık bu fiyatlandırma değişiklikleri yalnızca bu teklif veya sözleşme için geçerli olacak şekilde fiyat listesini açabilir ve rol veya gider kategorisi fiyatını düzenleyebilirsiniz. 
  
Aşağıdaki grafik, özel fiyat listeleri oluşturulmadan önceki durumu gösterir.

![Zaman girişi işleme akışı](media/before-custom-price-lists-13.png)

Aşağıdaki grafik, özel fiyat listeleri oluşturulduktan sonraki durumu gösterir.

![Zaman girişi işleme akışı](media/after-custom-price-lists-14.png)

> [!NOTE]
> Özel fiyat listesi oluştururken **Özel Fiyat Oluştur** öğesini tıklattığınızda kısa bir gecikme yaşanabilir. Birden çok kez tıklatmak yerine ızgarayı yenilemenizi öneririz. İlişkili fiyat listesi adında kendisine eklenen teklif adı veya proje sözleşmesi adı varsa özel fiyat listesi oluşturulmuştur.
