---
title: Faturalama sürecine genel bakış
description: Bu konuda, kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations uygulamasında faturalamaya genel bir bakış sağlanmaktadır.
author: sigitac
manager: Annbe
ms.date: 01/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fbc1519b6cbcf231cfa89df8b7843d11a8904e49
ms.sourcegitcommit: b4298ca4729643c1040ef35dde8c67f829461ce7
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2021
ms.locfileid: "5089316"
---
# <a name="invoicing-process-overview"></a>Faturalama sürecine genel bakış

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Project Operations, kaynağı/stoğu tutulmayanları temel alan senaryolar için hem Proje yöneticisinin hem de Alacak hesapları memurunun/proje muhasebecisinin ihtiyaçlarına uyacak şekilde uyarlanmış kapsamlı yetenekler sunar. Faturalama sürecinde Proje yöneticisi, proje faturalaması biriktirme listesini yönetir ve Alacak hesapları memuru/proje muhasebecisi, uyumlu ve müşteriye yönelik doğru bir fatura belgesi oluşturur.

![Faturalama akışı diyagramı](./media/invoicing-flow.png)

Proje sözleşmesi satırı, ilişkili proje işlemleri için faturalama yöntemini tanımlar. Proje yöneticisi zaman ve gider işlemlerini onayladığında sistem, **Proje Gerçek Tutarları** varlığındaki işlemleri kaydeder ve bilgileri Dynamics 365 Finance uygulamasındaki **Proje yönetimi ve muhasebe** modülüne gönderir. Proje muhasebecisi daha sonra [Project Operations Entegrasyon günlüğü](../project-accounting/project-operations-integration-journal.md)'nü kullanarak kayıtları inceler ve deftere kaydeder. Bu günlük; proje gerçek tutarları için faturalama, satış vergisi grubu, faturalama öğesi satış vergisi grubu ve mali boyutlar gibi önemli muhasebe ayrıntılarını içerir.

Proje yöneticisi, [Zaman ve malzeme faturalama biriktirme listesi](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog)'ndeki zaman ve malzeme faturalama yöntemini ve [Sabit fiyat kilometre taşları](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones)'ndaki malzeme faturalama biriktirme listesini kullanarak faturalanmayan satış işlemlerini inceleyebilir. Bu görünümler, bir sonraki faturalama döngüsüne dahil edilmesi gereken işlemleri filtrelemenize ve seçmenize ve ardından bunları **Faturalanmaya Hazır** olarak işaretlemenize olanak tanır.

[El ile bir proforma fatura oluşturabilir](../proforma-invoicing/create-manual-proforma-invoice.md) veya bir [dönemsel işlem](../proforma-invoicing/configure-automated-invoice-creation.md) kullanabilirsiniz. Proje yöneticisi gerektiğinde [taslak proforma fatura düzenleyebilir](../proforma-invoicing/manage-proforma-invoice.md) ve ardından onaylayabilir.

Onaylanan proforma fatura, Finance uygulamasındaki **Proje yönetimi ve muhasebe** modülüne gönderilir. Proje muhasebecisi, proje faturası teklifini biçimlendirip güncelleştirir ve ardından belgeyi deftere kaydederek yazdırır. Gönderilen proje faturaları, Genel muhasebe defterinin yanı sıra Müşteri ve Proje alt defterlerine de kaydedilir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]