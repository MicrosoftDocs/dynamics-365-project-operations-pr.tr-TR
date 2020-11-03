---
title: Proje tabanlı sözleşme satırına tahmin aktarma
description: Bu konuda, tahminleri projeden sözleşme satırına içe aktarma hakkında bilgiler sağlanmaktadır.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f2b9cbb4cce1691f262c85d95849e01f1a812d51
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/20/2020
ms.locfileid: "4086559"
---
# <a name="import-an-estimate-to-a-project-based-contract-line"></a>Proje tabanlı sözleşme satırına tahmin aktarma

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Dynamics 365 Project Operations'ta, tahminleri bir projeden proje tabanlı bir sözleşme satırına aktarabilirsiniz.

1. Proje tabanlı sözleşme satırındaki **proje** alanının doldurulduğunu doğrulayın.
2. Sekme **sözleşme satırı ayrıntıları** sekmesinde, alt ızgarada **Proje tahmininden ithal et** 'i seçin. Özetleme seçenekleri bulunan bir iletişim kutusu sayfası açılır. Kullanılabilir özetleme seçenekleri, **İşlem sınıfı** , **Kategori** , **Rol** ve **Proje görevi** 'dir. Özelleştirme seçiminize bağlı olarak, bu sözleşme satırındaki tüm işlem sınıfları için projeden alınan tahmin, üzerine kopyalanır. 
3. Hangi işlem sınıflarının eklendiğini denetlemek için sözleşme satırında **Genel** sekmesini seçin ve **Zaman Ekle** , **Gider Ekle** ve **Ücret Ekle** değerlerini kontrol edin.

Tahminleri içe aktardığınızda sistem, fiyatlandırmayı sözleşme satırında ayarlanan teklife ve faturalama türüne eklenen proje fiyat listelerine bağlı olarak varsayılan yapar. Sözleşme satırında bir görev, rol veya kategori borçlandırılamaz olarak ayarlanırsa içe aktarılan tahmin satırı borçlandırılamaz olarak ayarlanır ve sözleşme satırının sözleşme değerine eklenmez.

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
| &nbsp;  | &nbsp;  | 1.10.2020 | Kategori 3.34 | 840 | Kategori 2800 |

Kullanıcı, **İşlem sınıfı** ve **Kategoriye** göre özetlemeyi seçtiğinde, aşağıdaki bilgiler içe aktarılır.

| Görev | Kategori | Tarih | Miktar | Birim fiyatı | Miktar |
| --- | --- | --- | --- | --- | --- |
| A Görevi | Uçak bileti ücreti | 1.10.2020 | 4 | 400 | 1600 |
| &nbsp;  | Otel | 1.10.2020 | 6 | 200 | 1200 |

Kullanıcı, **İşlem sınıfı** , **Kategori** ve **Yaprak Düğüm Görevine** göre özetlemeyi seçtiğinde, aşağıdakiler içe aktarılır. Bu sonucun, projedeki sonuçla aynı olduğuna dikkat edin:

| Görev | Kategori | Tarih | Miktar | Birim fiyatı | Miktar |
| --- | --- | --- | --- | --- | --- |
| A Görevi | Uçak bileti ücreti | 1.10.2020 | 4 | 400 | 1600 |
| B Görevi | Otel | 1.10.2020 | 4 | 200 | 800 |
| C Görevi | Otel | 1.11.2020 | 2 | 200 | 400 |
