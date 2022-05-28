---
title: Project Service Automation Güncelleştirme Sürümü 38, V3'teki yenilikler veya değişiklikler
description: Bu konu, Microsoft Dynamics 365 Project Service Automation Güncelleştirme Sürümü 38, V3'tebulunan özellikleri ve düzeltmeleri listeler.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 12/06/2021
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
ms.openlocfilehash: 16994535d57dc1d7fefbe6e892c154f52638c7c0
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598742"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Project Service Automation Güncelleştirme Sürümü 38, V3'teki yenilikler veya değişiklikler

[!include [banner](../includes/psa-now-project-operations.md)]

Microsoft Dynamics 365 Project Service Automation uygulaması için en yeni güncelleştirmeyi sunmaktan mutluluk duyarız. Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir. Dynamics 365 9.x ile uyumludur. Bu sürüme güncelleştirmek için Dynamics 365 çevrimiçi çözümler sayfasının için Yönetici Merkezi sayfasını ziyaret edin ve güncelleştirmeyi kurun. Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.

Bu konuda, Project Service Automation Güncelleştirme Sürümü 38 V3'te yeni veya değiştirilmiş özellikler ve düzeltmeler listelenmektedir. Bu sürümün derleme numarası V3.10.59.117'dur ve genellikle Aralık 2021'de kendi kendini güncelleştirme aracılığıyla kullanılabilir.

## <a name="update-release-38"></a>Güncelleştirme Sürümü 38

### <a name="bug-fixes"></a>Hata düzeltmeleri

Aşağıdaki sorunlar giderilmiştir.

**Zaman ve Gider**

- Onay kümesi günlüklerinin uzunluğu 100.000 kaydı aştığında bir özel durum oluşur.
- Kullanıcılar **Zaman Girişi** ana sayfasından **Zaman Girişi** kılavuzuna erişemez.
- **İçeri Aktarma Saati** giriş iletişim kutusunda, hiçbir öğe içe aktarmaya uygun olmadığında herhangi bir metin gösterilmez.
- Kullanıcılar, **Hedef Durum** alanının **Bilinmiyor** olarak ayarlandığı onay kümeleri oluşturabilir.

**Proje Yönetimi**

- Gün ışığından yararlanma saati başladığında UTC (+09:30) ve UTC (+10:00) için kaynak atamalarında konturlar doğru gösterilmez.
- İş kırılım yapıları için **Ek Sütun** alanı bazı yerel yönetimlerde gizlidir.
- **Proje Görevi** kılavuzundaki takvim denetiminin tarih seçicisi Çince için doğru yerelleştirilmemiş.

**Satışlar**

- Farklı sözleşme birimlerine ve para birimlerine sahip rezerve edilebilir kaynaklar zaman girişleri gönderdiğinde **Sözleşme Performansı** ve **Proje Fiili Maliyeti** değerleri eşleşmez.
- Faturalar yönetilen bir çözüm olarak alındığında faturaları otomatik olarak onaylamak için özel bir iş akışı başarısız olur. Aşağıdaki ileti gösterilir: "Microsoft.Xrm.Sdk.InvalidPluginExecutionException Message: Geçersiz fatura durumu."
- Özetleme seçeneği olarak **Kök** seçildiğinde ve proje, hareket sınıflarının bir karışımından (örneğin, zaman, gider ve malzeme tahminlerinin birleşimi) oluşan tahminlere sahip olduğunda, sistem hareket sınıfları arasında tek bir ücret satırı olarak özetler.
- Sözleşme satırı bir projeyle ilişkilendirilmeden önce gider satırının eklendiği senaryolarda, **Fiyatı Güncelleştir** alanına varsayılan değer olarak doğru fiyatlandırma girilmiyor.
- **Proje** ve **Görev** varlıklarında negatif satış tutarlarına izin verilmez.
