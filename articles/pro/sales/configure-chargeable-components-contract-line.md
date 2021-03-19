---
title: Proje tabanlı sözleşme satırının borçlandırılabilir bileşenlerini yapılandırma -lite
description: Bu konu, Project Operations'daki sözleşme satırlarına ücretlendirilebilir bileşenlerin nasıl eklenebilir olduğu hakkında bilgi sağlar.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cf3f2a28fc992d6444b35d6ffa0c3f6cadcf16ea
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273942"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line---lite"></a>Proje tabanlı sözleşme satırının borçlandırılabilir bileşenlerini yapılandırma -lite

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Proje tabanlı bir sözleşme satırı *dahil edilen* bileşenler ve *Borçlandırılabilir* bileşenler kavramıdır.

Dahil edilen bileşenler, şu bileşenlere tabi olan bileşenlerdir:

  - Faturalama yöntemi ve müşteri bölmeleri
  - Aşılamaz sınırlar 
  - Proje tabanlı sözleşme satırında tanımlanan fatura sıklığı ayarları

Dahil edilen bileşenlerin bir alt kümesi, **Fatura Türü** alanı kullanılarak ücretlendirilebilir olarak işaretlenebilir. **Faturalama Türü** alanı, sözleşme satırı bağlamında aşağıdaki değerlere izin veren bir seçenek kümesidir:

  - Borçlandırılabilir
  - Borçlandırılamaz

Ücretlendirilebilir bileşenler görevlerde, rollerde ve işlem kategorilerinde tanımlanabilir.

Borçlandırılabilirlik, bir proje sözleşme satırı için görevlerde tanımlanır ve o satıra dahil edilen tüm işlem sınıflarına uygulanır. Sözleşme satırındaki **Görevleri Dahil Et** alanı boşsa veya **Tüm proje** olarak ayarlanmışsa **Borçlandırılabilir görevler** sekmesi kullanılamaz.

Borçlandırılabilirlik, bir teklif satırı için rollerde tanımlanır ve yalnızca **Zaman** işlem sınıfına uygulanır. Sözleşme satırına **Zamanı dahil et** alanı proje teklif satırında **Hayır** olarak ayarlanırsa **ücrete tabi roller** sekmesi kullanılamaz.

Borçlandırılabilirlik, bir proje sözleşme satırı için işlem kategorilerinde tanımlanır ve yalnızca **Gider** işlem sınıfına uygulanır. Sözleşme satırına **Giderleri dahil et** alanı proje teklif satırında **Hayır** olarak ayarlanırsa **ücrete tabi kategoriler** sekmesi kullanılamaz.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Proje görevini borçlandırılabilir veya borçlandırılamayan olarak güncelleştirme

Proje görevi, aşağıdaki kurulumu olası yapan belirli bir sözleşme satırı bağlamında Masraflandırılabilir veya borçlandırılamayan olabilir:

Proje tabanlı bir sözleşme satırı **Zaman** ve belirli bir görev içeriyorsa, **T1** bununla ücretli olarak ilişkilendirilir. **Giderleri** içeren ikinci bir sözleşme satırı varsa , sözleşme satırındaki T1 görevini borçlandırılamayan olarak ilişkilendirebilirsiniz. Sonuçta, görevde kaydedilen tüm zaman borçlandırılabilir ve tüm giderler Borçlandırılamaz.

Görevin faturalama türü, sözleşme satırı görevleri alt kılavuzundaki **faturalama türü** alanını güncelleştirerek, sözleşme satırındaki **ücrete tabi Görevler** sekmesinde yapılandırılabilir. Alternatif olarak, görevle ilişkili sözleşme satırlarını gösteren bir projenin görev faturalama kurulumunun alt kılavuzundaki **fatura türü** alanını güncelleştirebilirsiniz.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Rolü borçlandırılabilir veya borçlandırılamayan olarak güncelleştirme

Bir rol, belirli bir sözleşme satırındaki Borçlandırılabilir veya borçlandırılamayan olabilir.

