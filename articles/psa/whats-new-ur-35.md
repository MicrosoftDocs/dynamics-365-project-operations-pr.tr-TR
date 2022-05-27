---
title: Project Service Automation Güncelleştirme Sürümü 35, V3'teki yenilikler veya değişiklikler
description: Bu konu, Microsoft Dynamics 365 Project Service Automation Güncelleştirme Sürümü 35, V3'tebulunan özellikleri ve düzeltmeleri listeler.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/03/2021
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
ms.openlocfilehash: e210777f1e4d149b700721ac7fb9bd129b1166fe
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574073"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-35-v3"></a>Project Service Automation Güncelleştirme Sürümü 35, V3'teki yenilikler veya değişiklikler

[!include [banner](../includes/psa-now-project-operations.md)]

Microsoft Dynamics 365 Project Service Automation uygulaması için en yeni güncelleştirmeyi sunmaktan mutluluk duyarız. Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir. Dynamics 365 9.x ile uyumludur. Bu sürüme güncelleştirmek için Dynamics 365 çevrimiçi çözümler sayfasının için Yönetici Merkezi sayfasını ziyaret edin ve güncelleştirmeyi kurun. Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.

Bu konuda, Project Service Automation Güncelleştirme Sürümü 35 V3'te yeni veya değiştirilmiş özellikler ve düzeltmeler listelenmektedir. Bu sürüm V3.10.56.110 derleme numarasına sahiptir ve Eylül 2021'de bir kendi kendine güncelleştirmeyle genel kullanıma sunulacaktır.

## <a name="update-release-35"></a>Güncelleştirme Sürümü 35

### <a name="bug-fixes"></a>Hata düzeltmeleri

Aşağıdaki sorunlar giderilmiştir.

**Zaman ve Gider**

- Proje onaylayanları, **Proje Onaylayan** rolü ile gider girişlerini onayladıklarında bir okuma ayrıcalığı hatası alıyor.
- Proje onaylayanları, **Proje Onaylayanı** rolüyle onaylanan bir zaman girişini iptal ederken **msdyn_projectapproval** üzerinde bir yazma ayrıcalığı hatası alıyor.
- Telefon için Dynamics 365 - Proje Kaynağı Merkezi uygulama modülünde **Haftayı kopyala**'yı seçtiğinizde şu hata oluşuyor: "...\OfficeProductivity_RibbonRules.js.map: HTTP error: status code 404, net::ERR_HTTP_RESPONSE_CODE_FAILURE."
- **Yeniden dene** ilkesi, daha önce reddedilen girişleri otomatik olarak onaylıyor.
- **Onay Kümeleri** alt ızgarası, geçerli olmayan şerit eylemlerini gösteriyor.
- **Zaman Girişi** varlığındaki **Proje Görevi** ve **Kaynak Rolü** için simgeler eksik.
- Kaynak atamalarını içeri aktardığınızda, içeri aktarılan zaman girişleri manuel mod görevleriyle oluşturulmuş atamalar için doğru süreye sahip olmuyor.
- **Zaman Giriş kayıtları için Gelişmiş Bul** sayfasında **Sil** yok.
- **Zaman giriş bilgileri** sayfasında **Kaydet** yok. Bu sorun, sayfa kapatıldığında değişikliklerin kaydedilmesini engeller.

**Proje planlama**

- **Kaynak Ataması** ve **Kaynak Mutabakatı** ızgaraları gruplandırılmış öznitelikleri alfabetik olarak sıralamıyor.
- Tarih davranışı **Yalnızca Tarih** olarak özelleştirilmişse görevler oluşturulamıyor.

**Kaynak yönetimi**

- Hem Dynamics 365 Field Service hem de Project Service Automation yüklüyse, **Kaynak Gereksinimi İlişkili Görünümü** ana sayfayla ilişkilendirildiğinde aşırı katmanlama sorunları oluşuyor.
- **Takım Üyesi Hızlı Oluştur** iletişim kutusunda **Kaydet**'e çift tıklamak, kaynak gereksiniminin oluşturulmasını engelliyor.

**Satışlar**

- **Kazanıldı** durumuna sahip bir teklifle ilişkilendirilmiş bir görevi sildiğinizde bir özel durum oluşuyor.
