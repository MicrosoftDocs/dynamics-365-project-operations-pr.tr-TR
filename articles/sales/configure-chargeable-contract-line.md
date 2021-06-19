---
title: Proje tabanlı bir sözleşme satırının borçlandırılabilir bileşenleri yapılandırma
description: Bu konu, sözleşme satırında borçlandırılabilir ve borçlandırılamayan bileşenler ayarlanması hakkında bilgiler sağlar.
author: rumant
ms.date: 10/12/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d42dd180dacc45e72eddcac70ae9ede38d4c36c6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013645"
---
# <a name="configure-chargeable-components-of-a-project-contract-line"></a>Proje tabanlı bir sözleşme satırının borçlandırılabilir bileşenleri yapılandırma

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
