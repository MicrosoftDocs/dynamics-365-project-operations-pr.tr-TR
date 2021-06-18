---
title: Proje tahminlerini Project Service Automation uygulamasından Finance and Operations uygulamasına doğrudan eşitleme
description: Bu konuda, proje saat tahminlerini ve proje gider tahminlerini Microsoft Dynamics 365 Project Service Automation uygulamasından Dynamics 365 Finance uygulamasına doğrudan eşitlemek için kullanılan şablonlar ve temel görevler açıklanır.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: a6955dcd1ebe494e0171c30ac4384089da6a8745
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999740"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a>Proje tahminlerini Project Service Automation uygulamasından Finance and Operations uygulamasına doğrudan eşitleme

[!include[banner](../includes/banner.md)]

Bu konuda, proje saat tahminlerini ve proje gider tahminlerini Dynamics 365 Project Service Automation uygulamasından Dynamics 365 Finance uygulamasına doğrudan eşitlemek için kullanılan şablonlar ve temel görevler açıklanır.

> [!NOTE]
> - 8.0 sürümünde proje görev tümleştirmesini, gider hareketi kategorilerini, saat tahminlerini, gider tahminlerini ve işlevsellik kilitlemeyi kullanabilirsiniz.
> - Gerçek değerler tümleştirmesi sürüm 8.0.1 veya daha sonraki sürümlerde kullanılabilir.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Project Service Automation ile Finance tümleştirmesi için veri akışı

Project Service Automation ile Finance tümleştirme çözümünde Project Service Automation ile Finance örnekleri arasında verinin eşitlenmesini sağlayan Veri tümleştirme özelliği kullanılır. Veri tümleştirme özelliğiyle kullanılabilen tümleştirme şablonu, proje saat tahminleri ve gider hareketi tahminleri ile ilgili verilerin Project Service Automation ile Finance uygulamasının arasında akışını sağlar.

Aşağıdaki şekilde Project Service Automation ve Finance arasındaki tümleştirmenin bir parçası olarak verilerin nasıl eşitleneceğini gösterilir.

