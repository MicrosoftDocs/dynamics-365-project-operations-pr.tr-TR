---
title: Proje tabanlı sözleşme satırlarıyla çalışma
description: Bu konu proje tabanlı sözleşme satırları hakkında bilgi sağlar.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c1c935a998cba8bd42ba2f11c8310d41e72de94adac7c2cb83f4c7224127b10b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6990070"
---
# <a name="work-with-projectbased-contract-lines"></a>Proje tabanlı sözleşme satırlarıyla çalışma

Dynamics 365 Project Operations'taki proje tabanlı sözleşme satırları, bir etkileşimde proje çalışmasının belirli bileşenleri için tahmin ve fatura anlaşmalarını tutacak şekilde tasarlanmıştır. Proje tabanlı bir sözleşme satırının yapısı, aşağıdaki kavramlarla proje tahminleri ve fatura senaryoları için genişletilir:

- Faturalama yöntemi
- Proje ve Görev Eşleme
- Dahil Edilen İşlem sınıfları
- Aşılamaz limit
- Borçlandırılabilirlik ayarı
- Sözleşme satırı ayrıntılarını kullanarak tahminler
- Sözleşme Satırı Müşterisi

Aşağıdaki alanlar Proje tabanlı sözleşme satırlarının **Genel** sekmesinde yer alır. Bu alanlar, ayrıntılı, yukarı tahmin ve proje tabanlı çalışma için faturalama düzenlemeleri için temel ayarlamanıza yardımcı olur.

| Alan | Veri Akışı Açıklaması | Aşağı yönlü etki |
| --- | --- | --- |
| **Ad** | Tahmini olan sözleşmenin kesikli bileşenini tanımlayan sözleşme satırının adı. Tekliften oluşturulan bir proje sözleşmesi için bu değer, proje tabanlı teklif satırının karşılık gelen değerinden kopyalanır. | Bu alan değeri, Fatura oluşturulduğunda bu sözleşme satırından oluşturulan proje fatura satırına kopyalanır. |
| **Faturalama Yöntemi** | Tekliften oluşturulan bir proje sözleşmesi için bu değer, teklif satırında karşılık gelen alandan kopyalanır. Bu, proje işlemleri tarafından desteklenen iki ana sözleşme modelini gösteren bir seçenek kümesi:</br>- **Sabit Fiyat**</br>- **Zaman ve Malzeme** | Başvurulan sözleşme satırının faturalama yöntemine dayalı olarak gerçek hareket işlenir. Gerçek tarafından başvurulan sözleşme satırı bir zaman ve malzeme faturalama yöntemi içeriyorsa, bir maliyet ve faturalanalınmamış satış fiili kaydı oluşturulur. Gerçek tarafından başvurulan sözleşme satırı sabit fiyatlı bir faturalama yöntemi içeriyorsa, yalnızca bir fiili maliyet oluşturulmuştur. |
| **Project** | Bu görevlendirmede iş teslim etmek için kullanılacak projeyi tanımlamak için bu alanı kullanın. | Bu alandaki değer, **eklenen görevler** ve **dahil edilen hareket sınıfları** alanlarıyla bağlantılı olarak, gerçek veya tahmin satırı kaydında sözleşme satırı başvurusunu düzeltmek için kullanılır. |
| **Zaman Ekle** | Bir bayrak Seçili projedeki zaman hareketlerinin veya işçilik maliyetlerinin Bu sözleşme satırına dahil edilip edilmeyeceğini gösterir. **Hiçbir** değer, zaman hareketlerinin veya işçilik maliyetlerinin Bu sözleşme satırına dahil edilmeyeceğini gösterir. Bir **Evet** değeri bunların olacağını belirtir. | Bu alan değeri, fiili veya tahmin satırı kaydında sözleşme satırı başvurusunu düzeltmek için Proje ile birlikte kullanılır. |
| **Gider Ekle** | Bir bayrak Seçili projedeki gider maliyetlerinin Bu sözleşme satırına dahil edilip edilmeyeceğini gösterir. **Hiçbir** değer, gider maliyetlerinin Bu sözleşme satırına dahil edilmeyeceğini gösterir. Bir **Evet** değeri bunların olacağını belirtir. | Bu alan değeri, fiili veya tahmin satırı kaydında sözleşme satırı başvurusunu düzeltmek için Proje ile birlikte kullanılır. |
| **Ücret Ekle** | Bir bayrak Seçili projedeki ücretlerin Bu sözleşme satırına dahil edilip edilmeyeceğini gösterir. **Hiçbir** değer, ücretlerin Bu sözleşme satırına dahil edilmeyeceğini gösterir. Bir **Evet** değeri bunların olacağını belirtir. | Bu alan değeri, fiili veya tahmin satırı kaydında sözleşme satırı başvurusunu düzeltmek için Proje ile birlikte kullanılır. |
| **Sözleşme Tutarı** | Sabit fiyatlı sözleşme satırında bu, bu sözleşme satırıyla ilişkilendirilmiş tüm iş bileşenleri için müşteriye Faturalanacak, üzerinde anlaşılan değer olarak kullanılır. Zaman ve materyal sözleşme satırında bu tutar, bu sözleşme satırıyla ilişkilendirilmiş tüm iş bileşenleri için müşteriye Faturalanacak, üzerinde anlaşılan değer olarak kullanılır. Tekliften oluşturulan bir proje sözleşmesi için bu değer, teklif satırında karşılık gelen alandan kopyalanır. Proje tabanlı bir sözleşme satırının satır ayrıntıları varsa, bu alan düzenleme için kilitlenir ve sözleşme satırı ayrıntılarındaki tutardan özetlenir. | Sözleşme satırının satır ayrıntıları varsa, bu değer satır ayrıntılarındaki tutarlar değiştirilerek değiştirilebilir. Sabit fiyat sözleşmesi satırındaki bu değer, dönemsel faturalama kilometre taşları üzerindeki vergi öncesindeki tutarı oluşturmak için kullanılır. |
| **Tahmini Vergi** | Kullanıcı, sözleşme satırındaki tahmini vergi tutarını girmek için bu alanı düzenleyebilir. Proje tabanlı bir sözleşme satırının satır ayrıntıları varsa, bu alan düzenleme için kilitlenir ve sözleşme satırı ayrıntılarındaki vergi tutarından özetlenir. | Sözleşme satırının satır ayrıntıları varsa, bu değer satır ayrıntılarındaki vergi tutarları değiştirilerek değiştirilebilir. Sabit fiyat sözleşmesi satırındaki bu değer, dönemsel faturalama kilometre taşları üzerindeki vergi oluşturmak için kullanılır. |
| **Vergi Sonrası Sözleşme Tutarı** | Vergi Sonrası Sözleşme Tutarı. Bu alan salt okunurdur ve **sözleşme gören tutar + vergi** olarak hesaplanır. | Sabit fiyat sözleşmesi satırındaki bu değer, dönemsel faturalama kilometre taşları oluşturmak için kullanılır. |
| **Aşılamaz limit** | Kullanıcı bu alanı düzenleyebilir ve yalnızca zaman ve malzeme faturalama yöntemi bulunan proje tabanlı sözleşme satırlarında kullanılabilir. | Kullanıcı bu alanı düzenleyebilir. Gerçek bir zaman veya gider, bu sözleşme satırına saat ve malzeme için başvurduğunda, zaten harcanan ve taahhüt edilen tutarlara yönelik hesap oluşturulduktan sonra, fiili üzerindeki tutar bu sözleşme satırındaki en fazla aşan sınıra göre değerlendirilir. |
| **Müşteri Bütçesi** | Bu alan düzenlenebilirdir ve sözleşme tekliften oluşturulduysa teklif satırında karşılık gelen alandan kopyalanır. | Bu alan yalnızca bilgi için kullanılır ve herhangi bir aşağı akış önemi içermez. |

