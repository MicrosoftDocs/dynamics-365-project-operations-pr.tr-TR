---
title: Kaynak tahminleri
description: Bu konuda, Project Operations'ta kaynak tahminlerinin nasıl hesaplanacağı hakkında bilgiler sağlanmaktadır.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2ebde2b3c5bcfb5faa02ee476065ac34b1953432
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086244"
---
# <a name="resource-estimates"></a>Kaynak tahminleri

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Kaynak tahminleri, uygun fiyatlandırma boyutlarıyla birlikte iş kırılım yapısında tanımlanan zaman aşamalı çalışmadan gelir. Genellikle hesaplama **her rol için oran/sa x saat** olarak yapılır. Her bir kaynağın zaman aşamalı çalışması, kaynak atama kaydında depolanır. Fiyatlandırma, önceden tanımlanmış bir fiyat listesinde depolanır. Birim dönüştürme, uygun fiyat listesine göre uygulanır.

![Kaynak Tahminleri](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Varsayılan maliyet fiyatı ve maliyet para birimi

Maliyet fiyatları varsayılan olarak Kuruluş Biriminden alınır.

## <a name="default-bill-rate-and-sales-currency"></a>Varsayılan fatura oranı ve satış para birimi

Satış fiyatları her anlaşma için bir kere uygulanır. Varsayılan satış fiyatı listesi hiyerarşisi aşağıdaki gibidir:

1. Kuruluş
2. Müşteri
3. Teklif/sözleşme
