---
title: Proje güncelleştirme
description: Bu konuda, Project Operations projelerini güncelleştirme hakkında bilgiler sağlanmaktadır.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 27444b072bdf7de55d6b38c30c1ea5fe66ed46ac
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286407"
---
# <a name="update-a-project"></a>Proje güncelleştirme

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Aşağıda, bir proje oluşturulduktan ve mevcut güncelleştirmeler uygulandıktan sonra güncelleştirilebilecek alanların özeti verilmiştir.

## <a name="project-detail-fields"></a>Proje ayrıntısı alanları

- **Ad**: Projenin başlığı.
- **Açıklama**: Projeye genel bakış.
- **Müşteri**: Projenin teslim edileceği şirket.
- **Takvim şablonu**: Projenin çalışma saatleri. Alan değiştirildiğinde, tüm zamanlama yeniden hesaplanır.
- **Para Birimi**: Projenin para birimi. Bu alanın varsayılan değeri, sözleşme biriminde tanımlanan para birimine göre belirlenir. Sözleşme birimi güncelleştirildiğinde alan da güncelleştirilir.
- **Sözleşme Birimi**: Satışı kazanmak ve iş ve servislerin müşteriye teslimini yönetmekten birincil olarak sorumlu olan şirket grubunu veya bölümü gösteren kuruluş birimidir. 
- **Proje Yöneticisi**: Zaman girişlerini ve giderleri inceleme ve onaylama yetkisine sahip proje takımı üyesi.

## <a name="estimate-fields"></a>Tahmin alanları

- **Tahmini Başlangıç Tarihi**: Projenin başlayacağı tarih. Bu alan güncelleştirildiğinde, projedeki tüm görevler yeni başlangıç tarihine göre uygun şekilde taşınır.
- **Bitiş Tarihi**: Projenin bitmesi planlanan tarih.
- **Çalışma Süresi**: Projenin tahmini çalışma süresi. Görevler projeye eklendikten sonra bu alan düzenlenemez.
- **Tahmini İşçilik Maliyeti**: Projenin tahmini işçilik maliyeti. İşçilik maliyetleri projeye eklendikten sonra bu alan düzenlenemez.
- **Tahmini Giderler**: Projenin tahmini giderleri. Giderler projeye eklendikten sonra bu alan düzenlenemez.

## <a name="project-actual-fields"></a>Projenin gerçek değer alanları
- **Fiili Başlangıç**: Projenin başlatıldığı tarih.
- **Fiili Bitiş**: Proje tamamlandığında güncelleştirilir.

## <a name="project-status-fields"></a>Proje durumu alanları

- **Genel Proje Durumu**: Proje yöneticisinin sağladığı genel proje durumu.
- **Yorumlar**: Proje yöneticisinin sağladığı, projenin geçerli durumuyla ilgili bir anlatım.



[!INCLUDE[footer-include](../includes/footer-banner.md)]