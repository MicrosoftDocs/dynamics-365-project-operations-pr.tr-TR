---
title: Proje tahminleri ve gerçek değerler için satış fiyatlarını çözümleme
description: Bu konu, proje tahminleri ve gerçek değerlerinde satış fiyatlarının çözümlenmesi hakkında bilgi sağlar.
author: rumant
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3bf4686b414300370e6b364834b33edad98b7f39
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877380"
---
# <a name="resolve-sales-prices-for-project-estimates-and-actuals"></a>Proje tahminleri ve gerçek değerler için satış fiyatlarını çözümleme

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Tahminler ve gerçek tutarlardaki satış fiyatları Dynamics 365 Project Operations'ta çözümlendiğinde sistem, satış fiyatı listesini çözümlemek için ilk olarak ilgili proje teklifinin veya sözleşmenin tarihini ve para birimini kullanır. Satış fiyatı listesi çözümlendikten sonra, sistem satış veya fatura hızını çözer.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a>Zaman için fiili ve tahmin satırlarındaki maliyet oranlarını çözme

Project Operations'ta süre için tahmin satırları, zaman ve projedeki kaynak atamalarının teklif satırını ve sözleşme satırı ayrıntılarını belirtmek için kullanılır.

Satışlar için fiyat listesi çözüldüğünde, sistem fatura oranının varsayılan olması için aşağıdaki adımları tamamlar.

1. Sistem, çözümlenen Fiyat listesinde rol fiyat satırları ile eşleşme için Zaman için tahmin satırında **Rol** ve **Kaynak Birimi** alanlarını kullanır. Bu eşleşme, işçilik maliyeti için hazır fiyatlandırma boyutları kullandığınızı varsayar. Sistemi, **Rol** ve **Kaynak Birimi** yerine veya buna ek olarak alanları eşleşecek şekilde yapılandırırsanız, eşleşen bir rol fiyat satırını almak için farklı bir kombinasyon kullanılır.
2. Sistem, rol için bir maliyet oranı olan bir rol fiyat satırı bulursa **Rol** ve **Kaynak Birimi** alanı kombinasyonu, bu varsayılan fatura oranıdır.
3. Sistem **Rol** ile eşleşmiyorsa **Kaynak Birimi** değerleri, o zaman eşleşen bir rol ile rol fiyat satırları alır, ancak **Kaynak Birimi** null değerleri. Sistem eşleşen bir rol fiyatı kaydı bulduktan sonra, bu kayıttan gelen fatura hızına varsayılan olarak gönderilir. Bu eşleştirme, **rol** ile ilgili **birimin** Satış fiyatlandırma boyutu olarak göreli önceliği için kullanıma hazır bir konfigürasyonun kutudan geçmiş olduğunu varsayar.

> [!NOTE]
> **Rol** ve **Kaynak Birimi**'nin farklı bir önceliklendirmesini yapılandırırsanız veya daha yüksek önceliğe sahip başka boyutlara sahipseniz, bu davranış buna göre değişecektir. Sistem, öncelik sırasına göre fiyatlandırma boyutu değerlerinin her biriyle eşleşen değerlerle, en son gelen boyutlar için null değerlere sahip satırlarla rol fiyat kayıtlarını alır.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Gider için fiili ve tahmin satırlarındaki maliyet oranlarını çözme

Project Operations'ta gider için tahmin satırları, giderler ve projedeki gider tahmin satırlarının teklif satırını ve sözleşme satırı ayrıntılarını belirtmek için kullanılır.

Satışlar için fiyat listesi çözüldüğünde, sistem birim satış fiyatının varsayılan olması için aşağıdaki adımları tamamlar.

1. Sistem çözümlenen fiyat listesinde kategori fiyat satırları eşleşmesi için gider için tahmin satırında **Ktegori** ve **Birim** alanları kombinasyonunu kullanır.
2. Sistem **Kategori** ve **Birim** alan birleşimi için satış oranına sahip bir kategori fiyat satırı bulursa, maliyet oranı varsayılan olarak.
3. Sistem eşleşen bir kategori fiyatı satırı bulursa, fiyatlandırma yöntemi satış fiyatı varsayılan olarak kullanılabilir. Aşağıdaki tabloda, Project Operations'ta varsayılan gider fiyatı davranışı gösterilmektedir.

    | Bağlam | Fiyatlandırma yöntemi | Varsayılan Fiyat |
    | --- | --- | --- |
    | Tahmin | Birim fiyatı | Kategori fiyat satırına dayalı olarak |
    | &nbsp; | Maliyette | Kategori 0.00 |
    | &nbsp; | Maliyet üzerinde kar payı | Kategori 0.00 |
    | Gerçek | Birim fiyatı | Kategori fiyat satırına dayalı olarak |
    | &nbsp; | Maliyette | İlgili fiili maliyet esas alınarak |
    | &nbsp; | Maliyet üzerinde kar payı | İlgili maliyetin gerçek olduğu birim maliyet oranına göre, kategori fiyatı satırıyla tanımlanan bir sair gider uygular. |

4. Sistem **Kategori** ve **birim** alanı değerlerini eşleyemediğinde satış fiyatı varsayılan olarak sıfırdır (0).

## <a name="resolving-sales-rates-on-actual-and-estimate-lines-for-material"></a>Malzemenin gerçek ve tahmin satırlarında satış oranlarını çözme

Project Operations'ta malzemenin tahmin satırları, malzemelerin teklif satırı ve sözleşme satırı ayrıntılarına ve projedeki malzeme tahmin satırlarını belirtmek için kullanılır.

Satışlar için fiyat listesi çözüldüğünde, sistem birim satış fiyatının varsayılan olması için aşağıdaki adımları tamamlar.

1. Sistem, malzemeyi çözülen fiyat listesindeki fiyat listesi maddesi satırlarıyla eşleştirmek için tahmin satırındaki **Ürün** ve **Birim** alanlarının birleşimini kullanır.
2. Sistem, **Ürün** ve **Birim** alan birleşimi için satış oranına sahip bir fiyat listesi maddesi satırı bulursa ve fiyatlandırma yöntemi **Para birimi tutarı** ise fiyat listesinde belirtilen satış fiyatı kullanılır.
3. **Ürün** ve **Birim** değerleri eşleşmiyorsa satış oranı varsayılan olarak sıfır olur.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
