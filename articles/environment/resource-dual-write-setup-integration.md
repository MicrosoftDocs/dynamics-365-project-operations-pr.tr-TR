---
title: Project Operations kurulumu ve yapılandırma verilerini tümleştirme
description: Bu konu, Project Operations çift yazma eşlemelerinin ayarlanması ve yapılandırılması hakkında bilgi sağlar.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1ffa25ff36c39010d6aee31d928c3eaa0086c3d8
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586920"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Project Operations kurulumu ve yapılandırma verilerini tümleştirme

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Bu konu, kurulum ve yapılandırma varlıkları için Project Operations çift yazma tümleştirmesiyle ilgili bilgi sağlar.

## <a name="project-contracts-contract-lines-and-projects"></a>Proje sözleşmeleri, sözleşme satırları ve projeler

Proje sözleşmeleri, sözleşme satırları ve projeler, Dataverse'te oluşturulur ve ek muhasebe için Finans ve Operasyon uygulamalarıyla eşitlenir. Bu varlıklardaki kayıtlar, yalnızca Dataverse'te oluşturulup silinebilir. Ancak satış vergisi grubu varsayılanları ve mali boyutlar gibi muhasebe öznitelikleri, Finans ve Operasyon uygulamalarında bu kayıtlara eklenebilir.

  ![Proje sözleşmesi tümleştirme kavramları.](./media/1ProjectContract.jpg)

Satış etkinliği müşteri adayları, fırsatlar ve teklifler, Dataverse'te izlenir ve bu etkinlikle ilişkilendirilmiş bir aşağı akış muhasebesi olmadığından Finans ve Operasyon uygulamalarıyla eşitlenmez.

Dataverse'teki proje sözleşmesi özelliği, **Proje sözleşmesi üst bilgileri (salesorders)** tablo eşlemesi kullanılarak Finans ve Operasyon uygulamalarında proje sözleşmesi kaydı oluşturur. Proje sözleşmesininin Dataverse'e kaydedilmesi ile proje sözleşmesi müşteri varlık kaydı oluşturulmaya başlanır. Bu kayıt, **Proje finansman kaynağı (msdyn\_projectcontractssplitbillingrules)** tablo eşlemesi kullanılarak Finans ve Operasyon uygulamalarıyla eşitlenir. Bu eşleme, proje sözleşmesi müşteri eklemelerini, güncelleştirmeleri ve silmeleri de eşitler. Faturalandırma yüzdelerinin proje sözleşmesi müşterileri arasında bölünmesi, yalnızca Dataverse'te gerçekleştirilir ve Finans ve Operasyon uygulamalarıyla eşitlenmez.

Proje sözleşmesinin Dataverse'te oluşturulmasından sonra proje muhasebecisi, **Proje yönetimi ve muhasebe** > **Proje sözleşmeleri** > **Kurulum** > **Varsayılan muhasebeyi göster** bölümüne giderek proje sözleşmesinin muhasebe özniteliklerini Finans ve Operasyon uygulamalarında güncelleştirebilir. Muhasebeci, Dataverse'te ilgili proje sözleşmesi kaydını açan Finans ve Operasyon uygulamalarındaki proje sözleşmesi kimliğini seçerek istenen teslim tarihi ve sözleşme tutarı gibi operasyonel proje sözleşmesi özniteliklerini inceleyebilir.

Proje varlığı, **Projects V2 (msdyn\_projects)** tablo eşlemesi kullanılarak Finans ve Operasyon uygulamalarıyla eşitlenir. Proje muhasebecisi şunları yapabilir:

  - **Proje yönetimi ve muhasebe** > **Tüm projeler**'e giderek Finans ve Operasyon uygulamalarında projeleri inceleyin. 
  - **Proje yönetimi ve muhasebe** > **Tüm projeler** > **Kurulum** > **Varsayılan muhasebeyi göster**'e giderek Finans ve Operasyon uygulamalarında projenin muhasebe özniteliklerini güncelleştirin.  
  - Dataverse'te ilgili proje kaydını açan proje kimliğini seçerek Finans ve Operasyon uygulamalarında tahmini başlangıç ve bitiş tarihleri gibi operasyonel proje özniteliklerini inceleyin.

Projeler, **Proje sözleşmesi satırı** varlığı aracılığıyla proje sözleşmeleriyle ilişkilendirilir.

