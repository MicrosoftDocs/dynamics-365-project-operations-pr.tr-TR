---
title: Proje tahminleri ve gerçek değerler tümleştirmesi
description: Bu makale, proje tahminleri ve fiili değerler için Project Operations çift yazma tümleştirmesiyle ilgili bilgi sağlar.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 43c868b051bf141cfc3211669c0a44333b4b2c65
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914610"
---
# <a name="project-estimates-and-actuals-integration"></a>Proje tahminleri ve gerçek değerler tümleştirmesi

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Bu makale, proje tahminleri ve fiili değerler için Project Operations çift yazma tümleştirmesiyle ilgili bilgi sağlar.

## <a name="project-estimates"></a>Proje tahminleri

Proje işçiliği, gider ve malzeme tahminleri Microsoft Dataverse'te oluşturulur ve muhasebe amacıyla Finans ve Operasyon uygulamalarıyla eşitlenir. Oluşturma, güncelleştirme ve silme işlemleri, Finans ve Operasyon uygulamaları üzerinden desteklenmez.

Tahminler oluşturmak için proje için geçerli bir hesaplama yapılandırması gerekir. Sözleşme satırlarıyla ilişkilendirilen projelerin, proje maliyet ve gelir profili kurallarında tanımlanmış geçerli bir proje maliyeti ve gelir profili olmalıdır. Daha fazla bilgi için bkz. [Faturalandırılabilir projelerin muhasebesini yapılandırma](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>İşçilik tahminleri

İşçilik tahminleri proje yöneticisine veya ayrıca proje görevine genel veya adlandırılmış bir kaynak atayan bir kaynak yöneticisi tarafından oluşturulur. Kaynak atama kayıtları, Dataverse içindeki **proje ayrıntıları** sayfasındaki **kaynak atamaları** sekmesinde gözden geçirilebilir. Dataverse'te kaynak atama kayıtları, **Project Operations tümleştirmesi saat tahminleri varlığı (msdyn\_resourceassignments)** kullanarak Finans ve Operasyon uygulamalarında saat tahmini kayıtları oluşturur.

   ![İşçilik tahminleri tümleştirmesi.](./Media/DW4LaborEstimates.png)

Çift yazma, kaynak atama kayıtlarını hazırlama tablosuna (**ProjCDSEstimateHoursImport**) eşitler ve ardından saat tahmini kayıtlarını (**ProjForecastEmpl**) oluşturmak ve güncelleştirmek için iş mantığını kullanır.

Proje muhasebecisi, **Proje yönetimi ve muhasebe** > **Tüm projeler** > **Plan** > **Saat tahminleri**'ne giderek Finans ve Operasyon uygulamalarında oluşturulan tahmini saat kayıtlarını gözden geçirir.

## <a name="expense-estimates"></a>Gider tahminleri

Gider tahminleri, Dataverse uygulamasındaki **proje ayrıntıları** sayfasındaki **gider tahminleri** sekmesinde yer alan Proje Yöneticisi tarafından oluşturulur. Gider tahmini kayıtları, Dataverse içindeki **tahmin satırı** varlığı içinde depolanır. Bu tahmin kayıtlarında **Gider** işlem sınıfı vardır ve bunlar, **Project Operations tümleştirmesi gider tahminleri varlığı (msdyn\_estimatelines)** kullanarak Finans ve Operasyon uygulamalarında gider tahmini kayıtlarıyla eşitlenir.

   ![Gider tahminleri tümleştirmesi.](./Media/DW4ExpenseEstimates.png)

Çift yazma, gider tahmini kayıtlarını hazırlama tablosuna (**ProjCDSEstimateExpenseImport**) eşitler ve ardından gider tahmini kayıtlarını (**ProjForecastCost**) oluşturmak ve güncelleştirmek için iş mantığını kullanır. Tahmin satırları satış tahminini ve maliyet tahmini kayıtlarını ayrı olarak depolar. Finans ve Operasyon uygulamalarındaki iş mantığı, hazırlama tablosundaki bu ayrıntıyı kullanarak tek bir Gider tahmini kaydını doldurur.

Proje muhasebecisi, **Proje yönetimi ve muhasebe** > **Tüm projeler** > **Plan** > **Gider tahminleri**'ne giderek Finans ve Operasyon uygulamalarındaki gider tahmini kayıtlarını gözden geçirebilir.

## <a name="material-estimates"></a>Malzeme Tahminleri

Malzeme tahminleri, Dataverse uygulamasındaki **proje ayrıntıları** sayfasındaki **Malzeme tahminleri** sekmesinde yer alan Proje Yöneticisi tarafından oluşturulur. Malzeme tahmini kayıtları, Dataverse içindeki **tahmin satırı** varlığı içinde depolanır. Bu tahmin kayıtlarında **Malzeme** işlem sınıfı vardır ve bunlar, **Project tümleştirmesi malzeme tahminleri tablosu (msdyn\_estimatelines)** kullanarak Finans ve Operasyon uygulamalarında madde tahmini kayıtlarıyla eşitlenir.

   ![Malzeme tahminleri tümleştirmesi.](./Media/DW4MaterialEstimates.png)

Çift yazma, malzeme tahmini kayıtlarını hazırlama tablosuna (**ProjForecastSalesImpor**) eşitler ve ardından madde tahmini kayıtlarını (**ForecastSales**) oluşturmak ve güncelleştirmek için iş mantığını kullanır. Tahmin satırları satış tahminini ve maliyet tahmini kayıtlarını ayrı olarak depolar. Finans ve Operasyon uygulamalarındaki iş mantığı, hazırlama tablosundaki bu ayrıntıyı kullanarak tek bir Madde tahmini kaydını doldurur.

Proje muhasebecisi, **Proje yönetimi ve muhasebe** > **Tüm projeler** > **Plan** > **Madde tahminleri**'ne giderek Finans ve Operasyon uygulamalarındaki madde tahmini kayıtlarını gözden geçirebilir.

## <a name="project-actuals"></a>Proje gerçek değerleri

Proje gerçek değerleri zaman, gider, malzeme ve fatura etkinliğine göre Dataverse uygulamasında oluşturulur. Bu hareketlerin miktar, maliyet fiyatı, satış fiyatı ve proje dahil tüm operasyon öznitelikleri bu Dataverse varlıkta yakalanır. Daha fazla bilgi için bkz. [Gerçek değerler](../actuals/actuals-overview.md). Gerçek tutar kayıtları, aşağı akış muhasebesi için **Project Operations tümleştirmesi gerçek tutarları (msdyn\_actuals)** çift yazma tablo eşlemesini kullanarak Finans ve Operasyon uygulamalarıyla eşitlenir.

   ![Gerçek değer tümleştirmesi.](./Media/DW4Actuals.png)

**Project Operations tümleştirmesi gerçek kaynak** tablosu eşlemesi, Dataverse'deki **gerçek değerler** varlığındaki tüm kayıtları, **eşitlemeyi atla (yalnızca iç kullanım)** özelliğini **yanlış** değerine ayarlanmış olarak eşitler. Bu öznitelik değeri, kayıt oluşturulduğunda Dataverse'te otomatik olarak ayarlanır. Bu özniteliğin **doğru** değerine ayarlandığı örnekler şunlardır:

  - Şirketlerarası hareketlere yönelik proje maliyet değerleri. Daha fazla bilgi için bkz. [Şirketlerarası işlemler oluşturma](../project-accounting/create-intercompany-transactions.md). Bu kayıtlar, şirketler arası satıcı faturası gönderildiğinde sistem Finans ve Operasyon uygulamalarında proje maliyeti gerçek tutarını yeniden oluşturduğundan atlanır.
  - Proforma faturası onaylandıktan sonra oluşturulan negatif edilmemiş satış kayıtları. Bu kayıtlar, Finans ve Operasyon uygulamalarındaki proje yardımcı defteri faturalama sırasında faturalandırılmamış satış kaydını tersine çevirmeyip durumu tamamen faturalanmış olarak değiştirdiğinden atlanır.

Çift yazma tablo eşlemesi, gerçek değerler kayıtlarını **ProjCDSActualsImport** hazırlama tablosu olarak eşitler. Bu kayıtlar, Project Operations tümleştirme günlüğü satırları ve proje fatura teklifi satırları oluşturulurken **hazırlık tablosundan içe aktar** dönemsel işlemi tarafından işlenir. Daha fazla bilgi için bkz. [Project Operations içindeki tümleştirme günlüğü](../project-accounting/project-operations-integration-journal.md).

Dataverse ayrıca, **İşlem bağlantısı** varlığındaki proje gerçek işlemleri arasındaki bağlantıları yakalar. Daha fazla bilgi için bkz. [Fiili değerleri özgün kayıtlara bağlama](../actuals/linkingactuals.md). Gerçek tutar işlemleri arasındaki bağlantılar ayrıca **Proje hareketi ilişkileri için tümleştirme varlığı (msdyn\_transactionconnections)** çift yazma tablo eşlemesini kullanarak Finans ve Operasyon uygulamalarıyla eşitlenir. Bu kayıtlar, Project Operations tümleştirme günlüğü satırları ve proje fatura teklifi satırları oluşturulurken **hazırlık tablosundan içe aktar** dönemsel işlemi tarafından kullanılır.

Project Operations tümleştirme günlüğünün ve Proje Fatura teklifinin deftere nakledilmesi, **ProjCDSActualsImport** hazırlama tablosundaki ilgili kayıtlarda bir güncelleştirmeyi tetikler . Sistem, Fiili hareketler için aşağıdaki hesaplama özniteliklerini yakalar ve kaydeder:

- Muhasebe para birimi miktarı
- Döviz kuru
- Makbuz Numarası
- Satış vergisi tutarı

**Project Operations tümleştirme fiili** tablo eşlemesi, Dataverse' de bu bilgilerle ilgili gerçek değer kayıtlarını güncelleştirir .
