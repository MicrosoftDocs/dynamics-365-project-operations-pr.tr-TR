---
title: Project Operations çift yazma eşlemesi sürümleri
description: Bu konu Dynamics 365 Project Operations için gereken çift yazma eşlemelerinin listesi sağlanır .
author: sigitac
ms.date: 04/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b24a20d47eefa43b2e4e184a377decdb280d436d
ms.sourcegitcommit: fd6e9ff78392c7bac35591d9130c00d2750438ae
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025798"
---
# <a name="project-operations-dual-write-map-versions"></a>Project Operations çift yazma eşlemesi sürümleri

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Kaynak/Stoklanmayan senaryolarda Dynamics 365 Project Operations kullanılması, bir dizi ikili yazma eşlemelerinin ortamda çalışmasını gerektiriyor. 

## <a name="prerequisite-maps-dual-write-orchestration-solution"></a>Önkoşul haritalari: Çift yazma düzenleme çözümü

Aşağıdaki eşlemeler Project Operations çözümü için gerekli ön koşullar. Aşağıdaki tabloda listelenen haritalara ve ortamınızda bulunan tüm ilişkili tablo haritalarına sahip olduğunuzdan emin olun.

| Tablo eşlemesi | İlk eşitleme |
| --- | --- |
| Kayıt Defteri (msdyn_ledgers) | Tablo haritasında ve tüm önkoşulların ilk eşitlemesini gerekir. İlk eşitleme için ana öğe, Finance and Operations uygulamalardı. |
| Tüzel kişilikler (cdm_companies) | Gerekli değil. Ortamlar çift yazma kullanılarak bağlandığında sistem bu varlığı otomatik olarak doldurur. |
| Müşteri V3 (firmalar) | Sağlama için gerekli değildir. |
| Satıcılar V2 (msdyn_vendors) | Sağlama için gerekli değildir. |

1. Eşlemeler listesinden, tüm ön koşullarıyla Kayıt Defteri **(msdyn\_ledgers)** eşlemesini seçin ve **İlk eşitleme** onay kutusunu seçin. **İlk eşitleme için asıl** alanında, hem genel muhasebe eşlemesi hem de tüm ön koşul haritaları için **Finance and Operations uygulamalar** seçin. **Çalıştır** seçin.

![Kayıt Defteri eşleme eşitlemesi](media/DW6.png)

2. Yukarıdaki tabloda listelenen tüm tablo haritalarının aynı adımlarını uygulayın. Bu eşlemeler çalıştırılırken **ilk eşitleme** onay kutusunu seçmeyin.

## <a name="project-operations-dual-write-maps"></a>Project Operations Çift Yazma haritaları

Aşağıdaki eşlemeler Project Operations çözümü için gerekli ön koşullar. Çift yazılır harita sürümleri, Project Operations 2021 güncelleştirmesi, sürüm 4.10.0.186'dan itibaren listelenir.

