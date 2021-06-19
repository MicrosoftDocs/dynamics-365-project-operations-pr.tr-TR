---
title: Proje tabanlı teklif satırına bir projeyle ilgili tahminleri aktarma - lite
description: Bu konuda, tahminleri projeden teklif satırına içe aktarma hakkında bilgiler sağlanmaktadır.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5cc1643751be25864e641ea297180fbefb1f2161
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003295"
---
# <a name="import-estimates-for-a-project-to-a-project-based-quote-line"></a>Proje tabanlı teklif satırına bir projeyle ilgili tahminleri aktarma 

_**Aşağıdakilere İçin Geçerlidir:** Lite dağıtımı - anlaşmadan proforma faturaya, kaynak/stoklanmayan tabanlı senaryolar için Project Operations_

Projenin satış öncesi aşama sırasında oluşturulması durumunda mali tahmini, projeden proje tabanlı teklif satırına içe aktarmayı seçebilirsiniz.

1. Proje tabanlı teklif satırının **Proje** alanında proje bilgilerine sahip olduğundan emin olun.
2. **Teklif satırı ayrıntıları** sekmesinde, **Proje Tahmininden İçe Aktar**'ı seçin.
3. İletişim sayfası açıldığında, aşağıdaki özetleme seçeneklerinden birini belirleyin.

  - **İşlem sınıfı**
  - **Kategori**
  - **Rol** 
  - **Proje görevi**

Seçiminize bağlı olarak, bu teklif satırındaki tüm işlem sınıfları için projeden alınan tahmin, üzerine kopyalanır. Hangi hareket sınıflarının dahil edildiğini kontrol etmek için proje tabanlı teklif satırındaki **Genel** sekmesini seçin ve **Zamanı Ekle**, **Giderleri Ekle**, **Malzemeleri Ekle** ve **Ücretleri Ekle** değerlerini kontrol edin.  Hangi görevlerin dahil edildiğini denetlemek için teklif satırındaki **Ücretli Görevler** sekmesini seçin.

İlişkili ve Dahil Edilen Hareket Sınıflarına bağlı olarak, bu görev ve hareket sınıfı birleşimlerinin tahminleri teklif satırına aktarılır.

Tahminleri içe aktardığınızda sistem, fiyatlandırmayı proje tabanlı teklif satırında ayarlanan teklife ve faturalama türüne eklenen proje fiyat listelerine bağlı olarak varsayılan yapar. Proje tabanlı teklif satırında bir görev, rol veya kategori borçlandırılamaz olarak ayarlanırsa içe aktarılan tahmin satırı borçlandırılamaz olarak ayarlanır ve teklif satırının teklif değerine eklenmez.

Teklif satırında satır ayrıntıları bulunduğunda, teklif satırındaki **Teklif Değeri** ve **Tahmini Vergi** alanları özetlenir ve düzenlenemez.

Birden çok özet seçeneği belirlendiğinde sistem, seçilen tüm seçeneklere göre özetlemeye çalışır. Bu, içe aktarılan teklif satırlarının çıktısının yalnızca bir özetleme seçeneği belirlemenizden daha fazlası olacağı anlamına gelir.

Örneğin, projede giderler için aşağıdaki tahmin satırları varsa.

| Görev | Kategori | Tarih | Miktar | Birim fiyatı | Miktar |
| --- | --- | --- | --- | --- | --- |
| A Görevi | Uçak bileti ücreti | 1.10.2020 | 4 | 400 | 1600 |
| B Görevi | Otel | 1.10.2020 | 4 | 200 | 800 |
| C Görevi | Otel | 1.11.2020 | 2 | 200 | 400 |

Kullanıcı, İşlem sınıfına göre özetlemeyi seçtiğinde, aşağıdaki bilgiler içe aktarılır.

| Görev | Kategori | Tarih | Miktar | Birim fiyatı | Miktar |
| --- | --- | --- | --- | --- | --- |
|||1.10.2020 | 3.34 | 840 | 2800 |

Kullanıcı, İşlem sınıfı ve Kategoriye göre özetlemeyi seçtiğinde, aşağıdaki bilgiler içe aktarılır.

| Görev | Kategori | Tarih | Miktar | Birim fiyatı | Miktar |
| --- | --- | --- | --- | --- | --- |
| A Görevi | Uçak bileti ücreti | 1.10.2020 | 4 | 400 | 1600 |
| | Otel | 1.10.2020 | 6 | 200 | 1200 |

Kullanıcı, İşlem sınıfı, Kategori ve Yaprak Düğüm Görevine göre özetlemeyi seçtiğinde, aşağıdaki bilgiler içe aktarılır. Bu sonucun, projedeki sonuçla aynı olduğuna dikkat edin.

| Görev | Kategori | Tarih | Miktar | Birim fiyatı | Miktar |
| --- | --- | --- | --- | --- | --- |
| A Görevi | Uçak bileti ücreti | 1.10.2020 | 4 | 400 | 1600 |
| B Görevi | Otel | 1.10.2020 | 4 | 200 | 800 |
| C Görevi | Otel | 1.11.2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
