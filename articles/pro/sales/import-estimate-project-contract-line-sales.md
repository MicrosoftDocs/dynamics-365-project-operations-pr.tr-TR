---
title: Bir projedeki tahminleri bir proje sözleşme satırına içeri aktarma
description: Bu makalede, projeden sözleşme satırına finansal tahminleri içe aktarma konusunda bilgiler sağlanmaktadır.
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 73ae0ccbb5372c9dfbc28ac154094c89add0913d
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824699"
---
# <a name="import-estimates-from-a-project-to-a-project-contract-line"></a>Bir projedeki tahminleri bir proje sözleşme satırına içeri aktarma

_**Şunlar için geçerlidir:** Lite dağıtım - anlaşmadan proforma faturaua kadar, Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_ _

Dynamics 365 Project Operations'ta, proje tabanlı sözleşme satırına bir projedeki tahminleri içeri aktarabilirsiniz.

1. Proje tabanlı sözleşme satırındaki **proje** alanının doldurulduğunu doğrulayın.
2. Sekme **Sözleşme Satırı Ayrıntıları** sekmesinde, alt ızgarada **Proje tahmininden ithal et**'i seçin. Özetleme seçenekleri bulunan bir iletişim kutusu sayfası açılır. Özetleme seçenekleri, **İşlem sınıfı**, **Kategori**, **Rol** ve **Proje görevi**'dir.
3. Özet seçiminize bağlı olarak, bu sözleşme satırındaki tüm işlem sınıfları ve görevleri için projeden alınan tahmin, üzerine kopyalanır. Hangi işlem sınıflarının eklendiğini denetlemek için proje tabanlı sözleşme satırında **Genel** sekmesini seçin ve **Zaman Ekle**, **Gider Ekle** ve **Ücret Ekle** değerlerini kontrol edin. 
4. Hangi görevlerin dahil edildiğini denetlemek için sözleşme satırındaki **Ücretli Görevler** sekmesini seçin. **Dahil Edilen İşlem Sınıfları** alanı **Evet** olan ilgili görevlere bağlı olarak, bu görev ve hareket sınıfı birleşimlerinin tahminleri sözleşme satırına aktarılır.

Tahminleri içe aktardığınızda sistem, fiyatlandırmayı sözleşme satırında ayarlanan sözleşme satırına ve faturalama türüne eklenen proje fiyat listelerine bağlı olarak varsayılan yapar. Sözleşme satırında bir göre borçlandırılamaz olarak ayarlanırsa içe aktarılan tahmin satırı borçlandırılamaz olarak ayarlanır ve sözleşme satırının sözleşme değerine eklenmez.

Sözleşme satırında satır ayrıntıları bulunduğunda, sözleşme satırındaki **Sözleşme Değeri** ve **Tahmini Vergi** alanları özetlenir ve düzenlenemez.

Birden çok özet seçeneği belirlendiğinde sistem, seçilen tüm seçeneklere göre özetlemeye çalışır. Özetleme çıkışı, yalnızca bir özetleme seçeneği seçenden daha fazla alınmış sözleşme satırı ile sonuçlanır.

Örneğin, projede giderler için aşağıdaki tahmin satırları varsa:

| Görev | Kategori | Tarih | Miktar | Birim fiyatı | Miktar |
| --- | --- | --- | --- | --- | --- |
| A Görevi | Uçak bileti ücreti | 1.10.2020 | 4 | 400 | 1600 |
| B Görevi | Otel | 1.10.2020 | 4 | 200 | 800 |
| C Görevi | Otel | 1.11.2020 | 2 | 200 | 400 |

Kullanıcı, **İşlem sınıfına** göre özetlemeyi seçtiğinde, aşağıdaki bilgiler içe aktarılır:

| Görev | Kategori | Tarih | Miktar | Birim fiyatı | Miktar |
| --- | --- | --- | --- | --- | --- |
| &nbsp; | &nbsp; | 1.10.2020 | Kategori 3.34 | 840 | Kategori 2800 |

Kullanıcı, **İşlem sınıfı** ve **Kategoriye** göre özetlemeyi seçtiğinde, aşağıdaki bilgiler içe aktarılır.

| Görev | Kategori | Tarih | Miktar | Birim fiyatı | Miktar |
| --- | --- | --- | --- | --- | --- |
| A Görevi | Uçak bileti ücreti | 1.10.2020 | 4 | 400 | 1600 |
| &nbsp;| Otel | 1.10.2020 | 6 | 200 | 1200 |

Kullanıcı, **İşlem sınıfı**, **Kategori** ve **Yaprak Düğüm Görevine** göre özetlemeyi seçtiğinde, aşağıdakiler içe aktarılır. Bu sonucun, projedeki sonuçla aynı olduğuna dikkat edin:

| Görev | Kategori | Tarih | Miktar | Birim fiyatı | Miktar |
| --- | --- | --- | --- | --- | --- |
| A Görevi | Uçak bileti ücreti | 1.10.2020 | 4 | 400 | 1600 |
| B Görevi | Otel | 1.10.2020 | 4 | 200 | 800 |
| C Görevi | Otel | 1.11.2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
