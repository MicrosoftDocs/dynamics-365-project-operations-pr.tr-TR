---
title: Fiyatlandırma boyutunu kapatma
description: Bu konuda, özel fiyatlandırma boyutlarının kapatılması hakkında bilgi verilmektedir.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: ffeff2ab465f37b8a4e40f4e64b118e3bb412cb8
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119307"
---
# <a name="turning-off-a-pricing-dimension"></a>Fiyatlandırma boyutunu kapatma

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Fiyatlandırma stratejinizi her beş yılda bir gözden geçirmeniz ve güncelleştirmeniz gerekebilir. Gerçekleştirdiğiniz güncelleştirmeler, varolan bir fiyatlandırma boyutunu kapatmanızı ve yeni bir tane oluşturmanızı gerektirebilir. Örneğin, önceden **Rol**'e göre fiyatlandırma yapıyorken artık **İş Deneyimi**'ne göre fiyatlandırma yapmaya karar verdiniz. Bunun için fiyatlandırma boyutu olarak **Rol**'ü kapatmanız ve yeni fiyatlandırma boyutu olarak **İş Deneyimi**'ni oluşturmanız gerekebilir. 

Bir fiyatlandırma boyutu kullanıma hazır veya özel olup olmadığından bağımsız olarak Fiyatlandırma Boyutunun **Maliyet için Geçerli** ve **Satış için Geçerli** alanları **Hayır** olarak ayarlanarak kapatılabilir.

Ancak bunu yaptığınızda, **İlişkili fiyat kayıtları varsa fiyatlandırma boyutu güncelleştirilemez veya silinemez.** hata iletisini alabilirsiniz.

Bu hata iletisi, kapatılan boyut için daha önceden ayarlanmış fiyat kayıtları olduğunu belirtir. Bir boyutla ilgili **Rol Fiyatı** ve **Rol Fiyatı Kar Payı** kayıtları, boyutun uygulanabilirliği **Hayır** olarak ayarlanmadan önce silinmelidir. Bu kural, hem kullanıma hazır fiyatlandırma boyutları hem de oluşturmuş olabileceğiniz özel fiyatlandırma boyutları için geçerlidir. Bu doğrulamanın nedeni, her **Rol Fiyatı** kaydının benzersiz bir boyut birleşimine sahip olması gerektiğidir. Örneğin, **ABD Maliyet Oranları 2018** adlı bir fiyat listesinde aşağıdaki **Rol Fiyatı** satırları bulunur. 

| Standart Başlık         | Kuruluş Birimi    |Birim   |Fiyat  |Para Birimi  |
| -----------------------|-------------|-------|-------|----------|
| Sistem Mühendisi|Contoso ABD|Hour| 100|USD|
| Kalfa Sistem Mühendisi|Contoso ABD|Hour| 150| USD|


**Standart Başlık**'ı fiyatlandırma boyutu olarak kapattığınızda ve fiyatlandırma altyapısı bir fiyat için arama yaptığında yalnızca giriş bağlamından **Kuruluş Birimi** değerini kullanır. Giriş bağlamının **Kuruluş Birimi** "Contoso ABD" ise her iki satır da eşleşeceğinden sonuç belirleyici olmaz. Bu senaryoyu önlemek için sistem, **Rol Fiyatı** kayıtları oluştururken boyut birleşiminin benzersiz olduğunu doğrular. **Rol Fiyatı** kayıtları oluşturulduktan sonra boyut kapatılırsa bu kısıtlama ihlal edilebilir. Bu nedenle bir boyutu kapatmadan önce bu boyut değeriyle doldurulmuş tüm **Rol Fiyatı** ve **Rol Fiyatı Kar Payı** satırlarını silmeniz gerekir.
