---
title: Teklif satırının borçlandırılabilir bileşenlerini yapılandırma - lite
description: Bu konu, proje tabanlı bir teklif satırında borçlandırılabilir ve borçlandırılamayan bileşenler ayarlanması hakkında bilgiler sağlar.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0e293587adf15d0523bef6b7e688fdc883aba0fa
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273897"
---
# <a name="configure-the-chargeable-components-of-a-quote-line---lite"></a>Teklif satırının borçlandırılabilir bileşenlerini yapılandırma - lite

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Proje tabanlı bir teklif satırı *dahil edilen* bileşenler ve *Borçlandırılabilir* bileşenler kavramıdır.

Eklenen bileşenler şunlara tabidir:

  - Faturalama yöntemi ve müşteri bölmeleri
  - Aşılamaz sınırlar 
  - Proje tabanlı teklif satırında tanımlanan fatura sıklığı ayarları

Dahil edilen bileşenlerin bir alt kümesi, **Fatura Türü** alanı kullanılarak ücretlendirilebilir olarak işaretlenebilir. **Faturalama Türü** alanı, teklif satırı bağlamında aşağıdaki değerlere izin veren bir seçenek kümesidir:

  - Borçlandırılabilir
  - Borçlandırılamaz

Ücretlendirilebilir bileşenler görevlerde, rollerde ve işlem kategorilerinde tanımlanabilir.

Borçlandırılabilirlik, bir teklif satırı için görevlerde tanımlanır ve o satıra dahil edilen tüm hareket sınıflarına uygulanır. **Görevleri dahil et** alanı **tüm proje** olarak ayarlandıysa veya boş bırakılırsa, **ücrete tabi görevler** sekmesi kullanılamaz.

Borçlandırılabilirlik, bir teklif satırı için rollerde tanımlanır ve yalnızca **Zaman** işlem sınıfına uygulanır. **Zamanı dahil et** alanı proje teklif satırında **Hayır** olarak ayarlanırsa **ücrete tabi roller** sekmesi kullanılamaz.

Borçlandırılabilirlik, bir teklif satırı için işlem kategorilerinde tanımlanır ve yalnızca **Gider** işlem sınıfına uygulanır. **Giderleri dahil et** alanı proje teklif satırında **Hayır** olarak ayarlanırsa **Ücrete tabi kategoriler** sekmesi kullanılamaz.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Proje görevini borçlandırılabilir veya borçlandırılamayan olarak güncelleştirme

Proje görevi, aşağıdaki kurulumu olası yapan belirli bir proje tabanlı teklif satırı bağlamında Masraflandırılabilir veya borçlandırılamayan olabilir:

Proje tabanlı teklif satırı **Saat** ve **T1** görev içeriyorsa bu görev teklif satırıyla Masraflandırılabilir olarak ilişkilendirilir. **Giderleri** içeren ikinci bir teklif satırı varsa , teklif satırındaki **T1** görevini borçlandırılamayan olarak ilişkilendirebilirsiniz. Sonuçta, görevde kaydedilen tüm zaman borçlandırılabilir ve görevde kaydedilen tüm giderler Borçlandırılamaz.

Görevin faturalama türü, **Teklif satırı görevleri** alt kılavuzundaki **faturalama türü** alanını güncelleştirerek, sözleşme satırındaki **ücrete tabi Görevler** sekmesinde yapılandırılabilir. Alternatif olarak, görevle ilişkili teklif satırlarını gösteren bir projenin görev faturalama kurulumunun alt kılavuzundaki **fatura türü** alanındaki proje görevi için fatura türünü güncelleştirebilirsiniz.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Rolü borçlandırılabilir veya borçlandırılamayan olarak güncelleştirme

Rol, belirli bir proje tabanlı teklif satırı bağlamında Masraflandırılabilir veya borçlandırılamayan olabilir.

