---
title: Project Service Automation Güncelleştirme Sürümü 25, V3'teki yenilikler veya değişiklikler
description: Bu makalede, Project Service Automation Güncelleştirme Sürümü 25, V3'de bulunan özellikler ve düzeltmeler listelenmektedir.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: 2330c7dc5d2dfb148d5c7fb9a5ce643fded84dde
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922568"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a>Project Service Automation Güncelleştirme Sürümü 25, V3'teki yenilikler veya değişiklikler

[!include [banner](../includes/psa-now-project-operations.md)]

Dynamics 365 için Project Service Automation uygulamasına yönelik en son güncelleştirmeyi duyurmaktan mutluluk duyuyoruz. Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir. Bu sürüm Dynamics 365 9.x ile uyumludur. Bu sürüme güncelleştirmek için Dynamics 365 online çözümler sayfası için Yönetim Merkezi'ni ziyaret edin ve güncelleştirmeyi yükleyin. Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.

Bu makalede, Project Service Automation V3, Güncelleştirme Sürümü 25 için yeni veya değiştirilen özellikler ve düzeltmeler yer alır. Bu sürümün derleme numarası V3.10.43.76'dır ve genellikle Ekim 2020'de otomatik güncelleştirme olarak mevcuttur.

## <a name="update-release-25"></a>Güncelleştirme Sürümü 25

### <a name="bug-fixes"></a>Hata düzeltmeleri

**Zaman ve Gider**

Aşağıdaki sorun düzeltildi:

- Zaman girişi grafiği çok büyük bir aralığa dayalı olarak daha fazla veri gösteriyor.

**Kaynak Yönetimi**

Aşağıdaki sorun düzeltildi:

- Daha yüksek bir sürüm düzeltme eki zaten varsa, Universal Resource Scheduling düzeltme eki alma işlemini atlamak için paket dağıtıcı kodu eklenmiştir.

**Proje Yönetimi**

Aşağıdaki sorunlar giderilmiştir:

- Düzeltilen yuvarlama ve Döviz Kuru tutarsızlıkları proje izleme ızgarasında yanlış planlanmış maliyete neden olur.
- **Proje** formunda iki veya daha fazla yanıt alan gösterimi görüntüleme yeteneğini destekler.
- Takvim bitiş tarihinden sonra görev atama yeteneğini ele almak için doğrulama sağlandı, bu da başarısız bir kaynak atamasına neden olacak.
- Aşağıdaki hatadan dolayı boş başvuru özel durumuna adres olarak geliştirilmiş hata işleme durumu üretildi:

    - **PreValidateProjectTeamMemberCreate** eklentisi
    - **PreValidateProjectTaskCreate**, ilişkilendirilen bir proje olmadan bir proje görevi oluşturulduğunda
    - **PreProjectTeamMemberCreate** eklentisi
    - **PostProjectTeamMemberDelete** eklentisi
    - **PreValidateProjectTaskDelete** eklentisi

**Sales**

Aşağıdaki sorunlar giderilmiştir:

- **Kopyalama Projesi: Yardımcı Kaynağı Yönetimini Tahmin Eder**'den oluşturulan boş başvuru özel durumlarına yönelik olarak geliştirilmiş hata işleme
- **Zaman ve Malzeme Faturalama Biriktirme listesi** üzerinde **faturalamaya hazır değil** fatura durumunu temizlemez.
- **Rol fiyatı** ve **Katalog öğeleri** sekmesindeki yanlış etiketli **fiyatlar** düğmeleri düzeltildi.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
