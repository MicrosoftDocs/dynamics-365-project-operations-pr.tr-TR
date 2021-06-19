---
title: Proje tahminleri ve gerçek değerlerde maliyet fiyatlarını çözümleme
description: Bu konu, proje tahminleri ve gerçek değerlerinde maliyet fiyatlarının nasıl çözümleneceği hakkında bilgi sağlar.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6b42bc97251aec7259d314fe51b3a012edf597aa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004420"
---
# <a name="resolve-cost-prices-on-project-estimates-and-actuals"></a>Proje tahminleri ve gerçek değerlerde maliyet fiyatlarını çözümleme 

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

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Malzemenin gerçek ve tahmin satırlarında maliyet oranlarını çözme

Malzemenin tahmin satırları, malzemelerin teklif ve sözleşme satırı ayrıntılarına ve projedeki malzeme tahmin satırları anlamına gelir.

Maliyet fiyatı listesi çözüldükten sonra, sistem çözülmüş fiyat listesindeki **Fiyat Listesi Öğeleri** satırlarına uyacak bir malzeme tahmini için tahmin satırındaki **Ürün** ve **Birim** alanlarının bir birleşimini kullanır. Sistem, **Ürün** ve **Birim** alan birleşimi için maliyet oranına sahip bir ürün fiyatı satırı bulursa maliyet oranı varsayılan olarak alınır. Sistem, **Ürün** ve **Birim** değerlerini eşleştiremiyorsa veya eşleşen bir fiyat listesi öğesi satırı bulmasına rağmen fiyatlandırma yöntemi Standart maliyeti veya Geçerli maliyeti temel alıyor ve bunların ikisi de üründe tanımlı değilse birim maliyeti sıfır olarak varsayılır.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
