---
title: Proje tabanlı teklif satırına bir projeyle ilgili tahminleri aktarma - lite
description: Bu makalede, projeden teklif satırına tahminleri içe aktarma konusunda bilgiler sağlanmaktadır.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 820d858fecf70e50a9ce8943db706ff6cac29992
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917324"
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
