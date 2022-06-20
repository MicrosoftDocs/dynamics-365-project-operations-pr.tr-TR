---
title: Alt sözleşme kapsamındaki bileşenler için süre, gider ve malzeme kullanımını kaydetme
description: Bu makale, alt sözleşme bileşenlerinden projelerde kaydedilen zaman, gider ve malzeme kullanımının Microsoft Dynamics 365 Project Operations tarafından nasıl izlendiğini açıklar.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1c05b941fb51c8b56422e3b5d3868c9b69197187
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927674"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Alt sözleşme bileşenleri için projelerde kayıt süresi, giderler ve malzeme kullanımı

[!include [banner](../../includes/dataverse-preview.md)]

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Bu makale, alt sözleşme bileşenlerinden projelerde kaydedilen zaman, gider ve malzeme kullanımının Microsoft Dynamics 365 Project Operations tarafından nasıl izlendiğini açıklar.

## <a name="costing-for-subcontractor-time-on-projects"></a>Projelerde alt sözleşme süresi için maliyet
Project Operations'da sözleşmeli çalışanlar, projelerde çalışanlarla benzer şekilde zaman kaydedebilir. Projelere ve/veya proje görevlerine zaman girerken, sözleşmeli çalışan belirli bir alt sözleşme ve alt sözleşme satırı seçebilir.

Sözleşmeli çalışanlar tarafından gönderilen süre onaylandığında, proje maliyeti, alt sözleşmedeki satınalma fiyatı listesinin **Rol fiyatları** bölümünde bu sözleşmeli çalışan kaynağı için ayarlanan birim maliyet oranı kullanılarak kaydedilir.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Projelerdeki alt sözleşme giderlerinin maliyeti
Projelerde oluşan giderleri girerken, gider girişinde bir alt sözleşme ve alt sözleşme satırı seçebilirsiniz. 

Bu gider girişi gönderildiğinde ve onaylandığında, gider maliyeti, alt sözleşmedeki satınalma fiyatı listesinin **Kategori fiyatları** bölümünde bu hareket kategorisi için ayarlanan birim maliyete göre projeye kaydedilir.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Projelerdeki alt sözleşme malzemelerinin maliyeti
Projelerde malzeme kullanımı girerken, malzeme kullanım günlüğünde bir alt sözleşme ve alt sözleşme satırı seçebilirsiniz. Malzeme kullanım günlüğü gönderildiğinde ve onaylandığında, malzeme maliyeti, alt sözleşme fiyat listesinin **Fiyat listesi maddeleri** bölümünde bu ürün için ayarlanan birim maliyete göre projeye kaydedilir.

Malzeme kullanımı, projelerdeki yazma ürünleri için de kaydedilebilir. Bu tür malzeme kullanımı bir alt sözleşme ve alt sözleşme satırına da bağlanabilir. Serbest ürün ekleme için malzeme kullanımını kaydederken, serbest ürün ekleme birim başına maliyetini girmeniz gerekir. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
