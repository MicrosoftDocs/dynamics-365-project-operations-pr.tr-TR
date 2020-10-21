---
title: Ürün tabanlı teklif satırları için kullanıcı başına, ay başına gibi karmaşık birimleri yönetme
description: Bu konuda, ürün tabanlı teklif satırları için karmaşık birimleri yönetme hakkında bilgiler sağlanmaktadır.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 741230e69302138cce8f7379f520f7178e1c80af
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965911"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines"></a>Ürün tabanlı teklif satırları için kullanıcı başına, ay başına gibi karmaşık birimleri yönetme

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Dynamics 365 Project Operations, abonelik tabanlı ürünlerin satışını desteklemek için miktar faktörleri kullanır. Abonelik tabanlı ürünler için teklif veya proje sözleşme satırındaki miktar, kullanıcı ay sayısı olarak ifade edilir.

Genellikle abonelik yazılımının fiyatı, katalogda kullanıcı başına aylık fiyat olarak depolanır. Satış işlemi sırasında, teklif satırındaki fiyat genellikle BT satış aracısı tarafından sağlanan ve indirim uygulanan kullanıcı başına aylık fiyattır. Her anlaşmanın farklı sayıda kullanıcısı ve farklı abonelik ayı sayısı vardır. Teklif satırını hesaplamak için kullanılan miktar, kullanıcı sayısı ile abonelik ayları sayısının bir bileşimidir.

Bu tür bir satışı desteklemek için Project Operations, miktar faktörleri kavramını sunmuştur. Miktar faktörleri Dynamics 365'teki ürün özniteliklerine dayanır. Bir ürün için özelliklerin tamamını yapılandırdığınızda Project Operations, miktar faktörleri olarak bu özelliklerin bir alt kümesini veya tüm özellikleri işaretlemenizi sağlar.

Project Operations yalnızca sayısal veri türüne sahip sayısal özellikleri veya ürün özelliklerini miktar faktörü olarak işaretlenmiş olarak doğrular. Teklif satırına miktar faktörleri içeren bir ürün eklediğinizde, **Miktar** alanı salt okunur hale gelir. Miktar faktörleri olan ürün özelliklerinin değerlerini girdikten sonra Project Operations, teklif satırı miktarını hesaplar.

Örneğin, Dynamics 365 Sales aşağıdaki özelliklere sahip olabilir:

- **Kullanıcı sayısı**: kullanıcı sayısı
- **Ay sayısı**: abonelik ayları sayısı
- **Ürün SKU'su**

**Kullanıcı Sayısı** ve **Ay Sayısı** özelliklerini, ürün satırının özelliklerini düzenleyerek miktar faktörü olarak işaretleyebilirsiniz.

Ürün özelliklerinden Miktar faktörleri oluşturmak için aşağıdaki adımları izleyin:

1. Project Operations sol gezinme bölmesinde, **Satış** > **Ürünler**'e gidin.
2. Miktar faktörlerini yapılandırmanız gereken ürünü açın. Ürünün önceden yapılandırılmış özelliklere sahip olduğundan emin olun.
3. Ürün için **Proje Bilgileri** sayfasında, **Miktar Faktörleri** sekmesini seçin.
4. Alt ızgarada, **+ Yeni alan hesaplaması**'nı seçin.
5. Miktar faktörünün adını girin ve alan hesaplamasıyla eşleşen özellik değerini seçin.
6. Formu kaydedin ve kapatın. Ürün tabanlı teklif satırının miktarını hesaplamak üzere tüm özellikler için bu adımları tekrarlayın.

Ürün için ürün tabanlı bir teklif satırı oluşturduğunuzda, teklif satırının miktarı kilitlenir. Miktar, o teklif satırı için girdiğiniz özellik değerlerinin bir bileşimi olarak hesaplanır.
