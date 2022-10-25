---
title: Project Service Automation'dan Project Operations'a Yükseltme
description: Bu makale, Microsoft Dynamics 365 Project Service Automation'dan Dynamics 365 Project Operations'a yükseltme işlemine genel bir bakış sunmaktadır.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/11/2022
ms.topic: article
ms.author: ruhercul
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
ms.openlocfilehash: 2d7b372cac391fab7a81ac6ac5d2ea6d12977b5c
ms.sourcegitcommit: 9de444ae0460c8d15c77d225d0c0ad7f8445d5fc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2022
ms.locfileid: "9687000"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Project Service Automation'dan Project Operations'a Yükseltme

Microsoft Dynamics 365 Project Service Automation'dan Microsoft Dynamics 365 Project Operations'a yükseltme için üç aşamadan ikincisini duyurmaktan heyecan duyuyoruz. Bu makale, bu heyecan verici yolculuğa çıkan müşterilere genel bir bakış sunar. 

Yükseltme sunma programı, üç aşamaya bölünecektir.

| Yükseltme sunma | 1. Aşama (Ocak 2022) | Aşama 2 (Kasım 2022) | 3. Aşama (Nisan Dalgası 2023)  |
|------------------|------------------------|---------------------------|---------------------------|
| Projeler için iş kırılım yapısına (İKY) bağımlılık yok | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Project Operations'ın şu anda desteklenen sınırları içindeki İKY | | :heavy_check_mark: | :heavy_check_mark: |
| Project Desktop Client desteği dahil olmak üzere şu anda desteklenen Project Operations sınırlarının dışındaki İKY | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Yükseltme işlemi özellikleri 

Yükseltme işleminin bir parçası olarak, yöneticilerin hataları daha kolay tanılayabilmesi için site haritasına yükseltme günlükleri ekledik. Yeni arabirime ek olarak yükseltmeden sonra veri bütünlüğünü sağlamak için yeni doğrulama kuralları eklenecektir. Yükseltme işlemine aşağıdaki doğrulamalar eklenecektir.

