---
title: Saat dilimlerini yönetme
description: Proje oluşturulduğunda projenin saat dilimi, uygulanan çalışma saati şablonunda tanımlanan saat dilimini temel alır.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 27f58f0dacc3404119a719547ad374629c740740
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086262"
---
# <a name="manage-time-zones"></a>Saat dilimlerini yönetme

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_


## <a name="projects"></a>Projeler

Proje oluşturulduğunda saat dilimi, uygulanan çalışma saati şablonunda tanımlanan saat dilimini temel alır. **Proje** 'de tarihler, **Görev** sekmesi dışındaki tüm sekmelerde her zaman oturum açan kullanıcının saat dilimine göredir. İş kırılım yapısını görüntülediğinizde, tarihler her zaman, projenin saat diliminde görüntülenir.

## <a name="tasks"></a>Görevler

Görev oluşturulduğunda başlangıç saati, bitiş saati ve saat/gün değerleri projenin çalışma saatleri tarafından denetlenir. Örneğin, saat dilimi -8 PST olan bir projeyle bir görev oluşturulursa ve bu projenin çalışma saatleri Pazartesiden Cumaya 09:00 ile 17:00 arasındaysa atama yapılmadan oluşturulan herhangi bir görev, proje takviminin başlangıç ve bitiş saatlerine uyacaktır.

## <a name="manage-resources-with-time-zones"></a>Kaynakları saat dilimleriyle yönetme

**Ayırmayı Genişlet** özelliğini kullanılırken doğru ve tahmin edilebilir sonuçlar elde etmek için karşılanması gereken iki temel önkoşul vardır:  

- Kullanıcı, cihazının saat dilimini sistemin **Kişiselleştirme Ayarları** 'nda tanımlanan zaman dilimiyle eşleşecek şekilde yapılandırmalıdır.
 
  ![Windows 10'da saat dilimi ayarları](media/reconcile-assignments-03.png)

  ![Kişiselleştirme ayarlarındaki saat dilimi ayarları](media/reconcile-assignments-04.png)
 
- Ayrılabilir kaynak, istenen genişletmeyi tanımlamak için kullanılan sınırlarla çakışan en az bir dakikalık çalışma zamanı içermelidir. Örneğin, çalışma saatlerinin 09:00 ile 19:00 arasında olduğu aşağıdaki kaynaklar. 

  ![Kaynak sınırlarını karşılaştırma](media/reconcile-assignments-05.png)

Aşağıdaki tabloda şunlar gösterilmektedir:

- Proje takvimi şablonu
- Kaynak A: Bu kaynak projeyle aynı takvime sahiptir ve aynı saat diliminde yer alır. Ayırmanın başlangıç saati 09:00 olarak görüntülenir.
- Kaynak B: Bu kaynak, projeden farklı bir saat diliminde bulunur ve çalışma saati kendi saat diliminde 07:00'de başlar. Ancak, ayırmalar atama sınırının en erken başlangıç saati olan 09:00'da başlar.
- Kaynak C ve D: Bu kaynakların bulundukları saat dilimleri hem birbirlerinden hem de projenin bulunduğu saat diliminden farklıdır ve ayırmaları, uygun oldukları başlangıç saatlerinden daha erken değildir.

|Varlık  |Takvim  |
|-|-|
|Proje takvimi şablonu   | ![proje takvimi](media/reconcile-assignments-06.png) |
|Kaynak A  | ![Kaynak A takvimi](media/reconcile-assignments-06.png) |
|Kaynak B  |  ![Kaynak B takvimi](media/reconcile-assignments-07.png) |
|Kaynak C  |  ![Kaynak C takvimi](media/reconcile-assignments-08.png) |
|Kaynak D  | ![Kaynak D takvimi](media/reconcile-assignments-09.png)  |
 
**Mutabakat** görünümüne gittiğinizde, kaynak atamaları ve ilişkili ayırma eksiklikleri görüntülenir.

![Uzatmadan önceki mutabakat görünümü](media/reconcile-assignments-10.png)

Her kaynak için ayırmayı genişlet işlevi kullanıldıktan sonra her kaynağın çalışma saati var olan eksikliğin sınırlarıyla çakıştığı için ayırmalar, her kaynak için başarıyla genişletilir.

![Ayırmayı uzatma sonrasındaki mutabakat görünümü](media/reconcile-assignments-11.png) 

Ayırmaların ayrıntılarına daha yakından bakıldığında ayırmaların başlangıç saatlerinde farklılıklar olduğu görülür. Ayırmaların başlangıcı, atama sınırının başlangıç zamanından ve kaynağın kullanılabilir başlangıç zamanından daha erken değildir.

![Zamanlama panosunda yeni kaynak ayırmaları](media/reconcile-assignments-12.png)
