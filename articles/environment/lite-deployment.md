---
title: Project Operations dağıtın - lite
description: Bu konuda, Project Operations Lite dağıtımını (anlaşmadan proforma faturaya) yükleme hakkında bilgiler sağlanmaktadır.
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: e33506504665f2e7ef7ad48469082f9f64a2a44b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580756"
---
# <a name="deploy-project-operations---lite"></a>Project Operations dağıtın - lite

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_



Project Operations birden çok dağıtım modelini destekler. En iyi dağıtım modelini belirlemek için bkz. [Dağıtım türleri](determine-deployment-type.md).


> [!IMPORTANT]
> Bu dağıtım (Lite dağıtımı) anlaşmadan proforma faturaya, **Dataverse-yalnızca Project Operations dağıtımı** ile sonuçlanır.

- [Project Operations'ı yeni bir Dataverse ortamına yükleme](#new)
- [Var olan bir Dataverse ortamına yükleme](#existing)



## <a name="install-project-operations-to-a-new-dataverse-environment"></a><a name="new"></a>Project Operations'ı yeni bir Dataverse ortamına yükleme

1. Project Operations lisansına sahip [Genel Yönetici veya Power Platform Yöneticisi](/power-platform/admin/global-service-administrators-can-administer-without-license) olarak [PowerPlatform yönetim merkezi](https://admin.powerplatform.com)'nde yeni bir Dataverse ortamı oluşturun. **Bu ortam için bir veritabanı oluştur** ve **Dynamics 365 Uygulamaları**'nın etkin olduğundan emin olun. Daha fazla bilgi için bkz. [Power Platform yönetim merkezinde ortamlar oluşturma ve yönetme](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Dynamics 365 uygulamaları dağıtım listesinden **Microsoft Dynamics 365 Project Operations**'ı seçin.


## <a name="install-project-operations-to-an-existing-dataverse-environment"></a><a name="existing"></a>Project Operations'ı var olan bir Dataverse ortamına yükleme
1. Ortamın yükleme sırasında [çift yazma](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview) ile yapılandırılmadığından emin olun. Ardından [Kaynak öğeleri/stoğu tutulmayan öğeleri temel alan senaryolar için Project Operations](project-operations-integrated-deployment-overview.md) özelliklerini yükleyin.
2. Project Operations lisansına sahip [Genel Yönetici Power Platform Yöneticisi](/power-platform/admin/global-service-administrators-can-administer-without-license) olarak Project Operations'ı yüklemek istediğiniz [PowerPlatform yönetim merkezi](https://admin.powerplatform.com)'nde ortamı bulun.
3. Dynamics 365 uygulamaları dağıtım listesinden **Microsoft Dynamics 365 Project Operations**'ı yükleyin. Daha fazla bilgi için bkz. [Dynamics 365 uygulamalarını yönetme](/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]
