---
title: Ayrılabilir kaynağı fiyatlandırma boyutu olarak kullanma
description: Bu konu, ayrılabilir kaynağı fiyatlandırma boyutu olarak kullanma hakkında bilgi sağlar.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 7b07ac8659c9eccf3db41775acf5ca2043016a59
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576432"
---
# <a name="use-bookable-resource-as-a-pricing-dimension"></a>Ayrılabilir kaynağı fiyatlandırma boyutu olarak kullanma

[!include [banner](../includes/psa-now-project-operations.md)]

Bu konu, ayrılabilir kaynağı fiyatlandırma boyutu olarak kullanma hakkında bilgi sağlar. Başlamadan önce, önceden bir fiyatlandırma boyutu çözümü oluşturmadıysanız yeni bir tane oluşturmanız gerekir. Zaten bir fiyatlandırma boyutu çözümünüz varsa değişikliklerinizi bu çözümde yapabilirsiniz. Kuruluşunuz için yeni bir fiyatlandırma boyutu çözümü oluşturmadıysanız [Özel alanlar ve varlıklar oluşturma](create-custom-fields-entities.md) konu başlığındaki yordamları tamamlayın.

## <a name="add-bookable-resource-to-forms-and-views"></a>Formlara ve görünümlere ayrılabilir kaynak ekleme
Fiyatlandırma boyutu çözümünde, kullanıcı arabiriminde alanları görünür kılmak için önemli Project Service varlıklarının tüm formlarını ve görümlerini incelemeniz ve bu alanları bu varlıkların formlarına ve görünümlerine eklemeniz gerekir.
Aşağıdaki tabloda, güncelleştirilmesi gereken, varlığa göre listelenen kullanıma hazır form ve görünümlerin kapsamlı bir listesi yer alır. Bu varlıklardaki özelleştirmelerinizde ek görünümler veya formlar varsa yeni alanları da bunlara ekleyin.
Fiyatlandırma boyutu çözümü için Çözüm Gezgini'ni açın ve **Tüm Özelleştirmeleri Yayımla**'ya tıklayın.


|   Varlık        | Formlar   |Görünümler        |
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

## <a name="set-up-bookable-resource-as-a-pricing-dimension"></a>Ayrılabilir kaynağı fiyatlandırma boyutu olarak ayarlama

1. Web arabiriminde **Project Service** > **Ayarlar** > **Parametreler**'e gidin. **Parametre** sayfasındaki **Tutar Tabanlı Fiyatlandırma Boyutları** sekmesinde, fiyatlandırma boyutları varlığındaki kayıtları gösteren sekmedeki ızgarayı not edin. 
2. Bu fiyatlandırma boyutları listesine **msdyn_bookableresource** olarak **Ayrılabilir Kaynak** ekleyin. 
3. Ayrılabilir kaynağının bir fiyatlandırma boyutu olarak çalıştığı bağlamı belirtin ve **Maliyet için geçerli** ve **Satış için geçerli** değerlerini ayarlayın.
4. **Boyut Türü** alanında, **Miktar tabanlı**'yı seçin. 
5. Ayrılabilir kaynak için maliyet ve satış önceliğini seçin. Tipik olarak, bir fiyatlandırma boyutu olarak eklendiğinde, ayrılabilir kaynak en yüksek önceliğe sahiptir ve bu nedenle **1** (veya önceliği nasıl saydığınıza bağlı olarak **0**) olarak ayarlamak bu davranışın gerçekleştirilmesini sağlar.

## <a name="set-up-pricing-dimension-field-names"></a>Fiyatlandırma boyutu alan adlarını ayarlama

**Rol Fiyatı** tablosundaki fiyatlandırma boyutunun alan adı, fiyat varsayılan girişinin çalışması gereken diğer herhangi bir varlıktaki alan adından farklıysa, fiyatlandırma boyutu kaydının farklı adlar konusunda bilgilendirilmesi gerekir.    
Ayrılabilir kaynak için, **Proje Takımı Üyeleri** varlığı, **Rol fiyatı** varlığındaki adından (**msdyn_bookableresource**) biraz farklı bir alan adına (**msdyn_bookableresourceid**) sahiptir. **msydn_bookableresource** için fiyatlandırma boyutu kaydının bunu bilmesi sağlanmalıdır. 
1. Bunu yapmak için **msdyn_bookableresource** boyut sayfasını açmak üzere **Fiyatlandırma Boyutları** ızgarasında satıra çift tıklayın.
2. Boyut sayfasında **İlgili** sekmesinde, **Fiyatlandırma Boyutu Alan Adları**'na tıklayın.

 ![Fiyatlandırma boyutu alan adları sekmesi.](media/PD-fieldname.png)

4. Açılan ilişkilendirilmiş görünümde **Yeni Fiyatlandırma Boyutu Alan Adı Ekle**'ye tıklayın.

 ![Yeni Fiyatlandırma Boyutu Alan Adları Ekle.](media/Add-NewPD-fieldname.png)


Bu, **msdyn_bookableresource** için **Yeni Fiyatlandırma boyutu alan adı** sayfasını açar. 

5. **msdyn_projectteam** öğesini **Varlık Mantıksal Adı** alanına **msdyn_bookableresourceid** öğesini **Alan Adı** alanına ekleyin. Kaydı kaydedin.

 ![Yeni Fiyatlandırma boyutu alan adı formu.](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
