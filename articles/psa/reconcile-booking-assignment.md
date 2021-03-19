---
title: Ayırmalar ve atamalar arasında mutabakat sağlama
description: Bu konu gerçek değerler hakkında bilgi sağlar.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/27/2019
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
ms.openlocfilehash: 30af3cca9b4c3dc3f1a9412de7380c963bde88f0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283437"
---
# <a name="reconcile-bookings-and-assignments"></a>Ayırmalar ve atamalar arasında mutabakat sağlama

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Proje takımı üyesinin proje ayırmaları ile proje görev atamaları arasında kesin bir eşleşme yoktur. Bu nedenle, bir kaynağın ayırmalara karşılık gelmeyen görev atamaları ve görev atamalarına karşılık gelmeyen ayırmaları olabilir. İdeal olarak, proje ayırmaları ve atamalar, kaynaklar görev atamalarını gerçekleştirmek için kapasiteyi taahhüt edecek şekilde hizalanır. Ancak gerçekte ayırmalar kullanılabilirliği temel alır ve proje yaşam döngüsü boyunca devam ederken görev zamanlamaları değişebilir. Bu nedenle, kesin olmayan bir eşleşme esnekliğe olanak tanır.

Proje ayırmalarının ve görev atamalarının kesin olarak eşleşmemesi nedeniyle Proje varlığına **Mutabakat** sekmesi dahil edilir. Bu sekme, proje yöneticilerinin proje takımı için takım üyesi ayırmalarını ve bunların atamalarını mutabık kılmasına yardımcı olur.

Adlandırılmış her bir takım üyesi için, **Mutabakat** sekmesi ayırmaları ve atamaları tek tek görev atamasına indirger. Hücrelerde saatleri göstererek aylardan günlere kadar olan dönemleri temsil edebilir.

**Zaman ölçeği** alanında, **Ay**, **Hafta** veya **Gün**'ü seçebilirsiniz. Varsayılan olarak, **Hafta** seçilidir. Ancak **Ayarlar** düğmesini seçerek varsayılan değeri değiştirebilirsiniz. **Mutabakat** sekmesi açıldığında, geçerli tarihi gösterir ancak zamanda ileri veya geri gitmek için takvim denetimini kullanabilirsiniz. Proje gelecekteki bir başlangıç tarihine sahipse sekme açıldığında bu tarihi gösterir. Takvim denetiminde, proje başlangıç ve bitiş tarihlerine taşımanıza olanak tanıyan seçeneklere de bulunur.

Kaynak ayırmalarının ayrıntılarını göstermek için her kaynakta genişletici denetimlerini kullanabilirsiniz. Her kaynağın atamasını tek tek görev düzeyinde de genişletebilirsiniz.

**Mutabakat** sekmesinin alt kısmında proje için genel net toplam gösterilir ve ayrıca sekmede toplam sütunu bulunur. Her kaynak için sekme, bir takım üyesinin projedeki ayırmaları ile bu takım üyesinin görev atamalarının toplu değeri arasındaki farkı alır. İdeal olarak, fark 0 (sıfır) olmalıdır. Başka bir deyişle, kaynağın ayırmaları ile görev atamaları arasında fark olmamalıdır. Tüm farklar, iki koşulu çağırmak için renk ve gölgelerle belirtilir:

- **Ayırma eksikliği** – Ayırma eksikliği bir kaynakta ayırmadan daha fazla atama varsa oluşur. Bu kapasite ayrılmadığından bir proje yöneticisi eksikliği gidermek için kaynağın ayırmalarını uzatarak bu koşulu düzeltebilir.
- **Aşırı ayırmalar** – Aşırı ayırmalar bir kaynak projeye ayrıldığında ancak görevlere atanmadığında oluşur. Bu koşul, örneğin, kaynak görev ataması gerçekleşmeden önce ayrılmışsa kabul edilebilir. Ancak diğer durumlarda kaynak atanmak üzere planlanmayabilir. Bu durumlarda Proje Yöneticisi, kapasitenin başka bir projede kullanılabilmesi için kaynağın ayırmalarını iptal etmeyi düşünmelidir.

> [!NOTE]
> Bu koşulların göstergesi, ızgarada daha fazla yer bırakmak için gizlenmiş olabilir. Bu durumda, **Ayarlar** düğmesini seçerek göstergeyi görünür hale getirebilirsiniz.

Bazı durumlarda, **Zaman ölçeği** alanı **Gün**'den daha yüksek bir düzeye ayarlandığında farklar 0 (sıfır) olarak hesaplanabilir. Örneğin, **Ay** düzeyinde, kaynak için net fark ayırmaların atamalara eşit olduğunu belirtmek için 0 (sıfır) olabilir. Ancak **Hafta** düzeyine bakarsanız ayın ilk haftasında 0 (sıfır) saat atama ve 40 saat ayırma ve ayın ikinci haftasında 40 saat atama ve 0 (sıfır) saat ayırma olduğunu görebilirsiniz. Aylık toplam ayırma ve atama aynı olsa da bunlar haftaya göre farklılık gösterir.

Daha yüksek zaman düzeylerini görüntülediğinizde **Mutabakat** sekmesinde alt zaman düzeylerinde farklar olduğunu bildiren bir hücre göstergesi gösterilir. Örneğin, aşağıdaki resimde Jale Özcan adlı kaynak için Ekim 2018 ayına ait hücrede bir hücre göstergesi görünmektedir. Bu nedenle kaynağın ayırmaları ve atamalarının **Ay** düzeyinde toplandıklarında eşit oldukları halde alt düzeylerde eşleşmediklerini görebilirsiniz.

