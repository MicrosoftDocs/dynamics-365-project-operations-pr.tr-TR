---
title: Proje faturalaması biriktirme listesini yönetme
description: Bu konu, projelerde fatura biriktirme listesini yönetirken kullanabileceğiniz çeşitli görünümler hakkında bilgi sağlar.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b3a90d50fcca8824db10594352cbd1e204665c53
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578165"
---
# <a name="manage-project-billing-backlog"></a>Proje faturalaması biriktirme listesini yönetme 

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Dynamics 365 Project Operations'ta, fatura biriktirme listesini yönetmeye yardımcı olmak için ayrılmış görünümler bulunur. Faturalama biriktirme listesini yönetmek için, **Satışlar** alanında, **fatura** altında bağlantıları seçin. 

Aşağıdaki görünümler kullanılabilir:

- Elde Tutulan Tutarlar ve Avanslar
- Kullanılabilir Elde Tutulan Tutarlar ve Avanslar
- Sabit Fiyat Kilometre Taşları
- Ürün Faturalama Biriktirme Listesi
- Zaman ve Malzeme Faturalama Biriktirme Listesi

## <a name="retainers-and-advances"></a>Elde Tutulan Tutarlar ve Avanslar

**Elde tutulan tutarlar ve avanslar** görünümü, sistemdeki tüm proje sözleşmeleri arasında bulunan tüm Elde tutulan tutarları ve avansları listeler. Bir Elde tutulan tutar veya avans faturalandıktan sonra, kullanım avans tutarı kullanıma hazır olur.

## <a name="available-retainers-and-advances"></a>Kullanılabilir Elde Tutulan Tutarlar ve Avanslar

**Mevcut Elde tutulan tutarlar ve avanslar** görünümü, sistemdeki tüm proje sözleşmeleri arasında bulunan tüm mevcut Elde tutulan tutarları ve avansları listeler. Bir Elde tutulan tutar veya avans faturalandıktan sonra, kullanım avans tutarı kullanıma hazır olur ve listeye eklenir. Elde tutulan tutarlar veya avans tutarının tamamen kullanılması, listesinden kaldırılır.

## <a name="fixed-price-milestones"></a>Sabit Fiyat Kilometre Taşları

**Sabit fiyatlı kilometre taşları** görünümü, sistemdeki tüm proje sözleşmesi satırlarındaki tüm sabit fiyat aşamalarını listeler. Tek veya birden çok kilometre taşı **Faturaya hazır** veya Bu görünümden **Faturaya hazır değil** olarak işaretlenebilir. Bir kilometre taşını **Faturaya hazır** olarak işaretlemek bunu bir taslak faturaya koymak için kullanılabilir hale getirir.

Çok müşterili sözleşme satırları sabit fiyatlı faturalama yöntemi olduğunda, sözleşme satırındaki her müşteri için bir kilometre taşı oluşturulur. Kilometre taşı oluşturulabilir ve ardından müşteriye özgü bağımsız kilometre taşı kayıtlarına ayrılabilir. Bu bölme, sözleşme satırındaki her müşteri için tanımlanan faturalama yüzdesine göre dahili ve sözleşmedir. **Sabit fiyatlı kilometre taşları** görünümünde, müşteriye özgü bağımsız kilometre taşı kayıtlarını görürsünüz. Bu kilometre taşı kayıtlarının her biri, Bu görünümden ayrı olarak **Faturaya hazır** olarak işaretlenebilir. İlgili kilometre taşlardan biri veya birkaçı, **Faturaya hazır** olarak işaretlendiğinde , başlık durumu, **başlatılmamış** durumundan **Devam ediyor** olarak güncelleştirilir. Tüm kilometre taşı bölmelerini faturalandığında, başlık kilometre taşı durumu **tamamlandı** olarak güncelleştirilir.

Bir taslak faturadaki kilometre taşı, bu görünümde, **oluşturulan müşteri faturasının** faturalama durumu ile gösterilir. Taslak fatura teyit edildiğinde, kayıttaki faturalama durumu **Müşteri faturası deftere nakledildi** olarak güncelleştirilir. Bu durum değerini özel kod kullanarak güncelleştirmezler. Bu durum değerleri özel kodla güncelleştirildiğinde Project Operations düzgün çalışmaz.

## <a name="product-billing-backlog"></a>Ürün Faturalama Biriktirme Listesi

**Ürün faturalama biriktirme listesi** görünümü, sistemdeki tüm proje sözleşmeleri arasında yer alarak tüm ürün tabanlı sözleşme satırlarını listeler. Tek veya birden çok ürün tabanlı sözleşme satırları **Faturaya Hazır** veya Bu görünümden **Faturaya Hazır Değil** olarak işaretlenebilir. Bir ürün tabanlı sözleşme satırını **Faturaya Hazır** olarak işaretlemek bunu bir taslak faturaya koymak için kullanılabilir hale getirir.

Bir taslak faturada bulunan ürün tabanlı bir sözleşme satırı, bu görünümde, **oluşturulan müşteri faturası**'nın faturalama durumuyla gösterilir. Taslak fatura teyit edildiğinde, bu kayıttaki faturalama durumu **deftere nakledilen müşteri fatura** olarak güncelleştirilir. Bu durum değerini özel kod kullanarak güncelleştirmezler. Bu durum değerleri özel kodla güncelleştirildiğinde Project Operations düzgün çalışmaz.

## <a name="time-and-material-billing-backlog"></a>Zaman ve Malzeme Faturalama Biriktirme Listesi

**Zaman ve malzeme faturalama biriktirme listesi** görünümü, tüm faturalanmamış satış fiili değerlerini sistemdeki tüm proje sözleşmeleri arasında listeler. Tek veya birden çok faturalandırılmamış satış fiilleri **faturaya hazır** veya Bu görünümden **faturaya hazır değil** olarak işaretlenebilir. Faturalandıralınmamış bir satış fiili gerçek değeri **faturaya hazır** olarak işaretlemek bunu bir taslak faturaya koymanıza olanak sağlar.

**Aşılamaz** durumu **Başarısız** olan faturalandırılmamış satış tahakkukları **Faturaya hazır** olarak işaretlenemez. Gerçek tutarların **Faturaya hazır** olarak işaretlenmesi gerekiyorsa sözleşme satırındaki kabul edilen diğer fiili değerlere ait durumu sıfırlayın. ve ardından **Aşılamaz** durumunu yeniden değerlendirin.

Çok müşterili sözleşme satırları zaman ve malzeme faturalama yöntemi içeriyorsa, saat ve giderler onaylandığında, her bir müşteri için tanımlanan faturalama yüzdesiyle ilgili olarak, sözleşme satırındaki her müşteriye için faturalandırmayan bir satış fiili gerçek oluşturulur. **Zaman ve malzeme faturalama biriktirme listesi** görünümünde, müşteriye özgü bu bağımsız satışlar fiili değerlerini görürsünüz. Bu faturalandırılmamış satış fiili kayıtlarının her biri, Bu görünümden ayrı olarak **Faturaya hazır** olarak işaretlenebilir.

Bir taslak faturada bulunan faturalandırılmamış satış tahakkuku, bu görünümde, **oluşturulan müşteri faturası**'nın faturalama durumuyla gösterilir. Taslak fatura teyit edildiğinde, bu kayıttaki faturalama durumu **deftere nakledilen müşteri fatura** olarak güncelleştirilir. Bu durum değerini özel kod kullanarak güncelleştirmezler. Bu durum değerleri özel kodla güncelleştirildiğinde Project Operations düzgün çalışmaz.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
