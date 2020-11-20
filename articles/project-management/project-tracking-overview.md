---
title: Proje izlemeye genel bakış
description: Bu konuda, proje ilerleme durumu ve maliyet tüketiminin nasıl izleneceği hakkında bilgiler sağlanmaktadır.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: f159ecac53b824ef208221bb14958923fb5da63b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127397"
---
# <a name="project-tracking-overview"></a>Proje izlemeye genel bakış

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Zamanlamaya göre ilerleme durumunun izlenmesi ihtiyacı endüstriye göre değişir. Bazı endüstriler ayrıntılı düzeyde; diğer endüstrilerse daha yüksek bir düzeyde izler. Bu konu, kuruluşunuzun gereksinimlerini karşılamak için nasıl zamanlanacağınızı gösterir.

## <a name="effort-tracking-view"></a>Çalışma izleme görünümü

**Çalışma izleme** görünümü, görevin planlanan çalışma saatlerini göreve harcanan gerçek çalışma saatleriyle karşılaştırarak görevlerin zamanlamadaki ilerlemelerini izler. Dynamics 365 Project Operations, izleme ölçümlerini hesaplamak için aşağıdaki formülleri kullanır:

- **İlerleme yüzdesi**: Bugüne kadar harcanan gerçek çalışma süresi ÷ Tahmini tamamlanma (EAC) 
- **Tahmini tamamlanma zamanı (ETC)**: Planlanan çalışma süresi – Bugüne kadar harcanan gerçek çalışma süresi 
- **EAC**: Kalan çalışma süresi + Bugüne kadar harcanan gerçek çalışma süresi 
- **Öngörülen çalışma farkı**: Planlanan çalışma süresi – EAC

Project Operations, görevdeki çalışma süresi farkının bir projeksiyonunu gösterir. EAC, planlanan çalışma süresinden daha fazlaysa görevin, başlangıçta planlanandan daha fazla zaman alacağı ve zamanlamanın gerisine düşeceği öngörülür. EAC, planlanan çalışma süresinden daha azsa görevin, başlangıçta planlanandan daha az zaman alacağı ve zamanlamanın önünde gideceği öngörülür.

## <a name="reprojecting-effort"></a>Çalışmayı yeniden tasarlama

Proje yöneticileri genellikle bir görevdeki özgün tahminleri düzeltir. Projelerin tekrar tasarımları, proje yöneticisinin projenin mevcut durumunu göz önüne aldığı tahmin algısıdır. Bununla birlikte, proje yöneticilerinin taban sayılarını değiştirmelerini tavsiye etmeyiz. Bunun nedeni, proje tabanının, projedeki tüm paydaşların kabul ettiği proje zamanlamasının ve maliyetlerin belirlenmiş tahmini için doğru kaynağı temsil etmesidir.

Proje yöneticisinin görevlerdeki çalışmayı yeniden tasarlamasının iki yolu vardır:

- Görevdeki gerçek kalan çalışmanın yeni bir tahminiyle varsayılan ETC'yi geçersiz kılın. 
- Görevdeki gerçek ilerleme durumunun yeni bir tahminiyle varsayılan ilerleme durumu yüzdesini geçersiz kılın.

Her yaklaşım, görevin ETC, EAC ve ilerleme durumu yüzdesinin yeniden hesaplanmasına ve bir görevde öngörülen çalışma farkına neden olur. EAC, ETC ve özet görevlerindeki ilerleme durumu yüzdesi de yeniden hesaplanır ve yeni bir çalışma farkı projeksiyonu oluşturur.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Özet görevlerde çalışmanın yeniden tasarlanması

Özet veya kapsayıcı görevlerdeki çalışmalar yeniden tasarlanabilir. Kullanıcının, özet görevlerdeki kalan çalışma değerini veya ilerleme durumu yüzdesini kullanarak yeniden tasarım yapmasından bağımsız olarak aşağıdaki hesaplamalar başlar:

