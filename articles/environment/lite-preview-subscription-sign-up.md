---
title: Önizleme aboneliğine kaydolma - lite
description: Bu konuda, Project Operations Lite dağıtımına (anlaşmadan proforma faturaya) abone olma ve dağıtma hakkında bilgiler sağlanmaktadır.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3b06ac29e8021967490534d3aefc8b5ce733413b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588024"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Önizleme aboneliği (lite) için kaydolma 

Bu konuda deneme teklifine nasıl abone olunacağı ve Dynamics 365 Project Operations lite dağıtımın nasıl dağıtılacağını (anlaşmadan proforma faturaya kadar) açıklanmaktadır.

> [!NOTE]
> Bu işlem, Project Operations'ın yaklaşan sürümlerinde değişecektir.

## <a name="prerequisites"></a>Ön koşullar
- Önizlemeyi dağıtan kullanıcının Azure kiracısı genel yönetici haklarına sahip olması gerekir. İlk teklif kullanımı sırasında bir kiracı oluşturabilirsiniz.

> [!IMPORTANT]
> Kuruluşta bu görevi, kiracı yönetici olarak yalnızca bir kişinin gerçekleştirmesi gerekir. Bu sürüme abone değilseniz kuruluşunuzun kaydolup kullanıcı kimlik bilgilerinizi alana kadar bekleyin.
> 
> Denemeler kiracıda tek kullanımlıktır. Denemeyi yalnızca bir kez çalıştırabilirsiniz. Deneme amacıyla yeni bir kiracı oluşturmanızı öneririz.

### <a name="dynamics-365-project-operations-trial"></a>Dynamics 365 Project Operations deneme sürümü 

Başlamadan önce, Proje İşlemleri önizlemesini istediğiniz kiracıdaki kullanıcı çalışma hesabının bulunduğu bir tarayıcıda oturum açtığınızdan emin olun.

1. **Dynamics 365 Project Operations** İlk teklif kodunu kullanmak için [Project Operations Denemesi](https://aka.ms/try-po)'ne gidin.
2. Siparişinizi onaylayın.

  Teklifinin başarıyla kullanıldığına ilişkin onay görürsünüz.

## <a name="assign-licenses"></a>Lisans atama

> [!IMPORTANT]
> Aşağıdaki adımları tamamlamak için kuruluşunuzun Microsoft 365 Portalı'na yönetim erişimine sahip olmanız gerekir.


1. Lisansları kullanıcılarınıza atamak için [Microsoft 365 yönetim merkezine](https://portal.office.com/) gidin.
2. **Etkin kullanıcılar** sayfasında lisans atamak istediğiniz kullanıcıları seçin.
3. **Dynamics 365 Project Operations** lisansının seçili olduğunu doğrulayın. 
4. **Değişiklikleri Kaydet**'i seçin.

## <a name="create-a-new-dataverse-environment"></a>Yeni bir Dataverse ortamı oluşturun

1. [Dataverse dağıtım modeli](lite-deployment.md) konusundaki yönergeleri izleyerek yeni bir Project Operations Dataverse dağıtım ortamı hazırlayın. Ortam türünü seçtiğinizde, **Deneme (Abonelik tabanlı)** kullandığınızdan emin olun.

  ![Yeni ortam.](./media/19CreateEnvironment.png)

2. **Dynamics 365 uygulamalarını etkinleştir** ayarını seçin ve **Bu uygulamaları otomatik olarak dağıt**'ı boş bırakın.  
3. Ortam oluşturmak için **Kaydet**'i seçin.

  ![Veritabanı ekle.](./media/20CreateEnvironment1.png)

4. Ortam oluşturulduktan sonra **Microsoft Dynamics 365 Project Operations** çözümünü yükleyin. 

![Çözüm Yükleme.](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>CDS yapılandırması yükleme ve demo verileri ayarlama

[Demo ayarlaması ve yapılandırma verileri uygulama](lite-apply-demo-setup-config-data.md) konusundaki yönergeleri izleyerek CDS yapılandırmasını yükleyin ve demo verileri ayarlayın.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
