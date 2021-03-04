---
title: Microsoft Dynamics 365 Project Service Automation sürüm 2.x veya 1.x'ten sürüm 3'e yükseltme işleminin önemli noktaları
description: Bu konu, Project Service Automation sürüm 2.x veya 1.x 'ten sürüm 3'e yükseltme işlemi gerçekleştirirken dikkat etmeniz gereken önemli noktalar hakkında bilgi sağlar.
manager: kfend
ms.prod: ''
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/13/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: c0c1e07bacb4867254a12436cf3bff58989e117f
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144209"
---
# <a name="upgrade-considerations---psa-version-2x-or-1x-to-version-3"></a>PSA sürüm 2.x veya 1.x'ten sürüm 3.x'e yükseltme işleminin önemli noktaları

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="project-service-automation-and-field-service"></a>Project Service Automation ve Field Service
Dynamics 365 Project Service Automation ve Dynamics 365 Field Service kaynak zamanlaması için Universal Resourcing Scheduling (URS) çözümünü kullanır. Kurulumunuzda Project Service Automation ve Field Service varsa her iki çözümü de en son sürüme yükseltin. Project Service Automation için sürüm 3.x. Field Service için sürüm 8.x. Project Service Automation veya Field Service'in yükseltilmesi URS'nin en son sürümünü yükler. Aynı kurulumdaki Project Service Automation ve Field Service çözümlerinin ikisi de en son sürüme yükseltilmezse bazı tutarsız davranışlar olabilir.

## <a name="resource-assignments"></a>Kaynak atamaları
Project Service Automation sürüm 2 ve sürüm 1'de, görev atamaları **Görev varlığı**'nda alt öğe görevleri olarak depolanır ve dolaylı olarak **Kaynak Atama** varlığıyla ilgilidir. Satır görevi İş Kırılım Yapısı'ndaki (İKY) atama açılır penceresinde görünür.

