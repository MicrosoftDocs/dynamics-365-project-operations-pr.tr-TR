---
title: Project Service Automation Güncelleştirme Sürümü 22, V3'teki yenilikler veya değişiklikler
description: Bu konuda, Project Service Automation, Güncelleştirme Sürümü 22, V3'teki özellikler ve düzeltmeler listelenir.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: 8863d321ad88d761d0fcbd82ca26562a69468f2f
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949028"
---
# <a name="project-service-automation-update-release-22-v3"></a>Project Service Automation, Güncelleştirme Sürümü 22, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Dynamics 365 için Project Service Automation uygulamasına yönelik en son güncelleştirmeyi duyurmaktan mutluluk duyuyoruz. Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir. Bu sürüm Dynamics 365 9.x ile uyumludur. Bu sürüme güncelleştirmek için Dynamics 365 online çözümler sayfası için Yönetim Merkezi'ni ziyaret edin ve güncelleştirmeyi yükleyin. Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.

Bu konuda, Project Service Automation Güncelleştirme Sürümü 22 V3'te yeni veya değiştirilmiş özellikler ve düzeltmeler listelenmektedir. Bu sürüm, V 3.10.33.48 derleme numarasına sahiptir ve Haziran 2020'de kendi başına güncelleştirme olarak genel kullanıma sunulmuştur.

## <a name="update-release-22"></a>Güncelleştirme Sürümü 22

### <a name="bug-fixes"></a>Hata düzeltmeleri



**Zaman ve Gider**

Aşağıdaki sorunlar giderilmiştir:

- Alma işleminden sonra, zaman girişleri **zaman girişleri** zamanlamasında otomatik olarak eklenmez.
- **Zaman girişi** kılavuz tarih seçicisi bir kullanıcının bölgesel ayarlarını tanımaz.

**Kaynak Yönetimi**

Aşağıdaki sorunlar giderilmiştir:

- El ile modunda, **kaynak gereksinimleri** üretilirken **kaynak atama** dağılımlarında yapılan değişiklikler tanınmaz.
- **Kaynak Istekleri**, özel istek durumlarını desteklemez.

**Proje Yönetimi**

Aşağıdaki sorunlar giderilmiştir:

- EstimateGridControl'de çift tıklama kullanmak Felemenkçe biçimindeki numaraları doğru olarak ayrıştırmaz.
- Atamalar Microsoft Project masaüstü istemcisi eklentisi kullanılarak değiştirildiğinde atanan saatler doğru şekilde güncelleştirilmez.
- Proje izleme ve tahminler ızgaraları, sözleşme para birimi müşteri para biriminden farklı olduğunda ve kuruluş para birimi sembolleri yerine para birimi kodlarını görüntülemek için yapılandırıldığı zaman, yanlış satış para birimi kodu görüntüler.
- Çalışma saati zamanlaması günde 24 saat ise, bir takım üyesinin bitiş tarihi bir gün ekler.
- Proje zamanlamasında, göreve bir hareket kategorisi eklemek otomatik kaydetmeyi tetiklemez.
- Proje şablonuna takım üyesi eklerken aşağıdaki hata görüntülenir: "kaynak gereksinimleri proje şablonlarıyla ilişkilendirilemez". 
- Şerit kuralı komut dosyası "msdyn.Approval.CanApproveOrReject" bir zaman aşımı hatası görüntüler.

**Sales**

Aşağıdaki sorunlar giderilmiştir:

- 'Yeni teklif proje fiyatı listesi' formunda/varlığında fiyat listesi aramasında bir maliyet fiyatı listesi seçildiğinde doğrulama hata iletisi görüntülenmez.
- Teklife iliştirilen bir BPF son aşamada ise, teklif Kazanıldı olarak kapatıldığında oluşturulan sözleşmeye gitmez.
- Bir zaman girişi geri alınırken **Faturalandıralınmamış satışların** ters işlemi özgün maliyete bağlıdır.
- **Onay** düğmesini seçtikten sonra Fatura yenilenene kadar fatura durumu **Onaylandı** olarak değişmez.


[!INCLUDE[footer-include](../includes/footer-banner.md)]