---
title: Proje gerçek değerlerini doğrudan Project Service Automation'dan proje tümleştirme günlüğüne, Finance and Operations uygulamasında deftere nakletmek için eşitleme
description: Bu konuda, proje gerçek değerlerini Microsoft Dynamics 365 Project Service Automation uygulamasından Finance and Operations uygulamasına doğrudan eşitlemek için kullanılan şablonlar ve temel görevler açıklanır.
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
ms.assetid: 02ae4986-8e7b-4abe-97d3-cff0904d84de
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 7e5aff102226e5eac2ba3de17407eaa4461cd1ac
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756662"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Proje gerçek değerlerini doğrudan Project Service Automation'dan proje tümleştirme günlüğüne, Finance and Operations uygulamasında deftere nakletmek için eşitleme

[!include[banner](../includes/banner.md)]

Bu konuda, proje gerçek değerlerini Dynamics 365 Project Service Automation uygulamasından Dynamics 365 Finance uygulamasına doğrudan eşitlemek için kullanılan şablonlar ve temel görevler açıklanır.

Şablon, Project Service Automation'dan hareketleri Finans uygulamasındaki hazırlama tablosuna eşitler. Eşitleme tamamlandıktan sonra, hazırlama tablosundaki verileri tümleştirme günlüğüne aktarmanız **gerekir**.

> [!NOTE]
> - Proje gerçek değerleri tümleştirmesi sürüm 8.0.1'den başlamak üzere kullanılabilir.
> - Enterprise Edition 7.3.0 kullanıyorsanız, KB 4132657 ve KB 4132660 yükledikten sonra, proje görevlerini, gider hareketi kategorilerini, saat tahminlerini, masraf tahminlerini ve gerçek değerleri tümleştirmek ve işlevsellik kilitlemeyi yapılandırmak için şablonları kullanabilirsiniz. Muhasebe dağıtımlarını sıfırlamanız gerekiyorsa, KB 4131710'u da yüklemenizi öneririz.
> - 7.3.0 sürümünü kullanıyorsanız ve Project Service Automation'dan ücret hareketleri alıyorsanız, bu ücretleri proje faturasına dahil etmek için KB 4345320 yüklemelisiniz.
> - Project Service Automation'da zaman veya gider hareketlerine satış vergisi tutarları giriyorsanız Project Service Automation güncelleştirme 7'yi yüklemelisiniz. Aksi takdirde, vergiye ait gerçek değerleri ilgili zaman veya gider gerçek değerlerine bağlanmaz ve Finance ile eşitlenmez. Daha fazla bilgi için Destek ile görüşün.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Project Service Automation ile Finance tümleştirmesi için veri akışı

Project Service Automation ile Finance tümleştirme çözümünde Project Service Automation ile Finance örnekleri arasında verinin eşitlenmesini sağlayan Veri tümleştirme özelliği kullanılır. Veri tümleştirme özelliğiyle kullanılabilen tümleştirme şablonları, proje gerçek değerleri ile ilgili verilerin Project Service Automation uygulamasından Finance uygulamasına akışını sağlar.

Aşağıdaki şekilde Project Service Automation ve Finance arasındaki tümleştirmenin bir parçası olarak verilerin nasıl eşitleneceğini gösterilir.