Dataverse'teki proje sözleşmesi satırları, **Proje sözleşmesi satırları (salesorderdetails)** tablo eşlemesini kullanarak Finans ve Operasyon uygulamalarında sözleşme faturalandırma kuralı oluşturur. Faturalandırma yöntemi, Finans ve Operasyon uygulamalarında proje sözleşmesi faturalandırma kuralı türünü tanımlar:

  - Zaman ve malzeme faturalandırma yöntemine sahip proje sözleşme satırları, zaman ve malzeme türünden faturalandırma kuralı oluşturur.
  - Sabit fiyat faturalandırma yöntemi olan sözleşme satırları, kilometre taşı faturalandırma kuralı oluşturur.

Finans ve Operasyon uygulamalarında proje sözleşme satırları, **Proje yönetimi ve muhasebe** > **Proje sözleşmeleri** > **Kurulum** > **Varsayılan muhasebeyi göster** bölümüne gidip **Sözleşme satırları** sekmesindeki ayrıntıları inceleyerek gözden geçirilir. Muhasebeci, bu sekme üzerinden sabit fiyatlı faturalandırma yöntemi kullanan sözleşme satırları için varsayılan mali boyutları da ayarlayabilir.

## <a name="billing-milestones"></a>Faturalandırma kilometre taşları

Sabit fiyatlı faturalandırma yöntemi kullanılarak oluşturulan proje sözleşme satırları, faturalandırma kilometre taşları aracılığıyla faturalandırılır. Faturalandırma kilometre taşları, **Project Operations tümleştirmesi sözleşme satırı kilometre taşları (msdyn\_contractlinescheduleofvalues)** tablo eşlemesini kullanarak Finans ve Operasyon uygulamalarında proje firma işlemleriyle eşitlenir.

  ![Faturalandırma kilometre taşı tümleştirmesi.](./media/2Milestones.jpg)

Muhasebeci, **Proje yönetimi ve muhasebe** > **Proje sözleşmeleri** > **Saklama** > **Hesaba mahsup işlemler** veya **Proje yönetimi ve muhasebe** > **Tüm projeler** > **Saklama** > **Hesaba mahsup işlemler**'e giderek hesaba mahsup işlemleri inceleyebilir ve bu işlemlerin muhasebe özniteliklerini ayarlayabilir.

Belirli bir proje sözleşmesi satırı için faturalandırma kilometre taşı oluştururken sistem, otomatik olarak bu sözleşme satırıyla ilişkilendirilen proje için sabit fiyatlı bir gelir tahmini projesi oluşturur. Sabit fiyatlı gelir tahmini projeleri, **Proje yönetimi ve muhasebe** > **Sabit fiyatlı gelir tahmini projeleri**'ne giderek incelenebilir.

### <a name="project-tasks"></a>Proje görevleri

Proje görevleri, **Proje görevleri (msdyn\_projecttasks)** tablo eşlemesi aracılığıyla yalnızca başvuru amacıyla Finans ve Operasyon uygulamalarıyla eşitlenir. Oluşturma, güncelleştirme ve silme işlemleri, Finans ve Operasyon uygulamalarıyla desteklenmez.

  ![Proje görevlerini tümleştirme.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Proje kaynakları

**Proje kaynak rolleri** varlığı, **Tüm şirketler için proje kaynak rolleri (bookableresourcecategories)** tablo eşlemesi kullanılarak yalnızca başvuru amacıyla Finans ve Operasyon uygulamalarıyla eşitlenir. Dataverse'teki kaynak rollerinin şirketlere özgü olmaması nedeniyle sistem, çift yazma tümleştirme kapsamına giren tüm tüzel kişilikler için Finans ve Operasyon uygulamalarında otomatik olarak şirkete özgü kaynak rolleri oluşturur.

![Kaynak rollerini tümleştirme.](./media/5Resources.jpg)

Project Operations'taki proje kaynakları, Dataverse'te saklanır ve Finans ve Operasyon uygulamalarıyla eşitlenmez.

### <a name="transaction-categories"></a>İşlem kategorileri

İşlem kategorileri, Dataverse'te saklanır ve **Proje işlem kategorileri (msdyn\_transactioncategories)** tablo eşlemesi kullanılarak Finans ve Operasyon uygulamalarıyla eşitlenir. İşlem kategorisi kaydı eşitlendikten sonra sistem otomatik olarak dört paylaşılan kategori kaydı oluşturur. Her kayıt, Finans ve Operasyon uygulamalarındaki bir işlem türüne karşılık gelir ve bunları işlem kategorisi kaydına bağlar.

![İşlem kategorilerini tümleştirme.](./media/4TransactionCategories.jpg)

Tahmini ve gerçek değerler için işlem kategorilerinin kullanılması için proje muhasebecisinin ya da sistem yöneticisinin her tüzel varlıkta karşılık gelen proje kategorilerini oluşturması gerekir. Daha fazla bilgi için bkz. [Proje kategorilerini yapılandırma](../project-accounting/configure-project-categories.md).
