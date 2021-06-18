---
title: Project Service Automation Güncelleştirme Sürümü 24, V3'teki yenilikler veya değişiklikler
description: Bu konuda, Project Service Automation, Güncelleştirme Sürümü 24, V3'teki özellikler ve düzeltmeler listelenir.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
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
ms.openlocfilehash: c95a9dcada4fbf6c462df29d450aaafab4e73aa5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000280"
---
# <a name="project-service-automation-update-release-24-v3"></a>Project Service Automation, Güncelleştirme Sürümü 24, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Dynamics 365 için Project Service Automation uygulamasına yönelik en son güncelleştirmeyi duyurmaktan mutluluk duyuyoruz. Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir. Bu sürüm Dynamics 365 9.x ile uyumludur. Bu sürüme güncelleştirmek için Dynamics 365 online çözümler sayfası için Yönetim Merkezi'ni ziyaret edin ve güncelleştirmeyi yükleyin. Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.

Bu konuda, Project Service Automation Güncelleştirme Sürümü 24 V3'te yeni veya değiştirilmiş özellikler ve düzeltmeler listelenmektedir. Bu sürüm, V 3.10.42.43 derleme numarasına sahiptir ve Ekim 2020 tarihinde kendi kendine güncelleştirme ile genel kullanıma sunulmuştur.

## <a name="update-release-24"></a>Güncelleştirme Sürümü 24

### <a name="bug-fixes"></a>Hata düzeltmeleri

**Sales**

Aşağıdaki sorunlar giderilmiştir:

- Ürünlerin varsayılan fiyat listesini ayarlarken sorun oluşuyor.
- Eklenmiş fiyat listesi ve rol fiyatı kayıtları kopyası nedeniyle Teklif Performansı kazancı yavaştır.
- **Proje Sözleşmesi/Satış Merkezi** > **Ürün Kalemi/Sipariş Satırı Miktarı** otomatik olarak en yakın tamsayıya yuvarlanır.
- Fiyat listelerini okurken sistem ayrıcalıklarına yükseltin.
- **address1_freighttermscode** ve **address1_shippingmethodcode** müşteri adresi alanlarını Teklif/Sipariş'e kopyalayın. 


**Zaman ve Gider**

Aşağıdaki sorunlar giderilmiştir:

- **Zaman Girişi Izgarası**, **Yalnızca Tarih** zaman davranışını desteklemez.
- **Zaman Girişi** otomatik olarak yenilenmiyor. El ile yenileme gerekiyor.
- Bir kaynağın atamalarında mola (0 saat) olduğunda atamadan zaman girişleri içeri aktarılamıyor.
- Bir zaman girişi oluştururken başlangıcı **msdyn_date** ile aynı olarak ayarlayın.
- Zaman girişi için toplu düzenlemeyi yeniden etkinleştirin.

**Kaynak Yönetimi**

Aşağıdaki sorunlar giderilmiştir:

- Gereksinim olmadan günler arası ayırma durumunu güncelleştirmeyi denemek, null başvuru özel durumu oluşturur.
- **Mutabakat Görünümü** yüklenirken hata oluşuyor.


**Proje Yönetimi**

Aşağıdaki sorunlar giderilmiştir:

- **Proje Zamanlaması**'nda, **El İle** seçeneğini **Otomatik** olarak değiştirirken otomatik kaydetme tamamlanmıyor.
- Gider maliyetleri, **Proje İzleme Izgarası**'nddaki fark üzerinden hesaplanmamalıdır.
- Yükleme sırasında **Tahminler etiketi** sütunları ile **Zaman Aşaması** türünü değiştirme arasında tutarsız davranış.
- Projedeki gerçek maliyet, **Gerçek Değerler** toplamlarını yansıtmayabilir.
- **Özet** sekmesindeki **Tahmini Bitiş Tarihi**, **İKY Zamanlaması** ile eşleşmiyor.
- Çıkıntıdaki **Gerçek Saatleri Güncelleştir** seçeneği doğru çalışmıyor.
- **BU** kökünün dışındaki bir proje yöneticisi proje oluşturamıyor.
- **Gider Tahminleri**'nde görev veya kategori değişiklikleri kalıcı olmuyor.
- **Sözleşmenin kopyası**, fatura zamanlamasını ve çalıştırma durumunu kopyalıyor.
- **Gerçek Değerleri Yenile** düğmesi, özet görevleri düzgün hesaplamıyor.
- Microsoft Project Eklentisi: Bir takım üyesi boş bir kaynak belirleme birimine sahipse null başvuru hatasını düzeltir.



[!INCLUDE[footer-include](../includes/footer-banner.md)]