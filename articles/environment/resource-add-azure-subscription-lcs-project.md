---
title: LCS projesine Azure aboneliği ekleme
description: Bu konuda, Azure aboneliğinizi bir LCS projesine bağlama hakkında bilgiler sağlanmaktadır.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6daa86d453ec5022cdd75dff0394c8818292406c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000640"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a>LCS projesine Azure aboneliği ekleme

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Bulutta barındırılan ortamların var olan bir Azure aboneliği kullanılarak dağıtılması gerekir. Bu konuda, mevcut Azure aboneliğinizin bir LCS projesine nasıl bağlanacağı açıklanmaktadır. 

## <a name="grant-admin-consent"></a>Yönetici onayı verme

1. LCS projenizde, **Ortamlar** bölümünde **Microsoft Azure ayarlarını** seçin.

![Microsoft Azure Ayarları](./media/1MicrosoftAzureSettings.png)

2. **Proje ayarları** sayfasında, **Azure bağlayıcıları** sekmesinde, **Yetkilendir**'i seçin. Bu, ortamların bu projeye dağıtılmasına izin verir.

![Azure Bağlayıcıları](./media/2AzureConnectors.png)

3. Yönetici onayı sağlamak için **Yetkilendir**'i yeniden seçin.

![Yönetici Onayı Verme](./media/3GrantAdminConsent.png)

4. İzin isteğini kabul edin.

![İzin İsteğini Kabul Etme](./media/4AcceptPermissionRequest.png)

Yetkilendirme işlemi artık tamamlanmıştır. 

![Yetkilendirme Başarılı](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a>Azure aboneliğinize Dynamics Dağıtım Hizmetleri erişimi sağlama

1. [Microsoft Azure faturalama](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) öğesine gidin ve aboneliğinizi seçin. Dynamics Dağıtım Hizmetleri'nin ortamları dağıtabilmesi için bu aboneliğe erişmesi gerekir.

![Azure Aboneliği Ayrıntıları](./media/6AzureSubscription.png)

2. Gezinti bölmesinde **Erişim denetimi (IAM)** öğesini ve ardından **Rol ataması ekle**'yi seçin.
3. Sağdaki kaydırıcıda, **Katılımcı rolü**'nü seçin ve sağlanan listede, **Dynamics Dağıtım Hizmetleri**'ni bulup seçin. 
4. **Kaydet**'i seçin.

![Abonelik Erişimi](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a>LCS projesine bir abonelik bağlayıcı ekleme

1. LCS projenizde, **Microsoft Azure ayarları** sayfasında, yeni bir bağlayıcı eklemek için **Ekle**'yi seçin.
2. Azure abonelik kimliğinizi girin. Ekranın sağ alt köşesindeki **Ayarlar** altında [Azure portal](https://ms.portal.azure.com/)'daki Azure abonelik kimliğinizi bulabilirsiniz.
3. **Azure Resource Manager'ı kullanmak için yapılandır** alanında **Evet**'i seçin.
4. Azure'un Abonelik AAD Kiracısı Etki Alanı'nın kullandığınız etki alanının sahibi olan Azure aboneliğiyle eşleştiğinden emin olun ve **İleri**'yi seçin.
5. **Microsoft Azure Kurulumu** ekranında, onaylamak için **İleri**'yi seçin. Bu ekranda bir hata alırsanız bu konudaki [Azure aboneliğine Dynamics Dağıtım Hizmetleri erişimi sağlama](#provide) bölümüne dönün ve tüm adımları tamamladığınızdan emin olun.
6. Azure Yönetim sertifikasını bilgisayarınızdaki yerel bir klasöre indirin. Aboneliği seçip **ayarlar** > **yönetim sertifikalarına** giderek Azure abonelik Yöneticinizden sertifikayı Azure yönetim portalına yüklemesini için isteyin. Bu sertifika, LCS'nin sizin adınıza Azure ile iletişim kurmasına olanak tanır. Kullanıcınızın aboneliğe erişimi varsa bu adımı atlayabilirsiniz.
7. **İleri**'yi seçin.
8. Dağıtımın yapılacağı Azure bölgesini seçin ve bu sistemi kullanmayı planladığınız yere yakın bir veri merkezi seçin.
9.  **Bağlan**'ı seçin.

Azure aboneliğinize başarıyla bağlandınız. Artık Dynamics 365 Finance bulutta barındırılan ortamlarını dağıtabilirsiniz.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
