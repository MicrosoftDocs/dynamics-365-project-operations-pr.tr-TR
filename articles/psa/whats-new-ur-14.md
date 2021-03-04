---
title: Project Service Automation Güncelleştirme Sürümü 14, V3'teki yenilikler veya değişiklikler
description: Bu konu Project Service Automation Güncelleştirme Sürüm 14 V3'teki yenilikler hakkında bilgi sağlar.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: f9347741d8dae2c9a810bb5b3a32d4d6c0a628ed
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147182"
---
# <a name="project-service-automation-update-release-14-v3"></a>Project Service Automation, Güncelleştirme Sürümü 14, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Dynamics 365 Project Service Automation (PSA) uygulaması için en son güncelleştirmeyi duyurmaktan mutluluk duyuyoruz. Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir. Bu sürüm Dynamics 365 9.x ile uyumludur. Bu sürüme güncelleştirmek için Dynamics 365 (online) için Yönetim Merkezi'ni ziyaret edin ve güncelleştirmeyi yüklemek için çözümler sayfasına gidin. Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.

Bu konuda, PSA V3, Güncelleştirme Sürümü 14'te yeni veya değiştirilmiş özellikler ve düzeltmeler listelenir. Bu sürüm, V3.10.4.21 derleme numarasına sahiptir ve aşağıdaki zamanlamada kullanılabilir:

- **Genel kullanılabilirlik (kendi kendine güncelleştirme):** Ocak 2020
- **Otomatik Güncelleştirme:** Şubat 2020

## <a name="update-release-14"></a>Güncelleştirme Sürümü 14

### <a name="enhancements"></a>Geliştirmeler

- Sales

     - **Teklif Satırı Ayrıntıları** içinden gelen özel alan değerleri bir teklif **Kazanıldı olarak kapatıldı** seçeneğine güncelleştirildiğinde **Proje Sözleşmesi Satır Ayrıntıları** altına kopyalanır.
     - Onaylanan projeler **Kaybedildi olarak kapatılabilir**.

- Kaynak Yönetimi

     - Ayırmalar uzatılırken, kullanıcılara ayırma sonuçlarını özetleyen ve Ayırmaları Koru bağlantısı içeren bir onay iletişim kutusu gösterilir.


### <a name="bug-fixes"></a>Hata düzeltmeleri

- Zaman ve Gider

     - Düzeltildi: Kullanıcı düzeltilecek herhangi bir giriş seçmediğinde gerçekleşen kullanıcı deneyimi iyileştirildi.

- Kaynak Yönetimi

     - Düzeltildi: Bir kaynağın birden çok kez ayrılması, ayrılabilir kaynağın adının taşmasına neden oluyor.

- Sales

     - Düzeltildi: Toplam satış fiyatı kullanıcı projedeki gider tahminleri için bir maliyet fiyatı girene kadar hesaplanmıyor.
     - Düzeltildi: İlişkili proje sözleşmesi **Taslak** durumunda değilse, teklif **Kazanıldı** olarak kapatılamıyor.



[!INCLUDE[footer-include](../includes/footer-banner.md)]