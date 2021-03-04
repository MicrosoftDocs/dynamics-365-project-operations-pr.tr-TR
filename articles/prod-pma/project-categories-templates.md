---
title: Finance and Operations ve Project Service Automation arasında proje gideri kategorilerini eşitleme
description: Bu konuda, proje gider kategorilerini Microsoft Dynamics 365 Finance ile Dynamics 365 Project Service Automation uygulamaları arasında eşitlemek için kullanılan şablon ve temel görev açıklanır.
author: Yowelle
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
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: ed7ca3c85d3f99b7eefe10f4ddec822b9aeb1684
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086463"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Finance and Operations ve Project Service Automation arasında proje gideri kategorilerini eşitleme

[!include[banner](../includes/banner.md)]

Bu konuda, proje gider kategorilerini Dynamics 365 Finance ile Dynamics 365 Project Service Automation uygulamaları arasında eşitlemek için kullanılan şablon ve temel görev açıklanır.

> [!NOTE]
> - 8.0 sürümünde proje görev tümleştirmesini, harcama hareketi kategorilerini, saat tahminlerini, masraf tahminlerini ve işlevsellik kilitlemeyi kullanabilirsiniz.
> - Gerçek değerler tümleştirmesi sürüm 8.0.1 veya daha sonraki sürümlerde kullanılabilir.
> - Enterprise Edition 7.3.0 kullanıyorsanız, KB 4132657 ve KB 4132660 yükledikten sonra, proje görevlerini, gider hareketi kategorilerini, saat tahminlerini, masraf tahminlerini ve gerçek değerleri tümleştirmek ve işlevsellik kilitlemeyi yapılandırmak için şablonları kullanabilirsiniz. Muhasebe dağıtımlarını sıfırlamanız gerekiyorsa, KB 4131710'u da yüklemenizi öneririz.

## <a name="data-flow-for-project-service-automation-and-finance"></a>Project Service Automation ile Finance tümleştirmesi için veri akışı

Project Service Automation ile Finance tümleştirme çözümünde Project Service Automation ile Finance örnekleri arasında verinin eşitlenmesini sağlayan Veri tümleştirme özelliği kullanılır. Veri tümleştirme özelliğiyle kullanılabilen tümleştirme şablonu, proje gider hareketi kategorileri ile ilgili verilerin Project Service Automation ile Finance uygulamasının arasında akışını sağlar.

Proje gideri kategorilerine ait ana kopya Finance uygulamasında ise, tümleştirme akışı ilk olarak Finance'den Project Service Automation'a doğru olur. Daha sonra proje gideri kategorilerinin tümleştirme kimlikleri Project Service Automation'dan Finance'e doğru eşitleme yoluyla güncelleştirilir.

Proje gideri kategorilerine ait ana kopya Project Service Automation uygulamasında ise, tümleştirme akışı ilk olarak Project Service Automation'dan Finance'e doğru olur. Proje kategorileri, Project Service Automation'dan eşitlenmeden önce Finance içinde önceden yapılandırılmış olmalıdır. Finance'den Project Service Automation'a geri eşitledikten sonra Project Service Automation'dan Finance'e tekrar eşitleyin. Bu şekilde, kategorilerin bağlantılandırılmasını ve hiçbir yinelenen değerlerin oluşturulmamasını sağlamanıza yardımcı olur.

> [!NOTE]
> Genellikle, proje gideri kategorilerine ait ana kopya Finance uygulamasında bulunur. Ancak değillerse veya gider kategorileri zaten Project Service Automation'da oluşturulmuşsa, Proje gideri hareket kategorileri (PSA'dan Fin and Ops'a) şablonunu kullanarak eşitleme yapmanız gerekir. Ardından Proje gideri hareket kategorileri (Fin and Ops'dan PSA'ya) şablonunu kullanarak eşitleme yapın. Daha sonra, Project Service Automation'dan Finance'e bir kez daha eşitlemek için eşitlemeyi çalıştırmanız gerekir.
>
> Öncelikle Project Service Automation'dan eşitleme yaparsanız, eşitleme işlemi başlatılmadan önce Finance'de aşağıdaki gereksinimlerin karşılanması gerekir:
>
> - Project Service Automation'da ayarlanan proje kategorisiyle eşleşen paylaşılan kategorinin var olması ve hem **Proje** hem de **Gider** için etkinleştirilmesi gerekir.
> - Tümleştirilmesi gereken her yasal varlık için aşağıdaki proje kategorilerinin bulunması gerekir:
>
>     - **Proje kategorisi** var. 
>     - **Giderde Kullan** etkin.
>     - **Günlükte Etkin** ayarı etkin.
>     - **Hareket türü** **Gider** olarak ayarlanmış.

