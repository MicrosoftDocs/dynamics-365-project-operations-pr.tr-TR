---
title: Gider yönetimi tümleştirmesi
description: Bu konu, çift yazma kullanarak Project Operations'da gider raporu tümleştirmesi hakkında bilgi sağlar.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b41be519dbfa89668712bc28ccb1888cd08c38a2
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585816"
---
# <a name="expense-management-integration"></a>Gider yönetimi tümleştirmesi

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Bu konu, çift yazma kullanarak Project Operations [tam gider dağıtımı](../expense/expense-overview.md) gider raporu tümleştirmesi hakkında bilgi sağlar.

## <a name="expense-categories"></a>Gider Kategorileri

Tam gider dağıtımında, Finans ve Operasyon uygulamalarında gider kategorileri oluşturulur ve korunur. Yeni bir gider kategorisi oluşturmak için aşağıdaki adımları izleyin:

1. Microsoft Dataverse'te, **İşlem** kategorisi oluşturun. Çift yazma tümleştirmesi, bu işlem kategorisini Finans ve Operasyon uygulamalarıyla eşitler. Daha fazla bilgi için bkz. [Proje kategorilerini yapılandırma](/dynamics365/project-operations/project-accounting/configure-project-categories) ve [Project Operations kurulumunu ve yapılandırma verileri tümleştirmesi](resource-dual-write-setup-integration.md). Bu tümleştirmenin sonucunda sistem, Finans ve Operasyon uygulamalarında dört adet paylaşılan kategori kaydı oluşturur.
2. Finance'te, **gider yönetimi** > **kurulumu** > **paylaşılan kategoriler**'e gidin ve bir **masraf** işlem sınıfı bulunan bir paylaşılan kategori seçin. **Giderde kullanılabilir** parametresinde **doğru** olarak ayarlayıp kullanılacak gider türünü tanımlayabilirsiniz.
3. Bu paylaşılan kategori kaydını kullanarak, **gider yönetimi** > **kurulum** > **gider kategorilerine** giderek **Yeni** bir gider kategorisi oluşturun. Kayıt kaydedildiğinde, Çift yazma, bu kaydı Dataverse ile eşitlemek için **Project Operations tümleştirme proje gideri kategorileri verme varlığı (msdyn\_expensecategories)** kullanır.

  ![Gider kategorileri tümleştirmesi.](./media/DW6ExpenseCategories.png)

Finans ve Operasyon uygulamalarındaki gider kategorileri şirkete veya tüzel kişiye özeldir. Dataverse'De, ilgili tüzel kişiliği özgü kayıtlar vardır . Proje yöneticisinin giderleri tahmin ettiği zaman, bunlar üzerinde çalıştıkları projeye sahip olan şirketten farklı bir şirkete ait olan bir proje için oluşturulmuş gider kategorilerini seçmezler. 

## <a name="expense-reports"></a>Gider raporları

Gider raporları Finans ve Operasyon uygulamalarında oluşturulur ve onaylanır. Daha fazla bilgi için, bkz. [Dynamics 365 Project Operations uygulamasında gider raporları oluşturma ve işleme](/learn/modules/create-process-expense-reports/). Gider raporu proje yöneticisi tarafından onaylandıktan sonra, genel muhasebeye nakledilir. Project Operations'da projeyle ilgili gider raporu satırları, özel deftere nakil kuralları kullanılarak deftere nakledilir:

  - Projeyle ilgili maliyet (kurtarılamayan KDV dahil), genel muhasebede proje maliyet hesabına hemen nakledilmez; bunun yerine gider tümleştirme hesabına nakledilir. Bu hesap, **Dynamics 365 Customer Engagement'ta Project Operations** sekmesindeki **Proje yönetimi ve hesap** > **kurulum** > **Proje yönetimi ve muhasebe parametreleri**'nde yapılandırılır.
  - İkili yazma **Project Operations tümleştirme proje masraflarını verme varlığı (msdyn\_expenses)** tablo haritasını kullanmak üzere Dataverse ile eşitlenir.
  - Vergi alt raporu, satıcı alt muhasebe ve diğer mali defter nakilleri, gider raporu giderme zamanında uygun olarak kaydedilir.

  ![Gider raporları tümleştirmesi.](./media/DW6ExpenseReports.png)

Dataverse içindeki **gider** varlığına bir kayıt yazıldığında, sistem kaydın otomatikleştirilmiş onay işlemini tetikler. Gerekirse, otomatik onay işlemi durumu **Gelişmiş ayarlar** > **sistem** > **sistemi işlerine** giderek Dataverse'te gözden geçirilebilir. Onay tamamlandıktan sonra, gider işlem sınıfı kayıtları **Gerçek değerler** varlığında oluşturur.

Giderle ilgili fiili değerler daha sonra çift yazma tablo eşlemesi, **Project Operations gerçek değerlerle tümleştirilmesine (msdyn\_actuals)** işlenir. Daha fazla bilgi için bkz. [Proje tahminleri ve gerçek değerler](resource-dual-write-estimates-actuals.md).

Periyodik işlem, **Hazırlamadan içe aktar**, Gider raporuyla ilgili Project Operations tümleştirme günlüğünde günlüksatırları oluşturur. Mahsup hesabı varsayılan olarak gider entegrasyonu hesabıdır. Deftere nakil tümleştirmesi günlüğü, masraf hareketinin hesap bakiyesini temizler ve gider tutarını proje maliyeti hesabına taşır. Sistem Ayrıca, aşağı akış ve gelir kabulü amaçları için proje alt muhasebe hareketleri de oluşturulur.
