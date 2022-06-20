---
title: Düzeltici proje tabanlı faturalar
description: Bu makalede, Project Operations'ta proje tabanlı faturaları oluşturma ve düzeltmeye yönelik bilgiler sağlanmaktadır.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: eecaf3dedeab5ff72d12808eb3144f9161313009
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931124"
---
# <a name="corrective-project-based-invoices"></a>Düzeltici proje tabanlı faturalar

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Onaylı proje faturaları müşteri ve proje yöneticisiyle görüşülür, değişiklikleri veya kredileri işlemek için düzeltilebilir.

Onaylı bir faturada düzenlemeler yapmak için, onaylanan faturayı açın ve **Bu faturayı Düzelt**'i seçin. 

> [!NOTE]
> Proje faturası onaylanmadıkça veya proje tabanlı faturada avanslar veya elde tutulan tutar ya da avansların veya elde tutulan tutarların mutabakatları yoksa bu seçim kullanılamaz.

Onaylanan faturadan yeni bir taslak fatura oluşturulur. Daha önce onaylanan faturadan tüm fatura satırı ayrıntıları yeni taslağın kopyası alınır. Yeni düzeltilen fatura hakkındaki satır ayrıntılarını anlamak için aşağıda yer alan önemli noktaların bazıları aşağıda verilmiştir:

- Tüm miktarlar sıfıra güncelleştirilir. Dynamics 365 Project Operations, tüm faturalanan maddelerin tam olarak alacaklandırıldığını varsayar. Gerekirse, bu miktarları, alacaklandırılan miktarı değil, faturalanan miktarı yansıtacak şekilde el ile güncelleştirebilirsiniz. Girdiğiniz miktara bağlı olarak, uygulama alacaklı miktarı hesaplar. Bu miktar, düzeltilen fatura onaylandığı zaman oluşturulan fiili değerlere yansıtılır. Vergi tutarında değişiklikler yapıyorsanız, alacak kaydedilen vergi tutarını değil, doğru vergi tutarını girmeniz gerekir.
- Kilometre taşı düzeltmeleri her zaman tam kredi olarak işlenir.


> [!IMPORTANT]
> Önceden faturalandırılmış diğer giderlere yönelik düzeltmeler olan fatura satırı ayrıntılarının **Düzeltme** alanı, **Evet** olarak ayarlanmıştır. Düzeltilmiş fatura satırı ayrıntıları olan faturaların **Düzeltmeler var** alanı, **Evet** olarak ayarlanmıştır.

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a>Bir düzeltici fatura onaylandığında oluşturulan gerçek değerler

Aşağıdaki tabloda, bir düzeltici fatura onaylandıktan sonra oluşturulan gerçek değerler listelenmiştir.

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
Daha önce faturalanmış bir malzeme hareketinin tam kredisinin faturalanması.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Malzemenin orijinal fatura satırı ayrıntılarındaki miktar ve tutar için faturalanmış satışı tersine çevirme işlemi.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Malzemenin orijinal fatura satırı ayrıntılarındaki miktar ve tutar için yeni faturalanmamış satış gerçek değeri.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Malzeme hareketindeki kısmi kredinin faturalanması.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Malzemenin orijinal fatura satırı ayrıntılarındaki miktar ve faturalanan tutar için faturalanmış satışı tersine çevirme işlemi.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Düzenlenen fatura satırı ayrıntısındaki miktar ve tutar için borçlandırılabilen yeni faturalanmayan satış gerçek değeri, bunun tersine çevrilmesi ve eşdeğer faturalanan satış gerçek değeri.
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
Kilometre taşının fatura durumu, <b>Deftere Nakledilen Müşteri Faturası</b> durumundan <b>Faturalanmaya Hazır</b> durumuna güncelleştirilir.
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
Bu senaryo desteklenmez.
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
