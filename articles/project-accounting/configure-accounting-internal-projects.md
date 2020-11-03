---
title: Dahili projeler için muhasebeyi yapılandırma
description: Bu konu, proje işlemlerinde dahili projeler için muhasebe uygulamaları ayarlama hakkında bilgi sağlar.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 504e7481cb2aee6310cb4ace2d0791d1c7fe360d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086258"
---
# <a name="configure-accounting-for-internal-projects"></a>Dahili projeler için muhasebeyi yapılandırma

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Dahili projeler, şirketlerin müşteriye faturalanmayan faaliyetlerle ilgili maliyeti izlemesine olanak verir. Dahili proje örnekleri şunlardır:

- Mobil uygulama gibi bir ürün geliştirme ve geliştirmeyle ilişkili maliyeti izleme.
- Satış öncesi süresi ve gideri yönetme. Bu satış öncesi dahili proje, teklif kazanıldığında daha sonra faturalandırılabilir bir projeye dönüştürülebilir.

Dynamics 365 Project Operations'da bir sözleşmeyle ilişkilendirilmemiş herhangi bir proje dahili olarak kabul edilir. Proje maliyet ve gelir profilleri, proje için muhasebe kurallarını belirlemek için kullanılmaz. Dahili proje maliyeti her zaman kar ve zarar ilkeleri kullanılarak deftere nakledilir. **Defter Nakli Kurulumu** sayfasında deftere nakiller için genel muhasebe hesapları tanımlanır.

- Zaman hareketleri, **Maliyet** hesabının borçlandırılması ve **Bordro tahsisatı** hesabında alacaklandırılması yoluyla deftere nakledilir.
- Gider hareketleri, **Maliyet** hesabının borçlandırılması ve **Gider için ofset hesabı** alacaklandırılması yoluyla deftere nakledilir.

Hareketler projeye nakledildikten sonra, proje bir proje sözleşmesiyle ilişkilendirilmişse, sistem tüm birikmiş hareketleri ters çevirir ve yeni faturalandırılabilir hareketler oluşturur. Faturalandırılabilir hareketler, ilgili proje maliyet ve gelir profili ' nde tanımlanan hesap kurallarını izler.


