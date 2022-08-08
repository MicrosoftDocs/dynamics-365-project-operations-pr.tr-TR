---
title: Project Operations kurulumu ve yapılandırma verilerini tümleştirme
description: Bu makale, Project Operations çift yazma eşlemelerinin ayarlanması ve yapılandırılması hakkında bilgi sağlar.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d03393de893c39ceb53c06a3031395f765a26f55
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029176"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Project Operations kurulumu ve yapılandırma verilerini tümleştirme

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Bu makale, kurulum ve yapılandırma varlıkları için Project Operations çift yazma tümleştirmesiyle ilgili bilgi sağlar.

## <a name="project-contracts-contract-lines-and-projects"></a>Proje sözleşmeleri, sözleşme satırları ve projeler

Proje sözleşmeleri, sözleşme satırları ve projeler, Dataverse'te oluşturulur ve ek muhasebe için finans ve operasyon uygulamalarıyla eşitlenir. Bu varlıklardaki kayıtlar, yalnızca Dataverse'te oluşturulup silinebilir. Ancak satış vergisi grubu varsayılanları ve mali boyutlar gibi muhasebe öznitelikleri, finans ve operasyon uygulamalarında bu kayıtlara eklenebilir.

  ![Proje sözleşmesi tümleştirme kavramları.](./media/1ProjectContract.jpg)

Satış etkinliği müşteri adayları, fırsatlar ve teklifler, Dataverse'te izlenir ve bu etkinlikle ilişkilendirilmiş bir aşağı akış muhasebesi olmadığından finans ve operasyon uygulamalarıyla eşitlenmez.

Dataverse'teki proje sözleşmesi özelliği, **Proje sözleşmesi üst bilgileri (salesorders)** tablo eşlemesi kullanılarak finans ve operasyon uygulamalarında proje sözleşmesi kaydı oluşturur. Proje sözleşmesininin Dataverse'e kaydedilmesi ile proje sözleşmesi müşteri varlık kaydı oluşturulmaya başlanır. Bu kayıt, **Proje finansman kaynağı (msdyn\_projectcontractssplitbillingrules)** tablo eşlemesi kullanılarak finans ve operasyon uygulamalarıyla eşitlenir. Bu eşleme, proje sözleşmesi müşteri eklemelerini, güncelleştirmeleri ve silmeleri de eşitler. Faturalandırma yüzdelerinin proje sözleşmesi müşterileri arasında bölünmesi, yalnızca Dataverse'te gerçekleştirilir ve finans ve operasyon uygulamalarıyla eşitlenmez.

Proje sözleşmesinin Dataverse'te oluşturulmasından sonra proje muhasebecisi, **Proje yönetimi ve muhasebe** > **Proje sözleşmeleri** > **Kurulum** > **Varsayılan muhasebeyi göster** bölümüne giderek proje sözleşmesinin muhasebe özniteliklerini finans ve operasyon uygulamalarında güncelleştirebilir. Muhasebeci, Dataverse'te ilgili proje sözleşmesi kaydını açan finans ve operasyon uygulamalarındaki proje sözleşmesi kimliğini seçerek istenen teslim tarihi ve sözleşme tutarı gibi operasyonel proje sözleşmesi özniteliklerini inceleyebilir.

Proje varlığı, **Projects V2 (msdyn\_projects)** tablo eşlemesi kullanılarak finans ve operasyon uygulamalarıyla eşitlenir. Proje muhasebecisi şunları yapabilir:

  - **Proje yönetimi ve muhasebe** > **Tüm projeler**'e giderek finans ve operasyon uygulamalarında projeleri inceleyin. 
  - **Proje yönetimi ve muhasebe** > **Tüm projeler** > **Kurulum** > **Varsayılan muhasebeyi göster**'e giderek finans ve operasyon uygulamalarında projenin muhasebe özniteliklerini güncelleştirin.  
  - Dataverse'te ilgili proje kaydını açan proje kimliğini seçerek finans ve operasyon uygulamalarında tahmini başlangıç ve bitiş tarihleri gibi operasyonel proje özniteliklerini inceleyin.

Projeler, **Proje sözleşmesi satırı** varlığı aracılığıyla proje sözleşmeleriyle ilişkilendirilir.

Dataverse'teki proje sözleşmesi satırları, **Proje sözleşmesi satırları (salesorderdetails)** tablo eşlemesini kullanarak finans ve operasyon uygulamalarında sözleşme faturalandırma kuralı oluşturur. Faturalandırma yöntemi, finans ve operasyon uygulamalarında proje sözleşmesi faturalandırma kuralı türünü tanımlar:

  - Zaman ve malzeme faturalandırma yöntemine sahip proje sözleşme satırları, zaman ve malzeme türünden faturalandırma kuralı oluşturur.
  - Sabit fiyat faturalandırma yöntemi olan sözleşme satırları, kilometre taşı faturalandırma kuralı oluşturur.

