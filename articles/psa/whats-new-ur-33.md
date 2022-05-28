---
title: Project Service Automation Güncelleştirme Sürümü 33, V3'teki yenilikler veya değişiklikler
description: Bu konuda, Project Service Automation, Güncelleştirme Sürümü 33, V3'teki özellikler ve düzeltmeler listelenir.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 063290526c25e7073137fc88408be6a61d2d20ac
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8601502"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a>Project Service Automation Güncelleştirme Sürümü 33, V3'teki yenilikler veya değişiklikler

[!include [banner](../includes/psa-now-project-operations.md)]

Microsoft Dynamics 365 Project Service Automation uygulaması için en yeni güncelleştirmeyi sunmaktan mutluluk duyarız. Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir. Dynamics 365 9.x ile uyumludur. Bu sürüme güncelleştirmek için Dynamics 365 çevrimiçi çözümler sayfasının için Yönetici Merkezi sayfasını ziyaret edin ve güncelleştirmeyi kurun. Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.

Bu konuda, Project Service Automation Güncelleştirme Sürümü 33 V3'te yeni veya değiştirilmiş özellikler ve düzeltmeler listelenmektedir. Bu sürüm V3.10.54.98 derleme numarasına sahiptir ve genellikle Temmuz 2021'de bir kendi kendine güncelleştirme yoluyla kullanılabilir.

## <a name="update-release-33"></a>Güncelleştirme Sürümü 33

### <a name="bug-fixes"></a>Hata düzeltmeleri

**Zaman ve Gider**

Aşağıdaki sorunlar giderilmiştir:

- Kilitli iki alan olan **msdyn_description** ve **msdyn_externaldescription** gönderimden sonra düzenlenebilir.
- Bir projeyle ilgili olmayan bir gider oluşturulursa bir hata iletisi oluşur.
- Bir zaman girişi oluşturulduğunda, kaynak rolü varsayılan olarak etkin olmayan bir role ayarlanır.
- Geri çağrılmış ve silinmiş giderle ilişkili günlük satırları silinmez.
- **Zaman girişi Hızlı Oluştur Formunda** varsayılan olarak görüntülenen tarihi görevin başlangıç tarihi olarak değiştirmek için **Proje Görev Listesi** görünümünü güncelleştirin.
- Ayrılabilir kaynağın **İlgili** sekmesinden bir zaman girişi oluşturduğunuzda, zaman girişi üst ayrılabilir kaynak yerine yanlışlıkla oturum açmış olan kullanıcısı için oluşturuluyor.
- **Toplu onay MDD** iletişim kutusuna yeni alanlar eklendi.

**Proje planlama**

Aşağıdaki sorunlar giderilmiştir:
- Proje çalışma saati şablonları karmaşık takvimlerle uygulandığında düşük proje oluşturma performansı.
- Başlangıç tarihi bitiş tarihinden büyük olduğunda, her alanın saat bileşenindeki farklılıklar nedeniyle proje şablonu kopyalama işleminde bir hata görüntülenir.

**Kaynak yönetimi**

Aşağıdaki sorunlar giderilmiştir:
- Kaynak kullanım sorgusunda yanlış bir parametre kullanılıyor ve XML **Kaynak Kullanımı** ızgarasında yanlış filtre sonuçlarına yol açıyor.
- **Ayırmaları Uzat** onayı, ayırmalar için yanlış bitiş tarihi görüntülüyor.

**Satışlar**

Aşağıdaki sorunlar giderilmiştir:
- Eksik değerlerle bir kategori fiyatı oluşturulursa bir hata iletisi oluşuyor.
- Bir sipariş satırı olmadan bir sözleşme satırı kilometre taşı oluşturulursa hata iletisi oluşuyor.
