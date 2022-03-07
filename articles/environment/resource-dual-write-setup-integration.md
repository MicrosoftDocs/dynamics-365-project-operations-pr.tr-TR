---
title: Project Operations kurulumu ve yapılandırma verileri tümleştirmesi
description: Bu konu, Project Operations ikili yazma eşlemelerinin ayarlanması ve yapılandırılması hakkında bilgi sağlar.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 1e9ca9407404274648f359be42d350137775ae55
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001090"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Project Operations kurulumu ve yapılandırma verileri tümleştirmesi

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Bu konu kurulum ve yapılandırma varlıkları için Project Operations iki yazma tümleştirmesiyle ilgili bilgi sağlar.

## <a name="project-contracts-contract-lines-and-projects"></a>Proje Sözleşmesi, Sözleşme Satırları ve projeler

Proje sözleşmeleri, sözleşme satırları ve projeler; daha fazla hesaplama için Dataverse uygulamasında oluşturulur ve Finance and Operations uygulamalara eşitlenir. Bu varlıklardaki kayıtlar yalnızca Dataverse uygulamasında oluşturulup silinebilir. Ancak, satış vergisi grubu Varsayılanları ve mali boyutlar gibi muhasebe öznitelikleri, Finance and Operations uygulamalarındaki bu kayıtlara eklenebilir.

  ![Proje sözleşmesi tümleştirme kavramları](./media/1ProjectContract.jpg)

Satış etkinliği müşteri adayları, fırsatlar ve teklifler Dataverse uygulamasında izlenir ve Bu etkinlikle ilişkilendirilmiş bir aşağı akış hesaplaması olmadığından Finance and Operations uygulamalara eşitlenmez.

Dataverse Uygulamasındaki proje sözleşmesi işlevi, **Proje sözleşmesi başlıkları (SalesOrders)** tablo eşlemesini kullanan Finance and Operations uygulamalarda proje sözleşme kaydı oluşturur. Proje sözleşmesini Dataverse'e kaydetme, Proje sözleşmesi müşteri varlık kaydının oluşturulmasına da başlar. Bu kayıt **proje finansmanı kaynak (msdyn\_projectcontractssplitbillingrules)** tablo haritasını kullanan Finance and Operations uygulamalarla eşitlenir . Bu harita proje sözleşmesi müşteri eklemelerini, güncelleştirmeleri ve silmeleri aynı zamanda eşitler. Faturalama yüzdelerini Proje sözleşmesi arasında bölme müşteriler yalnızca Dataverse uygulamasında ana ve Finance and Operations uygulamalarına eşitlenmemiş durumdadır.

Dataverse'de bir proje Sözleşmesinde oluşturulduktan sonra, proje muhasebecisi, **proje yönetimi ve hesap** > **projesi sözleşmeleri** > **Kurulum** > **Varsayılan muhasebeyi göster**'e giderek Finance and Operations uygulamalardaki Bu proje sözleşmesi için hesap özniteliklerini güncelleştirebilir. Muhasebeci, Dataverse uygulamasında ilgili proje sözleşme kaydını açan Finance and Operations uygulamalardaki proje sözleşme kimliğini seçerek, istenen teslim tarihi ve sözleşme tutarı gibi işlemsel Proje sözleşmesi özniteliklerini gözden geçirebilir.

Proje varlığı, **Projects v2 (msdyn\_projects)** tablo eşlemesi kullanılarak Finance and Operations uygulamalarla eşitlenir. Proje muhasebecisi şunları yapabilir:

  - **Proje yönetimi ve muhasebe** > **Tüm projeler**'e gderek Finance and Operations'ta projeleri gözden geçirin. 
  - **Proje yönetimi ve hesap** > **Tüm projeler** > **Kurulum** > **Varsayılan muhasebeyi göster**'e giderek Finance and Operations uygulamalarında proje için hesaplama özniteliklerini güncelleştirin.  
  - Dataverse Uygulamasında ilgili proje kaydını açan Finance and Operations uygulamalardaki proje kimliğini seçerek tahmini başlangıç ve bitiş tarihleri gibi işlemsel proje özniteliklerini gözden geçirin.

Proje, **Proje sözleşmesi satırı** varlığı aracılığıyla proje sözleşmesiyle ilişkilendirilmiştir.

Dataverse Uygulamasındaki proje sözleşmesi satırları, **Proje sözleşmesi satırları (salesorderdetails)** tablo eşlemesini kullanan Finance and Operations uygulamalarda proje sözleşme kaydı oluşturur. Faturalandırma yöntemi, Finance and Operations uygulamalardaki Proje sözleşmesi faturalama kural türünü tanımlar :

  - Bir saat ve malzeme faturalama yöntemine sahip Proje sözleşmesi satırları, saat ve malzeme türünde faturalama kuralı oluşturur.
  - Sabit fiyat faturalama yöntemi sözleşme satırları bir kilometre taşı faturalama kuralı oluşturun.

