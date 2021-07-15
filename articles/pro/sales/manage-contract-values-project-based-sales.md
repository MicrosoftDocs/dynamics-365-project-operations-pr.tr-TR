---
title: Proje tabanlı sözleşme satırlarına genel bakış
description: Bu konu proje tabanlı sözleşme satırlarıyla çalışma hakkında bilgi sağlar.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 22e8ff927c5ff6c3748a35031e7703e3fcfe0dab
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369940"
---
# <a name="project-based-contract-lines-overview"></a>Proje tabanlı sözleşme satırlarına genel bakış

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Dynamics 365 Project Operations'taki proje tabanlı sözleşme satırları, bir etkileşimde proje çalışmasının belirli bileşenleri için tahmin ve fatura anlaşmalarını tutacak şekilde tasarlanmıştır. Proje tabanlı bir sözleşme satırının yapısı, aşağıdaki kavramlarla proje tahminleri ve fatura senaryoları için genişletilir:

- Faturalama yöntemi
- Proje ve Görev Eşleme
- Dahil Edilen İşlem sınıfları
- Aşılamaz limit
- Borçlandırılabilirlik ayarı
- Sözleşme satırı ayrıntılarını kullanarak tahminler
- Sözleşme Satırı Müşterisi

Aşağıdaki tabloda , ayrıntılı, bir kara-yukarı tahmin ve proje tabanlı çalışma için faturalama düzenlemeleri için temel ayarlanmasına yardımcı olan proje tabanlı sözleşme satırlarının **genel** sekmesindeki alanlar yer almaktadır.

