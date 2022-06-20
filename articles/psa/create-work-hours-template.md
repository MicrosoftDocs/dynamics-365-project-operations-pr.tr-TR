---
title: Çalışma saatleri şablonu oluşturma
description: Bu makalede, Project Service'te çalışma saatleri şablonunun nasıl oluşturulacağı açıklanmaktadır.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 8f3ac17a29e79f86f7c3ce127edb4b02ca63ea04
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916082"
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
3. Kaynağın **çalışma saatleri** sekmesini seçin ve Takvim kurallarını yapılandırmak için [bir kaynak için çalışma saatleri ayarla](/dynamics365/field-service/set-work-hours-resource) alanındaki yönergeleri doldurun.

**Yeni bir takvim şablonu oluşturun**

1. **Ayarlar** \> **Takvim Şablonu**'na gidin.
2. **Yeni**'yi seçin ve bir ad, açıklama ve şablon kaynağı girin.


> [!NOTE]
> Takvim şablonunda bir kaynağa başvurulduğunda, kaynağın takvimin bir kopyası takvim şablonuyla ilişkilidir. Kopyalanan şablonun çalışma saatlerini değiştirirseniz, bu değişiklikler takvim şablonuna yansımaz.


### <a name="see-also"></a>Ayrıca bkz.  
 [Kaynakları ayarlama](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
