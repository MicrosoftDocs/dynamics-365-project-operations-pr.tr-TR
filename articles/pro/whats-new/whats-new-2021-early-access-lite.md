---
title: Yeni 2021 2. erken erişim sürümündeki yenilikler - Project Operations lite dağıtımı
description: Bu makale, Project Operations lite dağıtımının 2021 dalga 2 erken erişim sürümünde kullanılabilen özellikler hakkında bilgi sağlar.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d245868c8bd9ff332707a81c074d6c7ae3649378
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924132"
---
# <a name="whats-new-2021-wave-2-early-access---project-operations-lite-deployment"></a>Yeni 2021 2. erken erişim sürümündeki yenilikler - Project Operations lite dağıtımı

_Şunlar için geçerlidir: Lite dağıtımı - anlaşmadan proforma faturaya_

Bu makale aşağıdaki Dynamics 365 Project Operations bileşenleri ve sürümleri için geçerlidir:

  - Dataverse ortamı sürüm 4.23.0.4'te Project Operations

Sürüm yalnızca bir ortam [Erken Erişim için etkinleştirildiğinde](/power-platform/admin/opt-in-early-access-updates#how-to-enable-early-access-updates) geçerlidir.

## <a name="features-included-in-this-release"></a>Bu sürümde yer alan özellikler

[Alt Sözleşme yönetimi](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview) - Bu özellik bir projedeki işin tüm yönleri üzerinde daha iyi görünürlük ve denetim sağlar. Alt sözleşme yönetimi önizlemesi aşağıdaki özellikleri içerir:

  - Proje yöneticisi bir satıcıyla alt sözleşme oluşturabilir. Varsayılan olarak, taşeron için satıcı kaydına iliştirilmiş fiyat listeleri kullanılır. Satıcı hesabının **satıcı** veya **tedarikçi** ilişki türü vardır.
  - Bir proje yöneticisi tüm satınalmaları alt sözleşmede satır maddeleri olarak listeleyebilir. Taşeron satırları zaman, masraf veya ürünler için olabilir. Alt sözleşme satırının işlem sınıfı, satırın ne için olduğunu belirler.
  - Satıcı hesap yöneticisi ve proje yöneticisi taşeron üzerinden yineleme yapabilir. Fiyatlandırma alt sözleşmeye ekli olan satın alma fiyat listelerinde ayarlanabilir.
  - Süreç boyunca, alt sözleme satırı zaman içinse, satıcı hesap yöneticisi satıcı ilgili kişilerini her bir alt sözleşme satırıyla ilişkilendirebilir. Bu ilişkilendirme, taşeron üzerinde çalışan proje yöneticisine bilgi sağlar. Bir satıcı ilgili kişisi alt sözleşme satırıyla ilişkilendirildiğinde, ayrılabilir bir kaynak yoksa sistem, ilgili kişiden otomatik olarak ayrılabilir bir kaynak oluşturur.
  - Her alt sözleşme satırındaki faturalama yöntemi sabit fiyat veya zaman ve malzeme olabilir. Sabit fiyatlı alt sözleşme satırları için kilometre taşı tabanlı bir fatura zamanlaması ayarlanır.
