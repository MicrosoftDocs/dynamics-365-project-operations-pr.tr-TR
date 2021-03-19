---
title: Proje tabanlı fırsat yönetimi
description: Bu konu, projelerle ilgili fırsatlarla nasıl çalışılacağı hakkında bilgi sağlar.
author: rumant
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2d1f9b29e0e9516ff78517e47694a2385c083ec7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277857"
---
# <a name="manage-project-based-opportunities"></a>Proje tabanlı fırsat yönetimi

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Proje tabanlı şirketlerin, genellikle birden çok ülkeye ve coğrafi bölgelerde teslimat işlemleri vardır. Projenin yürütülme ve teslimat maliyeti, teslimi hangi Coğrafya veya bölmenin yönetmediğini temel alarak değişiklik gösterebilir. Bunun için, bu işlem, anlaşma kenar boşluklarını etkileyebilir. Proje tabanlı servislerin teslimatı genellikle büyük miktarda insan kaynakları süresi, seyahat için önemli giderler, malzeme maliyetleri ve diğer giderler içerir.

Dynamics 365 Project Operations'ta proje tabanlı fırsatlar, Dynamics 365 Sales için uzantılarla tasarlanmıştır. Konu, proje tabanlı şirketlerin proje bazlı fırsatları yönetmesi için gereken ek işlevselliğe dahil edilen farklı alanlar ve iş mantığı hakkında ayrıntılar sağlar.

## <a name="view-all-project-based-opportunities"></a>Proje tabanlı fırsatları görüntüleme

Proje tabanlı tüm fırsatların listesi **Fırsat** listesi sayfasından görülebilir. 

1. **Satış** > **Fırsatlar**'a gidin.
2. Fırsatların diğer filtre uygulanmış görünümlerini seçmek için **görünüm değiştiriciyi** kullanın. Bu görünümleri ve gezinti seçeneklerini yapılandırmak için özel filtre ölçütleriyle birlikte kendi görünümlerinizi oluşturabilirsiniz.

Proje Fırsatları, bu liste sayfasından veya ayrıntı sayfasından oluşturulabilir veya silinebilir.

## <a name="business-process-flow-for-project-based-deals"></a>Proje tabanlı anlaşmalar için iş süreci akışı

Project Operations'ta proje tabanlı anlaşmalar için aşağıdaki iş süreci akışları desteklenir:

- Müşteri Adayından Fırsata iş süreci
- Fırsat satış süreci

### <a name="lead-to-opportunity-business-process"></a>Müşteri Adayından Fırsata iş süreci 
Müşteri Adayından Fırsata iş süreci aşağıdaki aşamaları destekler:

| Aşama | Eşlenen varlık | İşlev |
| --- | --- | --- |
| Nitelikli Hale Getir | Müşteri adayı | Firma, ilgili kişi ve fırsat oluşturmak için müşteri adayını uygun bulun. |
| Geliştir | Fırsat | Mevcut çalışmalar, önemli paydaşlar ve rekabet hakkında daha fazla bilgi eklemek için fırsatı geliştirin. |
| Teklif Et | Fırsat | Teklifi geliştirin ve dahili inceleme takımından onay alın. |
| Kapat | Fırsat | Anlaşmaya varmak için fırsatı kazanın. |

### <a name="opportunity-sales-process"></a>Fırsat satış süreci
Proje İşlemlerindeki fırsat satış süreci, satış uygulamasındaki fırsat satışları işi iş akışına bir uzantıdır. Bu iş süreci proje tabanlı bir fırsatta aşağıdaki aşamaları desteklemek için kullanıma hazır olarak tasarlanmıştır.

| Aşama | Eşlenen varlık | İşlev |
| --- | --- | --- |
| Nitelikli Hale Getir | Fırsat | Firma, ilgili kişi ve fırsat oluşturmak için müşteri adayını uygun bulun. |
| Teklif Et | Teklif | Proje tekliflerini kullanarak teklifi geliştirin ve dahili inceleme takımından onay alın. |
| Sözleşme | Proje Sözleşmesi | Sözleşmeyi oluşturmak için teklifi kazanın ve projede yürütmeye ve teslimata başlanır. |
| Kapat | Proje Sözleşmesi | İşi başarıyla bitirin ve proje sözleşmesini kapatın. |

> [!NOTE]
> Proje tabanlı anlaşma bir müşteri adayıyla başlatıldıysa, fırsatın iş fırsatına göre önceliği vardır.
>
> Proje tabanlı anlaşma bir Fırsatla başlatıldıysa, Fırsat satışları iş fırsatına göre önceliği vardır.

Satış sürecinizi gerektiği gibi izlemek için ürün iş süreci akışı düzenleyebilir veya kendi iş süreci akışlarınızı oluşturabilirsiniz. İş süreci akışları hakkında daha fazla bilgi için bkz. [İş süreci akışlarına genel bakış](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).


[!INCLUDE[footer-include](../includes/footer-banner.md)]