- Görevdeki EAC, ETC. ve ilerleme durumu yüzdesi hesaplanır.
- Yeni EAC alt öğe görevlerine, özgün EAC'nin görevde sahip olduğu oranda dağıtılır.
- Tek tek her görevin yaprak düğüm görevlerine kadar yeni EAC'si hesaplanır. 
- Yaprak düğümlerine kadar etkilenen alt öğe görevleri ETC değerlerine sahiptir ve ilerleme durumu yüzdesi, EAC değerine göre yeniden hesaplanır. Bu, görevin çalışma farkı için yeni bir projeksiyonla sonuçlanır. 
- Özet görevlerden kök düğümlere kadar tüm EAC'ler yeniden hesaplanır.

### <a name="cost-tracking-view"></a>Maliyet izleme görünümü 

**Maliyet izleme** görünümü bir göreve harcanan gerçek maliyeti, bir görevin planlanan maliyetiyle karşılaştırır. 

> [!NOTE]
> Bu görünüm yalnızca işçilik maliyetlerini gösterir ve gider tahminlerindeki maliyetleri içermez. Project Operations, izleme ölçümlerini hesaplamak için aşağıdaki formülleri kullanır:

- **Tüketilen maliyetin yüzdesi**: Bugüne kadar harcanan gerçek maliyet ÷ İş tamamlandığında tahmini maliyet
- **Tamamlamak için gereken maliyet (CTC)**: Planlanan maliyet – Bugüne kadar harcanan gerçek maliyet
- **EAC**: Kalan maliyet + Bugüne kadarki gerçek maliyet
- **Öngörülen maliyet farkı**: Planlanan maliyet – EAC

Görevdeki maliyet farkının bir projeksiyonu gösterilir. EAC, planlanan maliyetten daha fazlaysa görevin başlangıçta planlanandan daha maliyetli olacağı öngörülür. Bu nedenle, bütçe üzerinde bir trende sahiptir. EAC, planlanan maliyetten daha azsa görevin başlangıçta planlanandan daha az maliyetli olacağı öngörülmektedir. Bu nedenle, bütçe altında bir trende sahiptir.

## <a name="project-managers-reprojection-of-cost"></a>Proje yöneticisinin maliyeti yeniden tasarlaması

Çalışma yeniden tasarlandığında CTC, EAC, tüketilen maliyet yüzdesi ve öngörülen maliyet farkı **Maliyet izleme** görünümünde yeniden hesaplanır.

## <a name="project-status-summary"></a>Proje durumu özeti

**Çalışma İzleme** ve **Maliyet izleme** görünümlerindeki verileri izleme proje kök düğümü, özet görevleri ve yaprak düğümü görevleri düzeylerindeki ilerleme durumunu ve maliyet tüketimini gösterir. **Proje varlığı** sayfasındaki **Durum** bölümü, proje düzeyi durumunun bir özetini gösterir.

## <a name="status-summary-fields"></a>Durum özeti alanları

İlk olarak **Genel proje durumu** alanı, projenin genel durumunu gösteren düzenlenebilir bir alandır. Artan riski göstermek için yeşil, sarı ve kırmızı gibi renk kodlaması kullanır. İkinci olarak **Yorumlar** alanı, proje yöneticisinin durumla ilgili belirli yorumlar girmesini sağlar. **Durum güncelleştirme tarihi** alanı düzenlenemez ve değer, durumun en son güncelleştirildiği tarihi gösteren bir zaman damgasıdır.

**Zamanlama performansı** ve **Maliyet performansı** alanları izleme tarihinden itibaren ayarlanır. **Çalışma izleme** görünümündeki kök düğümün zamanlama ve maliyet farkı pozitif olduğunda bu alanları **İleride** olarak ayarlayabilirsiniz. Kök düğümün zamanlama ve maliyet farkı negatif olduğunda bunları **Geride** olarak ayarlayabilirsiniz.
