---
title: Ürün tabanlı sözleşme satırlarına genel bakış - lite
description: Bu konu ürün tabanlı sözleşme satırlarıyla ilgili bilgi sağlar.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 8464eefbce9ba266360e10039e2a0be78982d8fa
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369760"
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