---
title: Proje takvimlerini tanımlama
description: Bu konu, proje zamanlamasını izlemek için takvim şablonunun projeye nasıl uygulanacağı hakkında bilgi sağlar.
author: ruhercul
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9c2ea49e008d6cde40f152320face073c7e5f548
ms.sourcegitcommit: bbe484e58a77efe77d28b34709fb6661d5da00f9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/10/2021
ms.locfileid: "7487664"
---
# <a name="define-project-calendars"></a>Proje takvimlerini tanımlama

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

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

Artık iş şablonunu proje takvimi şablonuyla ilişkilendirebilirsiniz.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

