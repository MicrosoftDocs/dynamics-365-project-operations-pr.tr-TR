---
title: Gider raporlarını deftere nakletme
description: Bu makalede gider raporlarının nasıl deftere nakledileceği açıklanmaktadır.
author: ramagadu
ms.date: 08/12/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d0ae4559a08553236158a663513401cb38cbe28f
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524894"
---
# <a name="post-expense-reports"></a>Gider raporlarını deftere nakletme

Gider raporu onaylanıp genel yevmiye defterine aktarıldıktan sonra, deftere nakledilebilir. Gider raporunu deftere naklettiğinizde, katma değer vergisi (KDV) iade edilebilecek giderler belirlenir. KDV ödemelerini doğrulama ve geri alma görevi gider raporunu doğrulamaktan sorumlu olan çalışana atanır.

Gider raporundaki giderler, çalışanın bağlı olduğu şirketten başka bir şirketten tahsil edilirse bu giderlerin borçlusu ve alacaklısı olan iki şirketi de doğrulamanız gerekir. Örneğin, gider raporunu gönderen çalışan, DAT şirketinde çalışmaktadır ancak bir gideri DIR şirketine faturalamıştır. Bu durumda, DAT giderin alacaklısı, DIR şirketiyse giderin borçlusudur. Bu yevmiye defteri satırlarını doğruladıktan sonra, bu gider satırlarını genel günlüğe nakledebilirsiniz.

Gider raporunu deftere nakletmek için **Onaylanmış gider raporları** sayfasında, gider raporunu seçin ve ardından Eylem Bölmesi'nde **Deftere Naklet** seçeneğini belirleyin.

Ayrıca listedeki tüm gider raporlarını aynı anda deftere nakledebilirsiniz. Tüm gider raporlarını seçin ve ardından **Deftere Naklet** seçeneğini belirleyin.

## <a name="enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature"></a>Nakit ödeme yöntemi için satıcı para birimi cinsinden gider borcunu deftere nakledilebilme özelliğini etkinleştirme

**Nakit ödeme yöntemi için satıcı para birimi cinsinden gider borcunu deftere nakledilebilme** özelliği, gider raporlarının nakit ödeme yöntemi için satıcı para biriminde deftere nakledilmesini sağlar.

Şu anda nakit giderleri gönderdiğinizde, gider raporları muhasebe para birimi cinsinden nakledilir. İşlem para birimi, muhasebe para birimi ve satıcı para birimi arasında tutar dönüştürmesi nedeniyle, giderin işlem tarihi ve gerçek ödeme tarihinin farklı döviz kurları varsa satıcılara yanlış tutar ödenir.

Bu özellik, gider raporu deftere nakledildiğinde satıcı bakiyesinin satıcı para birimi cinsinden kaydedilmesini sağlar.

1. **Çalışma alanları**\>**Özellik Yönetimi**'ne gidin.
2. Listede **Nakit ödeme yöntemi için satıcı para birimi cinsinden gider borcunu deftere nakledilebilme** özelliğini bulup seçin ve ardından **Şimdi etkinleştir**'i seçin.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
