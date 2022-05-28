---
title: Proje maliyeti izleme
description: Bu konu, Project Operations'ın bir projedeki işçilik maliyeti ve harcamalara ilişkin ilerlemeyi nasıl izlediği hakkında bilgiler sağlar.
author: rumant
ms.date: 03/22/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f724ee29728a363c58ed0e69087f4c18be89ea2d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591474"
---
# <a name="labor-cost-tracking-on-projects"></a>Projelerde işçilik maliyeti izleme

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Dynamics 365 Project Operations, işçilik tahminlerini ve harcamalarını proje planında gerekli olan en düşük düzeyde izler. İşçilik maliyetinin mali tahmini, proje planındaki her bir yaprak düğümü görevine atanan planlanan çalışma saati ve genel veya adlandırılmış kaynaklara dayanır. Proje başladığında ve insanlar çeşitli proje görevlerinde harcadıkları süreyi raporlamaya başladığında, işçilikte harcanan gerçek değerler özetlenir ve bu durum projeksiyonların hesaplanmasını başlatır.

## <a name="labor-cost-tracking-view"></a>İşçilik Maliyeti İzleme görünümü

**Projeler** sayfasındaki **İzleme** sekmesinde, **Maliyet İzleme**'yi açmak ve proje planındaki her bir görevin işçilik harcamalarının ilerlemesini görmek için **İzleme** > **Maliyet**'i seçebilirsiniz. Bu görünüm aynı zamanda bir görevde harcanan gerçek işçilik maliyetini, görevin planlanan işçilik maliyetiyle karşılaştırır. Project Operations, işçilik maliyet ölçümlerini hesaplamak için aşağıdaki formülleri kullanır:

- **Planlanan maliyet**: Her bir yaprak düğüm görevindeki tüm kaynak atamalarının tahmini maliyeti
- **Gerçek Maliyet**: Göreve kaydedilen süre boyunca tüm maliyet gerçek değerlerinin toplamı
- **Maliyet tüketimi yüzdesi**: Gerçek maliyet ÷ Tahmini tamamlanma maliyeti
- **Kalan Maliyet**: Tahmini tamamlanma maliyeti ÷ Gerçek maliyet
- **Tahmini Tamamlama Maliyeti**: Kalan maliyet + Gerçek maliyet
- **Maliyet değişimi**: Planlanan maliyet – Tahmini tamamlanma maliyeti

Her bir görev, görevdeki maliyet değişiminin bir projeksiyonu gösterir. Tahmini tamamlama maliyeti, planlanan maliyetten fazlaysa görevin bütçeyi aşacağı tahmini yapılır. Tahmini tamamlama maliyeti, planlanan maliyetten azsa görevin bütçenin altında tamamlanacağı tahmini yapılır.

>[!NOTE]
> Project Operations, işçilik maliyetlerini yalnızca **İzleme** sekmesindeki **Proje** sayfasında gösterir. Malzemeler ve giderler tüketim için tahmin edilip izlenebilir ancak bu maliyetler **İzleme** sekmesinde gösterilen maliyetlere dahil edilmez. Bu sekme, yalnızca işçilik maliyetlerinin yeniden tahmin edilme çalışmalarıyla çalışacak şekilde tasarlanmıştır.
Gösterilen tüm maliyet miktarları, projenin maliyet oranını belirlemek için kullanılan maliyet fiyatı para birimindeki proje maliyet para birimine dönüştürülür. Projenin maliyet para birimi, projedeki sözleşme birimi cinsinden para birimidir. Proje sayfasındaki tahminler sekmesinde gösterilen zaman için tahmini maliyet değerleri **Proje** sayfasındaki **Tahminler** sekmesinde gösterilen zaman maliyetiyle ilgili tahmin değerleri, **İzleme** sekmesindeki planlanan maliyetlerle aynı olmayabilir. Bu uyumsuzluğun nedeni, **Tahmin** ızgarasında tahmin edilen maliyetin özetlenme şekliyle **İzleme** ızgarasında planlanan maliyetin hesaplanma şekli arasındaki farktan dolayıdır. 
>
> - **Tahminler sekmesi**, fiyat listesindeki maliyet oranıyla aynı para birimini kullanarak tahmini maliyeti hesaplar. Ardından, fiyat listesi para birimi cinsinden tahmini maliyet, projenin maliyet para birimi cinsinden tahmini maliyete dönüştürülür. Proje para birimi cinsinden tahmini maliyet, 2 ondalık basamağa yuvarlanır. Bu dönüşümün hiçbir noktasında para birimi duyarlığı uygulanmaz. 
> - **İzleme** sekmesinde planlanan maliyet hesaplaması, iki aşamada uygulanan para birimi duyarlığı içeren biraz farklı bir hesaplama sırası izler: 
   ><ol>
   ><li>Fiyat listesi para birimi cinsinden tahmini maliyet tutarı, baz para birimine dönüştürülür (dönüştürme 1).</li>
   ><li>Baz para birimi cinsinden tahmini maliyet tutarı, proje maliyeti para birimine dönüştürülür (dönüştürme 2). </li>
   ></ol>
   >Para birimi duyarlığı her iki adımda da uygulanır. Bunun amacı, tahmini maliyetten (**Tahminler** sekmesinde **Zaman aşamalı** görünümde) biraz sapan bir planlanan maliyet (**İzleme** sekmesinde) elde etmektir. 
   
