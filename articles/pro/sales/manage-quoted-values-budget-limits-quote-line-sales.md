---
title: Proje tabanlı teklif satırlarına genel bakış
description: Bu konuda, proje çalışmaları için proje tabanlı teklif satırlarını kullanma hakkında bilgiler sağlanmaktadır.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: b7076a4b9280472f8c30d0b58c3aa9b9bc86d651
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369895"
---
# <a name="project-based-quote-lines-overview"></a>Proje tabanlı teklif satırlarına genel bakış 

_**Aşağıdakilere İçin Geçerlidir:** Lite dağıtımı - anlaşmadan proforma faturaya, kaynak/stoklanmayan tabanlı senaryolar için Project Operations_

Proje tabanlı teklif satırları, bir etkileşimdeki proje çalışmalarının tahmin edilmesine yardımcı olmak için tasarlanmıştır. Proje tabanlı teklif satırının yapısı, aşağıdaki kavramlarla proje tahminleri için genişletilmiştir:

- Faturalama Yöntemi
- Proje ve Görev Eşleme
- Dahil Edilen İşlem sınıfları
- Aşılamaz Limit
- Borçlandırılabilirlik ayarı
- Teklif Satırı Ayrıntılarını kullanarak tahmin yürütme
- Teklif satırı Müşterileri

Aşağıdaki tabloda proje tabanlı teklif satırının **Genel** sekmesindeki alanlar hakkında bilgi sağlanmaktadır. Bu alanlar, proje çalışmaları için ayrıntılı, baştan sona bir tahmin için temel oluşturulmasına yardımcı olur.

