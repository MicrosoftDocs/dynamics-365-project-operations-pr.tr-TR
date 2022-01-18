---
title: Yenilikler Aralık 2021 - Project Operations Lite dağıtımı
description: Bu konu, Project Operations lite dağıtımının Aralık 2021 sürümünde kullanılabilen kalite güncelleştirmeleri hakkında bilgi sağlar.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0432e2d4970c352e91cca589987bbdace57c6eaf
ms.sourcegitcommit: 9d20e7738cce195d344f5925a115741a1ce3ca36
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/21/2021
ms.locfileid: "7943001"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Yenilikler Aralık 2021 - Project Operations Lite dağıtımı

_Şunlar için geçerlidir: Lite dağıtımı - anlaşmadan proforma faturaya_

Bu konu aşağıdaki Microsoft Dynamics 365 Project Operations bileşenleri ve sürümleri için geçerlidir:

- Dataverse ortamı sürüm 4.27.0.195, 4.27.0.242'deki Project Operations


## <a name="features-included-in-this-release"></a>Bu sürümde yer alan özellikler

### <a name="subcontract-management"></a>Alt sözleşme yönetimi 

- [Alt sözleşme proje takımı üyeleri](../subcontracting/subcontracting-project-team-members.md): Proje yöneticisi, personel ekleme ve tahmini etkilemek için alt sözleşme ve alt sözleşme satırlarıyla adlandırılmış veya genel takım üyeleri oluşturabilir.
- [Proje takımı üyeleri için alt sözleşme seçenekleri](../subcontracting/subcon-options.md): Adlandırılmış veya genel proje takımı üyeleri için personel seçimleri yaparken, proje yöneticisi var olan alt sözleşmeleri gözden geçirebilir veya bir veya daha fazla proje takımı üyesi için yeni alt sözleşmeler oluşturabilir. 
- [Alt sözleşme kaynak atamalarının maliyet tahmini](../subcontracting/costing-subcon-ra.md): Proje maliyet tahmini, alt sözleşme kaynak atamalarını dikkate alır ve alt sözleşmelerle ilişkili satınalma fiyatı listelerini kullanarak bunlara maliyetlendirme yapar. 
- [Sözleşmeli çalışanları ve alt sözleşme kapasitesini göstermek için Zamanlama Panosu'nu yapılandırma](../subcontracting/configure-sb-subcon.md): Project Operations'da zamanlama panosu artık sözleşmeli çalışanın ayrılabilir kaynak türünü ve çalışanlarla birlikte alt sözleşme kapasitesini arayacak ve önerecek şekilde yapılandırılabilir. Bu yapılandırma, belirli bir proje gereksinimi için personel bağlamında kaynak ararken veya proje gereksinimi bağlamının dışında arama yaparken uygulanabilir.
- [Sözleşmeli çalışanlar ve alt sözleşme kapasitesi olan bir projeye personel ekleme](../subcontracting/staffing-cw.md): Sözleşmeli çalışanlar artık zamanlama panosu deneyimlerinden yararlanan projelerde ayrılabilir.
- [Alt sözleşme bileşenleri için projelerde kayıt süresi, giderler ve malzeme kullanımı](../subcontracting/recording-subcon-actuals.md): Sözleşmeli çalışanlar zaman ve giderleri kaydedebilir ve proje takımı üyeleri bir projede alt sözleşme kullanarak satın alınan malzemelerin kullanımını da kaydedebilir. Bu, satın alınan kapasiteyi veya malzemeleri kullanan projelerde doğru maliyetlerin kaydedilmesine neden olacaktır.
- [Alt sözleşmedeki durum geçişleri](../subcontracting/subcon-states.md): Alt sözleşmeler satıcıyla anlaşmayı tamamlamak için onaylanabilir, teslimatın tamamlandığını belirtmek için kapatılabilir veya teslimat tamamlanmadan önce satıcıyla sözleşmenin feshedildiğini belirtmek için iptal edilebilir.

### <a name="task-planning"></a>Görev Planlaması
- Sistem yöneticileri için sorun giderme geliştirildi. Kullanıcı bir projeyi açamadığında, yönetici [Proje zamanlama günlüklerinde](../../project-management/schedule-api-logs.md) Project for the Web'den oluşturulan lisansla ilgili olmayan hataları gözden geçirebilir.
- [Microsoft Project for the Web'de görev denetim listelerini kullanın](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). Microsoft Project for the Web'de, belirli öğeleri izlemek için göreve denetim listesi ekleyebilirsiniz.

## <a name="quality-updates"></a>Kalite güncelleştirmeleri

| **Özellik alanı** | **Referans numarası** | **Kalite güncelleştirmeleri** |
| --- | --- | --- |
| Planlama ve İzleme | 2392596 | Zamanlama API'leri artık **Kalan çalışma**, **Tamamlanan çalışma** ve **Tamamlanma yüzdesi** alanlarında güncelleştirmelere izin verir. |
| Planlama ve İzleme | 2478497 | Sistem bunları otomatik numaralandırma kullanarak dolduracağından, API'leri Zamanla **Etkinlik numarası** ve **Görev kimliği** alanları girişte boş olabilir.|
| Zaman ve Gider | 2468135 | Onay yeniden denemelerinin sayısı beşten üçe düşürülür. |
| Zaman ve Gider | 2468188 | **Ek açıklama** varlığının **not metni** özniteliğindeki en fazla uzunluğu aşan günlük metni sorunu giderildi. |
