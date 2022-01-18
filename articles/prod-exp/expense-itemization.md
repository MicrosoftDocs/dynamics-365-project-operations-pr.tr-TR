---
title: Gider dökümü
description: Bu konuda, yeniden tasarlanan Gider çalışma alanını kullanarak giderlerin nasıl listelendirileceği açıklanmaktadır.
author: suvaidya
ms.date: 12/16/2021
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: b2077b77af036ce64aad203f52b03cacca8c4099
ms.sourcegitcommit: 9d20e7738cce195d344f5925a115741a1ce3ca36
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944135"
---
# <a name="expense-itemization"></a>Gider dökümü

[!include [banner](../includes/banner.md)]

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Kuruluşlar genellikle çalışanların seyahat sırasında yapılan harcamaların ayrıntılı bir dökümünü sağlamasını gerektirir. Örneğin, bir otel portföyü oda fiyatı, vergi, otopark ve konaklama süresince her gün yapılan diğer çeşitli masraflar için çeşitli maddeleştirilmiş satırlar içerebilir. Veya bir yemek masrafı kahvaltı, öğle veya akşam yemeği için daha ayrıntılı bir döküm sağlamanızı gerektirebilir. Kuruluşun gereksinimleri ne olursa olsun, her gider kategorisi alt kategorileri veya gideri oluşturan satır maddelerini yansıtacak şekilde ayarlanabilir. Döküm her zaman **Gider yönetiminde** desteklenmiş olsa da, **Yeniden tasarlanan gider** çalışma alanı, **yinelenen giderleri hızlı bir şekilde döküm yeteneği** etkinleştirildiğinde daha verimli döküm sağlar.  

## <a name="enable-quick-itemization"></a>Hızlı dökümü etkinleştirme 

Konaklama süresince her seferinde günlük giderleri girme gereksiniminden kaçınırken yinelenen giderleri hızlı bir şekilde döküm almak için **Yinelenen giderlerin hızlı bir şekilde dökümünü alma özelliğini** kullanabilirsiniz. Hızlı öğe oluşturmayı etkinleştirmek için aşağıdaki adımları tamamlayın.

1.  **Özellik Yönetimi** çalışma alanına gidin ve özellikler listesinde, **Yeniden Tasarlanan Gider Raporları**'nı bulun ve seçin. 
2. **Şİmdi Etkinleştir**'i seçin. 
3. Özellik listesinde, **Yinelenen giderlerin hızlı bir şekilde dökümünü alma**'yı bulun ve seçin.
4. **Şİmdi Etkinleştir**'i seçin. 

## <a name="itemization-grid"></a>Döküm kılavuzu 

Bir gider kategorisinin alt kategorileri veya bu gideri oluşturan farklı bileşenleri varsa bunun dökümü alınabilir. Bir giderin dökümünü almak için gider raporunda gider satırını seçin ve **Gider ayrıntıları** bölmesinde **Eylemler** > **Döküm oluştur**'u seçin. **Döküm** kaydırıcısı, alanları olan bir ızgarayı ortaya çıkarır. Aşağıdaki tablo, kılavuzdaki her alanın ve alanın gider raporunda nasıl işlendiğinin bir örneğini sağlar. 

|     Alan          |     Description                                                                                  |     Örnek              |
|--------------------|--------------------------------------------------------------------------------------------------|--------------------------|
|     Alt kategori    |     **Otel** gider kategorisi türü altında yapılandırılan alt kategorilerin listesi.             |     Günlük oda fiyatı      |
|     Başlangıç tarihi     |     Masraf öğesinin ilk tahakkuk ettiği tarih.                                           |     09/13/2021           |
|     Günlük Fiyat     |     Masraf öğesi için tahakkuk eden tutar.                                                    |     200                  |
|     Miktar       |     Ücretin sürekli bir süre boyunca tekrarlanma sayısı.                       |     3                    |

![Giderin dökümünü alın.](media/Itemization%20screen%201.png)

Bir dökümü kaydettiğinizde, Döküm alma kılavuzunda belirtilen miktar için tek bir maddeleştirilmiş satır görürsünüz. Her satır kılavuzda belirtilen tarihte başlar.

![Dökümü alınan rapor.](media/Itemization%20screen%202.png)

