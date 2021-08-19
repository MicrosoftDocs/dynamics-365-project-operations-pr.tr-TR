---
title: Proje sözleşmelerinde proje fiyat listelerini yönetme
description: Bu konu proje sözleşmeleri üzerinde proje fiyat listelerinin yönetilmesi hakkında bilgi sağlar.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 824026d0620de809c0366c86c2d4d13fe83d4d1ddd4c0dc1cc2645ff712705d5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996505"
---
# <a name="manage-project-price-lists-on-project-contracts"></a>Proje sözleşmelerinde proje fiyat listelerini yönetme

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Dynamics 365 Project Operations'ta proje sözleşmeleri, bir sözleşmede birden fazla tarihe duyarlı satış fiyat listesini desteklemek için tasarlanmıştır. Project Operations, **Proje fiyat listeleri** olarak adlandırılan yeni bir ilişkili varlık vardır. Bu varlık bir proje sözleşmesiyle bire çok ilişkiye sahiptir.

Proje fiyat listeleri, bir projedeki süre, malzeme ve gider hareketlerinin fiyatlarını belirlemek için kullanılır. Bir sözleşmede bir veya daha fazla proje fiyat listesi varsa bu fiyat listeleri, sözleşme satırı üzerinden sözleşmeyle ilişkili projelerde zaman, malzeme, gider tahminleri ve gerçek değerler için fiyat sağlamak amacıyla kullanılır.

Bir proje sözleşmesinde proje fiyat listesi olmadığında, proje fiyat listelerinin olmadığına ve tahminlerinizin, gerçek proje çalışmasının, malzemenin ve günlüğe kaydedilen giderlerin fiyatlandırılmayacağını belirten bir uyarı iletisi görürsünüz. Satış değerleri için fiyat yoktur.

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a>Proje sözleşmesindeki proje fiyat listesini ilişkilendirme veya ilişkilendirmeyi kaldırma

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-material-and-expenses"></a>Proje tabanlı çalışmayı, malzemeyi ve giderleri tahmin etmek için belirli bir fiyat listesi oluşturma veya ilişkilendirme

1. Proje sözleşmesinde, **Proje fiyat listeleri** sekmesini seçin.
2. Alt ızgarada, **+ Yeni proje fiyat listesi Ekle**'yi seçin.
3. **Hızlı kayıt** kaydırıcısının içinde bir fiyat listesi seçin. 

  Açılan liste, Fiyat listesindeki para biriminin sözleşmedeki para birimiyle eşleştiği **Satış** olarak ayarlanmış içeriğe sahip tüm fiyat listelerini gösterir.
  
4. Proje fiyat listesi ilişkilendirmesi için bir açıklama girin ve ardından **hızlı kayıt** kaydırıcısını kapatmak için **Kaydet**'i seçin.

   Proje fiyat listesi ilişkisi oluşturulur.
   
5. Birden çok proje fiyat listesini proje sözleşmesiyle ilişkilendirmek için 1-4 arasındaki adımları yineleyin. Birden çok proje fiyat listesi oluşturarak, her bir ilişkilendirilmiş proje fiyat listesinin her birinde farklı tarih efektlerinizin olması gerekir.

> [!NOTE]
> Project Operations proje fiyat listelerinin Tarih efektinin çakışmasına kadar örtüşmesini desteklemez. Belirli bir tarihe sahip bir hareket için birden çok proje fiyatı listesi varsa, bu hareketteki fiyat varsayılan olarak sıfıra kaydedilir.

### <a name="remove-a-project-price-list-association"></a>Proje fiyat listesi ilişkisini kaldır

- Proje fiyat listesini seçin ve ardından alt ızgarada **sözleşme proje fiyat listesini sil**'i seçin. 

  Fiyat listesi, sözleşmedeki proje fiyat listelerinden kaldırılır. Fiyat listesi silinmez. Yalnızca sözleşmeyle ilişkilendirme silinir.

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a>Bir sözleşmede proje fiyat listelerinin otomatik olarak varsayılan durumunu ayarlama

Bir proje fiyat listesi, varsayılan proje fiyat listesi olarak ayarlanabilir. Bu kurulum, kuruluşunuzdaki tüm sözleşmelerin her zaman için bu fiyat dönemi için bir standart proje fiyat listesiyle başlamasını sağlar.

### <a name="set-up-the-organizational-default-for-project-price-lists"></a>Proje fiyat listeleri için organizasyon varsayılanını ayarlama

1. **Ayarlar** > **Genel** bölümüne gidin ve **parametreler**'i seçin.
2. **Etkin parametreler** listesi sayfasında, kaydı seçip çift tıklatarak açın. Çift tıklatıldığında, köprü olan bir alan değerini tıklattığınızdan emin olun. 
3. **Etkin Parametreler** sayfasında, **Fiyat listesi** sekmesini seçin. Bir alt ızgara, varsayılan fiyat listelerinin listesini gösterir. Bu, standart maliyet ve satış fiyatı listelerinin listesidir. Uygulamasında satış yaptığınız her para birimi için burada ilişkilendirilmiş bir **satış** fiyatı listesi varsa, satış fiyatı listesi bu para birimiyle işlem oluşturduğunuz herhangi bir sözleşmede varsayılan olur.

### <a name="set-up-a-customer-specific-project-price-list"></a>Müşteriye özel proje fiyat listesi ayarlama

Müşterilerinizle bir ana fiyatlandırma anlaşması konusunda anlaştığınız zaman, müşteriye özgü proje fiyat listelerini de ayarlayabilirsiniz.

1. **Satış** > **Müşteriler**'e gidin.
2. Etkin firmalar listesinden, özel fiyat listesi olan müşteriyi seçin.
3. Açılacak müşteri kaydını seçin ve **Proje fiyat listeleri** sekmesini seçin. Alt ızgara, bu müşteriye özgü proje fiyat listelerinin listesini gösterir. 
4. Burada, bu müşteriye özgü proje fiyatı listesi oluşturmak için yeni bir fiyat listesi ilişkilendirmesi oluşturun.

## <a name="custom-pricing-on-a-project-contract"></a>Proje sözleşmesi üzerinde özel fiyatlandırma

Kuruluş ve müşteriye özel varsayılan proje fiyat listeleri aldıktan sonra, proje sözleşmeleriniz bu proje fiyat listesi ilişkilendirmeleriyle otomatik olarak oluşturulur. Ancak, bir proje sözleşmesindeki proje fiyat listeleri her zaman bunlara eklenen tarih ve sözleşme adıyla birlikte kopyalanır. Daha sonra firma ve proje yöneticileri bu kopyalarda fiyatlarda düzenlemeler yapmaya başlayabilir. Bu değiştirilen fiyatlar yalnızca bu proje sözleşmesine uygulanabilir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
