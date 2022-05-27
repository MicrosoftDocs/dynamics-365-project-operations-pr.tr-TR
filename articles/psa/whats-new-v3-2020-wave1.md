---
title: Project Service Automation sürüm 3.x dalga 1 2020'deki yenilikler veya değişiklikler
description: Bu konu Project Service Automation sürüm 3 dalga 1 2020'deki yenilikler veya değişiklikler hakkında bilgi sağlar.
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
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
ms.openlocfilehash: 073b70b4ae02d943eb0794b51e888815ee16f438
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577904"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Project Service Automation sürüm 3 dalga 1 2020'deki yenilikler veya değişiklikler

[!include [banner](../includes/psa-now-project-operations.md)]

Bu konuda Project Service Automation (PSA) sürüm 3.x dalga 1 2020'nin son sürümüne geçerken dikkat edilmesi gereken önemli yükseltme konuları vurgulanmaktadır.

## <a name="time-entry"></a>Zaman girişi
Zaman girişi deneyimi, zaman girişini daha fazla müşteri senaryosuna dağıtma yetenekleri sağlayacak şekilde uzatılmıştır. Bu giriş türleri ekleme yeteneğini de kapsar. Bu da **Zaman Kaynağı** olarak görüntülenen **Zaman Girişi Ayarları** alan şeması adına göre belirli davranışları destekler. Bu işlevi desteklemek için Zaman, Gider, Durum ve Onaylar (TESA) adında yeni bir çözüm eklenmiştir.

### <a name="upgrade-consideration"></a>Yükseltmeyle ilgili önemli bir nokta
Bu işlevselliği desteklemek için PSA içindeki roller yeni ayrıcalıklar içerecek şekilde güncelleştirilmiştir. Bu ayrıcalıklar yeni **Zaman Girişi Ayarları** varlığına okuma erişimi verir.

Zaman günlüğü tutma özelliğine gereksinim duyan kullanıcılara var olan rollere ek olarak **Zaman Girişi Kullanıcısı** kullanıcı rolü de verilmelidir. Bu rol yeni işlevler içerir ve zaman girişinin çalışmaya devam etmesini sağlar.

Ayrıca, zaman girişi varlığı için tüm formları içeren herhangi bir özel uygulama modülünüz varsa, **TESA zaman girişi Hızlı Oluştur Formu**'nu modülden kaldırmanız gerekir.

### <a name="currently-extended-time-entry-changes"></a>Şu anda uzatılmış zaman girişi değişiklikleri
Zaman girişinin geçerli kullanıcılar üzerindeki etkisini en aza indirmek amacıyla, bu rol değişikliği zaman girişinden yararlanmaya devam etmek için gereken tek temel gereksinimdir. Özel görünümler veya ayrı zaman girişi deneyimleri oluşturduysanız, **Zaman Girişi Ayarı** alanlarını doğru PSA değerine ayarlamanız gerekir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
