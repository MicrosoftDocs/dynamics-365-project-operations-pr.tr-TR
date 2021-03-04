---
title: Tahminlerde ve gerçek değerlerde maliyet fiyatlarını çözümleyin - lite
description: Bu konu, tahminler ve fiili olarak maliyet fiyatlarının nasıl çözüldüğü hakkında bilgi sağlar.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d2afaa2231f4044dbcbfa24b91aec39289275a91
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764618"
---
# <a name="resolve-cost-prices-on-estimates-and-actuals---lite"></a>Tahminlerde ve gerçek değerlerde maliyet fiyatlarını çözümleyin - lite

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Maliyet fiyatlarını ve tahminler ve fiili matların maliyet fiyat listesini çözmek için sistem, ilgili projenin **Tarih**, **Para Birimi** ve **Sözleşme Birimi** alanlarındaki bilgileri kullanır. Maliyet fiyat listesi çözüldükten sonra, uygulama maliyet oranını çözer.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Zaman için fiili ve tahmin satırlarındaki maliyet oranlarını çözme

Zaman için tahmin satırları, projedeki zaman ve kaynak atamaları için teklif ve sözleşme satırı ayrıntılarına bakın.

Maliyet fiyatı listesi çözümlendikten sonra Zaman için tahmin satırındaki **Rol** ve **Kaynak Belirleme Birimi** alanları, fiyat listesindeki rol fiyatı satırlarıyla eşleştirilir. Bu eşleştirme, işçilik maliyeti için standart fiyatlandırma boyutlarını kullandığınızı varsayar. Sistemi, **Rol** ve **Kaynak Birimi** yerine veya buna ek olarak alanları eşleşecek şekilde yapılandırırsanız, eşleşen bir rol fiyat satırını almak için farklı bir kombinasyon kullanılır. Uygulama Rol için bir maliyet oranı olan bir rol fiyat satırı bulursa **Rol** ve **Kaynak Birimi** kombinasyonu, bu varsayılan maliyet oranıdır. Uygulama **Rol** ile eşleşmiyorsa **Kaynak Birimi** değerleri, o zaman eşleşen bir rol ile rol fiyat satırları alır, ancak **Kaynak Birimi** null değerleri. Eşleşen bir rol fiyat kaydı na sahip olduktan sonra, maliyet oranı bu kayıttan varsayılan olarak çıkar. 

> [!NOTE]
> **Rol** ve **Kaynak Birimi**'nin farklı bir önceliklendirmesini yapılandırırsanız veya daha yüksek önceliğe sahip başka boyutlara sahipseniz, bu davranış buna göre değişecektir. Sistem, öncelik sırasına göre fiyatlandırma boyutu değerlerinin her biriyle eşleşen değerlerle, en son gelen boyutlar için null değerlere sahip satırlarla rol fiyat kayıtlarını alır.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Gider için fiili ve tahmin satırlarındaki maliyet oranlarını çözme

Gider için tahmin satırları, projedeki giderler ve gider tahmini satırları için teklif ve sözleşme satırı ayrıntılarına bakın.

Maliyet fiyatı listesi çözümlendikten sonra sistem, gider tahmini satırındaki **Kategori** ve **Birim** alanlarının bir birleşimini çözümlenen fiyat listesindeki **Kategori Fiyatı** satırlarıyla eşleştirmek için kullanır. Sistem **Kategori** ve **Birim** alan birleşimi için maliyet oranına sahip bir kategori fiyat satırı bulursa, maliyet oranı varsayılan olarak. Sistem, **Kategori** ve **Birim** değerleriyle eşleşmiyorsa veya sistem, eşleşen bir kategori fiyatı satırı bulmasına rağmen fiyatlandırma yöntemi **Birim Fiyatı** değilse maliyet oranı varsayılan olarak sıfır (0) olur.
