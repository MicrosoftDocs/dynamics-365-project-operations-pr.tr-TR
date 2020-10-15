---
title: Proje kopyalama
description: Bu konuda, Dynamics 365 Project Operations'ta projeleri kopyalama hakkında bilgiler sağlanmaktadır.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e35dc725e7938e9f59f7151dd1b37500fabf77a4
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908693"
---
# <a name="copy-a-project"></a>Proje kopyalama

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Dynamics 365 Project Operations ile **Projeler** formunda **Projeyi Kopyala** eylemini kullanarak hızlıca yeni projeler oluşturabilirsiniz. Projeyi kopyalamak için bir projeyi ve ardından **Kopyala**'yı seçin. Eylem şunları kopyalar:

- Proje özellikleri
- İş kırılım yapısı
- Proje takımı üyeleri
- Proje tahminleri
- Proje gider tahminleri

## <a name="project-properties"></a>Proje özellikleri

Proje kopyalandığında, aşağıdaki alanlardaki değerler kopyalanır:

- Veri Akışı Adı
- Veri Akışı Açıklaması
- Müşteri
- Takvim Şablonu
- Para birimi
- Sözleşme Birimi
- Proje Yöneticisi
- Durum
- Genel Proje Durumu
- Açıklamalar
- Tahminler
- Tahmini Başlangıç Tarihi
- Bitiş Tarihi
- Çalışma Süresi (Saat)
- Tahmini İşçilik Maliyeti
- Tahmini Gider Maliyeti

## <a name="work-breakdown-structure"></a>İş kırılım yapısı

Proje kopyalandığında, kaynağı yüklü iş kırılım yapısının tamamı kopyalanır. Adlandırılmış kaynaklar, genel kaynaklarla değiştirilir. Adlandırılmış kaynaklarda genel kaynakla aynı çalışma saatleri yoksa zamanlama yeniden hesaplanır ve görev süreleri değişebilir.

## <a name="project-team-members"></a>Proje takımı üyeleri

Proje takımı, kaynak projeden kopyalandığında, genel kaynaklar kopyalanır. Genel kaynak atamaları da kaynak projede olduğu gibi korunur. Adlandırılmış kaynaklar, genel takım üyelerine dönüştürülür.

## <a name="estimates"></a>Tahminler

Proje kopyalandığında, kaynak projeden kaynak ve gider tahmini satırları kopyalanır.