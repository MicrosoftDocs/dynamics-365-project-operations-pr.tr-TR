---
title: Proje aşamaları türleri
description: Bu konu proje aşamaları hakkında bilgi sağlar.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: e4f50d12b4f0bf1586d0a5702bcd38b891590bffe0d3f9661d7f5d170877b54e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996910"
---
# <a name="project-stage-types"></a>Proje aşamaları türleri 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Proje aşamaları, proje ilerledikçe projenin durumunu gösterecek şekilde tasarlanır. Özelleştirmeler, iş süreci akışları, Power Automate veya eklenti uzantıları olan aşamaları otomatik olarak güncelleştirmek için kullanılabilir.

Varsayılan BPF'de aşağıdaki aşamalar tanımlanmıştır:

- Yeni
- Teklif
- Plan
- Teslim Et
- Tamamla
- Kapat 

## <a name="new"></a>Yeni

Bir proje oluşturduğunuzda, proje aşaması **Yeni** olarak ayarlanır. Proje bir şablondan oluşturulmuşsa zamanlaması, tahmini ve takım verileri olabilir. Aksi takdirde bu sadece projenin ana hatlarıdır ve kalan bileşenler girilmelidir.

## <a name="quote"></a>Teklif

Bir projeyi teklifle ilişkilendirdiğinizde veya tekliften oluşturduğunuzda, proje aşaması **Teklif** olarak ayarlanır ve tahmini başlangıç ve bitiş tarihleri güncelleştirilir. Proje **Teklif** aşamasındayken **Proje Varlığı** sayfasındaki **Satış** sekmesi teklifin ayrıntılarını gösterir.

## <a name="plan"></a>Plan

Bir proje ile ilişkili bir teklif kazandığınızda ve proje **Sözleşme** aşamasına taşındığında, proje aşaması **Plan** olarak güncelleştirilir. Proje **Plan** aşamasındayken **Proje Varlığı** sayfası sözleşmenin ayrıntılarını gösterir.

## <a name="deliver"></a>Teslim Et

Proje planı tamamlandığında ve projeyi başlatmaya hazır olduğunuzda, proje yöneticisi projenin başladığını göstermek için proje aşamasını **Teslim Et** olarak güncelleştirmelidir.

## <a name="complete"></a>Tamamla 

Proje için çalışmalar tamamlandığında, proje yöneticisi aşamayı **Tamamla** olarak güncelleştirebilir. Proje aşamasını **Tamamla** olarak güncelleştirerek, proje yöneticisi çalışmanın yüzde 100 oranında tamamlandığını ancak herhangi bir bekleme süresi veya gider girişinin kaydedilebilmesi için projenin açık tutulduğunu gösterir.

## <a name="close"></a>Kapat

Tüm işlemler kaydedildiğinde proje yöneticisi aşamayı **Kapat** olarak güncelleştirebilir. Bu noktada hiçbir işlem kaydedilemez ve proje salt okunur olarak ayarlanır.


[!INCLUDE[footer-include](../includes/footer-banner.md)]