## <a name="validation-rule-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Proje tabanlı sözleşme satırları Genel sekmesindeki seçeneklerin doğrulama kuralı

Kural: bir proje ve belirli bir işlem sınıfı yalnızca bir sözleşmede bulunan proje tabanlı bir sözleşme satırına dahil edilebilir.

| Sözleşme | Sözleşme Satırı | Project | Zaman ekle | Gider ekle | Ücret Ekle | Geçerli/geçerli değil | Nedeni                                                                                                                                                                                                  |
|----------|---------------|---------|--------------|-----------------|-------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| C1       | CL1           | P1      | Evet          | Evet             | Evet         | Geçerli değil       | Kuralı ihlal ediyor. Proje P1 üzerinde zaman, masraf ve ücretler, CL1 ve CL2 sözleşme satırlarına eklenir.                                                                                       |
| C1       | CL2           | P1      | Evet          | Evet             | Evet         | Geçerli değil       | Kuralı ihlal ediyor. Proje P1 üzerinde zaman, masraf ve ücretler, CL1 ve CL2 sözleşme satırlarına eklenir.                                                                                       |
| C1       | CL1           | P1      | Evet          | No              | Evet         | Geçerli değil       | Kuralı ihlal ediyor. Proje P1 üzerinde zaman ve ücretler, CL1 ve CL2 sözleşme satırlarına eklenir.                                                                                                   |
| C1       | CL2           | P1      | Evet          | Evet             | Evet         | Geçerli değil       | Kuralı ihlal ediyor. Proje P1 üzerinde zaman ve ücretler, CL1 ve CL2 sözleşme satırlarına eklenir.                                                                                                   |
| C1       | CL1           | P1      | Evet          | No              | Evet         | Geçerli           | Proje P1 için zaman ve ücretler CL1'e eklenir. P1 projesindeki giderler CL2'ye dahildir. </br>   Her bir sözleşme satırına nelerin dahil edildiği ve bu nedenle geçerli olan bir çakışma yoktur.  |
| C1       | CL2           | P1      | No           | Evet             | No          | Geçerli           | Proje P1 için zaman ve ücretler CL1'e eklenir. P1 projesindeki giderler CL2'ye dahildir. </br>   Her bir sözleşme satırına nelerin dahil edildiği ve bu nedenle geçerli olan bir çakışma yoktur.  |
| C1       | CL1           | P1      | Evet          | Evet             | Evet         | Geçerli değil       | Kuralı ihlal ediyor. Proje P1 üzerinde zaman, masraf ve ücretler, iki sözleşmedeki satırlarına eklenir.                                                                                               |
| CL2      | CL2           | P1      | Evet          | Evet             | Evet         | Geçerli değil       | Kuralı ihlal ediyor. Proje P1 üzerinde zaman, masraf ve ücretler, iki sözleşmedeki satırlarına eklenir.                                                                                               |


[!INCLUDE[footer-include](../includes/footer-banner.md)]