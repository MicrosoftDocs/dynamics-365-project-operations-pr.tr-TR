---
title: Project Operations denemelerine kaydolma
description: Bu konu, Dynamics 365 Project Operations denemesi dağıtma hakkında bilgi sağlar.
author: ruhercul
ms.date: 08/19/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e9c0d81591061f0ff01200dd5fd634a4a9ff31e4
ms.sourcegitcommit: 0e5de344f2040075ba431918a4499a80510458d9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/25/2021
ms.locfileid: "7418481"
---
# <a name="sign-up-for-project-operations-trials"></a>Project Operations denemelerine kaydolma 

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı - anlaşmadan proforma faturaya, stoklu/ürün tabanlı senaryolar için Project Operations_ 

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Bu konu, önizleme işortağı teklifine nasıl abone olacağınızı ve nasıl Dynamics 365 Project Operations ortamı dağıtacağınızı açıklar.

Yeni Project Operations denemesiyle, en iyi dağıtım yaklaşımını öneren bir soru formunu tamamlayarak desteklenen üç dağıtım senaryosundan birini otomatik olarak dağıtabilirsiniz. Bu konu aşağıdakilerin nasıl yapılacağı hakkında bilgi sağlar:

- Deneme teklifinizi kullanma.
- Sağlamayı başlatma.
- Çift yazma yapılandırma.
- Project Operations hakkında daha fazla bilgi edinin. 

Aşağıdaki tabloda yeni deneme teklifinizin ayrıntıları özetlenmektedir.

| **Teklif öğesi**               | **Ayrıntılar**                                  |
|------------------------------|----------------------------------------------|
| Teklif türü                   | Bu teklif türü Yönetim lideri olduğundan, kullanmak için bir kiracı yöneticisi gereklidir. |
| Teklif kullanımı                    | Her kiracı için tek bir kez                          |
| Teklif süresi               | 30 takvim günü                             |
| Kiracı başına kullanımlar       | 1                                            |
| Kullanıcı sayısı              | 25                                           |
| Dahili                    | 1 uzatma, 30 takvim günü               |
| Deneme ortamı sayısı | 3                                            |


## <a name="admin-trial-details"></a>Yönetici denemesi ayrıntıları
Aşağıdaki tabloda, deneme ayrıntıları ve bunların her bir dağıtım türüne nasıl uygulandığı listelenmektedir.

| **Kalem**                      | **Lite**                                     | **Stoğu tutulmayan malzemeler** | **Stoklu malzemeler** |
|-------------------------------|----------------------------------------------|---------------------------|-----------------------|
| Kurulum verileri sağlanır           | Evet                                          | Evet                       | Evet (USSI)            |
| İşlem verileri            | No                                           | No                        | No                    |
| Dakika olarak sağlama süresi  | 15                                           | 90                        | 30                    |
 
## <a name="prerequisites"></a>Ön koşullar
Dynamics 365 Project Operations denemesini dağıtmak için aşağıdaki önkoşullar gerekir.

