---
title: LCS projesine Azure aboneliği ekleme
description: Bu konuda, Azure aboneliğinizi bir LCS projesine bağlama hakkında bilgiler sağlanmaktadır.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ad1ddd69cbb8db7780b8277a7ed7533d3ea3d053
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289933"
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
6. Azure Yönetim Sertifikası'nı bilgisayarınızda yerel bir klasöre indirin ve ardından **Ayarlar** > **Yönetim Sertifikaları**'na giderek Azure Yönetim Portalı'na yükleyin. Bu sertifika, LCS'nin sizin adınıza Azure ile iletişim kurmasına olanak tanır. Kullanıcınızın aboneliğe erişimi varsa bu adımı atlayabilirsiniz.
7. **İleri**'yi seçin.
8. Dağıtımın yapılacağı Azure bölgesini seçin ve bu sistemi kullanmayı planladığınız yere yakın bir veri merkezi seçin.
9.  **Bağlan**'ı seçin.

Azure aboneliğinize başarıyla bağlandınız. Artık Dynamics 365 Finance bulutta barındırılan ortamlarını dağıtabilirsiniz.




[!INCLUDE[footer-include](../includes/footer-banner.md)]