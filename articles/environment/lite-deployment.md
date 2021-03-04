---
title: Project Operations dağıtın - lite
description: Bu konuda, Project Operations Lite dağıtımını (anlaşmadan proforma faturaya) yükleme hakkında bilgiler sağlanmaktadır.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d4ef905f875ac8af7b2d70c3e64506558bdea1ed
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642207"
---
# <a name="deploy-project-operations---lite"></a>Project Operations dağıtın - lite

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Project Operations birden çok dağıtım modelini destekler. En iyi dağıtım modelini belirlemek için bkz. [Dağıtım türleri](determine-deployment-type.md).


> [!IMPORTANT]
> Bu dağıtım (Lite dağıtımı) anlaşmadan proforma faturaya, **Common Data Service-yalnızca Project Operations dağıtımı** ile sonuçlanır.

- [Project Operations'ı yeni bir CDS ortamına yükleme](#new)
- [Var olan bir CDS ortamına yükleme](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a>Project Operations'ı yeni bir CDS ortamına yükleme

1. Project Operations lisansına sahip [Genel Yönetici veya Power Platform Yöneticisi](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) olarak [PowerPlatform yönetim merkezi](https://admin.powerplatform.com)'nde yeni bir CDS ortamı oluşturun. **CDS veritabanı** ve **Dynamics 365 Uygulamaları**'nın etkinleştirildiğinden emin olun. Daha fazla bilgi için bkz. [Power Platform yönetim merkezinde ortamlar oluşturma ve yönetme](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Dynamics 365 uygulamaları dağıtım listesinden **Microsoft Dynamics 365 Project Operations**'ı seçin.


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a>Project Operations'ı var olan bir CDS ortamına yükleme

1. Project Operations lisansına sahip [Genel Yönetici Power Platform Yöneticisi](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) olarak Project Operations'ı yüklemek istediğiniz [PowerPlatform yönetim merkezi](https://admin.powerplatform.com)'nde ortamı bulun.
2. Dynamics 365 uygulamaları dağıtım listesinden **Microsoft Dynamics 365 Project Operations**'ı yükleyin. Daha fazla bilgi için bkz. [Dynamics 365 uygulamalarını yönetme](https://docs.microsoft.com/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]