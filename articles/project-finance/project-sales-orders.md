---
title: Zaman ve malzeme projeleri için proje satış siparişleri
description: Bu konuda, zaman ve malzeme projeleri için proje tabanlı satış siparişlerinin nasıl oluşturulacağı açıklanmaktadır.
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 05ab0cf6-318c-42de-ba56-3e662283497e
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 446c73e9491b1892847caf7e843c802292107ef9
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756590"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Zaman ve malzeme projeleri için proje satış siparişleri

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Bu konuda bir proje için satış siparişinin nasıl oluşturulacağı açıklanır. Satış siparişleri yalnızca **zaman ve malzeme** türünde projeler için oluşturulabilir.

Bir zaman ve malzeme projesinin proje sözleşmesi üzerinde birden çok finansman kaynağı varsa, **Proje yönetimi ve muhasebe parametreleri** sayfasından **Birden finansman kaynağı bulunan projelerin satış siparişlerine izin ver** parametresini etkinleştirmeniz gerekir. 

> [!NOTE]
> - Birden çok finansman kaynağı bulunan proje satış siparişleri için destek, 10.0.2 uygulama sürümü ve sonraki sürümlerden başlayacak şekilde kullanılabilir.
> - Birden çok finansman kaynağı içeren proje satış siparişlerine yönelik desteği etkinleştiren parametre, 2020 yayın dalgasından sonra kaldırılmıştır ve bu tarihten sonra işlev sürekli etkinleştirilmiştir.

Proje tabanlı satış siparişlerini iki şekilde oluşturabilirsiniz:

- Projenin kendisine gidin. Eylem Bölmesi'nde, **Yönet > Madde görevleri > Satış siparişi** seçeneğini belirleyin. Proje bilgileri varsayılan olarak projede bulunan satış siparişinde kullanılır. Proje sözleşmesinde birden çok finansman kaynağı varsa, satış siparişinin ait olduğu müşteriyi ayarlamak üzere finansman kaynağını seçmeniz gerekir. Proje için yalnızca bir finansman kaynağı varsa, müşteri otomatik olarak ayarlanır.
- **Tüm satış sipariş** listesi sayfasına gidin ve yeni bir satış siparişi oluşturun. Satış siparişi için projeyi seçmeniz gerekir. Proje seçildikten sonra, müşteri finansman kaynağından ayarlanır veya proje sözleşmesinde birden çok finansman kaynağı varsa, finansman kaynağını seçmeniz gerekir.

