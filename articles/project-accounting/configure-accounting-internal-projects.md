---
title: Dahili projeler için muhasebeyi yapılandırma
description: Bu konu, proje işlemlerinde dahili projeler için muhasebe uygulamaları ayarlama hakkında bilgi sağlar.
author: sigitac
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ad8b974ef75cb0a4e43af0aa254cec1bbcab154a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012880"
---
# <a name="configure-accounting-for-internal-projects"></a>Dahili projeler için muhasebeyi yapılandırma

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Dahili projeler, şirketlerin müşteriye faturalanmayan faaliyetlerle ilgili maliyeti izlemesine olanak verir. Dahili proje örnekleri şunlardır:

- Mobil uygulama gibi bir ürün geliştirme ve geliştirmeyle ilişkili maliyeti izleme.
- Satış öncesi süresi ve gideri yönetme. Bu satış öncesi dahili proje, teklif kazanıldığında daha sonra faturalandırılabilir bir projeye dönüştürülebilir.

Dynamics 365 Project Operations'ta bir sözleşmeyle ilişkili olmayan projeler, dahili olarak görülür. Proje maliyet ve gelir profilleri, proje için muhasebe kurallarını belirlemek için kullanılmaz. Dahili proje maliyeti her zaman kar ve zarar ilkeleri kullanılarak deftere nakledilir. **Defter Nakli Kurulumu** sayfasında deftere nakiller için genel muhasebe hesapları tanımlanır.

- Zaman hareketleri, **Maliyet** hesabının borçlandırılması ve **Bordro tahsisatı** hesabında alacaklandırılması yoluyla deftere nakledilir.
- Gider hareketleri, **Maliyet** hesabının borçlandırılması ve **Gider için ofset hesabı** alacaklandırılması yoluyla deftere nakledilir.
- Madde hareketleri, **Maliyet** hesabına alacak olarak kaydedilip **Maliyet - Madde** hesabına ödenerek deftere nakledilir.

Hareketler projeye nakledildikten sonra, proje bir proje sözleşmesiyle ilişkilendirilmişse, sistem tüm birikmiş hareketleri ters çevirir ve yeni faturalandırılabilir hareketler oluşturur. Faturalandırılabilir hareketler, ilgili proje maliyet ve gelir profili ' nde tanımlanan hesap kurallarını izler.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
