---
title: Gereksinimleri geçici ayırma
description: Bu konu, gereksinimleri geçici ayırma hakkında bilgi sağlar.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 09f7acb95be014034cc03d7eed9d37363d430601
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147409"
---
# <a name="soft-book-requirements"></a>Gereksinimleri geçici ayırma

[!include [banner](../includes/psa-now-project-operations.md)]

Kaynak gereksinimi kesin ayrılmış olabilir. Kesin ayırma, bir kaynağın kapasitesini kullanan bir teklif oluşturur. Teklif, daha sonra onay için istek sahibine geri gönderilir. Geçici ayırma, proje takımına geçici olarak bir kaynak ekler ve Zamanlama Panosunda farklı bir duruma sahiptir ancak kaynağın kapasitesini kullanmaz. Zamanlama Panosundan bir kaynağı geçici ayırmak için **Ayırma Durumu** alanını **Geçici** olarak ayarlayın.

![Ayırma durumu Geçici olarak ayarlandı](media/Resource-Management-image77.png)

**Takım** sekmesi **Adlandırılmış Takım Üyeleri** görünümündeyken kaynak orada görünür. Geçici ayrılan saatler, **Geçici Ayrılan Saat Sayısı** sütununda bildirilir.

![Adlandırılmış Takım Üyeleri görünümünde geçici ayrılan saatler](media/Resource-Management-image78.png)

Geçici ayrılan takım üyeleri görevlere atanabilir.

![Göreve atanan geçici ayrılmış takım üyesi](media/Resource-Management-image79.png)

**Mutabakat** sekmesinde geçici ayrılmış bir kaynak için hiçbir ayırma gösterilmez çünkü **Mutabakat** sekmesi yalnızca kesin ayırmaları dikkate alır.

![Mutabakat sekmesinde ayrılması olmayan geçici ayrılmış kaynak](media/Resource-Management-image80.png)

> [!NOTE]
> Genel takım üyesinden oluşturulan bir gereksinimden, bir kaynağı geçici ayıramazsınız.

Zamanlama Panosunda, bir kaynağın geçici ayrılmaları için farklı bir renklendirme kullanılır.

![Zamanlama Panosundaki geçici ayrılmalar](media/Resource-Management-image81.png)

Geçici bir ayırmayı kesin ayırmaya dönüştürmek için Zamanlama Panosunda geçici ayırmayı sağ tıklayın ve ardından **Durumu Değiştir** \> **Kesin Ayırma** \> **Kesin**'i seçin.

![Ayırma durumunu Kesin olarak değiştirme](media/Resource-Management-image82.png)

Ayırma değiştirilir ve durum Zamanlama Panosunda değiştirilir. Ayırma durumu şimdi **Kesin** olduğu için kaynak ayrıldı olarak gösterilir ve kapasitesi ve uygunluğu ayarlanır.

Aynı yöntemi kesin bir ayırmayı veya geçici bir ayırmayı Zamanlama Panosundan iptal etmek için kullanabilirsiniz.

Projenin **Takım** sekmesinde geçici ayrılan bir kaynağı kesin ayrılana dönüştürmek için kaynağı seçin ve ardından **Onayla**'yı seçin.

![Komutu onayla](media/Resource-Management-image83.png)