![Project Service Automation sürüm 2 ve sürüm 1'deki İKY üzerinde satır görevleri](media/upgrade-line-task-01.png)

Project Service Automation sürüm 3'te, görevlere ayrılabilir kaynaklar atama temel şeması değişti. Satır görevi kullanımdan kaldırılmıştır ve **Görev varlığı**'ndaki görev ile **Kaynak Atama** varlığındaki takım üyesi arasında doğrudan bire bir ilişki vardır. Proje takım üyesine atanan görevler artık doğrudan Kaynak Atama varlığında depolanır.  

Bu değişiklikler, bir proje takımındaki adlandırılmış ayrılabilir kaynaklar ve genel kaynaklar için kaynak atamalarının olduğu varolan projelerin yükseltilmesini etkiler. Bu konuda, sürüm 3'e yükseltirken projelerinizde dikkate almanız gereken önemli noktalar verilir. 

### <a name="tasks-assigned-to-named-resources"></a>Adlandırılmış kaynaklara atanan görevler
Sürüm 2 ve sürüm 1'de, görevler, temel görev varlığı kullanılarak takım üyelerinin varsayılan tanımlı rollerinden başka bir rol oynamalarına olanak tanıyordu. Örneğin, varsayılan olarak Program Yöneticisi rolüne atanan Emine Şen, Geliştirici rolünün olduğu bir göreve atanabilirdi. Sürüm 3'te, adlandırılmış takım üyesinin rolü her zaman varsayılandır. Bu nedenle Emine Şen'in atandığı herhangi bir görev Emine'nin varsayılan Program Yöneticisi rolünü kullanır.

Sürüm 2 ve sürüm 1'de bir kaynağı varsayılan rolü dışındaki bir göreve atadığınızda, yükseltme işleminden sonra sürüm 2'deki rol atamasından bağımsız olarak, adlandırılmış kaynak tüm görev atamaları için varsayılan role atanır. Tahminler satır görevi atamasına değil kaynağın rolüne göre hesaplandığından bu atama, sürüm 2 veya sürüm 1'de hesaplanan tahminlerin sürüm 3'ten farklı olmasına neden olur. Örneğin, sürüm 2'de Begüm Sağlam'a iki görev atanmıştır. Satır görevindeki rol, görev 1 için Geliştirici ve görev 2 için Program Yöneticisidir. Begüm Sağlam Program Yöneticisi varsayılan rolüne sahiptir.

![Bir kaynağa atanan birden çok rol](media/upgrade-multiple-roles-02.png)

Geliştirici ve Program Yöneticisi rolleri farklı olduğundan maliyet ve satış tahminleri aşağıdaki gibi olur:

![Kaynak rolleri için maliyet tahminleri](media/upggrade-cost-estimates-03.png)

![Kaynak rolleri için satış tahminleri](media/upgrade-sales-estimates-04.png)

Sürüm 3'e yükseltme işlemi gerçekleştirdiğinizde satır görevleri, ayrılabilir kaynak takım üyesinin görevindeki kaynak atamalarıyla değiştirilir. Atama, ayrılabilir kaynağının varsayılan rolünü kullanır. Aşağıdaki grafikte, Program Yöneticisi rolüne sahip Begüm Sağlam kaynaktır.

![Kaynak atamaları](media/resource-assignment-v2-05.png)

Tahminler kaynağın varsayılan rolünü temel aldığından satış ve maliyet tahminleri değişebilir. Aşağıdaki grafikte rol şimdi ayrılabilir kaynağın varsayılan rolünden alındığı için artık **Geliştirici** rolünü göremezsiniz.

![Varsayılan roller için maliyet tahminleri](media/resource-assignment-cost-estimate-06.png)
![Varsayılan roller için satış tahmini](media/resource-assignment-sales-estimate-07.png)

Yükseltme işlemi tamamlandıktan sonra bir takım üyesinin rolünü, atanan varsayılan dışında bir rol olacak şekilde düzenleyebilirsiniz. Ancak takım üyelerinin rolünü değiştirirseniz sürüm 3'te takım üyelerine birden çok rol atanamayacağı için atanmış görevlerinin tümü değiştirilir.

![Kaynak rolünü güncelleştirme](media/resource-role-assignment-08.png)

Bu, kaynağın kuruluş birimini varsayılandan başka bir kuruluş birimine değiştirdiğinizde adlandırılmış kaynaklara atanan satır görevleri için de geçerlidir. Sürüm 3 yükseltme işleminin tamamlanmasının ardından atama, satır görevindeki bir küme yerine kaynağın varsayılan kuruluş birimini kullanır.

### <a name="tasks-assigned-to-generic-resources"></a>Genel kaynaklara atanan görevler
Sürüm 2 ve sürüm 1'de, bir görev üzerinde rolü ve kuruluş birimini ayarlayabilir ve ardından görevde ayarlanan öznitelikleri temel alan genel kaynaklar oluşturmak için **Takım oluştur** özelliğini kullanabilirsiniz. Sürüm 3'te, rol ve kuruluş birimiyle genel takım üyeleri oluşturabilir ve ardından takım üyelerini görevlere atayabilirsiniz.

Sürüm 2 ve sürüm 1'de, genel kaynakların bulunduğu projeler iki durumda veya görev düzeyinde her ikisinin karışımı olabilir. Örneğin, şu senaryolarla karşılaşabilirsiniz:

- Roller ve kuruluş birimlerinin bulunduğu görevler ayarlanmış ancak bağlı kaynak ataması oluşturulmamış.
- Genel takım üyesi kaynak atamalarının bulunduğu görevler **Takım oluştur** özelliği kullanılarak genel kaynak oluşturularak atanmış.

Yükseltme işlemine başlamadan önce, genel kaynaklara atanan veya bunlar üzerinde takım oluşturma işlemini henüz çalıştırması gerekmeyen her proje için takımı yeniden oluşturmanızı öneririz.

**Takım oluştur** özelliğiyle oluşturulmuş genel takım üyelerine atanan görevler için yükseltme işlemi, takımdaki genel kaynağı ve bu genel takım üyesine yapılan atamayı bırakır. Genel takım üyesi için kaynak gereksinimini yükseltme işleminin ardından ancak bir kaynak isteği ayırmadan veya göndermeden önce oluşturmanızı öneririz. Bu, projenin sözleşme kuruluş biriminden farklı olan genel takım üyelerindeki kuruluş birimi atamalarını korur.

Örneğin, Proje Z projesinde, sözleşme kuruluş birimi Contoso ABD'dir. Proje planında, Uygulama aşamasındaki test görevleri, Teknik Danışman rolüne atanmıştır ve atanan kuruluş birimi Contoso Hindistan'dır.

![Uygulama aşaması kuruluş ataması](media/org-unit-assignment-09.png)

Uygulama aşamasından sonra, tümleştirme testi Teknik danışman rolüne atanır ancak kuruluş Contoso ABD olarak ayarlanır.  

![Tümleştirme testi görevi kuruluş ataması](media/org-unit-generate-team-10.png)

Proje için bir takım oluşturduğunuzda görevlerdeki farklı kuruluş birimleri nedeniyle iki genel takım üyesi oluşturulur. Teknik danışman 1, Contoso Hindistan görevlerine ve Teknik danışman 2 Contoso ABD görevlerine atanır.  

![Oluşturulan genel takım üyeleri](media/org-unit-assignments-multiple-resources-11.png)

> [!NOTE]
> Project Service Automation sürüm 2 ve sürüm 1'de, takım üyesi satır görevinde saklanan kuruluş birimini içermez.

![Project Service Automation'da sürüm 2 ve sürüm 1 satır görevleri](media/line-tasks-12.png)

Kuruluş birimini tahminler görünümünde görebilirsiniz. 

![Kuruluş birimi tahminleri](media/org-unit-estimates-view-13.png)
 
Yükseltme işlemi tamamlandığında, satır görevinde genel takım üyesine karşılık gelen kuruluş birimi genel takım üyesine eklenir ve satır görevi kaldırılır. Bu nedenle, yükseltme işleminden önce genel kaynaklar içeren her projede takımı oluşturmanızı veya yeniden oluşturmanızı öneririz.

Sözleşme projesinin kuruluş biriminden farklı bir kuruluş biriminin olduğu bir role atanan ve bir takımın oluşturulmadığı görevler için yükseltme işlemi, rol için genel takım üyesi oluşturur ancak takım üyesinin kuruluş birimi için projenin sözleşme birimini kullanır. Proje Z örneğine geri dönersek, sözleşme kuruluş birimi Contoso ABD ve Uygulama aşamasındaki proje planı test görevleri, Contoso Hindistan'a atanan kuruluş birimiyle Teknik Danışman rolüne atanmıştır. Uygulama aşamasından sonra tamamlanan Tümleştirme testi görevi Teknik danışman rolüne atanmıştır. Kuruluş birimi Contoso ABD'dir ve bir takım oluşturulmamıştır. Yükseltme işlemi, genel takım üyesi olarak tüm üç görevin atanmış saatlerine sahip bir Teknik danışmanı ve projenin sözleşme kuruluş birimi olarak Contoso ABD kuruluş birimini oluşturur.   
 
Oluşturulmamış takım üyelerinde farklı kaynak belirleme kuruluş birimlerinin varsayılan değerinin değişmesi nedeniyle kuruluş birimi atamalarının kaybedilmemesi için yükseltme işleminden önce genel kaynaklar içeren her projede takım oluşturmanızı veya yeniden oluşturmanızı öneririz.



[!INCLUDE[footer-include](../includes/footer-banner.md)]