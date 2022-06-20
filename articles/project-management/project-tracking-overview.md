---
title: Proje çalışması izleme
description: Bu makalede, proje çabası ve ilerleme durumunun nasıl izleneceği hakkında bilgiler sağlanmaktadır.
author: ruhercul
ms.date: 02/15/2022
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: c41dbc138f6fc92a9586de173ba5dfc89c7e44e3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929284"
---
# <a name="project-effort-tracking"></a>Proje çalışması izleme

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Zamanlamaya göre ilerleme durumunun izlenmesi ihtiyacı endüstriye göre değişir. Bazı endüstriler ayrıntılı düzeyde; diğer endüstrilerse daha yüksek bir düzeyde izler. Bu makale, kuruluşunuzun gereksinimlerini karşılamak için nasıl zamanlanacağınızı gösterir.

## <a name="effort-tracking-view"></a>Çalışma izleme görünümü

**Çalışma izleme** görünümü, görevin planlanan çalışma saatlerini göreve harcanan gerçek çalışma saatleriyle karşılaştırarak görevlerin zamanlamadaki ilerlemelerini izler. Dynamics 365 Project Operations, izleme ölçümlerini hesaplamak için aşağıdaki formülleri kullanır:

- **İlerleme yüzdesi**: Bugüne kadar harcanan gerçek çalışma süresi ÷ Tahmini tamamlanma (EAC) 
- **Kalan Çalışma**: Tahmini tamamlanma çalışma – Bugüne kadar harcanan gerçek çalışma süresi 
- **EAC**: Kalan çalışma süresi + Bugüne kadar harcanan gerçek çalışma süresi 
- **Öngörülen çalışma farkı**: Planlanan çalışma süresi – EAC

Project Operations, görevdeki çalışma süresi farkının bir projeksiyonunu gösterir. EAC, planlanan çalışma süresinden daha fazlaysa görevin, başlangıçta planlanandan daha fazla zaman alacağı ve zamanlamanın gerisine düşeceği öngörülür. EAC, planlanan çalışma süresinden daha azsa görevin, başlangıçta planlanandan daha az zaman alacağı ve zamanlamanın önünde gideceği öngörülür.

## <a name="reprojecting-effort-on-leaf-node-tasks"></a>Yaprak düğüm görevlerinde çalışmayı yeniden tahmin etme

Proje yöneticileri genellikle bir görevdeki özgün tahminleri düzeltir. Projelerin tekrar tasarımları, proje yöneticisinin projenin mevcut durumunu göz önüne aldığı tahmin algısıdır. Ancak, proje yöneticilerinin planlanan çalışma rakamlarını değiştirmesini önermeyiz. Bunun nedeni, proje planlanan çalışmanın proje zamanlaması ve maliyet tahmini için kurulu kaynağı yansıtması ve tüm proje hissedarlarının bu konuda anlaşmış olmasıdır.

Proje yöneticileri, görevlerin çalışmasını, **Kalan Çalışma** varsayılan değerini görevde yeni bir tahminle güncelleştirerek yeniden tahmin edebilir. Bu güncelleştirme, görevin tahmini tamamlanma (EAC) çalışmasının ilerleme yüzdesinin ve görevdeki tahmin edilen çalışma değişikliğinin yeniden hesaplanmasına neden olur. EAC, ETC ve özet görevlerindeki ilerleme durumu yüzdesi de yeniden hesaplanır ve yeni bir çalışma farkı projeksiyonu oluşturur.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Özet görevlerde çalışmanın yeniden tasarlanması

Özet veya kapsayıcı görevlerdeki çalışmalar yeniden tasarlanabilir. Proje yöneticileri, özet görevlerde kalan çalışmayı güncelleştirebilir. Kalan çalışmanın güncelleştirilmesi, uygulamada aşağıdaki hesaplamaların yapılmasına neden olur:

- Görevdeki EAC ve ilerleme durumu yüzdesi hesaplanır.
- Yeni EAC alt öğe görevlerine, özgün EAC'nin görevde sahip olduğu oranda dağıtılır.
- Tek tek her görevin yaprak düğüm görevlerine kadar yeni EAC'si hesaplanır. 
- Yaprak düğümlerine kadar etkilenen alt öğe görevleri kalan çalışma değerlerine sahiptir ve ilerleme durumu yüzdesi, EAC değerine göre yeniden hesaplanır. Bu, görevin çalışma farkı için yeni bir projeksiyonla sonuçlanır. 
- Özet görevlerden kök düğümlere kadar tüm EAC'ler yeniden hesaplanır.
- Özet görevde onaylanan çalışma, tüm alt görevlerde onaylanan çalışma ile özet görevde onaylanan çalışmanın toplanmasıyla elde edilir.
- Özet görevde kalan çalışma, tüm alt görevlerde kalan çalışmadan özet görevde onaylanan çalışmanın çıkarılmasıyla elde edilir.

## <a name="project-status-summary"></a>Proje durumu özeti

**Çalışma İzleme** ve **Maliyet izleme** görünümlerindeki verileri izleme proje kök düğümü, özet görevleri ve yaprak düğümü görevleri düzeylerindeki ilerleme durumunu ve maliyet tüketimini gösterir. **Proje varlığı** sayfasındaki **Durum** bölümü, proje düzeyi durumunun bir özetini gösterir.

## <a name="status-summary-fields"></a>Durum özeti alanları

İlk olarak **Genel proje durumu** alanı, projenin genel durumunu gösteren düzenlenebilir bir alandır. Artan riski göstermek için yeşil, sarı ve kırmızı gibi renk kodlaması kullanır. İkinci olarak **Yorumlar** alanı, proje yöneticisinin durumla ilgili belirli yorumlar girmesini sağlar. **Durum güncelleştirme tarihi** alanı düzenlenemez ve değer, durumun en son güncelleştirildiği tarihi gösteren bir zaman damgasıdır.

**Zamanlama performansı** ve **Maliyet performansı** alanları izleme tarihinden itibaren ayarlanır. **Çalışma izleme** görünümündeki kök düğümün zamanlama ve maliyet farkı pozitif olduğunda bu alanları **İleride** olarak ayarlayabilirsiniz. Kök düğümün zamanlama ve maliyet farkı negatif olduğunda bunları **Geride** olarak ayarlayabilirsiniz.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
