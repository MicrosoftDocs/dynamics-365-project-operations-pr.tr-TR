---
title: Projelerdeki giderler için mali tahminler
description: Bu konuda, proje tabanlı giderleri tanımlama veya tahmin etme hakkında bilgiler sağlanmaktadır.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f4d42724af61aa241671e8dacacbe2be5a7d531f55c2025a89ff777ac41e9b67
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987865"
---
# <a name="financial-estimates-for-expenses-on-projects"></a>Projelerdeki giderler için mali tahminler
_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Dynamics 365 Project Operations, Proje yöneticilerinin her proje ya da görev için proje tabanlı giderler tanımlamalarına izin verir. Her gider maddesi, belirli bir proje göreviyle ilişkilendirilebilir. Giderler, kuruluş düzeyinde tanımlanan farklı masraf kategorilerine kategorilere ayrılır. Her bir gider kategorisi için fiyatlandırma ve maliyetlendirme, fiyat listesinde tanımlanır. 

Proje giderini görüntülemek, eklemek veya silmek için aşağıdaki adımları tamamlayın.

1. **Projeler**'e gidin ve üzerinde çalışmak istediğiniz projeyi seçin.
2. **Proje Tahminleri** sekmesini seçin ve proje giderleri listesini görüntüleyin.
3. Gider eklemek için **Yeni Gider**'i seçin. Alternatif olarak, silinecek gideri seçin ve ardından **Gideri Sil** seçeneğini belirleyin.

Aşağıdaki tabloda, bir projedeki **Masraf Tahmini satırındaki** alanlar hakkında bilgi verilmiştir. 

| **Alan** | **Açıklama** | **Aşağı yönlü etki** |
| --- | --- | --- |
| Görev | Projedeki görevlerin bir listesi. Buna, özet ve yaprak düğüm görevleri dahildir. | Bir masraf tahmin satırı için bir görev seçilmesi, görevin tahmini gider maliyeti ve tahmini gider satışlarını etkiler. Bu alan boş bırakılırsa gider tahmini yalnızca proje düzeyinde izlenir ve özetlenir. |
| Kategori | Uygulamada bağlantılı gider kategorileri bulunan hareket kategorilerinin bir listesi. | Bir kategori seçildiğinde, masraf tahmini satırındaki fiyatlandırmayı ve maliyetlendirmeyi harekete geçirir. |
| Başlangıç tarihi | Giderin gerçekleşeceği tahmini tarih. | Bu alanda aşağı yönlü etki yoktur. |
| Birim grubu | Bu alandaki varsayılan değer, seçilen kategoride varsayılan olarak ayarlanan birim grubundan alınır. Başka bir birim grubunu seçerek bu alanı güncelleştirebilirsiniz. | Bu alanda aşağı yönlü etki yoktur. |
| Birim | Bu alandaki değer, varsayılan olarak seçili kategorinin varsayılan birimidir. Başka bir birim seçerek bu alanı güncelleştirebilirsiniz. | Birim değiştirildiğinde, farklı bir varsayılan birim fiyatı ve maliyet elde edilir. |
| Miktar | Karşılayacağınız tahmini giderin miktarı. | Bu alanda aşağı yönlü etki yoktur. |
| Birim Maliyeti | Seçilen kategori ve birim birleşiminin, geçerli maliyet fiyatı listesinde ayarlandığı üzere maliyeti | Birim maliyeti her zaman projenin maliyet para biriminde gösterilir. |
| Birim Fiyatı | Seçilen kategori ve birim birleşiminin, geçerli satış fiyatı listesinde ayarlandığı üzere fiyatı. | Birim fiyatı her zaman projenin satış para biriminde gösterilir. |
| Toplam Maliyet | Miktar \* birim maliyeti olarak hesaplanan maliyet tutarı.| Maliyet tutarı her zaman projenin maliyet para biriminde gösterilir. |
| Toplam Satış | Miktar \* birim fiyatı olarak hesaplanan satış tutarı. | Satış tutarı her zaman projenin satış para biriminde gösterilir. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
