---
title: Project Service Automation Güncelleştirme Sürümü 15, V3'teki yenilikler veya değişiklikler
description: Bu konu Project Service Automation Güncelleştirme Sürüm 15, V3'teki yenilikler hakkında bilgi sağlar.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.openlocfilehash: 6112e4874025e528a2bb583cf215fd9eff681534
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086281"
---
# <a name="project-service-automation-update-release-15-v3"></a>Project Service Automation, Güncelleştirme Sürümü 15, V3

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