## <a name="reprojecting-costs-on-leaf-node-tasks"></a>Yaprak düğüm görevlerinde maliyetleri yeniden tahmin etme

Bir yaprak düğümü görevindeki işçilik maliyetleri, **Proje sayfasındaki** **İzleme** sekmesinde doğrudan yeniden tahmin edilemez. Ancak, görevdeki kalan çalışmayı yeniden hesaplamak için **Çalışma İzleme** görünümünü kullanabilirsiniz. Bunu yaptığınızda, görevdeki kalan maliyet yeniden hesaplanır. Aşağıda, bunun nasıl çalıştığı açıklanmıştır.

1. Proje yöneticileri, **Kalan Çalışma** alanındaki varsayılan değeri görevdeki kalan çalışmanın yeni tahminiyle güncelleştirerek görevdeki çalışmaları yeniden tahmin edebilir. Yeniden tahmin etme, görevin tahmini tamamlanma (EAC) çalışmasının ilerleme yüzdesinin ve görevdeki tahmin edilen çalışma değişikliğinin yeniden hesaplanmasına neden olur. EAC, tahmini tamamlanma süresi (ETC) ve özet görevlerindeki ilerleme durumu yüzdesi de yeniden hesaplanır ve yeni bir çalışma farkı tahmini oluşturulur.
2. Görevdeki kalan çalışma için yeni değere dayalı olarak sistem, **Maliyet İzleme** görünümünde kalan maliyeti hesaplar. Kalan çalışmaya dayanan kalan maliyeti hesaplamak için sistem, ilk olarak görevde planlanan maliyet veya planlanan çalışma olarak bir saatlik çalışmanın ortalama maliyetini hesaplar. Planlanan maliyet, görevdeki tüm kaynak atamalarının maliyetinin toplamıdır. Saat başına ortalama maliyet, görevdeki yeni tahmini kalan çalışma için kalan maliyeti hesaplamak amacıyla kullanılır.
3. Yaprak düğümü görevdeki tamamlanma maliyeti ve maliyet tüketimi yüzdesi yeniden hesaplanır.
4. Özet görevlerden kök düğümlere kadar tüm tamamlanma maliyeti değeri yeniden hesaplanır.

## <a name="reprojecting-costs-on-summary-tasks"></a>Özet görevlerinde maliyetleri yeniden tahmin etme

İşçilik maliyetlerini özet görevlerde veya konteyner görevlerinde yeniden tahmin edebilirsiniz. Ancak özet projesi görevindeki işçilik maliyetleri, **Proje** sayfasındaki **İzleme** sekmesinde doğrudan yeniden tahmin edilemez. Yaprak düğüm görevlerinde olduğu gibi özet ve konteyner görevlerini yeniden hesaplarken **Çalışma İzleme** görünümü kullanılabilir. Bu görünümde, bir özet görevdeki kalan çalışmayı yeniden tahmin edebilirsiniz. Bu durumda, özet görevdeki kalan maliyet de yeniden hesaplanır. Aşağıda, bunun nasıl çalıştığı açıklanmıştır.

1. Proje yöneticileri, özet görevlerin çalışmasını, kalan çalışmanın varsayılan değerini görevde yeni bir tahminle güncelleştirerek yeniden tahmin edebilir. Bu güncelleştirme, özet görevinin tahmini tamamlanma (EAC) çalışmasının ilerleme yüzdesinin ve görevdeki tahmin edilen çalışma değişikliğinin yeniden hesaplanmasına neden olur. EAC, ETC ve özet görevlerindeki ilerleme durumu yüzdesi de yeniden hesaplanır ve yeni bir çalışma farkı projeksiyonu oluşturur.
2. Özet görevindeki kalan çalışma için yeni değere dayalı olarak sistem, **Maliyet İzleme** görünümünde kalan maliyeti hesaplar. Kalan çalışmaya dayanan kalan maliyeti hesaplamak için sistem, ilk olarak özet görevinde planlanan maliyet veya planlanan çalışma olarak bir saatlik çalışmanın ortalama maliyetini hesaplar. Saat başına ortalama maliyet, özet görevindeki yeni tahmini kalan çalışma için maliyeti hesaplamak amacıyla kullanılır.
3. Özet görevindeki tamamlanma maliyeti ve maliyet tüketimi yüzdesi yeniden hesaplanır.
4. Yeni tamamlanma maliyeti alt öğe görevlerine, özgün planlanan maliyetin görevde sahip olduğu oranda dağıtılır.
5. Tek tek her görevin yaprak düğüm görevlerine kadar yeni tamamlanma maliyeti değeri hesaplanır. Bu değere bağlı olarak, yaprak düğümlere kadar alt görevlerin kalan maliyeti ve maliyet tüketme yüzdesi tamamlanma maliyeti değerine dayaranarak yeniden hesaplanır. Bu değer, görevin maliyet farkı için yeni bir tahminle sonuçlanır. 


**Maliyet performansı** alanı, izleme verilerinden ayarlanabilir. **Maliyet** izleme görünümündeki kök düğümün maliyet farkı negatifse bu alanı **Bütçe Altında** olarak ayarlayabilirsiniz. Kök düğümünün maliyet farkı pozitifse değeri **Bütçe Üzerinde** olarak ayarlayabilirsiniz.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
