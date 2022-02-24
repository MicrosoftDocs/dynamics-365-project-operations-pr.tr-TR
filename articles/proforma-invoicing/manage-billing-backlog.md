---
title: Fatura biriktirme listesini yönetme
description: Bu konu, Project Operations'ta faturalama biriktirme listesini görüntüleme ve bunlarla çalışma hakkında bilgiler sağlar.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bec6afe04a705d4f55ac3a7de93a64b47021fbb4
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122367"
---
# <a name="manage-the-billing-backlog"></a>Fatura biriktirme listesini yönetme

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Dynamics 365 Project Operations ile çalışmanıza ve faturalama biriktirme listesine yönetmenize yardımcı olacak iki adanmış görünüme sahiptir. Bunlar **Sabit fiyatlı kilometre taşları** ve **zaman ve malzeme faturalama biriktirme listesi** olarak bir görünüm seçmek için, Project Operations'nin **satış** alanında, sol gezinti sayfasında, **fatura**'yı seçin. Fatura biriktirme listesi bağlantıları orada depolanır.

## <a name="fixed-price-milestones"></a>Sabit Fiyat Kilometre Taşları

Bu görünümde tüm sabit fiyat kilometre taşları sistemdeki Proje sözleşmesi satırlarının tümünde listelenir. Tek veya birden çok kilometre taşı **faturaya hazır** veya Bu görünümden **faturaya hazır değil** olarak işaretlenebilir. Kilometre taşını **faturaya hazır** olarak işaretlediğinizde , kilometre taşı taslak fatura için kullanılabilir duruma gelir.

Birden çok müşteri sözleşme satırındaki sabit fiyatlı faturalama yöntemi olduğunda, sözleşme satırındaki her müşteri için bir aşama oluşturulur. Kullanıcı bir kilometre taşı oluşturur ve bu kilometre taşına müşteri = özgü kilometre taşı kayıtları dahili olarak, sözleşme satırındaki her müşteri için tanımlanan faturalama yüzdesine göre bölünmüş olarak bölünür. **Sabit fiyatlı kilometre taşları** görünümünde, müşteriye özgü bağımsız kilometre taşı kayıtlarını görürsünüz. Bu kilometre taşı kayıtlarının her biri, Bu görünümden ayrı olarak **Faturaya hazır** olarak işaretlenebilir. İlgili kilometre taşlardan biri veya birkaçı, **Faturaya hazır** olarak işaretlendiğinde , başlık, **başlatılmamış** durumdan **Devam ediyor** durumuna gider. Tüm kilometre taşı bölmelerini faturalandığında, başlık kilometre taşı durumu **tamamlandı** olur.

Bir taslak faturadaki kilometre taşı, bu görünümde, **oluşturulan müşteri faturasının** faturalama durumu ile gösterilir. Taslak fatura teyit edildiğinde, bu kayıttaki faturalama durumu **deftere nakledilen fatura** olarak güncelleştirilir. Bu durum değerini özel kod kullanarak güncelleştirmek önerilmez. Bu durum değerleri özel kodla güncelleştirildiğinde Project Operations düzgün çalışmaz.

## <a name="time-and-material-billing-backlog"></a>Zaman ve Malzeme Faturalama Biriktirme Listesi

Bu görünümde, sistemdeki tüm proje sözleşmeleri arasında faturalanmamış tüm faturalandırılmamış satış gerçekleri listelenir. Tek veya birden çok faturalandırılmamış satış fiilleri **faturaya hazır** veya Bu görünümden **faturaya hazır değil** olarak işaretlenebilir. Faturalandıralınmamış bir satış fiili gerçek değeri **faturaya hazır** olarak işaretlemek bunu bir taslak faturaya koymanıza olanak sağlar.

**Aşılamaz Limit** durumu **Başarısız** olan faturalandırılmamış satış fiileri **Faturalamaya hazır** olarak işaretlenemez. Bu gerçeklerin bu şekilde işaretlenmesi gerekiyorsa, sözleşme satırındaki diğer fiili değerler üzerindeki durumu sıfırlayın ve ardından **aşmayan** durumunu değerlendirin.

Zaman ve malzeme faturalama yöntemi olan çok müşterili sözleşme satırlarında, saat ve giderler onaylandığında, sözleşme satırındaki her müşteri için tanımlanan faturalama yüzdesiyle ilgili olarak, sözleşme satırındaki her müşteri için faturalandırmayan bir satış fiili gerçek oluşturulur. **Zaman ve malzeme faturalama biriktirme listesi** görünümünde, müşteriye özgü bu bağımsız satışlar fiili değerlerini görürsünüz. Bu faturalandırılmamış satış fiili kayıtlarının her biri, Bu görünümden ayrı olarak **Faturaya hazır** olarak işaretlenebilir.

Bir taslak faturadaki faturalandırılmamış satış fiileri bu görünümde, **oluşturulan müşteri faturasının** **faturalama durumu** ile gösterilir. Taslak fatura teyit edildiğinde, bu kayıttaki faturalama durumu **deftere nakledilen müşteri fatura** olarak güncelleştirilir. Bu durum değerini bu durumdayken özel kod kullanarak güncelleştirmek önerilmez. Bu durum değerleri özel kodla güncelleştirildiğinde Project Operations düzgün çalışmaz.
