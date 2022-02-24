---
title: Project Service Automation Güncelleştirme Sürümü 30, V3'teki yenilikler veya değişiklikler
description: Bu konuda, Project Service Automation, Güncelleştirme Sürümü 30, V3'teki özellikler ve düzeltmeler listelenir.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 1169ee13c42e982cb30a40d92df660f8933786a9
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852903"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a>Project Service Automation Güncelleştirme Sürümü 30, V3'teki yenilikler veya değişiklikler

[!include [banner](../includes/psa-now-project-operations.md)]

Dynamics 365 için Project Service Automation uygulamasına yönelik en son güncelleştirmeyi duyurmaktan mutluluk duyuyoruz. Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir. Bu sürüm Dynamics 365 9.x ile uyumludur. Bu sürüme güncelleştirmek için Dynamics 365 online çözümler sayfası için Yönetim Merkezi'ni ziyaret edin ve güncelleştirmeyi yükleyin. Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.

Bu konuda, Project Service Automation Güncelleştirme Sürümü 30 V3'te yeni veya değiştirilmiş özellikler ve düzeltmeler listelenmektedir. Bu sürüm, V3.10.51.61 derleme numarasına sahiptir ve Nisan 2021'de kendi başına güncelleştirme olarak genel kullanıma sunulmuştur.

## <a name="update-release-30"></a>Güncelleştirme Sürümü 30

### <a name="bug-fixes"></a>Hata düzeltmeleri

**Zaman ve Gider**

Aşağıdaki sorunlar giderilmiştir:

- **Rol** alanı kaldırılmışsa **Hızlı Oluştur** sayfasında bir zaman girişi oluşturulup kaydedildiğinde bir hata oluşur.
- Zaman Girişi filtresi, yanlış filtre işlecini uygular.
- Zaman girişi denetiminde **Haftayı Kopyala** seçeneğini belirlediğinizde, kopyalanan zaman çizelgeleri otomatik olarak görüntülenmiyor.

**Kaynak Yönetimi**

Aşağıdaki sorunlar giderilmiştir:

- Bir ayırmayı genişlettiğinizde, sabit duruma göre atanan ayırma durumu yanlış oluyor. Bir ayırma genişletildiğinde, ayırma kurulumu meta verilerinde **Taahhüt edilen** olarak tanımlanan ayırma durumu geçerli sayılır.
- Geçerli bir kayıt durumu belirtilmediğinde, hata iletisi doğru olarak yerelleştirilmez.

**Proje Yönetimi**

Aşağıdaki sorunlar giderilmiştir:

- Tek bir para biriminde oluşturulan projelerde, ilgili görevlerde başka bir para birimi dahil edilemez.

**Satışlar**

Aşağıdaki sorunlar giderilmiştir:

- Bir fiyat listesi kopyalandığında, fiyatlar güncelleştirilmiyor.
- Maliyet ayrıntısı kaynak için bir değere sahip olduğunda, teklif kazanıldı olarak işaretlenip kapatılamaz.
- **Proje Görevi** varlığındaki **Tahmini Maliyet**, **Planlanan Maliyet (Baz)** olarak yeniden adlandırılmıştır.
- Faturalar oluşturulduğunda veya silindiğinde bir null başvuru özel durumu üretiliyor.
