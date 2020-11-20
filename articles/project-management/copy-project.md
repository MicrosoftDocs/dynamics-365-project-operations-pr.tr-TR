---
title: Proje kopyalama
description: Bu konuda, Dynamics 365 Project Operations'ta projeleri kopyalama hakkında bilgiler sağlanmaktadır.
author: ruhercul
manager: AnnBe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 53c72e5fd680eb28128644788752368705440445
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131817"
---
# <a name="copy-a-project"></a>Proje kopyalama

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Dynamics 365 Project Operations ile **Projeler** formunda **Projeyi Kopyala** eylemini seçerek hızlıca yeni projeler oluşturabilirsiniz. Bir proje kopyalamak için kopyalamak istediğiniz projeyi açın ve **proje Kopyala** seçeneğini belirleyin. Eylem şunları kopyalar:

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

Program aracılığıyla uygulamasına yönelik kopyalama projesi hakkında daha fazla bilgi için bkz. [Kopyalama projesi ile proje şablonları geliştirme](dev-copy-project.md).