| **Alan** | **Açıklama** | **Aşağı yönlü etki** |
| --- | --- | --- |
| Adı | Tahmin edilen teklifin farklı bileşenini belirlemenize yardımcı olan teklif satırı adı. | Teklif kazanıldığında, bu teklif satırından oluşturulan proje sözleşme satırına kopyalanır. |
| Faturalama Yöntemi | Fırsattan oluşturulan bir teklifte bu değer, fırsat satırındaki ilgili alandan kopyalanır. Bu alan, Dynamics 365 Project Operations tarafından desteklenen iki ana sözleşme modeli içerir:</br>- Sabit fiyat</br>- Zaman ve malzeme.| Bu değer, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşmesi satırına kopyalanır. |
| Project | Bu etkileşimde kullanılacak projeyi belirleyerek çalışmayı teslim etmek için bu isteğe bağlı alanı kullanın. Proje bir teklif satırına eşlendiğinde, borçlandırılabilir görevler oluşturulmasına ve ayrıca proje bazlı bir tahminin teklif satırına teklif satırı ayrıntıları olarak getirilmesine yardımcı olur. Proje, proje bazlı bir teklif satırına eşlenmediğinde tahmin, her bir teklif satırı ayrıntısının el ile oluşturulmasıyla elde edilmelidir. | Bu değer, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşmesi satırına kopyalanır.|
| Dahil Edilen Görevler | Bu teklif satırının seçilen projenin görevlerinin tümünde veya bazılarında kullanılıp kullanılmadığını gösterir. Bu alan aşağıdaki olası değerlere sahiptir:</br>- Tüm proje görevleri</br>- Yalnızca seçili proje görevleri</br>Bu alandaki boş bir değer **Tüm proje görevleri** seçeneğinin eşdeğeridir. | Proje sayfasında **Yalnızca seçili proje görevleri** seçeneği belirlendiğinde **Görev fatura ayarı** sekmesi, bu teklif satırıyla ilişkilendirmek üzere belirli görevleri seçmenize olanak sağlar. Bu değer, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşmesi satırına kopyalanır. |
| Zaman Ekle | **Evet**/**Hayır** değeri, seçili projedeki zaman hareketlerinin veya işçilik maliyetlerinin bu teklif satırı tahminine dahil edilip edilmeyeceğini gösterir. **Hayır** değeri, zaman işlemlerinin veya işçilik maliyetinin bu teklif satırındaki tahmine dahil edilmeyeceğini belirtir. **Evet** değeri, zaman işlemlerinin veya işçilik maliyetinin bu teklif satırındaki tahmine dahil edileceğini belirtir. | Bu değer, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşmesi satırına kopyalanır. |
| Gider Ekle | **Evet**/**Hayır** değeri, seçili projedeki gider maliyetlerinin bu teklif satırı tahminine dahil edilip edilmeyeceğini gösterir. **Hayır** değeri, gider maliyetinin bu teklif satırındaki tahmine dahil edilmeyeceğini belirtir. **Evet** değeri, gider maliyetinin bu teklif satırındaki tahmine dahil edileceğini belirtir. | Bu değer, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşmesi satırına kopyalanır. |
| Malzeme Ekle | **Evet**/**Hayır** değeri, seçili projedeki malzeme maliyetlerinin bu teklif satırı tahminine dahil edilip edilmeyeceğini gösterir. **Hayır** değeri, malzeme maliyetlerinin bu teklif satırı tahminine dahil edilmeyeceğini gösterir. **Evet** değeri, malzeme maliyetlerinin bu teklif satırı tahminine dahil edileceğini gösterir. | Bu değer, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşmesi satırına kopyalanır. |
| Ücret Ekle | **Evet**/**Hayır** değeri, seçili projedeki ücretlerin bu teklif satırı tahminine dahil edilip edilmeyeceğini gösterir. **Hayır** değeri, ücretlerin bu teklif satırındaki tahmine dahil edilmeyeceğini belirtir. **Evet** değeri, ücretlerin bu teklif satırındaki tahmine dahil edileceğini belirtir. | Bu değer, teklif kazanıldığında bu teklif satırından oluşturulan Proje sözleşmesi satırına kopyalanır. |
| Teklif Edilen Tutar | Bu, proje tabanlı teklif satırındaki tüm tahmin edilen çalışma için müşteriye teklif edilecek tutardır. Fırsattan oluşturulan bir teklifte, bu değer fırsat satırındaki **Müşteri Bütçesi** alanından kopyalanır. Proje tabanlı teklif satırı satır ayrıntılarına sahip olduğunda, bu alan düzenlemeye kilitlenir ve teklif satırı ayrıntılarındaki tutardan özetlenir. | Bu değer, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşmesi satırına kopyalanır. |
| Tahmini Vergi | Bu, kullanıcının teklif satırına tahmini vergi tutarını ekleyebileceği düzenlenebilir bir alandır. Proje tabanlı teklif satırı, satır ayrıntılarına sahip olduğunda, bu alan düzenlemeye kilitlenir ve teklif satırı ayrıntılarındaki vergi tutarından özetlenir. | Bu değer, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşmesi satırına kopyalanır. |
| Vergi Sonrası Teklif Tutarı | Bu alan, vergi sonrası teklif satırı tutarıdır ve salt okunurdur. Bu alandaki tutar *Teklif Tutarı + Vergi* olarak hesaplanır. | Bu değer, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşmesi satırına kopyalanır. |
| Aşılamaz Limit | Bu alan, düzenlenebilirdir ve yalnızca **Zaman ve Malzeme** faturalama yöntemine sahip proje bazlı teklif satırlarında kullanılabilir. | Bu değer, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşmesi satırına kopyalanır. |
| Müşteri Bütçesi | Bu alan, düzenlenebilirdir ve teklif bir fırsattan oluşturulmuşsa fırsat satırındaki ilgili alandan kopyalanır. | Bu değer, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşmesi satırına kopyalanır. |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Proje tabanlı teklif satırlarının Genel sekmesindeki alanları için doğrulama kuralları

**Kural 1**: **Eklenen Görevler** alanı boşsa veya bu alan **Tüm proje görevleri** olarak ayarlanmışsa teklif satırına bir proje dahil edilir.

**Kural 2**: **Eklenen Görevler** alanı boşsa veya bu alan **Tüm proje görevleri** olarak ayarlanmışsa bir proje ve belirli bir işlem sınıfı, bir teklifin yalnızca proje tabanlı bir teklif satırına dahil edilebilir.

**Kural 3**: **Eklenen Görevler** alanı **Yalnızca seçili proje görevleri** olarak ayarlanmışsa bir proje ve belirli bir işlem sınıfı, bir teklifin birden çok proje tabanlı teklif satırına dahil edilebilir.

