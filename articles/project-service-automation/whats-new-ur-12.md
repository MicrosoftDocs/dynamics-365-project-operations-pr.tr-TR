---
title: Project Service Automation Güncelleştirme Sürümü 12, V3'teki yenilikler
description: Bu konu Project Service Automation Güncelleştirme Sürüm 12, V3'teki yenilikler hakkında bilgi sağlar.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: af8dbfe3-7ce9-4374-9c03-17b2e1d6ac32
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 758717562c12a72848f1a874fa8b1171139ebb0c
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756636"
---
# <a name="project-service-automation-v3-update-release-12"></a>Project Service Automation V3, Güncelleştirme Sürümü 12
Dynamics 365 Project Service Automation (PSA) uygulaması için en son güncelleştirmeyi duyurmaktan mutluluk duyuyoruz. Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir. Bu sürüm Dynamics 365 9.x ile uyumludur. Bu sürüme güncelleştirmek için Dynamics 365 (online) için Yönetim Merkezi'ni ziyaret edin ve güncelleştirmeyi yüklemek için çözümler sayfasına gidin. Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.

Bu konuda, Project Service Automation V3, Güncelleştirme Sürümü 12'de yeni veya değiştirilmiş özellikler ve düzeltmeler listelenir. Bu sürüm, V3.10.2.34 derleme numarasına sahiptir ve Ekim 2019 tarihinde kendi kendine güncelleştirme ile genel kullanıma sunulmuştur.

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