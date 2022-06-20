---
title: Her tüzel kişilik için Project Operations tümleştirmesini yapılandırma
description: Bu makale, Project Operations'ta tüzel kişilik tarafından tümleştirme kurulumu hakkında bilgi sağlar.
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3f33e641ee0932655282618c99a26e2603660059
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914702"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>Her tüzel kişilik için Project Operations tümleştirmesini yapılandırma 

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Bu makalede, tüzel kişilik başına Dynamics 365 Project Operations yapılandırmak için gerekli adımlar açıklanır.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Dynamics 365 Finance'te özellik anahtarlarını etkinleştirme

Gerekli özellikleri etkinleştirmek için aşağıdaki adımları izleyin.

1. Dynamics 365 Finance'te, **Özellik Yönetimi** çalışma alanına gidin.
2. **Özellik listesinde**, aşağıdaki özellikleri bulun ve etkinleştirin:
  
    - **Bir proje için birden çok sözleşme satırını etkinleştirme**
    - **Dynamics 365 Customer Engagement'ta Project Operations'ı etkinleştirme**

> [!NOTE]
> **Özellik anahtarlarını** listede göremiyorsanız, Finance sürümünüzün en düşük sürüm gereksinimini (uygulama sürümü 10.0.13 uygulanmış veya daha yüksek) karşıladığını doğrulayın. Özellik listesini yenilemek için **güncelleştirmeleri denetle**'yi seçin.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>Geçerli bir varlık için Project Operations dağıtımı senaryosu tanımlayın

Tüzel kişilik düzeyinde Dynamics 365 Customer Engagement'ta Project Operations'ı etkinleştirebilirsiniz. Kaynak öğeleri/stoğu tutulmayan öğeleri temel alan senaryolar için Dynamics 365 Customer Engagement'ta Project Operations'ı kullanarak bir tüzel kişiliğe sahip olabilirsiniz. Aynı ortamda, Stoklanmayan/üretim emri senaryoları için Project Operations'ı kullanarak başka bir tüzel kişiliye sahip olabilirsiniz.

1. Dynamics 365 Finance'te **Proje yönetimi ve muhasebe** > **Kurulum** > **Genel proje yönetimi ve muhasebe parametreleri**'ne gidin.
2. Kullanılabilir tüzel kişilikler listesinde, birden çok sözleşme satır ve Dynamics 365 Customer Engagement'ta Project Operations özelliklerinin etkinleştirileceği varlıkları seçin. Stoğu/üretim emri senaryoları seçili olmadığı için Project Operations'ı kullanacak hukuk tüzel vrlıkları bırakın.

> [!NOTE]
> Yasal bir varlık, yalnızca varolan bir proje içermiyorsa seçilebilir.

## <a name="configure-project-management-and-accounting-parameters"></a>Proje yönetimi ve muhasebeye genel bakış parametrelerini yapılandırın

Dynamics 365 Customer Engagement'ta Project Operations'ı kullanan her tüzel kişilik için bir dizi varsayılan parametre gerekir. Bu parametreler **Proje yönetimi ve hesap oluşturma parametreleri** sayfasındaki **Project Operations** sekmesinde yapılandırılır . Parametreler şunlardır:

  - **Fatura türü varsayılanları**: Project Operations, satır özellikleri finans ile eşlenmesi gereken sabit bir faturalama türü varsayılan kümesi kullanır. Her faturalama türü için bir kayıt oluşturun: **belirtilmemiş**, **Borçlandırılabilir**, **borçlandırılamayan**, **Kapanış** ve **kullanılamaz**.
  - **Proje kategorisi Varsayılanları**: her hareket türü için kullanılacak varsayılan Proje kategorilerini seçin. Bu varsayılanlar **Project Operations tümleştirme günlüğünde** ve proje fiili için herhangi bir hareket kategorisinin belirtilmediğinde tahminlerde kullanılır.
  - **Tahminler**: Zaman ve gider tahminlerinde kullanılacak tahmin modelini seçin.


[!INCLUDE[footer-include](../includes/footer-banner.md)]