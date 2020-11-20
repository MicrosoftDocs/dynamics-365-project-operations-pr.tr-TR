---
title: Project Service Automation Güncelleştirme Sürümü 25, V3'teki yenilikler veya değişiklikler
description: Bu konuda, Project Service Automation, Güncelleştirme Sürümü 25, V3'teki özellikler ve düzeltmeler listelenir.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: a5a81893c4a804deb09cf33e0ac3f1a25b8bca36
ms.sourcegitcommit: a2b810219d381716d3eedb14c4eb6cdefb5b5845
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/02/2020
ms.locfileid: "4183567"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a>Project Service Automation Güncelleştirme Sürümü 25, V3'teki yenilikler veya değişiklikler

Dynamics 365 için Project Service Automation uygulamasına yönelik en son güncelleştirmeyi duyurmaktan mutluluk duyuyoruz. Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir. Bu sürüm Dynamics 365 9.x ile uyumludur. Bu sürüme güncelleştirmek için Dynamics 365 online çözümler sayfası için Yönetim Merkezi'ni ziyaret edin ve güncelleştirmeyi yükleyin. Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.

Bu konu, yeni olan veya Project Service Automation V3 için değiştirilen özellikleri ve onarımları, güncelleştirme sürüm 25'i listelemektedir. Bu sürümde sürüm numarası V 3.10.43.76 şeklindedir ve genellikle 2020 ekim'de kendi kendini güncelleştirme aracılığıyla kullanılabilir.

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