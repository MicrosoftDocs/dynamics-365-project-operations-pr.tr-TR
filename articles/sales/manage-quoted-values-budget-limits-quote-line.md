---
title: Proje tabanlı teklif satırlarına genel bakış
description: Bu konuda, proje çalışmaları için proje tabanlı teklif satırlarını kullanma hakkında bilgiler sağlanmaktadır.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e61a9fbf357123884397b930662d11f22bfdeaa0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277812"
---
# <a name="project-based-quote-lines-overview"></a>Proje tabanlı teklif satırlarına genel bakış

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Proje tabanlı teklif satırları, bir etkileşimdeki proje çalışmalarının tahmin edilmesine yardımcı olmak için tasarlanmıştır. Proje tabanlı teklif satırının yapısı, aşağıdaki kavramlarla proje tahminleri için genişletilmiştir:

- Faturalama Yöntemi
- Proje Eşlemesi
- Dahil Edilen İşlem sınıfları
- Aşılamaz Limit
- Borçlandırılabilirlik ayarı
- Teklif Satırı Ayrıntılarını kullanarak tahmin yürütme
- Teklif satırı Müşterileri

Aşağıdaki tabloda proje tabanlı teklif satırının **Genel** sekmesindeki alanlar hakkında bilgi sağlanmaktadır. Bu alanlar, proje çalışmaları için ayrıntılı, baştan sona bir tahmin için temel oluşturulmasına yardımcı olur.

