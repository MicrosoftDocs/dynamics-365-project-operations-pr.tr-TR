---
title: Gider kategorilerini ayarlama
description: Bu konuda, gider raporları için gider kategorilerini ve paylaşılan kategorileri ayarlama hakkında bilgiler sağlanmaktadır.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: f051d70f3dfe3b241dc0a206c0cdfda000f87c76
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896710"
---
# <a name="set-up-expense-categories"></a>Gider kategorilerini ayarlama

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Çalışanlar gider raporları oluşturduğunda, kaydettikleri her gider, bir gider kategorisiyle ilişkilendirilmelidir. Gider kategorileri, kuruluşunuzdaki tüzel kişilikler arasında paylaşılabilen paylaşılan kategorilerden türetilir. Kuruluşunuzun nasıl tanımlandığına bağlı olarak bu gider kategorileri başka alanlarda da paylaşılabilir. Kuruluşunuzun tanımını ve uygulama takımının rehberliğini temel alarak Gider yönetiminde kullanılan kategorilerin yalnızca Gider yönetiminde mi kullanılacağını yoksa başka alanlarda da paylaşılacağını belirlemeniz gerekir.

> [!NOTE]
> Bu kategoriler Proje yönetimi ile muhasebe ve Gider yönetimi arasında veya Proje yönetimi ile muhasebe ve Üretim arasında paylaşılabilir. Ancak Gider yönetimi ve Üretim arasında paylaşılamaz.

Kurulum sürecine başlamadan önce her gider kategorisi için aşağıdaki kararların alınması gerekir:

- Gider kategorisi nedir? Örnekler arasında uçuşlar, otel veya kilometre kategorileri yer alır.
- Gider kategorisi, Proje yönetimi ve muhasebede de kullanılabilir mi? Mümkünse, aşağıdaki kararları da vermeniz gerekir:

    - Aşağıdaki giderler için hangi maliyet hesapları kullanılır?

        - Maliyet
        - Bordro tahsisatı
        - WIP-maliyet değeri
        - Maliyet-öğe
        - WIP-maliyet değeri-öğe
        - Tahakkuk eden zarar
        - WIP-tahakkuk eden zarar

    - Aşağıdaki gelir kaynakları için hangi gelir hesapları kullanılır?

        - Faturalanan gelir
        - Tahakkuk eden gelir-satış değeri
        - WIP-satış değeri
        - Tahakkuk eden gelir-üretim
        - WIP-üretim
        - Tahakkuk eden gelir-kar
        - WIP-kar
        - Tahakkuk eden gelir-abonelik
        - WIP-abonelik

- Gider türü nedir?
- Gider kategorisi için varsayılan ödeme yöntemi nedir?
- Gider kategorisindeki giderlerin dökümünün alınması gerekir mi?
- Gider kategorisi için ana varsayılan hesap nedir?
- Gider kategorisi için varsayılan öğe satış vergisi grubu nedir?
- Gider kategorisi için ek ödeme yöntemlerine izin verilir mi? Öyleyse, bunlar nelerdir?
- Bu gider kategorisinde alt kategoriler var mı? Alt kategoriler varsa aşağıdaki kararları da vermeniz gerekir:

    - Vergiden düşmeden dışlanan alt kategoriler var mı?
    - Alt kategorilerin öğe satış vergisi grubu nedir?
