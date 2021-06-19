---
title: Proje tabanlı teklif satırının borçlandırılabilir bileşenlerini yapılandırma
description: Bu konu, proje tabanlı teklif satırlarında eklenen, borçlandırılabilir ve borçlandırılamaz bileşenler hakkında bilgi sağlar.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a9febf305e3cd29bab42cd6c83a941f7b494fa56
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013600"
---
# <a name="configure-the-chargeable-components-of-a-project-based-quote-line"></a>Proje tabanlı teklif satırının borçlandırılabilir bileşenlerini yapılandırma

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Proje tabanlı bir teklif satırında eklenen bileşenler ve borçlandırılabilir bileşenler bulunabilir.

Eklenen bileşenler, proje tabanlı teklif satırında tanımlanan faturalama yöntemi, müşteri bölmeleri, aşılamaz limitler ve fatura sıklığı ayarlarına tabidir.
Eklenen bileşenlerin bir alt kümesi, **Fatura Türü**'nü kullanarak borçlandırılabilir olarak işaretlenebilir. Teklif satırı bağlamında **Fatura Türü** alanında aşağıdaki seçeneklerden birini belirleyebilirsiniz:

   - Borçlandırılabilir
   - Borçlandırılamaz

Borçlandırılabilir bileşenler, rollerde ve işlem kategorilerinde tanımlanabilir.

Proje teklif satırı için rollerde tanımlanan borçlandırılabilirlik yalnızca **Zaman** işlem sınıfına uygulanır. Proje teklif satırında **Zaman Ekle** = **Hayır** varsa **Borçlandırılabilir Roller** sekmesi kullanılamaz.

Proje teklif satırı için işlem kategorilerinde tanımlanan borçlandırılabilirlik yalnızca **Gider** işlem sınıfına uygulanır. Proje teklif satırında **Gider Ekle** = **Hayır** varsa **Borçlandırılabilir Kategoriler** sekmesi kullanılamaz.

## <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Rolü borçlandırılabilir veya borçlandırılamayan olarak güncelleştirme
Rol, proje tabanlı bir teklif satırında borçlandırılabilir veya borçlandırılamaz olabilir. Roldeki fatura türü, proje tabanlı teklif satırının **Borçlandırılabilir Roller** sekmesinde yapılandırılabilir. Bunu yapmak için **Borçlandırılabilir roller** alt ızgarasındaki **Fatura Türü** alanını güncelleştirin. 

## <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Bir işlem kategorinin ücretlendirilebilir veya ücretlendirilemez olarak güncelleştirin
İşlem kategorisi, proje tabanlı bir teklif satırında borçlandırılabilir veya borçlandırılamaz olabilir. İşlemdeki fatura türü, proje tabanlı teklif satırının **Borçlandırılabilir Kategoriler** sekmesinde yapılandırılabilir. Bunu yapmak için, **Borçlandırılabilir Kategoriler** alt kılavuzundaki **faturalama türü** alanını güncelleştirin. 

## <a name="resolve-chargeability"></a>Şarj edilebilirliği çözme

Zaman için oluşturulan bir tahmin veya gerçek tutar yalnızca zamanın teklif satırına eklenmesi ve rolün borçlandırılabilir olarak yapılandırılması durumunda borçlandırılabilir kabul edilir.
Gider için oluşturulan bir tahmin veya gerçek tutar yalnızca giderin teklif satırına eklenmesi ve teklif satırında işlem kategorisinin borçlandırılabilir olarak yapılandırılması durumunda borçlandırılabilir kabul edilir. Aşağıdaki tabloda, borçlandırılabilirliğin her gerçek tutarda nasıl varsayılan olduğu gösterilir. Varsayılanlar, eklenen bileşenleri ve teklif satırında ayarlanan fatura türünü temel alır.

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