[![Finance ile Project Service Automation tümleştirmesi için veri akışı](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)

## <a name="project-hour-estimates"></a>Proje saat tahminleri

### <a name="template-and-tasks"></a>Şablon ve görevler

Hazır şablonlara erişmek için, Microsoft Power Apps yönetim merkezinde, **Projeler**'i seçin ve ardından sağ üst köşeden, ortak şablonları seçmek için **Yeni proje**'yi seçin.

Project Service Automation uygulamasından Finance uygulamasına proje saat tahminlerini eşitlemek için şu şablon ve temel görevler kullanılır:

- **Veri tümleştirmedeki şablonun adı:** Proje saat tahminleri (PSA'dan Fin and Ops'a)
- **Projedeki görevlerin adı:**

    - Hareket ilişkileri
    - Gider tahminleri

### <a name="entity-set"></a>Varlık kümesi

| Project Service Automation | Finans                                       |
|----------------------------|-----------------------------------------------|
| Proje görevleri              | Proje saat tahminleri için tümleştirme varlığı |

### <a name="entity-flow"></a>Varlık akışı

Proje saat tahminleri Project Service Automation uygulamasında yönetilir ve proje saat tahminleri olarak Finance ile eşitlenir.

### <a name="prerequisites"></a>Ön koşullar

Proje saat tahminlerinin eşitlenmesi gerçekleşmeden önce, projeleri, proje görevlerini ve proje gideri hareketi kategorilerini eşitlemeniz gerekir.

### <a name="power-query"></a>Power Query

Proje saat tahminleri şablonunda, aşağıdaki görevleri gerçekleştirmek için Excel için Microsoft Power Query kullanmanız gerekir:

- Tümleştirme yeni saat tahminleri oluşturduğunda kullanılacak varsayılan tahmin modeli kodunu ayarlayın.
- Saat tahminlerinde tümleştirmeyi başarısız olacak görevdeki kaynağa özgü kayıtları filtreleyin.
- Boş hareket kategorisi satırlarını filtreleyin. Bu görevin tamamlanamamasının nedeni yanlış saat tahminlerine neden olabilir.

#### <a name="set-the-default-forecast-model-id"></a>Varsayılan tahmin modeli kodunu ayarlama

Şablondaki varsayılan tahmin model kodunu güncelleştirmek için eşlemeyi açmak üzere **Eşleme** okunu tıklayın. Ardından **Gelişmiş sorgu ve Filtreleme** bağlantısını seçin.

- Varsayılan Proje saat tahminleri (PSA'dan Fin and Ops'a) şablonunu kullanıyorsanız, **Uygulanan adımlar** listesinden **Eklenen Koşul** öğesini seçin. **İşlev** girişinde, **O\_forecast** öğesini tümleştirmeyle kullanılması gereken tahmin model kodu ile değiştirin. Varsayılan şablonunda demo verilerine ait bir tahmin modeli kodu vardır.
- Yeni bir şablon oluşturuyorsanız, bu sütunu eklemeniz gerekir. Power Query'de **Koşullu Sütun Ekle**'yi seçin ve sütun için **ModelID** gibi bir ad girin. Sütun için bir koşul girin; proje görevi null değilse ardından \<enter the forecast model ID\>; diğer null'dur.

#### <a name="filter-out-resource-specific-records"></a>Kaynağa özgü kayıtları filtreleme

Proje saat tahminleri (PSA'dan Fin and Ops'a) şablonunda herhangi bir kaynağa özgü kayıtları kaldıran, varsayılan bir filtre vardır. Kendi şablonunuzu oluşturursanız, bu filtreyi eklemeniz gerekir. **msdyn\_islinetask** sütununda filtreleme yapmak için **Gelişmiş Sorgu ve Filtreleme** bağlantısını seçin. Böylece yalnızca **Yanlış** kayıtlar dahil edilir.

#### <a name="filter-out-empty-transaction-category-rows"></a>Boş hareket kategorisi satırlarını filtrenin dışında bırakma

Boş hareket kategorileri olan satırları kaldırmak için bir filtre eklemeniz gerekir. Bu görev, varsayılan şablonu kullanıyor olmanıza veya kendi şablonunuzu oluşturmanıza bakılmaksızın gereklidir. Bu filtre, Finance içindeki saat tahminlerinin yanlış olmasına neden olabilen tüm özet satırları Project Service Automation'dan kaldırır. **msdyn\_transactioncategory\_value** sütunundaki boş kayıtları filtrenin dışında bırakmak için **Gelişmiş Sorgu ve Filtreleme** bağlantısını seçin.

### <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşlemesi

Aşağıdaki çizimde Veri tümleştirmede şablon görev eşlemesinin bir örneği gösterilmektedir. Eşleme, Project Service Automation'dan Finance'e eşitlenecek alan bilgilerini gösterir.

[![Veri tümleştirmede şablon görevi eşlemesi](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

## <a name="project-expense-estimates"></a>Proje gider tahminleri

### <a name="template-and-tasks"></a>Şablon ve görevler

Project Service Automation uygulamasından Finance uygulamasına proje gider tahminlerini eşitlemek için şu şablon ve temel görevler kullanılır:

- **Veri tümleştirmedeki şablonun adı:** Proje gider tahminleri (PSA'dan Fin and Ops'a)
- **Projedeki görevlerin adı:**

    - Hareket ilişkileri 
    - Gider tahminleri

### <a name="entity-set"></a>Varlık kümesi

| Project Service Automation | Finans                                                  |
|----------------------------|----------------------------------------------------------|
| İşlem Bağlantıları    | Proje hareket ilişkilerine ait tümleştirme varlığı |
| Tahmin Satırları             | Proje gider tahminleri için tümleştirme varlığı         |

### <a name="entity-flow"></a>Varlık akışı

Proje gider tahminleri Project Service Automation uygulamasında yönetilir ve proje gider tahminleri olarak Finance ile eşitlenir.

### <a name="prerequisites"></a>Ön koşullar

Proje gider tahminlerinin eşitlenmesi gerçekleşmeden önce, projeleri, proje görevlerini ve proje gideri hareketi kategorilerini eşitlemeniz gerekir.

### <a name="power-query"></a>Power Query

Proje gider tahminleri şablonunda, aşağıdaki görevleri gerçekleştirmek için Power Query kullanmanız gerekir:

- Yalnızca gider tahmini satır kayıtlarını dahil etmek için filtreleyin.
- Tümleştirme yeni saat tahminleri oluşturduğunda kullanılacak varsayılan tahmin modeli kodunu ayarlayın.
- Faturalama türlerini dönüştürün.
- Hareket türlerini dönüştürün.

#### <a name="filter-to-include-only-expense-estimate-lines"></a>Yalnızca gider tahmini satırlarını dahil etmek için filtreleyin.

Proje gideri tahminleri (PSA'dan Fin and Ops'a) şablonunda yalnızca tümleştirmede gider satırlarını içeren bir varsayılan filtre vardır. Kendi şablonunuzu oluşturursanız, bu filtreyi eklemeniz gerekir. **Hareketi ilişkileri** görevini seçin ve eşlemeyi açmak için **Eşleme** okunu tıklayın. **Gelişmiş Sorgu ve Filtreleme** bağlantısını seçin. **msdyn\_transactiontype1** sütununa yalnızca **msdyn\_estimateline** koşulunu içermesi için filtre uygulayın.

#### <a name="set-the-default-forecast-model-id"></a>Varsayılan tahmin modeli kodunu ayarlama

Şablondaki varsayılan tahmin model kodunu güncelleştirmek için **Gider tahminleri** görevini seçip ardından eşlemeyi açmak üzere **Eşleme** okunu tıklayın. **Gelişmiş Sorgu ve Filtreleme** bağlantısını seçin.

- Varsayılan Proje gider tahminleri (PSA'dan Fin and Ops'a) şablonunu kullanıyorsanız, Power Query uygulamasında, **Uygulanan adımlar** bölümünden ilk **Eklenen Koşul** öğesini seçin. **İşlev** girişinde, **O\_forecast** öğesini tümleştirmeyle kullanılması gereken tahmin model kodu ile değiştirin. Varsayılan şablonunda demo verilerine ait bir tahmin modeli kodu vardır.
- Yeni bir şablon oluşturuyorsanız, bu sütunu eklemeniz gerekir. Power Query'de **Koşullu Sütun Ekle**'yi seçin ve sütun için **ModelID** gibi bir ad girin. Sütun için bir koşul girin; Tahmin satırı kimliği null değilse ardından \<enter the forecast model ID\>; diğer null'dur.

#### <a name="transform-the-billing-types"></a>Faturalama türlerini dönüştürme

Proje gideri tahminleri (PSA'dan Fin and Ops'a) şablonu, tümleştirme sırasında Project Service Automation'dan alınan faturalama türlerini dönüştürmek için kullanılan koşullu bir sütun içerir. Kendi şablonunuzu oluşturursanız, bu koşullu sütunu eklemeniz gerekir. **Gelişmiş Sorgu ve Filtre** bağlantısını seçin ve ardından **Koşullu Sütun Ekle** öğesini seçin. Yeni sütun için **BillingType** gibi bir ad girin. Ardından aşağıdaki koşulu girin:

If **msdyn\_billingtype** = 192350000, then **NonChargeable**  
else if **msdyn\_billingtype** = 192350001, then **Chargeable**  
else if **msdyn\_billingtype** = 192350002, then **Complimentary**  
else **NotAvailable**

#### <a name="transform-the-transaction-types"></a>Hareket türlerini dönüştürme

Proje gideri tahminleri (PSA'dan Fin and Ops'a) şablonu, tümleştirme sırasında Project Service Automation'dan alınan hareket türlerini dönüştürmek için kullanılan koşullu bir sütun içerir. Kendi şablonunuzu oluşturursanız, bu koşullu sütunu eklemeniz gerekir. **Gelişmiş Sorgu ve Filtre** bağlantısını seçin ve ardından **Koşullu Sütun Ekle** öğesini seçin. Yeni sütun için **TransactionType** gibi bir ad girin. Ardından aşağıdaki koşulu girin:

If **msdyn\_transactiontypecode** = 192350000, then **Cost**  
else if **msdyn\_transactiontypecode** = 192350005, then **Sales**  
else **null**

### <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşlemesi

Aşağıdaki çizimlerde Veri tümleştirmede şablon görev eşlemelerinin örnekleri gösterilmektedir. Eşleme, Project Service Automation'dan Finance'e eşitlenecek alan bilgilerini gösterir.

[![Gider tahmini hareketlerinin şablon eşlemesi](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Gider tahminlerinin şablon eşlemesi](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]