---
title: Proje tabanlı sözleşme satırının borçlandırılabilir bileşenlerini yapılandırma
description: Bu konu, sözleşme satırında borçlandırılabilir ve borçlandırılamayan bileşenler ayarlanması hakkında bilgiler sağlar.
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2266d8e0fe998e7161ede4cb4eaf7d3c70c54f71
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278720"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>Proje tabanlı sözleşme satırının borçlandırılabilir bileşenlerini yapılandırma

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Proje tabanlı bir sözleşme satırı dahil edilen, Borçlandırılabilir ve borçlandırılamaz bileşenler kavramıdır.

Dahil edilen bileşenler, proje tabanlı sözleşme satırında tanımlanan faturalama yöntemine, müşteri böler, aşılamaz sınırlara ve fatura sıklığı ayarlarına tabidir.

Dahil edilen bileşenlerin bir alt kümesi, **Fatura Türü** alanı kullanılarak ücretlendirilebilir olarak işaretlenebilir.

Ücretlendirilebilir bileşenler rollerde ve işlem kategorilerinde tanımlanabilir.

Borçlandırılabilirlik, bir teklif satırı için rollerde tanımlanır ve yalnızca **Zaman** işlem sınıfına uygulanır. **Zamanı dahil et** alanı proje sözleşme satırında **Hayır** olarak ayarlanırsa **ücrete tabi roller** sekmesi kullanılamaz.

Borçlandırılabilirlik, bir proje sözleşme satırı için işlem kategorilerinde tanımlanır ve yalnızca **Gider** işlem sınıfına uygulanır. **Giderleri dahil et** alanı proje sözleşme satırında **Hayır** olarak ayarlanırsa **ücrete tabi kategoriler** sekmesi kullanılamaz.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Rolü borçlandırılabilir veya borçlandırılamayan olarak güncelleştirme

Bir rol, belirli proje tabanlı sözleşme satırındaki Borçlandırılabilir veya borçlandırılamayan olabilir.

Proje tabanlı sözleşme satırının **Ücretlendirilir Roller** sekmesinin **Ücretlendirilebilir Kategoriler** alt kılavuzundaki **Faturalama Türü** alanında rol için faturalandırma türünü güncelleştirin.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Bir işlem kategorinin ücretlendirilebilir veya ücretlendirilemez olarak güncelleştirin

Bir hareket kategorisi, belirli bir proje tabanlı sözleşme satırındaki Borçlandırılabilir veya borçlandırılamayan olabilir.

Proje tabanlı sözleşme satırının **Ücretlendirilir Kategoriler** sekmesinin **Ücretlendirilebilir Kategoriler** alt kılavuzundaki **Faturalama Türü** alanında işlem için faturalandırma türünü güncelleştirin.

### <a name="resolve-chargeability"></a>Şarj edilebilirliği çözme

Bir tahmin veya zaman için oluşturulan fiili, yalnızca sözleşme satırına saat dahil edildiğinde Borçlandırılabilir olarak değerlendirilir ve rol sözleşme satırında Borçlandırılabilir olarak yapılandırılır.

Bir tahmin veya gider için oluşturulan fiili, yalnızca sözleşme satırına Gider dahil edildiğinde Borçlandırılabilir olarak değerlendirilir ve görev ve İşlem kategorisi sözleşme satırında Borçlandırılabilir olarak yapılandırılır.

| Zaman dahil eder | Gider içerir | Rol | Kategori | Görev |
| --- | --- | --- | --- | --- |
| Evet | Evet | Borçlandırılabilir | Borçlandırılabilir | Bir Zaman fiili faturalama: Ücretli </br>Geçerli gider faturalama türü: Borçlandırılabilir |
| Evet | Evet | Borçlandırılamaz | Borçlandırılabilir | Bir Zaman fiili faturalama: Ücretlendirilemez </br>Geçerli gider faturalama türü: Borçlandırılabilir |
| Evet | Evet | Borçlandırılamaz | Borçlandırılamaz | Bir Zaman fiili faturalama: Ücretlendirilemez </br>Geçerli gider faturalama türü: Borçlandırılamaz |
| No | Evet | Ayarlanamıyor | Borçlandırılabilir | Bir Zaman fiili faturalama: Kullanılamaz </br>Geçerli gider faturalama türü: Borçlandırılabilir |
| No | Evet | Ayarlanamıyor | Borçlandırılamaz | Bir Zaman fiili faturalama: Kullanılamaz </br>Geçerli gider faturalama türü: Borçlandırılamaz |
| Evet | No | Borçlandırılabilir | Ayarlanamıyor | Bir Zaman fiili faturalama: Ücretli </br>Geçerli gider faturalama türü: Kullanılamaz |
| Evet | No | Borçlandırılamaz | Ayarlanamıyor | Bir Zaman fiili faturalama: Ücretlendirilemez </br> Geçerli gider faturalama türü: Kullanılamaz |


[!INCLUDE[footer-include](../includes/footer-banner.md)]