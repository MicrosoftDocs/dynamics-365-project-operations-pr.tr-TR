---
title: Önizleme aboneliğine kaydolma - lite
description: Bu konuda, Project Operations Lite dağıtımına (anlaşmadan proforma faturaya) abone olma ve dağıtma hakkında bilgiler sağlanmaktadır.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 44edf2613ea4b26dadbd9edc47c784c488c577de
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290068"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Önizleme aboneliğine kaydolma - lite 

Bu konuda, önizleme iş ortağı teklifine abone olma ve Dynamics 365 Project Operations lite dağıtımı: anlaşmadan proforma faturaya açıklanmaktadır.

> [!NOTE]
> Bu işlem, Project Operations'ın yaklaşan sürümlerinde değişecektir.

## <a name="prerequisites"></a>Ön koşullar

- Sizi önizlemeye katılmaya davet eden bir e-posta alırsınız. [Project Operations web sitesinde](https://dynamics.microsoft.com/en-us/project-operations/overview/) bir önizleme isteyebilirsiniz.
- Önizlemeyi dağıtan kullanıcının Azure kiracısı genel yönetici haklarına sahip olması gerekir.
- Tüm hüküm ve koşulları gözden geçirin.

## <a name="subscribe"></a>Abone ol

[Önizleme isteği](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) onayı aldığınızda Microsoft'tan e-posta ile iki teklif alırsınız. Bu teklifler, Project Operations Önizlemesi'ni dağıtmanıza olanak tanır:

- Dynamics 365 Project Operations (CRM) - Önizleme Denemesi
- Office 365 Project Operations - Önizleme Denemesi

> [!IMPORTANT]
> Kuruluşta bu görevi, kiracı yönetici olarak yalnızca bir kişinin gerçekleştirmesi gerekir. Bu sürüme abone değilseniz kuruluşunuzun kaydolup kullanıcı kimlik bilgilerinizi alana kadar bekleyin.

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Dynamics 365 Project Operations (CRM) - Önizleme Denemesi 

Başlamadan önce, Proje İşlemleri önizlemesini istediğiniz kiracıdaki kullanıcı çalışma hesabının bulunduğu bir tarayıcıda oturum açtığınızdan emin olun.

1. Tarayıcı URL'sine yapıştırarak **Dynamics 365 Project Operations (CRM) - Önizleme Denemesi** ilk teklif kodunu kullanın.

![Teklifi Kullanma](./media/16RedeemFirstOfferNew.png)

2. Siparişinizi onaylayın.
![Siparişi onaylayın](./media/17ConfirmOrderNew.png)

Onay teklifinin başarıyla kurtarıldığını göreceksiniz.

![Onay](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Office 365 Project Operations - Önizleme Denemesi

İlk teklif koduyla aynı adımları yineleyin. İlk teklif koduyla birlikte kullanılan aynı kullanıcı hesabını kullanarak ikinci teklif kodunu eklediğinizden emin olun.

## <a name="assign-licenses"></a>Lisans atama

> [!IMPORTANT]
> Aşağıdaki adımları tamamlamak için kuruluşunuzun Microsoft 365 Portalı'na yönetim erişimine sahip olmanız gerekir.


1. Kullanıcılarınıza lisans atamak için [Microsoft 365 yönetim merkezine](https://portal.office.com/) gidin.

![Yönetim merkezi giriş sayfası](./media/14AdminPortal.png)

2. **Etkin kullanıcılar** sayfasında lisans atamak istediğiniz kullanıcıları seçin.

![Lisans Atama](./media/15AssignLicenses.png)

3. **Dynamics 365 Project Operations (CRM) Önizlemesi** ve **Office 365 Project Operations - Önizlemesi** lisanslarının seçildiğini doğrulayın. 
4. **Değişiklikleri Kaydet**'i seçin.

## <a name="create-a-new-cds-environment"></a>Yeni CDS ortamı oluşturma

1. [CDS dağıtım modeli](lite-deployment.md) konusundaki yönergeleri izleyerek yeni bir Project Operations CDS dağıtım ortamı hazırlayın. Ortam türünü seçtiğinizde, **Deneme (Abonelik tabanlı)** kullandığınızdan emin olun.
![Yeni ortam](./media/19CreateEnvironment.png)

2. **Dynamics 365 uygulamalarını etkinleştir** ayarını seçin ve **Bu uygulamaları otomatik olarak dağıt**'ı boş bırakın.  
3. Ortam oluşturmak için **Kaydet**'i seçin.

![Veritabanı ekle](./media/20CreateEnvironment1.png)

4. Ortam oluşturulduktan sonra **Microsoft Dynamics 365 Project Operations** çözümünü yükleyin. 

![Çözüm Yükleme](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>CDS yapılandırması yükleme ve demo verileri ayarlama

[Demo ayarlaması ve yapılandırma verileri uygulama](lite-apply-demo-setup-config-data.md) konusundaki yönergeleri izleyerek CDS yapılandırmasını yükleyin ve demo verileri ayarlayın.


[!INCLUDE[footer-include](../includes/footer-banner.md)]