---
title: Proje tabanlı sözleşme satırının borçlandırılabilir bileşenlerini yapılandırma
description: Bu konu, Project Operations'daki sözleşme satırlarına ücretlendirilebilir bileşenlerin nasıl eklenebilir olduğu hakkında bilgi sağlar.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4d665a6351d2315d185e64e4eb6b0b8859f7bbc4
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086231"
---
# <a name="configuring-chargeable-components-of-a-project-based-contract-line"></a>Proje tabanlı sözleşme satırının borçlandırılabilir bileşenlerini yapılandırma

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

Borçlandırılabilirlik, bir proje sözleşme satırı için görevlerde tanımlanır ve o satıra dahil edilen tüm hareket sınıflarına uygulanır. Proje satırındaki **Görevleri dahil et** alanı * *tüm proje* * olarak ayarlandıysa veya boş bırakılırsa, **ücrete tabi görevler** sekmesi kullanılamaz.

Borçlandırılabilirlik, bir teklif satırı için rollerde tanımlanır ve yalnızca **Zaman** işlem sınıfına uygulanır. Sözleşme satırına **Zamanı dahil et** alanı proje teklif satırında **Hayır** olarak ayarlanırsa **ücrete tabi roller** sekmesi kullanılamaz.

Borçlandırılabilirlik, bir proje sözleşme satırı için işlem kategorilerinde tanımlanır ve yalnızca **Gider** işlem sınıfına uygulanır. Sözleşme satırına **Giderleri dahil et** alanı proje teklif satırında **Hayır** olarak ayarlanırsa **ücrete tabi kategoriler** sekmesi kullanılamaz.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Proje görevini borçlandırılabilir veya borçlandırılamayan olarak güncelleştirme

Proje görevi, aşağıdaki kurulumu olası yapan belirli bir sözleşme satırı bağlamında Masraflandırılabilir veya borçlandırılamayan olabilir:

Proje tabanlı bir sözleşme satırı **Zaman** ve belirli bir görev içeriyorsa, **T1** bununla ücretli olarak ilişkilendirilir. **Giderleri** içeren ikinci bir sözleşme satırı varsa , sözleşme satırındaki T1 görevini borçlandırılamayan olarak ilişkilendirebilirsiniz. Sonuçta, görevde kaydedilen tüm zaman borçlandırılabilir ve tüm giderler Borçlandırılamaz.

Görevin faturalama türü, sözleşme satırı görevleri alt kılavuzundaki **faturalama türü** alanını güncelleştirerek sözleşme satırının **ücrete tabi Görevler** sekmesinde yapılandırılabilir. Alternatif olarak, görevle ilişkili sözleşme satırlarını gösteren **faturalama türü** alanında bulunan proje göreviyle ilgili faturalama türünü güncelleştirebilirsiniz.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Rolü borçlandırılabilir veya borçlandırılamayan olarak güncelleştirme

Bir rol, belirli bir sözleşme satırındaki Borçlandırılabilir veya borçlandırılamayan olabilir.

Bir rolün fatura türü, sözleşme satırının **Ücretlendirilebilir Roller** sekmesinde yapılandırılabilir. Bunu yapmak için, **Ücretli Roller** alt ızgarasındaki **Fatura Türü** alanını güncelleştirin.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Bir işlem kategorinin ücretlendirilebilir veya ücretlendirilemez olarak güncelleştirin

Bir hareket kategorisi, belirli bir sözleşme satırındaki Borçlandırılabilir veya borçlandırılamayan olabilir.

Bir işlemin fatura türü, proje tabanlı sözleşme satırının **Ücretlendirilebilir Kategoriler** sekmesinde yapılandırılabilir. Bunu yapmak için, **Ücretli Kategoriler** alt ızgarasındaki **Fatura Türü** alanını güncelleştirin.

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
