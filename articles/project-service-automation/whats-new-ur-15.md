---
title: Project Service Automation Güncelleştirme Sürümü 15, V3'teki yenilikler
description: Bu konu Project Service Automation Güncelleştirme Sürüm 15, V3'teki yenilikler hakkında bilgi sağlar.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: 75117934-8042-448b-91dc-b43f1f677e4f
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 68e0faa4c1afdb0d1520388253671330f9b7d334
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756633"
---
# <a name="project-service-automation-v3-update-release-15"></a>Project Service Automation V3, Güncelleştirme Sürümü 15

Dynamics 365 Project Service Automation (PSA) uygulaması için en son güncelleştirmeyi duyurmaktan mutluluk duyuyoruz. Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir. Bu sürüm Dynamics 365 9.x ile uyumludur. Bu sürüme güncelleştirmek için Dynamics 365 (online) için Yönetim Merkezi'ni ziyaret edin ve güncelleştirmeyi yüklemek için çözümler sayfasına gidin. Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.

Bu konuda, PSA V3, Güncelleştirme Sürümü 15'te yeni veya değiştirilmiş özellikler ve düzeltmeler listelenir. Bu sürüm, V3.10.5.28 derleme numarasına sahiptir ve Ocak 2020 tarihinde kendi kendine güncelleştirme ile genel kullanıma sunulmuştur.

## <a name="update-release-15"></a>Güncelleştirme Sürümü 15 

### <a name="enhancements"></a>Geliştirmeler

- Proje Yönetimi

### <a name="bug-fixes"></a>Hata düzeltmeleri

- Zaman ve Gider

  - Düzeltildi: Mutabakat görünümünde eklenti yükleme hatası işleme.
  - Düzeltildi: Proje Kaynak Merkezi: Belirsizliği azaltmak için **Tutar** olarak yeniden adlandırıldı.
  - Düzeltildi: **Zaman Girişi Sütunlarını Kopyala** görünümü, türü de içerecek şekilde düzenlendi.
  - Düzeltildi: Kılavuz görünümünde zaman girişi süresinin ondalık sayılar kullanarak düzenlenmesi bazı sayılarda bilinmeyen hatalara neden oluyor.

- Proje Yönetimi

  - Düzeltildi: **İzleme Görünümünde Kullan** açılır menüsü artık seçeneklerin genişliğine göre genişliyor.
  - Düzeltildi: Projeler +13 saat diliminde yönetilirken görev hesaplamaları yanlış sonuçlar gösterebilir.
  - Düzeltildi: **Takım Üyesi Bitiş Saati** 24 saatlik takvim seçeneği için düzeltildi.
  - Düzeltildi: **msdyn_project** ana formunda **BPF** yeniden etkinleştirildi.
  - Düzeltildi: Atama hesaplaması artık bir günü yok saymıyor.
  - Düzeltildi: Kullanıcının ve projenin saat diliminin farklı olduğu durumlarda proje formuna yeni bir bildirim başlığı eklendi.

- Sales

  - Düzeltildi: Gider tahmini kategori araması, yinelenen öğeleri filtrelemek için kullanılabilir.
  - Düzeltildi: **PluginDomain.ExecuteInTryCatchBlock(..)** içindeki kod artık özel durumun kaynağını gizlemiyor.
  - Düzeltildi: 1000'den fazla proje olduğunda, **Teklif Satırı** formundaki **Proje arama** hata iletisi artık görünmüyor.
  - Düzeltildi: İşçilik tahminleri ve gider tahminleri için **Tahminler** ızgarası artık doğru para birimi simgesiyle görüntüleniyor.
  - Düzeltildi: Bir kuruluş PSA'yı Güncelleştirme Sürümü 14'ten Güncelleştirme Sürümü 15'e güncelleştirdiğinde, **Zamanlama** sekmesi **Proje** formunda artık boş görünmüyor.
