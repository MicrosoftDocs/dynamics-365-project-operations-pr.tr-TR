---
title: Proje görevlerini Project Service Automation uygulamasından Finance and Operations uygulamasına doğrudan eşitleme
description: Bu konuda, proje görevlerini Microsoft Dynamics 365 Project Service Automation uygulamasından Dynamics 365 Finance uygulamasına doğrudan eşitlemek için kullanılan şablon ve temel görev açıklanır.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: d7f32327-33c4-43ab-b799-786210e93277
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 66a255346727c7ee4fbbf2920d2ef437ded03308
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756700"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Proje görevlerini Project Service Automation uygulamasından Finance and Operations uygulamasına doğrudan eşitleme

[!include[banner](../includes/banner.md)]

Bu konuda, proje görevlerini Dynamics 365 Project Service Automation uygulamasından Dynamics 365 Finance uygulamasına doğrudan eşitlemek için kullanılan şablon ve temel görev açıklanır.

> [!NOTE]
> - 8.0 sürümünde proje görev tümleştirmesini, harcama hareketi kategorilerini, saat tahminlerini, masraf tahminlerini ve işlevsellik kilitlemeyi kullanabilirsiniz.
> - Enterprise Edition 7.3.0 kullanıyorsanız, KB 4132657 ve KB 4132660 yükledikten sonra, proje görevlerini, gider hareketi kategorilerini, saat tahminlerini, masraf tahminlerini ve gerçek değerleri tümleştirmek ve işlevsellik kilitlemeyi yapılandırmak için şablonları kullanabilirsiniz. Muhasebe dağıtımlarını sıfırlamanız gerekiyorsa, KB 4131710'u da yüklemenizi öneririz.
> - Gerçek değerler tümleştirmesi sürüm 8.0.1 veya daha sonraki sürümlerde kullanılabilir.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Project Service Automation ile Finance tümleştirmesi için veri akışı

Project Service Automation ile Finance tümleştirme çözümünde Project Service Automation ile Finance örnekleri arasında verinin eşitlenmesini sağlayan Veri tümleştirme özelliği kullanılır. Veri tümleştirme özelliğiyle kullanılabilen tümleştirme şablonu, proje görevleri ile ilgili verilerin Project Service Automation uygulamasından Finance uygulamasına akışını sağlar.

Aşağıdaki şekilde Project Service Automation ve Finance arasındaki tümleştirmenin bir parçası olarak verilerin nasıl eşitleneceğini gösterilir.

[![Finance ile Project Service Automation tümleştirmesi için veri akışı](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Şablon ve görev

Şablona erişmek için, Microsoft Power Apps Yönetim Merkezi'nde, **Projeler**'i seçin ve ardından sağ üst köşeden, ortak şablonları seçmek için **Yeni proje**'yi seçin.

Project Service Automation uygulamasından Finance uygulamasına proje görevlerini eşitlemek için şu şablon ve temel görev kullanılır:

- **Veri tümleştirmedeki şablonun adı:** Proje görevleri (PSA'dan Fin and Ops'a)
- **Projedeki görevin adı:** Proje görevleri

Proje görevlerinin eşitlenmesi gerçekleştirilmeden önce proje sözleşmelerini ve projeleri eşitlemeniz gerekir.

## <a name="entity-set"></a>Varlık kümesi

| Project Service Automation | Finans                             |
|----------------------------|-------------------------------------|
| Proje Görevleri              | Proje göreviyle ilgili tümleştirme varlığı |

## <a name="entity-flow"></a>Varlık akışı

Proje görevleri Project Service Automation uygulamasında yönetilir ve proje etkinlikleri olarak Finance ile eşitlenir.

## <a name="prerequisites-and-mapping-setup"></a>Ön koşullar ve eşleme ayarı

Proje görevlerinin eşitlenmesi gerçekleştirilmeden önce proje sözleşmelerini ve projeleri eşitlemeniz gerekir.

## <a name="power-query"></a>Power Query

Bu koşulun karşılanması durumunda verileri filtrelemek için Excel'de Microsoft Power Query kullanmanız gerekir:

- Bir proje görevinde kaynağa özgü kayıtlarınız vardır.

Power Query kullanmanız gerekiyorsa aşağıdaki kılavuzu izleyin:

- Proje görevleri (PSA'dan Fin and Ops'a) şablonunda, **IsLineTask** filtresini **False** değeri olarak ayarlayarak proje görevinden kaynağa özgü kayıtları dışarıda bırakan varsayılan bir filtre vardır. Kendi şablonunuzu oluşturursanız, bu filtreyi eklemeniz gerekir.

## <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşlemesi

Aşağıdaki çizimde veri tümleştirmede şablon görev eşlemelerinin bir örneği gösterilmektedir. Eşleme, Project Service Automation'dan Finance'e eşitlenecek alan bilgilerini gösterir.

[![Şablon eşlemesi](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)