Rolün faturalama türü, **Ücretlendirilir Roller** alt kılavuzundaki **faturalama türü** alanını güncelleştirerek, sözleşme satırındaki **ücrete tabi roller** sekmesinde yapılandırılabilir.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Bir işlem kategorinin ücretlendirilebilir veya ücretlendirilemez olarak güncelleştirin

Bir hareket kategorisi, belirli bir teklif satırındaki Borçlandırılabilir veya borçlandırılamayan olabilir.

İşlemin faturalama türü, **Ücretlendirilir Kategoriler** alt kılavuzundaki **Faturalama Türü** alanını güncelleştirerek, sözleşme satırındaki **Ücrete Tabi Kategoriler** sekmesinde yapılandırılabilir.

### <a name="resolve-chargeability"></a>Şarj edilebilirliği çözme
Bir tahmin veya zaman için oluşturulan fiili, yalnızca teklif satırına **saat** dahil edildiğinde Borçlandırılabilir olarak değerlendirilir ve **görev** ve **rol** teklif satırında Borçlandırılabilir olarak yapılandırılır.

Bir tahmin veya gider için oluşturulan fiili, yalnızca teklif satırına **Gider** dahil edildiğinde Borçlandırılabilir olarak değerlendirilir ve **görev** ve **İşlem kategorisi** teklif satırında Borçlandırılabilir olarak yapılandırılır.

| Zaman dahil eder | Gider içerir | Dahil Edilen Görevler | Rol | Kategori | Görev | Faturalama |
| --- | --- | --- | --- | --- | --- | --- |
| Evet | Evet | Tüm Proje | Borçlandırılabilir | Borçlandırılabilir | Ayarlanamıyor | Bir Zaman fiili faturalama: Ücretli </br>Geçerli gider faturalama türü: Borçlandırılabilir |
| Evet | Evet | Yalnızca seçili görevler | Borçlandırılabilir | Borçlandırılabilir | Borçlandırılabilir | Bir Zaman fiili faturalama: Ücretli</br>Geçerli gider faturalama türü: Borçlandırılabilir |
| Evet | Evet | Yalnızca seçili görevler | Borçlandırılamaz | Borçlandırılabilir | Borçlandırılabilir | Bir Zaman fiili faturalama: Ücretlendirilemez</br>Geçerli gider faturalama türü: Borçlandırılabilir |
| Evet | Evet | Yalnızca seçili görevler | Borçlandırılabilir | Borçlandırılabilir | Borçlandırılamaz | Bir Zaman fiili faturalama: Ücretlendirilemez</br> Geçerli gider faturalama türü: Borçlandırılamaz |
| Evet | Evet | Yalnızca seçili görevler | Borçlandırılamaz | Borçlandırılabilir | Borçlandırılamaz | Bir Zaman fiili faturalama: Ücretlendirilemez</br> Geçerli gider faturalama türü: Borçlandırılamaz |
| Evet | Evet | Yalnızca seçili görevler | Borçlandırılamaz | Borçlandırılamaz | Borçlandırılabilir | Bir Zaman fiili faturalama: Ücretlendirilemez</br> Geçerli gider faturalama türü: Borçlandırılamaz |
| No | Evet | Tüm Proje | Ayarlanamıyor | Borçlandırılabilir | Ayarlanamıyor | Bir Zaman fiili faturalama: Kullanılamaz </br>Geçerli gider faturalama türü: Borçlandırılabilir |
| No | Evet | Tüm Proje | Ayarlanamıyor | Borçlandırılamaz | Ayarlanamıyor | Bir Zaman fiili faturalama: Kullanılamaz </br>Geçerli gider faturalama türü: Borçlandırılamaz |
| Evet | No | Tüm Proje | Borçlandırılabilir | Ayarlanamıyor | Ayarlanamıyor | Bir Zaman fiili faturalama: Ücretli</br>Geçerli gider faturalama türü: Kullanılamaz |
| Evet | No | Tüm Proje | Borçlandırılamaz | Ayarlanamıyor | Ayarlanamıyor | Bir Zaman fiili faturalama: Ücretlendirilemez </br>Geçerli gider faturalama türü: Kullanılamaz |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]