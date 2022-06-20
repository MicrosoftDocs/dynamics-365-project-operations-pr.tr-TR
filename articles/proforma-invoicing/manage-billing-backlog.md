---
title: Fatura biriktirme listesini yönetme
description: Bu makalede, Project Operations'ta faturalama biriktirme listesini görüntüleme ve bunlarla çalışma konusunda bilgiler sağlanmaktadır.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 5be05639650bb5b9d646067e8d83bada60824081
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929402"
---
# <a name="manage-billing-backlog"></a>Fatura biriktirme listesini yönetme

**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations

Dynamics 365 Project Operations'ta, fatura biriktirme listesini yönetmeye yardımcı olmak için ayrılmış görünümler bulunur. Faturalama biriktirme listesini yönetmek için, **Satışlar** alanında, **fatura** altında bağlantıları seçin. 

Aşağıdaki görünümler kullanılabilir:

- Elde Tutulan Tutarlar ve Avanslar
- Kullanılabilir Elde Tutulan Tutarlar ve Avanslar
- Sabit Fiyat Kilometre Taşları
- Zaman ve Malzeme Faturalama Biriktirme Listesi

## <a name="retainers-and-advances"></a>Elde Tutulan Tutarlar ve Avanslar

**Elde Tutulan Tutarlar ve Avanslar** görünümü, tüm proje sözleşmelerindeki elde tutulan tutarlar ve avansları listeler. Bir Elde tutulan tutar veya avans faturalandıktan sonra, kullanım avans tutarı kullanıma hazır olur.

## <a name="available-retainers-and-advances"></a>Kullanılabilir Elde Tutulan Tutarlar ve Avanslar

**Kullanılabilir Elde Tutulan Tutarlar ve Avanslar** görünümü, tüm proje sözleşmelerindeki kullanılabilir elde tutulan tutarlar ve avansları listeler. Bir Elde tutulan tutar veya avans faturalandıktan sonra, kullanım avans tutarı kullanıma hazır olur ve listeye eklenir. Elde edilen tutar veya avans tutarı tamamen kullanıldıktan sonra listeden kaldırılır.

## <a name="fixed-price-milestones"></a>Sabit Fiyat Kilometre Taşları

**Sabit Fiyat Kilometre Taşları** görünümü, tüm proje sözleşmesi satırlarındaki tüm sabit fiyat aşamalarını listeler. Bu görünümde, bir veya birden çok kilometre taşı **Faturalamak için hazır** veya **Faturalamak için hazır değil** olarak işaretlenebilir. Bir kilometre taşını **Faturaya hazır** olarak işaretlemek bunu bir taslak faturaya koymak için kullanılabilir hale getirir.

Çok müşterili sözleşme satırları sabit fiyatlı faturalama yöntemi olduğunda, sözleşme satırındaki her müşteri için bir kilometre taşı oluşturulur. Kilometre taşı oluşturulabilir ve ardından müşteriye özgü bağımsız kilometre taşı kayıtlarına ayrılabilir. Bu bölme, sözleşme satırındaki her müşteri için tanımlanan faturalama yüzdesine göre dahili ve sözleşmedir. **Sabit fiyatlı kilometre taşları** görünümünde, müşteriye özgü bağımsız kilometre taşı kayıtlarını görürsünüz. Bu kilometre taşı kayıtlarının her biri, Bu görünümden ayrı olarak **Faturaya hazır** olarak işaretlenebilir. Bir veya birden fazla ilgili kilometre taşı bölmesi **Faturalamak için hazır** olarak işaretlendiğinde **Devam Ediyor** olan üst bilgi durumu, **Başlamadı** olarak güncelleştirilir. Tüm kilometre taşı bölmelerini faturalandığında, üst bilgi kilometre taşı durumu **Tamamlandı** olarak güncelleştirilir.

Bir taslak faturadaki kilometre taşı, bu görünümde, **oluşturulan müşteri faturasının** faturalama durumu ile gösterilir. Taslak fatura teyit edildiğinde, kayıttaki faturalama durumu **Müşteri faturası deftere nakledildi** olarak güncelleştirilir. 

> [!NOTE] 
> Bu durum değerini, özel kod kullanarak güncelleştirmeyin. Bu durum değerleri özel kodla güncelleştirildiğinde Project Operations düzgün çalışmaz.

## <a name="time-and-material-billing-backlog"></a>Zaman ve Malzeme Faturalama Biriktirme Listesi

**Zaman ve malzeme faturalama biriktirme listesi** görünümü, tüm faturalanmamış satış fiili değerlerini sistemdeki tüm proje sözleşmeleri arasında listeler. Tek veya birden çok faturalandırılmamış satış fiilleri **faturaya hazır** veya Bu görünümden **faturaya hazır değil** olarak işaretlenebilir. Faturalandıralınmamış bir satış fiili gerçek değeri **faturaya hazır** olarak işaretlemek bunu bir taslak faturaya koymanıza olanak sağlar.

**Aşılamaz** durumu **Başarısız** olan faturalandırılmamış satış tahakkukları **Faturaya hazır** olarak işaretlenemez. Gerçek değerlerin **Faturalamak için hazır** olarak işaretlenmesi gerekiyorsa sözleşme satırındaki diğer gerçek değerlerin durumunu sıfırlayın ve ardından **Aşılamaz** durumunu yeniden değerlendirin.

Çok müşterili sözleşme satırları zaman ve malzeme faturalama yöntemi içeriyorsa, saat ve giderler onaylandığında, her bir müşteri için tanımlanan faturalama yüzdesiyle ilgili olarak, sözleşme satırındaki her müşteriye için faturalandırmayan bir satış fiili gerçek oluşturulur. **Zaman ve malzeme faturalama biriktirme listesi** görünümünde, müşteriye özgü bu bağımsız satışlar fiili değerlerini görürsünüz. Bu faturalandırılmamış satış fiili kayıtlarının her biri, Bu görünümden ayrı olarak **Faturaya hazır** olarak işaretlenebilir.

Taslak faturada bulunan faturalanmamış satış gerçek değeri bu görünümde, **Müşteri Faturası Oluşturuldu** fatura durumu ile görüntülenir. Taslak fatura teyit edildiğinde, bu kayıttaki faturalama durumu **deftere nakledilen müşteri fatura** olarak güncelleştirilir. 

> [!NOTE] 
> Bu durum değerini, özel kod kullanarak güncelleştirmeyin. Bu durum değerleri özel kodla güncelleştirildiğinde Project Operations düzgün çalışmaz.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