Proje sözleşmesi satırları, **Proje Yönetim ve muhasebe** > **Proje sözleşmeleri** > **Kurulum** > **varsayılan muhasebeyi göster**'e giderek ve **sözleşme satırları** sekmesindeki ayrıntıları gözden geçirerek, Finance and Operations uygulamalardaki proje muhasebecisi tarafından gözden geçirilebilir. Muhasebeci, bu sekmedeki sabit fiyat faturalama yöntemi sözleşme satırları için varsayılan mali boyutları da ayarlayabilir.

## <a name="billing-milestones"></a>Faturalama Kilometre Taşı

Sabit fiyatlı fatura yöntemi kullanılarak oluşturulan proje sözleşme satırları, fatura kilometre taşları aracılığıyla faturalandırılır. Fatura kilometre taşları , **Project Operations tümleştirme sözleşmesi satırı kilometre taşları (msdyn\_contractlinescheduleofvalues)** tablo eşlemesini kullanarak, Finance and Operations uygulamalardaki proje mahsup hareketleriyle eşitlenir.

  ![Faturalama Kilometre Taşı tümleştirmesi](./media/2Milestones.jpg)

Muhasebeci hesaba mahsup hareketleri gözden geçirebilir ve **proje yönetimi ve muhasebe** > **proje sözleşmeleri** > **Sürdür** > **Hesapta işlemler** veya **PRoje yönetimi ve muhasebe** > **tüm projeler** > **Sürdür** > **Hesapta işlemler**'e giderek bu işlemler için hesapta işlemler ve muhasebe özniteliklerini ayarlayın.

Belirli bir proje sözleşme satırı için ilk olarak bir faturalama kilometre taşı oluşturduğunuzda, sistem otomatik olarak bu sözleşme satırıyla ilişkilendirilen proje için sabit fiyatlı bir gelir tahmini projesi oluşturur. Sabit fiyatlı gelir tahmin projeleri **Proje yönetimi ve muhasebe** > **Sabit fiyatlı gelir tahmin etme projelerine** giderek gözden geçirilebilir.

### <a name="project-tasks"></a>Proje görevleri

Proje görevleri yalnızca başvuru amacıyla **proje görevleri (msdyn\_projecttasks)** tablosu aracılığıyla Finance and Operations uygulamalarla eşitlenir. Oluşturma, güncelleştirme ve silme işlemleri Finance and Operations uygulamalar aracılığıyla desteklenmez.

  ![Proje görevleri tümleştirmesi](./media/3Tasks.jpg)

## <a name="project-resources"></a>Proje kaynakları

**Proje kaynak rolleri** varlığı, yalnızca başvuru amacıyla tüm şirketlerin **proje kaynak rolleri (bookableresourcecategories)** tablo eşlemesi kullanılarak Finance and Operations uygulamalarla eşitlenir. Dataverse Uygulamasındaki kaynak rolleri şirkete özgü olmadığı için, sistem otomatik olarak, Çift yazma tümleştirme kapsamına dahil edilen tüm yasal varlıklar için Finance and Operations uygulamalara özgü ilgili kaynak rolleri kayıtlarını otomatik olarak oluşturur.

![Kaynak rolleri tümleştirmesi](./media/5Resources.jpg)

Project Operations proje kaynakları Dataverse uygulamasında saklanır ve Finance and Operations uygulamalarla eşitlenmez.

### <a name="transaction-categories"></a>Hareket kategorileri

İşlem kategorileri, Dataverse'te sürdürülür ve **Proje işlem kategorileir (msdyn\_transactioncategories)** Tablo eşlemesi kullanılarak Finance and Operations uygulamalara eşitlenir. Hareket kategorisi kaydı eşitlendikten sonra, sistem otomatik olarak dört paylaşılan kategori kaydı oluşturur. Her kayıt, Finance and Operations uygulamalardaki bir hareket türüne karşılık gelir ve bunları hareket kategorisi kaydıyla bağlantılandırır.

![İşlem kategorileri tümleştirmesi](./media/4TransactionCategories.jpg)

Tahminler ve gerçekler için hareket kategorileri kullanılması, her yasal varlıkta karşılık gelen proje kategorilerini oluşturmak için proje muhasebeci veya sistem Yönetici gerekir. Daha fazla bilgi için bkz. [Proje kategorilerini yapılandırma](../project-accounting/configure-project-categories.md).
