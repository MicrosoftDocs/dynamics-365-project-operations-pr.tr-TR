---
title: Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations önizleme aboneliklerine kaydolma
description: Bu konuda, kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations'a nasıl abone olunacağı ve Project Operations'ın nasıl dağıtılacağı hakkında bilgiler sağlanmaktadır.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: da93fcf23ee3f255812842e31cb22b5d39daa963
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334851"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations önizleme aboneliklerine kaydolma

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Bu konuda, deneme teklifine nasıl abone olunacağı ve kaynak/stoklu olmayan öğeleri temel alan senaryolar için Project Operations ortamının nasıl dağıtılacağı açıklanmaktadır.

## <a name="prerequisites"></a>Ön koşullar
- Önizlemeyi dağıtan kullanıcının Azure kiracısı genel yönetici haklarına sahip olması gerekir. İlk teklif kullanımı sırasında bir kiracı oluşturabilirsiniz. 
- Finance ortamını dağıtmak için ortam başına faturalanacak geçerli bir Azure aboneliği gereklidir. Başlamak için kuruluşunuzun mevcut aboneliğini veya bir [Azure deneme sürümünü](https://azure.microsoft.com/en-us/free/) kullanabilirsiniz. CDS ortamı, 30 günlük sınırlı bir süre boyunca ücretsiz olarak sağlanır.

> [!IMPORTANT]
> Kuruluşta bu görevi, kiracı yönetici olarak yalnızca bir kişinin gerçekleştirmesi gerekir. Bu sürüme abone değilseniz kuruluşunuzun kaydolup kullanıcı kimlik bilgilerinizi alana kadar bekleyin.
> 
> Denemeler kiracıda tek kullanımlıktır. Denemeyi yalnızca bir kez çalıştırabilirsiniz. Deneme amacıyla yeni bir kiracı oluşturmanızı öneririz.


### <a name="dynamics-365-project-operations-ce---preview-trial"></a>Dynamics 365 Project Operations (CE) - Önizleme Denemesi 

Başlamadan önce, Proje İşlemleri önizlemesini istediğiniz kiracıdaki kullanıcı çalışma hesabının bulunduğu bir tarayıcıda oturum açtığınızdan emin olun.

1. İlk teklif kodunu **Dynamics 365 Project Operations** burada kullanın [Project Operations Denemesi](https://aka.ms/try-po).
2. Siparişinizi onaylayın.

  Onay teklifinin başarıyla kurtarıldığını göreceksiniz.

### <a name="dynamics-365-finance-preview-trial"></a>Dynamics 365 Finance önizleme denemesi

[Dynamics 365 for Finance Önizleme Denemesi](https://aka.ms/trypoche)'ne gidin ve teklifin önceki bölümündeki adımları tekrarlayın, Bulutta Barındırılan Ortam için Kaydolun.  

## <a name="assign-licenses"></a>Lisans atama

> [!IMPORTANT]
> Aşağıdaki adımları tamamlamak için kuruluşunuzun Microsoft 365 Portalı'na yönetim erişimine sahip olmanız gerekir.

1. Kullanıcılarınıza lisans atamak için [Microsoft 365 yönetim merkezine](https://portal.office.com/) gidin.

2. **Etkin kullanıcılar** sayfasında lisans atamak istediğiniz kullanıcıları seçin.

3. **Dynamics 365 Project Operations** lisansının seçili olduğunu doğrulayın ve **Değişiklikleri kaydet**'i seçin.

> [!NOTE]
> Finance deneme teklifinin bir kullanıcıya atanması gerekmez.

## <a name="start-a-new-project-in-lcs"></a>LCS'de yeni bir proje başlatma

[LCS'de yeni bir proje başlatma](create-lcs-project.md) başlıklı konuda açıklandığı gibi yeni bir LCS projesi oluşturun

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>LCS projesine Azure aboneliği ekleme

Bu görevi tamamlamak için [LCS projesine Azure aboneliği ekleme](resource-add-azure-subscription-lcs-project.md) konusundaki adımları izleyin.

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Finance demo ortamını kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations ile dağıtma

Dağıtımı tamamlamak için [Yeni bir ortam sağlama](resource-provision-new-environment.md) başlıklı konuda verilen kılavuzu izleyin. Önizleme için [demo ortamı](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) dağıtım türünü kullanın. 

## <a name="install-cds-setup-and-configuration-data"></a>CDS kurulum ve yapılandırma verilerini yükleme

CDS kurulum ve yapılandırma verilerini [Common Data Service uygulamasında yapılandırma verilerini ayarlama ve uygulama](resource-apply-pro-setup-config-data.md) başlıklı konuda açıklandığı gibi yükleyin.
Bu adımı yalnızca Finance tanıtım ortamı dağıtıldıktan ve tanıtım verileri hazır olduktan sonra tamamlayın.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
