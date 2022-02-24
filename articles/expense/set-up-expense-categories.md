---
title: Gider kategorilerini ayarlama
description: Bu konuda, gider raporları için gider kategorilerini ve paylaşılan kategorileri ayarlama hakkında bilgiler sağlanmaktadır.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 13e72e4b852fd0edac5ad35d5162e74b016bce33
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123807"
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