**Kural 4**: Bir fırsatın birden fazla teklifi varsa hepsi aynı projeye atıfta bulunan ve aynı işlem sınıfını içeren farklı tekliflerden teklif satırları olabilir.

**Kural 5**: Teklifler aynı fırsata ait değilse aynı projeyi ve işlem sınıfını içeremezler.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p>
                    <strong>Fırsat</strong>
                </p>
            </td>
            <td width="39" valign="top">
                <p>
                    <strong>Teklif</strong>
                </p>
            </td>
            <td width="40" valign="top">
                <p>
                    <strong>Teklif satırı</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="77" valign="top">
                <p>
                    <strong>Dahil edilen görevler</strong>
                </p>
            </td>
            <td width="45" valign="top">
                <p>
                    <strong>Zaman Ekle</strong>
                </p>
            </td>
            <td width="46" valign="top">
                <p>
                    <strong>Gider Ekle</strong>
                </p>
            </td>
            <td width="43" valign="top">
                <p>
                    <strong>Malzeme Ekle</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Ekle</strong>
                </p>
                <p>
                    <strong>Ücret</strong>
                </p>
            </td>
            <td width="49" valign="top">
                <p>
                    <strong>Geçerli/Geçerli değil</strong>
                </p>
            </td>
            <td width="200" valign="top">
                <p>
                    <strong>Neden</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Ç1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Boş </p>
            </td>
            <td width="45" valign="top">
                <p>
Evet </p>
            </td>
            <td width="46" valign="top">
                <p>
Evet </p>
            </td>
            <td width="43" valign="top">
                <p>
Evet </p>
            </td>
            <td width="41" valign="top">
                <p>
Evet </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Geçerli değil </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Kural 2'nin ihlali. P1 projesindeki Zaman, Gider ve Ücretler, QL1 ve QL2 teklif satırlarına dahil edilir </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Ç1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Boş </p>
            </td>
            <td width="45" valign="top">
                <p>
Evet </p>
            </td>
            <td width="46" valign="top">
                <p>
Evet </p>
            </td>
            <td width="43" valign="top">
                <p>
Evet </p>
            </td>
            <td width="41" valign="top">
                <p>
Evet </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Ç1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Boş </p>
            </td>
            <td width="45" valign="top">
                <p>
Evet </p>
            </td>
            <td width="46" valign="top">
                <p>
No </p>
            </td>
            <td width="43" valign="top">
                <p>
Evet </p>
            </td>
            <td width="41" valign="top">
                <p>
Evet </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Geçerli değil </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Kural 2'nin ihlali. P1 projesindeki Zaman, Malzeme ve Ücretler, QL1 ve QL2 teklif satırlarına dahil edilir </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Ç1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Boş </p>
            </td>
            <td width="45" valign="top">
                <p>
Evet </p>
            </td>
            <td width="46" valign="top">
                <p>
Evet </p>
            </td>
            <td width="43" valign="top">
                <p>
Evet </p>
            </td>
            <td width="41" valign="top">
                <p>
Evet </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Ç1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Boş </p>
            </td>
            <td width="45" valign="top">
                <p>
Evet </p>
            </td>
            <td width="46" valign="top">
                <p>
No </p>
            </td>
            <td width="43" valign="top">
                <p>
Evet </p>
            </td>
            <td width="41" valign="top">
                <p>
Evet </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Geçerli </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
P1 projesindeki Zaman, Malzeme ve Ücretler QL1'e dahil edilir <br>
P1 projesindeki giderler QL2'ye dahildir <br>
Her bir teklif satırına dahil edilenler arasında çakışma yok ve bu nedenle geçerli.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Ç1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Boş </p>
            </td>
            <td width="45" valign="top">
                <p>
No </p>
            </td>
            <td width="46" valign="top">
                <p>
Evet </p>
            </td>
            <td width="43" valign="top">
                <p>
No </p>
            </td>
            <td width="41" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Ç1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Yalnızca seçili görevler </p>
            </td>
            <td width="45" valign="top">
                <p>
Evet </p>
            </td>
            <td width="46" valign="top">
                <p>
Evet </p>
            </td>
            <td width="43" valign="top">
                <p>
