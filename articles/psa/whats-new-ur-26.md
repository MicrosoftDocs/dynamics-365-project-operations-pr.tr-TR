---
title: Project Service Automation Güncelleştirme Sürümü 26, V3'teki yenilikler veya değişiklikler
description: Bu konuda, Project Service Automation, Güncelleştirme Sürümü 26, V3'teki özellikler ve düzeltmeler listelenir.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 6aafe66fe8c63dc886455a36e93f32d4a581d5cc
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005590"
---
# <a name="project-service-automation-update-release-26-v3"></a>Project Service Automation, Güncelleştirme Sürümü 26, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Dynamics 365 için Project Service Automation uygulamasına yönelik en son güncelleştirmeyi duyurmaktan mutluluk duyuyoruz. Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir. Bu sürüm Dynamics 365 9.x ile uyumludur. Bu sürüme güncelleştirmek için Dynamics 365 online çözümler sayfası için Yönetim Merkezi'ni ziyaret edin ve güncelleştirmeyi yükleyin. Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.

Bu konuda, Project Service Automation Güncelleştirme Sürümü 26 V3'te yeni veya değiştirilmiş özellikler ve düzeltmeler listelenmektedir. Bu sürümün derleme numarası V3.10.44.59'dur ve genellikle Aralık 2020'de kendi kendini güncelleştirme aracılığıyla kullanılabilir.

## <a name="update-release-26"></a>Güncelleştirme Sürümü 26

### <a name="bug-fixes"></a>Hata düzeltmeleri

**Zaman ve Gider**

Aşağıdaki sorunlar giderilmiştir:

- Kullanıcıların, onaylanan/gönderilen bir zaman girişinde görevi değiştirebilmesi.
- Zaman girişini kaydederken karşılaşılan "Nesne Başvurusu Ayarlanmadı" hatası.
- Kaynak atamalarından zaman girişi içeri aktarmasının yanlış DateTime değerlerine sahip zaman girişleri oluşturması.
- Project Service Automation ve Field Service uygulamalarının her ikisi de yüklüyken Field Service uygulamasındaki zaman girişleri için komut çubuğunda **Yeni** düğmesinin iki kez görüntülenmesi.
- **Birime İzin Ver** ve **Birim grubu** hücre güncelleştirmelerinin artık **Gider Tahminleri** ızgarasında çalışması.
- **Zaman Girişi Düzenlemesi Güncelleştirmesi** formunun **Zaman Çizelgesi** içermesi.
- Proje dışı zaman girişleri için zaman onayının, bir proje onaylayıcı rolü araması sırasında sistemi engellemesi.

**Kaynak Yönetimi**

Aşağıdaki sorunlar giderilmiştir:

- Birincil gereksinim oluşturmadan önce başka bir birincil gereksinim olup olmadığını kontrol etmek için **PostProjectCreate** eklentisine doğrulama eklendi.
- **Proje Takımı Üyesi** hızlı oluşturma formunun, alanlar formdan kaldırıldığında null başvuru özel durumu oluşturması.
- 1 yıldan uzun bir süre için 12 saatlik gereksinimler oluşturma işleminin başarısız olması.
- Kaynak gereksinimi oluşturma sırasında görüntülenen hata iletisi null başvuru özel durumu iyileştirildi.

**Proje Yönetimi**

Aşağıdaki sorunlar giderilmiştir:

- **PreProjectUpdate** eklentisinde oluşturulan null başvuru özel durumunu gidermek için doğrulama iyileştirildi.
- Microsoft Project masaüstü eklentisi tarafından yayımlanan projelerin atanmamış atamaları silmesi.
- **PreValidateProjectTaskUpdate** eklentisindeki null başvuru özel durumu nedeniyle bir görevin proje başvurusunun geçersiz olduğu durum için yeni doğrulama eklendi.
- Takım Üyesi kılavuzunun takım üyesi kaydında farklı atamalar göstermemesi.
- **PreProjectTaskDelete** eklentisindeki null başvuru özel durumu için yeni doğrulama ve hata iletileri eklendi.

**Sales**

Aşağıdaki sorunlar giderilmiştir:

- Teklif veya sözleşmede proje tabanlı bir satır seçerken **Öneri** düğmesinin yalnızca var olan bir ürünle ilişkili ürün tabanlı bir satır seçildiğinde görünür olması.
- **Create_Product** ayrıcalığının **Create_ProjectContract** ayrıcalığından ayrılması.
- Fatura satırının silinmesinin **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice** üzerinde null başvuru hatasına neden olması.


[!INCLUDE[footer-include](../includes/footer-banner.md)]