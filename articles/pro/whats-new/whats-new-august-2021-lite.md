---
title: Ağustos 2021'deki yenilikler - Project Operations lite dağıtımı
description: Project Operations lite dağıtımının Ağustos 2021 sürümünde bulunan kalite güncelleştirmeleri hakkında bilgi sağlar.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3cb6f92bfb28dc64f0f689e0070b0506644c2320
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586460"
---
# <a name="whats-new-august-2021---project-operations-lite-deployment"></a>Ağustos 2021'deki yenilikler - Project Operations lite dağıtımı

_Şunlar için geçerlidir: Lite dağıtımı - anlaşmadan proforma faturaya_

Bu konu aşağıdaki Dynamics 365 Project Operations bileşenleri ve sürümleri için geçerlidir:

  - Dataverse ortamı sürüm 4.13.0.152'te Project Operations

## <a name="features-included-in-this-release"></a>Bu sürümde yer alan özellikler

Bu sürümde aşağıdaki özellikler yer almaktadır:

- **Onay kümeleri**: Onay kümeleri zaman, gider veya malzeme kullanımı onay isteklerini daha küçük işlem alt kümelerinde bir araya getirir. Bu gruplandırma, onayların projeye göre belirli bir sırada işlenmesine ve yeniden denemeye ve sıralamaya olanak tanır. İsteklerin gruplandırılması, büyük hacimli onaylar için onay işleminin güvenilirliğini ve izlenebilirliğini artırır. Daha fazla bilgi için bkz. [Onay kümeleri](../../approvals/approval-sets.md).

## <a name="quality-updates"></a>Kalite güncelleştirmeleri

### <a name="project-operations-on-dataverse"></a>Dataverse üzerinde Project Operations

| **Özellik alanı** | **Referans numarası** | **Kalite güncelleştirmeleri** |
| --- | --- | --- |
| Fatura ve fiyatlandırma | 2295625 | Kilometre taşı adı, fatura zamanlamasından fatura satırı ayrıntısına kopyalanmalıdır. |
| Fatura ve fiyatlandırma | 2316323 | İndirim, kaynak tabanlı senaryolar için Project Operations'da proforma faturada düzenlenebilir olmamalıdır. |
|   Fırsat yönetimi | 2338619 | **Fırsat** ve **Teklif** iş kurallarının yalnızca sayfalarda çağrılması gerekir. |
| Kaynak yönetimi | 2316523 | Ekli rolü bulunan kaynak gereksinimden **İstek Gönder** kullanıldığında hata gösterilmemelidir. |
| Kaynak yönetimi | 2326885 | Proje aracılığıyla kaynak gereksinimi oluşturma işlemi hata görüntülememelidir. |
| Zaman ve gider | 2335584 | Zaman girişindeki kullanım dışı bırakılan görev akışları. |
| Zaman ve gider | 2336884 | **Haftayı Kopyala** zaman girişi düğmesi, geçerli kullanıcıdan daha fazlası için çalışmalıdır. |
