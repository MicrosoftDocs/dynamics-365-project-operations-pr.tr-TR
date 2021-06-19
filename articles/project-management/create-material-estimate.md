---
title: Projelerdeki malzemeler için mali tahminler
description: Bu konu, proje tabanlı malzemeleri tanımlama veya tahmin etme hakkında bilgi sağlar.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 768da6adb83b4593a227f60182179b3036f4c040
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002710"
---
# <a name="financial-estimates-for-materials-on-projects"></a>Projelerdeki malzemeler için mali tahminler

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Dynamics 365 Project Operations, Proje yöneticilerinin her proje ya da görev için proje tabanlı malzeme maliyetlerini tanımlamalarına izin verir. Her malzeme tahmini, belirli bir proje göreviyle ilişkilendirilebilir. Giderler, kuruluş düzeyinde tanımlanan farklı masraf kategorilerine kategorilere ayrılır. Her bir gider kategorisi için fiyatlandırma ve maliyetlendirme, fiyat listesinde tanımlanır. 

Bir proje malzeme tahminini görüntülemek, eklemek veya silmek için aşağıdaki adımları uygulayın.

1. **Projeler**'e gidin ve güncelleştirmek istediğiniz projeyi seçin.
2. **Malzeme Tahminleri** sekmesinde, proje malzeme tahminleri listesini görüntüleyin.
3. Yeni malzeme tahmini oluşturmak için **Yeni Malzeme tahmini**'ni seçin. Veya silinecek malzeme tahminini seçin ve sonra **Malzeme Tahminini Sil**'i seçin.

Aşağıdaki tabloda, bir projedeki **Malzeme Tahmini satırındaki** alanlar hakkında bilgi verilmiştir. 

| **Alan** | **Açıklama** | **Aşağı yönlü etki** |
| --- | --- | --- |
| Görev | Projedeki görevlerin bir listesi. Buna, özet ve yaprak düğüm görevleri dahildir. | Bir malzeme tahmin satırı için bir görev seçtiğinizde, görevin tahmini malzeme maliyeti ve tahmini malzeme satışları da etkilenir. Bu alan boş bırakılırsa malzeme tahmini yalnızca proje düzeyinde izlenir ve özetlenir. |
| Ürün Seç |  Bu tahmin satırının, varolan (katalog) bir ürün için mi serbest bir ürün için mi olduğunu belirleyebilirsiniz. | Bu alan, katalogdan bir ürün mü yoksa serbest bir ürün mü seçtiğinizi belirler. |
| Ürün | Ürün kataloğundan ürün kimliği. Bir ürün kimliği seçtiğinizde, **Ürün Seç** alanındaki değer otomatik olarak **Varolan ürün** olarak güncelleştirilir. Kimlik, fiyat listesinden maliyet ve satış fiyatını almak için kullanılır. | Bu alanda aşağı yönlü etki yoktur. |
| Serbest Ürün Açıklaması | Ürünün adını yazmak için bir metin alanı. Bu alan, yalnızca **Ürün Seç** alanında **Serbest** öğesi seçildiğinde kullanılmalıdır.| Bu alanda aşağı yönlü etki yoktur. |
| Başlangıç tarihi | Malzemenin kullanılması beklenen tahmini tarih. | Bu alanda aşağı yönlü etki yoktur. |
| Birim grubu | Bu alandaki varsayılan değer, katalog üründeki varsayılan birim grubundan alınır. Başka bir birim grubunu seçerek bu alanı güncelleştirebilirsiniz. | Bu alanda aşağı yönlü etki yoktur. |
| Birim | Bu alandaki değer, seçili ürünün varsayılan biriminden gelir. Başka bir birim seçerek bu alanı güncelleştirebilirsiniz. | Birim değiştirildiğinde, farklı bir varsayılan birim fiyatı ve maliyet elde edilir. |
| Miktar | Projede kullanılacak tahmini ürün miktarı. | Bu alanda aşağı yönlü etki yoktur. |
| Birim Maliyeti | Seçilen ürün ve birim birleşiminin, geçerli maliyet fiyatı listesinde ayarlandığı üzere birim maliyeti. | Birim maliyeti her zaman projenin maliyet para biriminde gösterilir. Ürün ve birim birleşiminin fiyat listesinde ayarlanmış bir birim maliyeti yoksa birim maliyeti varsayılan olarak 0,00 olur. |
| Birim Fiyatı | Seçilen ürün ve birim birleşiminin, geçerli satış fiyatı listesinde ayarlandığı üzere fiyatı. | Birim fiyatı her zaman projenin satış para biriminde gösterilir. Seçilen ürün ve birim birleşiminin geçerli maliyet fiyatı listesinde ayarlanmış bir birim fiyatı yoksa birim fiyatı varsayılan olarak 0,00 olur.|
| Toplam Maliyet | Miktar \* birim maliyeti olarak hesaplanan maliyet tutarı.| Maliyet tutarı her zaman projenin maliyet para biriminde gösterilir. |
| Toplam Satış | Miktar \* birim fiyatı olarak hesaplanan satış tutarı. | Satış tutarı her zaman projenin satış para biriminde gösterilir. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
