---
title: Kaynak mutabakatına genel bakış
description: Bu makalede, projelerin kaynak rezervasyonlarından ve atamalarının hizalandığından emin olmanıza yardımcı olacak bilgiler sağlanmaktadır.
author: ruhercul
ms.date: 01/08/2021
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: eaad9187f08be810d730f5a8ca6411ecee85bbc4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926340"
---
# <a name="resource-reconciliation-overview"></a>Kaynak mutabakatına genel bakış

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Takım üyeleri için, atamalar ve ayırmalar çok sıkı şekilde eşleştirilmez. Başka bir deyişle, kaynaklar atamalara sahip olabilir ve herhangi bir ayırma olmayabilir veya ayırmaları varken atamaları olmayabilir. İdeal olarak, ayırmalar ve atamaların, kaynakların görev atamalarını gerçekleştirmek için kapasiteyi taahhüt edebilecekleri şekilde uyumlu olması gerekir. Bununla birlikte, ayırmalar kullanılabilirliğine dayalı olabilir ve proje devam ederken görev zamanlamaları değiştirilebilir. Bu nedenle, ayırmalar ve atamaların çok sıkı şekilde eşlenmemesi esneklik sağlar.

**Projeler** sayfasındaki **Mutabakat** sekmesi, proje yöneticilerinin proje takımları için takım üyelerinin ayırmaları ile atamaları arasında mutabakat sağlamasına olanak tanır.

**Mutabakat** sekmesi ayırmaları ve atamaları her takım üyesi için bireysel görev ataması düzeyinde gösterir. Saatler, aylardan günlere kadar olan dönemleri temsil eden hücrelerde gösterilir. Sekme ayrıca, **Toplam** sütunuyla birlikte proje için genel bir net toplam gösterir.

Her kaynak için **Mutabakat** sekmesi, takım üyesinin ayırmaları ile takım üyesinin görev atamalarının toplu değeri arasındaki farkı hesaplar. İdeal olarak, bu fark 0 (sıfır) olmalıdır. Başka bir deyişle, ayırmalar ile görev atamaları arasında fark olmamalıdır. İki koşula dikkat çekmek için farklılıklar renkli ve gölgeli olarak belirtilir:

- **Ayırma eksikliği** – Ayırma eksikliği bir kaynakta ayırmadan daha fazla atama varsa oluşur. Kapasite ayrılmadığından proje yöneticisi eksikliği gidermek için kaynağın ayırmalarını uzatarak bu koşulu düzeltmek isteyebilir.
- **Aşırı ayırmalar** – Aşırı ayırmalar bir kaynak projeye ayrıldığında ancak görevlere atanmadığında oluşur. Bu koşul, görev ataması gerçekleşmeden önce kaynağın projeye ayrılmış olduğu durumlarda kabul edilebilir. Bununla birlikte, kaynağı görevlere atama planının olmadığı diğer durumlarda proje yöneticisi, kaynağın ayırmalarını iptal etmeyi düşünmelidir. Bu şekilde kapasite başka bir proje için kullanılabilir.

Bazı durumlarda, zamanı gün düzeyinden daha yüksek bir düzeyde (örneğin, ay düzeyi) görüntülediğinizde kaynak için sıfır (başka bir deyişle, ayırmalar eşittir atamalar) net farkını görebilirsiniz. Ancak, zamanı hafta düzeyinde görüntülerseniz ayın ilk haftasında 0 (sıfır) saat atama ve 40 saat ayırma ve ayın ikinci haftasında 40 saat atama ve 0 (sıfır) saat ayırma olduğunu görebilirsiniz. Genel olarak, ayırmalar ve atamalar üzerinde mutabakat sağlanır, ancak bunlar bir haftadan diğerine farklılık gösterir.

Zamanı daha yüksek düzeylerde görüntülediğinizde **Mutabakat** sekmesindeki hücrelerde alt zaman düzeylerinde farklar olduğunu bildiren bir gösterge bulunur. Bir hücreye çift dokunarak veya çift tıklayarak farkı görüntülemek için yakınlaştırabilirsiniz. Daha sonra uzaklaştırmak için basılı tutabilirsiniz (veya sağ tıklayabilirsiniz). Bir kaynağı seçip, ardından kılavuz araç çubuğundaki **Sonraki fark** denetimini kullanarak bu kaynağın ayırmaları ve atamaları arasındaki sonraki farka gidebilirsiniz. Daha sonra geri gitmek için **Önceki fark** denetimini kullanabilirsiniz. Ayrıca **Ayarlar** altındaki fark göstergesini ve gezinme davranışını devre dışı bırakabilirsiniz.

Kaynak için görev atamalarınızın olması ancak ayırmalarınızın olmaması durumunda **Projeler** sayfasının **Mutabakat** sekmesinde ayırma eksikliğini seçin ve ardından **Ayırmayı Uzat**'ı seçin. Görüntülenen **Ayırmayı Uzat** iletişim kutusu, kaynağın eksikliğini ele almak için gereken ayırmayı gösterir. İletişim kutusu, kaynağın tüm projeler veya diğer zamanlanabilir varlıklarda var olan ayırmalarını da gösterir. Kaynağın kullanılabilirliğinden bağımsız olarak, kaynak için ayırma oluşturmak üzere **Tamam**'ı seçerseniz, fazladan ayırmaya neden olabilirsiniz.

**Ayırmayı Uzat** eylemiyle oluşturulan ayırmalar, birincil proje gereksinimi ile ilişkilendirilir. Uzatma başlatıldığında kaynak, proje için birden fazla gereksinimle ilişkilendirilebileceğinden uzatılması gereken özel gereksinim belirlenemez.

Ardından proje yöneticisi veya kaynak yöneticisi, bir kaynağın kapasitesi üzerinde ayrılmış olan durumları yönetmek için Zamanlama panosunu kullanabilir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]