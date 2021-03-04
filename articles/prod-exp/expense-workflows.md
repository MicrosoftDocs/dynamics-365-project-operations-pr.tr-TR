---
title: Gider yönetimi çalışma akışları ayarlama
description: Seyahat ve gider belgelerini gözden geçirmek ve onaylamak için bir iş akışı işlemi ayarlayabilirsiniz.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8f3235d12499c68a52f9d1c7e118e7bc91dc3a0a
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960541"
---
# <a name="set-up-expense-management-workflows"></a>Gider yönetimi çalışma akışları ayarlama

Seyahat ve gider belgelerini gözden geçirmek ve onaylamak için kullanılan bir iş akışı işlemi ayarlayabilirsiniz. İş akışlarının tanımlanabildiği belgelere gider raporları, seyahat talepleri ve nakit avans talepleri dahildir.

Bir iş akışı, bir iş işlemini temsil eder. Bir belgenin sistemde nasıl akar ve bir görevi tamamlamasını veya belgeyi onaylaması gerektiğini gösterir. Kuruluşunuzda iş akışı sistemi kullanmanın birçok yararı vardır:

-   **Tutarlı işlemler**: Satınalma talepleri ve gider raporları gibi belirli belgeler için onay süreci tanımlayabilirsiniz. İş akışı sistemi kullanılması, belgelerin tutarlı ve verimli bir şekilde işlenmesini ve onaylanmasını sağlar.

-   İşlem görünürlüğü: Belirli bir iş akışı örneğinin durumunu, geçmişini ve performans ölçümlerini izleyebilirsiniz. Bu, verimliliği artırmak için iş akışına değişikliklerin yapılması gerekip gerekmediğini belirlemenize yardımcı olur.

-   Merkezi çalışma listesi: Kullanıcılar kendilerine atanan iş akışı görevlerini ve onaylarını görüntülemek için merkezi bir çalışma listesini görüntüleyebilir. 

**Oluşturabileceğiniz iş akışı türleri**

Aşağıdaki tabloda, **Gider** öğesinde oluşturabileceğiniz iş akışı türleri listelenmektedir.


|              <strong>Tür</strong>              |                   <strong>Türün kullanım amacı:</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <strong>Gider raporu</strong>         |            Gider raporları için onay iş akışları oluşturun.             |
|  <strong>Gider raporlarını otomatik deftere nakletme</strong>   |        Gider raporları için otomatik deftere nakletme iş akışları oluşturun.        |
|       <strong>Gider satırı öğesi</strong>        |     Gider raporlarında satır öğeleri için onay iş akışları oluşturun.      |
| <strong>Gider satırı öğesi otomatik deftere nakil</strong> | Gider raporlarında satır öğeleri için deftere nakil iş akışları oluşturun. |
|       <strong>Seyahat talebi</strong>       |          Seyahat istekleri için onay iş akışları oluşturun.           |
|      <strong>Nakit avans isteği</strong>      |         Nakit avans istekleri için onay iş akışları oluşturun.          |
|        <strong>KDV vergisinden düşme</strong>        | Katma değer vergisinin (KDV) düşülmesi için onay iş akışları oluşturun.  |