| **Alan** | **Açıklama** | **Aşağı yönlü etki** |
| --- | --- | --- |
| Veri Akışı Adı | Tahmin edilen teklifin farklı olan bileşenini belirlemenize yardımcı olması gereken teklif satırının adı. | Teklif kazanıldığında, bu teklif satırından oluşturulan proje sözleşme satırına kopyalanır. |
| Faturalama Yöntemi | Fırsattan oluşturulan bir teklifte bu değer, fırsat satırındaki ilgili alandan kopyalanır. Bu alan, Dynamics 365 Project Operations tarafından desteklenen iki ana sözleşme modeli içerir:</br>- Sabit fiyat</br>- Zaman ve malzeme.| Bu alanın değeri, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşme satırına kopyalanır. |
| Project | Bu etkileşimde kullanılacak projeyi belirleyerek çalışmayı teslim etmek için bu isteğe bağlı alanı kullanın. Proje bir teklif satırına eşlendiğinde, borçlandırılabilir görevler oluşturulmasına ve ayrıca proje bazlı bir tahminin teklif satırına teklif satırı ayrıntıları olarak getirilmesine yardımcı olur. Proje, proje bazlı bir teklif satırına eşlenmediğinde tahmin, her bir teklif satırı ayrıntısının el ile oluşturulmasıyla elde edilmelidir. | Bu alanın değeri, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşme satırına kopyalanır. |
| Zaman Ekle | **Evet**/**Hayır** bayrağı, seçilen projedeki zaman işlemlerinin veya işçilik maliyetlerinin bu teklif satırındaki tahmine dahil edilip edilmeyeceğini belirtir. **Hayır** değeri, zaman işlemlerinin veya işçilik maliyetinin bu teklif satırındaki tahmine dahil edilmeyeceğini belirtir. **Evet** değeri, zaman işlemlerinin veya işçilik maliyetinin bu teklif satırındaki tahmine dahil edileceğini belirtir. | Bu alanın değeri, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşme satırına kopyalanır. |
| Gider Ekle | **Evet**/**Hayır** bayrağı, seçilen projedeki gider maliyetlerinin bu teklif satırındaki tahmine dahil edilip edilmeyeceğini belirtir. **Hayır** değeri, gider maliyetinin bu teklif satırındaki tahmine dahil edilmeyeceğini belirtir. **Evet** değeri, gider maliyetinin bu teklif satırındaki tahmine dahil edileceğini belirtir. | Bu alanın değeri, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşme satırının üzerine kopyalanır. |
| Ücret Ekle | **Evet**/**Hayır** bayrağı, seçilen projedeki ücretlerin bu teklif satırındaki tahmine dahil edilip edilmeyeceğini belirtir. **Hayır** değeri, Ücretlerin bu teklif satırındaki tahmine dahil edilmeyeceğini belirtir. **Evet** değeri, Ücretlerin bu teklif satırındaki tahmine dahil edileceğini belirtir. | Bu alanın değeri, teklif kazanıldığında bu teklif satırından oluşturulan Proje sözleşme satırına kopyalanır. |
| Teklif Edilen Tutar | Bu, proje tabanlı teklif satırında tahmin edilen tüm çalışmalar için müşteriye teklif edilecek tutardır. Fırsattan oluşturulan bir teklifte, bu değer fırsat satırındaki **Müşteri Bütçesi** alanından kopyalanır. Proje tabanlı teklif satırı satır ayrıntılarına sahip olduğunda, bu alan düzenlemeye kilitlenir ve teklif satırı ayrıntılarındaki tutardan özetlenir. | Bu alanın değeri, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşme satırına kopyalanır. |
| Tahmini Vergi | Bu, kullanıcının teklif satırına tahmini vergi tutarını ekleyebileceği düzenlenebilir bir alandır. Proje tabanlı teklif satırı, satır ayrıntılarına sahip olduğunda, bu alan düzenlemeye kilitlenir ve teklif satırı ayrıntılarındaki vergi tutarından özetlenir. | Bu alanın değeri, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşme satırına kopyalanır. |
| Vergi Sonrası Teklif Tutarı | Bu alan, vergi sonrası teklif satırı tutarıdır ve salt okunurdur. Bu alandaki tutar *Teklif Tutarı + Vergi* olarak hesaplanır. | Bu alanın değeri, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşme satırına kopyalanır. |
| Aşılamaz Limit | Bu alan, düzenlenebilirdir ve yalnızca **Zaman ve Malzeme** faturalama yöntemine sahip proje bazlı teklif satırlarında kullanılabilir. | Bu alanın değeri, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşme satırına kopyalanır. |
| Müşteri Bütçesi | Bu alan, düzenlenebilirdir ve teklif bir fırsattan oluşturulmuşsa fırsat satırındaki ilgili alandan kopyalanır. | Bu alanın değeri, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşme satırına kopyalanır. |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Proje tabanlı teklif satırlarının Genel sekmesindeki alanları için doğrulama kuralları

**Kural 1**: Seçilen projedeki belirli bir işlem sınıfı bir teklifin yalnızca bir proje tabanlı teklif satırına dahil edilebilir.

**Kural 2**: Bir fırsatın birden fazla teklifi varsa hepsi aynı projeye atıfta bulunan ve aynı işlem sınıfını içeren farklı tekliflerden teklif satırları olabilir.

**Kural 3**: Teklifler aynı fırsata ait değilse aynı projeyi ve işlem sınıfını içeremezler.

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p>
                    <strong>Fırsat</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Teklif</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Teklif satırı</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Zaman ekle</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Gider ekle</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Ekle</strong>
                </p>
                <p>
                    <strong>ücret</strong>
                </p>
            </td>
            <td width="54" valign="top">
                <p>
                    <strong>Geçerli/Geçerli değil</strong>
                </p>
            </td>
            <td width="308" valign="top">
                <p>
                    <strong>Neden</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Ç1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
            <td width="54" rowspan="2" valign="top">
                <p>
Geçerli değil </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Kural 1'nin ihlali. P1 projesindeki Zaman, Gider ve Ücretler, QL1 ve QL2 teklif satırlarının her ikisine de dahil edilir.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Ç1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Ç1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
            <td width="54" rowspan="2" valign="top">
                <p>
Geçerli değil </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Kural 1'nin ihlali. P1 projesindeki Zaman ve Ücretler, QL1 ve QL2 teklif satırlarının her ikisine de dahil edilir.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Ç1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Ç1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
            <td width="54" rowspan="2" valign="top">
                <p>
Geçerli </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
P1 projesindeki zaman ve ücretler, QL1'e dahil edilir.
P1 projesindeki giderler QL2'ye dahildir.
Dahil edilen teklif satırlarının hiçbirinin birbiriyle çakışması yoktur ve bu yüzden geçerlidir.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Ç1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Ç1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
            <td width="54" rowspan="2" valign="top">
                <p>
Geçerli değil </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Kural 1'nin yukarıdaki ihlali </p>
                <p>
Q1, P1 projesinin tamamı için Zaman, Giderler ve Ücretleri içerir.
                </p>
                <p>
QL2, P1 projesinin tamamı için Zaman, Giderler ve Ücretleri içerir ve Q1'e dahil olanlarla örtüşür.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Ç1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Ç1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
            <td width="54" valign="top">
                <p>
Geçerli </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Kural 2'e göre, Q1 ve Q2 aynı fırsatta iki tekliftir; böylelikle projenin aynı bileşenleri için ikisi de tahmin edilebilir.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Ç2 </p>
            </td>
            <td width="42" valign="top">
                <p>
Q2'de QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Ç1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
            <td width="54" valign="top">
                <p>
Geçerli </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Kural #3 göre, Q1 ve Q2 farklı fırsatlarda iki tekliftir; bu nedenle aynı projenin aynı bileşenleri için tahmin edilemezler.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O2 </p>
            </td>
            <td width="41" valign="top">
                <p>
Ç1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
            <td width="54" valign="top">
                <p>
Geçerli Değil </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../includes/footer-banner.md)]