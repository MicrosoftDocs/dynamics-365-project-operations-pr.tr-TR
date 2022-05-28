---
title: İşlem Kategorisini fiyatlandırma boyutu olarak kullanma
description: Bu konu, İşlem Kategorisi alanının bir fiyatlandırma boyutu olarak kullanılması hakkında bilgi sağlar.
author: rumant
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a7fe9bfc87db992252f8ef3f0f688e7426cafebb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591152"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>İşlem Kategorisini fiyatlandırma boyutu olarak kullanma


_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_


Bu konu, **İşlem Kategorisi** alanının bir fiyatlandırma boyutu olarak nasıl kullanılacağını açıklar. 

## <a name="prerequisites"></a>Ön koşullar
Bu konudaki yordamları tamamlamadan önce kuruluşunuz için yeni bir fiyatlandırma boyutu çözümüne sahip olmanız gerekir. Henüz bir tane oluşturmadıysanız bkz. [Fiyatlandırma boyutları olarak özel alanlar ve varlıklar oluşturma](create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-transaction-category-field-to-forms-and-views"></a>İşlem Kategorisi alanını formlara ve görünümlere ekleme
Fiyatlandırma boyutu çözümünde **İşlem Kategorisi** alanını görünür hale getirmek için alanı tüm formlara ve görünümlere varlık olarak eklemeniz gerekir.

Aşağıdaki tabloda tüm kullanıma hazır formlar ve görünümler varlığa göre listelenmektedir. Yeni alanı, özelleştirilmiş varlıklarınızdaki ek formlara veya görünümlere de eklemeniz gerekir.

|  Entity        | Formlar     |Görünümler        |
| ------------------------------|---------------------------------|----------------------------------|
|  Rol Fiyatı| Bilgiler |- Etkin Kaynak Kategorisi Fiyatları<br> - İlişkili Kaynak Kategorisi Fiyatı |
|  Rol Fiyatı Kar Payı| Bilgiler|- Etkin Rol Fiyatı Kar Payı<br>- İlişkili Rol Fiyatı Kar Payı |
|  Teklif Satırı Ayrıntısı|- Proje Bilgileri<br>- Hızlı Proje Oluştur| - Etkin Teklif Satırı Ayrıntısı<br>- Birleşik Teklif Satırı Ayrıntıları<br>- İlişkili Teklif Satırı Ayrıntısı |
|  Proje Sözleşme Satırı Ayrıntısı|- Proje Bilgileri<br>- Hızlı Proje Oluştur|- Birleşik Sözleşme Satırı Ayrıntıları<br>- Etkin Sözleşme Satırı Ayrıntıları<br>- İlişkili Sözleşme Satırı Ayrıntısı |
|  Proje Görevi|- Bilgi<br>- Yeni Form| &nbsp; |
|  Proje Takımı Üyesi|- Bilgi<br>- Yeni Form|- Etkin Proje Takımı Üyeleri<br>- Proje Takımı Üyeleri<br>- İlişkili Proje Takımı Üyeleri |
|  Zaman Girişi|- Bilgi<br>- Zaman Girişi Oluştur|- Tarihe Göre Zaman Girişlerim<br>- Bu Hafta için Zaman Girişlerim<br>- Onaylanacak zaman girişleri|
|  Yevmiye Defteri Satırı|- Bilgi<br>- Hızlı Oluştur|- Etkin Yevmiye Defteri Satırları<br>- İlişkili Yevmiye Defteri Satırı|
|  Fatura Satırı Ayrıntısı|- Bilgi<br>- Hızlı Oluştur|- Etkin Fatura Satırı Ayrıntıları<br>- Borçlandırılabilir Fatura İşlemleri<br>- Ücretsiz Fatura İşlemleri<br>- İlişkili Fatura Satırı Ayrıntısı <br>- Borçlandırılamaz Fatura İşlemleri|
|  Gerçek|- Bilgi<br>- Etkin Gerçek Tutarlar| İlişkili Gerçek Tutar |

## <a name="set-up-the-transaction-category-field-as-a-pricing-dimension"></a>İşlem Kategorisi alanını fiyatlandırma boyutu olarak ayarlama

1. **Ayarlar** > **Parametreler**'e gidin. 
2. **Parametreler** sayfasındaki **Tutar Tabanlı Fiyatlandırma Boyutları** sekmesinde, **Fiyatlandırma Boyutları** varlığındaki kayıtları gösteren sekmedeki ızgarayı doğrulayın.
3. **İşlem Kategorisi**'ni bu listeye ekleyin ve **Maliyet için Geçerli** ve **Satış için Geçerli** alanlarını **Evet** olarak ayarlayın.
4. **Boyut Türü** alanında, **Tutar tabanlı** öğesini ve ardından maliyet ve satışla ilgili **İşlem Kategorisi** için önceliği seçin.


[!INCLUDE[footer-include](../includes/footer-banner.md)]