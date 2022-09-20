---
title: Proje tahmini ve gerçek değerleri için maliyet oranlarını belirleme
description: Bu makale proje tahmini ve gerçek değerleriyle ilgili maliyet oranlarının nasıl belirleneceği hakkında bilgi sağlar.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c2295174df1ce766c6d1304f4e9c55d32d5c4775
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475260"
---
# <a name="determine-cost-rates-for-project-estimates-and-actuals"></a>Proje tahmini ve gerçek değerleri için maliyet oranlarını belirleme

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Microsoft Dynamics 365 Project Operations'ta tahminlerdeki maliyet oranlarını ve fiili değerleri belirlemek için sistem, maliyet fiyatı listesini belirlemek için ilk olarak, gelen tahmini veya fiili değer bağlamındaki tarihi ve para birimini kullanır. Özellikle de gerçek bağlamda sistem, hangi fiyat listesinin geçerli olduğunu belirlemek için **Hareket tarihi** alanını kullanır. Gelen tahminin veya fiili değerin **İşlem tarihi** değeri fiyat listesindeki **Geçerlilik Başlangıcı (saat diliminden bağımsız)** ve **Geçerlilik bitişi (saat diliminden bağımsız)** değerleri ile karşılaştırılır. Maliyet fiyat listesi belirlendikten sonra sistem maliyet oranını belirler. 

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Zaman için tahmini ve gerçek bağlamlarda maliyet oranlarını belirleme

**Zaman** için tahmin bağlamı şuna başvurur:

- **Zaman** için teklif satırı ayrıntıları.
- **Zaman** için sözleşme satırı ayrıntıları.
- Projedeki kaynak atamaları.

**Zaman** için gerçek bağlam şuna başvurur:

- **Zaman** için Giriş ve Düzeltme yevmiye defteri satırları.
- Bir zaman girişi gönderildiğinde oluşturulan yevmiye defteri satırları.

Bir maliyet fiyatı listesi belirlendiğinde sistem, varsayılan maliyet oranını girmek için aşağıdaki adımları tamamlar.

1. Sistem, **Zaman** için tahmini veya gerçek bağlamdaki **Rol** ve **Kaynak Birimi** alanları kombinasyonunu fiyat listesindeki rol fiyat satırlarıyla eşleştirir. Bu eşleştirme, işçilik maliyeti için standart fiyatlandırma boyutlarını kullandığınızı varsayar. Sistemi, **Rol** ve **Kaynak Birimi** alanları dışındaki veya bu alanlara ek alanlarla eşleşecek şekilde yapılandırdıysanız eşleşen bir rol fiyat satırını almak için farklı bir kombinasyon kullanılır.
1. Sistem, **Rol** ve **Kaynak Birimi** kombinasyonu için bir maliyet oranına sahip bir rol fiyat satırı bulursa bu maliyet oranı varsayılan maliyet oranı olarak kullanılır.
1. Sistem, **Rol** ve **Kaynak Birimi** değerlerini eşleştiremiyorsa, **Rol** alanı için eşleşen değerlere sahip ancak **Kaynak Birimi** alanı için boş değerlere sahip rol fiyat satırlarını alır. Sistem eşleşen bir rol fiyatı kaydı bulduktan sonra, bu kayıttan gelen maliyet oranı varsayılan maliyet oranı olarak kullanılır.

> [!NOTE]
> **Rol** ve **Kaynak Birimi** alanlarının farklı bir önceliklendirmesini yapılandırırsanız veya daha yüksek önceliğe sahip başka boyutlara sahipseniz, önceki davranış buna göre değişecektir. Sistem, her fiyatlandırma boyutu değeriyle eşleşen değerleri olan rol fiyatı kayıtlarını öncelik sırasına göre alır. Bu boyutlar için boş değer içeren satırlar en son gelir.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Gider için fiili ve tahmin satırlarındaki maliyet oranlarını belirleme

**Gider** için tahmin bağlamı şuna başvurur:

- **Gider** için teklif satırı ayrıntıları.
- **Gider** için sözleşme satırı ayrıntıları.
- Projeye ilişkin gider tahminleri.

**Gider** için gerçek bağlam şuna başvurur:

- **Gider** için Giriş ve Düzeltme yevmiye defteri satırları.
- Bir gider girişi gönderildiğinde oluşturulan yevmiye defteri satırları.

Bir maliyet fiyatı listesi belirlendiğinde sistem, varsayılan maliyet oranını girmek için aşağıdaki adımları tamamlar.

1. Sistem, **Gider** için tahmini veya gerçek bağlamdaki **Kategori** ve **Birim** satırları kombinasyonunu fiyat listesindeki kategori fiyat satırlarıyla eşleştirir.
1. Sistem, **Kategori** ve **Birim** alanları birleşimi için maliyet oranına sahip bir kategori fiyat satırı bulursa, bu maliyet oranı varsayılan maliyet oranı olarak kullanılır.
1. Sistem, **Kategori** ve **Birim** değerlerini eşleştiremiyorsa fiyat varsayılan olarak **0**'a (sıfır) ayarlanır.
1. Tahmin bağlamında sistem, eşleşen bir kategori fiyatı satırı bulabiliyorsa ancak fiyatlandırma yöntemi **Birim Fiyatı** dışında bir seçeneğe ayarlıysa maliyet oranı varsayılan olarak **0** (sıfır) olur.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-material"></a>Malzemenin gerçek ve tahmin satırlarında maliyet oranlarını belirleme

**Malzeme** için tahmin bağlamı şuna başvurur:

- **Malzeme** için teklif satırı ayrıntıları.
- **Malzeme** için sözleşme satırı ayrıntıları.
- Projeye ilişkin malzeme tahminleri.

**Malzeme** için gerçek bağlam şuna başvurur:

- **Malzeme** için Giriş ve Düzeltme yevmiye defteri satırları.
- Bir Malzeme kullanım günlüğü gönderildiğinde oluşturulan yevmiye defteri satırları.

Bir maliyet fiyatı listesi belirlendiğinde sistem, varsayılan maliyet oranını girmek için aşağıdaki adımları tamamlar.

1. Sistem, **Malzeme** için tahmini veya gerçek bağlamdaki **Ürün** ve **Birim** satırları kombinasyonunu fiyat listesindeki fiyat listesi kalemi satırlarına karşı kullanır.
1. Sistem, **Ürün** ve **Birim** alanları birleşimi için maliyet oranına sahip bir fiyat listesi kalemi bulursa, bu maliyet oranı varsayılan maliyet oranı olarak kullanılır.
1. Sistem, **Ürün** ve **Birim** değerlerini eşleştiremiyorsa birim maliyet varsayılan olarak **0** (sıfır) olur.
1. Tahmini veya gerçek bağlamda sistem, eşleşen bir fiyat listesi kalemi satırı bulabiliyorsa ancak fiyatlandırma yöntemi **Para birimi tutarı** dışında bir seçeneğe ayarlıysa birim maliyet varsayılan olarak **0** (sıfır) olur. Bu davranış, Project Operations yalnızca bir projede kullanılan malzemeler için **Para birimi tutarı** fiyatlandırma yöntemini desteklediği için oluşur.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
