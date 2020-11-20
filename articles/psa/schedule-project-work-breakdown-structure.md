---
title: İş kırılım yapısına sahip bir projeyi zamanlama
description: Project Service'ta iş kırılım yapısına sahip bir projeyi zamanlama
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 04f30f2f2ed93dd1525f1c86a7521cdbf39a77bc
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127902"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a>İş kırılım yapısına sahip bir projeyi zamanlama (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Proje zamanlaması, çalışmanın gerçekleştirilmesi için gereken kaynaklarla ve çalışmanın zaman dilimi ile iletişim kurar. Proje zamanlaması, projenin zamanında teslimi ile ilişkili tüm çalışmayı yansıtır. Projenin başlangıç aşamasının ilk adımlardan biri, bir proje takvimi oluşturmaktır. Bir proje planı oluşturmak için, iş kırılım yapısı oluşturmanız gerekir.  
  
 Aşağıdakilerde size yardımcı olan bir iş kırılım yapısına sahip proje yapısını oluşturun:  
  
- Yönetilebilir görevlerde çalışmayı bölme  
  
- Bir görevi tamamlamak için gereken zamanı tahmin etme  
  
- Görev bağımlılıkları ve görev süresini ayarlama  
  
- Her bir görevi tamamlamak için gereken rollerini tanımla  
  
  İş kırılım yapısındaki proje zamanlaması, etkileşimli bir Gantt şemasına benzer bir görünüm ve kullanıma sahiptir.  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a>Bir proje için iş kırılım yapısı oluşturma  
 Projedeki görevlerin sırasını göstermek için bir iş kırılım yapısı oluşturun. İş kırılım yapısı, görevleri, her görevin gereksinimlerini ve gelir ve maliyet bilgilerini içerir. İş kırılım yapınızda şunları ekleyebilirsiniz:  
  
-   Bir hiyerarşideki görev dizisi  
  
-   Varsa, bir görev başlatılmadan önce tamamlanması gereken diğer görevler  
  
-   Başlangıç tarihi, bitiş tarihi ve görev süresi  
  
-   Bir görev için gereken saat sayısı  
  
-   Tüm gerekli çalışan becerileri ve eğitimi  
  
-   Bir göreve atanan çalışanlar  
  
-   Tahmini gelir ve maliyetler  
  
## <a name="task-types"></a>Görev türleri  
İş kırılım yapınızı oluştururken aşağıdaki görev türlerini kullanırsınız:  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| **Proje kök düğümü** | Proje için en üst düzey özet görevi. Diğer tüm proje görevleri, proje altında oluşturulur. Kök görevin adı proje adıdır. Kök düğümün çalışması, tarihleri ve süresi aşağıdaki hiyerarşide bulunan değerleri temel alır. Kök düğümü özelliklerini düzenleyemez veya kök düğümü silemezsiniz. | 
| **Özet veya kapsayıcı görevleri** | Bir özet görev, altında alt görevlere sahip olan bir görevdir. Bir özet görev herhangi bir iş çalışmasına veya kendi maliyetine sahip değildir. Çalışma ve maliyet alt görevlerinin toplu değeridir. Bir özet görevin adını değiştirebilirsiniz ancak, otomatik olarak hesaplandığı için çalışmayı, tarihleri veya süreyi değiştiremezsiniz. Bir özet görevin silinmesi, görevi ve onun alt görevlerini siler.|  
| **Yaprak düğüm görevleri** | Bir yaprak düğüm görevi, projedeki en ayrıntılı çalışmayı temsil eder. Bu, bir tahmini çalışmaya, kaynakların planlanan sayısını, planlanan başlangıç ve bitiş tarihlerini ve bir süreye sahiptir.|

  
## <a name="task-hierarchy"></a>Görev hiyerarşisi  
 Görev hiyerarşisi oluşturma sırasında aşağıdaki seçeneklere sahipsiniz:  
  
- **Görev ekle**.   Görev hiyerarşisinde seçtiğiniz bir konuma görev ekleyebilirsiniz. Bir konum seçmezseniz, yeni göreviniz en sonda görünür.  
  
- **Görevi girintile**.   Görevi hemen üstündekinin alt görevi yapmak için bir görevi girintileyin.  
  
- **Görevi çıkıntıla**.   Artık kendi özgün üst görevin alt görevi olmaması için bir görevi çıkıntılayın.  
  
- **Yukarı taşı ve Aşağı taşı**.   Görevleri kendi ana görev hiyerarşisinde yukarı ve aşağı taşıyın. Bir görevin yukarı veya aşağı taşınması çalışma, maliyet, tarihler veya süre üzerinde hiçbir etkisi olmaz.  
  
## <a name="task-attributes"></a>Görev öznitelikleri  
 Görevin adı tamamlanması gereken işi tanımlar. Görev için zamanlama ve kadro ihtiyaçlarını tanımlamak için görev öznitelikleri kullanın.  
  
### <a name="schedule-attributes"></a>Zamanlama öznitelikleri

 - Görevin zamanlamasını belirlemek için **Çalışma saati**, **Kaynak sayısı**, **Başlangıç tarihi**, **Bitiş tarihi** ve **Süre** öğelerine değer atayın. 
 - **Çalışma**, görevi tamamlamak için gereken saatlik bir tahmindir.
 - **Kaynak sayısı**, proje yöneticisinin olası en iyi zamanlamayı oluşturmasına yardımcı olması için göreve eklediği bir tahmindir. 
 - **Süre** (gün cinsinden), görevi tamamlamak için gereken iş günü sayısını gösterir.  
  