| Alan | Veri Akışı Açıklaması | Aşağı yönlü etki |
| --- | --- | --- |
| **Ad** | Sözleşme satırının adı. Bu, tahmini olan sözleşmenin kesikli bileşenini tanımlar. Tekliften oluşturulan bir proje sözleşmesi için bu değer, proje tabanlı teklif satırının karşılık gelen değerinden kopyalanır. | Kopyalanan ad, Fatura oluşturulduğunda bu sözleşme satırından oluşturulan proje fatura satırına kopyalanır. |
| **Faturalama Yöntemi** | Tekliften oluşturulan bir proje sözleşmesi için bu değer, teklif satırında karşılık gelen alandan kopyalanır. Bu, proje işlemleri tarafından desteklenen iki ana sözleşme modelini gösteren bir seçenek kümesi:</br>- **Sabit Fiyat**</br>- **Zaman ve Malzeme** | Başvurulan sözleşme satırının faturalama yöntemine dayalı olarak gerçek hareket işlenir. Gerçek tarafından başvurulan sözleşme satırı bir zaman ve malzeme faturalama yöntemi içeriyorsa, bir maliyet ve faturalanalınmamış satış fiili kaydı oluşturulur. Gerçek tarafından başvurulan sözleşme satırı sabit fiyatlı bir faturalama yöntemi içeriyorsa, yalnızca bir fiili maliyet oluşturulmuştur. |
| **Project** | Bu görevlendirmede iş teslim etmek için kullanılacak projeyi tanımlamak için bu alanı kullanın. | Bu değer, gerçek veya tahmin satır kaydındaki sözleşme satırı referansını çözmek için **Dahil Edilen Görevler** ve **Dahil Edilen İşlem Sınıfları** ile birlikte kullanılır. |
| **Dahil Edilen Görevler** | Bu sözleşme satırının Seçili projeyle ilgili tüm proje görevlerini mi yoksa yalnızca görevlerin bir alt kümesi mi içerdiğini gösterir. Bu, aşağıdaki olası değerlere sahip bir seçenek kümesidir:</br>- **Tüm Proje Görevleri**</br>- **Yalnızca seçili proje görevleri**. Bu alandaki boş bir değer, **Tüm proje görevlerini** seçmek için eşittir. | **Yalnızca seçili görevler** seçiliyse, belirli görevleri seçebilir ve **Proje** sayfasındaki **Görev faturalama ayarı** sekmesinde Bu sözleşme satırıyla ilişkilendirebilirsiniz. Değer, **Proje** ve **dahil edilen işlem** sınıfları ile bağlantılı olarak, gerçek veya tahmin satırı kaydında sözleşme satırı başvurusunu düzeltmek için kullanılır. |
| **Zaman Ekle** | **Evet**/**Hayır** değeri, seçili projedeki zaman hareketlerinin veya işçilik maliyetlerinin bu sözleşme satırına dahil edilip edilmeyeceğini gösterir. **Hiçbir** değer, zaman hareketlerinin veya işçilik maliyetinin Bu sözleşme satırına dahil edilmeyeceğini gösterir. Bir **Evet** değeri bunların olacağını belirtir. | Bu değer, gerçek veya tahmin satırı kaydında sözleşme satırı başvurusunu düzeltmek için projeyle birlikte kullanılır. |
| **Gider Ekle** | **Evet**/**Hayır** değeri, seçili projedeki gider maliyetlerinin bu sözleşme satırına dahil edilip edilmeyeceğini gösterir. **Hiçbir** değer, gider maliyetlerinin Bu sözleşme satırına dahil edilmeyeceğini gösterir. Bir **Evet** değeri bunların olacağını belirtir. | Bu değer, gerçek veya tahmin satırı kaydında sözleşme satırı başvurusunu düzeltmek için projeyle birlikte kullanılır. |
| **Malzemeleri Dahil Et** | **Evet**/**Hayır** değeri, seçili projedeki malzeme maliyetlerinin bu sözleşme satırına dahil edilip edilmeyeceğini gösterir. **Hayır** değeri, malzeme maliyetlerinin bu sözleşme satırına dahil edilmeyeceğini gösterir. Bir **Evet** değeri bunların olacağını belirtir. | Bu değer, gerçek veya tahmin satırı kaydında sözleşme satırı başvurusunu düzeltmek için projeyle birlikte kullanılır. |
| **Ücret Ekle** | **Evet**/**Hayır** değeri, seçili projedeki ücretlerin bu sözleşme satırına dahil edilip edilmeyeceğini gösterir. **Hiçbir** değer, ücretlerin Bu sözleşme satırına dahil edilmeyeceğini gösterir. Bir **Evet** değeri bunların olacağını belirtir. | Bu değer, gerçek veya tahmin satırı kaydında sözleşme satırı başvurusunu düzeltmek için projeyle birlikte kullanılır. |
| **Sözleşme Tutarı** | Sabit fiyatlı sözleşme satırında bu tutar, bu sözleşme satırıyla ilişkilendirilmiş tüm iş bileşenleri için müşteriye Faturalanacak, üzerinde anlaşılan değer olarak kullanılır. Zaman ve materyal sözleşme satırında bu tutar, bu sözleşme satırıyla ilişkilendirilmiş tüm iş bileşenleri için müşteriye Faturalanacak, üzerinde anlaşılan değer olarak kullanılır. Tekliften oluşturulan bir proje sözleşmesi için bu değer, teklif satırında karşılık gelen alandan kopyalanır. Proje tabanlı bir sözleşme satırının satır ayrıntıları varsa, bu alan düzenleme için kilitlenir ve sözleşme satırı ayrıntılarındaki tutardan özetlenir. | Sözleşme satırının satır ayrıntıları varsa, bu değer satır ayrıntılarındaki tutarlar değiştirilerek değiştirilebilir. Sabit fiyat sözleşmesi satırındaki bu değer, dönemsel faturalama kilometre taşları üzerindeki vergi öncesindeki tutarı oluşturmak için kullanılır. |
| **Tahmini Vergi** | Kullanıcı, sözleşme satırındaki tahmini vergi tutarını girmek için bu alanı düzenleyebilir. Proje tabanlı bir sözleşme satırının satır ayrıntıları varsa, bu alan düzenleme için kilitlenir ve sözleşme satırı ayrıntılarındaki vergi tutarından özetlenir. | Sözleşme satırının satır ayrıntıları varsa, bu değer satır ayrıntılarındaki vergi tutarları değiştirilerek değiştirilebilir. Sabit fiyat sözleşmesi satırındaki bu değer, dönemsel faturalama kilometre taşları üzerindeki vergi oluşturmak için kullanılır. |
| **Vergi Sonrası Sözleşme Tutarı** | Vergi Sonrası Sözleşme Tutarı. Bu alan salt okunurdur ve **Sözleşme Gören Tutar + Vergi** olarak hesaplanır. | Sabit fiyat sözleşmesi satırındaki bu değer, dönemsel faturalama kilometre taşları oluşturmak için kullanılır. |
| **Aşılamaz limit** | Kullanıcı bu alanı düzenleyebilir ve yalnızca zaman ve malzeme faturalama yöntemi bulunan proje tabanlı sözleşme satırlarında kullanılabilir. | Kullanıcı bu alanı düzenleyebilir. Gerçek bir zaman veya gider, bu sözleşme satırına saat ve malzeme için başvurduğunda, fiili üzerindeki tutar bu sözleşme satırındaki en fazla aşan sınıra göre değerlendirilir. Bu değerlendirme, zaten harcanan ve taahhüt edilen tutarların muhasebesi yapıldıktan sonra tamamlanır. |
| **Müşteri Bütçesi** | Bu alan düzenlenebilirdir ve sözleşme tekliften oluşturulduysa teklif satırında karşılık gelen alandan kopyalanır. | Bu alan yalnızca bilgi için kullanılır ve herhangi bir aşağı akış önemi içermez. |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Proje tabanlı sözleşme satırları Genel sekmesindeki seçeneklerin doğrulama kuralı

