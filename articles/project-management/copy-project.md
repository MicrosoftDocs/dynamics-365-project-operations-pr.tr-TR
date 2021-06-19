---
title: Proje kopyalama
description: Bu konuda, Dynamics 365 Project Operations'ta projeleri kopyalama hakkında bilgiler sağlanmaktadır.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c3055ab5b8c07faa2bc9167956d283e2a66029dd
ms.sourcegitcommit: 173f2b1f4e063c440a5f78d76d456c62aadbd89e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2021
ms.locfileid: "6091278"
---
# <a name="copy-a-project"></a>Projeyi kopyalama

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Dynamics 365 Project Operations ile, **Projeler** formunda **Projeyi Kopyala** seçeneğini belirleyerek hızlıca yeni projeler oluşturabilirsiniz. Bir proje kopyalamak için kopyalamak istediğiniz projeyi açın ve **proje Kopyala** seçeneğini belirleyin. Eylem, aşağıdakileri kopyalayacaktır:

- Proje özellikleri 
- İş kırılım yapısı
- Proje takımı üyeleri
- Proje tahminleri
- Proje gider tahminleri
- Proje malzeme tahminleri

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
- Tahmini Başlangıç Tarihi: Bu, projenin kopyadan oluşturulduğu tarihtir.
- Tahmini Bitiş Tarihi: Bu tarih, kopyadan oluşturulan yeni projenin başlangıç tarihine göre belirlenir.
- Çalışma Süresi (Saat)
- Tahmini İşçilik Maliyeti
- Tahmini Gider Maliyeti
- Tahmini Malzeme Maliyeti

> [!NOTE]
> Projeyi kopyala, uzun süre çalışan bir işlemdir. Proje kayıtları, bunların ilgili öznitelikleri ve pek çok ilişkili varlık da kopyalanır. İşlemin uzun süre çalışması nedeniyle, kopyalama başladıktan sonra hedef proje sayfası kopyalama işlemi tamamlanana kadar düzenleme için kilitlenir.

## <a name="work-breakdown-structure"></a>İş kırılım yapısı

Proje kopyalandığında, kaynağı yüklü iş kırılım yapısının tamamı kopyalanır. Adlandırılmış kaynaklar, genel kaynaklarla değiştirilir. Adlandırılmış kaynaklarda genel kaynakla aynı çalışma saatleri yoksa zamanlama yeniden hesaplanır ve görev süreleri değişebilir.

## <a name="project-team-members"></a>Proje takımı üyeleri

Proje takımı, kaynak projeden kopyalandığında, genel kaynaklar kopyalanır. Genel kaynak atamaları da kaynak projede olduğu gibi korunur. Adlandırılmış kaynaklar, genel takım üyelerine dönüştürülür.

## <a name="estimates"></a>Tahminler

Proje kopyalandığında, kaynak, gider ve malzeme tahmin satırları kaynak projeden kopyalanır. 

Program aracılığıyla uygulamasına yönelik kopyalama projesi hakkında daha fazla bilgi için bkz. [Kopyalama projesi ile proje şablonları geliştirme](dev-copy-project.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
