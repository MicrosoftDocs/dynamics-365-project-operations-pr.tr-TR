---
title: Project Service Automation Güncelleştirme Sürümü 19, V3'teki yenilikler veya değişiklikler
description: Bu konuda, Project Service Automation, Güncelleştirme Sürümü 19, V3'teki özellikler ve düzeltmeler listelenir.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: b9baeca9e79e233c25a6310e426d755b9162bbad
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280737"
---
# <a name="project-service-automation-update-release-19-v3"></a>Project Service Automation, Güncelleştirme Sürümü 19, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Dynamics 365 için Project Service Automation uygulamasına yönelik en son güncelleştirmeyi duyurmaktan mutluluk duyuyoruz. Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir. Bu sürüm Dynamics 365 9.x ile uyumludur. Bu sürüme güncelleştirmek için Dynamics 365 online çözümler sayfası için Yönetim Merkezi'ni ziyaret edin ve güncelleştirmeyi yükleyin. Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.

Bu konuda, PSA V3, Güncelleştirme Sürümü 19'te yeni veya değiştirilmiş özellikler ve düzeltmeler listelenir. Bu sürüm, V3.10.30.41 derleme numarasına sahiptir ve Mayıs 2020'de kendi başına güncelleştirme olarak genel kullanıma sunulmuştur.

## <a name="update-release-19"></a>Güncelleştirme Sürümü 19

### <a name="bug-fixes"></a>Hata düzeltmeleri

**Zaman ve Gider**

Aşağıdaki sorunlar giderilmiştir: 

- Zaman girişi içeri aktarma işlemlerinden kaynaklanan hatalar doğru şekilde görüntülenmiyor.
- Zaman Girişi Kılavuzu **Yalnızca Tarih** alanı davranışını desteklemez.
- Proje Kaynakları projeyle bir gider oluşturamıyor.

**Proje Yönetimi**

Aşağıdaki sorunlar giderilmiştir: 

-  En alt görev Tamamlama Hesaplaması (EAC) sırasında yanlış çalışma tahmini oluşturulmasına neden oluyor.

**Sales**

Aşağıdaki sorunlar giderilmiştir: 

- **Yeniden hesapla** eylemi gider sözleşme satırı ayrıntıları veya teklif satırı ayrıntıları ile çalışmaz.
- **Masrafları Güncelleştir** gider tahminlerde eksik.
-  Müşteriler **Proje Sözleşmesi** sayfasından özel sözleşme durumunu seçemiyor.
- Bir tekliften özel bir fiyat listesi oluştururken, müşterilerin performansta bozulmayla karşılaşıyor.
- Müşteriler **Teklif Satırı Ayrıntıları** ve **Sözleşme Satırı Ayrıntıları** sayfalarında **birim** varsayılanlarıyla ilgili tutarsızlık yaşıyor.
- Borçlandırılabilir sözleşme satırına borçlandırılamayan işlem kategorisi eklemek, işlem kategorisinin **Borçlandırılamaz** faturalama türünü dikkate almaz.
- Müşteriler önceden oluşturulan sözleşmelere yeni eklenen rolleri ve kategoriyi kullanamaz.
- Müşteriler PreValidateProjectTeamMemberUpdate.cs öğesinde Gereksiz alma konusunda performansta bozulmayla karşılaşıyor
- **Kaynak Kategoriler** listesinde borçlandırılamaz olarak ayarlanan rollerin, birprojenin sözleşme satırında **Borçlandırılabilir Roller** sekmesine **Borçlandırılamaz** olarak eklenmesi gerekir.
- **GetBookableResourceIdFromUser** yalnızca birincil kimlik yerine ayrılabilir kaynaklara ait tüm sütunları aldığından müşteriler proje oluştururken performans sorunlarıyla karşılaşabilir.
- **TransactionType** varlığında, kullanıcıların işlem türleri için geçerli olmayan **Birimler** ve **UnitGroups** girmesini önlemek için ön doğrulama güncelleştirmesi eklentisi yoktur.
- **Kaldır** adımı, zaman girişi içeri aktarma için kullanılamaz.


[!INCLUDE[footer-include](../includes/footer-banner.md)]