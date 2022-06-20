---
title: Proje satışı izleme
description: Bu makalede, Project Operations'ın, işçilik gelirine göre nasıl izlediği ve bir proje üzerinde harcadıkları hakkında bilgiler yer alır.
author: rumant
ms.date: 03/24/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ce61acf95ee5e9ac10047406c9d4a5c9b1f92aad
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911298"
---
# <a name="project-sales-tracking"></a>Proje satışı izleme

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Dynamics 365 Project Operations, işçilik tahminlerini ve gelirlerini proje planında gerekli olan en düşük düzeyde izler. İşçilik gelirinin tahmini, proje planındaki her bir yaprak düğümü görevine atanan planlanan çalışma saati ve genel veya adlandırılmış kaynaklara dayanır. Proje başladığında ve insanlar çeşitli proje görevlerinde harcadıkları süreyi raporlamaya başladığında, gerçek işçilik geliri değerleri özetlenir ve bu durum projeksiyonların hesaplanmasını başlatır.

## <a name="labor-revenue-tracking-view"></a>İşçilik geliri izleme görünümü

**Projeler** sayfasındaki **İzleme** sekmesinde, **Maliyet İzleme** görünümünü açmak için **İzleme** > **Maliyet**'i seçebilirsiniz. Ya da proje planındaki her bir görevin işçilik geliri ilerlemesini gösteren **Gelir İzleme** görünümünü açmak için **Kullan** > **Fatura Oranı**'nı seçebilirsiniz. Bu görünüm aynı zamanda bir görevde harcanan gerçek işçilik gelirini, görevin planlanan işçilik geliriyle karşılaştırır. Project Operations, işçilik geliri ölçümlerini hesaplamak için aşağıdaki formülleri kullanır:

- **Planlanan Gelir**: Her bir yaprak düğüm görevindeki tüm kaynak atamalarının tahmini satış değerleri
- **Gerçek Gelir**: Göreve kaydedilen süre boyunca tüm faturalanmamış satış gerçek değerlerinin toplamı
- **Faturalanabilir Gelir Yüzdesi**: Gerçek gelir ÷ Tahmini sonuç geliri
- **Kalan Gelir**: Tahmini sonuç geliri – Gerçek gelir
- **Tahmini Sonuç Geliri**: Kalan gelir + Gerçek gelir
- **Gelir farkı**: Planlanan gelir – Tahmini sonuç geliri


> [!NOTE]
> Project Operations, işçilik gelirlerini yalnızca **İzleme** sekmesindeki **Proje** sayfasında gösterir. Malzemeler ve giderler tüketim için tahmin edilip izlenebilir ancak bu gelirler **İzleme** sekmesinde gösterilen gelirlere dahil edilmez. Bu sekme, yalnızca işçilik gelirlerinin yeniden tahmin edilme çalışmalarıyla çalışacak şekilde tasarlanmıştır.  
> Gösterilen tüm gelir miktarları, projenin maliyet para birimine dönüştürülür. Projenin maliyet para birimi, projedeki sözleşme birimi cinsinden para birimidir. Sabit fiyatlı projelerde, **İşçilik geliri izleme** görünümündeki gelir rakamlarının bir anlamı yoktur çünkü faturalanmayan satış gerçek değerleri zaman onayında kaydedilmez.
> Projenin **Tahmin** sekmesinde gösterilen zaman için tahmini satış değerleri, **İzleme** sekmesindeki planlanan gelir değeriyle aynı olmayabilir. Bu tutarsızlığın iki olası kaynağı olabilir:
><ol>
   ><li> <b>Tahminler</b> sekmesi, tahmini geliri satış para birimi cinsinden gösterirken <b>İzleme</b> sekmesi, planlanan geliri maliyet para birimine dönüştürülmüş şekilde gösteriyordur. </li>
   ><li> Tahmini satışlar, <b>Tahminler</b> sekmesinde gösterilen proje para birimine göre sözleşme para birimine dönüştürüldüğünde, dönüştürme işlemi doğruluk kaybına neden olabilecek adımlar içerir: </li>
><ol>
><li> Sözleşme para birimi cinsinden tahmini satış tutarı öncelikle baz para birimine dönüştürülür (dönüştürme 1).</li>
><li> Baz para birimi cinsinden tahmini satış tutarı, proje maliyeti para birimine dönüştürülür (dönüştürme 2). </li>
></ol>
></ol>
> Para birimi duyarlığı her iki adımda da uygulanır, bu da sözleşme para biriminde planlanan satışlardan alınan proje para birimindeki planlı gelirde sapmaya neden olur.
   

## <a name="reprojecting-revenues-on-leaf-node-tasks"></a>Yaprak düğüm görevlerinde gelirleri yeniden tahmin etme

