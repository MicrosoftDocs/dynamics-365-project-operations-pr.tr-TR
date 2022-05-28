---
title: Bir proje için satınalma siparişleri
description: Bu makalede, bir projeyle ilgili satınalma siparişleri oluşturmak için kullanabileceğiniz çeşitli yöntemler açıklanmaktadır. Kullanacağınız yöntem, satınalma siparişi amacına ve satın alınan maddelerin ne zaman tüketilip bir projeye ücretlendirildiğine bağlıdır.
author: Yowelle
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 49ca1f9af715dcb1beb7932f7c484abc7b183dcd
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685034"
---
# <a name="purchase-orders-for-a-project"></a>Bir proje için satınalma siparişleri

[!include [banner](../includes/banner.md)]

Bu makalede, bir projeyle ilgili satınalma siparişleri oluşturmak için kullanabileceğiniz çeşitli yöntemler açıklanmaktadır. Kullanacağınız yöntem, satınalma siparişi amacına ve satın alınan maddelerin ne zaman tüketilip bir projeye ücretlendirildiğine bağlıdır.

### <a name="methods-for-creating-a-purchase-order"></a>Satınalma siparişi oluşturma yöntemleri

Proje yönetimi ve muhasebe modülünde bir satın alma siparişi oluşturmak için aşağıdaki yöntemlerden birini kullanabilirsiniz. Satınalma siparişinin amacı satın alınan maddelerin ne zaman tüketilip bir projeye ne zaman ücretlendirildiğini belirler.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Yöntem</th>
<th>Amaç</th>
<th>Maddelerin tüketimi</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Bir projeden doğrudan satınalma siparişi oluşturun.</td>
<td>Bir proje üzerinde tüketim amacıyla harici bir satıcıdan madde satın almak için bu yöntemi kullanın. Satınalma siparişi iki şekilde oluşturulabilir:
<ul>
<li>Projenin kendisinden. Bu durumda, proje satınalma siparişi için önceden tanımlanmıştır.</li>
<li>Proje satın alma siparişine giderek. Satınalma siparişi oluşturmak için hem satıcıyı, hem de projeyi seçmeniz gerekir.</li>
</ul></td>
<td>Maddeler, satıcı faturası güncelleştirildiğinde tüketilir.</td>
</tr>
<tr class="even">
<td>Satış siparişinden bir satınalma siparişi oluşturun.</td>
<td>Bir projeden satış siparişi oluşturduğunuzda, maddeleri satın almak için bu yöntemi kullanın.</td>
<td>Maddeler, satış siparişi müşteriye faturalandığı zaman tüketilir.</td>
</tr>
<tr class="odd">
<td>Bir madde gereksiniminden satınalma siparişi oluşturun.</td>
<td>Bir projeden madde gereksinimi oluşturduğunuzda, maddeleri satın almak için bu yöntemi kullanın.</td>
<td>Maddeler, madde gereksinim sevk irsaliyesi güncelleştirildiğinde tüketilir.</td>
</tr>
</tbody>
</table>

> [!NOTE] 
> Satıcı faturasını veya sevk irsaliyesini güncelleştirdiğinizde, madde gereksiniminden sevk irsaliyesini güncelleştirmeniz istenir.

Daha fazla bilgi için, bkz. [Madde gereksiniminden satınalma siparişindeki maddeleri alma](tasks/receive-items-purchase-order-item-requirement.md).



[!INCLUDE[footer-include](../includes/footer-banner.md)]