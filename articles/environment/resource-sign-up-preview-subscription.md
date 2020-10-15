---
title: Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations önizleme aboneliklerine kaydolma
description: Bu konuda, kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations'a nasıl abone olunacağı ve Project Operations'ın nasıl dağıtılacağı hakkında bilgiler sağlanmaktadır.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949122"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations önizleme aboneliklerine kaydolma

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Bu konuda, önizleme/iş ortağı teklifine nasıl abone olunacağı ve kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations ortamının nasıl dağıtılacağı açıklanmaktadır.

## <a name="prerequisites"></a>Ön koşullar

- Sizi önizlemeye katılmaya davet eden bir e-posta alırsınız. [Project Operations web sitesinde](https://dynamics.microsoft.com/en-us/project-operations/overview/) bir önizleme isteyebilirsiniz.
- Önizlemeyi dağıtan kullanıcının Azure kiracısı genel yönetici haklarına sahip olması gerekir.
- Finance ortamını dağıtmak için ortam başına faturalanacak geçerli bir Azure aboneliği gereklidir. Başlamak için kuruluşunuzun mevcut aboneliğini veya bir [Azure deneme sürümünü](https://azure.microsoft.com/en-us/free/) kullanabilirsiniz. CDS ortamı, 30 günlük sınırlı bir süre boyunca ücretsiz olarak sağlanır.

## <a name="subscribe"></a>Abone ol

[Önizleme isteğiniz](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) onaylandığında Microsoft'tan e-posta ile iki teklif alırsınız. Bu teklifler, Project Operations Önizlemesi'ni dağıtmanıza olanak tanır:

- Dynamics 365 Project Operations: Önizleme Denemesi
- Dynamics 365 for Finance and Operations Önizleme Denemesi.

> [!IMPORTANT]
> Kuruluşta bu görevi, kiracı yönetici olarak yalnızca bir kişinin gerçekleştirmesi gerekir. Bu sürüme abone değilseniz kuruluşunuzun kaydolup kullanıcı kimlik bilgilerinizi alana kadar bekleyin.

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations: Önizleme denemesi

1. Karşılama e-postanızda sağlanan URL ile ilk teklif olan **Dynamics 365 Project Operations Denemesi**'ni kullanın.

![İlk Teklif](./media/1FirstOffer.png)

2. Hizmete abone olacak kuruluşa ait olan kullanıcı olarak oturum açtığınızdan emin olun.
3. Teklifi kullanmaya devam edin. 
4. **Evet, hesabıma ekle** seçeneğini belirleyin.

![Teklifi Kullanma](./media/2RedeemFirstOffer.png)

![Teklifi Onaylama](./media/3ConfirmFirstOffer.png)

![Teklif Kullanıldı](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a>Dynamics 365 Finance önizleme denemesi

Karşılama e-postasındaki ikinci teklif için aynı adımları tekrarlayın.

## <a name="assign-licenses"></a>Lisans Atama

> [!IMPORTANT]
> Aşağıdaki adımları tamamlamak için kuruluşunuzun Office 365 Portalı'na yönetim erişimine sahip olmanız gerekir.

1. Kullanıcılarınıza lisans atamak için [Microsoft 365 yönetim merkezine](https://portal.office.com/) gidin.

![Office Yönetim Portalı](./media/5OfficeAdminPortal.png)

2. **Etkin kullanıcılar** sayfasında lisans atamak istediğiniz kullanıcıları seçin.

![Lisans Atama](./media/6AssignLicenses.png)

3. Project Operations lisansının seçildiğini doğrulayın ve **Değişiklikleri kaydet**'i seçin. 

> [!NOTE]
> Finance deneme teklifinin bir kullanıcıya atanması gerekmez.

## <a name="start-a-new-project-in-lcs"></a>LCS'de yeni bir proje başlatma

[LCS'de yeni bir proje başlatma](create-lcs-project.md) başlıklı konuda açıklandığı gibi yeni bir LCS projesi oluşturun

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>LCS projesine Azure aboneliği ekleme

Bu görevi tamamlamak için [LCS projesine Azure aboneliği ekleme](resource-add-azure-subscription-lcs-project.md) konusundaki adımları izleyin.

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Finance demo ortamını kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations ile dağıtma

Dağıtımı tamamlamak için [Yeni bir ortam sağlama](resource-provision-new-environment.md) başlıklı konuda verilen kılavuzu izleyin. Önizleme için [demo ortamı](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) dağıtım türünü kullanın.

## <a name="install-cds-setup-and-configuration-data"></a>CDS kurulum ve yapılandırma verilerini yükleme

CDS kurulum ve yapılandırma verilerini [Common Data Service uygulamasında yapılandırma verilerini ayarlama ve uygulama](resource-apply-pro-setup-config-data.md) başlıklı konuda açıklandığı gibi yükleyin.

