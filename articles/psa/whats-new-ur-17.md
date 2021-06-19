---
title: Project Service Automation Güncelleştirme Sürümü 17, V3'teki yenilikler veya değişiklikler
description: Bu konuda, Project Service Automation, Güncelleştirme Sürümü 17, V3'teki özellikler ve düzeltmeler listelenir.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: 364a64e0ea501ac5b7faaf254c7af3648cfe1f9b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006715"
---
# <a name="project-service-automation-update-release-17-v3"></a>Project Service Automation, Güncelleştirme Sürümü 17, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Dynamics 365 için Project Service Automation uygulamasına yönelik en son güncelleştirmeyi duyurmaktan mutluluk duyuyoruz. Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir.  Bu sürüm Dynamics 365 9.x ile uyumludur. Bu sürüme güncelleştirmek için Dynamics 365 online Yönetim Merkezi'ni ziyaret edin ve çözümler sayfasından güncelleştirmeyi yükleyin. Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.

Bu konuda, PSA V3, Güncelleştirme Sürümü 17'te yeni veya değiştirilmiş özellikler ve düzeltmeler listelenir. Bu sürüm, V3.10.6.34 derleme numarasına sahiptir ve Mart 2020 tarihinde kendi kendine güncelleştirme ile genel kullanıma sunulmuştur.


## <a name="update-release-17"></a>Güncelleştirme Sürümü 17

### <a name="bug-fixes"></a>Hata düzeltmeleri

**Genel**

- Düzeltildi: Project Service Automation Takım Üyesi lisanslarını zorlamak üzere güncelleştirildi (Proje Kaynağı Merkezi, Takım Üyesi Hizmet planı meta verileri 3.x'i içerecektir)
 
**Zaman ve Gider**

- Düzeltildi: Gider tahminini sıfır olmayan bir fiyattan sıfıra (0) değiştirmek mümkün değildir. Bu değişiklik yok sayılır.

**Proje Yönetimi**

- Düzeltildi: Takım üyesinin pozisyon adına null değerleri için bir denetim eklendi.
- Düzeltildi: **msdyn_resourceassignment** varlığındaki **msdyn_userresourceid** alanı kullanımdan kaldırıldı.
- Düzeltildi: 2.x'ten 3.x'e yükseltme artık görev atamalarındaki boş çalışma sınırlarını işliyor.

**Sales**

- Düzeltildi: **Invoice.PreValidateInvoiceUpdate** artık kayıt sahiplerini düzgün şekilde yeniden atama senaryosunu işliyor.
- Düzeltildi: İşlem sınıfı **Zaman** olduğunda **UnitGroup**; **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail** ve **ContractLineDetails** dahil tüm varlıklar için düzenlenebilir değildir. Ancak, **Birim** yalnızca **JournalLine** ve **InvoiceLineDetails** için düzenlenemez.




[!INCLUDE[footer-include](../includes/footer-banner.md)]