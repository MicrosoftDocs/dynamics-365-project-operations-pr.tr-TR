---
title: Proje aşamaları
description: Bu konu, Microsoft Dynamics Project Operations'da kullanılabilir olan proje aşamaları hakkında bilgiler sağlar.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: aa3d692a46165b01eafbd7619578cead8dd912d6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127497"
---
# <a name="project-stages"></a>Proje aşamaları

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Proje aşamaları, proje ilerledikçe projenin durumunu gösterecek şekilde tasarlanır. Özelleştirmeler, iş süreci akışları, Power Automate veya eklenti uzantıları olan aşamaları otomatik olarak güncelleştirmek için kullanılabilir.

Varsayılan iş süreci akışında aşağıdaki aşamalar tanımlanmıştır:

- Yeni
- Teklif
- Plan
- Teslim Et
- Tamamla
- Kapat 

## <a name="new"></a>Yeni

Bir proje oluşturduğunuzda, proje aşaması **Yeni** olarak ayarlanır. Proje bir şablondan oluşturulmuşsa zamanlaması, tahmini ve takım verileri olabilir. Aksi takdirde bu projenin ana hatlarıdır ve kalan bileşenler girilmelidir.

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

