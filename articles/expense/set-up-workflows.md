---
title: Gider yönetimi için iş akışlarını ayarlama
description: Seyahat ve gider belgelerini gözden geçirmek ve onaylamak için kullanılan bir iş akışı işlemi ayarlayabilirsiniz.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: dfc5945f32bb8d4073fc31499979ba279fef66a4
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896575"
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
