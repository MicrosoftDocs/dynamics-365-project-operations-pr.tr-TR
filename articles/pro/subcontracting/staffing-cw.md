---
title: Sözleşmeli çalışanlar ve alt sözleşme kapasitesi ile bir projede personel alımı
description: Bu konuda, Microsoft Dynamics 365 Project Operations'da sözleşmeli çalışanlar veya alt sözleşme kapasitesi kullanılarak proje gereksinimlerinin nasıl kadrolanabileceği açıklanmaktadır.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 7e9a0ca08f472999138589f31ca820b733b6303e
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903568"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Sözleşmeli çalışanlar ve alt sözleşme kapasitesi ile bir projede personel alımı

[!include [banner](../../includes/dataverse-preview.md)]

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Genel proje takımı üyeleri çalışanlarla veya sözleşmeli çalışanlarla doldurulabilir. Sözleşmeli çalışanlarla bir projeye personel sağlarken, kadro seçeneklerinizi alt sözleşme satırına atanan belirli sözleşmeli çalışanlarla sınırlayabilirsiniz. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Belirli bir alt sözleşme satırına ait sözleşmeli çalışanlarla personel kaynak gereksinimlerini arama

Belirli bir alt sözleşme satırına ait sözleşmeli çalışanlarla kaynak gereksinimlerini aramak ve personel eklemek için şu adımları izleyin:

1. Alt sözleşme ve alt sözleşme satırına başvuran genel bir proje takımı üyesi oluşturun.
2. Proje takımı üyeleri alt kılavuzundaki **Gereksinim oluştur** düğmesini kullanarak bu genel proje takımı üyesi için bir kaynak gereksinimi oluşturun.
3. Takım üyesi satırını seçin ve ardından alt ızgaradaki **Ayır** düğmesini seçin. 
4. Bu, gereksinim bağlamının bulunduğu Zamanlama Panosu'nu açar. Tarihler, rol ve kuruluş birimi alanları gibi diğer özniteliklerin yanı sıra, Zamanlama Panosu filtreleri de kaynak gereksinimindeki satıcı, alt sözleşme ve alt sözleşme satırı alanlarıyla otomatik olarak doldurulur.
5. Sistem, filtre ölçütlerini karşılayan kaynakları arar ve bunları listeler. 
6. Filtrelenen kaynaklardan birini seçin ve gereksinim için kaynak rezervasyonu yapın. 
7. Bir proje takımı üyesi oluşturulur, alt sözleşme ve alt sözleşme satırı başvurularıyla güncelleştirilir. **Proje Tahminleri**'ne gidin ve kaynak atamasının güncelleştirilmiş maliyetini görmek için **Fiyatları güncelleştir**'i seçin. 

> [!NOTE]
> Kaynak birden çok alt sözleşme satırına atanmışsa proje takımı üyesini alt sözleşme ve alt sözleşme satırı başvurusuyla güncelleştirmek, ayırma işlemi sırasında her zaman mümkün olmayabilir. Sistem, proje takımı üyesini alt sözleşme ve alt sözleşme satırıyla güncelleştiremezse proje takımı üyesi kaydını açın ve mali maliyet tahmininin alt sözleşme maliyetini doğru şekilde yansıtması için bu alanları el ile güncelleştirin.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Kaynak gereksinimlerini arama ve bunlara herhangi bir sözleşmeli çalışanla personel sağlama

Kaynak gereksinimlerini aramak ve herhangi bir sözleşmeli çalışanla personel sağlamak için şu adımları izleyin:

1. Genel bir proje takımı üyesi oluşturun.
2. Proje takımı üyeleri alt kılavuzundaki **Gereksinim oluştur** düğmesini kullanarak bu genel proje takımı üyesi için bir kaynak gereksinimi oluşturun.
3. Takım üyesi satırını seçin ve ardından alt ızgaradaki **Ayır** düğmesini seçin. 
4. Bu, gereksinim bağlamının bulunduğu Zamanlama Panosu'nu açar. Tarihler, rol ve kuruluş birimi alanları gibi diğer özniteliklerin yanı sıra, Zamanlama Panosu filtreleri de kaynak gereksinimindeki satıcı, alt sözleşme ve alt sözleşme satırı alanlarıyla otomatik olarak doldurulur. Gereksinimde doldurulmuş herhangi bir alt sözleşme veya alt sözleşme satırı değeri olmadığından, bu öznitelikler filtre bölmesinde boş olacaktır.
5. Sistem, filtre ölçütlerini karşılayan kaynakları arar ve bunları listeler.
6. Aramayı sözleşmeli çalışanlarla sınırlamak için filtre bölmesindeki **Çalışan türü** alanını **Sözleşmeli Çalışan** olarak güncelleştirin. Aramayı yalnızca belirli bir satıcı şirketine ait sözleşmeli çalışanları gösterecek şekilde sınırlayacak bir satıcı seçmek için filtre bölmesindeki **Satıcı**'yı güncelleştirin.
7. Listeden bir sözleşmeli çalışan seçin ve gereksinim için kaynak rezervasyonu yapın.
8. Bir proje takımı üyesi oluşturulur. Ancak, proje takımı üyesi herhangi bir alt sözleşme veya alt sözleşme satırıyla güncelleştirilmez ve bu nedenle kaynak ataması alt sözleşme fiyatlandırması kullanılarak maliyetlendirilmez. Proje takımı üyesini bir alt sözleşme satırıyla el ile güncelleştirin ve kaynak atamasının güncelleştirilmiş maliyetini görmek için **Proje Tahminleri**'ne gidip **Fiyatları güncelleştir**'i seçin.

> [!NOTE]
> **Çalışan türü** **Sözleşmeli çalışan** olan ancak alt sözleşme başvurusu olmayan proje takımı üyeleri, **Proje takımı üyeleri** kılavuzunda **Geçersiz** olarak işaretlenir. Bu durumda herhangi bir proje takımı üyesi varsa proje takımı üyesi kaydını açın ve alt sözleşme ve alt sözleşme satırı alanlarını el ile güncelleştirin, böylece mali maliyet tahmini **Tahminler** sekmesinde alt yüklenici maliyetini doğru bir şekilde yansıtır. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
