---
title: Project Service Automation Güncelleştirme Sürümü 12, V3'teki yenilikler veya değişiklikler
description: Bu konu Project Service Automation Güncelleştirme Sürüm 12, V3'teki yenilikler hakkında bilgi sağlar.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: 58a12ded135712d8194499ce4a9ba9e4e2aa99bd
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949523"
---
# <a name="project-service-automation-update-release-12-v3"></a>Project Service Automation, Güncelleştirme Sürümü 12, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Dynamics 365 Project Service Automation (PSA) uygulaması için en son güncelleştirmeyi duyurmaktan mutluluk duyuyoruz. Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir. Bu sürüm Dynamics 365 9.x ile uyumludur. Bu sürüme güncelleştirmek için Dynamics 365 (online) için Yönetim Merkezi'ni ziyaret edin ve güncelleştirmeyi yüklemek için çözümler sayfasına gidin. Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.

Bu konuda, Project Service Automation Güncelleştirme Sürümü 12 V3'te yeni veya değiştirilmiş özellikler ve düzeltmeler listelenmektedir. Bu sürüm, V3.10.2.34 derleme numarasına sahiptir ve Ekim 2019 tarihinde kendi kendine güncelleştirme ile genel kullanıma sunulmuştur.

## <a name="update-release-12"></a>Güncelleştirme Sürümü 12

### <a name="bug-fixes"></a>Hata düzeltmeleri

- Zaman ve Gider

    - Düzeltildi: Zaman girişi hatası iletileri daha ilgili içerikle güncelleştirildi.
    - Düzeltildi: Zaman girişi ızgarası ve zamanlama, gerektiğinde doğru şekilde dikey kaydırma çubuğunu görüntülüyor.
    - Düzeltildi: Gönderilen gider veya zaman girişleri onaylanabilir.
    - Düzeltildi: Onay onayını iptal et iletişim kutusu iletisi **Onaylandı** olan durum **Gönderildi** olarak değiştirildiğinde, onayın durumunu yansıtacak şekilde düzeltildi.
    - Düzeltildi: **Fiyat**, **Birim** ve **Miktar** alanları artık, onaylandıktan sonra Gider kaydına kilitleniyor.

- Proje Yönetimi

    - Düzeltildi: **Takım üyesi** ana formundaki **Yeni** eylemi kaldırıldı.
    - Düzeltildi. Kaynak atamaları görevin bitiş tarihinde kaymaya neden olan yanlış yuvarlama hatalarını dikkate alacak şekilde güncelleştirildi.
    - Düzeltildi: Görev ızgarasında, ilgili sunucu tarafı hataları kullanıcıya sunulacak.
    - Düzeltildi: Takım üyesinin adı artık konum adı yerine görev kişi seçicisinde işleniyor.

- Kaynak Yönetimi

    - Düzeltildi: Şablondan oluşturulan projeler için kaynak gereksinimi ayrıntıları artık proje takvimini kullanıyor.
    - Düzeltildi: Artık beceriler ve yetenekler varsayılan olarak ana verilerden bu rol için oluşturulmuş kaynak gereksinimine ayarlanır.

- Sales

    - Düzeltildi: **Sözleşme ana** formunda bulunan yinelenen nesne kimlikleri.
    - Düzeltildi: Mantık, sekmenin meta veri kurulumunu görüntüleyebilmesi için **Teklif Analizi** sekmesini görünür yapacak şekilde güncelleştirildi.
    - Düzeltildi: Gerçek kayıttaki muhasebe tarihi artık onay tarihinden değil, zaman/gider giriş tarihinden alınıyor.


[!INCLUDE[footer-include](../includes/footer-banner.md)]