| **Varlık eşlemesi** | **En son sürüm** | **İlk eşitleme** |
| --- | --- | --- |
| Proje işlem ilişkilerine ait tümleştirme varlığı (msdyn\_transactionconnections) | Kategori 1.0.0.0 | Sağlama için gerekli değildir. |
| Proje sözleşmesi başlıkları (satış siparişleri) | Kategori 1.0.0.1 | Sağlama için gerekli değildir. |
| Proje sözleşme satırları (salesorderdetails) | Kategori 1.0.0.0 | Sağlama için gerekli değildir. |
| Proje Finansmanı kaynağı (msdyn_projectcontractsplitbillingrules) | 1.0.0.2 | Sağlama için gerekli değildir. |
| Malzeme tahminleri için Project Operations tümleştirme tablosu (msdyn\_estimatelines) | Kategori 1.0.0.0 | Sağlama için gerekli değildir. |
| Proje faturası teklifleri V2 (faturalar) | 1.0.0.3 | Sağlama için gerekli değildir. |
| Project Operations tümleştirmesi gerçek değerleri (msdyn_actuals) | Kategori 1.0.0.14 | Sağlama için gerekli değildir. |
| Project Operations tümleştirme sözleşme satırı kilometre taşları (msdyn_contractlinesscheduleofvalues) | Kategori 1.0.0.4 | Sağlama için gerekli değildir. |
| Gider tahminleri için Project Operations tümleştirme varlığı (msdyn_estimateslines) | Kategori 1.0.0.2 | Sağlama için gerekli değildir. |
| Saat tahminleri için Project Operations tümleştirme varlığı (msdyn_resourceassignments) | Kategori 1.0.0.5 | Sağlama için gerekli değildir. |
| Project Operations tümleştirme proje gideri kategorileri dışarı aktarma varlığı (msdyn_expensecategories) | 1.0.0.1 | Sağlama için gerekli değildir. |
| Project Operations tümleştirme proje giderleri dışarı aktarma varlığı (msdyn_expenses) | Kategori 1.0.0.2 | Sağlama için gerekli değildir. |
| Project Operations tümleştirme projesi satıcı fatura dışa aktarma varlığı (msdyn_projectvendorinvoices) | Kategori 1.0.0.0 | Sağlama için gerekli değildir. |
| Project Operations tümleştirme projesi satıcı fatura satırı dışa aktarma varlığı (msdyn_projectvendorinvoicelines) | 1.0.0.1 | Sağlama için gerekli değildir. |
| Tüm Şirketler için Proje Kaynak Rolleri (bookableresourcecategories) | Kategori 1.0.0.1 | Sağlama sırasında Dynamics 365 Dataverse ortamında doldurulan proje yöneticisi ve takım üyesi kaynak rollerini eşitlemek için tablo haritasında başlangıç eşitlemesi yapılmasını ister. Dataverse, ilk eşitleme için ana kaynaktır. |
| Proje görevleri (msdyn_projecttasks) | Kategori 1.0.0.4 | Sağlama için gerekli değildir. |
| Proje hareket kategorileri (msdyn_transactioncategories) | Kategori 1.0.0.0 | Sağlama için gerekli değildir. |
| Projeler v2 (msdyn_projects) | 1.0.0.2 | Sağlama için gerekli değildir. |

Listelenen eşlemelerde çalışmak için aşağıdaki adımları uygulayın.

1. Bu eşleme ilk eşitlemeyi gerektirmesi için **tüm şirketler (bookableresourcecategories)** tablo eşlemesi Için proje kaynak rolleri etkinleştirin. **İlk eşitleme için asıl** alanında **Common Data Service**'ni seçin. 

 ![Kaynak rolü tablo eşlemesi eşitlemesi](media/6ResourceInitialSync.jpg)

 Sonraki adıma geçmeden önce eşlemenin durumunun **çalışır** durumda olmasını bekleyin.

2. Kalan tüm gerekli haritaların tümünü seçin. Bunları çift noktalı harita listesinde, anahtar sözcüğü, sağ üst köşedeki arama **projesi** ile filtreleyebilirsiniz. Tüm eşleşmeleri çoklu seçebilir ve çalıştırabilirsiniz. Daha fazla bilgi için bkz. [Birden çok tablo haritası yönetme](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/multiple-entity-maps). Ayrıca ilgili varlık eşlemelerini etkinleştirip çalıştırmayı unutmayın.

### <a name="project-operations-dual-write-map-versions"></a>Project Operations çift yazma eşlemesi sürümleri

Her zaman ortamınızda eşlemenin en son sürümünü çalıştırın. Aşağıdaki koşullardan biri geçerliyse, belirli özellikler ve yetenekler doğru çalışmayabilir:

- Bir harita etkinleştirilmez.
- Haritanın en son sürümü etkin değil. 
- İlgili tablo eşleşmeleri etkinleştirilmez.

Haritanın etkin sürümünü **ikili yazma** sayfasındaki **sürüm** sütununda görebilirsiniz. Yeni bir harita sürümünü, **tablo Haritası sürümlerini** seçip en son sürümü seçerek ve ardından seçili sürümü kaydederek etkinleştirebilirsiniz. Kutulu bir tablo haritasını özelleştirdiyseniz, değişiklikleri yeniden uygulayın. Daha fazla bilgi için bkz. [Uygulama Yaşam Döngüsü Yönetimi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)
