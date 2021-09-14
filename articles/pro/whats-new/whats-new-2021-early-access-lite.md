---
title: Yeni 2021 2. erken erişim sürümündeki yenilikler - Project Operations lite dağıtımı
description: Bu konu, Project Operations lite dağıtımının Temmuz 2021 2. dalga erken erişim sürümünde bulunan özellikler hakkında bilgi sağlar.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a201e3e4333b8892eea72387222d64e18b74d71b
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323935"
---
# <a name="whats-new-2021-wave-2-early-access---project-operations-lite-deployment"></a>Yeni 2021 2. erken erişim sürümündeki yenilikler - Project Operations lite dağıtımı

_Şunlar için geçerlidir: Lite dağıtımı - anlaşmadan proforma faturaya_

Bu konu aşağıdaki Dynamics 365 Project Operations bileşenleri ve sürümleri için geçerlidir:

  - Dataverse ortamı sürüm 4.23.0.4'te Project Operations

Sürüm yalnızca bir ortam [Erken Erişim için etkinleştirildiğinde](/power-platform/admin/opt-in-early-access-updates#how-to-enable-early-access-updates) geçerlidir.

## <a name="features-included-in-this-release"></a>Bu sürümde yer alan özellikler

[Alt Sözleşme yönetimi](../subcontracting/subcontracting_EA_scope.md) - Bu özellik bir projedeki işin tüm yönleri üzerinde daha iyi görünürlük ve denetim sağlar. Alt sözleşme yönetimi önizlemesi aşağıdaki özellikleri içerir:

  - Proje yöneticisi bir satıcıyla alt sözleşme oluşturabilir. Varsayılan olarak, taşeron için satıcı kaydına iliştirilmiş fiyat listeleri kullanılır. Satıcı hesabının **satıcı** veya **tedarikçi** ilişki türü vardır.
  - Bir proje yöneticisi tüm satınalmaları alt sözleşmede satır maddeleri olarak listeleyebilir. Taşeron satırları zaman, masraf veya ürünler için olabilir. Alt sözleşme satırının işlem sınıfı, satırın ne için olduğunu belirler.
  - Satıcı hesap yöneticisi ve proje yöneticisi taşeron üzerinden yineleme yapabilir. Fiyatlandırma alt sözleşmeye ekli olan satın alma fiyat listelerinde ayarlanabilir.
  - Süreç boyunca, alt sözleme satırı zaman içinse, satıcı hesap yöneticisi satıcı ilgili kişilerini her bir alt sözleşme satırıyla ilişkilendirebilir. Bu ilişkilendirme, taşeron üzerinde çalışan proje yöneticisine bilgi sağlar. Bir satıcı ilgili kişisi alt sözleşme satırıyla ilişkilendirildiğinde, ayrılabilir bir kaynak yoksa sistem, ilgili kişiden otomatik olarak ayrılabilir bir kaynak oluşturur.
  - Her alt sözleşme satırındaki faturalama yöntemi sabit fiyat veya zaman ve malzeme olabilir. Sabit fiyatlı alt sözleşme satırları için kilometre taşı tabanlı bir fatura zamanlaması ayarlanır.
