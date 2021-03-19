---
title: Gider yönetimi için iş akışlarını ayarlama
description: Seyahat ve gider belgelerini gözden geçirmek ve onaylamak için kullanılan bir iş akışı işlemi ayarlayabilirsiniz.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: e54fca67427e8f3d0e7050563a751b5be354356c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276057"
---
# <a name="set-up-workflows-for-expense-management"></a>Gider yönetimi için iş akışlarını ayarlama

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Seyahat ve gider belgelerini gözden geçirmek ve onaylamak için bir iş akışı işlemi ayarlayabilirsiniz. Gider raporları, seyahat talepleri ve nakit avans taleplerine yönelik iş akışları tanımlayabilirsiniz.

Bir iş akışı, bir iş sürecini temsil eder ve bir belgenin sistemden nasıl ilerleyeceğini tanımlar. İş akışı aynı zamanda bir görevi kimin tamamlaması veya belgeyi kimin onaylaması gerektiğiniz gösterir. Kuruluşunuzda iş akışı sistemi kullanmanın birçok yararı vardır:

- **Tutarlı işlemler**: Satınalma talepleri ve gider raporları gibi belirli belgeler için onay süreci tanımlayabilirsiniz. İş akışı sistemi kullanılması, belgelerin tutarlı ve verimli bir şekilde işlenmesini ve onaylanmasını sağlar.
- **İşlem görünürlüğü**: Belirli bir iş akışı örneğinin durumunu, geçmişini ve performans ölçümlerini izleyebilirsiniz. Bu, verimliliği artırmak için iş akışına değişikliklerin yapılması gerekip gerekmediğini belirlemenize yardımcı olur.
- **Merkezi çalışma listesi**: Kullanıcılar kendilerine atanan iş akışı görevlerini ve onaylarını görüntülemek için merkezi bir çalışma listesini görüntüleyebilir. 

## <a name="workflow-types"></a>İş akışı türleri

Aşağıdaki tabloda, **Gider yönetimi** öğesinde oluşturabileceğiniz iş akışı türleri listelenmektedir.


|              <strong>Tür</strong>              |                   <strong>Türün kullanım amacı:</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <strong>Gider raporlarını otomatik onaylama</strong> |            Gider raporları için onay iş akışları oluşturun.             |
|  <strong>Gider raporlarını otomatik deftere nakletme</strong>   |        Gider raporları için otomatik deftere nakletme iş akışları oluşturun.        |
|       <strong>Gider satırı öğesi</strong>        |     Gider raporlarında satır öğeleri için onay iş akışları oluşturun.      |
| <strong>Gider satırı öğesi otomatik deftere nakil</strong> | Gider raporlarında satır öğeleri için deftere nakil iş akışları oluşturun. |
|       <strong>Seyahat talebi</strong>       |          Seyahat istekleri için onay iş akışları oluşturun.           |
|      <strong>Nakit avans isteği</strong>      |         Nakit avans istekleri için onay iş akışları oluşturun.          |
|        <strong>KDV vergisinden düşme</strong>        | Katma değer vergisinin (KDV) düşülmesi için onay iş akışları oluşturun.  |


[!INCLUDE[footer-include](../includes/footer-banner.md)]