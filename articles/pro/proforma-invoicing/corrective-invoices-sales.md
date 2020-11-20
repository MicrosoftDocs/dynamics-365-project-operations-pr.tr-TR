---
title: Düzeltilen faturalar - lite
description: Bu konuda, Project Operations'ta doğrulanan faturalar hakkında bilgiler sağlanmaktadır.
author: rumant
manager: Annbe
ms.date: 10/15/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 55bec8ad1d9c2b55cabb453321f13df8b7cd1614
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176455"
---
# <a name="corrected-invoices---lite"></a>Düzeltilen faturalar - lite

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Onaylı proje faturaları müşteri ve proje yöneticisiyle görüşülür, değişiklikleri veya kredileri işlemek için düzeltilebilir.

Onaylı bir faturada düzenlemeler yapmak için, onaylanan faturayı açın ve **Bu faturayı Düzelt**'i seçin. 

> [!NOTE]
> Bir proje faturası onaylanmadıkça bu seçim kullanılamaz.

Onaylanan faturadan yeni bir taslak fatura oluşturulur. Daha önce onaylanan faturadan tüm fatura satırı ayrıntıları yeni taslağın kopyası alınır. Yeni düzeltilen fatura hakkındaki satır ayrıntılarını anlamak için aşağıda yer alan önemli noktaların bazıları aşağıda verilmiştir:

- Tüm miktarlar sıfıra güncelleştirilir. Uygulama tüm faturalanan maddelerin tam olarak alacaklandırıldığını kabul eder. Gerekirse, bu miktarları, alacaklandırılan miktarı değil, faturalanan miktarı yansıtacak şekilde el ile güncelleştirebilirsiniz. Girdiğiniz miktara bağlı olarak, uygulama alacaklı miktarı hesaplar. Bu miktar, düzeltilen fatura onaylandığı zaman oluşturulan fiili değerlere yansıtılır. Vergi tutarında değişiklikler yapıyorsanız, alacak kaydedilen vergi tutarını değil, doğru vergi tutarını girmeniz gerekir.
- Önceden onaylanmış ürün tabanlı sözleşme satırları üzerine kopyalanmaz. Ürün tabanlı bir proje faturasındaki düzeltmelerin işlenmesi desteklenmez.
- Kilometre taşı düzeltmeleri her zaman tam kredi olarak işlenir.
- Müşteri hatalı bir tutar için faturalandıysa, Retainer veya avans tutarları düzeltilebilir.
- Önceden onaylanmış bir faturadaki giderlere göre mutabakat sağlamak için yanlış bir tutar kullanılmışsa, retainers ve avanslar mutabakatları düzeltilebilir.

> [!IMPORTANT]
> Önceden faturalandırılmış diğer giderlere yönelik düzeltmeler olan fatura satırı ayrıntıları, alan **düzeltmesi** **Evet** olarak ayarlanmıştır. Düzeltilen fatura satırı ayrıntıları olan faturalarda **Evet** olarak ayarlanmış **düzeltmeler vardır** adlı alanı bulunur.

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a>Düzeltme faturasının onaylanması sırasında oluşturulan gerçek değerler:

Aşağıda, onay öncesinde taslak düzeltme faturasında gerçekleştirilen operasyonlara dayalı olarak düzeltme onaylamada uygulama tarafından oluşturulan fiili değerler yer alır.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p>
                    <strong>Senaryo</strong>
                </p>
            </td>
            <td width="808" valign="top">
                <p>
                    <strong>Onayda oluşturulan fiililer</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
