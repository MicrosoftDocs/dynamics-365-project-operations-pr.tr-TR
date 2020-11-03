---
title: Proje tabanlı teklif satırları (Pro)
description: Bu konuda, proje çalışmaları için proje tabanlı teklif satırlarını kullanma hakkında bilgiler sağlanmaktadır. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a409d1e378afe97de7fb6c77cf3ad6703661bdff
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086254"
---
# <a name="project-based-quote-lines-pro"></a>Proje tabanlı teklif satırları (Pro)

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Proje tabanlı teklif satırları, bir etkileşimdeki proje çalışmalarının tahmin edilmesine yardımcı olmak için tasarlanmıştır. Proje tabanlı teklif satırının yapısı, aşağıdaki kavramlarla proje tahminleri için genişletilmiştir:

- Faturalama Yöntemi
- Proje ve Görev Eşleme
- Dahil Edilen İşlem sınıfları
- Aşılamaz Limit
- Borçlandırılabilirlik ayarı
- Teklif Satırı Ayrıntılarını kullanarak tahmin yürütme
- Teklif satırı Müşterileri

Aşağıdaki tabloda proje tabanlı teklif satırının **Genel** sekmesindeki alanlar hakkında bilgi sağlanmaktadır. Bu alanlar, proje çalışmaları için ayrıntılı, baştan sona bir tahmin için temel oluşturulmasına yardımcı olur.

