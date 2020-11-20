---
title: Tahminlerde ve gerçek değerlerde maliyet fiyatlarını çözümleyin - lite
description: Bu konu, tahminler ve fiili olarak maliyet fiyatlarının nasıl çözüldüğü hakkında bilgi sağlar.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3fedf7b577e2372fb10ea85ea1e3caa9bf2f5ad0
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176815"
---
# <a name="resolve-cost-prices-on-estimates-and-actuals---lite"></a>Tahminlerde ve gerçek değerlerde maliyet fiyatlarını çözümleyin - lite

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Maliyet fiyatlarını ve tahminler ve fiili matların maliyet fiyat listesini çözmek için sistem, ilgili projenin **Tarih**, **Para Birimi** ve **Sözleşme Birimi** alanlarındaki bilgileri kullanır. Maliyet fiyat listesi çözüldükten sonra, uygulama maliyet oranını çözer.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Zaman için fiili ve tahmin satırlarındaki maliyet oranlarını çözme

Zaman için tahmin satırları, projedeki zaman ve kaynak atamaları için teklif ve sözleşme satırı ayrıntılarına bakın.

Bir maliyet fiyat listesi çözüldükten sonra, sistem Fiyat listesinde rol fiyat satırları ile eşleşme için Zaman için tahmin satırında **Rol** ve **Kaynak Birimi** alanlarını kullanır. Bu eşleşme, işçilik maliyeti için hazır fiyatlandırma boyutları kullandığınızı varsayar. Sistemi, **Rol** ve **Kaynak Birimi** yerine veya buna ek olarak alanları eşleşecek şekilde yapılandırırsanız, eşleşen bir rol fiyat satırını almak için farklı bir kombinasyon kullanılır. Uygulama Rol için bir maliyet oranı olan bir rol fiyat satırı bulursa **Rol** ve **Kaynak Birimi** kombinasyonu, bu varsayılan maliyet oranıdır. Uygulama **Rol** ile eşleşmiyorsa **Kaynak Birimi** değerleri, o zaman eşleşen bir rol ile rol fiyat satırları alır, ancak **Kaynak Birimi** null değerleri. Eşleşen bir rol fiyat kaydı na sahip olduktan sonra, maliyet oranı bu kayıttan varsayılan olarak çıkar. 

> [!NOTE]
> **Rol** ve **Kaynak Birimi**'nin farklı bir önceliklendirmesini yapılandırırsanız veya daha yüksek önceliğe sahip başka boyutlara sahipseniz, bu davranış buna göre değişecektir. Sistem, öncelik sırasına göre fiyatlandırma boyutu değerlerinin her biriyle eşleşen değerlerle, en son gelen boyutlar için null değerlere sahip satırlarla rol fiyat kayıtlarını alır.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Gider için fiili ve tahmin satırlarındaki maliyet oranlarını çözme

Gider için tahmin satırları, projedeki giderler ve gider tahmini satırları için teklif ve sözleşme satırı ayrıntılarına bakın.

Bir maliyet fiyat listesi çözüldükten sonra, sistem Fiyat listesinde rol fiyat satırları ile maç için Zaman için tahmin satırında **Ktegori**, **Ünite** ve **Kategori fiyatı** alanlarını kullanır. Sistem **Kategori** ve **Birim** alan birleşimi için maliyet oranına sahip bir kategori fiyat satırı bulursa, maliyet oranı varsayılan olarak. Sistem **Kategori** ve **Birim** değerleriyle eşleşemezse veya eşleşen bir kategori fiyat satırı bulabiliyorsa ancak fiyatlandırma yöntemi **Birim Başına Fiyat** değilse, maliyet oranı sıfır(0) olarak varsayılan olarak verilir.
