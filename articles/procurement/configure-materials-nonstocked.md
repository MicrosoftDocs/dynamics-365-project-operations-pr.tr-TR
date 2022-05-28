---
title: Stoğu tutulmayan malzemeleri ve bekleyen satıcı faturalarını yapılandırma
description: Bu konu, stoklanmayan malzemelerin ve bekleyen satıcı faturalarının nasıl etkinleştirileceğini açıklar.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1b14ab17a317e7082bc9c24709590745a5c48ea8
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8592992"
---
# <a name="configure-non-stocked-materials-and-pending-vendor-invoices"></a>Stoğu tutulmayan malzemeleri ve bekleyen satıcı faturalarını yapılandırma

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

## <a name="minimum-version-requirement"></a>Gereken en düşük sürüm

Stoklanmayan malzemelerin ve bekleyen Satıcı faturalarının kullanılması Dynamics 365 Project Operations stoğu olmayan/kaynak tabanlı senaryolar için aşağıdaki sürümleri gerekir:

Dynamics 365 Dataverse çözümleri:

- Project Operations – 4.9.0.221 veya üzeri
- Çift yazma uygulaması düzenleme çözümü - 2.2.2.23 veya üstü

Dynamics 365 Finance:
- 10.0.18 (10.0.793.52) veya üzeri. Finance ortamınızın güncel olduğundan ve tüm kalite güncelleştirmelerinin minimum sürüm gereksinimlerini karşılayacak şekilde uygulandığından emin olun.

## <a name="run-dual-write-maps-for-non-stocked-materials-and-vendor-invoice-integration"></a>Stoklanmayan malzemeler ve Tedarikçi faturası tümleştirmesi için çift-yazılır eşlemeler çalıştırın.

