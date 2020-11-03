---
title: Birden fazla para birimi senaryoları (sürüm 3.x)
description: Bu konu, çoklu para birimi senaryoları hakkında bilgi sağlar.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/26/2018
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
ms.openlocfilehash: 7be029eeca3129d30f4bec1bf9b180a0a5122a86
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086434"
---
# <a name="multiple-currency-scenarios"></a>Birden fazla para birimi senaryoları

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Microsoft Dynamics 365, para birimleri için iki kavrama sahiptir:

- **İşlem para birimi** - Bir işlemin gerçekleştirildiği para birimi. 
- **Temel para birimi** - Dynamics 365 kurulumunun para birimi. Bu para birimi, bir Dynamics 365 kurulumu hazırlandığında ayarlanır. Değiştirilemez.

Örneğin, Contoso US, Birleşik Krallık'taki bir müşteriye tanesi 15 pound (GBP) olmak üzere 100 adet tişört satar. Aşağıdaki tabloda, bu işlemin Sipariş Ürünü varlığına nasıl kaydedildiği gösterilmektedir.

| Ürün | Miktar | Birim fiyatı | Para Birimi | Miktar | Döviz kuru | Birim fiyatı (Temel)| Tutar (Temel)|
|---------|----------|----------------|----------|--------|---------------|----------------------|--------------|
| Tişört | 100      | 15             | GBP      | 1500   | 0.94          | 17,25 USD               | 1.725 USD       |

**Para birimi** sütunu, satışın oluştuğu para birimi olan işlem para birimini gösterir. **Döviz kuru** sütunu, işlem para birimi ile temel para birimi arasındaki döviz kurunu gösterir. Temel para birimi ABD Dolarıdır (USD). Bu temel para birimi, Dynamics 365 kurulumu hazırlandığında ayarlanmıştır.
Tablonun gösterdiği gibi, her işlem hem işlem para birimi, hem de temel para birimi cinsinden kaydedilir. Dynamics 365, para birimi döviz kurunu temel para birimi tutarlarını hesaplamak için kullanır.

## <a name="project-service-automation-extensions"></a>Project Service Automation uzantıları

Dynamics 365 Project Service Automation iş işlemlerinin genellikle maliyet ve satış gibi iki yönü olduğundan, işlem para birimini etkiler.

Aşağıdaki varlıklar, iş işlemleri olarak düşünülür:

- Teklif satırı ayrıntısı
- Proje sözleşme satırı ayrıntısı
- Tahmin satırı
- Yevmiye defteri satırı
- Fatura satırı ayrıntısı
- Gerçek

Bu varlıkların her birinde, maliyet tutarını veya satış tutarını gösteren bir kayıt vardır. **Tutar** alanı bulunan herhangi bir Dynamics 365 varlığında olduğu gibi, her kayıt hem işlem para birimi hem de temel para birimi cinsinden tutarları içerir. 

PSA, maliyet ve satışlar için işlem para birimi kavramını aşağıdaki yollarla genişletir:

- Zaman işlemleri için maliyet işlemi para birimi her zaman projenin sahibi olan veya projeyi yöneten kuruluş biriminin para biriminden gelir. Bu kuruluş birimi, sözleşme birimi olarak bilinir.
- Zaman ve gider işlemleri için satış işlemi para birimi her zaman proje sözleşmesinin para biriminden gelir.
- Giderler için maliyet işlem para birimi, gider girişinin oluşturulduğu para biriminden gelir.

## <a name="multiple-currency-scenario"></a>Birden fazla para birimi senaryosu

Bu bölümde, Contoso UK'nin Fabrikam, Japonya adlı bir müşteri için kullandığı bir proje örneği açıklanmaktadır. Bu senaryo şu şekilde ayarlanmıştır:

