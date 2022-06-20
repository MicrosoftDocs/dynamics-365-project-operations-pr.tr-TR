---
title: Tahminler ve gerçek değerler için satış fiyatlarını çözümleme
description: Bu makale tahminlerde ve gerçek değerlerle satış oranlarının nasıl çözümleneceği hakkında bilgi sağlar.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ee750b93a5be7be09ed76942c7c235f8c811e8bb
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911850"
---
# <a name="resolve-sales-prices-for-estimates-and-actuals"></a>Tahminler ve gerçek değerler için satış fiyatlarını çözümleme

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Tahminler ve gerçek tutarlardaki satış fiyatları Dynamics 365 Project Operations'ta çözümlendiğinde sistem, satış fiyatı listesini çözümlemek için ilk olarak ilgili proje teklifinin veya sözleşmenin tarihini ve para birimini kullanır. Satış fiyatı listesi çözümlendikten sonra, sistem satış veya fatura hızını çözer.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a>Zaman için fiili ve tahmin satırlarındaki maliyet oranlarını çözme

Project Operations'ta süre için tahmin satırları, zaman ve projedeki kaynak atamalarının teklif satırını ve sözleşme satırı ayrıntılarını belirtmek için kullanılır.

Satışlar için fiyat listesi çözüldüğünde, sistem fatura oranının varsayılan olması için aşağıdaki adımları tamamlar.

1. Sistem, çözümlenen Fiyat listesinde rol fiyat satırları ile eşleşme için Zaman için tahmin satırında **Rol**, **Kaynak şirket** ve **Kaynak Birimi** alanlarını kullanır. Bu eşleşme, işçilik maliyeti için hazır fiyatlandırma boyutları kullandığınızı varsayar. Sistemi, **Rol**, **Kaynak Şİrket** ve **Kaynak Birimi** yerine veya buna ek olarak alanları eşleşecek şekilde yapılandırırsanız, eşleşen bir rol fiyat satırını almak için farklı bir kombinasyon kullanılır.
2. Sistem, rol için bir maliyet oranı olan bir rol fiyat satırı bulursa **Rol**, **Kaynak Şİrket** ve **Kaynak Birimi** alanı kombinasyonu, bu varsayılan fatura oranıdır.
3. Sistem **Rol**, **Kaynak şirket** ve **Kaynak birim** ile eşleşmiyorsa, o zaman eşleşen bir rol ile rol fiyat satırları alır, ancak **Kaynak Birimi** null değerleri. Sistem eşleşen bir rol fiyatı kaydı bulduktan sonra, bu kayıttan gelen fatura hızına varsayılan olarak gönderilir. Bu eşleştirme, **rol** ile ilgili **birimin** Satış fiyatlandırma boyutu olarak göreli önceliği için kullanıma hazır bir yapılandırmanın kutudan geçmiş olduğunu varsayar.

> [!NOTE]
> **Rol**, **Kaynak Şirketi** ve **Kaynak Birimi**'nin farklı bir önceliklendirmesini yapılandırırsanız veya daha yüksek önceliğe sahip başka boyutlara sahipseniz, bu davranış buna göre değişecektir. Sistem, öncelik sırasına göre fiyatlandırma boyutu değerlerinin her biriyle eşleşen değerlerle, en son gelen boyutlar için null değerlere sahip satırlarla rol fiyat kayıtlarını alır.

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

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-material"></a>Malzemenin gerçek ve tahmin satırlarında satış oranlarını çözme

Project Operations'ta malzemenin tahmin satırları, malzemelerin teklif satırı ve sözleşme satırı ayrıntılarına ve projedeki malzeme tahmin satırlarını belirtmek için kullanılır.

Satışlar için fiyat listesi çözüldüğünde, sistem birim satış fiyatının varsayılan olması için aşağıdaki adımları tamamlar.

1. Sistem, malzemeyi çözülen fiyat listesindeki fiyat listesi maddesi satırlarıyla eşleştirmek için tahmin satırındaki **Ürün** ve **Birim** alanlarının birleşimini kullanır.
2. Sistem, **Ürün** ve **Birim** alan birleşimi için satış oranına sahip bir fiyat listesi maddesi satırı bulursa ve fiyatlandırma yöntemi **Para birimi tutarı** ise fiyat listesinde belirtilen satış fiyatı kullanılır.
3. **Ürün** ve **Birim** değerleri eşleşmiyorsa satış oranı varsayılan olarak sıfır olur.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
