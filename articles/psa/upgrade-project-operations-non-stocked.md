---
title: Project Service Automation'dan Project Operations'a Yükseltme
description: Bu konuda Microsoft Dynamics 365 Project Service Automation'dan Dynamics 365 Project Operations'a yükseltme işlemine genel bakış sunulmaktadır.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/05/2022
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
ms.openlocfilehash: 9363fd5a06b6b1ba023961b03228e13a53a82002
ms.sourcegitcommit: 5789766efae1e0cb513ea533e4f9ac1e553158a5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/10/2022
ms.locfileid: "7952852"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Project Service Automation'dan Project Operations'a Yükseltme

Microsoft Dynamics 365 Project Service Automation'dan Dynamics 365 Project Operations'a yükseltme için üç aşamadan ilkini duyurmaktan heyecan duyuyoruz. Bu konu, bu heyecan verici yolculuğa çıkan müşteriler için genel bir bakış sağlar. Gelecekteki konular geliştirici konuları ve özellik geliştirmeleri hakkında ayrıntılar içerecektir. Bunlar yalnızca Project Operations'a yükseltmenize hazırlanmanıza yardımcı olacak rehberlik sağlamakla kalmaz, aynı zamanda yükselttikten sonra neler bekleyebileceğinizi de açıklar.

Yükseltme sunma programı üç aşamaya bölünecektir.

| Yükseltme sunma | Aşama 1 (Ocak 2022) | Aşama 2 (Nisan Dalgası 2022) | Aşama 3 (Nisan Dalgası 2022) |
|------------------|------------------------|---------------------------|---------------------------|
| Projeler için iş kırılım yapısına (İKY) bağımlılık yok | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Project Operations'ın şu anda desteklenen sınırları içindeki İKY | | :heavy_check_mark: | :heavy_check_mark: |
| Project Desktop Client desteği de dahil olmak üzere, şu anda desteklenen Project Operations sınırlarının dışındaki İKY | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Yükseltme işlemi özellikleri 

Yükseltme işleminin bir parçası olarak, yöneticilerin hataları daha kolay tanılayabilmesi için site haritasına yükseltme günlükleri ekledik. Yeni arabirime ek olarak, yükseltmeden sonra veri bütünlüğünü sağlamak için yeni doğrulama kuralları eklenecektir. Yükseltme işlemine aşağıdaki doğrulamalar eklenecektir.