1. GBP ve Japon Yeni (JPY) **Ayarlar** \> **İşletme Yönetimi**\> **Para birimleri**  altında ayarlanır. 
2. **Fabrikam-Japonya** adlı bir müşteri hesabı ayarlanmıştır ve hesapta para birimi olarak JPY seçilir.
3. **Contoso UK** adlı bir kuruluş birimi ayarlanır ve para birimi olarak GBP seçilir.
4. **Contoso UK** 'nin sözleşme birimi olarak ve **Fabrikam-Japonya** 'nın müşteri olarak belirtildiği bir proje sözleşmesi oluşturulur.
5. Proje sözleşme satırları, zaman için faturalama ile giderler için faturalama gibi projedeki çeşitli işlem sınıfları için faturalama düzenlemeleri temel alınarak oluşturulur.
6. **Contoso UK** 'nin sözleşme birimi olarak belirtildiği bir proje oluşturulur. Bu proje oluşturulur ve proje sözleşmesi satırlarıyla eşleştirilir.


Teklif satırı ayrıntısını, proje sözleşme satırı ayrıntısını veya zamanlamanın tahmini satırını kullanan tahmin sırasında, varlıkta her zaman iki kayıt oluşturulur. Bir kayıt maliyet için ve diğer kayıt satış içindir.

- Varsayılan olarak, maliyet kaydındaki işlem para birimi, projenin sözleşme birimindeki para birimi olarak ayarlanır. Bu örnekte para birimi GBP'dir
- Varsayılan olarak, satış kaydındaki işlem para birimi, proje sözleşmesindeki para birimi olarak ayarlanır. Bu örnekte para birimi JPY'dir

Zaman girişi veya yevmiye defteri satırı kullanılarak zaman için fiili değerler oluşturulduğunda aşağıdaki davranış oluşur:

- Varsayılan olarak, maliyet kaydındaki işlem para birimi, projenin sözleşme birimindeki para birimi olarak ayarlanır.
- Varsayılan olarak, satış kaydındaki işlem para birimi, proje sözleşmesindeki para birimi olarak ayarlanır.

Gider girişi veya yevmiye defteri satırı kullanılarak giderler için fiili değerler oluşturulduğunda aşağıdaki davranış oluşur:

- Gider tutarını herhangi bir para birimi cinsinden kaydedebilirsiniz. **Gider Girişi** sayfasında veya **Yevmiye defteri satırı** sayfasında para birimi seçicisini kullanarak para birimini seçin. Varsayılan olarak, maliyet kaydındaki işlem para birimi, gider girişindeki para birimi olarak ayarlanır. 
- Varsayılan olarak, satış kaydı için işlem para birimi, proje sözleşmesindeki para birimidir. Bu para birimini ayarlamak için, sistem önce işlem tutarını kullanıcının temel para birimine girdiği para birimiyle dönüştürür. Ardından, tutarı proje sözleşmesinin para birimine dönüştürür. 

### <a name="computing-roll-ups-when-project-actuals-are-recorded-in-multiple-transaction-currencies"></a>Proje fiili değerleri birden çok işlem para birimi cinsinden kaydedildiğinde toplamları hesaplama

Dynamics 365, farklı para birimlerindeki tutarların toplamalarını otomatik olarak işler. İşte bir örnek.

| İşlem sınıfı | İşlem türü| Date   | Kaynak | İşlem kategorisi | Miktar | Birim fiyatı | Miktar      | Döviz kuru | Temel para birimi cinsinden tutar |
|-------------------|------------------|--------|----------|----------------------|----------|--------------|-------------|---------------|----------------|
| Time              | Faturalanmayan satış   | 14 Haz | Doğu  |                      | 8 sa.    | 20.000 JPY    | 160.000 JPY | 123           | 1.300,81 USD    |
| Time              | Faturalanmayan satış   | 15 Haz | Doğu  |                      | 8 sa.    | 20.000 JPY    | 160.000 JPY | 123           | 1.300,81 USD    |
| Gider           | Faturalanmayan satış   | 16 Haz | Doğu  | Otel                | 1 ea     | 250 EUR      | 250 EUR     | 0.94          | 265,95 USD     |
| Gider           | Faturalanmayan satış   | 17 Haz | Doğu  | Araba Kiralama           | 1 ea     | 150 EUR      | 150 EUR     | 0.94          | 159,57 USD     |

Projedeki toplam faturalandırmayan satış değerini hesaplamak için, tüm ilgili faturalanmayan satış fiili değerleri üzerinde **Tutar** alanı için bir toplama alanı oluşturabilirsiniz. Toplama alanı, ilgili kayıtlarda hızlı formüllere olanak sağlayan bir Dynamics 365 yapısıdır.
