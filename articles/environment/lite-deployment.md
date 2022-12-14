---
title: Project Operations Lite Dağıtma
description: Bu makalede, Project Operations hafif dağıtım - anlaşmadan proforma faturayı kurma hakkında bilgiler sağlanmaktadır.
author: stsporen
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 2c508f56b3018b6a86fea78bcf9ee4136e90f385
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/30/2022
ms.locfileid: "9811003"
---
# <a name="deploy-project-operations-lite"></a>Project Operations Lite Dağıtma

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_



Project Operations birden çok dağıtım modelini destekler. En iyi dağıtım modelini belirlemek için bkz. [Dağıtım türleri](determine-deployment-type.md).


> [!IMPORTANT]
> Bu dağıtım (Lite dağıtımı) anlaşmadan proforma faturaya, **Dataverse-yalnızca Project Operations dağıtımı** ile sonuçlanır.

- [Project Operations'ı yeni bir Dataverse ortamına yükleme](#new)
- [Var olan bir Dataverse ortamına yükleme](#existing)
- [Çift yazma bileşenleri olan mevcut bir Dataverse ortamına yükleme](#existingdw)



## <a name="install-project-operations-lite-to-a-new-dataverse-environment"></a><a name="new"></a>Project Operations Lite'ı yeni bir Dataverse ortamına yükleme

1. Project Operations lisansına sahip [Genel Yönetici veya Power Platform Yöneticisi](/power-platform/admin/global-service-administrators-can-administer-without-license) olarak [PowerPlatform yönetim merkezi](https://admin.powerplatform.com)'nde yeni bir Dataverse ortamı oluşturun. **Bu ortam için bir veritabanı oluştur** ve **Dynamics 365 Uygulamaları**'nın etkin olduğundan emin olun. Daha fazla bilgi için bkz. [Power Platform yönetim merkezinde ortamlar oluşturma ve yönetme](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
1. Dynamics 365 uygulamaları dağıtım listesinden **Microsoft Dynamics 365 Project Operations**'ı seçin.


## <a name="install-project-operations-lite-to-an-existing-dataverse-environment"></a><a name="existing"></a>Project Operations Lite'ı mevcut bir Dataverse ortamına yükleme 
1. Project Operations lisansına sahip [Genel Yönetici Power Platform Yöneticisi](/power-platform/admin/global-service-administrators-can-administer-without-license) olarak Project Operations'ı yüklemek istediğiniz [PowerPlatform yönetim merkezi](https://admin.powerplatform.com)'nde ortamı bulun.
1. Dynamics 365 uygulamaları dağıtım listesinden **Microsoft Dynamics 365 Project Operations**'ı yükleyin. Daha fazla bilgi için bkz. [Dynamics 365 uygulamalarını yönetme](/power-platform/admin/manage-apps).

## <a name="install-project-operations-lite-to-an-existing-dataverse-environment-where-dual-write-solutions-are-already-present"></a><a name="existingdw"></a>Project Operations Lite'ı Çift yazma çözümlerinin bulunduğu mevcut bir Dataverse ortamına yükleme

Project Operations'ı Lite Dağıtım modunda çalıştırmaya devam etmek isterseniz, aşağıdaki adımları izlemelisiniz:

1. Project Operations lisansına sahip [Genel Yönetici Power Platform Yöneticisi](/power-platform/admin/global-service-administrators-can-administer-without-license) olarak Project Operations'ı yüklemek istediğiniz [PowerPlatform yönetim merkezi](https://admin.powerplatform.com)'nde ortamı bulun.
1. Dynamics 365 uygulamaları dağıtım listesinden **Microsoft Dynamics 365 Project Operations**'ı yükleyin. Daha fazla bilgi için bkz. [Dynamics 365 uygulamalarını yönetme](/power-platform/admin/manage-apps).
1. Ortamınızda finans ve operasyon uygulamaları yüklemesiyle tümleştirmeye yardımcı olan Çift yazma bileşenleri olduğundan Project Operations yüklemesi, projeyle ilgili verileri finans ve operasyonlar uygulamalarıyla tümleştirmek için gerekli özellikleri ve uzantıları da yükler. Project Operations'ı Lite dağıtımda çalıştırmak istediğinizden bu tümleştirme bileşenlerinin, Lite dağıtım senaryoları için kısıtlamalar ve yük oluşturduklarından kaldırılması gerekir. Bu bileşenleri kaldırmak için **Dynamics 365 Project Operations Çift Yazma** ve **Dynamics 365 Project Operations Çift Yazma Varlığı Eşlemeleri**'ni el ile kaldırın.
1. **Project Operations -> Ayarlar -> Parametreler**'e gidin. **Proje Parametresi** ayrıntıları sayfasını açın ve **Çözüm Yükseltme Davranışı** alanını **yalnızca Lite** olarak ayarlayın. Bu, sonraki Project Operations yükseltmelerinin tümleştirme bileşenlerini Project Operations'a geri getirmemesini garanti eder.  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
