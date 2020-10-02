---
title: Kaynak mutabakatına genel bakış
description: Bu konu kaynakları ayırma ve görevlere atama konusunda uyumun sağlanması hakkında bilgi sağlar.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1b60ed9d15f51ff01f27bcc231f5db27513a838f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897475"
---
# <a name="resource-reconciliation-overview"></a>Kaynak mutabakatına genel bakış

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Takım üyeleri için, atamalar ve ayırmalar çok sıkı şekilde eşleştirilmez. Başka bir deyişle, kaynaklar atamalara sahip olabilir ancak herhangi bir ayırma olmayabilir veya ayırmaları varken atamaları olmayabilir. İdeal olarak, ayırmalar ve atamaların, kaynakların görev atamalarını gerçekleştirmek için kapasiteyi taahhüt edebilecekleri şekilde uyumlu olması gerekir. Bununla birlikte, ayırmalar kullanılabilirliğine dayalı olabilir ve proje devam ederken görev zamanlamaları değiştirilebilir. Bu nedenle, ayırmalar ve atamaların çok sıkı şekilde eşlenmemesi esneklik sağlar.

**Proje** formundaki **Mutabakat** sekmesi proje yöneticilerinin proje takımları için takım üyesi ayırmaları ile atamaları arasında mutabakat sağlamasına olanak tanır.

Ayrıca **Mutabakat** sekmesi ayırmaları ve atamaları her takım üyesi için bireysel görev ataması düzeyinde gösterir. Hücrelerde aylardan günlere kadar olan dönemleri temsil eden saatler gösterilir.

Sekme ayrıca, **Toplam** sütunuyla birlikte proje için genel bir net toplam gösterir.

Her kaynak için sekme, takım üyesinin projedeki ayırmaları ile takım üyesinin görev atamalarının toplu değeri arasındaki farkı hesaplar. İdeal olarak, bu fark 0 (sıfır) olmalıdır. Başka bir deyişle, ayırmalar ile görev atamaları arasında fark olmamalıdır. İki koşula dikkat çekmek için farklılıklar renkli ve gölgeli olarak belirtilir:

- **Ayırma eksikliği** – Ayırma eksikliği bir kaynakta ayırmadan daha fazla atama varsa oluşur. Bu kapasite ayrılmadığından bir proje yöneticisi eksikliği gidermek için kaynağın ayırmalarını uzatarak bu koşulu düzeltmek isteyebilir.
- **Aşırı ayırmalar** – Aşırı ayırmalar bir kaynak projeye ayrıldığında ancak görevlere atanmadığında oluşur. Bu koşul, görev ataması gerçekleşmeden önce kaynağın projeye ayrılmış olduğu durumlarda kabul edilebilir. Ancak diğer durumlarda kaynak görevlere atanmak üzere planlanmaz. Bu durumlarda Proje Yöneticisi, kapasitenin başka bir projede kullanılabilmesi için kaynağın ayırmalarını iptal etmeyi düşünmelidir.

Bazı durumlarda, zamanı gün düzeyinden daha yüksek bir düzeyde (örneğin, ay düzeyi) görüntülediğinizde, kaynak için sıfır (başka bir deyişle, ayırmalar = atamalar) net farkını görebilirsiniz. Ancak, zamanı hafta düzeyinde görüntülerseniz ayın ilk haftasında 0 (sıfır) saat atama ve 40 saat ayırma ve ayın ikinci haftasında 40 saat atama ve 0 (sıfır) saat ayırma olduğunu görebilirsiniz. Genel olarak, ayırmalar ve atamalar üzerinde mutabakat sağlanır, ancak bunlar bir haftadan diğerine farklılık gösterir.

Zamanı daha yüksek düzeylerde görüntülediğinizde **Mutabakat** sekmesindeki hücrelerde alt zaman düzeylerinde farklar olduğunu bildiren bir gösterge bulunur. Bir hücreye çift tıklayarak, farkı yakından görüntüleyebilirsiniz. Daha sonra uzaklaştırmak için sağ tıklayabilirsiniz. Bir kaynağı seçip, ardından kılavuz araç çubuğundaki **Sonraki fark** denetimini kullanarak, bu kaynağın ayırmaları ve atamaları arasındaki sonraki farka gidebilirsiniz. Daha sonra geri gitmek için **Önceki fark** denetimini kullanabilirsiniz. Ayrıca **Ayarlar** altındaki fark göstergesini ve gezinme davranışını devre dışı bırakabilirsiniz.


Bir kaynak için görev atamalarınızın olması ancak ayırmalarınızın olmaması durumunda **Projeler** sayfasındaki **Mutabakat** sekmesinde ayırma eksikliğini ve ardından **Ayırmayı Genişlet**'i seçin. **Ayırmayı Genişlet** iletişim kutusu görüntülenir ve kaynağın eksikliğini ele almak için gereken ayırmayı gösterir. Ayrıca, kaynağın tüm projeler veya diğer zamanlanabilir varlıklardaki varolan ayırmalarını da gösterir. Kaynağın kullanılabilirliğinden bağımsız olarak, kaynak için ayırma oluşturmak üzere **Tamam**'ı seçerseniz, fazladan ayırmaya neden olabilirsiniz.

Ardından proje yöneticisi veya kaynak yöneticisi, bir kaynağın kapasitesi üzerinde ayrılmış olduğu durumları yönetmek için Zamanlama Panosunu kullanabilir.

