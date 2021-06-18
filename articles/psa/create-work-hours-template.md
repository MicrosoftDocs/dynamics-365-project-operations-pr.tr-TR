---
title: Çalışma saatleri şablonu oluşturma
description: Bu konuda Project Service'ta çalışma saatleri şablonu oluşturma açıklanmaktadır.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 105e3cb2ef7b904e96dc21013906e0b7444e3b88
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997220"
---
# <a name="create-a-work-hours-template-project-service"></a>Çalışma saatleri şablonu oluşturma (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

Bir proje oluşturmak ve yönetmek için projeye bir takvim şablonu uygulamanız gerekir. Takvim şablonu aşağıdaki proje özniteliklerini tanımlar:

- Başlangıç ve bitiş saati dahil çalışma saatleri
- Çalışma günleri
- Çalışılmayan günler gibi takvim özel durumları

Bir projeye uygulanan takvim şablonu, kuruluşunuzun ayarlarında tanımlanan takvim şablonunun bir kopyasıdır.

> [!NOTE]
> Takvim şablonunu değiştirirseniz, bu değişiklikler projenin çalışma saatlerine yayılmaz. Projenin çalışma saatlerini değiştirmek için yeni bir şablon uygulanması gerekir.

Kuruluşunuz için bir takvim şablonu oluşturmak üzere, iki önemli gereksinim vardır:

- Şablonun istenen çalışma saatlerini yeni veya varolan bir takılabilir kaynak kullanarak tanımlayın.
- Yeni bir takvim şablonu oluşturun ve şablonu ayrılabilir kaynağı ile ilişkilendirin.

**Şablonun çalışma saatlerini tanımlayın**

1. **Kaynaklar** \> **Kaynaklar**'a gidin.
2. Takvim şablonuna başvuracak yeni bir kaynak oluşturun veya varolan bir kaynağı seçin.
3. Kaynağın **çalışma saatleri** sekmesini seçin ve Takvim kurallarını yapılandırmak için [bir kaynak için çalışma saatleri ayarla](/dynamics365/field-service/set-work-hours-resource.md) alanındaki yönergeleri doldurun.

**Yeni bir takvim şablonu oluşturun**

1. **Ayarlar** \> **Takvim Şablonu**'na gidin.
2. **Yeni**'yi seçin ve bir ad, açıklama ve şablon kaynağı girin.


> [!NOTE]
> Takvim şablonunda bir kaynağa başvurulduğunda, kaynağın takvimin bir kopyası takvim şablonuyla ilişkilidir. Kopyalanan şablonun çalışma saatlerini değiştirirseniz, bu değişiklikler takvim şablonuna yansımaz.


### <a name="see-also"></a>Ayrıca bkz.  
 [Kaynakları ayarlama](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
