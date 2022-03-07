---
title: Project Service Automation Güncelleştirme Sürümü 29, V3'teki yenilikler veya değişiklikler
description: Bu konuda, Project Service Automation, Güncelleştirme Sürümü 29, V3'teki özellikler ve düzeltmeler listelenir.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 87f10d793f9edc055444a3cecea9ea709c1fd7ff7213d6cfaf6b3cbe83a6a5a6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6985120"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a>Project Service Automation Güncelleştirme Sürümü 29, V3'teki yenilikler veya değişiklikler

[!include [banner](../includes/psa-now-project-operations.md)]

Dynamics 365 için Project Service Automation uygulamasına yönelik en son güncelleştirmeyi duyurmaktan mutluluk duyuyoruz. Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir. Bu sürüm Dynamics 365 9.x ile uyumludur. Bu sürüme güncelleştirmek için Dynamics 365 online çözümler sayfası için Yönetim Merkezi'ni ziyaret edin ve güncelleştirmeyi yükleyin. Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.

Bu konuda, Project Service Automation Güncelleştirme Sürümü 29 V3'te yeni veya değiştirilmiş özellikler ve düzeltmeler listelenmektedir. Bu sürümün derleme numarası V3.10.47.7'tür ve genellikle Şubat 2021'de kendi kendini güncelleştirme aracılığıyla kullanılabilir.

## <a name="update-release-29"></a>Güncelleştirme Sürümü 29

### <a name="bug-fixes"></a>Hata düzeltmeleri

**Zaman ve Gider**

Aşağıdaki sorunlar giderilmiştir:

- Kullanıcılar, zaman girişi ızgarasında çalışma dışı günlerde günlüğe kaydedilen çalışma saatlerini göremez.
- Onaylanan gider girişleri, kılavuzda düzenlenebilir.

**Proje Yönetimi**

Aşağıdaki sorunlar giderilmiştir:

- Kaynak atama çalışma saatlerinin negatif olamamasını sağlamak için doğrulama mantığı eksik.
- **AssignResourcesForTask** özel eylemi yalnızca değiştirilen alanlar yerine tüm alanları güncelleştirir.
- **CreateProject** olayında kaydedilen eklentiler veya iş akışları olan bir ortamda bir projeyi kopyalarken **CopyWBSToProject** başarısız olursa **msdyn_bulkgenerationstatus** özniteliği güncelleştirilmez.
- Proje takvimini genişlettiğinizde çalışma günleri, bazı proje görevi güncelleştirmelerinin başarısız olmasına neden olacak şekilde artan düzende sıralanmaz.
- Mevcut bir projede Proje Yöneticisi'ni değiştirmek, kuruluş birimi varsayılan mantığını tetikler.

**Satışlar**

Aşağıdaki sorunlar giderilmiştir:

- **Sözleşme** sayfasındaki **Sözleşme Performansı** sekmesi, sözleşme satırı olmadığında başlatma sırasında sessizce başarısız olur.