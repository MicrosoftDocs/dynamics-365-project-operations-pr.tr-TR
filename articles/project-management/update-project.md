---
title: Proje oluşturma ve güncelleştirme
description: Bu makale Project Operations'ta projeleri güncelleştirme hakkında bilgi sağlar.
author: ruhercul
ms.date: 10/20/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: dcb822a726f94a7e8e8621dc7a04f9051168d361
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911114"
---
# <a name="create-and-update-a-project"></a>Proje oluşturma ve güncelleştirme

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Aşağıda, oluşturulduktan sonra bir projede güncelleştirilebilen alanların özeti verilmiştir. Bu, bu güncelleştirmelere dayalı geçerli etkileri de içerir.

## <a name="project-detail-fields"></a>Proje ayrıntısı alanları

- **Ad**: Projenin başlığı.
- **Açıklama**: Projeye genel bakış.
- **Müşteri**: Projenin teslim edileceği şirket.
- **Takvim şablonu**: Projenin çalışma saatleri. Alan değiştirildiğinde, tüm zamanlama yeniden hesaplanır.
- **Para Birimi**: Projenin para birimi. Bu alanın varsayılan değeri, sözleşme biriminde belirlenen para birimini temel alır. Sözleşme birimi güncelleştirildiğinde alan da güncelleştirilir.
- **Sözleşme Birimi**: Satışı kazanmak ve iş ve servislerin müşteriye teslimini yönetmekten birincil olarak sorumlu olan şirket grubunu veya bölümü gösteren kuruluş birimidir.  Proje yöneticisinin organzasyon birimi tanımlanmamışsa, bu alan varsayılan olarak proje parametrelerinde tanımlanan değere göredir.
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