Bir yaprak düğümü görevindeki işçilik gelirleri, **Proje sayfasındaki** **İzleme** sekmesinde doğrudan yeniden tahmin edilemez. Ancak, görevdeki kalan çalışmayı yeniden hesaplamak için **Çalışma İzleme** görünümünü kullanabilirsiniz. Bunu yaptığınızda, görevdeki kalan gelir yeniden hesaplanır. Aşağıda, bunun nasıl çalıştığı açıklanmıştır.

1. Proje yöneticileri, **Kalan Çalışma** alanındaki varsayılan değeri görevdeki kalan çalışmanın yeni tahminiyle güncelleştirerek görevdeki çalışmaları yeniden tahmin edebilir. Yeniden tahmin etme, görevin tahmini tamamlanma (EAC) çalışmasının ilerleme yüzdesinin ve görevdeki tahmin edilen çalışma değişikliğinin yeniden hesaplanmasına neden olur. EAC, tahmini tamamlanma süresi (ETC) ve özet görevlerindeki ilerleme durumu yüzdesi de yeniden hesaplanır ve yeni bir çalışma farkı tahmini oluşturulur.
2. Görevdeki kalan çalışma için yeni değere dayalı olarak sistem, **Gelir İzleme** görünümünde kalan geliri hesaplar. Kalan çalışmaya dayanan kalan geliri hesaplamak için sistem, ilk olarak özet görevinde planlanan gelir veya planlanan çalışma olarak bir saatlik çalışmanın ortalama gelirini hesaplar. Planlanan gelir, görevdeki tüm kaynak atamalarının gelirinin toplamıdır. Saat başına ortalama gelir, görevdeki yeni tahmini kalan çalışma için kalan geliri hesaplamak amacıyla kullanılır.
3. Yaprak düğümü görevdeki tahmini sonuç geliri ve gelir tüketimi yüzdesi yeniden hesaplanır.
4. Özet görevlerden kök düğümlere kadar tüm tamamlanma geliri değeri yeniden hesaplanır.

## <a name="reprojecting-revenues-on-summary-tasks"></a>Özet görevlerinde gelirlerini yeniden tahmin etme

İşçilik gelirlerini özet görevlerinde veya konteyner görevlerinde yeniden tahmin edebilirsiniz. Ancak özet projesi görevindeki işçilik gelirleri, **Proje** sayfasındaki **İzleme** sekmesinde doğrudan yeniden tahmin edilemez. Yaprak düğüm görevlerinde olduğu gibi özet ve konteyner görevlerini yeniden hesaplarken **Çalışma İzleme** görünümü kullanılabilir. Bu görünümde, bir özet görevdeki kalan çalışmayı yeniden tahmin edebilirsiniz. Bu durumda, özet görevindeki kalan gelir de yeniden hesaplanır. Aşağıda, bunun nasıl çalıştığı açıklanmıştır.

1. Proje yöneticileri, **Kalan Çalışma** alanındaki varsayılan değeri görevdeki yeni **Kalan Çalışma** tahminiyle güncelleştirerek görevdeki çalışmaları yeniden tahmin edebilir. Yeniden tahmin etme, görevin tahmini tamamlanmasının (EAC) ilerleme yüzdesinin ve görevdeki tahmin edilen çalışma değişikliğinin yeniden hesaplanmasına neden olur. EAC, ETC ve özet görevlerindeki ilerleme durumu yüzdesi de yeniden hesaplanır ve yeni bir çalışma farkı projeksiyonu oluşturur.
2. Görevdeki **Kalan çalışma** alanındaki yeni değere dayalı olarak sistem, **Gelir İzleme** görünümünde kalan geliri hesaplar. Kalan çalışmaya dayanan kalan geliri hesaplamak için sistem, ilk olarak özet görevinde planlanan gelir veya planlanan çalışma olarak bir saatlik çalışmanın ortalama gelirini hesaplar. Planlanan gelir, görevdeki tüm kaynak atamalarının gelirinin toplamıdır. Bu saat başına ortalama gelir, görevdeki yeni tahmini kalan çalışmanın kalan gelirini hesaplamak amacıyla kullanılır.
3. Özet görevindeki tahmini sonuç geliri ve gelir tüketimi yüzdeleri yeniden hesaplanır.
4. Yeni tahmini sonuç geliri değeri alt öğe görevlerine, özgün planlanan gelirin görevde sahip olduğu oranda dağıtılır.
5. Tek tek her görevin yaprak düğüm görevlerine kadar yeni tahmini sonuç geliri hesaplanır. Bu değere bağlı olarak, yaprak düğümlere kadar alt görevlerin kalan geliri ve gelir tüketme yüzdesi tahmini sonuç geliri değerine dayaranarak yeniden hesaplanır. Bu, görevin gelir farkı için yeni bir tahminle sonuçlanır. 
6. Özet görevlerden kök düğümlere kadar tüm tamamlanma geliri değeri yeniden hesaplanır.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

