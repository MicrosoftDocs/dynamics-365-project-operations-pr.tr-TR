---
title: Proje ilerleme durumu ve maliyet tüketimi
description: Bu konu, proje ilerleme durumu ve maliyet tüketiminin nasıl izleneceği hakkında bilgi sağlar.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756694"
---
# <a name="project-progress-and-cost-consumption"></a>Proje ilerleme durumu ve maliyet tüketimi

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Zamanlamaya göre ilerleme durumunun izlenmesi ihtiyacı endüstriye göre değişir. Bazı endüstriler ayrıntılı düzeyde; diğer endüstrilerse daha yüksek bir düzeyde izler. Bu konu, kuruluşunuzun gereksinimlerini karşılamak için nasıl zamanlanacağınızı gösterir.

## <a name="effort-tracking-view"></a>Çalışma izleme görünümü

**Çalışma İzleme** görünümü zamanlamadaki görevlerin ilerleme durumunu izler. Bu, bir görev için planlanan çalışma saatlerini görev için harcanan gerçek çalışma saatleriyle kıyaslar. PSA, izleme ölçümlerini hesaplamak için aşağıdaki formülleri kullanır:

- İlerleme yüzdesi = Bugüne kadar harcanan gerçek çalışma süresi ÷ Görev için planlanan çalışma süresi 
- Tahmini tamamlanma zamanı (ETC) = Planlanan çalışma süresi – Bugüne kadar harcanan gerçek çalışma süresi 
- Tahmini tamamlanma zamanı (EAC) = Kalan çalışma süresi + Bugüne kadar harcanan gerçek çalışma süresi 
- Öngörülen çalışma farkı = Planlanan çalışma süresi – EAC

PSA, görevdeki çalışma süresi farkının bir projeksiyonunu gösterir. EAC planlanan çalışma süresinden daha fazlaysa görevin başlangıçta planlanandan daha fazla zaman alacağı öngörülmektedir. Bu nedenle, zamanlamanın gerisindedir. EAC planlanan çalışma süresinden daha az ise görevin başlangıçta planlanandan daha az zaman alacağı öngörülmektedir. Bu nedenle, zamanlamanın ilerisindedir.

## <a name="re-projecting-effort"></a>Çalışmayı yeniden tasarlama

Proje yöneticisinin bir görevdeki özgün tahminleri düzeltmesi yaygın bir uygulamadır. Projelerin tekrar tasarımları, proje yöneticisinin projenin mevcut durumunu göz önüne aldığı tahmin algısıdır. Bununla birlikte, proje yöneticilerinin taban sayılarını değiştirmelerini tavsiye etmeyiz çünkü proje tabanı, projedeki tüm paydaşların kabul ettiği projenin zamanlamasının ve maliyetlerin belirlenmiş tahmini için gerçeğin kaynağıdır.

Proje yöneticisinin görevlerdeki çalışmayı yeniden tasarlamasının iki yolu vardır:

- Görevdeki gerçek kalan çalışmanın yeni bir tahminiyle varsayılan ETC'yi geçersiz kılın. 
- Görevdeki gerçek ilerleme durumunun yeni bir tahminiyle varsayılan ilerleme durumu yüzdesini geçersiz kılın.

Bu yaklaşımların her biri görevin ETC, EAC ve ilerleme durumu yüzdesinin yeniden hesaplanmasına ve bir görevde öngörülen çalışma farkına neden olur. EAC, ETC ve özet görevlerindeki ilerleme durumu yüzdesi de yeniden hesaplanır ve yeni bir çalışma farkı projeksiyonu oluşturur.

## <a name="re-projection-of-effort-on-summary-tasks"></a>Özet görevlerde çalışmanın yeniden tasarlanması

Özet veya kapsayıcı görevlerdeki çalışmalar yeniden tasarlanabilir. Kullanıcının, özet görevlerdeki kalan çalışma değerini veya ilerleme durumu yüzdesini kullanarak yeniden tasarım yapmasından bağımsız olarak aşağıdaki hesaplamalar başlar:

