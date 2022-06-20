---
title: Project Service Automation Güncelleştirme Sürümü 38, V3'teki yenilikler veya değişiklikler
description: Bu makalede, Microsoft Dynamics 365 Project Service Automation Güncelleştirme Sürümü 38, V3'de bulunan özellikler ve düzeltmeler listelenmektedir.
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
ms.openlocfilehash: ccc08cd0bc365bd4761424a4c0ceac91985e7c89
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915209"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Project Service Automation Güncelleştirme Sürümü 38, V3'teki yenilikler veya değişiklikler

[!include [banner](../includes/psa-now-project-operations.md)]

Microsoft Dynamics 365 Project Service Automation uygulaması için en yeni güncelleştirmeyi sunmaktan mutluluk duyarız. Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir. Dynamics 365 9.x ile uyumludur. Bu sürüme güncelleştirmek için Dynamics 365 çevrimiçi çözümler sayfasının için Yönetici Merkezi sayfasını ziyaret edin ve güncelleştirmeyi kurun. Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.

Bu makalede, Project Service Automation Güncelleştirme Sürümü 38, V3'de yeni ve değiştirilen özellikler ve düzeltmeler listelenmektedir. Bu sürümün derleme numarası V3.10.59.117'dur ve genellikle Aralık 2021'de kendi kendini güncelleştirme aracılığıyla kullanılabilir.

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
