---
title: Proforma faturaları onaylama
description: Bu konuda, bir proforma faturanın onaylanması hakkında bilgiler sağlanmaktadır.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b2ed241509d2643d841ce55777e6e316612f70b8
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287892"
---
# <a name="confirm-a-proforma-invoice"></a>Proforma faturaları onaylama

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Proforma fatura onaylandıktan sonra, proje faturasının durumu **Onaylandı** güncellenir. Bir fatura onaylandığında, salt okunur olur. İleriye dönük olarak, fatura yalnızca müşteri tarafından başlatılan düzeltmeler veya krediler varsa veya ödeme olarak işaretlendiğinde düzeltilebilir.

Aşağıdaki tabloda sistem tarafından oluşturulan fiili listeler. Bu fiili işlemler, onaylanmadan önce taslak proje faturasında belirli işlemler gerçekleştirildiğinde oluşturulur.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p>
                    <strong>Senaryo</strong>
                </p>
            </td>
            <td width="608" valign="top">
                <p>
                    <strong>Onayda oluşturulan fiililer</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Taslak faturada herhangi bir işlem yapılmadan bir zaman hareketi faturalandırma.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Orijinal saat onayının saat ve tutarı için faturalandırılmamış satış tersi.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Orijinal saat onayının saat ve tutarı için faturalandırılmış satış fiili.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Miktarı azaltmak için düzenlenen bir zaman hareketinin faturalandırması.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Orijinal saat onayının saat ve tutarı için faturalandırılmamış satış tersi.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Düzenlenen fatura satırı ayrıntısı üzerindeki saat ve tutar için ücretlendirilebilen yeni bir faturalanmamış satış fiili, faturalandırılmamış satışların fiilinin tersine çevrilmesi ve eşdeğer faturalı satışların fiili.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Düzenlenen fatura satırı ayrıntısı üzerindeki doğrulanan rakamlar çıkarıldıktan sonra kalan saat ve tutar için ücretlendirilemeyen yeni bir faturalanmamış satış fiili, faturalandırılmamış satışların fiilinin tersine çevrilmesi ve eşdeğer faturalı satışların fiili.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Miktarı artırmak için düzenlenen bir zaman hareketinin faturalandırması.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Orijinal saat onayının saat ve tutarı için faturalandırılmamış satış tersi.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Düzenlenen fatura satırı ayrıntısı üzerindeki saat ve tutar için ücretlendirilebilen yeni bir faturalanmamış satış fiili, faturalandırılmamış satışların fiilinin tersine çevrilmesi ve eşdeğer faturalı satışların fiili.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Taslak faturada herhangi bir işlem yapılmadan bir gider hareketi faturalandırma.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Orijinal gider onayının miktarı ve tutarı için faturalandırılmamış satış tersi.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Orijinal gider onayının miktarı ve tutarı için faturalandırılmış satış fiili.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Miktarı azaltmak için düzenlenen bir gider hareketinin faturalandırması.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Orijinal gider onayının miktarı ve tutarı için faturalandırılmamış satış tersi.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Düzenlenen fatura satırı ayrıntısı üzerindeki miktar ve tutar için ücretlendirilebilen yeni bir faturalanmamış satış fiili, faturalandırılmamış satışların fiilinin tersine çevrilmesi ve eşdeğer faturalı satışların fiili. 
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Düzenlenen fatura satırı ayrıntısı üzerindeki doğrulanan rakamlar çıkarıldıktan sonra kalan miktar ve tutar için ücretlendirilemeyen yeni bir faturalanmamış satış fiili, faturalandırılmamış satışların fiilinin tersine çevrilmesi ve eşdeğer faturalı satışların fiili.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Miktarı artırmak için düzenlenen bir gider hareketinin faturalandırması.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Orijinal gider onayının miktarı ve tutarı için faturalandırılmamış satış tersi.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Düzenlenen fatura satırı ayrıntısı üzerindeki miktar ve tutar için ücretlendirilebilen yeni bir faturalanmamış satış fiili, faturalandırılmamış satışların fiilinin tersine çevrilmesi ve eşdeğer faturalı satışların fiili.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Bir ücret faturalama.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Orijinal yevmiye defteri satırında ücret tutarı için faturalandırılmamış satış tersi.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Orijinal ücret yevmiye defteri satırı miktarı ve tutarı için faturalandırılmış satış fiili.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Bir kilometre taşını faturalama.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Proje sözleşmesi satırındaki özgün kilometre taşındaki kilometre taşı tutarı için faturalı satış fiili.
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]