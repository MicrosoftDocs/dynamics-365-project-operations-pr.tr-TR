---
title: Ürün tabanlı teklif satırları
description: Bu konu ürün tabanlı teklif satırlarıyla ilgili bilgi sağlar.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 8bde88f5f2d00c09129c6a9363c09f6f6ad1dd90
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284112"
---
# <a name="product-based-quote-lines"></a>Ürün tabanlı teklif satırları

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


Dynamics 365 Project Service Automation'da ürün tabanlı teklif satırları oluşturabilirsiniz. Ürün tabanlı teklif satırları "serbest" satırlar veya ürün kataloğundaki maddeler olabilir.

## <a name="product-catalog"></a>Ürün kataloğu

Bir Dynamics 365 ürün kataloğundaki ürünlerde varsayılan bir birim ve birim grubu vardır. Birden çok ürün aynı öznitelik kümesini paylaşıyorsa, bu özniteliklere de sahip olan bir ürün ailesi oluşturabilirsiniz. Bir ürün ailesindeki tüm ürünler aynı öznitelik kümesini devralır.

Örneğin, bir şirket çeşitli yazılımlar için abonelik lisansları satar. Tüm yazılım aboneliklerinin aşağıdaki iki özniteliği vardır:

- Kullanıcı sayısı 
- Abonelik süresi (ay)

Bu tür bir kataloğu yönetmenin iyi bir yolu da **Yazılım Aboneliği** olarak adlandırılan ve **Kullanıcı sayısı** ve **Abonelik süresi** özniteliklerine sahip olan bir ürün ailesi oluşturmaktır. Daha sonra **Yazılım Aboneliği** ürün ailesine **Dynamics 365 Field Service** veya **Dynamics 365 Sales** gibi bağımsız ürünler ekleyebilirsiniz.

## <a name="adding-product-catalog-items-to-a-project-quote"></a>Proje teklifine ürün kataloğu öğeleri ekleme

Proje teklifi ve proje sözleşmesi sayfalarında, iki satır türü için bölümler vardır: proje tabanlı satırlar ve ürün tabanlı satırlar. Ürün tabanlı satırlarda, Dynamics 365 teklife ürün kataloğundan maddeler eklemek için kullanılır. Teklif satırı veya proje sözleşmesi satırındaki açılan liste, teklife veya proje sözleşmesine iliştirilen ürün fiyatı listesindeki tüm ürünleri ve birimleri içerir. Teklifin ürün fiyatı listesinin parçası olmayan ürünler de ekleyebilirsiniz.

Ayrıca, diğer fiyat listelerinden ürünler seçebilir veya ürünleri doğrudan ürün kataloğundan seçebilirsiniz. Ürünleri doğrudan bir ürün kataloğundan seçtiğinizde, ürünün satış fiyatını almak için o ürünün varsayılan fiyat listesi kullanılır. Varsayılan bir fiyat listesi ayarlanmamışsa, fiyat 0 (sıfır) olarak ayarlanır.

Bir teklif satırı bir ürün kataloğuna dayanıyorsa, satış fiyatını doğrudan teklif satırında geçersiz kılabilirsiniz. Dynamics 365'teki bir teklif satırında **Fiyatlandırma** alanı olduğunu unutmayın. İki değer vardır:

- Fiyatlandırmayı geçersiz kıl  
- Varsayılanı kullan

Bu alanı **Fiyatlandırmayı geçersiz kıl** olarak belirlerseniz, Dynamics 365 varsayılan bir fiyat ayarlamaz. Teklif satırındaki ürün için bir fiyat girmeniz gerekir. Bu alanı **Varsayılanı kullan** olarak ayarladığınızda, Dynamics 365 varsayılan satış fiyatını kullanır ve düzenlemeyi engellemek için alanı kilitler.

PSA'yı yükledikten sonra, varsayılan satış fiyatları bir teklifteki ürün tabanlı satırlara girilir. Ardından **Fiyatlandırma** alanı **Fiyatlandırmayı geçersiz kıl** olarak ayarlanır ve böylece teklif satırlarındaki varsayılan fiyatı düzenleyebilirsiniz.

> ![Fiyatlandırmayı geçersiz kıl ayarı](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a>Ürünler için miktar faktörleri

PSA, abonelik tabanlı ürünlerin satışını desteklemek için miktar faktörleri kullanır. Abonelik tabanlı ürünler için, teklif veya proje sözleşmesi satırındaki miktar kullanıcı ay sayısı olarak ifade edilir.

Genellikle abonelik yazılımının fiyatı, katalogda kullanıcı başına aylık fiyat olarak depolanır. Bununla birlikte, bunun yerine başka zaman açıklamaları da kullanabilirsiniz. Satış işlemi sırasında, teklif satırındaki fiyat genellikle BT satış aracısı tarafından sağlanan ve indirim uygulanan kullanıcı başına aylık fiyattır. Her anlaşmanın farklı sayıda kullanıcısı ve farklı abonelik ayı sayısı vardır. Teklif satırının tutarını hesaplamak için kullanılan miktar bir kullanıcı sayısı ve abonelik ayları sayısı ürünüdür.

Bu tür bir satışı desteklemek için PSA miktar faktörleri kavramını sunmuştur. Miktar faktörleri Dynamics 365'teki ürün özniteliklerine dayanır. Bir ürün için belirli özellikler yapılandırdığınızda PSA, miktar faktörleri olarak bu özelliklerin bir alt kümesini veya tüm özellikleri işaretlemenizi sağlar.

PSA, yalnızca sayısal veri türüne sahip sayısal özellikleri veya ürün özelliklerini miktar faktörü olarak işaretlenmiş olarak doğrular. Miktar faktörlerinin yapılandırıldığı bir ürün bir teklif satırına eklendiğinde, teklif satırındaki **Miktar** alanı salt okunur bir alan haline gelir. Miktar faktörleri olan ürün özelliklerinin değerlerini girdikten sonra PSA teklif satırı miktarını hesaplar.

Örneğin, Dynamics 365 aşağıdaki özelliklere sahip olabilir: 

- **Kullanıcı sayısı** - Kullanıcı sayısı 
- **Ay sayısı**  - Abonelik ayları sayısı
- **Ürün SKU'su** 

**Kullanıcı sayısı** ve **Ay sayısı** özellikleri ürün satırının özellikleri düzenlenerek miktar faktörü olarak işaretlenebilir. 

> ![Kullanıcı sayısı ve Ay sayısını kalite faktörleri olarak işaretleme](media/basic-guide-11.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]