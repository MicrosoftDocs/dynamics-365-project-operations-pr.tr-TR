---
title: Ürün tabanlı teklif satırlarına genel bakış - lite
description: Bu konu ürün tabanlı teklif satırlarıyla çalışma ilgili bilgi sağlar.
author: rumant
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6aa428c486f149308ad078f9d7a80a0be0f0f04
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4178212"
---
# <a name="product-based-quote-lines-overview---lite"></a>Ürün tabanlı teklif satırlarına genel bakış - lite

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Dynamics 365 Project Operations'da ürün tabanlı teklif satırları oluşturabilirsiniz. Ürün tabanlı teklif satırları manuel eklenebilir veya ürün kataloğundaki maddeler olabilir.

## <a name="product-catalog"></a>Ürün kataloğu

Ürün kataloğundaki ürünlerde varsayılan bir birim ve birim grubu vardır. Birden çok ürün aynı öznitelik kümesini paylaşıyorsa, bu özniteliklere de sahip olan bir ürün ailesi oluşturabilirsiniz. 

Örneğin, bir şirket çeşitli yazılımlar için abonelik lisansları satar. Tüm yazılım aboneliklerinin aşağıdaki iki özniteliği vardır:

- Kullanıcı sayısı
- Ay olarak ölçülen abonelik süresi

Bu tür bir kataloğu yönetmenin iyi bir yolu da **Yazılım Aboneliği** olarak adlandırılan ve Kullanıcı sayısı ve Abonelik süresi özniteliklerine sahip olan bir ürün ailesi oluşturmaktır. Daha sonra, **abonelik yazılımı** ürün ailesine tek bir ürün ekleyebilirsiniz.

## <a name="add-product-catalog-items-to-a-project-quote"></a>Proje teklifine ürün kataloğu öğeleri ekleme

**Proje Teklifi** ve **proje sözleşmesi** sayfalarında, iki satır türü için bölümler vardır: proje tabanlı satırlar ve ürün tabanlı satırlar. Ürün tabanlı satırlar için teklif satırı veya proje sözleşmesi satırındaki açılan liste, ürün fiyatı listesindeki tüm ürünleri ve birimleri içerir. Ürün fiyatı listesinin parçası olmayan ürünler de ekleyebilirsiniz.

Ayrıca, diğer fiyat listelerinden ürünler seçebilir veya ürünleri doğrudan ürün kataloğundan seçebilirsiniz. Ürünleri doğrudan bir ürün kataloğundan seçtiğinizde, ürünün satış fiyatını almak için o ürünün varsayılan fiyat listesi kullanılır. Varsayılan bir fiyat listesi ayarlanmamışsa, fiyat 0 (sıfır) olarak ayarlanır.

Bir teklif satırı bir ürün kataloğuna dayanıyorsa, satış fiyatını doğrudan teklif satırında geçersiz kılabilirsiniz. **Fiyatlandırma** alanında kullanılabilen iki değerli bir teklif satırı:

- **Fiyatlandırmayı geçersiz kıl**
- **Varsayılanı Kullan**

**Fiyatlandırmayı geçersiz kıl** seçeneğini belirlerseniz varsayılan fiyat ayarlanmamış demektir. Bunun yerine teklif satırındaki ürün için bir fiyat girmeniz gerekir. **Varsayılanı kullan** seçeneğini belirlerseniz varsayılan satış fiyatı kullanılır ve alan düzenlenmek üzere kilitlenir.

Varsayılan satış fiyatları bir teklifteki ürün tabanlı satırlara girilir. Ardından **Fiyatlandırma** alanı **Fiyatlandırmayı geçersiz kıl** olarak ayarlanır ve böylece teklif satırlarındaki varsayılan fiyatı düzenleyebilirsiniz. Bu, Dynamics 365 Sales içindeki ürün tabanlı satırlara yönelik Project Operations'a özgü geçersiz kılmanızı sağlar.