---
title: Kaynak kullanımına genel bakış
description: Bu konu Project Operations'ta kaynak kullanımı hakkında bilgi sağlar.
author: ruhercul
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8b85464dbb68523b122116225a604f67e7236f3e
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401400"
---
# <a name="resource-utilization-overview"></a>Kaynak kullanımına genel bakış

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Kaynaklarda bir faturalandırılabilir kullanım hedefi olabilir. Bu kullanım hedefi, bir kaynağın varsayılan rolündeki bir öznitelik olarak tanımlanır veya ayrılabilir kaynakların her birinin kaydında ayarlanır. Kullanım hesaplamaları, onaylanan zaman girişleri kullanılarak kaynakların bildirdiği gerçek saatleri temel alır.

Kullanımı hesaplamak için aşağıdaki formüller kullanılır:

  - Faturalanabilir kullanım = Borçlandırılabilir gerçek saat sayısı ÷ Kaynak kapasitesi
  - Faturalanamayan kullanım = Faturalama türü kimliği ile gerçek zaman = Borçlandırılamaz, Tamamlayıcı veya Kullanılamaz ÷ Kaynak kapasitesi
  - Dahili = Satış sözleşmesi olmayan gerçek zaman ÷ Kaynak kapasitesi
  - Kaynak kapasitesi = Kaynak çalışma saatleri – Ofis dışında – Çalışma günü olmayan günler

**Kaynak Kullanımı** görünümünü **Kaynaklar** bölmesinde bulabilirsiniz.

Izgaradaki her hücre; gün, hafta veya ay gibi dönemlerde kaynağın faturalandırılabilir kullanım yüzdesini gösterir. Hücreleri renklendirmek için aşağıdaki formüller kullanılır:

  - **Yeşil**: faturalanabilir kullanım > = kaynak hedef kullanımı
  - **Sarı**: hedef kullanım – 20 < = faturalanabilir kullanım < hedef kullanım
  - **Kırmızı**: faturalanabilir kullanım < hedef kullanım - 20

**Kaynak Kullanımı** görünümü Zamanlama Panosunu temel aldığından, yorumunuzu filtrelemek için Zamanlama Panosunun filtreleme yeteneklerini kullanabilirsiniz.

Izgara, rolde veya her kaynak için bir hedef kullanımı belirlemenizi gerektirir. Bu kurulumu yapmak için **Kaynaklar** > **Kaynak rolleri**'ne gidin.

Ek olarak, her ayrılabilir kaynağa varsayılan bir rol atanması gerekir. **Kaynaklar** > **Kaynaklar**'a gidin. **Project Service** sekmesinde, bir kaynak rolünün tanımlandığından ve bunun için **Varsayılan** alanının **Evet** olarak ayarlandığından emin olun. **Varsayılan** = **Hayır** olduğunda ilave roller ekleyebilirsiniz. **Varsayılan** = **Evet** olduğu durumlarda rol, kaynağın kullanımının bu rolün hedefiyle karşılaştırmalı değerlendirmesi için kullanılır.

**Project Service** sekmesinde, kaynak için ayrı bir hedef kullanımı da ayarlayabilirsiniz. Sonrasında kullanım hesaplaması kaynağın hedefini değerlendirmek için kaynağın varsayılan rolünün hedefi yerine bu hedef kullanımını kullanır.

Kaynağın kullanımı, yalnızca söz konusu kaynağın ızgarada gösterilen dönem içinde borçlandırılabilir bir zaman olduğu onaylanırsa gösterilir.