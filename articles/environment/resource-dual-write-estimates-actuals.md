---
title: Proje tahminleri ve gerçek değerler tümleştirmesi
description: Bu konu proje tahminleri ve gerçek değerler için Project Operations iki yazma tümleştirmesiyle ilgili bilgi sağlar.
author: sigitac
manager: Annbe
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 88df3385fac0a78a827d65a77d3b04c9d6499536
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955852"
---
# <a name="project-estimates-and-actuals-integration"></a>Proje tahminleri ve gerçek değerler tümleştirmesi

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Bu konu proje tahminleri ve gerçek değerler için Project Operations iki yazma tümleştirmesiyle ilgili bilgi sağlar.

## <a name="project-estimates"></a>Proje tahminleri

Muhasebe amaçlarına yönelik olarak proje işçiliği, gider ve malzeme tahminleri uygulamasında oluşturulur ve Microsoft Dataverse ve Finance and Operations uygulamalara eşitlenir. Oluşturma, güncelleştirme ve silme işlemleri Finance and Operations uygulamalar aracılığıyla desteklenmez.

Tahminler oluşturmak için proje için geçerli bir hesaplama yapılandırması gerekir. Sözleşme satırlarıyla ilişkilendirilen projelerin, proje maliyet ve gelir profili kurallarında tanımlanmış geçerli bir proje maliyeti ve gelir profili olmalıdır. Daha fazla bilgi için bkz. [Faturalandırılabilir projelerin muhasebesini yapılandırma](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>İşçilik tahminleri

İşçilik tahminleri proje yöneticisine veya ayrıca proje görevine genel veya adlandırılmış bir kaynak atayan bir kaynak yöneticisi tarafından oluşturulur. Kaynak atama kayıtları, Dataverse içindeki **proje ayrıntıları** sayfasındaki **kaynak atamaları** sekmesinde gözden geçirilebilir. Dataverse'deki kaynak atama kayıtları, **saat tahminleri için Project Operations tümleştirme varlığı (msdyn\_resourceassignments)** kullanarak Finance and Operations uygulamalarındaki tahmin kayıtlarını oluşturur.

   ![İşçilik tahminleri tümleştirmesi](./Media/DW4LaborEstimates.png)

Çift yazma, kaynak atama kayıtlarını hazırlama tablosuna (**ProjCDSEstimateHoursImport**) eşitler ve ardından saat tahmini kayıtlarını (**ProjForecastEmpl**) oluşturmak ve güncelleştirmek için iş mantığını kullanır.

Proje muhasebecisi, **Proje yönetimi ve hesap** > **Tüm projeler** > **Plan** > **Saat tahminleri**'ne giderek Finance and Operations'ta oluşturulan tahmini saat kayıtlarını inceler.

## <a name="expense-estimates"></a>Gider tahminleri

Gider tahminleri, Dataverse uygulamasındaki **proje ayrıntıları** sayfasındaki **gider tahminleri** sekmesinde yer alan Proje Yöneticisi tarafından oluşturulur. Gider tahmini kayıtları, Dataverse içindeki **tahmin satırı** varlığı içinde depolanır. Bu tahmin kayıtları **gider** adlı işlem sınıfına sahiptir ve **gider tahminleri için Project Operations tümleştirme varlığı (msdyn\_estimatelines)** kullanılarak Finance and Operations uygulamalardaki masraf tahmini kayıtlarıyla eşitlenir .

   ![Gider tahminleri tümleştirmesi](./Media/DW4ExpenseEstimates.png)

Çift yazma, gider tahmini kayıtlarını hazırlama tablosuna (**ProjCDSEstimateExpenseImport**) eşitler ve ardından gider tahmini kayıtlarını (**ProjForecastCost**) oluşturmak ve güncelleştirmek için iş mantığını kullanır. Tahmin satırları satış tahminini ve maliyet tahmini kayıtlarını ayrı olarak depolar. Finance and Operations uygulamalarındaki iş mantığı, hazırlama tablosundaki bu ayrıntıyı kullanarak tek bir masraf tahmini kaydını doldurur.

Proje muhasebecisi, **Proje yönetimi ve hesap** > **Tüm projeler** > **Plan** > **gider tahminleri**'ne giderek Finance and Operations'ta oluşturulan gider tahmini kayıtlarını inceler.

## <a name="material-estimates"></a>Malzeme Tahminleri

Malzeme tahminleri, Dataverse uygulamasındaki **proje ayrıntıları** sayfasındaki **Malzeme tahminleri** sekmesinde yer alan Proje Yöneticisi tarafından oluşturulur. Malzeme tahmini kayıtları, Dataverse içindeki **tahmin satırı** varlığı içinde depolanır. Bu tahmin kayıtları **gider** adlı işlem sınıfına sahiptir ve **Malzeme tahminleri için Proje tümleştirme tablosu (msdyn\_estimatelines)** kullanılarak Finance and Operations uygulamalardaki malzeme tahmini kayıtlarıyla eşitlenir .

   ![Malzeme tahminleri tümleştirmesi](./Media/DW4MaterialEstimates.png)

Çift yazma, malzeme tahmini kayıtlarını hazırlama tablosuna (**ProjForecastSalesImpor**) eşitler ve ardından madde tahmini kayıtlarını (**ForecastSales**) oluşturmak ve güncelleştirmek için iş mantığını kullanır. Tahmin satırları satış tahminini ve maliyet tahmini kayıtlarını ayrı olarak depolar. Finance and Operations uygulamalarındaki iş mantığı, hazırlama tablosundaki bu ayrıntıyı kullanarak tek bir madde tahmini kaydını doldurur.

Proje muhasebecisi, **Proje yönetimi ve hesap** > **Tüm projeler** > **Plan** > **madde tahminleri**'ne giderek Finance and Operations'ta oluşturulan madde tahmini kayıtlarını inceler.

## <a name="project-actuals"></a>Proje gerçek değerleri

Proje gerçekleri zaman, gider, malzeme ve fatura etkinliğine göre Dataverse uygulamasında oluşturulur. Bu hareketlerin miktar, maliyet fiyatı, satış fiyatı ve proje dahil tüm operasyon öznitelikleri bu Dataverse varlıkta yakalanır. Daha fazla bilgi için bkz. [Gerçek değerler](../actuals/actuals-overview.md). Gerçek kayıtlar ikili yazma tablo eşlemesi, **Project Operations tümleştirmesi (msdyn\_ fiili değerleri)** kullanımı ile Finance and Operations uygulamalarına eşitlenir.

   ![Gerçek değer tümleştirmesi](./Media/DW4Actuals.png)

**Project Operations tümleştirmesi gerçek kaynak** tablosu eşlemesi, Dataverse'deki **gerçek değerler** varlığındaki tüm kayıtları, **eşitlemeyi atla (yalnızca iç kullanım)** özelliğini **yanlış** değerine ayarlanmış olarak eşitler. Bu öznitelik değeri, kayıt oluşturulduğunda Dataverse'te otomatik olarak ayarlanır. Bu özniteliğin **doğru** değerine ayarlandığı örnekler şunlardır:

  - Şirketlerarası hareketlere yönelik proje maliyet değerleri. Daha fazla bilgi için bkz. [Şirketlerarası işlemler oluşturma](../project-accounting/create-intercompany-transactions.md). Bu kayıtlar, şirketlerarası satıcı faturası deftere nakledildiğinde sistem proje maliyetini Finance and Operations uygulamalarda fiili yeniden oluşturduğundan, atlanır.
  - Proforma faturası onaylandıktan sonra oluşturulan negatif edilmemiş satış kayıtları. Bu kayıtlar, Finance and Operations uygulamalardaki proje alt muhasebeyi Faturalandırma sırasında faturalanmamış satış kaydını ters atmadığından atlanır, ancak durumu tamamen faturalandı olarak değiştirir.

Çift yazma tablo eşlemesi, gerçek değerler kayıtlarını **ProjCDSActualsImport** hazırlama tablosu olarak eşitler. Bu kayıtlar, Project Operations tümleştirme günlüğü satırları ve proje fatura teklifi satırları oluşturulurken **hazırlık tablosundan içe aktar** dönemsel işlemi tarafından işlenir. Daha fazla bilgi için bkz. [Project Operations içindeki tümleştirme günlüğü](../project-accounting/project-operations-integration-journal.md).

Dataverse ayrıca, **İşlem bağlantısı** varlığındaki proje gerçek işlemleri arasındaki bağlantıları yakalar. Daha fazla bilgi için bkz. [Fiili değerleri özgün kayıtlara bağlama](../actuals/linkingactuals.md). Gerçek işlemler arasındaki bağlantılar aynı zamanda çift yazılır tablo eşlemesi, **proje işlem İlişkileri için tümleştirme varlığı (msdyn\_transactionconnections)** kullanılarak Finance and Operations uygulamalarla eşitlenir. Bu kayıtlar, Project Operations tümleştirme günlüğü satırları ve proje fatura teklifi satırları oluşturulurken **hazırlık tablosundan içe aktar** dönemsel işlemi tarafından kullanılır.

Project Operations tümleştirme günlüğünün ve Proje Fatura teklifinin deftere nakledilmesi, **ProjCDSActualsImport** hazırlama tablosundaki ilgili kayıtlarda bir güncelleştirmeyi tetikler . Sistem, Fiili hareketler için aşağıdaki hesaplama özniteliklerini yakalar ve kaydeder:

- Muhasebe para birimi miktarı
- Döviz kuru
- Makbuz Numarası
- Satış vergisi tutarı

**Project Operations tümleştirme fiili** tablo eşlemesi, Dataverse' de bu bilgilerle ilgili gerçek değer kayıtlarını güncelleştirir .
