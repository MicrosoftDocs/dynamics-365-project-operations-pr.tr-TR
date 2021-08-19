---
title: Project Service Automation Güncelleştirme Sürümü 32, V3'teki yenilikler veya değişiklikler
description: Bu konuda, Project Service Automation, Güncelleştirme Sürümü 32, V3'teki özellikler ve düzeltmeler listelenir.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 023e51e834060a35d2d7e3469d34297192e38ba11c12a2c4f57424213aba44ba
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994885"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a>Project Service Automation Güncelleştirme Sürümü 32, V3'teki yenilikler veya değişiklikler

[!include [banner](../includes/psa-now-project-operations.md)]

Microsoft Dynamics 365 Project Service Automation uygulaması için en yeni güncelleştirmeyi sunmaktan mutluluk duyarız. Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir. Dynamics 365 9.x ile uyumludur. Bu sürüme güncelleştirmek için Dynamics 365 çevrimiçi çözümler sayfasının için Yönetici Merkezi sayfasını ziyaret edin ve güncelleştirmeyi kurun. Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.

Bu konuda, Project Service Automation Güncelleştirme Sürümü 32 V3'te yeni veya değiştirilmiş özellikler ve düzeltmeler listelenmektedir. Bu sürümün derleme numarası V3.10.53.108'dir ve genellikle Haziran 2021'de kendi kendine güncelleştirme aracılığıyla kullanılabilir.

## <a name="update-release-32"></a>Güncelleştirme Sürümü 32

### <a name="bug-fixes"></a>Hata düzeltmeleri

#### <a name="general"></a>Genel

- Büyük bir yükseltme başarısız olduğunda, paylaşılan varlıkların hala erişilebilir olduğundan emin olmak için yalnızca ana uygulama giriş noktalarının engellenmesi gerekir.

#### <a name="time-and-expense"></a>Zaman ve Gider

Aşağıdaki sorunlar giderilmiştir:

- **TimeEntriesImportFromResourceAssignment**, kaynak atama kontur diliminin başlangıç ve bitiş saatlerini korumaz.
- **Zaman Girişi** ızgarasında **Açık Giriş**'i seçtiğinizde, diğer formların seçilmesini engellemiş olabilirsiniz.
- Zaman girişlerine atamaları aktarırken istemci kod sorgusu, sorguyu geçemeyen uzun bir URL oluşturabilir.
- **Zaman Girişi** ızgarasında bir değer bir hücreden silindikten sonra, odak ızgara içinde kalmaz.
- Modern onaylar için **İşleme onayları** görünümünden **Reddet** düğmesi kaldırılmıştır.
- Zaman girişi toplu onayının kararlılığı ve performansı, kilitlenmelerden etkilenir ve **Zaman Girişi** varlığıyla ilişkili özelleştirmelerin uygun şekilde işlenememesinden etkilenir.

#### <a name="project-planning"></a>Proje Planlama

- **Sözleşme Birimi** alanında null değere sahip bir projeyi güncelleştirdiğinizde null başvuru istisnası oluşturulur.
- **Proje Toplamlarını Yenile**, projedeki kalan maliyeti ve kalan satışları yanlış şekilde hesaplar.
- Yedek fiyatlandırma hesaplamaları, kaynak atama dağılımlarındaki güncelleştirmelerle ilgili performansı etkiler.

#### <a name="resource-management"></a>Kaynak Yönetimi

Aşağıdaki sorun düzeltildi:

- Ayrılabilir bir kaynağın takvim kapasitesi 1'den fazla olduğunda, Project Service Automation kapasiteyi yanlış bir şekilde 0 (sıfır) olarak tanır. Bu nedenle zamanlama görünümünde sonsuz bir döngü oluşur.

#### <a name="sales"></a>Satışlar

Aşağıdaki sorunlar giderilmiştir:

- Özel bir hareket türüne sahip bir günlük satırı oluşturulduğunda, şu null başvuru özel durumu oluşturulur: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.
- Bir teklif kopyalanmadan önce devre dışı bırakılan roller ve kategoriler, yeni kopyalanan teklifin borçlandırılabilir rol ve kategorilerine eklenmemelidir.
- Belge tarihi ve muhasebe tarihi, doğrudan bir taslak faturada oluşturulan fatura satırı ayrıntısı üzerinde sağlanan başlangıç tarihiyle uyumlu değildir.
- Null başvuru istisnaları, bir teklif kopyalanmadan önce rollerin ve kategorilerin etkinleştirilmesiyle ilgili senaryolarda üretilir.
- **Projeler** sayfasındaki **Fiyatları güncelleştir** eylemi, masraf tahminlerini ve malzeme tahminlerini güncelleştirmez.
