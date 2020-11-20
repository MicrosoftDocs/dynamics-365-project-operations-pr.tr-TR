---
title: Tahminler ve gerçek değerler için satış fiyatlarını çözümleme
description: Bu konu, tahminler ve fiili olarak satış fiyatlarının nasıl çözüldüğü hakkında bilgi sağlar.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8c18dd734312b2dd147381169f5c3dc38a68a601
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119577"
---
# <a name="resolve-sales-prices-for-estimates-and-actuals"></a>Tahminler ve gerçek değerler için satış fiyatlarını çözümleme

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Tahminlerin ve gerçek tutarların satış fiyatları Dynamics 365 Project Operations'ta çözümlenmişse, sistem öncelikle satış fiyatı listesini düzeltmek için ilgili Proje teklifinin veya sözleşmenin tarihini ve para birimini kullanır. Satış fiyatı listesi çözümlendikten sonra, sistem satış veya fatura hızını çözer.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a>Zaman için fiili ve tahmin satırlarındaki maliyet oranlarını çözme

Project Operations'ta süre için tahmin satırları, zaman ve projedeki kaynak atamalarının teklif satırını ve sözleşme satırı ayrıntılarını belirtmek için kullanılır.

Satışlar için fiyat listesi çözüldüğünde, sistem fatura oranının varsayılan olması için aşağıdaki adımları tamamlar.

1. Sistem, çözümlenen Fiyat listesinde rol fiyat satırları ile eşleşme için Zaman için tahmin satırında **Rol**, **Kaynak şirket** ve **Kaynak Birimi** alanlarını kullanır. Bu eşleşme, işçilik maliyeti için hazır fiyatlandırma boyutları kullandığınızı varsayar. Sistemi, **Rol**, **Kaynak Şİrket** ve **Kaynak Birimi** yerine veya buna ek olarak alanları eşleşecek şekilde yapılandırırsanız, eşleşen bir rol fiyat satırını almak için farklı bir kombinasyon kullanılır.
2. Sistem, rol için bir maliyet oranı olan bir rol fiyat satırı bulursa **Rol**, **Kaynak Şİrket** ve **Kaynak Birimi** alanı kombinasyonu, bu varsayılan fatura oranıdır.
3. Sistem **Rol**, **Kaynak şirket** ve **Kaynak birim** ile eşleşmiyorsa, o zaman eşleşen bir rol ile rol fiyat satırları alır, ancak **Kaynak Birimi** null değerleri. Sistem eşleşen bir rol fiyatı kaydı bulduktan sonra, bu kayıttan gelen fatura hızına varsayılan olarak gönderilir. Bu eşleştirme, **rol** ile ilgili **birimin** Satış fiyatlandırma boyutu olarak göreli önceliği için kullanıma hazır bir konfigürasyonun kutudan geçmiş olduğunu varsayar.

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