| **Alan** | **İlgi, amaç ve kılavuz** | **Aşağı yönlü etki** |
| --- | --- | --- |
| Veri Akışı Adı | Tahmin edilen teklifin farklı olan bileşenini belirlemenize yardımcı olması gereken teklif satırının adı. | Teklif kazanıldığında, bu teklif satırından oluşturulan proje sözleşme satırına kopyalanır. |
| Faturalama Yöntemi | Fırsattan oluşturulan bir teklifte bu değer, fırsat satırındaki ilgili alandan kopyalanır. Bu alan, Dynamics 365 Project Operations tarafından desteklenen iki ana sözleşme modelini içerir:</br>- Sabit fiyat</br>- Zaman ve malzeme.| Bu alanın değeri, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşme satırına kopyalanır. |
| Project | Bu etkileşimde kullanılacak projeyi belirleyerek çalışmayı teslim etmek için bu isteğe bağlı alanı kullanın. Proje bir teklif satırına eşlendiğinde, borçlandırılabilir görevler oluşturulmasına ve ayrıca proje bazlı bir tahminin teklif satırına teklif satırı ayrıntıları olarak getirilmesine yardımcı olur. Proje, proje bazlı bir teklif satırına eşlenmediğinde tahmin, her bir teklif satırı ayrıntısının el ile oluşturulmasıyla elde edilmelidir. | Bu alanın değeri, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşme satırına kopyalanır.|
| Dahil Edilen Görevler | Bu teklif satırının seçilen projenin görevlerinin tümünde veya bazılarında kullanılıp kullanılmadığını gösterir. Bu alan aşağıdaki olası değerlere sahiptir:</br>- Tüm proje görevleri</br>- Yalnızca seçili proje görevleri</br>Bu alandaki boş bir değer **Tüm proje görevleri** seçeneğinin eşdeğeridir. | Proje sayfasında **Yalnızca seçili proje görevleri** seçildiğinde, **Görev faturalama ayarları** sekmesi belirli görevleri, bu teklif satırıyla ilişkilendirmek için seçmenize olanak tanır. Bu alanın değeri, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşme satırına kopyalanır. |
| Zaman Ekle | **Evet**/**Hayır** bayrağı, seçilen projedeki zaman işlemlerinin veya işçilik maliyetlerinin bu teklif satırındaki tahmine dahil edilip edilmeyeceğini belirtir. **Hayır** değeri, zaman işlemlerinin veya işçilik maliyetinin bu teklif satırındaki tahmine dahil edilmeyeceğini belirtir. **Evet** değeri, zaman işlemlerinin veya işçilik maliyetinin bu teklif satırındaki tahmine dahil edileceğini belirtir. | Bu alanın değeri, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşme satırına kopyalanır. |
| Gider Ekle | **Evet**/**Hayır** bayrağı, seçilen projedeki gider maliyetlerinin bu teklif satırındaki tahmine dahil edilip edilmeyeceğini belirtir. **Hayır** değeri, gider maliyetinin bu teklif satırındaki tahmine dahil edilmeyeceğini belirtir. **Evet** değeri, gider maliyetinin bu teklif satırındaki tahmine dahil edileceğini belirtir. | Bu alanın değeri, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşme satırının üzerine kopyalanır. |
| Ücret Ekle | **Evet**/**Hayır** bayrağı, seçilen projedeki ücretlerin bu teklif satırındaki tahmine dahil edilip edilmeyeceğini belirtir. **Hayır** değeri, Ücretlerin bu teklif satırındaki tahmine dahil edilmeyeceğini belirtir. **Evet** değeri, Ücretlerin bu teklif satırındaki tahmine dahil edileceğini belirtir. | Bu alanın değeri, teklif kazanıldığında bu teklif satırından oluşturulan Proje sözleşme satırına kopyalanır. |
| Teklif Edilen Tutar | Bu, proje tabanlı teklif satırında tahmin edilen tüm çalışmalar için müşteriye teklif edilecek tutardır. Fırsattan oluşturulan bir teklifte, bu değer fırsat satırındaki **Müşteri Bütçesi** alanından kopyalanır. Proje tabanlı teklif satırı satır ayrıntılarına sahip olduğunda, bu alan düzenlemeye kilitlenir ve teklif satırı ayrıntılarındaki tutardan özetlenir. | Bu alanın değeri, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşme satırına kopyalanır. |
| Tahmini Vergi | Bu, kullanıcının teklif satırına tahmini vergi tutarını ekleyebileceği düzenlenebilir bir alandır. Proje tabanlı teklif satırı, satır ayrıntılarına sahip olduğunda, bu alan düzenlemeye kilitlenir ve teklif satırı ayrıntılarındaki vergi tutarından özetlenir. | Bu alanın değeri, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşme satırına kopyalanır. |
| Vergi Sonrası Teklif Tutarı | Bu alan, vergi sonrası teklif satırı tutarıdır ve salt okunurdur. Bu alandaki tutar *Teklif Tutarı + Vergi* olarak hesaplanır. | Bu alanın değeri, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşme satırına kopyalanır. |
| Aşılamaz Limit | Bu alan, düzenlenebilirdir ve yalnızca **Zaman ve Malzeme** faturalama yöntemine sahip proje bazlı teklif satırlarında kullanılabilir. | Bu alanın değeri, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşme satırına kopyalanır. |
| Müşteri Bütçesi | Bu alan, düzenlenebilirdir ve teklif bir fırsattan oluşturulmuşsa fırsat satırındaki ilgili alandan kopyalanır. | Bu alanın değeri, teklif kazanıldığında bu teklif satırından oluşturulan proje sözleşme satırına kopyalanır. |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Proje tabanlı teklif satırlarının Genel sekmesindeki alanları için doğrulama kuralları

**Kural 1** : **Eklenen Görevler** alanı boşsa veya bu alan **Tüm proje görevleri** olarak ayarlanmışsa teklif satırına bir proje dahil edilir.

**Kural 2** : **Eklenen Görevler** alanı boşsa veya bu alan **Tüm proje görevleri** olarak ayarlanmışsa bir proje ve belirli bir işlem sınıfı, bir teklifin yalnızca proje tabanlı bir teklif satırına dahil edilebilir.

**Kural 3** : **Eklenen Görevler** alanı **Yalnızca seçili proje görevleri** olarak ayarlanmışsa bir proje ve belirli bir işlem sınıfı, bir teklifin birden çok proje tabanlı teklif satırına dahil edilebilir.

**Kural 4** : Bir fırsatın birden fazla teklifi varsa hepsi aynı projeye atıfta bulunan ve aynı işlem sınıfını içeren farklı tekliflerden teklif satırları olabilir.

**Kural 5** : Teklifler aynı fırsata ait değilse aynı projeyi ve işlem sınıfını içeremezler.

<table border="0" cellspacing="0" cellpadding="0">
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
            <td width="90" valign="top">
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
                    <strong>Ekle</strong>
                </p>
                <p>
                    <strong>Ücret</strong>
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
            <td width="90" valign="top">
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
            <td width="54" rowspan="2" valign="top">
                <p>
Geçerli değil </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Kural 2'nin ihlali. P1 projesindeki Zaman, Gider ve Ücretler, QL1 ve QL2 teklif satırlarına dahil edilir.
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
            <td width="90" valign="top">
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
            <td width="90" valign="top">
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
            <td width="90" valign="top">
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
            <td width="54" rowspan="2" valign="top">
                <p>
Geçerli değil </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Kural 2'nin ihlali. P1 projesindeki Zaman ve Ücretler, QL1 ve QL2 teklif satırlarına dahil edilir.
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
            <td width="90" valign="top">
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
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
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
            <td width="90" valign="top">
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
            <td width="54" rowspan="2" valign="top">
                <p>
Geçerli </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
P1 projesindeki Zaman ve Ücretler, QL1'e dahil edilir.
P1 projesindeki giderler QL2'ye dahildir.
Dahil edilen teklif satırlarının hiçbirinin birbiriyle çakışması yoktur ve hepsi geçerlidir.
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
            <td width="90" valign="top">
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
            <td width="90" valign="top">
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
            <td width="90" valign="top">
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
            <td width="54" rowspan="2" valign="top">
                <p>
Geçerli değil </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Kural 2'nin yukarıdaki ihlali </p>
                <p>
Q1, proje P1 üzerinde bir görev alt kümesinde Zaman, Giderler ve Ücretleri içerir.
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
            <td width="90" valign="top">
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
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
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
            <td width="90" valign="top">
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
            <td width="54" rowspan="2" valign="top">
                <p>
Geçerli </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Yukarıdaki Kural 3'e göre, </p>
                <p>
Q1, proje P1 üzerinde bir görev alt kümesinde Zaman, Giderler ve Ücretleri içerir.
                </p>
                <p>
QL2, proje P1 üzerinde bir görev alt kümesinde Zaman, Giderler ve Ücretleri içerir.
                </p>
                <p>
Tek ek doğrulama, QL2'deki görevlerin alt kümesinden farklı olan QL1'deki görevlerin alt kümesiyle ilgilidir. Bu sayede hiçbir çakışma olmaması sağlanır. Bu, görevler ilişkilendirildiğinde sistem tarafından yapılır.
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
            <td width="90" valign="top">
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
            <td width="90" valign="top">
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
            <td width="90" valign="top">
                <p>
Tüm proje görevleri veya boş </p>
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
Kural 5'e göre, Q1 ve Q2 aynı fırsatta iki tekliftir; böylelikle projenin aynı bileşenleri için ikisi de tahmin edilebilir.
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
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Tüm proje görevleri veya boş </p>
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
            <td width="90" valign="top">
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
            <td width="90" valign="top">
                <p>
Tüm proje görevleri veya boş </p>
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
Kural #4 göre, Q1 ve Q2 farklı fırsatlarda iki tekliftir; bu nedenle aynı projenin aynı bileşenleri için tahmin edilemezler.
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
            <td width="90" valign="top">
                <p>
Tüm proje görevleri veya boş </p>
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

