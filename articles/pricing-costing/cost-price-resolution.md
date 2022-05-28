---
title: Tahminler ve gerçek değerler için maliyet fiyatlarını çözümleme
description: Bu konu, tahminler ve fiili olarak maliyet fiyatlarının nasıl çözüldüğü hakkında bilgi sağlar.
author: rumant
ms.date: 04/09/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7395a1845f4a895efbabda36ba3b2a2f3c1eea52
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587932"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>Tahminler ve gerçek değerler için maliyet fiyatlarını çözümleme

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Maliyet fiyatlarını ve tahminler ve fiili matların maliyet fiyat listesini çözmek için sistem, ilgili projenin **Tarih**, **Para Birimi** ve **Sözleşme Birimi** alanlarındaki bilgileri kullanır. Maliyet fiyat listesi çözüldükten sonra, uygulama maliyet oranını çözer.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Zaman için fiili ve tahmin satırlarındaki maliyet oranlarını çözme

Zaman için tahmin satırları, projedeki zaman ve kaynak atamaları için teklif ve sözleşme satırı ayrıntılarına bakın.

Bir maliyet fiyat listesi çözüldükten sonra, sistem Fiyat listesinde rol fiyat satırları ile maç için Zaman için tahmin satırında **Rol**, **Kaynak Şirketi** ve **Kaynak Birimi** alanlarını kullanır. Bu eşleşme, işçilik maliyeti için hazır fiyatlandırma boyutları kullandığınızı varsayar. Sistemi, **Rol**, **Kaynak Şirketi** ve **Kaynak Ünitesi** yerine veya buna ek olarak alanları eşleşecek şekilde yapılandırırsanız, eşleşen bir rol fiyat satırını almak için farklı bir kombinasyon kullanılır. Uygulama Rol için bir maliyet oranı olan bir rol fiyat satırı bulursa **Rol**, **Kaynak Şirket** ve **Kaynak Birimi** kombinasyonu, bu varsayılan maliyet oranıdır. Uygulama; **Rol**, **Kaynak Atayan Şirket** ve **Kaynak Belirleme Birimi** değerlerinin birleşimiyle tam olarak eşleşmiyorsa rol değeri eşleşen ancak **Kaynak Belirleme Birimi** ve **Kaynak Atayan Şirket** değerleri null olan bir rol fiyat satırı alır. Eşleşen rol fiyatı değerine sahip eşleşen bir rol fiyatı kaydı bulunursa maliyet oranı varsayılan olarak bu kayıttan alınır. 

> [!NOTE]
> **Rol**, **Kaynak Şirketi** ve **Kaynak Birimi**'nin farklı bir önceliklendirmesini yapılandırırsanız veya daha yüksek önceliğe sahip başka boyutlara sahipseniz, bu davranış buna göre değişecektir. Sistem rol fiyatı kayıtlarını, öncelik sırasında en son kullanılan boyutlar için null değerlere sahip satırlarla öncelik sırasına göre, her bir fiyatlandırma boyutu değeriyle eşleşen değerlerle alır.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Gider için fiili ve tahmin satırlarındaki maliyet oranlarını çözme

Gider için tahmin satırları, projedeki giderler ve gider tahmini satırları için teklif ve sözleşme satırı ayrıntılarına bakın.

Bir maliyet fiyat listesi çözüldükten sonra, sistem Fiyat listesinde rol fiyat satırları ile maç için Zaman için tahmin satırında **Ktegori**, **Ünite** ve **Kategori fiyatı** alanlarını kullanır. Sistem **Kategori** ve **Birim** alan birleşimi için maliyet oranına sahip bir kategori fiyat satırı bulursa, maliyet oranı varsayılan olarak. Sistem **Kategori** ve **Birim** değerleriyle eşleşemezse veya eşleşen bir kategori fiyat satırı bulabiliyorsa ancak fiyatlandırma yöntemi **Birim Başına Fiyat** değilse, maliyet oranı sıfır(0) olarak varsayılan olarak verilir.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Malzemenin gerçek ve tahmin satırlarında maliyet oranlarını çözme

Malzemenin tahmin satırları, malzemelerin teklif ve sözleşme satırı ayrıntılarına ve projedeki malzeme tahmin satırları anlamına gelir.

Maliyet fiyatı listesi çözüldükten sonra, sistem çözülmüş fiyat listesindeki **Fiyat Listesi Öğeleri** satırlarına uyacak bir malzeme tahmini için tahmin satırındaki **Ürün** ve **Birim** alanlarının bir birleşimini kullanır. Sistem, **Ürün** ve **Birim** alan birleşimi için maliyet oranına sahip bir ürün fiyatı satırı bulursa maliyet oranı varsayılan olarak alınır. Sistem, **Ürün** ve **Birim** değerlerini eşleştiremiyorsa birim maliyet varsayılan olarak sıfır olur. Bu varsayılan, eşleşen bir fiyat listesi öğesi satırı varsa ancak fiyatlandırma yöntemi üründe tanımlı olmayan standart bir maliyeti veya geçerli maliyeti temel alıyorsa da ortaya çıkar.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
