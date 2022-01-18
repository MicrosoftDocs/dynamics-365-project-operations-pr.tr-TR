---
title: "Kasım 2021'deki Yenilikler: Project Operations lite dağıtımı"
description: Bu konu, Project Operations Lite dağıtımı için Kasım 2021 sürümünde yer alan kalite güncelleştirmeleri hakkında bilgi sağlar.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0fd910fb1b1e4e4576afa386a600e56e6f2dd504
ms.sourcegitcommit: 9d20e7738cce195d344f5925a115741a1ce3ca36
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/21/2021
ms.locfileid: "7942955"
---
# <a name="whats-new-november-2021---project-operations-lite-deployment"></a>Kasım 2021'deki Yenilikler: Project Operations lite dağıtımı

_Şunlar için geçerlidir: Lite dağıtımı - anlaşmadan proforma faturaya_

Bu konu aşağıdaki Microsoft Dynamics 365 Project Operations bileşenleri ve sürümleri için geçerlidir:

- Dataverse ortamı sürüm 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155'teki Project Operations
  
## <a name="features-included-in-this-release"></a>Bu sürümde yer alan özellikler

Bu sürümde aşağıdaki özellikler yer almaktadır:

- Proje Zamanlama uygulaması programlama arabirimleri (API) artık Proje demetleri oluşturma ve silme özelliğini desteklemektedir

## <a name="quality-updates"></a>Kalite güncelleştirmeleri

### <a name="project-operations-in-dataverse"></a>Dataverse'de Project Operations

| Özellik alanı | Referans numarası | Kalite güncelleştirmeleri |
| --- | --- | --- |
| Fatura ve Fiyatlandırma | 2358236 | Fatura düzeltmesi, sıfır fiyatlı satırları bulunan düzeltmelere izin vermelidir. |
| Kaynak Yönetimi | 2410072 | Göreve proje yöneticisi olarak atanan bir kaynağın ayarlanmasına izin verir. |
| Fatura ve Fiyatlandırma | 2430234 | Maliyet performans hesaplaması sorununu düzeltir. |
| Zaman ve Gider | 2436978 | Saatin, ss:dd biçiminde girilmesine olanak tanır. |
| Fatura ve Fiyatlandırma | 2448623 | Fiyat listelerinin Bir kuruluş birimiyle ilişkilendirildikten sonra güncelleştirilmesine izin verir. |
| Zaman ve Gider | 2460396 | Bir zaman girişinin hücre temizlendiğinde silinmesine izin verir. |
| Fatura ve Fiyatlandırma | 2467386 | Görev kazanılmış bir teklifle ilişkilendirilmiş olsa bile, görevi bulunan bir projenin silinmesine izin verir. |
| Zaman ve Gider | 2461744 | **Başarısız onayım** görünümü, yalnızca **Gönderilen** aşamasındaki proje onaylarını içerir. |
| Zaman ve Gider | 2464082 | Bir hedef durumu eşleştiğinde, proje onaylarının onay kümesine bağlantısını kaldırır. |
| Zaman ve Gider | 2468108 | Zamanlama işi, onay kümesi için bir **İşleme** durumu ayarlamamalıdır. |
| Zaman ve Gider | 2471503 | Yedi gün öncesine ait onay kümelerini silin. |
| Fatura ve Fiyatlandırma | 2480687 | Teklif satırı kilometre taşı oluşturulduğunda teklif satırı başvurusu kaldırılmamalıdır. |
