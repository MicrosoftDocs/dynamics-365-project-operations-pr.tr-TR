---
title: LCS projesine Azure aboneliği ekleme
description: Bu makalede Azure aboneliğinizi bir LCS projesine bağlama hakkında bilgiler sağlanmaktadır.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 64ee8cfa7394a08c3d588c0e8f4a73185d9496cf
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912172"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a>LCS projesine Azure aboneliği ekleme

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Bulutta barındırılan ortamların var olan bir Azure aboneliği kullanılarak dağıtılması gerekir. Bu makalede, mevcut Azure aboneliğinizi bir LCS projesine bağlama hakkında bilgiler sağlanmaktadır. 

## <a name="grant-admin-consent"></a>Yönetici onayı verme

1. LCS projenizde, **Ortamlar** bölümünde **Microsoft Azure ayarlarını** seçin.

![Microsoft Azure ayarları.](./media/1MicrosoftAzureSettings.png)

2. **Proje ayarları** sayfasında, **Azure bağlayıcıları** sekmesinde, **Yetkilendir**'i seçin. Bu, ortamların bu projeye dağıtılmasına izin verir.

![Azure Bağlayıcıları.](./media/2AzureConnectors.png)

3. Yönetici onayı sağlamak için **Yetkilendir**'i yeniden seçin.

![Yönetici onayı verme.](./media/3GrantAdminConsent.png)

4. İzin isteğini kabul edin.

![İzin İsteğini Kabul Etme.](./media/4AcceptPermissionRequest.png)

Yetkilendirme işlemi artık tamamlanmıştır. 

![Yetkilendirme Başarılı.](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a>Azure aboneliğinize Dynamics Dağıtım Hizmetleri erişimi sağlama

1. [Microsoft Azure faturalama](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) öğesine gidin ve aboneliğinizi seçin. Dynamics Dağıtım Hizmetleri'nin ortamları dağıtabilmesi için bu aboneliğe erişmesi gerekir.

![Azure aboneliği ayrıntıları.](./media/6AzureSubscription.png)

2. Gezinti bölmesinde **Erişim denetimi (IAM)** öğesini ve ardından **Rol ataması ekle**'yi seçin.
3. Sağdaki kaydırıcıda, **Katılımcı rolü**'nü seçin ve sağlanan listede, **Dynamics Dağıtım Hizmetleri**'ni bulup seçin. 
4. **Kaydet**'i seçin.

![Abonelik Erişimi.](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a>LCS projesine bir abonelik bağlayıcı ekleme

1. LCS projenizde, **Microsoft Azure ayarları** sayfasında, yeni bir bağlayıcı eklemek için **Ekle**'yi seçin.
2. Azure abonelik kimliğinizi girin. Ekranın sağ alt köşesindeki **Ayarlar** altında [Azure portal](https://ms.portal.azure.com/)'daki Azure abonelik kimliğinizi bulabilirsiniz.
3. **Azure Resource Manager'ı kullanmak için yapılandır** alanında **Evet**'i seçin.
4. Azure'un Abonelik AAD Kiracısı Etki Alanı'nın kullandığınız etki alanının sahibi olan Azure aboneliğiyle eşleştiğinden emin olun ve **İleri**'yi seçin.
5. **Microsoft Azure Kurulumu** ekranında, onaylamak için **İleri**'yi seçin. Bu ekranda bir hata alırsanız, bu makaledeki [Azure aboneliğine Dynamics Dağıtım Hizmetleri erişimi sağlama](#provide) konusuna dönün ve tüm adımları tamamladığınızdan emin olun.
6. Azure Yönetim sertifikasını bilgisayarınızdaki yerel bir klasöre indirin. Aboneliği seçip **ayarlar** > **yönetim sertifikalarına** giderek Azure abonelik Yöneticinizden sertifikayı Azure yönetim portalına yüklemesini için isteyin. Bu sertifika, LCS'nin sizin adınıza Azure ile iletişim kurmasına olanak tanır. Kullanıcınızın aboneliğe erişimi varsa bu adımı atlayabilirsiniz.
7. **İleri**'yi seçin.
8. Dağıtımın yapılacağı Azure bölgesini seçin ve bu sistemi kullanmayı planladığınız yere yakın bir veri merkezi seçin.
9.  **Bağlan**'ı seçin.

Azure aboneliğinize başarıyla bağlandınız. Artık Dynamics 365 Finance bulutunda barındırılan ortamları dağıtabilirsiniz.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
