---
title: Proje kopyalama
description: Bu konuda, Dynamics 365 Project Operations'ta projeleri kopyalama hakkında bilgiler sağlanmaktadır.
author: ruhercul
manager: AnnBe
ms.date: 02/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: af1942e81691d9e13fdcbbf68599c1a8a4004582
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2021
ms.locfileid: "5479543"
---
# <a name="copy-a-project"></a>Projeyi kopyalama

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Dynamics 365 Project Operations ile, **Projeler** formunda **Projeyi Kopyala** seçeneğini belirleyerek hızlıca yeni projeler oluşturabilirsiniz. Bir proje kopyalamak için kopyalamak istediğiniz projeyi açın ve **proje Kopyala** seçeneğini belirleyin. Eylem şunları kopyalar:

- Proje özellikleri (Tahmini başlangıç tarihi, kaynak projeden kopyalanır)
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
