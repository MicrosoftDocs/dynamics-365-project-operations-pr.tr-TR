---
title: Tahminler ve gerçek değerler için maliyet fiyatlarını çözümleme
description: Bu konu, tahminler ve fiili olarak maliyet fiyatlarının nasıl çözüldüğü hakkında bilgi sağlar.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c447e725753d738662f33cc9a5f20ec1a72b2e18
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119723"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>Tahminler ve gerçek değerler için maliyet fiyatlarını çözümleme

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Maliyet fiyatlarını ve tahminler ve fiili matların maliyet fiyat listesini çözmek için sistem, ilgili projenin **Tarih**, **Para Birimi** ve **Sözleşme Birimi** alanlarındaki bilgileri kullanır. Maliyet fiyat listesi çözüldükten sonra, uygulama maliyet oranını çözer.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Zaman için fiili ve tahmin satırlarındaki maliyet oranlarını çözme

Zaman için tahmin satırları, projedeki zaman ve kaynak atamaları için teklif ve sözleşme satırı ayrıntılarına bakın.

Bir maliyet fiyat listesi çözüldükten sonra, sistem Fiyat listesinde rol fiyat satırları ile maç için Zaman için tahmin satırında **Rol**, **Kaynak Şirketi** ve **Kaynak Birimi** alanlarını kullanır. Bu eşleşme, işçilik maliyeti için hazır fiyatlandırma boyutları kullandığınızı varsayar. Sistemi, **Rol**, **Kaynak Şirketi** ve **Kaynak Ünitesi** yerine veya buna ek olarak alanları eşleşecek şekilde yapılandırırsanız, eşleşen bir rol fiyat satırını almak için farklı bir kombinasyon kullanılır. Uygulama Rol için bir maliyet oranı olan bir rol fiyat satırı bulursa **Rol**, **Kaynak Şirket** ve **Kaynak Birimi** kombinasyonu, bu varsayılan maliyet oranıdır. Uygulama **Rol** ile eşleşmiyorsa **Kaynak Şirket**, ve **Kaynak Birimi** değerleri, o zaman eşleşen bir rol ile rol fiyat satırları alır, ancak **Kaynak Birimi** null değerleri. Eşleşen bir rol fiyat kaydı na sahip olduktan sonra, maliyet oranı bu kayıttan varsayılan olarak çıkar. 

> [!NOTE]
> **Rol**, **Kaynak Şirketi** ve **Kaynak Birimi**'nin farklı bir önceliklendirmesini yapılandırırsanız veya daha yüksek önceliğe sahip başka boyutlara sahipseniz, bu davranış buna göre değişecektir. Sistem, öncelik sırasına göre fiyatlandırma boyutu değerlerinin her biriyle eşleşen değerlerle, en son gelen boyutlar için null değerlere sahip satırlarla rol fiyat kayıtlarını alır.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Gider için fiili ve tahmin satırlarındaki maliyet oranlarını çözme

Gider için tahmin satırları, projedeki giderler ve gider tahmini satırları için teklif ve sözleşme satırı ayrıntılarına bakın.

Bir maliyet fiyat listesi çözüldükten sonra, sistem Fiyat listesinde rol fiyat satırları ile maç için Zaman için tahmin satırında **Ktegori**, **Ünite** ve **Kategori fiyatı** alanlarını kullanır. Sistem **Kategori** ve **Birim** alan birleşimi için maliyet oranına sahip bir kategori fiyat satırı bulursa, maliyet oranı varsayılan olarak. Sistem **Kategori** ve **Birim** değerleriyle eşleşemezse veya eşleşen bir kategori fiyat satırı bulabiliyorsa ancak fiyatlandırma yöntemi **Birim Başına Fiyat** değilse, maliyet oranı sıfır(0) olarak varsayılan olarak verilir.
