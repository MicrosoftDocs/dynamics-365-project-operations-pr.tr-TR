---
title: Yeni bir ortam sağlama
description: Bu konuda, yeni bir Project Operations ortamı sağlama hakkında bilgiler sağlanmaktadır.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9ed502a1312b702e029d8910d62f72b8e0e4df06
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643016"
---
# <a name="provision-a-new-environment"></a>Yeni bir ortam sağlama

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Bu konu, kaynağı/stoğu tutulmayanları temel alan senaryolar için yeni bir Dynamics 365 Project Operations ortamı hazırlama hakkında bilgi sağlar.

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>LCS projesinde Project Operations otomatik sağlama işlevini etkinleştirme

LCS projenizde Project Operations otomatik sağlama akışını etkinleştirmek için aşağıdaki adımları kullanın.

1. [LCS](https://lcs.dynamics.com/v2) öğesine gidin ve **Önizleme Özelliği yönetimi** kutucuğunu seçin.
2. **Önizleme özelliği** listesinde, **Project Operations Özelliği**'ni seçin ve Project Operations'ı etkinleştirmek için **Önizleme özelliği etkin** seçeneğini belirleyin.

> [!NOTE]
> Bu adım, her LCS projesi için yalnızca bir kez gerçekleştirilir.

## <a name="provision-a-project-operations-environment"></a>Project Operations ortamı sağlama

1. Yeni bir Dynamics 365 Finance [demo ortamı](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) veya [korumalı alan/ üretim ortamı](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) dağıtımı açın. 
2. **Ortam sağlama** sihirbazını adım adım inceleyin. 

> [!IMPORTANT]
> Seçili uygulama sürümünün 10.0.13 veya üstü olduğundan emin olun.

3. Project Operations'ı sağlamak için **Gelişmiş ayarlar** altında **Common Data Service** seçeneğini belirleyin. 
4. **Common Data Service Ayarı**'nı etkinleştirmek için **Evet**'i seçin ve ardından gerekli alanlara bilgileri girin:

  - Veri Akışı Adı
  - Bölge
  - Dil
  - Para birimi
 
5. **Common Data Service Şablonu** alanında, **Project Operations**'ı seçin 

6. Dağıtımınız için ortam türünü seçin. Abonelik tabanlı deneme sürümü 30 gün boyunca bir CDS ortamını dağıtmanızı sağlar. 

![Dağıtım Ayarları](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> Hizmet koşullarını kabul etmek için **Kabul Et**'i ve ardından dağıtım ayarlarına dönmek için **Bitti**'yi seçin.

![Dağıtım Onayı](./media/2DeploymentConsent.png)

7. Sihirbazdaki kalan gerekli alanları doldurun ve dağıtımı onaylayın. Ortam sağlama süresi ortam türüne göre değişir. Sağlama işlemi altı saat kadar sürebilir.

  Dağıtım başarıyla tamamlandıktan sonra, ortam **Dağıtıldı** olarak görünür.

8. Ortamın başarıyla dağıtıldığını doğrulamak için **Oturum Aç**'ı seçin ve onaylamak üzere ortamda oturum açın.

![ Ortam Ayrıntıları](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a>Project Operations Finance demo verilerini uygulama (isteğe bağlı adım)

Project Operations Finance demo verilerini 10.0.13 hizmet sürümü Bulutta Barındırılan Ortama [bu makalede](resource-apply-finance-demo-data.md) anlatıldığı gibi uygulayın.

## <a name="apply-updates-to-the-finance-environment"></a>Finance ortamına güncelleştirmeleri uygulama

Project Operations, uygulama sürümü **10.0.13 (10.0.569.20009)** veya üstü olan bir Finance ortamı gerektirir.

Bu sürümü almak için Finance ortamınıza kalite güncelleştirmeleri uygulamanız gerekebilir.

1. LCS'de, **Ortam ayrıntıları** sayfasının **Kullanılabilir Güncelleştirmeler** bölümünde **Güncelleştirmeyi Görüntüle**'yi seçin.

![Güncelleştirmeleri Görüntüle](./media/5ViewUpdates.png)

2. **İkili güncelleştirmeler** sayfasında, **Paketi kaydet**'i seçin.

![Paketi kaydetme](./media/6SavePackage.png)

3. **Tümünü seç**'e tıklayın ve ardından **Paketi kaydet**'i seçin.

![Güncelleştirmeleri gözden geçirme ve kaydetme](./media/7ReviewAndSaveUpdates.png)

4. Paketin adını ve açıklamasını girin ve ardından **Kaydet**'i seçin. İnternet bağlantısına bağlı olarak bu işlem biraz zaman alabilir.

![Paketi Varlıklar Kitaplığı'na yükleme](./media/8UploadPackageToAssetsLibrary.png)

5. Paket kaydedildikten sonra, **Bitti**'yi seçin ve bu paketi LCS projenizdeki Varlıklar kitaplığına kaydedin.

Paketi kaydetme ve doğrulama işlemi yaklaşık 15 dakika sürebilir.

6. Güncelleştirmeyi uygulamak için LCS içindeki **Ortam ayrıntıları** sayfasına gidin ve **Bakım** > **Güncelleştirmeleri uygula**'yı seçin.

![Ortamları Koruma](./media/9MaintainEnvironment.png)

7. Güncelleştirmeler listesinde, oluşturduğunuz paketi seçin ve **Uygula** seçeneğini belirleyin.

![Güncelleştirmeleri Uygulama](./media/10ApplyUpdates.png)

Ortamın bakımı biraz zaman alır. Tamamlandıktan sonra, ortam dağıtıldı durumuna geri döner.

![Ortam Dağıtıldı](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a>Çift Yazma bağlantısı kurma 

1. LCS projenizde **Ortam ayrıntıları** sayfasına gidin.
2. **Common Data Service Ortam Bilgileri** altında, **Uygulamalar için CDS bağlantısı**'nı seçin.
3. Bağlantı tamamlandıktan sonra, **Uygulamalar için CDS bağlantısı**'nı tekrar seçin. Finance uygulamasında Çift Yazma alanına yönlendirilirsiniz.

![CDS bağlantısı](./media/12LinktoCDS.png)

4. Tümleştirmede eşlenecek varlıklara erişmek için **Çözümü Uygula**'yı seçin.

![Çözümleri Uygulama](./media/13ApplySolutions.png)

5. **Dynamics 365 Finance and Operations Çift Yazma Varlık Eşlemesi** ve **Dynamics 365 Project Operations Çift Yazma Varlık Eşlemeleri** çözümlerini seçin ve ardından **Uygula** seçeneğini belirleyin.

![Çözümleri Onaylama](./media/14ConfirmSolutions.png)

Çözümler uygulandıktan sonra, Çift Yazma varlıkları ortama uygulanır.

![Çözümleri Uygulama](./media/15ApplyingSolutions.png)

Varlıklar uygulandıktan sonra, kullanılabilir tüm eşlemeler ortam içinde listelenir.

![Çift Yazma Eşlemeleri](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a>Güncelleştirme sonrasında veri varlıklarını yenileme

1. Finance uygulamasında, **Veri yönetimi** çalışma alanına gidin.

![Veri Yönetimi çalışma alanı](./media/16DataManagement.png)

2. **Çerçeve parametreleri** kutucuğunu seçin.

![Çerçeve Parametreleri](./media/17FrameworkParameters.png)

3. **Varlık ayarları** sayfasında **Varlık Listesini Yenile**'yi seçin.

![Varlık Listesini Yenileme](./media/18RefreshEntityList.png)

Yenileme işlemi yaklaşık 20 dakika sürer. İşlem tamamlandığında bir uyarı alırsınız.

![Yenileme Onayı](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a>Project Operations Çift Yazma eşlemelerini çalıştırma

1. LCS projenizde **Ortam ayrıntıları** sayfasına gidin.
2. **Common Data Service Ortam Bilgileri** altında, **Uygulamalar için CDS bağlantısı**'nı seçin. Bağlantıyı seçtikten sonra, eşlemelerdeki varlık listesine yönlendirilirsiniz.
3. Eşlemeleri aşağıdaki tabloda açıklandığı gibi başlatın. Sıralamayı listelendiği gibi izlediğinizden emin olun.

| **Varlık Eşlemesi** | **Varlığı yenileme** | **İlk eşitleme** | **İlk eşitleme için ana öğe** | **Önkoşulları çalıştırma** | **Önkoşullar için ilk eşitleme** |
| --- | --- | --- | --- | --- | --- |
| **Tüm Şirketler için Proje Kaynak Rolleri (bookableresourcecategories)** | No | Evet | Common Data Service | No | Yok |
| **Tüzel kişilikler (cdm\_companies)** | No | Evet | Finance and Operations uygulamaları | No | Yok |
| **Kayıt Defteri (msdyn_ledgers)** | No | Evet | Finance and Operations uygulamaları | Evet | Evet, Finance and Operations uygulamaları |
| **Project Operations tümleştirme gerçek değerleri (msdyn\_actuals)** | No | No | Yok | Evet | No |
| **Proje sözleşme satırları (salesorderdetails)** | No | No | Yok | No | No |
| **Proje işlem ilişkilerine ait tümleştirme varlığı (msdyn\_transactionconnections)** | No | No | Yok | No | Yok |
| **Project Operations tümleştirme sözleşme satırı kilometre taşları (msdyn\_contractlinesscheduleofvalues)** | No | No | Yok | No | Yok |
| **Gider tahminleri için Project Operations tümleştirme varlığı (msdyn\_estimateslines)** | No | No | Yok | No | Yok |
| **Project Operations tümleştirme proje gideri kategorileri dışarı aktarma varlığı (msdyn\_expensecategories)** | No | No | Yok | No | Yok |
| **Project Operations tümleştirme proje giderleri dışarı aktarma varlığı (msdyn\_expenses)** | Evet | No | Yok | No | Yok |
| **Saat tahminleri için Project Operations tümleştirme varlığı (msdyn\_resourceassignments)** | Evet | No | Yok | No | Yok |


4. Varlığı yenilemek için eşleme adını seçin ve ardından **Varlıkları yenile**'yi seçin. 


![Eşlemeyi Yenileme](./media/20RefreshMapping.png)

5. Yenileme işlemi tamamlandıktan sonra eşlemeyi çalıştırın. Sonraki eşlemeyi etkinleştirebilmeniz için tablodaki eşlemenin **Çalışıyor** durumunda olduğunu doğrulayın. Daha fazla sayıda önkoşul içeren eşlemeleri çalıştırmak biraz zaman alabilir.

Önkoşullara sahip bir eşlemeyi çalıştırmak için **İlgili varlık eşlemelerini göster** seçeneğini etkinleştirin. Tabloda **Önkoşul için ilk eşitleme** ayarı **Hayır** görünüyorsa çalıştırmadan önce tüm önkoşul eşlemelerinde **İlk eşitleme** bayrağının **Kapalı** olduğunu doğrulayın.

![Eşlemeyi Çalıştırma](./media/21RunMap.png)

6. Projeyle ilgili tüm eşlemelerin çalışıyor durumunda olduğunu doğrulayın.

![Tüm Eşlemeler Çalışıyor](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a>Project Operations için CDS'de yapılandırma verilerini uygulama (isteğe bağlı)

Finans ortamına demo verileri uyguladıysanız, CDS ortamına tanıtım verilerini uygulamak için [Proje işlemleri için Common Data Service'te yapılandırma verileri ayarlama ve uygulama](resource-apply-pro-setup-config-data.md)'ya bakın.


Project Operations ortamınız artık sağlanmış ve yapılandırılmıştır. 
