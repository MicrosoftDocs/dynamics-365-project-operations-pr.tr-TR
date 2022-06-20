---
title: İşlem Kategorisini fiyatlandırma boyutu olarak kullanma
description: Bu makale, fiyatlandırma boyutu olarak Hareket Kategorisi alanını kullanma hakkında bilgi sağlar.
author: rumant
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 648933299616a683b19bbe2f1231caac779bd1f8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911731"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>İşlem Kategorisini fiyatlandırma boyutu olarak kullanma


_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_


Bu makale, fiyatlandırma boyutu olarak **Hareket Kategorisi** alanını kullanma hakkında bilgi verir. 

## <a name="prerequisites"></a>Önkoşullar
Bu makaledeki yordamları tamamlamadan önce, organizasyonunuz için yeni bir fiyatlandırma boyutu çözümünüz olması gerekir. Henüz bir tane oluşturmadıysanız bkz. [Fiyatlandırma boyutları olarak özel alanlar ve varlıklar oluşturma](create-custom-fields-entities-pricing-dimensions.md).

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