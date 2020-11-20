---
title: Project Service Automation Güncelleştirme Sürümü 18, V3'teki yenilikler veya değişiklikler
description: Bu konuda, Project Service Automation, Güncelleştirme Sürümü 18, V3'teki özellikler ve düzeltmeler listelenir.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: 3a6d3ee21ecf742b2253132f3d3cc1cb2b57af75
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119892"
---
# <a name="project-service-automation-update-release-18-v3"></a>Project Service Automation, Güncelleştirme Sürümü 18, V3

Dynamics 365 için Project Service Automation uygulamasına yönelik en son güncelleştirmeyi duyurmaktan mutluluk duyuyoruz. Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir. Bu sürüm Dynamics 365 9.x ile uyumludur. Bu sürüme güncelleştirmek için Dynamics 365 online Yönetim Merkezi'ni ziyaret edin ve çözümler sayfasından güncelleştirmeyi yükleyin. Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.

Bu konuda, Project Service Automation V3, Güncelleştirme Sürümü 18'de yeni veya değiştirilmiş özellikler ve düzeltmeler listelenir. Bu sürüm, V3.10.8.12 derleme numarasına sahiptir ve Nisan 2020'de kendi başına güncelleştirme olarak genel kullanıma sunulmuştur.

## <a name="update-release-18"></a>Güncelleştirme Sürümü 18

### <a name="bug-fixes"></a>Hata düzeltmeleri

**Zaman ve Gider**

- Düzeltildi: **Geri Çek**, **İste** ve **Onayı İptal Et** akışları anlaşılamaz hata iletileriyle özel durumlar oluşturur.
- Düzeltildi: **Onayı İptal Et** bir gider için başarısız olduğunda ilgili özel durum hatası oluşturulmaz.
- Düzeltildi: Zaman Girişi ızgarası, Avustralya'da Ekim ayında günışığından tasarrufa (DST) geçişten sonra iş günü olmayan günleri yanlış şekilde işler.
- Düzeltildi: Yanlış varsayılan mantığı, giderlerin gönderilmesini engeller.
- Düzeltildi: Zaman girişi onayı başarısız olduğunda onay **Beklemede** durumunda kalır.
- Düzeltildi: Toplu onaylardaki SQL Hataları (kilitlenme/zaman aşımı).
- Düzeltildi: Zaman girdilerini onaylarken takım üyelerini güncelleştirmeden kaynaklanan kullanıcı deneyiminde önemli performans sorunları.

**Proje Yönetimi**

- Düzeltildi: Saat dilimi bildirimi, **Mutabakat** görünümünden **Proje** ana formuna taşındı.
- Düzeltildi: Takvim şablonu, yeni bir proje formu açıldığında doğru şekilde varsayılan hale gelmiyor.
- Düzeltildi: Chromium tabanlı tarayıcılar için kullanıcılar, silinecek öncül görevleri kolay şekilde seçemiyor.
- Düzeltildi: **Boş Şablondan Proje** oluşturmak veya kopyalamak, ilişkisiz atamalar getirir.
- Düzeltildi: Özel uç durumlarda görev kılavuzundan yeni atama oluşturmak, oluşturulan kayıtların yinelenmesiyle sonuçlanır.
- Düzeltildi: El ile modunda kullanıcılar, görevin başlangıç tarihlerini geçerli kayıt tarihinden sonra olacak şekilde güncelleştiremez.

**Kaynak Yönetimi**

- Düzeltildi: **Mutabakat** görünümü alt toplam satırı, ayırmaları uzattıktan sonra ayırma farkını yanlış şekilde hesaplar.
- Düzeltildi: **Mutabakat** görünümü, ayrılabilir kaynak proje takvimiyle eşleşmeyen bir takvime sahip olduğunda kaynak atamalarını yanlış şekilde görüntüler.

**Sales**

- Düzeltildi: Zaman girişleri yeniden onaylandığında (**Onayla > İptal Et >** yeniden onayla) yinelenen bir borçlandırılamaz gerçek değer oluşturulur.