| Doğrulamalar | Aşama 1 (Ocak 2022) | Aşama 2 (Nisan Dalgası 2022) | Aşama 3 (Nisan Dalgası 2022) |
|-------------|------------------------|---------------------------|---------------------------|
| İKY, yaygın veri bütünlüğü ihlallerine (örneğin, aynı üst görevle ilişkili ancak farklı üst projeleri olan kaynak atamaları) karşı doğrulanır. | | :heavy_check_mark: | :heavy_check_mark: |
| İKY, [Project for the Web'in bilinen sınırlarına](/project-for-the-web/project-for-the-web-limits-and-boundaries) göre doğrulanır. | | :heavy_check_mark: | :heavy_check_mark: |
| İKY, Project Desktop Client'ın bilinen sınırlarına göre doğrulanır. | | :heavy_check_mark: | :heavy_check_mark: |
| Ayrılabilir kaynaklar ve proje takvimleri, yaygın uyumsuz takvim kuralı özel durumlarına göre değerlendirilir. | | :heavy_check_mark: | :heavy_check_mark: |

2. aşamada, Project Operations'a yükseltme yapan müşteriler, mevcut projelerini proje planlaması için salt okunur bir deneyime yükseltir. Bu salt okunur deneyimde, tam İKY izleme kılavuzunda görünür olacaktır. İKY'yi düzenlemek için proje yöneticileri ana **Projeler** sayfasında **Dönüştür**'ü seçebilir. Arka plan işlemi daha sonra projeyi Project for the Web'den yeni proje zamanlama deneyimini destekleyecek şekilde güncelleştirir. Bu aşama, [Project for the Web'in bilinen sınırlarına](/project-for-the-web/project-for-the-web-limits-and-boundaries) uyan projeleri olan müşteriler için uygundur.

3. aşamada, projelerini bu uygulamadan düzenlemeye devam etmek isteyen müşterilere fayda sağlamak üzere Project Desktop Client için destek eklenecektir. Ancak, var olan projeler yeni Project for the Web deneyimine dönüştürülürse dönüştürülen her proje için eklentiye erişim devre dışı bırakılır.

## <a name="prerequisites"></a>Önkoşullar

Aşama 1 yükseltmesine uygun olmak için müşterinin aşağıdaki ölçütleri karşılaması gerekir:

- Hedef ortam **msdyn_projecttask** varlığında herhangi bir kayıt içermemelidir.
- Geçerli Project Operations lisansları müşterinin tüm etkin kullanıcılarına atanmalıdır. 
- Müşteri, yükseltme işlemini, üretim verilerine uygun temsili bir veri kümesine sahip en az bir üretim dışı ortamda doğrulamalıdır.
- Hedef ortam Project Service Automation Güncelleştirme Sürümü 38 veya sonraki bir sürüme güncelleştirilmelidir.

Aşama 2 ve aşama 3 için ön koşullar, genel kullanılabilirlik tarihleri yaklaştıkça güncellenecektir.

## <a name="licensing"></a>Lisanslama

Project Service Automation için etkin lisanslarınız varsa Project Service Automation'ın tüm özelliklerini ve daha fazlasını içeren Project Operations'ı yükleyebilir ve kullanabilirsiniz. Bu şekilde, üretimde Project Service Automation'ı kullanmaya devam ederken Project Operations'ın özelliklerini test edebilirsiniz. Project Service Automation lisanslarınızın süresi dolduktan sonra Project Operations'a geçiş yapmalısınız. Bu geçişi planlarken, Project Operations lisansının bir Project Service Automation lisansı içermediğini hesaba katmalısınız.

## <a name="testing-and-refactoring-customizations"></a>Özelleştirmeleri test etme ve yeniden düzenleme

Başlangıç noktası olarak içeri aktarma işleminin başarılı olduğunu ve iş operasyonlarının beklendiği gibi çalıştığını onaylamak için tüm özelleştirmeleri temiz bir Project Operations (lite) ortamına alın.

Dikkat edilmesi gereken bazı hususlar şunlardır:

- Eksik bağımlılıklar nedeniyle içeri aktarma işlemi başarısız olabilir. Başka bir deyişle, özelleştirmeler Project Operations'da kaldırılan alanlara veya diğer bileşenlere başvurur. Bu durumda, bu bağımlılıkları geliştirme ortamından kaldırın.
- Yönetilmeyen ve yönetilen çözümleriniz özelleştirilmemiş bileşenler içeriyorsa bu bileşenleri çözümden kaldırın. Örneğin, **Project** varlığını özelleştirdiğinizde, çözümünüze yalnızca varlık üst bilgisini ekleyin. Tüm alanları eklemeyin. Daha önce tüm alt bileşenleri eklediyseniz el ile yeni bir çözüm oluşturmanız ve buna ilgili bileşenler eklemeniz gerekebilir.
- Formlar ve görünümler beklenmeyen olarak görünmeyebilir. Bazı durumlarda, ilk çalıştırma formlarından veya görünümlerinden herhangi birini özelleştirdiyseniz özelleştirmeler Project Operations'daki yeni güncelleştirmelerin etkili olmasını engelleyebilir. Bu sorunları belirlemek için Project Operations'ın temiz bir yüklemesinin ve özelleştirmelerinizi içeren Project Operations yüklemesinin yan yana gözden geçirilmesini öneririz. Form sürümünüzün hala mantıklı olduğunu ve formun temiz sürümünden bir şey eksik olmadığını onaylamak için işletmenizdeki en sık kullanılan formları karşılaştırın. Özelleştirdiğiniz görünümler için aynı tür yan yana inceleme yapın.
- Çalışma zamanında iş mantığı başarısız olabilir. Eklentilerinizdeki alanlara yapılan başvurular içeri aktarma işleminde doğrulanmadığından, artık var olmayan alanlara yapılan başvurular nedeniyle iş mantığı başarısız olabilir ve aşağıdaki örneğe benzer bir hata iletisi alabilirsiniz: "'Project' varlığı Ad = 'msdyn_plannedhours' and NameMapping = 'Logical' bir öznitelik içermiyor." Bu durumda, özelleştirmelerinizi yeni alanları kullanacak şekilde değiştirin. Eklenti mantığınızda otomatik olarak oluşturulan proxy sınıflarını ve güçlü tür başvurularını kullanıyorsanız bu proxy'leri temiz bir yüklemeden yeniden oluşturmayı düşünün. Bu şekilde, eklentilerinizin kullanımdan kaldırılan alanlara bağlı olduğu tüm yerleri kolayca tanımlayabilirsiniz.

Project Operations'ı temiz bir şekilde içeri aktarmak için özelleştirmelerinizi güncelleştirdikten sonra sonraki adımlara geçin.

## <a name="end-to-end-testing-in-lower-environments"></a>Alt ortamlarda uçtan uca testler

### <a name="run-the-upgrade-in-production"></a>Yükseltmeyi üretimde çalıştırma

1. Power Platform yönetim merkezinde ortamınızı bulup seçin. Ardından, uygulamalarda **Dynamics 365 Project Operations**'ı bulup seçin.
2. Yükseltmeyi başlatmak için **Yükle**'yi seçin. Power Platform yönetim merkezi bu yüklemeyi yeni bir yükleme olarak sunacaktır. Ancak, Project Service Automation'ın önceki bir sürümünün varlığı algılanacak ve var olan yükleme yükseltilecektir.

    Yükseltme tamamlandıktan sonra, ortam Project Operations'ın yüklü olduğunu ve Project Service Automation'ın yüklü olmadığını göstermelidir.

    > [!NOTE]
    > Ortamdaki veri miktarına bağlı olarak yükseltme birkaç saat sürebilir. Yükseltmeyi yöneten çekirdek takım buna göre planlama yapmalı ve yükseltmeyi iş saatleri dışında çalıştırmalıdır. Bazı durumlarda, veri birimi büyükse yükseltme hafta sonu çalıştırılmalıdır. Zamanlama ile ilgili karar, alt ortamlardaki test sonuçlarına dayanmalıdır.

3. Özel çözümleri uygun şekilde yükseltin. Bu noktada, özelleştirmelerinizde yaptığınız değişiklikleri bu konunun [Özelleştirmeleri test etme ve yeniden düzenleme](#testing-and-refactoring-customizations) bölümünde dağıtın.
4. **Ayarlar** \> **Çözümler**'e gidin ve **Project Operations Kullanımdan Kaldırılan Bileşenler** çözümünü kaldırmak için seçin.

    Bu çözüm, yükseltme sırasında var olan veri modelini ve bileşenleri tutan geçici bir çözümdür. Bu çözümü kaldırarak artık kullanılmayan tüm alanları ve bileşenleri kaldırırsınız. Bu şekilde, arayüzü basitleştirmeye ve tümleştirme ve uzantıyı kolaylaştırmaya yardımcı olursunuz.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Project Service Automation ile Project Operations arasındaki önemli değişiklikler

Bu bölüm, Project Service Automation ile Project Operations arasında bekleyebileceğiniz önemli değişikliklerin bir özetini sağlar.

### <a name="project-planning"></a>Proje planlama

Project Operations'daki proje planlama özellileri artık istemci tarafı mantığı ve sunucu tarafı mantığını bir arada kullanamaz. Bunun yerine, Project Operations, zamanlama altyapısı olarak Project for the Web'i kullanır. Zamanlama özelliklerindeki bu değişiklik, Pano ve Gantt görünümleri, kaynak temelli planlama, [görev denetim listesi öğeleri](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c)ve proje zamanlama modları gibi çeşitli yeni özellikler sağlar. Yeni zamanlama özellikleri, zengin bir yeni [uygulama programlama arabirimleri (API)](../project-management/schedule-api-preview.md)kümesiyle de desteklenir. Bu API'ler, İKY'de varlık oluşturmak, güncelleştirmek veya silmek için hiçbir programlı işlemin zamanlamadaki hesaplanan alanları bozmamasını sağlamaya yardımcı olmak için tasarlanmıştır.

## <a name="billing-and-pricing"></a>Fatura ve fiyatlandırma

Project Operations'a yönelik devam eden yatırımların bir parçası olarak, Faturalama ve fiyatlandırma bölümündeki çeşitli yeni özellikler mevcuttur. İşte bazı örnekler:

- [Projelerde ve proje görevlerinde malzeme kullanımını kaydetme](../material/material-usage-log.md)
- [Alt sözleşme yönetimi](../pro/subcontracting/managing-subcontracts-overview.md)
- [Avanslar ve elde tutulan tutar tabanlı sözleşmeler](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Sözleşmenin aşılmama durumu ve doğrulamaları](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Görev tabanlı faturalandırma

## <a name="frequently-asked-questions"></a>Sık sorulan sorular

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Yükseltme için şu anda hangi dağıtım türleri destekleniyor?

| Source                                                 | Target                                                    | Status                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Proje Hizmeti Otomasyonu                             | Project Operations Lite Dağıtımı                        | Desteklenir               |
| Dynamics 365 Finance Proje Yönetimi ve Muhasebe | Project Operations Lite Dağıtımı                        | Şu anda desteklenmiyor |
| Finans Proje Yönetimi ve Muhasebe              | Kaynağı/stoğu tutulmayanlara ait senaryolar için Project Operations     | Şu anda desteklenmiyor |
| Finans Proje Yönetimi ve Muhasebe              | Stoklu/üretim siparişi senaryoları için Project Operations | Şu anda desteklenmiyor |
| Project Service Automation 3.x                         | Kaynağı/stoğu tutulmayanlara ait senaryolar için Project Operations     | Şu anda desteklenmiyor |
| Project for the Web (ayrılmış ortam)            | Project Operations Lite Dağıtımı                        | Şu anda desteklenmiyor |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Yükseltme aracı kullanıma sunulmadan önce Project Operations'ı nasıl yükleyebilirim?

Yükseltme aracı kullanıma sunulmadan önce Project Operations'ı yüklemek için iki seçenek vardır:

- Yeni ortam hazırlama.
- Project Service Automation'ın bulunmadığı herhangi bir satış kuruluşunda Project Operations'ı ayrı ayrı dağıtın.

> [!NOTE]
> Bir kuruluşta Project Service Automation yüklüyse ancak kullanılmamışsa kaldırılabilir. Project Service Automation'ı tamamen kaldırdıktan sonra, Project Operations aynı kuruluşa yüklenebilir.
