---
title: Project Operations'da alt sözleşme yönetimi
description: Bu konu, Microsoft Dynamics 365 Project Operations'taki uç-uç taşeron yönetim sürecine genel bir bakış sağlar.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6ffceb0886fdc841ea01a099243cf4eeb43e5374a18414576f3639a3e50857fd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994255"
---
# <a name="subcontract-management-in-project-operations"></a>Project Operations'da alt sözleşme yönetimi

[!include [banner](../../includes/dataverse-preview.md)]

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Microsoft Dynamics 365 Project Operations'ta taşeronluk aşağıdaki iş süreci akışı destekler.

![Taşeron işlem akışı](../media/SubcontractingProcessFlow.png)

İşte taşeronluk işleminin adım adım açıklaması.

1. Proje yöneticisi bir satıcıyla taşeron oluşturur. Varsayılan olarak, taşeron için satıcı kaydına iliştirilmiş fiyat listeleri kullanılır. Satıcı hesabının **satıcı** veya **tedarikçi** ilişki türü vardır.
2. Proje yöneticisi tüm satınalmaları taşeronda satır maddeleri olarak listeleyebilir. Taşeron satırları zaman, masraf veya ürünler için olabilir. Her taşeron satırında seçilen hareket sınıfı, satırın ne için olduğunu belirler.
3. Satıcı hesap yöneticisi ve proje yöneticisi taşeron üzerinden yineleme yapabilir. Fiyatlandırma alt sözleşmeye ekli olan satın alma fiyat listelerinde ayarlanabilir.
4. Bu noktada veya işlemin ilerleyen saatlerinde, taşeron satırı zaman içinse, satıcı hesap yöneticisi ilgili kişileri her taşeron satırıyla ilişkilendirir. Bu ilişkilendirme, taşeron üzerinde çalışan proje yöneticisine bilgi sağlar. Bir ilgili kişi taşeron hattıyla ilişkilendirildiğinde, rezerve edilebilir bir kaynak yoksa, sistem ilgili kişiden otomatik olarak rezerve edilebilir bir kaynak oluşturur.
5. Her taşeron satırındaki faturalama yöntemi **Sabit Fiyat** veya **Zaman ve Malzeme** olabilir. Sabit fiyatlı taşeron satırları için kilometre taşı tabanlı bir fatura planı ayarlayabilirsiniz.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
