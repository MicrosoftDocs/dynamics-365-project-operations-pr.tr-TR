---
title: İşçilik ve giderlere yönelik standart maliyetleri yapılandırma
description: Bu konuda, bir projenin işçilik ve giderleri için standart maliyetlerin nasıl ayarlanacağını açıklanır.
author: KimANelson
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.assetid: fa7c024f-4b18-4d29-9fd4-9c430cd83fad
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f3e796cc03aeaa28938c56ce37d5075755248dfa
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756727"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a>İşçilik ve giderlere yönelik standart maliyetleri yapılandırma

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu konuda, bir projenin işçilik ve giderleri için standart maliyetlerin nasıl ayarlanacağını açıklanır. Bu görevde USSI veri kümesi kullanılır.

1. Gezinti bölmesinde, **Modüller > Proje yönetimi ve muhasebe > Kurulum > Fiyatlar > Maliyet fiyatı (saat)** modülüne gidin.
2. **Yeni**'yi seçin.
3. **Yürürlük tarihi** alanına bir tarih girin.
4. **Maliyet fiyatı** alanına bir sayı girin. Proje kategorisi için standart bir maliyet fiyatı ayarlayabilir veya bir maliyet fiyatını çalışan numarasına, proje numarasına, kategoriye, tarihe veya bunların herhangi bir birleşimine göre ayarlayabilirsiniz. Uygulanan maliyet fiyatı, en yüksek ayrıntı düzeyini içeren maliyet fiyatıdır.  
5. **Kaydet**'i seçin.
6. Gezinti bölmesinde, **Modüller > Proje yönetimi ve muhasebe > Kurulum > Fiyatlar > Satış fiyatı (saat)** modülüne gidin.
7. **Yeni**'yi seçin.
8. **Yürürlük tarihi** alanına bir tarih girin.
9. **Geçerlilik:** alanından bir seçenek belirleyin.
10. **Fiyat** alanına bir sayı girin. Saatlik hareketler için veya bir proje kategorisi için standart satış fiyatı ayarlayabilirsiniz. Ayrıca, satış fiyatlarını çalışan numarasına, proje numarasına, kategoriye, hareket tarihine veya bunların herhangi bir birleşimine göre de ayarlayabilirsiniz. Bir çalışan Saat günlüğüne bir hareket girdiğinde uygulanan gerçek satış fiyatı, en yüksek ayrıntı düzeyini içeren satış fiyatıdır. Örneğin, hem genel satış fiyatı, hem de çalışana özgü satış fiyatı ayarlandıysa, çalışana özgü satış fiyatı kullanılır.  
11. **Kaydet**'i seçin.
12. Sayfayı kapatın.
13. Gezinti bölmesinde, **Modüller > Proje yönetimi ve muhasebe > Kurulum > Fiyatlar > Maliyet fiyatı (gider)** modülüne gidin.
14. **Yeni**'yi seçin.
15. **Yürürlük tarihi** alanına bir tarih girin.
16. **Maliyet fiyatı** alanına bir sayı girin. Birden çok alan doldurulabilir; ancak bu, kaydın yapılması için gereken en düşük gereksinimdir.  
17. **Kaydet**'i seçin.
18. Gezinti bölmesinde, **Modüller > Proje yönetimi ve muhasebe > Kurulum > Fiyatlar > Satış fiyatı (gider)** modülüne gidin.
19. **Yeni**'yi seçin.
20. **Yürürlük tarihi** alanına bir tarih girin.
21. **Geçerlilik:** alanından bir seçenek belirleyin.
22. **Fiyat** alanına bir sayı girin. Bir çalışan gider günlüğüne hareketleri girdiğinde uygulanan gerçek satış fiyatı, en yüksek ayrıntı düzeyini içeren satış fiyatıdır. Örneğin, hem genel, hem de çalışana özgü satış fiyatı ayarlandıysa, çalışana özgü satış fiyatı kullanılır.  
23. **Kaydet**'i seçin.

