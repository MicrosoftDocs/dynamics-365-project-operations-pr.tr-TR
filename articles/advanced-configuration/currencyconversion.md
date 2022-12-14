---
title: Maliyet oranlarından satış fiyatlarını hesaplamak için para birimi dönüştürme ayarlama
description: Bu makalede, satıi işlemleri maliyet işlemlerinden oluşturulduğunda Microsoft Dynamics 365 Project Operations'ta kullanılacak para birimi dönüştürme davranışının nasıl yapılandırılacağı açıklanmaktadır.
author: rumant
ms.date: 11/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3fa8077deb18f1a54e7f0f5e6dc4491a830df45b
ms.sourcegitcommit: 95e52fcf012a51229f3f6ae7dbf7b0fa56072a85
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/01/2022
ms.locfileid: "9816680"
---
# <a name="set-up-currency-conversion-to-calculate-sales-prices-from-cost-rates"></a>Maliyet oranlarından satış fiyatlarını hesaplamak için para birimi dönüştürme ayarlama

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Microsoft Dynamics 365 Project Operations'ta, gider kategorilerinin satış fiyatları sayısal değerler olarak ayarlanabilir veya bunlar gerçekleşen maliyete göre hesaplanmak üzere de ayarlanabilir.

Gerçekleşen maliyete göre hesaplanacak şekilde ayarlandıklarında, aşağıdaki seçenekler kullanılabilir:

- Maliyette
- Maliyet üzerinde kar payı yüzdesi

Gider maliyetinin, proje sözleşmesinin satış para biriminden farklı bir para birimiyle gerçekleştiği senaryolarda para birimi dönüştürme, satış fiyatını maliyete dayalı olarak hesaplamak için gereklidir.

## <a name="currency-conversion-behavior-that-uses-native-dataverse-exchange-rates"></a>Yerel Dataverse döviz kurlarını kullanan para birimi dönüştürme davranışı

Varsayılan olarak, Project Operations Dataverse'deki Para birimi tablosunda depolanan döviz kurlarını kullanır. Project Operations'ı satış fiyatlarını maliyetten hesaplamak amacıyla yerel döviz kurlarını kullanmak üzere yapılandırmak için aşağıdaki adımları uygulayın.

1. **Project Operations \> Ayarlar \> Parametreler**'e gidin.
1. **Proje Parametresi** ayrıntılar sayfasını açın.
1. **Para birimi dönüştürme mantığı** alanını boş bir değere ayarlayın.

## <a name="currency-conversion-behavior-that-uses-exchange-rates-from-finance-and-operations-apps"></a>Finans ve operasyon uygulamalarındaki döviz kurlarını kullanan para birimi dönüştürme davranışı

Dataverse'te yerel olarak kullanılabilen Para birimi tablosundaki döviz kurları tarihe duyarlı değildir. Bu nedenle, her zaman maliyet oranlarından satış fiyatları hesaplaması için mevcut gereksinimlerinize göre ölçeklenmeyebilir.

Maliyet para birimi cinsindeki bir maliyet oranından satış para birimi cinsindeki satış fiyatını hesaplamak için finans ve operasyonlar ortamındaki döviz kurlarını kullanabilirsiniz. Bu para birimi dönüştürme davranışını yapılandırmak için aşağıdaki adımları uygulayın.

1. **Proje parametreleri** sayfasında **Para birimi dönüştürme mantığı** alanını ekleyin. Ardından özelleştirmeyi kaydedin ve yayımlayın.
1. **Project Operations \> Ayarlar \> Parametreler**'e gidin.
1. **Proje Parametresi** ayrıntılar sayfasını açın. 
1. **Para birimi dönüştürme davranışı** alanını **Varsayılana geri dönüş ile genişletildi** olarak ayarlayın.
1. Aşağıdaki tablolara **Çift yazma uygulama kullanıcısı** güvenlik rolü **Genel Okuma** izni verin:

    - msdyn\_currencyexchangerates
    - msdyn\_currencyexchangeratepairs
    - msdyn\_exchangeratetypes

1. Finans ve operasyonlar ortamınızda, ilk eşitlemeyle birlikte aşağıdaki çift yazma eşlemelerini çalıştırın:

    - Döviz kuru türü (msdyn\_exchangeratetypes)
    - Döviz kuru para birimi çifti (msdyn\_currencyexchangeratepairs)
    - CDS Döviz Kurları (msdyn\_currencyexchangerates)

Bu değişiklikler tamamlandıktan sonra çift yazma, finans ve operasyonlar ortamındaki döviz kurlarını Dataverse'de kullanılabilir duruma getirir. Project Operations daha sonra bu döviz kurlarını kullanarak maliyet oranlarını sözleşmenin satış para birimine dönüştürür.

> [!NOTE]
> Bu para birimi dönüştürme davranışı, yalnızca maliyet oranlarındaki satış fiyatlarının hesaplanmasında geçerlidir. Temel para birimi değerlerini genel olarak hesaplamak için kullanılmaz. Temel para birimi değerleri, bu yordamı tamamlayıp tamamlamadığınıza bakılmaksızın her zaman yerel Dataverse döviz kurlarını kullanır.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
