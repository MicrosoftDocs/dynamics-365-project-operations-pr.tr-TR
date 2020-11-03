---
title: Teklif satırının borçlandırılabilir bileşenlerini yapılandırma
description: Bu konu, proje tabanlı bir teklif satırında borçlandırılabilir ve borçlandırılamayan bileşenler ayarlanması hakkında bilgiler sağlar.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e0b64d7edb21df127bf7544f044de7f3c496dfe3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086445"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a>Teklif satırının borçlandırılabilir bileşenlerini yapılandırma

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

Görevin faturalama türü, **teklif satırı görevleri** alt kılavuzundaki **faturalama türü** alanını güncelleştirerek proje tabanlı teklif satırının **ücrete tabi Görevler** sekmesinde yapılandırılabilir. Alternatif olarak, görevle ilişkili teklif satırlarını gösteren bir projenin görev faturalama kurulumunda yer alan faturalama türü alanında bulunan proje göreviyle ilgili **faturalama türünü** güncelleştirebilirsiniz.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Rolü borçlandırılabilir veya borçlandırılamayan olarak güncelleştirme

Rol, belirli bir proje tabanlı teklif satırı bağlamında Masraflandırılabilir veya borçlandırılamayan olabilir.

Rolün faturalama türü, **ücrete tabi roller** alt kılavuzundaki **faturalama türü** alanını güncelleştirerek proje tabanlı teklif satırının **ücrete tabi roller** sekmesinde yapılandırılabilir.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Bir işlem kategorinin ücretlendirilebilir veya ücretlendirilemez olarak güncelleştirin

Bir hareket kategorisi, belirli bir teklif satırındaki Borçlandırılabilir veya borçlandırılamayan olabilir.

İşlemin faturalama türü, **ücrete tabi kategoriler** alt kılavuzundaki **faturalama türü** alanını güncelleştirerek proje tabanlı teklif satırının **ücrete tabi kategoriler** sekmesinde yapılandırılabilir.

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
