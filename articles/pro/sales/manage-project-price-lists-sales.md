---
title: Proje tekliflerinde proje fiyat listelerini yönetme - lite
description: Bu konuda, tekliflerde proje fiyat listeleriyle çalışma hakkında bilgiler sağlanmaktadır. (Sales)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d48da44f382e329a978a8ceee59c354d009f2114
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273042"
---
# <a name="manage-project-price-lists-on-project-quotes---lite"></a>Proje tekliflerinde proje fiyat listelerini yönetme - lite

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Proje teklifleri, birden çok tarihte etkin satış fiyatı listelerini desteklemek için tasarlanmıştır. Dynamics 365 Project Operations ile, **Proje fiyat listeleri** adı verilen yeni bir ilişkili varlık eklenir. Bu varlıkta, proje teklifi için 1-çok ilişkisi bulunur.

Proje fiyat listeleri, projedeki fiyat süresi ve gider hareketleri için kullanılır. Bir teklifte bir veya daha fazla proje fiyat listesi olduğunda bu fiyat listeleri, teklif satırı üzerinden teklifle ilişkilendirilen projelerdeki zaman ve gider tahminlerini ve gerçek değerleri fiyatlandırmak için kullanılır.

Proje teklifinde proje fiyat listesi olmadığında bir uyarı iletisi alırsınız. İletide, proje fiyat listesi olmadığından tahmini ve gerçek proje işi ve giderlerinin fiyatlandırılmayacağı belirtilir. Bunun yerine, satış değerleri için fiyat sıfır (0) olur.

## <a name="associate-or-disassociate-a-project-price-list-on-a-project-quote"></a>Proje teklifinde proje fiyat listesi ilişkilendirme veya ilişkisini kaldırma

Proje tabanlı iş ve giderleri tahmin etmek için belirli bir fiyat listesi oluşturmak veya seçmek üzere aşağıdaki adımları tamamlayın.

1. Teklifte **Proje Fiyatı** sekmesini seçin ve alt ızgarada **+ Yeni Proje Fiyat Listesi Ekle** seçeneğini belirleyin.
2. Hızlı Oluştur sayfasında bir fiyat listesi seçin. Açılır liste, **Satış** olarak ayarlanan bağlama sahip tüm fiyat listelerini gösterir ve para birimi, teklifteki para birimi ile eşleşir.
4. Proje fiyat listesi ilişkisi için bir açıklama girin ve **Kaydet ve Kapat**'ı seçin.

Proje fiyat listesi ilişkisi oluşturulur.

Proje teklifi ile birden çok proje fiyat listesini ilişkilendirmeniz gerekirse bu işlemi tekrarlayabilirsiniz. Yalnızca ilişkilendirilen proje fiyat listelerinin her birinde farklı geçerlilik tarihleri varsa birden çok proje fiyat listesi oluşturun.

> [!NOTE]
> Project Operations, proje fiyat listelerinde çakışan tarih geçerliliğini desteklemez. Belirli bir tarihteki işlem için birden çok proje fiyat listesi varsa bu işlemdeki fiyat varsayılan olarak sıfır (0) olur.
Proje fiyat listesi ilişkisini kaldırmak için proje fiyat listesini seçin ve ardından **Teklif Projesi Fiyat Listesini Sil** seçeneğini belirleyin. Fiyat listesi, teklifin proje fiyat listelerinden kaldırılır ancak fiyat listesinin kendisi silinmez. Yalnızca teklifin ilişkisi silinir.

## <a name="set-up-default-project-price-lists-on-a-quote"></a>Teklifte varsayılan proje fiyat listelerini ayarlama

Proje fiyat listeleri, proje teklifinde varsayılan olarak ayarlanabilir. Bu ayar, kuruluşunuzdaki tüm tekliflerin her zaman bu fiyat dönemi için bir standart fiyat listesiyle başlamasını sağlar.

### <a name="set-up-organizational-default-for-project-price-lists"></a>Proje fiyat listeleri için kuruluş varsayılanını ayarlama

1. **Ayarlar** > **Genel** > **Parametreler**'e gidin.
2. **Etkin Parametreler** listesi sayfasında, kaydı bulun ve açmak için çift tıklayın. 
3. **Parametreler** sayfasında, **Fiyat Listesi** sekmesini seçin. Gösterilen varsayılan fiyat listelerinin listesini görebilirsiniz. Bu, standart maliyet ve satış fiyatı listelerinin listesidir. Satış yaptığınız her para birimi için burada ilişkilendirilmiş bir satış fiyatı listesine sahip olmak, bu satış fiyatı listesinin bu para biriminde işlem yapan müşterilere yönelik oluşturduğunuz tekliflerde varsayılan olmasını sağlar.

### <a name="set-up-customer-specific-project-price-lists"></a>Müşteriye özel proje fiyat listeleri ayarlama

Müşterilerinizle bir ana fiyatlandırma sözleşmesi yaparken ayrıca müşteriye özel proje fiyat listeleri de ayarlayabilirsiniz.

Müşteriye özel proje fiyat listesi ayarlamak için aşağıdaki adımları tamamlayın.

1. **Satış** alanında **Müşteriler**'i seçin.
2. Etkin firmalarınızın listesinde özel fiyat listesi olan müşteri kaydını seçin ve açın.
3. **Proje Fiyat Listeleri** sekmesinde, proje fiyat listesinin bu müşteriye özel olması için yeni bir fiyat listesi ilişkisi oluşturun.

## <a name="create-custom-pricing-on-a-project-quote"></a>Proje teklifinde özel fiyat oluşturma

Kuruluşa ve müşteriye özel varsayılan proje fiyat listeleriniz olduktan sonra proje teklifleriniz, bu proje fiyat listesi ilişkileriyle otomatik olarak oluşturulur. Ancak belirli durumlarda belirli bir proje teklifi için özel fiyat oluşturmanız gerekebilir. 

1. **Proje Teklifi**'ndeki **Proje Fiyat Listesi** sekmesinde alt ızgarada seçilen özel fiyat listesi kaydı olmadığını doğrulayın.
2. **Özel Fiyat Oluştur**'u seçin. Bu işlem, şu anda teklifle ilişkili tüm standart fiyat listelerinin kopyalarını yapar ve bu kopyaları teklifle ilişkilendirir. Standart fiyat listeleri için mevcut ilişkiler kaldırılır. Ardından satış temsilcisi bu kopyalardaki fiyatlarda düzenlemeler yapmaya başlayabilir. Bu değiştirilen fiyatlar yalnızca bu proje teklifi için geçerlidir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]