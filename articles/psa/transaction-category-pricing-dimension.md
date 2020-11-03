---
title: İşlem kategorisini fiyatlandırma boyutu olarak kullanma
description: Bu konu, işlem kategorisini fiyatlandırma boyutu olarak kullanma hakkında bilgi sağlar.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
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
ms.openlocfilehash: 0019571a1d37d3b6a503e7221db3c3b51365c236
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086408"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>İşlem kategorisini fiyatlandırma boyutu olarak kullanma
Bu konu, bir işlem kategorisinin fiyatlandırma boyutu olarak nasıl kullanılacağını gösterir. Başlamadan önce, önceden bir fiyatlandırma boyutu çözümü oluşturmadıysanız yeni bir tane oluşturmanız gerekir. Zaten bir fiyatlandırma boyutu çözümünüz varsa değişikliklerinizi bu çözümde yapabilirsiniz. Kuruluşunuz için yeni bir fiyatlandırma boyutu çözümü oluşturmadıysanız [Özel alanlar ve varlıklar oluşturma](create-custom-fields-entities.md) konu başlığındaki yordamları tamamlayın.

## <a name="add-transaction-category-to-forms-and-views"></a>Formlara ve görünümlere işlem kategorisi ekleme
Fiyatlandırma boyutu çözümünde, kullanıcı arabiriminde işlem kategorisini görünür kılmak için önemli varlıkların tüm formlarını ve görümlerini incelemeniz ve bu alanları bu varlıkların formlarına ve görünümlerine eklemeniz gerekir.
Aşağıdaki tabloda, yeni alanlarla güncelleştirilmesi gereken, varlığa göre listelenen kullanıma hazır form ve görünümlerin kapsamlı bir listesi yer alır. Bu varlıklardaki özelleştirmelerinizde ek görünümler veya formlar varsa yeni alanları da bunlara ekleyin.

|  Varlık        | Formlar     |Görünümler        |
| ------------------------------|---------------------------------|----------------------------------|
|  Rol Fiyatı|• Bilgi |• Etkin Kaynak Kategorisi Fiyatları<br> • Kaynak Kategorisi Fiyatı İlişkili Görünümü|
|  Rol Fiyatı Kar Payı|• Bilgi|• Etkin Rol Fiyatı Kar Payı<br>• Rol Fiyatı Kar Payı İlişkili Görünümü|
|  Teklif satırı ayrıntısı|• Proje Bilgileri<br>• Hızlı Proje Oluştur|• Etkin Teklif Satırı Ayrıntısı<br>• Birleşik Teklif Satırı Ayrıntıları<br>• Teklif Satırı Ayrıntısı ilişkili görünümü|
|  Proje Sözleşme satırı ayrıntısı|• Proje Bilgileri<br>• Hızlı Proje Oluştur|• Birleşik Sözleşme satırı Ayrıntıları<br>• Etkin Sözleşme Satırı Ayrıntıları<br>• Sözleşme Satırı Ayrıntısı ilişkili görünümü|
|  Proje Görevi|• Bilgi<br>• Yeni Form||
|  Proje Takımı Üyesi|• Bilgi<br>• Yeni Form|• Etkin Proje Takımı Üyeleri<br>• Proje Takımı Üyeleri<br>• Proje Takımı üyeleri ilişkili görünümü|
|  Zaman Girişi|• Bilgi<br>• Zaman Girişi Oluştur|• Tarihe Göre Zaman Girişlerim<br>• Bu hafta için Zaman Girişlerim<br>• Onaylanacak zaman girişleri|
|  Yevmiye Defteri Satırı|• Bilgi<br>• Hızlı oluşturma|• Etkin yevmiye defteri satırları<br>• Yevmiye Defteri Satırı ilişkili görünümü|
|  Fatura Satırı Ayrıntısı|• Bilgi<br>• Hızlı oluşturma|• Etkin Fatura Satırı Ayrıntıları<br>• Borçlandırılabilir Fatura İşlemleri<br>• Ücretsiz Fatura İşlemleri<br>• Fatura Satırı Ayrıntısı ilişkili görünümü<br>• Borçlandırılamaz Fatura İşlemleri|
|  Gerçek|• Bilgi<br>• Etkin Gerçek Tutarlar|• Gerçek Tutar İlişkili görünümü|

## <a name="set-up-transaction-category-as-a-pricing-dimension"></a>İşlem kategorisini fiyatlandırma boyutu olarak ayarlama

1. Web arabiriminde **Project Service** > **Ayarlar** > **Parametreler** 'e gidin. 
2. **Parametreler** sayfasındaki **Tutar Tabanlı Fiyatlandırma Boyutları** sekmesinde, **Fiyatlandırma Boyutları** varlığındaki kayıtları gösteren sekmedeki ızgarayı not edin.
3. **İşlem Kategorisi** 'ni bu listeye ekleyin ve **Maliyet için Geçerli** ve **Satış için Geçerli** alanlarını **Evet** olarak ayarlayın.
4. **Boyut Türü** alanında **Tutar tabanlı** öğesini ve ardından maliyet ve satışla ilgili **İşlem Kategorisi** için önceliği seçin.