Bu bölümde, Stoklanmayan malzemeler ve satıcı faturaları için gerekli olan eşlemelerle ilgili bilgiler yer almaktadır. [Yeni bir ortam sağlama](../environment/resource-provision-new-environment.md#run-project-operations-dual-write-maps) konusunda listelenen ön koşul eşlemelerinin ortamınızda çalıştığını doğrulayın.

1. Lifecycle Services'e (LCS) gidin, LCS projenize gidin ve **ortam ayrıntıları** sayfasına gidin.
2. **Common Data Service Ortam bilgileri** bölümünde, **Uygulamalar için CDS bağlantısı**'nı seçin. Bağlantıyı seçtikten sonra, eşlemelerdeki varlık listesine yönlendirilirsiniz.
3. Aşağıdaki haritaların çalıştığından emin olun. Çalışmıyorsa, bunları başlatın ve tüm ilgili tablo haritalarını eklediğinizden emin olun.

    - Piyasaya sürülen CDS farklı ürünler (Ürünler)
    - Satıcılar v2 (msdyn_vendors)
    - Malzeme tahminleri için Project Operations tablosu (msdyn_estimatelines)
    - Project Operations tümleştirme projesi satıcı fatura dışa aktarma varlığı (msdyn_projectvendorinvoices)
    - Project Operations tümleştirme projesi satıcı faturası satırı dışa aktarma varlığı (msdyn_projectvendorinvoicelines)
    - Project Operations tümleştirmesi gerçek değerleri (msdyn_actuals). Eşleme sürümü 1.0.0.14 veya üstü çalıştırdığınızdan emin olun. Haritanın etkin sürümünü **çift yazma** sayfasındaki **sürüm** sütununda görebilirsiniz. Yeni bir harita sürümünü, **tablo Haritası sürümlerini** seçip ardından seçili sürümü kaydederek etkinleştirebilirsiniz.

Standart gösteri verilerini kullanıyorsanız, ilk eşitleme ile aşağıdaki varlık eşlemelerini durdurup yeniden başlatmanız da gerekebilir:
  - Ödeme günleri CDS v2 (msdyn_paymentdays)
  - Ödeme zamanlaması (msdyn_paymentschedules)
  - Ödeme koşulları (msdyn_paymentterms)
  - Satıcı grupları (msdyn_vendorgroups)
  - Birimler (UOM)

> [!NOTE]
> Satıcı grupları ve birimleri için ilk eşitleme, varolan gösteride veri kümesi birkaç kayıt için başarısız olabilir. Hataları yok sayabilirsiniz; Bu hatalar, Project Operations ile gösteri verilerini kullanmaktan engellemediklerinden ortaya çıkmasını önleyebilirsiniz.

## <a name="configure-prerequisites-in-dataverse"></a>Dataverse'te Ön koşulları yapılandırma

### <a name="activate-workflow-to-create-accounts-based-on-vendor-entity"></a>Satıcı varlığına göre firmalar oluşturmak için iş akışını etkinleştirin.

Çift yazma düzenleme çözümü, [satıcı ana tümleştirmesi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-mapping) sağlar. Bu özelliğin ön koşul olarak, satıcı verilerinin **firmalar** varlığında oluşturulması gerekir. [Satıcı tasarımları arasında geçiş](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-switch) olarak açıklandığı gibi **firmalar** tablosunda satıcılar oluşturmak için bir şablon iş akışı işlemini etkinleştirin.

### <a name="set-products-to-be-created-as-active"></a>Ürünleri etkin olarak oluşturulacak şekilde ayarlama

Stoklanmayan malzemeler, Finance'te içinde **serbest bırakılan ürünler** olarak konfigüre edilmiş olmalıdır . Çift Yazma Düzenleme çözümü, [Dataverse ürün kataloğuna yayınlanmış kullanıma hazır ürün entegrasyonu](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/product-mapping) sağlar. Varsayılan olarak, Finance ürünleri Dataverse'e taslak olarak eşitlenir. Malzeme kullanımı veya bekleyen satıcı faturalarında doğrudan kullanılabilmesi için ürünü etkin bir durumla eşitlemek için, **sistem** > **Yönetim** > **Sistem Yönetimi** > **sistem ayarları**'na gidin ve **Satışlar** sekmesinde, **etkin durumdayken ürün oluştur**'u **Evet**'e ayarlayın.

## <a name="configure-prerequisites-in-finance"></a>Finance'te Ön koşulları yapılandırma

### <a name="enable-the-feature-key-for-pending-vendor-invoices"></a>Bekleyen satıcı faturaları için özellik anahtarını etkinleştirme

Bekleyen satıcı faturası satırlarına proje ayrıntıları eklemek için işlevleri etkinleştirmek üzere aşağıdaki adımları uygulayın.

1. Finance'te, **Özellik Yönetimi** çalışma alanına gidin.
2. Özellik listesinde, **kaynak tabanlı/Stoklanmayan senaryolar özelliği için Project Operations'da bekleyen satıcı faturalarını etkinleştir**'i bulun ve **Etkinleştir**'i seçin.

### <a name="define-category-groups-and-project-categories-for-items"></a>Maddelerle ilgili kategori gruplarını ve Proje kategorilerini tanımlama

**Öğe** işlem türü için en az bir kategori grubunu ve bu grubu kullanan en az bir proje kategorisini yapılandırın. Daha fazla bilgi için bkz. [Proje kategorilerini yapılandırma](../project-accounting/configure-project-categories.md#category-groups).

Proje maliyet ve gelir profillerini gözden geçirin ve madde hareketleri için genel muhasebeye nakil ayarını yapılandırın. Daha fazla bilgi için bkz. [Faturalandırılabilir projelerin muhasebesini yapılandırma](../project-accounting/configure-accounting-billable-projects.md).

### <a name="set-up-a-write-in-product"></a>Serbest Eklenen Ürün ayarlama

Project Operations, yayınlanmış ürün kataloğu ve serbest ürün kataloğunda yapılandırılan Katalog ürünlerinin malzeme tahminlerini ve kullanımını kaydedebilirsiniz. Yazma ürünlerinin kullanılması için, bu amaçla Finance'de yapılandırılmış tek bir yayınlanmış ürün gerekir. Bir serbest ürün yapılandırmak için aşağıdaki adımları izleyin. Kaynak/Stoklanmayan senaryolar için Project Operations kullanan her yasal varlıkta bu adımları yineleyin.

1. Finance'de **ürün bilgileri yönetimi** > **ürünler** > **yayımlanmış ürünler** bölümüne gidin ve **yeni**'yi seçin.
2. **Ürün türü** alanında, **Madde**'yi seçin ve **ürün alt türü** alanında, **ürün**'ü seçin.
3. Ürün numarasını (WRITEIN) ve ürün adını (serbest ürün) girin.
4. Madde modeli grubunu seçin. Seçtiğiniz madde modeli grubunda **Stok ilkesi stoğu ürün** alanının **yanlış** değerine ayarlanmış olduğundan emin olun.
5. **Madde grubu**, **depolama boyutu grubu** ve **izleme boyutu grubu** alanlarındaki değerleri seçin. Yalnızca **Site** için **Depolama boyutu**'nu kullanın ve **İzleme boyutları** alanında **Hiçbiri**'ni seçin.
6. **Stok birimi**, **Satınalma birimi** ve **Satış birimi** alanındaki değerleri seçin ve ardından değişikliklerinizi kaydedin.
7. **Plan** sekmesinde, varsayılan sipariş ayarlarını ayarlayın ve **Stok** sekmesinde varsayılan tesis ve ambarı ayarlayın.
8. **Proje yönetimi ve hesaplama** > **ayar** > **Proje yönetimi ve hesap oluşturma parametreleri**'ne gidin ve **Dynamics 365 Dataverse'te Project Operations**'ı açın. 
9. **Malzemeler** sekmesinde, **serbest ürün** alanında, oluşturduğunuz ürünü seçin.
10. Dataverse ortamınızda, site haritasında, **Ürünler** varlığını açın ve serbest ürün kaydını bulun. 
11. Kayıt ayrıntılarını açın ve ürün durumunu **kullanımdan kaldırma** olarak ayarlayın. Bu ürün durumu, malzeme tahminleri ve kullanım belgelerinde bu kaydı doğrudan yanlışlıkla kullanmalarını engeller.

### <a name="set-up-a-procurement-integration-account"></a>Satın alma entegrasyonu hesabı ayarlama

Satın alma tümleştirmesi hesabı, bir projeye ait satırları bulunan ve bekleyen bir satıcı faturasını deftere naklederken bir takas hesabı olarak kullanılır.

Sistem bekleyen bir satıcı faturasını deftere naklettiğinde, bu hesap proje maliyet tutarı için kullanılır. Satıcı faturası ayrıntıları Dataverse uygulamasında işlenir ve ilgili proje fiili oluşturulur. Gerçek proje bilgileri Project Operations tümleştirme günlüğüne eklenir. Tümleştirme günlüğünü deftere naklederken, miktar satın alma tümleştirmesi hesabından temizlenir ve proje maliyetine kaydedilir.

1. Hazırlık tümleştirme hesabı ayarlamak için **Proje yönetimi ve hesap** > **kurulum** > **Proje yönetimi ve muhasebe parametreleri**'ne gidin ve **Dynamics 365 Dataverse'te Project Operations**'ı açın. 
2. **Malzemeler** sekmesini seçin ve **tedarik entegrasyonu hesabı** alanında bir değer seçin.

#### <a name="set-up-project-category-defaults-for-an-item"></a>Bir öğe için proje kategori varsayılanlarını ayarlama

1. Finance'te **Proje yönetimi ve hesaplama** > **ayar** > **Proje yönetimi ve hesap oluşturma parametreleri**'ne gidin ve **Dynamics 365 Dataverse'te Project Operations**'ı açın. 
2. **Proje kategori Varsayılanları** sekmesinde, **öğe** alanında bir değer seçin. Bu proje kategorisi, proje kategorisi proje fiili kaydı üzerinde ayarlanmamışsa malzeme hareketleri için kullanılır.
