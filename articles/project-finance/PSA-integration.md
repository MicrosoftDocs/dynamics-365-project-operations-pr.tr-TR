---
title: Project Service Automation'a genel bakış
description: Bu konuda, Dynamics 365 Project Service Automation ile Dynamics 365 Finance arasındaki tümleştirme çözümü hakkında bilgi sağlanır.
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 897e1a1c-d31c-42b8-bb59-6b67202d8d61
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 080a545d8713e52d9778367aec1969b815d683e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756658"
---
# <a name="project-service-automation-overview"></a>Project Service Automation'a genel bakış

[!include[banner](../includes/banner.md)]

Finance için Project Service Automation tümleştirme çözümünde Common Data Service üzerinden Dynamics 365 Finance ve Dynamics 365 Project Service Automation örneği arasında verinin eşitlenmesini sağlayan Veri tümleştirme özelliği kullanılır. Veri tümleştirme özelliğiyle kullanılabilen tümleştirme şablonları, Project Service Automation'dan Finance'e projelerin, proje sözleşmelerinin, proje sözleşme satırlarının, proje sözleşme satırı kilometre taşlarının, proje görevlerinin, masraf hareketi kategorilerinin, saat tahminlerinin ve gider tahminlerinin akışını etkinleştirir.

> [!NOTE]
> - 7.3.0 sürümünü kullanıyorsanız, KB 4074835 yüklemelisiniz. Daha sonra sabit fiyatlı projeleri tümleştirebilirsiniz.
> - 7.3.0 sürümünü kullanıyorsanız ve Project Service Automation'dan ücret hareketleri alıyorsanız, bu ücretleri proje faturasına dahil etmek için KB 4345320 yüklemelisiniz.
> - 8.0 sürümünü kullanıyorsanız proje görev tümleştirmesini, harcama hareketi kategorilerini, saat tahminlerini, masraf tahminlerini ve işlevsellik kilitlemeyi kullanabilirsiniz.
> - Sürüm 8.0.1 veya sonrasını kullanıyorsanız, gerçek değerleri eşitleyebilirsiniz.

Project Service Automation Finance parametrelerini tümleştirebilmeniz için önce Project Service Automation tümleştirme parametrelerini yapılandırmanız gerekir. Daha fazla bilgi için bkz. [Project Service Automation tümleştirme parametreleri](PSA-parameters.md).

Bu tümleştirme çözümü, aşağıdaki senaryolarda doğrudan eşitlemeyi sağlar:

- Project Service Automation'da proje sözleşmelerini koruyun ve bunları doğrudan Project Service Automation'dan Finance'e eşitleyin.
- Project Service Automation'da projeler oluşturun ve bunları doğrudan Project Service Automation'dan Finance'e eşitleyin.
- Project Service Automation'da proje sözleşme satırlarını koruyun ve bunları doğrudan Project Service Automation'dan Finance'e eşitleyin.
- Project Service Automation'da proje sözleşme satırları kilometre taşlarını koruyun ve bunları doğrudan Project Service Automation'dan Finance'e eşitleyin.
- Project Service Automation'da proje görevlerini koruyun ve bunları doğrudan Project Service Automation'dan Finance'e eşitleyin.
- Finance'de gider hareketi kategorilerini koruyun ve bunları doğrudan Finance'den Project Service Automation'a eşitleyin.
- Project Service Automation'da proje saat tahminleri oluşturun ve bunları doğrudan Project Service Automation'dan Finance'e eşitleyin.
- Project Service Automation'da proje gider tahminleri oluşturun ve bunları doğrudan Project Service Automation'dan Finance'e eşitleyin.
- Project Service Automation'da proje saati, masraf ve ücret fiili değerlerini oluşturun ve Project Service Automation tümleştirme günlüğünde proje harekelerini oluşturun. Böylece bu değerler Finance'de deftere nakledilebilir.

## <a name="data-synchronization"></a>Veri eşitleme

Aşağıdaki şekilde Project Service Automation ve Finance arasındaki tümleştirmenin bir parçası olarak verilerin nasıl eşitleneceğini gösterilir.

> [!NOTE]
> Tüm şablonlar şu anda kullanılabilir değil. Şablonlar tamamlandıklarında yayınlanacaktır.

[![Finance ile Project Service Automation tümleştirmesi](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>Finance için sistem gereksinimleri

Project Service Automation ile Finance tümleştirmesi çözümünü kullanmak için, Platform güncelleştirmesi 12 ve sonrası ile birlikte Enterprise Edition 7.3 uygulamasını yüklemelisiniz.

## <a name="system-requirements-for-project-service-automation"></a>Project Service Automation için sistem gereksinimleri

Project Service Automation ile Finance arasındaki tümleştirmesi çözümünü kullanmak için aşağıdaki bileşenleri yüklemelisiniz:

- Dynamics 365 Project Service Automation sürüm 9.0.0.0 veya üstü
- Dynamics 365 Sales, sürüm 1.14.0.0 (v14) veya sonraki sürümler için nakit potansiyeli çözümü
- Dynamics 365 Project Service Automation sürüm 1.0.0.0 veya üstü için Project Service Automation'dan Finance'e çözümü

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>Project Service Automation örneğinizde Project Service Automation'dan Finance'e tümleştirme çözümünü yükleme

Project Service Automation'dan Finance'e tümleştirme çözümünü [Microsoft Yükleme Merkezi](https://www.microsoft.com/download/details.aspx?id=57016)'nden indirin ve çözüme dahil edilen yönergeleri izleyin.
