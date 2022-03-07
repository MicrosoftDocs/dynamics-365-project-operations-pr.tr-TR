---
title: Fiyat listelerini kopyalama
description: Bu konuda Project Operations'ta fiyat listeleri kopyalanması hakkında bilgi sağlanır.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ad09bdce563a48843b3ed96e7aaabd9c0d5960336b9e1c74fddb9b61f760f4cd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003750"
---
# <a name="copy-price-lists"></a>Fiyat listelerini kopyalama

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Dynamics 365 Project Operations'ta fiyat listelerinin kopyalarını oluşturabilirsiniz. Örneğin, geçerli yılın fiyat listesini kullanarak yaklaşan yıl için fiyat listeleri oluşturabilirsiniz.  Veya maliyet için fiyat listelerinden fatura oranları ve satış fiyatları için bir fiyat listesi kopyalayabilirsiniz. 

Fiyat listesinin kopyasını oluşturmak için aşağıdaki adımları izleyin.

1. Kopyasını yapmak istediğiniz fiyat listesini açın ve **Kopyala**'yı seçin.
2. Fiyat listesini kopyalamak için gerekli bilgileri girin. Aşağıdaki tabloda bilgi girerken dikkat edilmesi gereken noktalar gösterilmektedir.

| Alan | Veri Akışı Açıklaması | Aşağı yönlü etki |
| --- | --- | --- |
| Veri Akışı Adı | Kaynak Fiyat listesinin, **-kopyası** eklenmiş olarak adı. | Fiyat listesi, bu değeri tüm liste sayfalarında ve açılan seçeneklerde içerir. |
| Bağlam | Hedef fiyat listesi için istediğiniz bağlamı girin. | **Maliyet** tahminleri ve maliyet fiili değerleri için fiyatı aramak amacıyla maliyet ayarı atanan bir fiyat listesi kullanılır. **Satış** tahminleri ve satış fiili değerleri için fiyatı aramak amacıyla satış ayarı atanan bir fiyat listesi kullanılır. Yalnızca bir müşteri, teklif veya sözleşme için yalnızca içeriği **Satış** olarak ayarı yapılmış fiyat listeleri bir proje fiyat listesine iliştirilebilir. |
| Başlangıç Tarihi | Fiyat listesinin geçerli olduğu dönemin başlangıç tarihi. | **Bitiş tarihiyle** birlikte bu alan belirli bir tahmin veya gerçek satır için hangi fiyat listesinin geçerli olduğunu belirlemek için kullanılır. |
| Bitiş Tarihi | Fiyat listesinin geçerli olduğu dönemin bitiş tarihi. | **Başlangıç tarihiyle** birlikte bu alan belirli bir tahmin veya gerçek satır için hangi fiyat listesinin geçerli olduğunu belirlemek için kullanılır. |
| Para birimi | Kaynak Fiyat listesinin para birimi. Bu değiştirilebilir. | Bu değiştirildiğinde, işçilik, gider ve ürün kataloğu öğelerine yönelik tüm ortaya çıkan fiyat satırları kopya sırasında hedef fiyat listesi para birimine dönüştürülür. |
| Zaman Birimi | Kaynak Fiyat listesinin para birimi. Bu değiştirilebilir. | Bu değiştirildiğinde, işçilik öğelerine yönelik tüm ortaya çıkan fiyat satırları kopya sırasında hedef fiyat listesi birimi para birimine dönüştürülür. Kaynak Fiyat listesi zaman birimi ve hedef fiyat listesi zaman biriminin birim kurulumundan dönüştürme kullanılır. |
| Veri Akışı Açıklaması | Kaynak Fiyat listesinin, **-kopyası** eklenmiş olarak açıklaması. Bu bir metin alanıdır ve fiyat listesinin çok satırlı bir açıklamasını kullanmanıza olanak sağlar. | Bu alan, ilgili fiyat listeleri içeren çeşitli varlıklarda fiyat listesindeki **ilişkili** görünümlerde gösterilir. |

3. Fiyat listesini kaydedin. 

## <a name="update-a-price-list-by-applying-a-mark-up-to-all-the-prices"></a>Tüm fiyatlara bir işaret uygulayarak bir fiyat listesini güncelleştirme

1. Bir fiyat listesinin **Rol**, **kategori** ve **Fiyat listesi öğesi** sekmelerinde, alt kılavuzdaki tüm fiyatlar için bir sair gider uygulamak üzere **Fiyatları Güncelleştir**'i seçebilirsiniz. 
2. Açılan iletişim kutusunda, bir işaretleme girin. Ayrıca, belirli bir yüzdeye göre fiyatları azaltmak için negatif bir yüzde işareti de girebilirsiniz. 
3. İletişim sayfasında **Tamam**'ı seçin ve ardından alt kılavuzdaki fiyatların yaptığınız değişiklikleri yansıttığından emin olun.


[!INCLUDE[footer-include](../includes/footer-banner.md)]