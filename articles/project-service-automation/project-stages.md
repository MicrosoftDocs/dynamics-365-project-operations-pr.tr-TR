---
title: Proje aşamaları
description: Bu konu proje aşamaları hakkında bilgi sağlar.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 983c25a0-ed21-4151-a109-b385a88285fa
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 70aa057e127df7ba925e84f5d056a06a4cc8833e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756610"
---
# <a name="project-stages"></a>Proje aşamaları 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Proje aşamaları, proje ilerledikçe projenin durumunu gösterecek şekilde güncelleştirilir. Varsayılan iş süreci akışı, projenin bazı aşamalarını otomatik olarak güncelleştirirken diğerleri proje yöneticisi tarafından el ile güncelleştirilir. 

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
