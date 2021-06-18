---
title: Her tüzel kişilik için Project Operations tümleştirmesini yapılandırma
description: Bu konuda Project Operations'ta tüzel varlık entegrasyonu ayarlama hakkında bilgi sağlanır.
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e5a12de275a9f886434da45fbbed5140e3913d83
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000100"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>Her tüzel kişilik için Project Operations tümleştirmesini yapılandırma 

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Bu konuda, Dynamics 365 Project Operations'ı her tüzel kişilik için yapılandırmak üzere gerekli adımlar ayrıntılı olarak gösterilmektedir.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Dynamics 365 Finance'te özellik anahtarlarını etkinleştir

Gerekli özellikleri etkinleştirmek için aşağıdaki adımları izleyin.

1. Dynamics 365 Finance'te **Özellik yönetimi** çalışma alanına gidin.
2. **Özellik listesinde**, aşağıdaki özellikleri bulun ve etkinleştirin:
  
    - **Bir proje için birden çok sözleşme satırını etkinleştirme**
    - **Dynamics 365 Customer Engagement'ta Project Operations'ı etkinleştirin**

> [!NOTE]
> **Özellik anahtarlarını** listede göremiyorsanız, Finance sürümünüzün en düşük sürüm gereksinimini (uygulama sürümü 10.0.13 uygulanmış veya daha yüksek) karşıladığını doğrulayın. Özellik listesini yenilemek için **güncelleştirmeleri denetle**'yi seçin.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>Geçerli bir varlık için Project Operations dağıtımı senaryosu tanımlayın

Geçerli bir varlık düzeyinde Dynamics 365 Customer Engagement'ta Project Operations'ı etkinleştirebilirsiniz. Kaynak/Stoklanmayan tabanlı senaryolarda Dynamics 365 Customer Engagement'ta Project Operations'ı kullanarak bir yasal varlığınız olabilir. Aynı ortamda, Stoklanmayan/üretim emri senaryoları için Project Operations'ı kullanarak başka bir tüzel kişiliye sahip olabilirsiniz.

1. Dynamics 365 Finance'te **Proje yönetimi ve muhasebe** > **Kurulum** > **Genel Proje yönetimi ve muhasebe parametreleri** 'ne gidin.
2. Kullanılabilir geçerli varlıklar listesinde, birden çok sözleşme satırı ve Dynamics 365 Customer Engagement özellikler üzerinde Project Operations'ın etkinleştirildiği varlıkları seçin. Stoğu/üretim emri senaryoları seçili olmadığı için Project Operations'ı kullanacak hukuk tüzel vrlıkları bırakın.

> [!NOTE]
> Yasal bir varlık, yalnızca varolan bir proje içermiyorsa seçilebilir.

## <a name="configure-project-management-and-accounting-parameters"></a>Proje yönetimi ve muhasebeye genel bakış parametrelerini yapılandırın

Dynamics 365 Customer Engagement üzerinde Project Operations kullanan her bir tüzel kişiliği bir varsayılan parametre kümesi gerektirir. Bu parametreler **Proje yönetimi ve hesap oluşturma parametreleri** sayfasındaki **Project Operations** sekmesinde yapılandırılır . Parametreler şunlardır:

  - **Fatura türü varsayılanları**: Project Operations, satır özellikleri finans ile eşlenmesi gereken sabit bir faturalama türü varsayılan kümesi kullanır. Her faturalama türü için bir kayıt oluşturun: **belirtilmemiş**, **Borçlandırılabilir**, **borçlandırılamayan**, **Kapanış** ve **kullanılamaz**.
  - **Proje kategorisi Varsayılanları**: her hareket türü için kullanılacak varsayılan Proje kategorilerini seçin. Bu varsayılanlar **Project Operations tümleştirme günlüğünde** ve proje fiili için herhangi bir hareket kategorisinin belirtilmediğinde tahminlerde kullanılır.
  - **Tahminler**: Zaman ve gider tahminlerinde kullanılacak tahmin modelini seçin.


[!INCLUDE[footer-include](../includes/footer-banner.md)]