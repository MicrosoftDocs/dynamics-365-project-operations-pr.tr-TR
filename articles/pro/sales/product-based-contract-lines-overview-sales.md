---
title: Ürün tabanlı sözleşme satırlarına genel bakış - lite
description: Bu konu ürün tabanlı sözleşme satırlarıyla ilgili bilgi sağlar.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: eb09140eae5383b882db73195d0360a836ece791
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177895"
---
# <a name="product-based-contract-lines-overview---lite"></a>Ürün tabanlı sözleşme satırlarına genel bakış - lite

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Dynamics 365 Project Operations'ta ürün tabanlı sözleşme satırları oluşturabilirsiniz. Ürün tabanlı sözleşme satırları, manuel oluşturulan satırlar veya ürün kataloğundaki maddeler olabilir.

## <a name="product-catalog"></a>Ürün kataloğu

Bir ürün kataloğundaki ürünlerde varsayılan bir birim ve birim grubu vardır. Birden çok ürün aynı öznitelik kümesini paylaşıyorsa, bu özniteliklere de sahip olan bir ürün ailesi oluşturabilirsiniz. Bir ürün ailesindeki tüm ürünler aynı öznitelik kümesini devralır.

Örneğin, bir şirket çeşitli yazılımlar için abonelik lisansları satar. Tüm yazılım aboneliklerinin aşağıdaki iki özniteliği vardır:

- Kullanıcı sayısı
- Abonelik süresi (ay)

Bu tür bir kataloğun bakımını yapmak için **abonelik yazılımı** adlı bir ürün ailesi oluşturun. Ürün ailesine öznitelikleri, **Kullanıcı sayısını** ve **abonelik süresini** ekleyin. Daha sonra, **abonelik yazılımı** ürün ailesine tek bir ürün ekleyin.

## <a name="add-product-catalog-items-to-a-project-contract"></a>Proje sözleşmesine ürün kataloğu öğeleri ekleme

Proje sözleşmesi sayfalarında, iki satır türü için bölümler vardır: proje tabanlı satırlar ve ürün tabanlı satırlar. Ürün tabanlı satırlar, sözleşmedeki ürün fiyatı listesinde yer alan tüm ürünleri ve birimleri içerir. Sözleşmenin ürün fiyatı listesinin parçası olmayan ürünler de ekleyebilirsiniz.

Diğer fiyat listelerinden veya doğrudan ürün kataloğundan ürünler seçebilirsiniz. Ürünleri doğrudan bir ürün kataloğundan seçtiğinizde, ürünün satış fiyatını almak için o ürünün varsayılan fiyat listesi kullanılır. Varsayılan bir fiyat listesi ayarlanmamışsa, fiyat 0 (sıfır) olarak ayarlanır.

Bir sözleşme satırı bir ürün kataloğuna dayanıyorsa, satış fiyatını doğrudan sözleşme satırında geçersiz kılabilirsiniz. Bir sözleşme satırı iki değere sahip **Fiyatlandırma** alanına sahiptir:

- **Fiyatlandırmayı geçersiz kıl**
- **Varsayılanı kullan**

**Fiyatlandırmayı** alanını **Fİyatlandırmayı geçersiz kıl** olarak belirlerseniz varsayılan fiyat ayarlanmaz. Sözleşme satırında ürün için fiyat girin. Alanını **Varsayılan kullanılacak** şekilde ayarladığınızda , varsayılan satış fiyatı kullanılır ve alan düzenlenemez.

Project Operations'ı yükledikten sonra, varsayılan satış fiyatları bir sözleşmedeki ürün tabanlı satırlara girilir. Ardından **Fiyatlandırma** alanı **Fiyatlandırmayı geçersiz kıl** olarak ayarlanır ve böylece sözleşme satırlarındaki varsayılan fiyatı düzenleyebilirsiniz. Bu, Dynamics 365 Sales içindeki ürün tabanlı satırlar davranışına projeyle ilgili özel geçersiz kılmanızı sağlar.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]