- [Dynamics 365 Project Operations - Önizleme Denemesi](https://www.aka.ms/try-po) için kaydolun.
- Önizlemeyi dağıtan kullanıcının Azure kiracısı genel yönetici haklarına sahip olması gerekir.

> [!IMPORTANT]
> Bir kuruluşta yalnızca bir kişinin (kiracı yöneticisi) bu görevi gerçekleştirmesi gerekir. Bu sürüme abone değilseniz kuruluşunuzun kaydolup kullanıcı kimlik bilgilerinizi alana kadar bekleyin.

### <a name="dynamics-365-project-operations---preview-trial"></a>Dynamics 365 Project Operations - Önizleme denemesi 

Başlamadan önce, Project Operations önizlemesini istediğiniz kiracıdaki kullanıcı iş hesabıyla tarayıcıda oturum açın.

1. Tarayıcı URL'sine yapıştırarak **Dynamics 365 Project Operations - Önizleme Denemesi** ilk teklif kodunu kullanın.

    ![Teklifi Kullanma](./media/16RedeemFirstOfferNew.png)

2. Siparişinizi onaylayın.

    ![Siparişi onaylayın](./media/17ConfirmOrderNew.png)

  Teklifinin başarıyla kullanıldığına ilişkin onay görürsünüz.

   ![Onay](./media/18OrderConfirmationNew.png)

  [Power Platform yönetici merkezine](https://admin.powerplatform.microsoft.com/projectoperationstrial) yönlendirilirsiniz.

## <a name="questionnaire-and-provisioning"></a>Soru formu ve sağlama

1.  [Power Platform yönetim merkezine](https://admin.powerplatform.com/projectoperationstrial) gidin ve soru formunu doldurun.  
2.  Önerilen dağıtım türünü gözden geçirin ve sağlamayı başlatmak için **Kuruluma Başla**'yı seçin.
3.  Hüküm ve koşulları gözden geçirin ve sonra **Başlat**'ı seçin.

   Sağlama işlemi başladıktan sonra, Power Platform yönetim merkezindeki ortam listesine yönlendirilirsiniz. Sağlama devam ederken, ortamınızın durumu **PreparingInstance** olur.
 
  Sağlama işlemi tamamlandıktan sonra, ortamınızın durumu **Hazır** olur.
 
4.  Sağlama tamamlandığında, dağıtımı doğrulamak için ilgili Microsoft Dataverse URL'sini ve Finance and Operations uygulamalarını seçin.

## <a name="demo-data-installation"></a>Demo verileri yükleme

Hem stoğu tutulmayan malzemeler hem de Lite dağıtım senaryoları için demo veri paketlerine erişmek üzere aşağıdaki bağlantıları kullanın. 
- [Stoğu tutulmayan malzemeler demo verileri](resource-apply-pro-setup-config-data.md)
- [Lite demo verileri](lite-apply-demo-setup-config-data.md)

## <a name="configuring-dual-write"></a>Çift yazmayı yapılandırma
Yalnızca stoğu tutulmayan malzeme dağıtımları için ikili yazma eşlemelerinizi yapılandırın. Daha fazla bilgi için bkz. [Project Operations çift yazma eşlemesi sürümleri](resource-dual-write-maps.md).

## <a name="assign-licenses"></a>Lisans atama

Aşağıdaki adımları tamamlamak için kuruluşunuzun Microsoft 365 Portalı'na yönetim erişimine sahip olmanız gerekir.

1. Lisansları kullanıcılarınıza atamak için [Microsoft 365 yönetim merkezine](https://portal.office.com/) gidin.

   ![Yönetim merkezi giriş sayfası](./media/14AdminPortal.png)

2. **Etkin kullanıcılar** sayfasında lisans atamak istediğiniz kullanıcıları seçin.

   ![Lisans Atama](./media/15AssignLicenses.png)

3. **Dynamics 365 Project Operations** Önizleme lisansının seçili olduğunu doğrulayın ve **Değişiklikleri kaydet**'i seçin.

## <a name="additional-resources"></a>Ek kaynaklar

Aşağıdaki kaynaklar, Project Operations yolculuğunuza başlarken yararlı yönergeler sağlar:

- [Video Serileri - Project Operations'a genel bakış, özellik ayrıntıları ve yol haritası](https://youtube.com/playlist?list=PLcakwueIHoT_LJ3Fr1tHnkPk5lioqE6uH)
- [Dynamics 365 Project Operations](/learn/modules/examine-dynamics-365-project-operations/)
- [Dağıtımınızın türünü belirleme](determine-deployment-type.md)

## <a name="frequently-asked-questions"></a>Sık sorulan sorular

### <a name="what-if-i-require-alm-or-elm-for-my-finance-and-operations-apps-environment"></a>Finance and Operations uygulamaları ortamım için ALM veya ELM gerekiyorsa ne olacak?

- Tam ortam yaşam döngüsü yönetimi özellikleri gerekli olan iş ortakları için yeni iş ortağı teklifini incelemek üzere [İş Ortağı Korumalı Alan Lisans İsteği](https://experience.dynamics.com/requestlicense) bölümüne bakın. 
- Dahili Kullanım Hakları hakkında daha fazla bilgi arayan iş ortakları [Dahili Kullanım Hakları bulut ve yazılım avantajı (microsoft.com](https://partner.microsoft.com/membership/internal-use-software) bölümüne bakabilir.

### <a name="can-i-extend-my-trial-beyond-30-days"></a>Deneme sürümünü 30 günden fazla uzatabilir miyim?
Deneme sürenizi uzatmak için aşağıdaki adımları gerçekleştirin.

1. **Microsoft 365 Yönetim Merkezinde**, **Fatura** > **Ürünleriniz**'e gidin.
2. **Dynamics 365 Project Operations (CE) - Önizleme Denemesi**'ni seçin.
3. **Son Kullanma tarihi** altında **Tarihi Uzat**'ı seçin.

### <a name="can-i-upgrade-from-the-lite-deployment-to-the-resourcenon-stocked-based-scenario-deployment"></a>Lite dağıtımından kaynak/stoğu tutulmayan tabanlı senaryo dağıtımına yükseltme yapabilir miyim?
Şu anda, bir ortamı Lite ortamından stoğu tutulmayan tabanlı dağıtıma yükseltme desteği yoktur.

### <a name="can-i-access-lifecycle-services-lcs-for-my-finance-environments"></a>Finance ortamlarım için Lifecycle Services'a (LCS) erişebilir miyim?  
No Bu denemeler için, dağıtım Power Platform Yönetim Merkezi aracılığıyla gerçekleştirilir. Finance ortamına erişim kısıtlıdır.

### <a name="can-i-install-my-trial-on-an-existing-environment"></a>Deneme sürümümü mevcut bir ortama yükleyebilir miyim?
Mevcut bir ortamınız varsa, Power Platform Yönetim Merkezi'nden mevcut bir satış Dataverse ortamına Lite dağıtımını yüklemenize izin verilir.

[!INCLUDE[footer-include](../includes/footer-banner.md)]