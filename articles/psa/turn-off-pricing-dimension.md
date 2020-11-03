---
title: Fiyatlandırma boyutunu kapatma
description: Bu konu, Project Service çözümünde fiyatlandırma boyutlarının nasıl ayarlanacağını gösterir.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 1ae95430c368370145c7081a5d94d6161a7700b4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086409"
---
# <a name="turn-off-a-pricing-dimension"></a>Fiyatlandırma boyutunu kapatma

Fiyatlandırma stratejinizi her beş yılda bir gözden geçirmeniz ve güncelleştirmeniz gerekebilir. Gerçekleştirdiğiniz güncelleştirmeler, varolan bir fiyatlandırma boyutunu kapatmanızı ve yeni bir tane oluşturmanızı gerektirebilir. Örneğin, önceden **Rol** 'e göre fiyatlandırma yapıyorken artık **İş Deneyimi** 'ne göre fiyatlandırma yapmaya karar verdiniz. Bunun için fiyatlandırma boyutu olarak **Rol** 'ü kapatmanız ve yeni fiyatlandırma boyutu olarak **İş Deneyimi** 'ni oluşturmanız gerekebilir. 

Bir fiyatlandırma boyutu kullanıma hazır veya özel olup olmadığından bağımsız olarak Fiyatlandırma Boyutunun **Maliyet için Geçerli** ve **Satış için Geçerli** alanları **Hayır** olarak ayarlanarak kapatılabilir.

Ancak bunu yaptığınızda, aşağıdaki hata iletisini alabilirsiniz.

![Bir fiyatlandırma boyutunu kapatırken İş Süreci Hatası oluşabilir](media/Business-Process-Error.png)


Bu hata iletisi, kapatılan boyut için daha önceden ayarlanmış fiyat kayıtları olduğunu belirtir. Bir boyutla ilgili **Rol Fiyatı** ve **Rol Fiyatı Kar Payı** kayıtları, boyutun uygulanabilirliği **Hayır** olarak ayarlanmadan önce silinmelidir. Bu kural, hem kullanıma hazır fiyatlandırma boyutları hem de oluşturmuş olabileceğiniz özel fiyatlandırma boyutları için geçerlidir. Bu doğrulamanın nedeni, Project Service'de **Rol Fiyatı** kaydının benzersiz bir boyut birleşimine sahip olması gerektiği kısıtlamasının olmasıdır. Örneğin, **ABD Maliyet Oranları 2018** adlı bir fiyat listesinde aşağıdaki **Rol Fiyatı** satırları bulunur. 

| Standart Başlık         | Kuruluş Birimi    |Birim   |Fiyat  |Para Birimi  |
| -----------------------|-------------|-------|-------|----------|
| Sistem Mühendisi|Contoso ABD|Hour| 100|USD|
| Kalfa Sistem Mühendisi|Contoso ABD|Hour| 150| USD|


**Standart Başlık** 'ı fiyatlandırma boyutu olarak kapattığınızda ve Project Service fiyatlandırma altyapısı bir fiyat için arama yaptığında yalnızca giriş bağlamından **Kuruluş Birimi** değerini kullanır. Giriş bağlamının **Kuruluş Birimi** "Contoso ABD" ise her iki satır da eşleşeceğinden sonuç belirleyici olmaz. Bu senaryoyu önlemek için Project Service, **Rol Fiyatı** kayıtları oluştururken boyut birleşiminin benzersiz olduğunu doğrular. **Rol Fiyatı** kayıtları oluşturulduktan sonra boyut kapatılırsa bu kısıtlama ihlal edilebilir. Bu nedenle bir boyutu kapatmadan önce bu boyut değeriyle doldurulmuş tüm **Rol Fiyatı** ve **Rol Fiyatı Kar Payı** satırlarını silmeniz gerekir.