### <a name="staffing-attributes"></a>Kadro oluşturma öznitelikleri

 - **Rol**, **Kaynak kuruluş birimi**, **Kaynak sayısı** ve **Kaynaklar**, görevin kadro oluşturma gereksinimlerini açıklar. 
 - **Rol**, görevi gerçekleştirmek için gereken kaynak türünü açıklar. 
 - **Kaynak kuruluş birimi**, görev için personel sağlanması gereken kuruluş birimini gösterir; bu aynı zamanda kaynak için birim satış fiyatını belirlerken hesaplandığından görevin maliyet ve satış tahminini de etkiler. 
 - **Kaynaklar**, genel bir kaynak veya biri bulunduğunda adlandırılmış bir kaynak barındırır.  
  
## <a name="task-dependencies"></a>Görev bağımlılıkları  
 İş kırılım yapısında bir veya daha fazla görev arasında öncül ilişkileri oluşturabilirsiniz. Görevlere bağımlı görevleri göstermek üzere öncül alan için bir veya daha fazla değer ayarlayabilirsiniz. Görev için bir öncül değer atadığınızda, yalnızca tüm öncül görevler tamamlandığında görev başlatabilirsiniz. Görev üzerinde bu bağımlılığı ayarlamanız, görevin planlanan başlangıç tarihinin tüm öncüllerinin sonu olarak hesaplanmasıyla sonuçlanır. Bir zamanlamadaki öncül ile ilgili etkiler, görevde tanımlı görev modu ile sınırlı değildir.  
  
## <a name="task-mode"></a>Görev modu  
 Görev modu, yaprak düğüm görevlerini zamanlamayı belirleyen önemli etkenlerden biridir. Her görev için iki görev modu vardır: otomatik zamanlama modu ve el ile zamanlama modu.  
  
-   **Otomatik zamanlama**.   Görev modunu Otomatik Olarak Zamanlandı olarak ayarladığınızda, görev zamanlama altyapısı görev için zamanlamayı belirlemek üzere aşağıdaki görev özniteliklerindeki zamanlama kurallarını kullanır:  
  
    -   Öncüller  
  
    -   Çalışma  
  
    -   Kaynak sayısı  
  
    -   Başlangıç ve bitiş tarihleri  
  
-   **Zamanlama kuralları**.   Öncülleri olmayan bir yaprak düğüm görevinin başlangıç tarihi, projenin zamanlama başlangıç tarihi olarak varsayılana ayarlanır. Bir yaprak düğüm görevinin süresi her zaman kendi başlangıç ve bitiş tarihleri arasındaki iş günü sayısı olarak hesaplanır. Bir görev otomatik olarak zamanlandığında, zamanlama altyapısı aşağıdaki kuralları uygular:  
  
    -   Bir görevin başlangıç ve bitiş tarihleri, projenin zamanlama takvimine bağlı olarak her zaman iş günü olmalıdır  
  
    -   Öncüllere sahip bir görevin başlangıç tarihi öncüllerinin en son bitiş tarihi varsayılanlarına ayarlanır  
  
    -   Çalışma = Kişi sayısı * Süre * saat, proje takviminin standart iş günüdür  
  
-   **El ile zamanlama**.   Bazı durumlarda, bu kuralların dışına çıkmak isteyebilirsiniz. Bu durumlarda, görevin elle zamanlanması için görev modunu ayarlayabilirsiniz. Bu, zamanlama altyapısının diğer zamanlama özniteliklerinin değerlerini hesaplamayı durdurur. Görevlerdeki öncüllerin ayarlanması her zaman bağımlı görevin başlangıç tarihini etkiler.  
  
## <a name="create-a-work-breakdown-structure"></a>İş kırılım yapısı oluşturma  
  
1.  **Project Service > Projeler**'e gidin.  
  
2.  Üzerinde çalışmak istediğiniz projeye tıklayın.  
  
3.  Ekranın en üstünde bulunan çubukta, proje adının yanındaki aşağı oku seçin ve ardından İş kırılım yapısı'na tıklayın.  
  
4.  Bir görev eklemek için, **Görev Ekle**'ye tıklayın. Görev için alanları doldurun ve **Kaydet** öğesine tıklayın.  
  
5.  İş kırılım yapınız tamamlanana kadar görev eklemeye devam edin. İş kırılım yapınızı oluştururken, görevlerinizi düzenlemek için aşağıdakileri yapabilirsiniz:  
  
    -   Bir görev seçin ve başka bir görevin altına taşımak için **Girintile** ya da bir düzeyden çıkarmak için Çıkıntıla'ya tıklayın.  
  
    -   Bir görev seçin ve listede aşağı ya da yukarı hareket etmek için **Yukarı Taşı** veya **Aşağı Taşı**'ya tıklayın.  
  
    -   Gantt grafiğini gizlemek için **Gantt'yi gizle**'ye tıklayın ve yeniden görüntülemek için **Gantt'yi göster**'e tıklayın.  
  
    -   **Zaman Ölçeği**'ndeki Gantt grafiği için farklı bir zaman dilimi seçin.  
  
6.  Projenizin takım üyeleri için iş kırılım yapınızda belirttiğiniz rolleri eklemek üzere, **Proje Takımı Oluştur**'a tıklayın.  
  
7.  Değişiklik yapmayı bitirdiğinizde ekranın sağ alt köşesindeki **Kaydet**'e tıklayın.  
  
### <a name="see-also"></a>Ayrıca bkz.  
 [Proje yöneticisi kılavuzu](../psa/project-manager-guide.md)
