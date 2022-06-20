---
title: Ayrılabilir kaynağı bir fiyatlandırma boyutu olarak kullanma
description: Bu makale, ayrılabilir kaynağı fiyatlandırma boyutu olarak kullanma hakkında bilgi sağlar.
author: Rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c467c45885bbd8931eccc75862f537c0f46433ef
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914840"
---
# <a name="use-a-bookable-resource-as-a-pricing-dimension"></a>Ayrılabilir kaynağı bir fiyatlandırma boyutu olarak kullanma

 _**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_ 

Bu makale, ayrılabilir kaynağı fiyatlandırma boyutu olarak kullanma hakkında bilgi sağlar. Fiyatlandırma stratejiniz, her ayrılabilir kaynağın belirli bir fiyat veya maliyet oranına sahip olması gerektiği şekilde ayarlandıysa fiyatlandırma boyutu olarak ayrılabilir bir kaynak kullanın.

## <a name="prerequisites"></a>Önkoşullar
Bu makaledeki yordamları tamamlamadan önce, organizasyonunuz için yeni bir fiyatlandırma boyutu çözümünüz olması gerekir. Henüz bir tane oluşturmadıysanız bkz. [Özel alanlar ve varlıklar oluşturma](../pricing-costing/create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-bookable-resource-field-to-forms-and-views"></a>Ayrılabilir Kaynak alanını formlara ve görünümlere ekleme
Fiyatlandırma boyutu çözümünde **Ayrılabilir Kaynak** alanını görünür hale getirmek için alanı tüm formlara ve görünümlere varlık olarak eklemeniz gerekir.

Aşağıdaki tabloda tüm kullanıma hazır formlar ve görünümler varlığa göre listelenmektedir. Yeni alanı, özelleştirilmiş varlıklarınızdaki ek formlara veya görünümlere de eklemeniz gerekir.

|   Entity        | Formlar   |Görünümler        |
| ------------------------------|---------------------------------|----------------------------------|
|  Rol Fiyatı| Bilgiler | - Etkin Kaynak Kategorisi Fiyatları<br> - İlişkili Kaynak Kategorisi Fiyatı |
|  Rol Fiyatı Kar Payı| Bilgiler| - Etkin Rol Fiyatı Kar Payı<br>- İlişkili Rol Fiyatı Kar Payı |
|  Teklif satırı ayrıntısı| - Proje Bilgileri<br>- Hızlı Proje Oluştur| - Etkin Teklif Satırı Ayrıntısı<br>- Birleşik Teklif Satırı Ayrıntıları<br>- İlişkili Teklif Satırı Ayrıntısı |
|  Proje Sözleşme satırı ayrıntısı| - Proje Bilgileri<br>- Hızlı Proje Oluştur| - Birleşik Sözleşme Satırı Ayrıntıları<br>- Etkin Sözleşme Satırı Ayrıntıları<br>- İlişkili Sözleşme Satırı Ayrıntısı |
|  Proje Görevi| - Bilgi<br>- Yeni Form| &nbsp; |
|  Proje Takımı Üyesi| - Bilgi<br>- Yeni Form| - Etkin Proje Takımı Üyeleri<br>- Proje Takımı Üyeleri<br>- İlişkili Proje Takımı üyeleri |
|  Zaman Girişi| - Bilgi<br>- Zaman Girişi Oluştur| - Tarihe Göre Zaman Girişlerim<br>- Bu Hafta için Zaman Girişlerim<br>- Onaylanacak Zaman Girişleri|
|  Yevmiye Defteri Satırı| - Bilgi<br>- Hızlı Oluştur| - Etkin Yevmiye Defteri Satırları<br>- İlişkili Yevmiye Defteri Satırı |
|  Fatura Satırı Ayrıntısı| - Bilgi<br>- Hızlı Oluştur| - Etkin Fatura Satırı Ayrıntıları<br>- Borçlandırılabilir Fatura İşlemleri<br>- Ücretsiz Fatura İşlemleri<br>- İlişkili Fatura Satırı Ayrıntısı <br>- Borçlandırılamaz Fatura İşlemleri|
|  Gerçek| - Bilgi<br>- Etkin Gerçek Tutarlar| İlişkili Gerçek Tutar |

## <a name="set-up-a-bookable-resource-as-a-pricing-dimension"></a>Ayrılabilir kaynağı bir fiyatlandırma boyutu olarak ayarlama
Ayrılabilir kaynağı bir fiyatlandırma boyutu olarak ayarlamak için şu adımları izleyin:

1. **Ayarlar** > **Parametreler**'e gidin. 
2. **Parametre** sayfasındaki **Tutar Tabanlı Fiyatlandırma Boyutları** sekmesinde, **Fiyatlandırma Boyutları** varlığındaki kayıtları gösteren sekmedeki ızgarayı doğrulayın. 
2. Bu fiyatlandırma boyutları listesine **msdyn_bookableresource** olarak **Ayrılabilir Kaynak** ekleyin. 
3. **Maliyet için geçerli** ve **Satış için geçerli** içinde bir değer seçin.
4. **Boyut Türü**'nde, **Miktar tabanlı**'yı seçin. 
5. Ayrılabilir kaynak için maliyet ve satış önceliğini seçin. Genellikle ayrılabilir bir kaynak, fiyatlandırma boyutu olarak eklendiğinde en yüksek önceliğe sahiptir. Bu davranışı sağlamak için önceliği **1** (veya önceliği nasıl saydığınıza bağlı olarak **0**) olarak ayarlayın.

## <a name="set-up-pricing-dimension-field-names"></a>Fiyatlandırma boyutu alan adlarını ayarlama

**Rol Fiyatı** tablosundaki bir fiyatlandırma boyutunun alan adı, varsayılan fiyatın kullanıldığı diğer varlıkların herhangi birindeki alan adından farklıysa fiyatlandırma boyutu kaydına farklı adlar bildirilmelidir.  

Ayrılabilir bir kaynak için **Proje Takımı Üyeleri** varlığı, **Rol Fiyatı** varlığındaki adından biraz farklı bir alan adına sahiptir: 

 - **Proje Takımı Üyeleri** varlığı = **msdyn_bookableresourceid**
 - **Rol Fiyatı** varlığı = **msdyn_bookableresource**

**msydn_bookableresource** için fiyatlandırma boyutu kaydına bu fark bildirilmelidir.

1. **msdyn_bookableresource** boyut sayfasını açmak üzere **Fiyatlandırma Boyutları** ızgarasında satıra çift tıklayın.
2. Boyut sayfasında **İlgili** sekmesinde, **Fiyatlandırma Boyutu Alan Adları**'nı seçin.

  ![Fiyatlandırma boyutu alan adları sekmesi.](media/PD-fieldname.png)

3. Açılan ilişkili görünümde **Yeni Fiyatlandırma Boyutu Alan Adı Ekle**'yi seçin.

  ![Yeni Fiyatlandırma Boyutu Alan Adları Ekle.](media/Add-NewPD-fieldname.png)

  Bu, **msdyn_bookableresource** için **Yeni Fiyatlandırma boyutu alan adı** sayfasını açar. 

4. **Yeni Fiyatlandırma Boyut Alanı Adı** sayfasında, **msdyn_projectteam** öğesini **Varlık Mantıksal Adı**'na ekleyin.
5. **msdyn_bookableresourceid** öğesini **Alan Adı**'na ekleyin.

 ![Yeni Fiyatlandırma boyutu alan adı formu.](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]