---
title: Ürün tabanlı sözleşme satırları için karmaşık birimleri yönetme - lite
description: Bu konu, abonelik tabanlı ürünlerin satışını destekleme hakkında bilgi sağlar.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 029d2aa4fd20fc036a34ae6136fe12454f3b7703
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273357"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a>Ürün tabanlı sözleşme satırları için karmaşık birimleri yönetme - lite

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Dynamics 365 Project Operations, abonelik tabanlı ürünlerin satışını desteklemek için miktar faktörleri kullanır. Abonelik tabanlı ürünler için, sözleşme veya proje sözleşmesi satırındaki miktar kullanıcı ay sayısı olarak ifade edilir.

Abonelik yazılımının fiyatı, katalogda kullanıcı başına aylık fiyat olarak depolanır. Satış işlemi sırasında, sözleşme satırındaki fiyat genellikle satış aracısı tarafından sağlanan ve indirim uygulanan kullanıcı başına aylık fiyattır. Her anlaşmanın farklı sayıda kullanıcısı ve farklı abonelik ayı sayısı vardır. Sözelşme satırının tutarını hesaplamak için kullanılan miktar bir kullanıcı sayısı ve abonelik ayları sayısı ürünüdür.

Bu tür bir satışı desteklemek için Project Operations *miktar faktörleri* kavramını destekler. Miktar faktörleri ürün özniteliklerine dayanır. Bir ürün için belirli özellikler yapılandırdığınızda miktar faktörleri olarak bu özelliklerin bir alt kümesini veya tüm özellikleri işaretleyebilirsiniz.

Project Operations yalnızca sayısal veri türüne sahip sayısal özellikleri veya ürün özelliklerini miktar faktörü olarak işaretlenmiş olarak doğrular. Yapılandırılan miktar faktörlerini içeren bir ürün bir sözleşme satırına eklendiğinde, **Miktar** alanı salt okunur olur. Miktar faktörleri olan ürün özelliklerinin değerlerini girdikten sonra Project Operations sözleşme satırı miktarını hesaplar.

Örneğin, Dynamics 365 Sales aşağıdaki özelliklere sahip olabilir:

- **Kullanıcı sayısı**: kullanıcı sayısı.
- **Ay sayısı**: abonelik ayları sayısı.
- **Ürün SKU'su**: Ürünün stok saklama birimi (SKU).

**Kullanıcı Sayısı** ve **Ay Sayısı** özellikleri ürün satırının özellikleri düzenlenerek miktar faktörü olarak işaretlenebilir.

Ürün özelliklerinden miktar faktörleri oluşturmak için aşağıdaki adımları izleyin.

1. **Project Operations**'ta **Satış-Ürünler**'i seçin.
2. Miktar faktörleri ayarlamanız gereken ürünü açın. Ürünün önceden ayarlanmış özellikleri olduğundan emin olun.
3. **Proje bilgileri** sayfasında **Miktar faktörleri** sekmesini seçin.
4. Alt ızgarada, **+ Yeni alan hesaplaması**'nı seçin.
5. **Miktar faktörünün** adını girin ve alan hesaplamasıyla eşleşen özellik değerini seçin.
6. Formu kaydedin ve kapatın.
7. Birlikte ürün tabanlı sözleşme satırı için miktarı oluşturan tüm özellikler için 2-6 arasındaki adımları yineleyin.

Miktar faktörleri ayarlandığında, Kullanıcı bu ürün için bir sözleşme satırı oluşturduğunda, sözleşme satırının miktarı kilitlenir. Miktar daha sonra, bu sözleşme satırı için özellik değerlerinin bir ürünü olarak hesaplanır.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]