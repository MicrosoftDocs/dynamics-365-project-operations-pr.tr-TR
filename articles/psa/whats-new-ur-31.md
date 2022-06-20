---
title: Project Service Automation Güncelleştirme Sürümü 31, V3'teki yenilikler veya değişiklikler
description: Bu makalede, Project Service Automation Güncelleştirme Sürümü 31, V3'de bulunan özellikler ve düzeltmeler listelenmektedir.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: 8d62b12a5363637e46b29c2e9edf4e1f17da729f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925052"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a>Project Service Automation Güncelleştirme Sürümü 31, V3'teki yenilikler veya değişiklikler

[!include [banner](../includes/psa-now-project-operations.md)]

Dynamics 365 için Project Service Automation uygulamasına yönelik en son güncelleştirmeyi duyurmaktan mutluluk duyuyoruz. Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir. Bu sürüm Dynamics 365 9.x ile uyumludur. Bu sürüme güncelleştirmek için Dynamics 365 online çözümler sayfası için Yönetim Merkezi'ni ziyaret edin ve güncelleştirmeyi yükleyin. Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.

Bu makalede, Project Service Automation V3, Güncelleştirme Sürümü 31'de yeni ve değiştirilen özellikler ve düzeltmeler listelenmektedir. Bu sürüm, V3.10.52.77 derleme numarasına sahiptir ve Mayıs 2021'de kendi başına güncelleştirme olarak genel kullanıma sunulmuştur.

## <a name="update-release-31"></a>Güncelleştirme Sürümü 31

### <a name="bug-fixes"></a>Hata düzeltmeleri

**Zaman ve Gider**

Aşağıdaki sorunlar giderilmiştir:

- **Ayrılabilir kaynak** sayfasındaki saat girişi denetimi komut düğmeleri kafa karıştırıcı olarak kullanıldı.
- **Project.SetTrackingFields**'de bir zaman girişi onaylarken bir null başvuru özel durumu üretildi.

**Kaynak Yönetimi**

Aşağıdaki sorunlar giderilmiştir:

- **Takım üyesi oluşturma**, **Varsayılan ayırma durumu taahhüt** ayarı için ayar meta verileri ayarını doğru olarak görüntülemez.
- PSA 1.X'den 3.X'e yükseltilirken yükseltme işlemi, **UpgradeResourceRequirements**'de başarısız olur .


**Satışlar**

Aşağıdaki sorunlar giderilmiştir:

- Gerçek gelir miktarları izleme kılavuzundaki proje para birimine dönüştürür.
- Bir kuruluşun temel para biriminin proje para biriminden farklı olduğu senaryolarda günlük satırları, teklif satırları ve sözleşme satırları oluştururken varsayılan para birimi belirsiz olur.
- **Bekleyen düzeltme günlüğü doğrulama** sorgusu projeye göre filtremiyor.
- Kalan satışlar, proje üzerinde yanlış hesaplanır.
- İlgili kişiye dayanan teklifler, Fiyat listesi olmadan oluşturulduklarında başarısız olur.
- **Faturayı Onayla** seçeneğini belirlediğinizde hiçbir işleme değiştiricisi görüntülenmez.
- **Fatura Oluştur** seçeneğini belirlediğinizde hiçbir işleme değiştiricisi görüntülenmez.
- Bir teklifin kaybedilmesi kayıp olarak kapatılırsa, rezervasyon iptal edilebilir.