Evet </p>
            </td>
            <td width="41" valign="top">
                <p>
Evet </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Geçerli değil </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Kural 2'nin ihlali </p>
                <p>
Q1'e, proje P1 üzerindeki bir görev alt kümesinde Zaman, Malzeme, Giderler ve Ücretler dahildir </p>
                <p>
QL2 tüm proje P1 için Zaman, Giderler ve Ücretleri içerir, bu nedenle Q1'in içerdiği verilerle örtüşür.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Ç1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Boş </p>
            </td>
            <td width="45" valign="top">
                <p>
Evet </p>
            </td>
            <td width="46" valign="top">
                <p>
Evet </p>
            </td>
            <td width="43" valign="top">
                <p>
Evet </p>
            </td>
            <td width="41" valign="top">
                <p>
Evet </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Ç1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Yalnızca seçili görevler </p>
            </td>
            <td width="45" valign="top">
                <p>
Evet </p>
            </td>
            <td width="46" valign="top">
                <p>
Evet </p>
            </td>
            <td width="43" valign="top">
                <p>
Evet </p>
            </td>
            <td width="41" valign="top">
                <p>
Evet </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Geçerli </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Kural 3 uyarınca, </p>
                <p>
Q1'e, proje P1 üzerindeki bir görev alt kümesinde Zaman, Malzeme, Giderler ve Ücretler dahildir.
                </p>
                <p>
QL2'e, proje P1 üzerindeki bir görev alt kümesi için Zaman, Malzeme ve Giderler dahildir.
                </p>
                <p>
Yalnızca tek bir ek doğrulama yapılır. Bu doğrulamanın amacı, çakışmaları önlemek için QL1 üzerindeki alt görevlerin QL2 üzerindeki alt görevlerden farklı olmasını kontrol etmektir. Bu, görevler ilişkilendirildiğinde sistem tarafından yapılır.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Ç1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Yalnızca seçili görevler </p>
            </td>
            <td width="45" valign="top">
                <p>
Evet </p>
            </td>
            <td width="46" valign="top">
                <p>
Evet </p>
            </td>
            <td width="43" valign="top">
                <p>
Evet </p>
            </td>
            <td width="41" valign="top">
                <p>
Evet </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Ç1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tüm proje görevleri veya boş </p>
            </td>
            <td width="45" valign="top">
                <p>
Evet </p>
            </td>
            <td width="46" valign="top">
                <p>
Evet </p>
            </td>
            <td width="43" valign="top">
                <p>
Evet </p>
            </td>
            <td width="41" valign="top">
                <p>
Evet </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Geçerli </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Kural 5 uyarınca, Q1 ve Q2 aynı fırsata yönelik iki tekliftir, bu nedenle ikisi de aynı proje bileşenleri için tahminde bulunabilir.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Ç2 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tüm proje görevleri veya boş </p>
            </td>
            <td width="45" valign="top">
                <p>
Evet </p>
            </td>
            <td width="46" valign="top">
                <p>
Evet </p>
            </td>
            <td width="43" valign="top">
                <p>
Evet </p>
            </td>
            <td width="41" valign="top">
                <p>
Evet </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Ç1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tüm proje görevleri veya boş </p>
            </td>
            <td width="45" valign="top">
                <p>
Evet </p>
            </td>
            <td width="46" valign="top">
                <p>
Evet </p>
            </td>
            <td width="43" valign="top">
                <p>
Evet </p>
            </td>
            <td width="41" valign="top">
                <p>
Evet </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Geçerli Değil </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Kural 4 uyarınca, Q1 ve Q2 farklı fırsatlara yönelik iki tekliftir, bu nedenle ikisi de aynı projenin aynı bileşenleri için tahminde bulunamaz.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O2 </p>
            </td>
            <td width="39" valign="top">
                <p>
Ç1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tüm proje görevleri veya boş </p>
            </td>
            <td width="45" valign="top">
                <p>
Evet </p>
            </td>
            <td width="46" valign="top">
                <p>
Evet </p>
            </td>
            <td width="43" valign="top">
                <p>
Evet </p>
            </td>
            <td width="41" valign="top">
                <p>
Evet </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
