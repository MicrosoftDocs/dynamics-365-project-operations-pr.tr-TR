---
title: Proje tabanlı tahminler ve fiili değerler için satış fiyatlarını belirleme
description: Bu makale proje tabanlı tahminler ve fiili değerlerle ilgili satış fiyatlarının nasıl belirleneceği hakkında bilgi sağlar.
author: rumant
ms.date: 09/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f0b95c651983230cbf340f2c06089a287b2c8a10
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475394"
---
#  <a name="determine-sales-prices-for-project-based-estimates-and-actuals"></a>Proje tabanlı tahminler ve fiili değerler için satış fiyatlarını belirleme

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Microsoft Dynamics 365 Project Operations'ta tahminler ve gerçek değerlere ilişkin satış fiyatlarını belirlemek için sistem, satış fiyatı listesini belirlemek için ilk olarak, gelen tahmini veya gerçek bağlamdaki tarihi ve para birimini kullanır. Özellikle de gerçek bağlamda sistem, hangi fiyat listesinin geçerli olduğunu belirlemek için **Hareket tarihi** alanını kullanır. Gelen tahminin veya fiili değerin **İşlem tarihi** değeri fiyat listesindeki **Geçerlilik Başlangıcı (saat diliminden bağımsız)** ve **Geçerlilik bitişi (saat diliminden bağımsız)** değerleri ile karşılaştırılır. Satış fiyatı listesi belirlendikten sonra sistem, satış veya fatura oranını belirler.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-time"></a>Zaman için gerçek ve tahmin satırlarındaki maliyet oranlarını belirleme

**Zaman** için tahmin bağlamı şuna başvurur:

- **Zaman** için teklif satırı ayrıntıları.
- **Zaman** için sözleşme satırı ayrıntıları.
- Projedeki kaynak atamaları.

**Zaman** için gerçek bağlam şuna başvurur:

- **Zaman** için Giriş ve Düzeltme yevmiye defteri satırları.
- Bir zaman girişi gönderildiğinde oluşturulan yevmiye defteri satırları.
- **Zaman** için fatura satırı ayrıntıları. 

Satışlar için fiyat listesi belirlendiğinde sistem, varsayılan fatura oranını girmek için aşağıdaki adımları tamamlar.

1. Sistem, **Zaman** için tahmini veya gerçek bağlamdaki **Rol**, **Kaynak Atayan Şirket** ve **Kaynak Atama Birimi** alanları kombinasyonunu fiyat listesindeki rol fiyat satırlarıyla eşleştirir. Bu eşleşme, fatura oranları için hazır fiyatlandırma boyutları kullandığınızı varsayar. Sistemi, **Rol**, **Kaynak Atayan Şirket** ve **Kaynak Atama Birimi** yerine veya buna ek olarak alanları temel alacak şekilde yapılandırırsanız, eşleşen bir rol fiyat satırını almak için bu alan kombinasyonu kullanılır.
1. Sistem, **Rol**, **Kaynak Atayan Şirket** ve **Kaynak Atama Birimi** kombinasyonu için fatura oranı olan bir rol fiyat satırı bulursa bu fatura oranı varsayılan fatura oranı olarak kullanılır.

> [!NOTE]
> **Rol**, **Kaynak Atayan Şirketi** ve **Kaynak Atama Birimi** alanlarının farklı bir önceliklendirmesini yapılandırırsanız veya daha yüksek önceliğe sahip başka boyutlara sahipseniz, önceki davranış buna göre değişecektir. Sistem, her fiyatlandırma boyutu değeriyle eşleşen değerleri olan rol fiyatı kayıtlarını öncelik sırasına göre alır. Bu boyutlar için boş değer içeren satırlar en son gelir.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Gider için fiili ve tahmin satırlarındaki maliyet oranlarını belirleme

**Gider** için tahmin bağlamı şuna başvurur:

