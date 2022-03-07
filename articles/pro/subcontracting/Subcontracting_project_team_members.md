---
title: Alt sözleşme proje takım üyeleri
description: Bu konuda, Microsoft Dynamics 365 Project Operations'da proje takımı üyeleri için alt sözleşmelerin nasıl oluşturulacağı açıklanmaktadır.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 846de9afab5bf9ebc13670abd6ce735801796f0e
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902957"
---
# <a name="subcontracting-project-team-members"></a>Alt sözleşme proje takım üyeleri

[!include [banner](../../includes/dataverse-preview.md)]

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Microsoft Dynamics 365 Project Operations'da, kadrolu olmayan veya kadrolu proje takımı üyelerine alt sözleşmeye dahil etmeyi seçebilirsiniz.

- Kadrolu olmayan proje takımı üyelerinin atanmış genel bir kaynağı vardır.
- Kadrolu takım üyelerinin atanmış adlandırılmış bir kaynağı vardır.

Bir proje takımı üyesini bir alt yüklenici satırına bağladığınızda, takım üyesinin sahip olduğu görevlere yapılan atamalar, alt yükleniciyle iliştirilen satınalma fiyatı listesine göre yeniden maliyetlendirilir.  **Proje Ayrıntıları** sayfasındaki **Tahminler** sekmesinde, alt sözleşme kararından kaynaklanan güncelleştirilmiş fiyatlandırmayı ve/veya maliyeti görmek için **Fiyatları güncelleştir** düğmesini seçin. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Kadrosuz bir proje takımı üyesini alt sözleşmeye dahil etme
**Takım Üyesi ayrıntıları** sayfasında, proje yöneticisinin bir alt sözleşmeden gereken kapasiteyi nasıl çekmek istediklerini ifade etmesine olanak sağlayan alt sözleşme ve alt sözleşme satırı alanları vardır. Proje takımı üyesini genel kaynak olarak alt sözleşmeye dahil etmek için şu adımları izleyin:

1.  **Takım üyesi ayrıntıları** sayfasında bir alt sözleşme seçin.

2.  Yalnızca **Taslak** veya **Onaylandı** durumundaki alt sözleşmeleri seçebilirsiniz. **Kapalı** veya **İptal edildi** durumundaki alt sözleşmeler seçilemez. 

3.  **Alt sözleşme satırı** alanı, bir alt sözleşme seçtikten sonra görünür hale gelir.

4.  **Alt sözleşme satırı** alanında, yalnızca zaman için olan alt sözleşme satırlarını seçebilirsiniz. Gider veya malzeme için alt sözleşme satırları seçemezsiniz.

5.  Proje takımı üyesi rolü kaydının alt sözleşme satırındaki rolle eşleşmesi gerekir. Bu, projede tahmin edilen rolün zamanının alt sözleşme satırındaki satın alınan rolle aynı olmasını sağlar. 

Genel bir takım üyesi bir alt sözleşme ve alt sözleşme satırıyla ilişkilendirildiğinde, genel takım üyesi satırındaki **Çalışan türü** alanı **Sözleşmeli Çalışan** ve **Alt Sözleşme Geçerliliği**, **Geçerli** olarak güncelleştirilir.

## <a name="subcontracting-a-staffed-project-team-member"></a>Kadrolu bir proje takım üyesini alt sözleşmeye dahil etme
Genel veya kadrosuz takım üyeleri gibi, bir projede gereken kadrolu takım üyesi kapasitesi de bir alt sözleşmeye bağlanabilir. Adlandırılan bir proje takımı üyesini alt sözleşmeye dahil etmek için şu adımları izleyin:

1.  Adlandırılmış kaynağın, ayrılabilir kaynağın sözleşmeli çalışan türü olarak ayarlandığından emin olun. Ayrıca, ayrılabilir kaynak üzerindeki **Satıcı** alanının seçtiğiniz alt sözleşmedeki satıcıyla eşleştiğinden emin olun. 

2.  Yalnızca **Taslak** veya **Onaylandı** durumundaki alt sözleşmeleri seçebilirsiniz. **Kapalı** veya **İptal edildi** durumundaki alt sözleşmeler seçilemez. 

3.  **Alt sözleşme satırı** alanı, bir alt sözleşme seçtikten sonra görünür hale gelir.

4.  **Alt sözleşme satırı** alanında, yalnızca zaman için olan alt sözleşme satırlarını seçebilirsiniz. Gider veya malzeme için alt sözleşme satırları seçemezsiniz.

5.  Proje takımı üyesi rolü kaydının alt sözleşme satırındaki rolle eşleşmesi gerekir. Bu, projede tahmin edilen rolün zamanının alt sözleşme satırındaki satın alınan rolle aynı olmasını sağlar. 

**Ayrılabilir kaynak**'ın sözleşmeli çalışan türü olarak ayarlanan adlandırılmış proje takımı üyeleri, bir alt sözleşmeyle bağlantılı değillerse **Geçerli değil** alt sözleşme geçerlilik durumuyla gösterilir. Adlandırılmış bir proje takımı üyesi bir alt sözleşme ve alt sözleşme satırıyla ilişkilendirildiğinde, takım üyesi satırındaki **Çalışan türü** alanı **Sözleşmeli Çalışan** ve **Alt Sözleşme Geçerliliği**, **Geçerli** olarak güncelleştirilir.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