Aşağıdaki şekilde Project Service Automation ve Finance arasındaki tümleştirmenin bir parçası olarak verilerin nasıl eşitleneceğini gösterilir.

[![Finance ile Project Service Automation tümleştirmesi için veri akışı](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a>Finance'den Project Service Automation'a proje gideri kategorilerini eşitleme

### <a name="template-and-task"></a>Şablon ve görev

Şablona erişmek için, Microsoft Power Apps Yönetim Merkezi'nde, **Projeler** 'i seçin ve ardından sağ üst köşeden, ortak şablonları seçmek için **Yeni proje** 'yi seçin.

Project Service Automation uygulamasından Finance uygulamasına proje gider kategorilerini eşitlemek için şu şablon ve temel görev kullanılır:

- **Veri tümleştirmedeki şablonun adı:** Proje gider hareket kategorileri (Fin and Ops'dan PSA'ya)
- **Projedeki görevin adı:** Kategorileri PSA'ya eşitle

### <a name="entity-set"></a>Varlık kümesi

| Finans                           | Project Service Automation |
|-----------------------------------|----------------------------|
| Kategoriler için tümleştirme varlığı | Hareket kategorileri     |

### <a name="entity-flow"></a>Varlık akışı

Proje gider kategorileri Finance uygulamasında yönetilir ve hareket kategorileri olarak Project Service Automation ile eşitlenir.

### <a name="power-query"></a>Power Query

Project Service Automation'a eşitleme yaparken, hareket kategorisindeki faturalama türünü ayarlamak için Excel için Microsoft Power Query kullanmanız gerekir. Proje gideri hareket kategorileri (Fin and Ops'dan PSA'ya) şablonu, varsayılan bir sütun ve eşleme sağlar. Kendi şablonunuzu oluşturursanız, Power Query'de koşullu bir sütun eklemeniz gerekir. Şu adımları izleyin.

1. Proje gideri kategori görevinin eşlemesini Proje gideri hareket kategorileri (Fin and Ops'dan PSA'ya) şablonunda açmak için oku tıklayın.
2. Power Query öğesini açmak için **Gelişmiş sorgu ve Filtreleme** bağlantısını tıklayın.
2. **Koşullu Sütun Ekle** 'yi seçin.
3. Yeni sütun için **BillingType** gibi bir ad girin.
4. Aşağıdaki koşulu girin: **CategoryID null değerine eşit değilse 19235001, aksi takdirde null yapın**.
5. Sütunda **Tamam** öğesini tıklayın.
6. Eşleme sayfasında bu yeni sütunu eşleştirdiğinizden emin olun.

Aşağıdaki çizimde Veri tümleştirmede şablon görev eşlemesinin bir örneği gösterilmektedir. Eşleme, Finance'den Project Service Automation'a eşitlenecek alan bilgilerini gösterir.

[![Proje gider kategorosini Project Service Automation şablonuna eşitleme](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a>Project Service Automation'dan Finance'e proje gideri kategorilerini eşitleme

### <a name="template-and-task"></a>Şablon ve görev

Finance uygulamasından Project Service Automation uygulamasına proje gider kategorilerini eşitlemek için şu şablon ve temel görev kullanılır:

- **Veri tümleştirmedeki şablonun adı:** Proje gider hareket kategorileri (PSA'dan Fin and Ops'a)
- **Projedeki görevin adı:** Kategorileri Fin Ops'a eşitle

### <a name="entity-set"></a>Varlık kümesi

| Project Service Automation | Finans                           |
|----------------------------|-----------------------------------|
| Hareket kategorileri     | Kategoriler için tümleştirme varlığı |

### <a name="entity-flow"></a>Varlık akışı

Proje gider kategorileri Finance uygulamasında yönetilir ve hareket kategorileri olarak Project Service Automation ile eşitlenir. Yeniden Finance'e eşitlenmesi Project Service Automation'dan tümleştirme kimlikleri ile Finance'de proje kategorilerini güncelleştirir.

### <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşlemesi

Aşağıdaki çizimde Veri tümleştirmede şablon görev eşlemesinin bir örneği gösterilmektedir.

> [!NOTE]
> Eşleme, Project Service Automation'dan Finance'e eşitlenecek alan bilgilerini gösterir.

[![Project Service Automation ile Finance şablon eşlemesi](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]