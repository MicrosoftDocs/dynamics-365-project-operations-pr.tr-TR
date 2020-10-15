---
title: Gider tahminleri
description: Bu konuda, proje tabanlı giderleri tanımlama veya tahmin etme hakkında bilgiler sağlanmaktadır.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2afe4ff2f84fc5426c409e6314da73b11a4de281
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908692"
---
# <a name="expense-estimates"></a>Gider tahminleri
_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Dynamics 365 Project Operations, Proje yöneticilerinin kaynak tabanlı tahminlerin yanı sıra, her proje için proje tabanlı giderler tanımlamasına da olanak tanır. Her gider öğesi, belirli bir proje görevi veya gider kategorisiyle ilişkilendirilebilir. Gider kategorileri genellikle kuruluş düzeyinde tanımlanır. Her gider kategorisinin fiyatlandırması genellikle aşağıdaki hiyerarşiye göre tanımlanır:

- Kuruluş
- Müşteri
- Teklif/sözleşme

Proje giderini görüntülemek, eklemek veya silmek için aşağıdaki adımları tamamlayın.

1. **Projeler**'e gidin ve üzerinde çalışmak istediğiniz projeyi seçin.
2. **Proje Tahminleri** sekmesini seçin ve proje giderleri listesini görüntüleyin.
3. Gider eklemek için **Yeni Gider**'i seçin. Alternatif olarak, silinecek gideri seçin ve ardından **Gideri Sil** seçeneğini belirleyin.

Aşağıdaki öznitelikler her gider satırı öğesi için tanımlanır:

- **Kategori**: Projede oluşan tüm giderleri tanımlamak için kullanılan ortak gruplar.
- **Başlangıç Tarihi**: Giderin oluşacağı tahmin edilen tarih.
- **Miktar**: Belirli bir kategori için gider öğelerinin tahmini sayısı.
- **Birim Maliyet Fiyatı**: Giderin maliyetini hesaplamak için kullanılan birim fiyatı.
- **Birim Satış Fiyatı**: Giderin satış fiyatlarını hesaplamak için kullanılan birim fiyatı.

