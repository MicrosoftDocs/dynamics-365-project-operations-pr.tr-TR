---
title: Project Service Automation Güncelleştirme Sürümü 41, V3'teki yenilikler veya değişiklikler
description: Bu makalede, Microsoft Dynamics 365 Project Service Automation Güncelleştirme Sürümü 41, V3'de bulunan özellikler ve düzeltmeler listelenmektedir.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/07/2022
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
ms.openlocfilehash: 8625ae16e45da30614b3a3eec44193bee0c0b36f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930572"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-41-v3"></a>Project Service Automation Güncelleştirme Sürümü 41, V3'teki yenilikler veya değişiklikler

[!include [banner](../includes/psa-now-project-operations.md)]

Microsoft Dynamics 365 Project Service Automation uygulaması için en yeni güncelleştirmeyi sunmaktan mutluluk duyarız. Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir. Dynamics 365 9.x ile uyumludur. Bu sürüme güncelleştirmek için Dynamics 365 çevrimiçi çözümler sayfasının için Yönetici Merkezi sayfasını ziyaret edin ve güncelleştirmeyi kurun. Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.

Bu makalede, Project Service Automation Güncelleştirme Sürümü 41, V3'de yeni ve değiştirilen özellikler ve düzeltmeler listelenmektedir. Bu sürüm, V3.10.62.162 derleme numarasına sahiptir ve Mart 2022 tarihinde kendi kendine güncelleştirme ile genel kullanıma sunulmuştur.

## <a name="update-release-41"></a>Güncelleştirme Sürümü 41

### <a name="bug-fixes"></a>Hata düzeltmeleri

Aşağıdaki sorunlar giderilmiştir.

**Proje Yönetimi**
- Masaüstü eklentisinden oluşturulan bir projeyi temel alan şablondan bir proje oluşturmaya şu hata görüntülenir: "Kaynak Atamasının Planlanan Çalışma alanı doğrulaması: Her Kaynak Atama Zaman Diliminin Bitiş Tarihi, Başlangıç Tarihinden önce olmamalıdır".

**Zaman ve Gider**
- Bir zaman girişini silmeye çalıştığınızda, şu hata iletisi görüntülenir: "ISV kodundan beklenmeyen bir hata oluşuyor".

**Satışlar**
- Sabit fiyatlı kilometre taşına yönelik bir fatura oluşturduğunuzda, **Açıklama** ve **Harici Açıklama** alanları doldurulmaz. 