Finans ve operasyon uygulamalarında proje sözleşme satırları, **Proje yönetimi ve muhasebe** > **Proje sözleşmeleri** > **Kurulum** > **Varsayılan muhasebeyi göster** bölümüne gidip **Sözleşme satırları** sekmesindeki ayrıntıları inceleyerek gözden geçirilir. Muhasebeci, bu sekme üzerinden sabit fiyatlı faturalandırma yöntemi kullanan sözleşme satırları için varsayılan mali boyutları da ayarlayabilir.

## <a name="billing-milestones"></a>Faturalandırma kilometre taşları

Sabit fiyatlı faturalandırma yöntemi kullanılarak oluşturulan proje sözleşme satırları, faturalandırma kilometre taşları aracılığıyla faturalandırılır. Faturalandırma kilometre taşları, **Project Operations tümleştirmesi sözleşme satırı kilometre taşları (msdyn\_contractlinescheduleofvalues)** tablo eşlemesini kullanarak finans ve operasyon uygulamalarında proje firma işlemleriyle eşitlenir.

  ![Faturalandırma kilometre taşı tümleştirmesi.](./media/2Milestones.jpg)

Muhasebeci, **Proje yönetimi ve muhasebe** > **Proje sözleşmeleri** > **Saklama** > **Hesaba mahsup işlemler** veya **Proje yönetimi ve muhasebe** > **Tüm projeler** > **Saklama** > **Hesaba mahsup işlemler**'e giderek hesaba mahsup işlemleri inceleyebilir ve bu işlemlerin muhasebe özniteliklerini ayarlayabilir.

Belirli bir proje sözleşmesi satırı için faturalandırma kilometre taşı oluştururken sistem, otomatik olarak bu sözleşme satırıyla ilişkilendirilen proje için sabit fiyatlı bir gelir tahmini projesi oluşturur. Sabit fiyatlı gelir tahmini projeleri, **Proje yönetimi ve muhasebe** > **Sabit fiyatlı gelir tahmini projeleri**'ne giderek incelenebilir.

### <a name="project-tasks"></a>Proje görevleri

Proje görevleri, **Proje görevleri (msdyn\_projecttasks)** tablo eşlemesi aracılığıyla yalnızca başvuru amacıyla finans ve operasyon uygulamalarıyla eşitlenir. Oluşturma, güncelleştirme ve silme işlemleri, finans ve operasyon uygulamalarıyla desteklenmez.

  ![Proje görevlerini tümleştirme.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Proje kaynakları

**Proje kaynak rolleri** varlığı, **Tüm şirketler için proje kaynak rolleri (bookableresourcecategories)** tablo eşlemesi kullanılarak yalnızca başvuru amacıyla finans ve operasyon uygulamalarıyla eşitlenir. Dataverse'teki kaynak rollerinin şirketlere özgü olmaması nedeniyle sistem, çift yazma tümleştirme kapsamına giren tüm tüzel kişilikler için finans ve operasyon uygulamalarında otomatik olarak şirkete özgü kaynak rolleri oluşturur.

![Kaynak rollerini tümleştirme.](./media/5Resources.jpg)

Project Operations'taki proje kaynakları, Dataverse'te saklanır ve finans ve operasyon uygulamalarıyla eşitlenmez.

### <a name="transaction-categories"></a>İşlem kategorileri

İşlem kategorileri, Dataverse'te saklanır ve **Proje işlem kategorileri (msdyn\_transactioncategories)** tablo eşlemesi kullanılarak finans ve operasyon uygulamalarıyla eşitlenir. İşlem kategorisi kaydı eşitlendikten sonra sistem otomatik olarak dört paylaşılan kategori kaydı oluşturur. Her kayıt, finans ve operasyon uygulamalarındaki bir işlem türüne karşılık gelir ve bunları işlem kategorisi kaydına bağlar.

![İşlem kategorilerini tümleştirme.](./media/4TransactionCategories.jpg)

Tahmini ve gerçek değerler için işlem kategorilerinin kullanılması için proje muhasebecisinin ya da sistem yöneticisinin her tüzel varlıkta karşılık gelen proje kategorilerini oluşturması gerekir. Daha fazla bilgi için bkz. [Proje kategorilerini yapılandırma](../project-accounting/configure-project-categories.md).
