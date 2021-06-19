---
title: Proforma proje faturalarını onaylama
description: Bu konu, Project Operations'ta proforma proje faturalarının onaylanmasının hakkında bilgi sağlar.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0ab40e38f221e57368949b7491578caa8ba88c02
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004150"
---
# <a name="confirm-a-proforma-project-invoice"></a>Proforma proje faturalarını onaylama 

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_


Proforma fatura onaylandıktan sonra, proje faturasının durumu **Onaylandı** güncellenir. Bir fatura onaylandığında, salt okunur olur. Devam ederseniz fatura yalnızca müşteri tarafından başlatılan düzeltmeler veya kredi varsa düzeltilebilir.

Aşağıdaki tabloda sistem tarafından oluşturulan fiili listeler. Bu fiili işlemler, onaylanmadan önce taslak proje faturasında belirli işlemler gerçekleştirildiğinde oluşturulur.

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
Elde tutulan tutar veya avans faturalama </p>
            </td>
            <td width="408" valign="top">
                <p>
Faturalı satış fiili türü, <strong>Elde kalan</strong> avans veya elde kalan üzerindeki tutar için oluşturulur.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Mutabakat için kullanılacak olan hizmetli veya avansın negatif tutarının faturalandırılmamış satışları.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Bir faturada bir elde kalanı veya avansı tamamen uzlaştırdıktan sonra.
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
Bu faturadaki tutar için faturalı satış fiili.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Bir faturada bir elde kalanı veya avansı kısmen uzlaştırdıktan sonra.
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
Bu faturadaki tutar için faturalı satış fiili.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Gelecek faturalarda mutabakat için kullanılacak olan hizmetli veya avansın negatif tutarının faturalandırılmamış satışları.
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
Düzenlenen fatura satırı ayrıntısı üzerindeki saat ve tutar için ücretlendirilebilen yeni bir faturalanmamış satış fiili, satışların fiilinin tersine çevrilmesi ve eşdeğer faturalı satışların fiili.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Düzenlenen fatura satırı ayrıntısı üzerindeki doğrulanan rakamlar çıkarıldıktan sonra kalan saat ve tutar için ücretlendirilemeyen yeni bir faturalanmamış satış fiili, satışların fiilinin tersine çevrilmesi ve eşdeğer faturalı satışların fiili.
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
Orijinal gider onayının miktarı ve tutarı için faturalandırılmış satış fiili </p>
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
Taslak faturasında herhangi bir düzenleme yapmadan bir malzeme hareketini faturalama.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Orijinal malzeme kullanımı onayındaki miktar ve tutar için faturalanmamış satışı tersine çevirme işlemi.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Orijinal malzeme kullanımı onayındaki miktar ve tutar için faturalanmış satış gerçek değeri.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Miktarı azaltmak için düzenlenen bir malzeme hareketini faturalama.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Orijinal zaman onayındaki miktar ve tutar için faturalanmamış satışı tersine çevirme işlemi.
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
Miktarı artırmak için düzenlenen bir malzeme hareketini faturalama.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Orijinal malzeme kullanımı onayındaki miktar ve tutar için faturalanmamış satışı tersine çevirme işlemi.
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
        <tr>
            <td width="216" valign="top">
                <p>
Ürün tabanlı sözleşme satırını faturalandırma.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Faturalanan bir satış, ürün tabanlı sözleşme satırından gelen miktar ve tutar içeren, ürün satırı için fiili olarak yapılır.
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
