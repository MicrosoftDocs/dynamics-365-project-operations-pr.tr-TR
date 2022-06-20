---
title: Dahili projeler için muhasebeyi yapılandırma
description: Bu makalede, Project Operations'ta dahili projeler için muhasebe uygulamalarının nasıl ayarlanacağı konusunda bilgiler yer alır.
author: sigitac
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 7fc2b7247da699a194688b18aa0a695b06cc44c6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919486"
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