- **Gider** için teklif satırı ayrıntıları.
- **Gider** için sözleşme satırı ayrıntıları.
- Projeye ilişkin gider tahmin satırları.

**Gider** için gerçek bağlam şuna başvurur:

- **Gider** için Giriş ve Düzeltme yevmiye defteri satırları.
- Bir gider girişi gönderildiğinde oluşturulan yevmiye defteri satırları.
- **Gider** için fatura satırı ayrıntıları. 

Satışlar için fiyat listesi belirlendiğinde sistem, varsayılan birim satış fiyatını girmek için aşağıdaki adımları tamamlar.

1. Sistem,**Gider**'e yönelik tahmin satırındaki **Kategori** ve **Birim** alanları kombinasyonunu fiyat listesindeki kategori fiyat satırlarına karşı eşleştirir.
1. Sistem, **Kategori** ve **Birim** birleşimi için satış oranına sahip bir kategori fiyat satırı bulursa, bu satış oranı varsayılan satış oranı olarak kullanılır.
1. Sistem eşleşen bir kategori fiyatı satırı bulursa, fiyatlandırma yöntemi varsayılan satış fiyatını girmek için kullanılabilir. Aşağıdaki tabloda, Project Operations'ta gider fiyatları için varsayılan davranış gösterilmektedir.

    | Bağlam | Fiyatlandırma yöntemi | Varsayılan fiyat |
    | --- | --- | --- |
    | Tahmin | Birim fiyatı | Kategori fiyat satırına dayalı olarak. |
    |        | Maliyette | Kategori 0.00 |
    |        | Maliyet üzerinde kar payı | Kategori 0.00 |
    | Gerçek | Birim fiyatı | Kategori fiyat satırına dayalı olarak. |
    |        | Maliyette | İlgili fiili maliyet esas alınarak. |
    |        | Maliyet üzerinde kar payı | Kategori fiyatı satırıyla tanımlanan bir kar payı, ilgili fiili maliyetin birim maliyet oranına uygulanır. |

1. Sistem, **Kategori** ve **Birim** değerlerini eşleştiremiyorsa satış oranı varsayılan olarak **0**'a (sıfır) ayarlanır.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-material"></a>Malzemenin gerçek ve tahmin satırlarında satış oranlarını belirleme

**Malzeme** için tahmin bağlamı şuna başvurur:

- **Malzeme** için teklif satırı ayrıntıları.
- **Malzeme** için sözleşme satırı ayrıntıları.
- Projeye ilişkin malzeme tahmin satırları.

**Malzeme** için gerçek bağlam şuna başvurur:

- **Malzeme** için Giriş ve Düzeltme yevmiye defteri satırları.
- Bir Malzeme kullanım günlüğü gönderildiğinde oluşturulan yevmiye defteri satırları.
- **Malzeme** için fatura satırı ayrıntıları. 

Satışlar için fiyat listesi belirlendiğinde sistem, varsayılan birim satış fiyatını girmek için aşağıdaki adımları tamamlar.

1. Sistem, **Malzeme**'ye yönelik tahmin satırındaki **Ürün** ve **Birim** alanlarının birleşimini fiyat listesindeki fiyat listesi maddesi satırlarıyla eşleştirir.
1. Sistem, **Ürün** ve **Birim** birleşimi için satış oranına sahip bir fiyat listesi maddesi satırı bulursa ve fiyatlandırma yöntemi **Para birimi tutarı** ise fiyat listesinde belirtilen satış fiyatı kullanılır. 
1. **Ürün** ve **Birim** alanı değerleri bir eşleşme değilse veya fiyatlandırma yöntemi olarak **Para birimi tutarı** dışında bir yöntem kullanılıyorsa satış oranı varsayılan olarak **0** (sıfır) olarak ayarlanır. Bu davranış, Project Operations yalnızca bir projede kullanılan malzemeler için **Para birimi tutarı** fiyatlandırma yöntemini desteklediği için oluşur.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