Kural 1: **Dahil edilen görevler** alanı boşsa veya **Tüm proje görevleri** olarak ayarlanmışsa proje tüm görevleri sözleşme satırına dahil edilir.

Kural 2: **dahil edilen görevler** alanı boş veya **Tüm Proje görevlerine** açık olarak ayarlandığında proje ve belirli bir hareket sınıfı yalnızca bir sözleşmenin yalnızca bir proje tabanlı sözleşme satırına dahil edilebilir.

Kural 3: **Dahil edilen görevler** alanı boş veya **Yalnızca seçili Proje görevlerine** açık olarak ayarlandığında proje ve belirli bir hareket sınıfı yalnızca bir sözleşmenin birdne çok proje tabanlı sözleşme satırına dahil edilebilir.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p>
                    <strong>Sözleşme</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Sözleşme Satırı</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="67" valign="top">
                <p>
                    <strong>Dahil edilen görevler</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Zaman Ekle</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Gider Ekle</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Malzemeleri Dahil Et</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Ekle</strong>
                </p>
                <p>
                    <strong>Ücret</strong>
                </p>
            </td>
            <td width="53" valign="top">
                <p>
                    <strong>Geçerli/Geçerli değil</strong>
                </p>
            </td>
            <td width="250" valign="top">
                <p>
                    <strong>Neden</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Boş </p>
            </td>
            <td width="48" valign="top">
                <p>
Evet </p>
            </td>
            <td width="48" valign="top">
                <p>
Evet </p>
            </td>
            <td width="42" valign="top">
                <p>
Evet </p>
            </td>
            <td width="42" valign="top">
                <p>
Evet </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Geçerli değil </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Kural 2'nin ihlali. P1 projesindeki Zaman, Gider, Malzeme ve Ücretler hem CL1 hem de CL2 Sözleşme satırlarına dahil edilir.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Boş </p>
            </td>
            <td width="48" valign="top">
                <p>
Evet </p>
            </td>
            <td width="48" valign="top">
                <p>