Bir rolün fatura türü, sözleşme satırının **Ücretlendirilebilir Roller** sekmesinde yapılandırılabilir. Bunu yapmak için, **Borçlandırılabilir roller** alt kılavuzundaki **faturalama türü** alanını güncelleştirin.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Bir işlem kategorinin ücretlendirilebilir veya ücretlendirilemez olarak güncelleştirin

Bir işlem kategorisi, belirli bir sözleşme satırındaki Borçlandırılabilir veya borçlandırılamayan olabilir.

Bir işlemin fatura türü, proje tabanlı sözleşme satırının **Ücretlendirilebilir Kategoriler** sekmesinde yapılandırılabilir. Bunu yapmak için, **Borçlandırılabilir Kategoriler** alt kılavuzundaki **faturalama türü** alanını güncelleştirin.

### <a name="resolve-chargeability"></a>Şarj edilebilirliği çözme

Bir tahmin veya zaman için oluşturulan fiili, yalnızca sözleşme satırına **saat** dahil edildiğinde Borçlandırılabilir olarak değerlendirilir ve **görev** ve **rol** sözleşme satırında Borçlandırılabilir olarak yapılandırılır.

Bir tahmin veya gider için oluşturulan fiili, yalnızca sözleşme satırına **Gider** dahil edildiğinde Borçlandırılabilir olarak değerlendirilir ve **görev** ve **İşlem kategorisi** sözleşme satırında Borçlandırılabilir olarak yapılandırılır.


| Zaman dahil eder | Gider içerir | Dahil Edilen Görevler | Rol           | Kategori       | Görev                                                                                                      |
|---------------|------------------|----------------|----------------|----------------|-----------------------------------------------------------------------------------------------------------|
| Evet           | Evet              | Tüm Proje | Borçlandırılabilir     | Borçlandırılabilir     | Bir Zaman fiili faturalama: **Ücretli** </br> Geçerli gider faturalama türü: **Borçlandırılabilir**           |
| Evet           | Evet              | Seçili görevler | Borçlandırılabilir     | Borçlandırılabilir     | Bir Zaman fiili faturalama: **Ücretli** </br> Geçerli gider faturalama türü: **Borçlandırılabilir**           |
| Evet           | Evet              | Seçili görevler | Borçlandırılamaz | Borçlandırılabilir     | Bir Zaman fiili faturalama: **Ücretlendirilemez** </br> Geçerli gider faturalama türü: **Borçlandırılabilir**       |
| Evet           | Evet              | Seçili görevler | Borçlandırılabilir     | Borçlandırılabilir     | Bir Zaman fiili faturalama: **Ücretlendirilemez** </br> Geçerli gider faturalama türü: **Borçlandırılamaz** |
| Evet           | Evet              | Seçili görevler | Borçlandırılamaz | Borçlandırılabilir     | Bir Zaman fiili faturalama: **Ücretlendirilemez** </br> Geçerli gider faturalama türü: **Borçlandırılamaz** |
| Evet           | Evet              | Seçili görevler | Borçlandırılamaz | Borçlandırılamaz | Bir Zaman fiili faturalama: **Ücretlendirilemez** </br> Geçerli gider faturalama türü: **Borçlandırılamaz** |
| No            | Evet              | Tüm Proje | Ayarlanamıyor   | Borçlandırılabilir     | Bir Zaman fiili faturalama: **Kullanılamaz**</br>Geçerli gider faturalama türü: **Borçlandırılabilir**          |
| No            | Evet              | Tüm Proje | Ayarlanamıyor   | Borçlandırılamaz | Bir Zaman fiili faturalama: **Kullanılamaz**</br> Geçerli gider faturalama türü: **Borçlandırılamaz**     |
| Evet           | No               | Tüm Proje | Borçlandırılabilir     | Ayarlanamıyor   | Bir Zaman fiili faturalama: **Ücretli** </br> Geçerli gider faturalama türü: **Kullanılamaz**        |
| Evet           | No               | Tüm Proje | Borçlandırılamaz | Ayarlanamıyor   | Bir Zaman fiili faturalama: **Ücretlendirilemez** </br>Geçerli gider faturalama türü: **Kullanılamaz**   |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]