---
title: Proje kopyalama
description: Bu konuda, Dynamics 365 Project Operations'ta projeleri kopyalama hakkında bilgiler sağlanmaktadır.
author: ruhercul
ms.date: 03/07/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: e9b637d2d282d123dfacb8a295292ea06549aa1e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574454"
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
- Proje denetim listeleri
- Proje demetleri

## <a name="project-properties"></a>Proje özellikleri

Proje kopyalandığında, aşağıdaki alanlardaki değerler kopyalanır.

| Alan | Stoğu Tutulmayan Malzemeler İçin Project Operations | Project Operations Lite | Project for the Web |
|-------|------------------------------------------|-------------------------|---------------------|
| Veri Akışı Adı | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Description | :heavy_check_mark: | :heavy_check_mark: | |
| Customer | :heavy_check_mark: | :heavy_check_mark: | |
| Takvim Şablonu | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Currency | :heavy_check_mark: | :heavy_check_mark: | |
| Sözleşme Birimi | :heavy_check_mark: | :heavy_check_mark: | |
| Sahibi Olan Şirket | :heavy_check_mark: | | |
| Proje Yöneticisi | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Status | :heavy_check_mark: | :heavy_check_mark: | |
| Genel Proje Durumu | :heavy_check_mark: | :heavy_check_mark: | |
| Açıklamalar | :heavy_check_mark: | :heavy_check_mark: | |
| Tahminler | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Tahmini Başlangıç Tarihi</p><p><strong>Not:</strong> Bu alan, projenin kopyadan oluşturulduğu tarihi belirtir. | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Tahmini Bitiş Tarihi</p><p><strong>Not:</strong> Bu alandaki tarih, kopyadan oluşturulan yeni projenin başlangıç tarihine göre düzenlenir.</p> | :heavy_check_mark: | :heavy_check_mark: | |
| Çalışma Süresi (Saat) | :heavy_check_mark: | :heavy_check_mark: | |
| Tahmini İşçilik Maliyeti | :heavy_check_mark: | :heavy_check_mark: | |
| Tahmini Gider Maliyeti | :heavy_check_mark: | :heavy_check_mark: | |
| Tahmini Malzeme Maliyeti | | :heavy_check_mark: | |

> [!NOTE]
> Projeyi kopyala, uzun süre çalışan bir işlemdir. Proje kayıtları, bunların ilgili öznitelikleri ve pek çok ilişkili varlık da kopyalanır. İşlemin uzun süre çalışması nedeniyle, kopyalama başladıktan sonra hedef proje sayfası kopyalama işlemi tamamlanana kadar düzenleme için kilitlenir.

## <a name="work-breakdown-structure"></a>İş kırılım yapısı

Proje kopyalandığında, kaynağı yüklü iş kırılım yapısının tamamı kopyalanır. Adlandırılmış kaynaklar, genel kaynaklarla değiştirilir. Adlandırılmış kaynaklar, genel kaynakla aynı çalışma saatlerine sahip değilse zamanlama yeniden hesaplanır ve görev süreleri değişebilir.

## <a name="project-team-members"></a>Proje takımı üyeleri

Proje takımı, kaynak projeden kopyalandığında, genel kaynaklar kopyalanır. Genel kaynak atamaları da kaynak projede olduğu gibi korunur. Adlandırılmış kaynaklar, genel takım üyelerine dönüştürülür.

> [!NOTE]
> Takım üyeleri ve atamalar Project for the Web'de kopyalanamaz.

## <a name="estimates"></a>Tahminler

Proje kopyalandığında, kaynak, gider ve malzeme tahmin satırları kaynak projeden kopyalanır. 

Program aracılığıyla uygulamasına yönelik kopyalama projesi hakkında daha fazla bilgi için bkz. [Kopyalama projesi ile proje şablonları geliştirme](dev-copy-project.md).

## <a name="quotes-and-contracts"></a>Teklifler ve sözleşmeler

Teklifler ve sözleşmeler hedef projeye bağlanamaz.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
