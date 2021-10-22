---
title: Project Service Automation Güncelleştirme Sürümü 36, V3'teki yenilikler veya değişiklikler
description: Bu konu, Microsoft Dynamics 365 Project Service Automation Güncelleştirme Sürümü 36, V3'tebulunan özellikleri ve düzeltmeleri listeler.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/06/2021
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
ms.openlocfilehash: 9b85aed79acb7e7784a23f54a2e9af1cc83f5f4d
ms.sourcegitcommit: 6d9fc4dc851814664bf71729904ab4bedd85fe70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/06/2021
ms.locfileid: "7606833"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-36-v3"></a>Project Service Automation Güncelleştirme Sürümü 36, V3'teki yenilikler veya değişiklikler

[!include [banner](../includes/psa-now-project-operations.md)]

Microsoft Dynamics 365 Project Service Automation uygulaması için en yeni güncelleştirmeyi sunmaktan mutluluk duyarız. Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir. Dynamics 365 9.x ile uyumludur. Bu sürüme güncelleştirmek için Dynamics 365 çevrimiçi çözümler sayfasının için Yönetici Merkezi sayfasını ziyaret edin ve güncelleştirmeyi kurun. Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.

Bu konuda, Project Service Automation Güncelleştirme Sürümü 36 V3'te yeni veya değiştirilmiş özellikler ve düzeltmeler listelenmektedir. Bu sürüm, V3.10.57.152 derleme numarasına sahiptir ve Ekim 2021 tarihinde kendi kendine güncelleştirme ile genel kullanıma sunulmuştur.

## <a name="update-release-36"></a>Güncelleştirme Sürümü 36

### <a name="bug-fixes"></a>Hata düzeltmeleri

Aşağıdaki sorunlar giderilmiştir.

**Genel**
- **Varsayılan Çalışma Saati Şablonu** alanı adı, **Proje parametreleri** sayfasında yanlış çevrilmiş.
- Zaman uyumsuz eklentiler **SharedVariableService** ile ilgili özel durumları doğru şekilde işlemiyor.

**Zaman ve Gider**
- Günlük satırları eksikse veya kullanıcının günlük satırlarını okumak için doğru ayrıcalıkları yoksa, proje onayları iptal edildiğinde yanlış bir hata oluşuyor.
- Bir gider veya zaman girişi birden fazla ilişkili proje onayına sahip olduğunda, kullanıcılar onay işlemini iptal edemiyor.
- **Devamsızlık** ve **Tatil**, **Zaman Giriş** hızlı oluşturma sayfasındaki aramada Çince dili için hatalı çevrilmiş.

**Kaynak yönetimi**
- Görüntüleme modu **Gün**, **Hafta** veya **Ay** olarak ayarlandığında kullanıcı **Zamanlama Yardımcısı**'nda kaynakları arayamıyor.
- Genel kaynakların yanlışlıkla boş konum adlarına sahip olmasına izin verilmiş. 
- Bir sözleşmeyi kaybedildi olarak kapatmak gelecekteki ayırmaları iptal etmiyor.

**Satışlar**
- Bir ortamnda yüksek hacimli ürün olduğunda **Malzeme Tahmini** ızgarasında performans düşüyor.
- Şablondan proje oluştururken, proje para birimi ilgili Proje Yöneticisinin sözleşme birimindeki varsayılan değerini almıyor.
- Gerçek tutarlar, projeye yansıtılan tutarla her zaman eşleşmiyor veya tutarlar belirli geri çağırma senaryolarında negatif oluyor.
- Proje şablonundan oluşturulan bir projeyi bir sözleşme satırıyla ilişkilendirdiğinde hata oluşuyor.
- Kullanıcılar, **Faturalamaya hazır** ve **Fatura Oluşturuldu** kilometre taşlarına sahip bir sözleşme satırını silebiliyorlar. Buna izin verilmemelidir.
- Tahminler bir projeden alındığında, teklif satırı için görev tabanlı faturalama etkinleştirildiğinde teklif satırı borçlandırılabilirlik ayrıntısı hatalı şekilde ayarlanıyor.
- Sabit fiyatlı faturalama kilometre taşı eklediğinizde, kilometre taşı sayfa yenilenene kadar kilometre taşı alt ızgarasında yansıtılmaz.
- Boş bir teklif adıyla bir proje sözleşmesi oluşturduğunuzda null başvuru özel durumu oluşur.
- Proje para biriminin kaynağın para biriminden farklı olduğu manuel mod görevleri yanlış fiyat tahminlerine neden olur.
- Kullanıcılar düzeltici fatura tarafından başarıyla düzeltilen bir hareketi geri çağıramıyor.
- Devre dışı bırakılan işlem kategorileri, **Gider Tahminleri** ızgarasında görüntüleniyor.



