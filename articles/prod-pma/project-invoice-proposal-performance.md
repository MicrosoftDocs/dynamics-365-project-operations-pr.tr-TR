---
title: Proje faturası teklif performansı
description: Bu konu, proje fatura tekliflerinde performans iyileştirmeleri hakkında bilgi sağlar.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: johnmichalak
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: e707b0d9b379df59726271b5a0441ac04e269b9a
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683470"
---
# <a name="project-invoice-proposal-performance"></a>Proje faturası teklif performansı

[!include [banner](../includes/banner.md)]

Yeni bir fatura teklifi oluşturduğunuzda, proje ve alt projelerin sayısı yükseldiğinden performans sorunlarıyla karşılaşabilirsiniz. Performansı iyileştirmek amacıyla deftere nakledilen proje hareketleri için yeni bir fatura teklifi oluşturmak için gereken süreyi azaltan bir özellik vardır.

## <a name="enable-project-invoice-proposal-performance-enhancement"></a>Proje faturası teklifi performansını iyileştirmeyi etkinleştirme
Proje faturası teklifi performansını iyileştirme özelliğini etkinleştirmek için aşağıdaki adımları izleyin.

1.  **Özellik yönetimi** > **Tümü**'ne gidin. Özellik listesinde, **Proje fatura tekliflerinde performans iyileştirmesi** seçeneğini bulun.
2.  **Şİmdi Etkinleştir**'i seçin.
3.  Tarayıcınızı yenileyin ve ardından yeni bir fatura teklifi oluşturun.

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a>Proje faturası teklifi performansını iyileştirmeyi devre dışı bırakın
Proje faturası teklifi performansını iyileştirme özelliğini devre dışı bırakmak için aşağıdaki adımları tamamlayın.

1.  **Özellik yönetimi** > **Tümü**'ne gidin. Özellik listesinde, **Proje fatura tekliflerinde performans iyileştirmesi** seçeneğini bulun.
2.  **Devre Dışı Bırak**'ı seçin.
3.  Tarayıcınızı yenileyin.

> [!NOTE]
> Faturalama kuralları etkinleştirildiğinde fatura teklifi performansı uygulanamaz.
> 
> Fatura teklifleri oluşturma toplu işlemi sırasında, alt görev sayısı ne girdiğinize bakılmaksızın, faturalanabilir işlemlere sahip sözleşmelerin sayısına bağlı olarak görevleri maksimum sayıya böler. Örneğin, toplu işle fatura teklifi oluşturma alt görev sayısı için **3** ve faturalanabilir işlemlere sahip yalnızca iki sözleşme varsa, yalnızca iki alt görev oluşturulur.
