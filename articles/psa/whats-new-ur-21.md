---
title: Project Service Automation Güncelleştirme Sürümü 21, V3'teki yenilikler veya değişiklikler
description: Bu konuda, Project Service Automation, Güncelleştirme Sürümü 21, V3'teki özellikler ve düzeltmeler listelenir.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: e7bf9d5c85d2fab0d17c435bdd96057c0c80be8f41b16f94afe6b1f554e7a9fe
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6984761"
---
# <a name="project-service-automation-update-release-21-v3"></a>Project Service Automation, Güncelleştirme Sürümü 21, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Dynamics 365 için Project Service Automation uygulamasına yönelik en son güncelleştirmeyi duyurmaktan mutluluk duyuyoruz. Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir. Bu sürüm Dynamics 365 9.x ile uyumludur. Bu sürüme güncelleştirmek için Dynamics 365 online çözümler sayfası için Yönetim Merkezi'ni ziyaret edin ve güncelleştirmeyi yükleyin. Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.

Bu konuda, Project Service Automation Güncelleştirme Sürümü 21 V3'te yeni veya değiştirilmiş özellikler ve düzeltmeler listelenmektedir. Bu sürüm, V 3.10.32.50 derleme numarasına sahiptir ve Haziran 2020'de kendi başına güncelleştirme olarak genel kullanıma sunulmuştur.

## <a name="update-release-21"></a>Güncelleştirme Sürümü 21

### <a name="bug-fixes"></a>Hata düzeltmeleri

**Zaman ve Gider**

Aşağıdaki sorunlar giderilmiştir:

- Panolar içinde **saat girişi kılavuz denetimi** barındırdığında kılavuz, pano kılavuz kapsayıcısının tam genişliğini kullanmaz.
- Belirli saat dilimlerinde, **zaman girişi** kılavuzu denetimi kayıtları görüntülemez.
- 21:00'den sonraki zaman girişleri yanlış gün içinde görüntüleniyor.
- Gider kategorisinde, **gerekli gider girişinde** değer yoksa, kullanıcılar giderleri gönderemiyor.

**Kaynak Yönetimi**

Aşağıdaki sorunlar giderilmiştir:

- Etkin olmayan kayıtlar **Mutabakat** görünümünde görüntülenir.
- Geçerli bir kayıt durumu olduğundan emin olmak için genel kaynak karşılama 'da doğrulama eksikti.

**Proje Yönetimi**

Aşağıdaki sorunlar giderilmiştir:

- **Proje** formu ızgaraları (**kaynak ataması**, **görev**, **Mutabakat** görünümü, **gider tahminleri**) bir proje etkin olmasa bile düzenlenebilir olmaya devam eder.
- Yinelenen müşteriler onaylı proje sözleşmelerine bağlı olan müşterilerle birleştirilemez.
- Geçerli takvimi olmayan bir kaynak eklendiğinde, sistem Kullanıcı dostu bir hata iletisi vermez.
- Proje **Microsoft Project eklentisi** ile bağlandığında görev üzerinde **Görev Ekle** düğmesi etkinleşir.
- Çaba, tanımlı bir maliyet fiyatı olan role sahip bir kaynağa sahip bir göreve atanan denetim düzgün olarak büyür.

**Sales**

Aşağıdaki geliştirmeler yapıldı:

- **Fatura sıklığı** ve **Faturalama başlangıcı**, **Fatura zamanlama** sekmesine taşınmıştır.

Aşağıdaki sorunlar giderilmiştir:

- **Rolde** sıfır olmayan toplam satış fiyatı olsa da **toplam satış fiyatı**, **Kategori** için sıfırdır (0).
- Başka bir özelleştirilmiş işlem ek bir alan güncellerken, müşteriler, **fatura durumu** alanının değerini **faturalama için hazır** olarak değiştiremezler.
- Sürekli seçilmişse, **fatura satırlarını Yenile** düğmesi birden çok yinelenen satır oluşturabilir.
- **Fiyatları Güncelleştir** düğmesi, **Hızlı görünüm** formunun **rol fiyatları** alt ızgarada çalışmaz.
- **Satış fiyatı listesi çözümleme** mantığı zaman dilimlerini yanlış işler ve hatalı fiyat listesi seçimine neden olur.
- Tek bir zaman girişi onaylandıktan sonra, projenin **toplam gerçek maliyeti** bir kesirli tutarla kapatılabilir.
- **Alınan roleprice**, **'birincil birim'** ve **'birincil birim fiyatı'** alanlarındaki değerlere sahip değilse, **Fiyat çözümü** mantığı Kullanıcı dostu bir hata iletisi sağlamaz.


[!INCLUDE[footer-include](../includes/footer-banner.md)]