![Aylık düzeyde yanlış eşleşen kayıtlar ve atamalar](media/reconcile-assignments-01.JPG)

Sonraki alt düzeye yakınlaştırmak için bir hücreyi çift tıklatın ve farkı görüntüleyin. Örneğin, Jale Özcan için Ekim 2018 farkını çift tıklatırsanız **Hafta** düzeyi detayına girersiniz. Ardından kaynağın Ekim ayının ilk iki haftasında 16 saat ayırması olduğunu ancak ataması olmadığını ve Ekim ayının üçüncü haftasında 16 saat ataması olduğunu ancak ayırması olmadığını görebilirsiniz.

![Haftalık düzeyde yanlış eşleşen kayıtlar ve atamalar](media/reconcile-assignments-02.JPG)

Sonraki üst düzeyi uzaklaştırmak için bir hücreyi sağ tıklatabilirsiniz. Ayrıca **Ayarlar** düğmesini seçerek hücre göstergesini kapatabilirsiniz. 

Projenizdeki farklar arasında geçiş yapmak için ızgaranın üzerindeki **Önceki** ve **Sonraki** düğmelerini de kullanabilirsiniz. Bu düğmeleri kullanmak için önce bir kaynak seçmeniz gerekir. Bu kaynağın ayırmaları ile atamaları arasındaki sonraki farka gitmek için **Sonraki** öğesini seçin. Önceki farka gitmek için **Önceki** öğesini seçin.

Bir kaynak için atamalarınızın olduğu ancak ayırmalarınızın olmadığı durumlarda ayırma eksikliğini ve ardından **Ayırmayı Uzat** öğesini seçebilirsiniz. Ardından kaynak eksikliğini gidermek için gerekli olan ayırmayı görebilirsiniz. Geçerli proje ve diğer projelerdeki kaynak ayırmalarını da görüntüleyebilirsiniz. Geçerli kullanılabilirliği dikkate almadan kaynak için ayırma oluşturmak için **Tamam** öğesini seçin. Ardından proje yöneticisi veya kaynak yöneticisi, ayırmalarının uzatılması nedeniyle bir kaynağın kapasitesinin üzerinde fazladan ayrıldığı durumları yönetmek için Zamanlama Panosu'nu kullanabilir.

## <a name="managing-with-time-zones"></a>Saat dilimleriyle yönetme
Ayırmayı Uzat özelliğini kullanırken doğru ve öngörülebilir sonuçlar elde etmek için karşılanması gereken iki önemli ön koşul vardır:  

- Kullanıcının, kendi cihazının saat dilimini, sisteminizin Kişiselleştirme Ayarları'nda tanımlanan saat dilimiyle eşleşecek şekilde yapılandırması gerekir.
 
  ![Windows 10'da saat dilimi ayarları](media/reconcile-assignments-03.png)

  ![Kişiselleştirme ayarlarındaki saat dilimi ayarları](media/reconcile-assignments-04.png)
 
- Ayrılabilir Kaynak, istenen uzatmayı tanımlamak için kullanılan sınırlarla çakışan en az bir dakikalık çalışma zamanı içermelidir. Örneğin, aşağıdaki örnek 09:00 ve 19:00 arasında kalan çalışma saatlerine sahip inceleme kaynaklarını gösterir. 

  ![Kaynak sınırlarını karşılaştırma](media/reconcile-assignments-05.png)

Aşağıdaki tabloda şunlar gösterilmektedir:

- Proje takvimi şablonu.
- Kaynak A: Bu kaynak projeyle aynı takvime sahiptir ve aynı saat diliminde yer alır. Ayırmanın başlangıç saati 09:00 olarak görüntülenir.
- Kaynaklar B: Bu kaynak projeden farklı bir saat diliminde yer alır ve bu nedenle kendi saat diliminde saat 07:00'da başlar. Ancak, ayırmalar atama sınırının en erken başlangıç saati olan 09:00'da başlar.
- Kaynaklar C ve D: Kaynaklar birbirinden ve projeden farklı saat dilimlerinde yer alır ve ayırmaları da kendileri için uygun başlangıç saatlerinden önce başlamaz.

|Varlık  |Takvim  |
|-|-|
|Proje takvimi şablonu   | ![proje takvimi](media/reconcile-assignments-06.png) |
|Kaynak A  | ![Kaynak A takvimi](media/reconcile-assignments-06.png) |
|Kaynak B  |  ![Kaynak B takvimi](media/reconcile-assignments-07.png) |
|Kaynak C  |  ![Kaynak C takvimi](media/reconcile-assignments-08.png) |
|Kaynak D  | ![Kaynak D takvimi](media/reconcile-assignments-09.png)  |
 
Mutabakat görünümüne gittiğinizde, kaynak atamaları ve ilişkili ayırma eksiklikleri görüntülenir.
 ![Uzatmadan önceki mutabakat görünümü](media/reconcile-assignments-10.png)

Ayırmayı Uzat işlevi her kaynakta yürütüldükten sonra ayırmalar her kaynak için başarıyla uzatılır. Bunun nedeni, her kaynağın çalışma saatlerinin eksiklik sınırlarıyla çakışmasıdır.
 ![Ayırmayı uzatma sonrasındaki mutabakat görünümü](media/reconcile-assignments-11.png) 

Ancak ayırmanın ayrıntılarına daha yakından bakıldığında ayırmaların başlangıç saatindeki farklılıklar görülür. Ayırmalar, atama sınırının başlangıç saatinden önce ve kaynağın kullanılabilir başlangıç saatinden önce başlamaz.
 ![Zamanlama panosunda yeni kaynak ayırmaları](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]