[![Project Service Automation ile Finance and Operations tümleştirmesi için veri akışı](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Project Service Automation uygulamasındaki proje gerçek değerleri

### <a name="template-and-tasks"></a>Şablon ve görevler

Hazır şablonlara erişmek için, Microsoft Power Apps yönetim merkezinde, **Projeler**'i seçin ve ardından sağ üst köşeden, ortak şablonları seçmek için **Yeni proje**'yi seçin.

Project Service Automation uygulamasından Finance uygulamasına proje gerçek değerlerini eşitlemek için şu şablon ve temel görevler kullanılır:

- **Veri tümleştirmedeki şablonun adı:** Proje gerçek değerleri (PSA'dan Fin and Ops'a)
- **Projedeki görevlerin adı:**

    - Gerçek değerler
    - TransactionConnections

### <a name="entity-set"></a>Varlık kümesi

| Project Service Automation | Finans                                   |
|----------------------------|----------------------------------------------------------|
| Gerçek değerler                    | Proje gerçek değerlerine ait tümleştirme varlığı                   |
| İşlem Bağlantıları    | Proje hareket ilişkilerine ait tümleştirme varlığı |

### <a name="entity-flow"></a>Varlık akışı

Proje gerçek değerleri Project Service Automation uygulamasında yönetilir ve Finance'de proje tümleştirme günlüğü ile eşitlenir. Muhasebe, varsayılan mali boyutlara ve deftere nakil kurulumuna göre uygulanır.

### <a name="prerequisites"></a>Ön koşullar

Gerçek değerlerin eşitlenmesi gerçekleşmeden önce, Project Service Automation tümleştirme parametrelerini yapılandırmalı ve projeleri, proje görevleri ve proje gideri hareketi kategorilerini eşitlemeniz gerekir.

### <a name="power-query"></a>Power Query

Proje gerçek değerleri şablonunda, aşağıdaki görevleri gerçekleştirmek için Excel için Microsoft Power Query kullanmanız gerekir:

- Project Service Automation'daki hareket türünü Finance içindeki doğru hareket türüne dönüştürün. Bu dönüşüm Proje gerçek değerleri (PSA'dan Fin and Ops'a) şablonunda zaten tanımlandı.
- Project Service Automation'daki faturalama türünü Finance içindeki faturalama türüne dönüştürün. Bu dönüşüm Proje gerçek değerleri (PSA'dan Fin and Ops'a) şablonunda zaten tanımlandı. Faturalama türü, **Project Service Automation tümleştirme parametreleri sayfasındaki** yapılandırmaya göre daha sonra satır özelliği ile eşleştirilir.
- Bu şablonla eşitlenmesi gereken belirli kaynak kuruluş birimlerine filtre uygulayın.
- Şirketlerarası zaman veya şirketlerarası gider gerçek değerleri Finance ile eşitlenirse, sözleşme kuruluş birimini Finance içindeki doğru yasal varlığa dönüştürmeniz gerekir. Proje gerçek değerleri (PSA'dan Fin and Ops'a) şablonunda, demo verilerine bağlı olarak bir koşullu sütun tanımlanır. Son eklenen koşullu sütunu doğru yasal varlıklara güncelleştirmeniz gerekir. Aksi takdirde, bir tümleştirme hatası oluşabilir veya Finance içine yanlış gerçek değer hareketleri alınabilir.
- Şirketlerarası zaman veya şirketlerarası gider gerçek değerleri Finance ile eşitlenmezse, son eklenen koşullu sütunu şablonunuzun içinden silmeniz gerekir. Aksi takdirde, bir tümleştirme hatası oluşabilir veya Finance içine yanlış gerçek değer hareketleri alınabilir.

#### <a name="contract-organizational-unit"></a>Sözleşme kuruluş birimi
Şablondaki eklenen koşullu sütunu güncelleştirmek için eşlemeyi açmak üzere **Eşleme** okunu tıklayın. Power Query öğesini açmak için **Gelişmiş sorgu ve Filtreleme** bağlantısını seçin.

- Varsayılan Proje gerçek değerleri (PSA'dan Fin and Ops'a) şablonunu kullanıyorsanız, Power Query uygulamasında, **Uygulanan adımlar** bölümünden son **Eklenen Koşul** öğesini seçin. **İşlev** girişinde, **USSI**'yi, tümleştirmeyle kullanılması gereken yasal varlığın adıyla değiştirin. **İşlev** girişine gereksinim duydukça ek koşullar ekleyin ve **USMF**'den **else** koşulunu doğru yasal varlığa güncelleştirin.
- Yeni bir şablon oluşturuyorsanız, şirketlerarası zaman ve giderleri desteklemek için sütun eklemeniz gerekir. **Koşullu Sütun Ekle**'yi seçin ve sütun için **LegalEntity** gibi bir ad girin. Sütun için bir koşul girin: if **msdyn\_contractorganizationalunitid.msdyn\_name** is \<organizational unit\>, then \<enter the legal entity\>; else null.

### <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşlemesi

Aşağıdaki çizimlerde Veri tümleştirmede şablon görev eşlemesinin bir örneği gösterilmektedir. Eşleme, Project Service Automation'dan Finance'e eşitlenecek alan bilgilerini gösterir.

[![Şablon eşlemesi](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Şablon eşlemesi](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Project Service Automation'ı tümleştirmeden sonra hazırlama tablosundan içe aktarma

Project Service Automation'dan Finance'e gerçek değerleri eşitlemeden sonra Hazırlama tablosundan içe aktar dönemsel olarak çalıştırılmalıdır. Bu işlem, muhasebenin uygulandığı ve içe aktarılan hareketlerin nakledildiği hazırlama tablosundan Project Service Automation tümleştirme günlüğüne proje hareketlerini aktarır. Bu işlemi toplu iş modunda çalıştırmanızı öneririz; isteğe bağlı olarak, yinelenen bir toplu işlem olarak çalıştırılmak üzere ayarlanabilir.

## <a name="update-actuals-from-finance"></a>Finance'den gerçek değerleri güncelleştirme

### <a name="template-and-tasks"></a>Şablon ve görevler

Aşağıdaki şablon ve temel görevler, Finance'den Project Service Automation'a nakledilmiş proje hareketlerinin makbuz numarasını ve satış vergilerini eşitlemek için kullanılır:

- **Veri tümleştirmedeki şablonun adı:** Proje gerçek değerlerini güncelleştirme (Fin and Ops'dan PSA'ya)
- **Projedeki görevlerin adı:**

    - Gerçek değerler 
    - TransactionConnections

### <a name="entity-set"></a>Varlık kümesi

| Finans                                                  | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| Proje gerçek değerlerine ait tümleştirme varlığı                   | Gerçek değerler                    |
| Proje hareket ilişkilerine ait tümleştirme varlığı | İşlem Bağlantıları    |

### <a name="entity-flow"></a>Varlık akışı

Proje gerçek değerleri Project Service Automation uygulamasında yönetilir ve Finance'de proje tümleştirme günlüğü ile eşitlenir. Gerçek değerler Finance'e nakledildikten sonra, Project Service Automation'da Finance içindeki makbuz numarasıyla güncelleştirilir. Finance'de satış vergileri eklenmişse, yeni vergi gerçek değerleri Project Service Automation'da oluşturulur.

### <a name="power-query"></a>Power Query

Proje gerçek değerleri şablonunda, aşağıdaki görevleri gerçekleştirmek için Power Query kullanmanız gerekir:

- Finance'deki hareket türünü Project Service Automation içindeki doğru hareket türüne dönüştürün. Bu dönüşüm Proje gerçek değerlerini güncelleştirme (Fin and Ops'dan PSA'ya) şablonunda zaten tanımlanmıştır.
- Finance içindeki faturalama türünü Project Service Automation içindeki faturalama türüne dönüştürün. Bu dönüşüm Proje gerçek değerlerini güncelleştirme (Fin and Ops'dan PSA'ya) şablonunda zaten tanımlanmıştır.

### <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşlemesi

Aşağıdaki çizimlerde Veri tümleştirmede şablon görev eşlemelerinin örnekleri gösterilmektedir. Eşleme, Finance'den Project Service Automation'a eşitlenecek alan bilgilerini gösterir.

[![Şablon eşlemesi](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Şablon eşlemesi](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)