Faturalandırılmış bir avans veya Retainer düzeltmesini onaylayın.<strong></strong>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Mutabakat için oluşturulan hizmetli nin veya avansın faturasız satış tersi. Bu tutar, hizmetli veya avans faturalandığında oluşturulan negatifi iptal etmek amacıyla olduğundan pozitiftir.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Bir faturalanmış satış ters çevirme fiili, Retainer üzerindeki tutar için oluşturulur veya orijinal Faturalanan Satışlar tersine çevrilmesine karşı ilerletir.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Yeni faturalı satış fiili türü, Elde kalan avans veya elde kalan üzerindeki tutar için oluşturulur.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Mutabakat için kullanılacak olan hizmetli veya avansa dayalı düzeltilmiş fatura satırının negatif tutarının faturalandırılmamış satışları.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
Daha önce mutabakat sağlanmış bir elde kalan veya avans düzeltmesi onayı.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Mutabakat için oluşturulan hizmetli nin veya avansın faturasız satış tersi. Bu tutar, önceki mutabakat meydana geldiğinde oluşturulan negatifi iptal etmek amacıyla olduğundan pozitiftir.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Önceki faturadaki tutar için faturalı satış ters fiili.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Yeni faturalı satış fiili türü, doğrulanan faturaya uyguanan elde kalan doğrulanan tutar içindir.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Sonraki faturalarda mutabakat için kullanılacak olan hizmetli veya avansa dayalı düzeltilmiş fatura satırının negatif tutarının faturalandırılmamış satışları.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Daha önce faturalandırılmış bir zaman hareketinin tam kredisinin faturalandırılması.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Saat için orijinal fatura satırı ayrıntısındaki saat ve tutarı için faturalandırılmış satış tersi.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Saat için orijinal fatura satırı ayrıntısındaki saat ve tutarı için yeni faturalandırılmış satış fiili.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Bir zaman hareketinde kısmi kredi faturalama.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Saat için orijinal fatura satırı ayrıntısındaki saat ve tutarı için faturalandırılmış satış tersi.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Düzenlenen fatura satırı ayrıntısı üzerindeki saat ve tutar için ücretlendirilebilen yeni bir faturalanmamış satış fiili, satışların fiilinin tersine çevrilmesi ve eşdeğer faturalı satışların fiili.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Fatura satırı ayrıntısıyla düzeltilen rakamların düşüldükten sonra kalan saatler ve tutar için masraflandırılabilen yeni faturalandırılamayan satış fiili gerçek değeri.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Daha önce faturalandırılmış bir gider hareketinin tam kredisinin faturalandırılması.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Gider için orijinal fatura satırı ayrıntısındaki miktar ve tutarı için faturalandırılmış satış tersi.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Gider için orijinal fatura satırı ayrıntısındaki miktar ve tutarı için yeni faturalandırılmamış satış fiili.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Daha önce faturalandırılmış bir gider hareketinin kısmi kredisinin faturalandırılması.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Gider için orijinal fatura satırı ayrıntısında faturalandırılan miktar ve tutarı için faturalandırılmış satış tersi.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Doğrulanan fatura satırı ayrıntısı üzerindeki miktar ve tutar için ücretlendirilebilen yeni bir faturalanmamış satış fiili, satışların fiilinin tersine çevrilmesi ve eşdeğer faturalı satışların fiili.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Fatura satırı ayrıntısıyla düzeltilen rakamların düşüldükten sonra kalan miktar ve tutar için masraflandırılabilen yeni faturalandırılamayan satış fiili gerçek değeri.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Daha önce faturalandırılmış bir ücret hareketinin tam kredisinin faturalandırılması.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Ücret için orijinal fatura satırı ayrıntısındaki miktar ve tutarı için faturalandırılmış satış tersi.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ücret için orijinal fatura satırı ayrıntısındaki miktar ve tutarı için yeni faturalandırılmamış satış fiili.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Daha önce faturalandırılmış bir ücret hareketinin kısmi kredisinin faturalandırılması.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Ücret için orijinal fatura satırında faturalanan miktar ve tutarı için faturalandırılmış satış tersi.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Doğrulanan fatura satırı ayrıntısı üzerindeki miktar ve tutar için ücretlendirilebilen yeni bir faturalanmamış satış fiili, satışların fiilinin tersine çevrilmesi ve eşdeğer faturalı satışların fiili.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Daha önce faturalandırılmış bir dönüm noktasının tam kredisinin faturalandırılması.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Dönüm noktası için orijinal fatura satırı ayrıntısındaki tutarı için faturalandırılmış satış tersi.
                </p>
                <p>
Proje sözleşmesi satırındaki kilometre taşı faturası veya fatura durumu **faturaya hazır** olarak güncelleştirilir.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Daha önce faturalandırılmış bir dönüm noktasının kısmi kredisinin faturalandırılması.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Desteklenmiyor </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Daha önce faturalandırılmış ürün tabanlı bir sözleşme satırındaki jenerik ve düzeltmeler.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Desteklenmiyor </p>
            </td>
        </tr>
    </tbody>
</table>