| Doğrulamalar | 1. Aşama (Ocak 2022) | Aşama 2 (Kasım 2022) | 3. Aşama  |
|-------------|------------------------|---------------------------|---------------------------|
| İKY, yaygın veri bütünlüğü ihlallerine (örneğin, aynı üst görevle ilişkili ancak farklı üst projeleri olan kaynak atamaları) karşı doğrulanır. | | :heavy_check_mark: | :heavy_check_mark: |
| İKY, [Project for the Web'in bilinen sınırlarına](/project-for-the-web/project-for-the-web-limits-and-boundaries) göre doğrulanır. | | :heavy_check_mark: | :heavy_check_mark: |
| İKY, Project Desktop Client'ın bilinen sınırlarına göre doğrulanır. | |  | :heavy_check_mark: |
| Ayrılabilir kaynaklar ve proje takvimleri, yaygın uyumsuz takvim kuralı özel durumlarına göre değerlendirilir. | | :heavy_check_mark: | :heavy_check_mark: |

2. aşamada, Project Operations'a yükseltme yapan müşterilerin mevcut projeleri, proje planlaması için salt okunur deneyime yükseltilir. Bu salt okunur deneyimde tam İKY, izleme kılavuzunda görünür olacaktır. İKY'yi düzenlemek için proje yöneticileri projenin ana sayfasında [**Dönüştür**](/PSA-Upgrade-Project-Conversion.md)'ü seçebilir. Arka plan işlemi daha sonra projeyi Project for the Web'den yeni proje zamanlama deneyimini destekleyecek şekilde güncelleştirir. Bu aşama, [Project for the Web'in bilinen sınırlarına](/project-for-the-web/project-for-the-web-limits-and-boundaries) uyan projeleri olan müşteriler için uygundur.

3. aşamada, projelerini bu uygulamadan düzenlemeye devam etmek isteyen müşterilere fayda sağlamak üzere Project Desktop Client desteği eklenecektir. Ancak, var olan projeler yeni Project for the Web deneyimine dönüştürülürse dönüştürülen her proje için eklentiye erişim devre dışı bırakılır.

## <a name="prerequisites"></a>Önkoşullar

1. Aşama yükseltmesine uygunluk için aşağıdaki ölçütleri karşılamanız gerekir:

- Hedef ortam **msdyn_projecttask** varlığında herhangi bir kayıt içermemelidir.
- Tüm etkin kullanıcılara geçerli Project Operations lisansları atanmalıdır. 
- Yükseltme işlemini, üretim ortamınıza uygun temsili bir veri kümesi içeren en az bir üretim dışı ortamda doğrulamalısınız.
- Hedef ortam, Project Service Automation Güncelleştirme Sürümü 37 (V3.10.58.120) veya sonraki bir sürüme güncelleştirilmelidir.

2. Aşama yükseltmesine uygunluk için aşağıdaki ölçütleri karşılamanız gerekir:

- Tüm etkin kullanıcılara geçerli Project Operations lisansları atanmalıdır. 
- Yükseltme işlemini, üretim ortamınıza uygun temsili bir veri kümesi içeren en az bir üretim dışı ortamda doğrulamalısınız.
- Hedef ortam, Project Service Automation Güncelleştirme Sürümü 37 (V3.10.58.120) veya sonraki bir sürüme güncelleştirilmelidir.
- Görev içeren ortamlar (msdyn_projecttask), yalnızca proje başına toplam görev sayısı 500 veya daha azsa desteklenir.

Genel kullanılabilirlik tarihi yaklaştıkça 3. Aşama ön koşulları güncellenecektir.

## <a name="licensing"></a>Lisanslama

Project Service Automation için etkin lisanslarınız varsa Project Service Automation'ın tüm özelliklerini ve daha fazlasını içeren Project Operations'ı yükleyebilir ve kullanabilirsiniz. Bu şekilde, üretimde Project Service Automation'ı kullanmaya devam ederken ayrı bir ortamda Project Operations'ın özelliklerini test edebilirsiniz. Project Service Automation lisanslarınızın süresi dolduktan sonra Project Operations'a geçiş yapmalısınız. Bu geçişi planlarken Project Operations lisansının Project Service Automation lisansı içermediğini hesaba katmalısınız.

## <a name="testing-and-refactoring-customizations"></a>Özelleştirmeleri test etme ve yeniden düzenleme

Başlangıç noktası olarak içeri aktarma işleminin başarılı olduğunu ve iş operasyonlarının beklendiği gibi çalıştığını onaylamak için tüm özelleştirmeleri temiz bir Project Operations (Lite) ortamına alın.

Dikkat edilmesi gereken bazı hususlar şunlardır:

- Eksik bağımlılıklar nedeniyle içeri aktarma işlemi başarısız olabilir. Başka bir deyişle, özelleştirmeler Project Operations'da kaldırılan alanlara veya diğer bileşenlere başvurur. Bu durumda, bu bağımlılıkları geliştirme ortamından kaldırın.
- Yönetilmeyen ve yönetilen çözümleriniz özelleştirilmemiş bileşenler içeriyorsa bu bileşenleri çözümden kaldırın. Örneğin, **Project** varlığını özelleştirirken çözümünüze yalnızca varlık üst bilgisini ekleyin. Tüm alanları eklemeyin. Tüm alt bileşenleri daha önce eklediyseniz el ile yeni bir çözüm oluşturmanız ve buna ilgili bileşenler eklemeniz gerekebilir.
- Formlar ve görünümler, beklenen şekilde görünmeyebilir. Bazı durumlarda, kullanıma hazır form veya görünümlerden birini özelleştirdiyseniz özelleştirmeler Project Operations'daki yeni güncelleştirmelerin etkili olmasını engelleyebilir. Bu sorunları belirlemek için Project Operations'ın temiz yüklemesinin ve özelleştirmelerinizi içeren Project Operations yüklemesinin yan yana gözden geçirilmesini öneririz. Form sürümünüzün hala mantıklı olduğunu ve formun temiz sürümünden herhangi bir eksik olmadığını onaylamak için işletmenizde en sık kullanılan formları karşılaştırın. Aynı yan yana incelemeyi, özelleştirdiğiniz görünümler de yapın.
- Çalışma zamanında iş mantığı başarısız olabilir. İçeri aktarma işlemi sırasında eklentilerinizdeki alanlara yapılan başvurular doğrulanmadığından, artık var olmayan alanlara yapılan başvurular nedeniyle iş mantığı başarısız olabilir ve şu örneğe benzer bir hata iletisi alabilirsiniz: "'Project' varlığı Ad = 'msdyn_plannedhours' and NameMapping = 'Logical' bir öznitelik içermiyor." Bu durumda, özelleştirmelerinizi yeni alanları kullanacak şekilde değiştirin. Eklenti mantığınızda otomatik olarak oluşturulan proxy sınıflarını ve güçlü tür başvurularını kullanıyorsanız bu proxy'leri temiz bir yüklemeden yeniden oluşturmayı düşünün. Bu şekilde, eklentilerinizin kullanımdan kaldırılan alanlara bağlı olduğu tüm yerleri kolayca tanımlayabilirsiniz.

Project Operations'ı temiz bir şekilde içeri aktarmak için özelleştirmelerinizi güncelleştirdikten sonra sonraki adımlara geçin.

## <a name="end-to-end-testing-in-development-environments"></a>Geliştirme ortamlarında uçtan uca test yapma

### <a name="initiate-upgrade"></a>Yükseltmeyi başlatma 

1. Power Platform yönetim merkezinde ortamınızı bulup seçin. Ardından, uygulamalarda **Dynamics 365 Project Operations**'ı bulup seçin.
2. Yükseltmeyi başlatmak için **Yükle**'yi seçin. Power Platform yönetim merkezi bu yüklemeyi yeni bir yükleme olarak sunacaktır. Ancak, Project Service Automation'ın önceki sürümünün varlığı algılanacak ve var olan yükleme yükseltilecektir.

    Yükseltme tamamlandıktan sonra ortam, Project Operations'ın yüklü olduğunu ve Project Service Automation'ın yüklü olmadığını göstermelidir.

    Ortamdaki veri miktarına bağlı olarak yükseltme birkaç saat sürebilir. Yükseltmeyi yöneten çekirdek takım buna göre planlama yapmalı ve yükseltmeyi iş saatleri dışında çalıştırmalıdır. Bazı durumlarda, veri birimi büyükse yükseltme hafta sonu çalıştırılmalıdır. Zamanlama ile ilgili karar, alt ortamlardaki test sonuçlarına göre verilmelidir.

3. Özel çözümleri uygun şekilde yükseltin. Bu noktada, özelleştirmelerinizde yaptığınız değişiklikleri bu makalenin [Özelleştirmeleri test etme ve yeniden düzenleme](#testing-and-refactoring-customizations) bölümünde dağıtın.
4. **Ayarlar** \> **Çözümler**'e gidin ve **Project Operations Kullanımdan Kaldırılan Bileşenler** çözümünü kaldırmak için seçin.

    Bu çözüm, yükseltme sırasında var olan veri modelini ve bileşenleri tutan geçici bir çözümdür. Bu çözümü kaldırarak artık kullanılmayan tüm alanları ve bileşenleri kaldırırsınız. Bu şekilde, arayüzü basitleştirmeye ve tümleştirme ve uzantıyı kolaylaştırmaya yardımcı olursunuz.
    
### <a name="upgrade-to-project-operations-lite"></a>Project Operations Lite'a yükseltme

Aşağıdaki adımlar yükseltme işlemini ve ilişkili hata günlüğünü açıklamaktadır:

1. **PSA Sürüm denetimi:** Project Operations'ı yüklemek için V3.10.58.120 veya sonraki bir sürümü gereklidir.
1. **Ön doğrulama:** Bir yönetici yükseltme başlattığında sistem, Project Operations çözümünün temelindeki her varlık için bir ön doğrulama işlemi çalıştırır. Bu adım tüm varlık başvurularının geçerli olduğunu doğrular ve İKY ile ilgili verilerin Project for the Web yayımlanmış sınırları içinde olmasını sağlar.
1. **Meta veri yükseltme**: Başarılı ön doğrulama işleminden sonra sistem, şemada değişiklikleri başlatır ve kullanım dışı bir bileşenler çözümü oluşturur. Özelleştirmelerin tüm gerekli yeniden düzenleme işlemleri tamamlandıktan sonra bu kullanım dışı çözümü kaldırabilirsiniz. Bu adım, yükseltme işleminin en uzun parçasıdır ve tamamlanması dört saate kadar sürebilir.
1. **Veri yükseltme:** Meta veri yükseltme adımında gerekli tüm şema değişiklikleri tamamlandıktan sonra verileriniz yeni şemaya taşınır. Ardından gerekli varsayılanlara sıfırlama ve yeniden hesaplama işlemleri yapılır.
1. **Proje zamanlama altyapısı güncelleştirmesi**: Başarılı veri yükseltmesinden sonra, ana sayfadaki **Zamanlama** sekmesi **Görevler** biçiminde yeniden etiketlenir. Kullanıcılar yükseltmenin ardından bu sekmeyi seçtiğinde, İKY'nin salt okunur bir sürümünü görüntülemek için izleme kılavuzuna gitmek üzere yönlendirilir. İKS'yi düzenlemek için zamanlama [dönüştürme işlemini](/PSA-Upgrade-Project-Conversion.md) başlatmaları gerekir. Önceden mevcut olan bir İKYS olmayan tüm projeler, dönüştürme olmadan yeni zamanlama deneyimini doğrudan kullanabilir.
 
### <a name="validate-common-scenarios"></a>Yaygın senaryoları doğrulama

Belirli özelleştirmelerinizi doğrularken uygulamalar genelinde desteklenen iş süreçlerini de gözden geçirmenizi öneririz. Bu iş süreçlerine teklif ve sözleşmeler gibi satış varlıklarının oluşturulması, İKY'leri içeren projelerin oluşturulması ve gerçek değerlerin onaylanması da dahildir.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Project Service Automation ile Project Operations arasındaki önemli değişiklikler

Bu bölümde Project Service Automation ile Project Operations arasında bekleyebileceğiniz önemli değişiklikler özetlenmektedir.

### <a name="project-planning"></a>Proje planlama

Project Operations'daki proje planlama özellikleri, artık istemci tarafı mantığı ve sunucu tarafı mantığını bir arada kullanamaz. Bunun yerine, Project Operations, zamanlama altyapısı olarak Project for the Web'i kullanır. Zamanlama özelliklerindeki bu değişiklik, Pano ve Gantt görünümleri, kaynak temelli planlama, [görev denetim listesi öğeleri](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c)ve proje zamanlama modları gibi çeşitli yeni özellikler sağlar. Yeni zamanlama özellikleri, zengin bir yeni [uygulama programlama arabirimleri (API)](../project-management/schedule-api-preview.md) kümesiyle de desteklenir. Bu API'ler, İKY'de varlık oluşturma, güncelleştirme veya silmeye yönelik programlı işlemlerin zamanlamada hesaplanan alanları bozmamasını sağlamayı amaçlar.

### <a name="billing-and-pricing"></a>Faturalandırma ve fiyatlandırma

Project Operations'a yönelik devam eden yatırımların bir parçası olarak, Faturalandırma ve fiyatlandırma bölümünde çeşitli yeni özellikler mevcuttur. İşte bazı örnekler:

- [Projelerde ve proje görevlerinde malzeme kullanımını kaydetme](../material/material-usage-log.md)
- [Alt sözleşme yönetimi](../pro/subcontracting/managing-subcontracts-overview.md)
- [Avanslar ve elde tutulan tutar tabanlı sözleşmeler](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Sözleşmenin aşılmama durumu ve doğrulamaları](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Görev tabanlı faturalandırma

### <a name="resource-management"></a>Kaynak yönetimi

Project Operations, Universal Resource Scheduling (URS) panosu ve zamanlama yardımcısı için isteğe bağlı destek sağlar. Bu yeni deneyim, Nisan 2023 dalgası kapsamında zorunlu olacaktır.

## <a name="frequently-asked-questions"></a>Sık sorulan sorular

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Yükseltme için şu anda hangi dağıtım türleri destekleniyor?

| Source                                                 | Target                                                    | Status                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Proje Hizmeti Otomasyonu                             | Project Operations Lite Dağıtımı                        | Desteklenir               |
| Dynamics 365 Finance Proje Yönetimi ve Muhasebe | Project Operations Lite Dağıtımı                        | Şu anda desteklenmiyor |
| Finans Proje Yönetimi ve Muhasebe              | Kaynağı/stoğu tutulmayanlara ait senaryolar için Project Operations     | Şu anda desteklenmiyor |
| Project Service Automation 3.x                         | Kaynağı/stoğu tutulmayanlara ait senaryolar için Project Operations     | Şu anda desteklenmiyor |
| Project for the Web (ayrılmış ortam)            | Project Operations Lite Dağıtımı                        | Şu anda desteklenmiyor |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Yükseltme aracı kullanıma sunulmadan önce Project Operations'ı nasıl yükleyebilirim?

Yükseltme aracı kullanıma sunulmadan önce Project Operations'ı yüklemek için iki seçenek vardır:

- Yeni ortam hazırlama.
- Project Service Automation'ın bulunmadığı herhangi bir satış kuruluşunda Project Operations'ı ayrı ayrı dağıtın.

Bir kuruluşta Project Service Automation yüklüyse ancak kullanılmamışsa kaldırılabilir. Project Service Automation'ı tamamen kaldırdıktan sonra Project Operations aynı kuruluşa yüklenebilir.
