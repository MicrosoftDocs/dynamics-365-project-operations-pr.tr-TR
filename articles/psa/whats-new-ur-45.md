---
title: Project Service Automation Güncelleştirme Sürümü 45, V3'teki yenilikler veya değişiklikler
description: Bu makalede, Microsoft Dynamics 365 Project Service Automation Güncelleştirme Sürümü 45, V3'de bulunan özellikler ve düzeltmeler listelenmektedir.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/14/2022
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
ms.openlocfilehash: 98f7c973917d7d6334e6e0aeb15214c538b33143
ms.sourcegitcommit: 36fda4f45ddeb0f81d30bd1e22852727df644754
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169169"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-45-v3"></a>Project Service Automation Güncelleştirme Sürümü 45, V3'teki yenilikler veya değişiklikler

[!include [banner](../includes/psa-now-project-operations.md)]

Microsoft Dynamics 365 Project Service Automation uygulaması için en yeni güncelleştirmeyi sunmaktan mutluluk duyarız. Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir. Dynamics 365 9.x ile uyumludur. Bu sürüme güncelleştirmek için Dynamics 365 çevrimiçi çözümler sayfasının için Yönetici Merkezi sayfasını ziyaret edin ve güncelleştirmeyi kurun. Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.

Bu makalede, Project Service Automation Güncelleştirme Sürümü 45, V3'de yeni ve değiştirilen özellikler ve düzeltmeler listelenmektedir. Bu sürüm V3.10.76.168 derleme numarasına sahiptir ve genellikle Temmuz 2022'de bir kendi kendine güncelleştirme yoluyla kullanılabilir.

## <a name="update-release-45"></a>Güncelleştirme Sürümü 45

### <a name="bug-fixes"></a>Hata düzeltmeleri

Aşağıdaki sorunlar giderilmiştir.

**Satışlar**

- Kullanıcılar aynı zamanda sayfanın aynı örneğini görüntülediklerinden ve yenilemediği bir fatura oluşturmak için, faturalandıktan sonra faturaları başarıyla fatura oluşturmazlar.

**Zaman ve Gider**

- Modern Onaylar etkinleştirildiğinde ve geri çekilmiş bir proje onayı onaylandığında, kayıt aşaması **Onaylandı İsteğini Geri Çek** şeklinde yanlış olarak güncelleştirilir.
- Modern onaylar etkinleştirildiğinde ve Bulut Akışları etkin olmadığında, onaylama işlemi başarılı olmaz ve kullanıcılara gönderim veya onaylamanın uyarılmaz.
