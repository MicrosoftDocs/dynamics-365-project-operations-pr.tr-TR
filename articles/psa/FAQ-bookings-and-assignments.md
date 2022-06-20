---
title: Kaynak ayırmaları ve görev atamaları ile ilişkilendirilmeleri
description: Bu makale adlandırılmış kaynakların, kaynak ayırmalarının ve görev atamalarının ve bunların birbiriyle nasıl ilişkili olacağını yönetme hakkında bilgi sağlar.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: fd8f028a9f4056a646f5001ee8c91191c71140af
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910976"
---
# <a name="resource-bookings-and-how-they-relate-to-task-assignments"></a>Kaynak ayırmaları ve görev atamaları ile ilişkilendirilmeleri

[!include [banner](../includes/psa-now-project-operations.md)]

Aadlandırılmış kaynakların bir proje takımına ayrılması ve proje görevlerine atanması iki yolla yapılabilir:

- Kaynak doğrudan bir projeye ayrılıp ardından proje görevlerine atanabilir.
- Görevler, daha sonra adlandırılmış bir kaynak bulup bu gerçek kaynakla değiştirilmek üzere kullanılabilen genel bir kaynağa atanabilir. 

Her iki durumda da kaynağı ayırma işlemi kaynağın kapasitesini rezerve eder.

Projeyi planlayan proje yöneticisi, proje planının ve zamanlamasının sahibidir. Proje yöneticisi, atama için genel kaynak kullanıp ardından bundan bir kaynak isteği oluşturarak, kaynakları, proje planında belirtilen sınırlarla projeye ayırabilir. Proje yöneticileri kaynakları bir projeye ayırıp ardından görevlere atayabilir ancak ayırma sınırlarını görevlerin sınırlarıyla eşleştirmek mümkün değildir. Ayırmalar proje zamanlamasını etkilemez.

Aynı türden birden fazla kaynağın aynı anda çalışması gerektiği, birden çok çakışan görevleri içeren karmaşık bir proje göz önünde bulundurun. Bir kaynağa, atamalarının toplamındakinden farklı bir sınır getirilirse, ayırmaların sınırını kendilerine ait görevlere ve kendi orijinal sınırlarına uygun hale getirmek üzere görevlerde değişiklik yapmak zordur.

Aşağıdaki örnekte, dört görevlik bir kümeden aynı kaynak için gereken toplam çalışma değeri, iki haftalık dönem için 62 saattir ve belirli bir sınır vardır. Kaynak (Bob) aynı iki hafta için 62 saatliğine ama farklı bir sınırla ayrılırsa, gereksinim ve ayırmalar uyumludur.

| **Görev sınırları**    | **Toplam saat sayısı** | Pt 6/4 | Sa 6/5 | Ça 6/6 | Pe 6/7 | Cu 6/8 | Ct 6/9 | Pz 6/10 | Pt 6/11 | Sa 6/12 | Ça 6/13 | Pe 6/14 | Cu 6/15 |
|----------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Görev 1               | 24              | 8      | 8      | 4      |        |        |        |         |         |         | 4       |         |         |
| Görev 2               | 16              |        |        | 4      | 4      |        |        |         | 8       |         |         |         |         |
| Görev 3               | 10              |        |        |        |        | 4      |        |         |         | 4       |         | 2       |         |
| Görev 4               | 12              |        |        |        |        |        |        |         |         |         | 4       |         | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |         |         |
| **Toplamlar**           | 62              | 8      | 8      | 8      | 4      | 4      |        |         | 8       | 4       | 8       | 2       | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |

### <a name="bobs-availability"></a>Bob'un kullanılabilirliği
| **Kaynak ayırma** | **Toplam saat sayısı** | Pt 6/4 | Sa 6/5 | Ça 6/6 | Pe 6/7 | Cu 6/8 | Ct 6/9 | Pz 6/10 | Pt 6/11 | Sa 6/12 | Ça 6/13 | Pe 6/14 | Cu 6/15 |
|------------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Bob                    | 62              | 4      | 4      | 8      | 8      | 8      |        |         | 4       | 4       | 8       | 8       | 6       |

Bununla birlikte, ayrılan saat sayısı sınırını görevlere günlük bazda atamak için sistematik bir yol yoktur. Proje yöneticisi, kaynağın kullanılabilirliğini karşılamak için proje zamanlamasını değiştirmek isterse, atamayı kaldırıp, tüm görevleri, ayırma sınırlarına uyacak şekilde gözden geçirmek zorunda kalacaktır.

Bir kuruluşun hem bir proje yöneticisine hem de bir kaynak yöneticisine proje planlama görevi vermesi durumunda, proje yöneticisi zamanlamayı ayarlar ve bu ayarlama işlemi, gereken çalışmanın sınırlandırılmasını içerir. Kaynak yöneticisi, gerçek kaynakları ayırırken proje yöneticisinin bilgisi olmadan çalışma sınırlarını değiştirerek zamanlamayı etkileyememelidir. Kaynak yöneticisi, proje yöneticisinin istediğinden farklı bir şeyi karşılıyorsa, bu iki yöneticinin, proje zamanlamasında gereken değişiklikler konusunda anlaşmaya varması gerekir.

Ayırmalar ve atamalar kesin bir şekilde eşleştirilmediği için, görev sınırlarından farklı sınırlar ayırmak veya ayırma ve atamaların uyumlu olmadığı durumlar elde etmek üzere atamaları değiştirmek mümkündür.

**Mutabakat Görünümü**, proje yöneticisinin her proje takımı üyesine ait ayırma ve atamaları görebilmesini sağlar. Görünümde, bir takım üyesinin ayırma ve atamaları arasındaki uyumsuzluğun yerini göstermek için renkler ve tonlar kullanılır. Proje yöneticisi, bu bilgiler temelinde, atamalar olduğu halde ayırmaların olmadığı durumlar için kaynak ayırmaları genişletmek veya kaynakların ayrıldığı ancak atamaların olmadığı durumlarda ayırmaları iptal etmek için düzeltici eylem yapabilir.

> [!NOTE]
> Kendi kendinize sınır koyduğunuz bir görevi taşıdığınız zaman bu sınırların korunmaz. Sınırlar, çalışma saatlerindeki ve tatillerdeki değişiklikleri hesaba katmak için proje takvimine göre yeniden üretilir. Sistem baştaki sınırın amacını bilmediği ve bu sınırı yeni bir dönemde korumanın anlamlı olup olmayacağına karar veremeyeceği için, bu kasten yapılır. Ayırmaların ve atamaların bağlantısı kaldırıldığı için, ayırmalar baştaki ayırma sınırlarını korur. Bu durumda, iptal etmeniz ve yeni atama sınırına göre yeniden ayırmanız gerekir.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
