---
title: Finance ortamınızda Project Operations uygulamasını güncelleştirme
description: Bu makalede, Dynamics 365 Finance ortamınızda Project Operations'ı güncelleştirme hakkında bilgi sağlanmaktadır.
author: ruhercul
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: aedfd815521054d58944496500aa03a27be9267b
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/18/2022
ms.locfileid: "9030059"
---
# <a name="update-project-operations-in-your-finance-environment"></a>Finance ortamınızda Project Operations uygulamasını güncelleştirme

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_


Bu makalede, Dynamics 365 Finance ortamınızda Dynamics 365 Project Operations'ı güncelleştirme hakkında bilgi sağlanmaktadır. Project Operations uygulamasını Güncelleştirme 5'e (UR5) güncelleştirmek için üç yordam gerekir:

- [Paketi, önizleme projenize içeri aktarma](#import)
- [Güncelleştirmeyi uygulama](#apply)
- [Dataverse ortamınızı güncelleştirme](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a>Paketi, LCS projenize içeri aktarma

1. [Lifecycle Services (LCS)](https://lcs.dynamics.com/) portalında Proje Sahibi veya Ortam yöneticisi olarak oturum açın.
2. Proje listesinden LCS projenizi seçin.
3. **Proje** sayfasındaki **Ortamlar** grubunda güncelleştirmek istediğiniz ortamı açın.
4. Ortamın çalıştığını doğrulayın. Başlatılmamışsa ortamı başlatın.
5. **Kullanılabilir güncelleştirmeler** altındaki **Yeni sürüm** bölümünde, 10.0.15 için **Güncelleştirmeyi görüntüle**'yi seçin.

![Güncelleştirmeyi görüntüle düğmesi.](media/view-update.png)

6. **İkili güncelleştirmeler** sayfasında, **Paketi kaydet**'i seçin.
7. **Güncelleştirmeleri incele ve kaydet** sayfasında, **Paketi kaydet**'i seçin.
8. Açılan **Paketi varlık kitaplığına kaydet** bölmesinde, paket adını girin ve ardından **Paketi kaydet**'i seçin.
9. LCS, paketi kaydetmeyi bitirdiğinde **Bitti** düğmesi etkinleştirilir. **Bitti**'yi seçin. LCS, paketi doğrular. Doğrulama birkaç dakika veya bir saat kadar sürebilir.


## <a name="apply-the-package-update"></a><a name="apply"></a>Paket güncelleştirmesini uygulama

1. LCS'de **Ortam ayrıntıları** sayfasında, **Bakım Yap** > **Güncelleştirmeleri Uygula**'yı seçin.
2. Listeden daha önce kaydettiğiniz paketi seçin ve ardından **Uygula** seçeneğini belirleyin.
3. Paketi dağıtmak istediğinizi onaylamak için **Evet**'i seçin.

![Paket dağıtımını onayla iletişim kutusu.](media/confirm-package-deployment.png)

4. Uygulamayı güncelleştirmek istediğinizi onaylamak için **Evet**'i seçin.

![Uygulama güncelleştirmesini onayla iletişim kutusu.](media/confirm-application-update.png)

Dağıtım ve uygulama güncelleştirmesi başlar. 

Sağ üst köşedeki **Ortam ayrıntıları** sayfasında ortam durumu **Bakım** olarak güncelleştirilir. Güncelleştirme yaklaşık iki saat içinde tamamlanır. Uygulama sürüm bilgileri **Microsoft Dynamics 365 for Finance and Operations 10.0.15** olarak ve ortam durumu **Dağıtıldı** olarak güncelleştirilir.


## <a name="update-your-dataverse-environment"></a><a name="update"></a>Dataverse ortamınızı güncelleştirme

1. [Power Platform yönetim merkezi](https://admin.powerplatform.com/)'nde oturum açın.
2. Listede, Project Operations'ı yüklemek için kullandığınız ortamı bulun ve açın.
3. **Ortamlar** sayfasında, **Kaynak** > **Dynamics 365 uygulamaları**'nı seçin.
4. Listede, **Microsoft Dynamics 365 Project Operations** uygulamasını bulun ve **Durum** sütununda **Güncelleştirme Mevcut**'u seçin.
5. **Hizmet Koşulları'nı kabul ediyorum** onay kutusunu seçin ve ardından **Güncelleştir**'i seçin. Çözümün en son sürümü yüklenir.

Yükleme tamamlandıktan sonra 4.5.0.134 sürümüne sahip olursunuz.

## <a name="configure-new-features"></a>Yeni özellikleri yapılandırma

### <a name="enable-dual-write-mapping"></a>Çift yazma eşlemesini etkinleştirme

Finance ve Dataverse ortamlarında güncelleştirmeyi tamamladıktan sonra gerekli çift yazma eşlemelerini etkinleştirebilirsiniz. Çift yazma eşlemelerini etkinleştirmek için aşağıdaki yordamları tamamlayın.

- [Customer Engagement ortamında güvenlik ayarlarını güncelleştirme](#security)
- [Veri varlıklarını yenileme](#refresh)
- [Çift yazma eşlemelerini güncelleştirme ve çalıştırma](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a>Dataverse ortamında güvenlik ayarlarını güncelleştirme

Varlıklar için güvenlik ayrıcalıklarına yönelik aşağıdaki güncelleştirmeler, UR5 güncelleştirmesinin bir parçası olarak gereklidir.

1. Dataverse ortamınızda, **Ayarlar**'a gidin ve **Sistem** grubunda **Güvenlik** seçeneğini belirleyin.

![Dataverse Ortam ayarları.](media/Picture21.png)

2. **Güvenlik Rolleri**'ni seçin.
3. Roller listesinde, **çift yazma uygulaması kullanıcısı**'nı ve **Özel Varlıklar** sekmesini seçin. 
4. Rolün aşağıdakiler için **Oku** ve **Şuna Ekle** izinlerinin olduğunu doğrulayın:

      - **Para Birimi Döviz Kuru Türü**
      - **Hesap Grafiği** 
      - **Mali Takvim** 
      - **Kayıt Defteri**

5. Güvenlik rolü güncelleştirildikten sonra **Ayarlar** > **Güvenlik** > **Takımlar**'a gidin. Takıma **çift yazma uygulaması kullanıcısı** rolünün uygulandığını doğrulayın. 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a>Veri varlıklarını güncelleştirmeyi kullanarak yenileme

1. Finance ortamınızda **Veri yönetimi** çalışma alanını açın ve ardından **Framework parametreleri** sayfasını açın.
2. **Varlık ayarları** sekmesinde, **Varlık listesini yenile**'yi seçin.
3. Varlık yenilemesini onaylamak için **Kapat**'ı seçin.

 > [!NOTE]
 > Bu işlemin tamamlanması yaklaşık 20 dakika sürer. Yenileme tamamlandığında bilgilendirilirsiniz.

### <a name="update-dual-write-mappings"></a><a name="run"></a>Çift yazma eşlemelerini güncelleştirme

1. **Veri yönetimi** çalışma alanında, **Çift yazma**'yı seçin.
2. **Çözümleri uygula**'yı seçin, listeden her iki çözümü de seçin ve ardından **Uygula**'yı seçin.
3. **Çift yazma** sayfasında, aşağıdaki tablo eşlemelerini seçin ve ardından **Durdur**'u seçin.

    - **Project Operations tümleştirmesi gerçek değerleri (msdyn_actuals)**
    - **Project Operations tümleştirmesi proje gider kategorileri (msdyn_expensecategories)**
    - **Project Operations tümleştirmesi gerçek değerleri proje giderleri dışarı aktarma varlığı (msdyn_expenses)**

4. **Tablo eşleşmesi sürümü** sayfasında, üç varlığın her birine eşleşmenin yeni bir sürümünü uygulayın.
5. **Çift yazma** sayfasında, eşleşmeleri yeniden başlatmak için çalıştır seçeneğini belirleyin.
6. Eşlemeler listesinden, tüm ön koşullarıyla **Kayıt Defteri (msdyn_ledgers)** eşlemesini seçin ve **İlk eşitleme** onay kutusunu seçin. 
7. **İlk eşitleme için ana öğe** alanında, **Finans ve operasyon uygulamaları**'nı seçin ve ardından **Çalıştır** seçeneğini belirleyin.
 
 ![Kayıt Defteri eşleme eşitlemesi.](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]