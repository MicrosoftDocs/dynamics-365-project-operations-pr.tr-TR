---
title: Proje için tahminleri proje tabanlı teklif satırına içe aktarma
description: Bu konuda, tahminleri projeden teklif satırına içe aktarma hakkında bilgiler sağlanmaktadır.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8c0fe18b33207f73848709b99334f64aadc7867a
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086240"
---
# <a name="import-estimates-for-a-project-to-a-project-based-quote-line"></a>Proje için tahminleri proje tabanlı teklif satırına içe aktarma

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_


Projenin satış öncesi aşama sırasında oluşturulması durumunda mali tahmini, projeden proje tabanlı teklif satırına içe aktarmayı seçebilirsiniz.

1. Proje tabanlı teklif satırının **Proje** alanında proje bilgilerine sahip olduğundan emin olun.
2. **Teklif satırı ayrıntıları** sekmesinde, **Proje Tahmininden İçe Aktar** 'ı seçin.
3. İletişim sayfası açıldığında, aşağıdaki özetleme seçeneklerinden birini belirleyin:

  - **İşlem sınıfı**
  - **Kategori**
  - **Rol** 
  - **Proje görevi**

Seçiminize bağlı olarak, bu teklif satırındaki tüm işlem sınıfları için projeden alınan tahmin, üzerine kopyalanır. Hangi işlem sınıflarının eklendiğini denetlemek için proje tabanlı teklif satırında **Genel** sekmesini seçin ve **Zaman Ekle** , **Gider Ekle** ve **Ücret Ekle** değerlerini kontrol edin.

Tahminleri içe aktardığınızda sistem, fiyatlandırmayı proje tabanlı teklif satırında ayarlanan teklife ve faturalama türüne eklenen proje fiyat listelerine bağlı olarak varsayılan yapar. Proje tabanlı teklif satırında bir rol veya kategori borçlandırılamaz olarak ayarlanırsa içe aktarılan tahmin satırı borçlandırılamaz olarak ayarlanır ve teklif satırının teklif değerine eklenmez.

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
| | | 1.10.2020 | 3.34 | 840 | 2800 |

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
