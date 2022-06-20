---
title: Project Service Automation Güncelleştirme Sürümü 13, V3'teki yenilikler veya değişiklikler
description: Bu makale, Project Service Automation Güncelleştirme Sürümü 13, V3'teki yenilikler hakkında bilgi sağlar.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.reviewer: johnmichalak
ms.openlocfilehash: f4898391922f5ecbc99d78e49358ea749fe27b3f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930710"
---
# <a name="project-service-automation-update-release-13-v3"></a>Project Service Automation, Güncelleştirme Sürümü 13, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Dynamics 365 Project Service Automation (PSA) uygulaması için en son güncelleştirmeyi duyurmaktan mutluluk duyuyoruz. Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir. Bu sürüm Dynamics 365 9.x ile uyumludur. Bu sürüme güncelleştirmek için Dynamics 365 (online) için Yönetim Merkezi'ni ziyaret edin ve güncelleştirmeyi yüklemek için çözümler sayfasına gidin. Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.

Bu makalede, Project Service Automation V3, Güncelleştirme Sürümü 13'de yeni ve değiştirilen özellikler ve düzeltmeler listelenmektedir. Bu sürüm, V3.10.3.18 derleme numarasına sahiptir ve aşağıdaki zamanlamada kullanılabilir:

- **Genel kullanılabilirlik (kendi kendine güncelleştirme):** Kasım 2019
- **Otomatik Güncelleştirme:** Aralık 2019


## <a name="update-release-13"></a>Güncelleştirme Sürümü 13 

### <a name="bug-fixes"></a>Hata düzeltmeleri

- Zaman ve Gider

     - Düzeltildi: **Gider onayı** sayfasındaki arama işlevi, gider amacına göre arama sırasında çalışmıyor.

- Kaynak Yönetimi

     - Düzeltildi: Mutabakattaki sayılar sağa dayalı olacak şekilde güncelleştirildi.
     - Düzeltildi: Adlandırılmış Kaynaklar **Zamanlama** sekmesi üzerinden görevlere atanamaz.

- Proje Yönetimi

     - Düzeltildi: **TransactionType** öğesinde **Birim** ve **DefaultGroup** kurulum bilgileri eksik olduğunda, takım üyesi atanırken boş başvuru özel durumu.

- Sales

     - Düzeltildi: Yinelenen işlem türü kayıtları rol fiyatı kayıtları oluşturulduğunda hata döndürüyor.
     - Sabit: **Yeni Fırsat**, **Teklif**, **sipariş satırı** ve **Ürün ekle** için ekstra düğmeler, fırsatlar, teklifler, sipariş ürünleri ve proje tabanlı satırlar alt Kılavuzu komutlarında görünür.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