Evet </p>
            </td>
            <td width="42" valign="top">
                <p>
Evet </p>
            </td>
            <td width="42" valign="top">
                <p>
Evet </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Boş </p>
            </td>
            <td width="48" valign="top">
                <p>
Evet </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Evet </p>
            </td>
            <td width="42" valign="top">
                <p>
Evet </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Geçerli değil </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Kural 2'nin ihlali. P1 projesindeki Zaman, Malzemeler, ve Ücretler hem CL1 hem de CL2 Sözleşme satırlarına dahil edilir.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Boş </p>
            </td>
            <td width="48" valign="top">
                <p>
Evet </p>
            </td>
            <td width="48" valign="top">
                <p>
Evet </p>
            </td>
            <td width="42" valign="top">
                <p>
Evet </p>
            </td>
            <td width="42" valign="top">
                <p>
Evet </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Boş </p>
            </td>
            <td width="48" valign="top">
                <p>
Evet </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Evet </p>
            </td>
            <td width="42" valign="top">
                <p>
Evet </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Geçerli </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
P1 projesindeki Zaman, Malzemeler ve Ücretler CL1'e dahil edilir.
                </p>
                <ul>
                    <li>
P1 projesindeki giderler CL2'ye dahildir.
                    </li>
                </ul>
                <p>
Her bir sözleşme satırına dahil edilenler arasında çakışma yok ve bu nedenle geçerli.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Boş </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="48" valign="top">
                <p>
Evet </p>
            </td>
            <td width="42" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Yalnızca seçili görevler </p>
            </td>
            <td width="48" valign="top">
                <p>
Evet </p>
            </td>
            <td width="48" valign="top">
                <p>
Evet </p>
            </td>
            <td width="42" valign="top">
                <p>
Evet </p>
            </td>
            <td width="42" valign="top">
                <p>
Evet </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Geçerli değil </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Kural 2'nin ihlali </p>
                <p>
C1'e, proje P1 üzerindeki bir görev alt kümesinde Zaman, Malzemeler, Giderler ve Ücretler dahildir.
                </p>
                <p>
CL2'ye tüm proje P1 için Zaman, Malzemeler, Giderler ve Ücretler dahildir ve bu nedenle C1'e dahil edilenlerle çakışır.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Boş </p>
            </td>
            <td width="48" valign="top">
                <p>
Evet </p>
            </td>
            <td width="48" valign="top">
                <p>
Evet </p>
            </td>
            <td width="42" valign="top">
                <p>
Evet </p>
            </td>
            <td width="42" valign="top">
                <p>
Evet </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Yalnızca seçili görevler </p>
            </td>
            <td width="48" valign="top">
                <p>
Evet </p>
            </td>
            <td width="48" valign="top">
                <p>
Evet </p>
            </td>
            <td width="42" valign="top">
                <p>
Evet </p>
            </td>
            <td width="42" valign="top">
                <p>
Evet </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Geçerli </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Kural başına #3 </p>
                <p>
C1'e, proje P1 üzerindeki bir görev alt kümesinde Zaman, Giderler ve Ücretler dahildir.
                </p>
                <p>
CL2'e, proje P1 üzerindeki bir görev alt kümesi için Zaman, Giderler ve Ücretler dahildir.
                </p>
                <p>
Yalnızca tek bir ek doğrulama yapılır. Bu doğrulamanın amacı, çakışmaları önlemek için CL1 üzerindeki alt görevlerin CL2 üzerindeki alt görevlerden farklı olmasını kontrol etmektir. Bu, görevler ilişkilendirildiğinde sistem tarafından yapılır.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Yalnızca seçili görevler </p>
            </td>
            <td width="48" valign="top">
                <p>
Evet </p>
            </td>
            <td width="48" valign="top">
                <p>
Evet </p>
            </td>
            <td width="42" valign="top">
                <p>
Evet </p>
            </td>
            <td width="42" valign="top">
                <p>
Evet </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
