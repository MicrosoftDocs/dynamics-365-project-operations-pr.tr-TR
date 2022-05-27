---
title: Project Operations'ta satıcı ve satınalma fiyatı listesi yönetimi
description: Bu konu, taşeronluk için satıcı verileri ve satınalma fiyat listeleri oluşturmanıza ve korumanıza yardımcı olacak bilgiler sağlar.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9c76d5ca45e03167f0ccfd2c1c7013f91fef0f86
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576754"
---
# <a name="vendor-and-purchase-price-list-management-in-project-operations"></a>Project Operations'ta satıcı ve satınalma fiyatı listesi yönetimi

[!include [banner](../../includes/dataverse-preview.md)]

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

## <a name="vendors-in-project-operations"></a>Project Operations'ta Satıcılar

Microsoft Dynamics 365 Project Operations'ta satıcı hesaplarının **Satıcı** veya **Tedarikçi** ilişki türü vardır. Taşeronda satıcı olarak yalnızca bu ilişki türlerinden birine sahip bir firma kaydı seçebilirsiniz.

Bir veya daha fazla satınalma fiyat listesini satıcı kaydıyla ilişkilendirebilirsiniz. Ancak, satıcı kaydıyla ilişkili her satınalma fiyat listesinin ayrı bir tarih efektivitesi olmalıdır. Project Operations, satınalma fiyat listeleri için çakışan geçerlilik tarihlerini desteklemez.

Varsayılan olarak, satıcı kaydındaki aşağıdaki alanlar ve kavramlar satıcı için oluşturulan herhangi bir taşeron için kullanılır:

- Ödeme koşulları
- Fatura İlgili Kişi
- Birincil ilgili kişi

    > [!NOTE]
    > Varsayılan olarak, satıcının birincil ilgili kişisi taşeronun satıcı hesabı yöneticisi olarak kullanılır.

- Currency
- Geçerli satın Alma Fiyat Listeleri

## <a name="purchase-price-lists-in-project-operations"></a>Project Operations'ta satınalma fiyat listeleri

**Bağlam** alanının **Satınalma** olarak ayarlandığı bir fiyat listesi, satınalma fiyat listesi olarak kabul edilir. Satınalma fiyat listeleri, zaman, gider ve malzemeler için satınalma oranları kataloğunu temsil etmek üzere tanımlanabilir. Satınalma fiyat listeleri, Project Operations'ta maliyet ve satış fiyat listelerine benzer. Aşağıdaki kavramlar, maliyet ve satış fiyat listelerine uygulandığı şekilde satınalma fiyat listeleri için de geçerlidir:

- **Tarih geçerliliği** – Satın alma fiyat listeleri tarih efektivitesi vardır. Tarih efektivitesi, her fiyat listesindeki başlangıç tarihi ve bitiş tarihi alanlarıyla temsil edilir. Başlangıç tarihi ile bitiş tarihi arasındaki saat, geçerlilik dönemi olan tarihtir.
- **Para Birimi** – Fiyat listesi başlığındaki para birimi, satınalma fiyatlarının katalogdaki işçilik, gider kategorileri ve ürünler için ifade edildiği para birimi olarak kullanılır.
- **Varsayılan zaman birimi** – Varsayılan zaman birimi satınalmalar için işçilik fiyatlarını ifade eder. Fiyat listesindeki zaman birimi alanı yalnızca varsayılan bir değer sağlamak için kullanılır. Bu değer tek tek rol fiyatı satırlarında değiştirilebilir.

Satınalma fiyat listeleri, satıcı kayıtlarına proje fiyat listeleri olarak bilinen ilişkilendirmeler olarak iliştirilebilir. Bu fiyat listeleri, taşeron satırlarına varsayılan fiyatları girmek için kullanılır. Varsayılan olarak, bir satıcı kaydına birden çok satınalma fiyat listesi iliştirildiğinde, satıcı için oluşturulan taşeronlar için en geçerli fiyat listesi kullanılır. Yalnızca **Bağlam** alanının **Satınalma** olarak ayarlandığı fiyat listeleri satıcı kayıtlarına iliştirilebilir.

### <a name="subcontract-specific-purchase-price-lists"></a>Taşerona özel satınalma fiyat listeleri

Satınalma fiyat listeleri, alt sözleşmelere proje fiyat listeleri olarak bilinen ilişkilendirmeler olarak iliştirilebilir. Bu fiyat listeleri, taşeron satırlarına varsayılan fiyatları girmek için kullanılır. Varsayılan olarak, bir taşerona birden çok satınalma fiyatı listesi eklendiğinde, her birinin ayrı tarih efektivitesine sahip olması gerekir. Project Operations, çakışan tarih efektivitesine sahip satınalma fiyat listelerini desteklemez. Yalnızca **Bağlam** alanının **Satınalma** olarak ayarlandığı fiyat listeleri alt sözleşmelere iliştirilebilir.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