- Görevdeki EAC, ETC. ve ilerleme durumu yüzdesi hesaplanır.
- Yeni EAC alt öğe görevlerine, özgün EAC'nin görevde sahip olduğu oranda dağıtılır.
- Tek tek her görevin yaprak düğüm görevlerine kadar yeni EAC'si hesaplanır. 
- Yaprak düğümlerine kadar etkilenen alt öğe görevleri ETC değerlerine sahiptir ve ilerleme durumu yüzdesi, EAC değerine göre yeniden hesaplanır. Bu, görevin çalışma farkı için yeni bir projeksiyonla sonuçlanır. 
- Özet görevlerden kök düğümlere kadar tüm EAC'ler yeniden hesaplanır.

### <a name="cost-tracking-view"></a>Maliyet izleme görünümü 

**Maliyet izleme** görünümü bir göreve harcanan gerçek maliyeti, bir görevin planlanan maliyetiyle karşılaştırır. 

> [!NOTE]
> Bu görünüm yalnızca işçilik maliyetlerini gösterir ve gider tahminlerindeki maliyetleri içermez. 

PSA, izleme ölçümlerini hesaplamak için aşağıdaki formülleri kullanır:

- Tüketilen maliyetin yüzdesi = Bugüne kadar harcanan gerçek maliyet ÷ Görev için planlanan maliyet
- Tamamlamak için gereken maliyet (CTC) = Planlanan maliyet – Bugüne kadar harcanan gerçek maliyet
- EAC = CTC + Bugüne kadar harcanan gerçek maliyet
- Öngörülen maliyet farkı = Planlanan maliyet – EAC

Görevdeki maliyet farkının bir projeksiyonu gösterilir. EAC, planlanan maliyetten daha fazlaysa görevin başlangıçta planlanandan daha maliyetli olacağı öngörülür. Bu nedenle, bütçe üzerinde bir trende sahiptir. EAC, planlanan maliyetten daha azsa görevin başlangıçta planlanandan daha az maliyetli olacağı öngörülmektedir. Bu nedenle, bütçe altında bir trende sahiptir.

## <a name="project-managers-re-projection-of-cost"></a>Proje yöneticisinin maliyeti yeniden tasarlaması

Çalışma yeniden tasarlandığında CTC, EAC, tüketilen maliyet yüzdesi ve öngörülen maliyet farkı **Maliyet izleme** görünümünde yeniden hesaplanır.

## <a name="project-status-summary"></a>Proje durumu özeti

**Çalışma İzleme** ve **Maliyet izleme** görünümlerindeki verileri izleme proje kök düğümü, özet görevleri ve yaprak düğümü görevleri düzeylerindeki ilerleme durumunu ve maliyet tüketimini gösterir. **Proje varlığı** sayfasındaki **Durum** bölümü, proje düzeyi durumunun bir özetini gösterir.

## <a name="status-summary-fields"></a>Durum özeti alanları

**Genel proje durumu** alanı, projenin genel durumunu gösteren düzenlenebilir bir alandır. Artan riski göstermek için yeşil, sarı ve kırmızı gibi renk kodlaması kullanır. **Yorumlar** alanı, proje yöneticisinin durumla ilgili belirli yorumlar girmesini sağlar. **Durum güncelleştirme tarihi** alanı düzenlenemez ve değer, durumun en son güncelleştirildiği tarihi gösteren bir zaman damgasıdır.

**Zamanlama performansı** ve **Maliyet performansı** alanları izleme tarihinden itibaren ayarlanır. **Çalışma izleme** görünümündeki kök düğümün zamanlama ve maliyet farkı pozitif olduğunda bu alanları **İleride** olarak ayarlayabilirsiniz. Kök düğümün zamanlama ve maliyet farkı negatif olduğunda bunları **Geride** olarak ayarlayabilirsiniz.
