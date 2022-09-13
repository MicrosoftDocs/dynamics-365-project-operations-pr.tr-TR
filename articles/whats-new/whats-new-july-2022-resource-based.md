---
title: Temmuz 2022'deki yenilikler - Kaynağı/stoğu tutulmayan öğeleri temel alan senaryolar için Project Operations
description: Bu makale, kaynak/stoğu tutulmayanları temel alan senaryolar için Microsoft Dynamics 365 Project Operations'ın Temmuz 2022 sürümünde kullanılabilen kalite güncelleştirmeleri hakkında bilgi sağlar.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: e63b29741dbaa400a2176ff8b4c35c6d64dfeab4
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403976"
---
# <a name="whats-new-july-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Temmuz 2022'deki yenilikler - Kaynağı/stoğu tutulmayan öğeleri temel alan senaryolar için Project Operations

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Bu makale aşağıdaki Microsoft Dynamics 365 Project Operations bileşenleri ve sürümleri için geçerlidir:

- Dataverse ortamı sürümü 4.44.0.22'da Project Operations
- Dynamics 365 Finance ortamı sürümü 10.0.28'da proje yönetimi ve muhasebe

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations çift yazma eşlemesi güncellemeleri

Bu sürümde Project Operations çift yazma eşlemeleri için güncelleştirme yoktur. Project Operations çift yazma eşlemelerinin geçerli listesi ve sürümleri için bkz. [Project Operations çift yazma eşleme sürümleri](../environment/resource-dual-write-maps.md).

Her zaman ortamınızda eşlemenin en son sürümünü çalıştırın ve Project Operations Dataverse çözümünüzü ve Finance çözümü sürümünüzü güncelleştirirken tüm ilgili tablo eşlemelerini etkinleştirin. Haritanın en son sürümü etkinleştirilmemişse bazı özellikler ve yetenekler doğru çalışmayabilir. Haritanın etkin sürümünü **çift yazma** sayfasındaki **sürüm** sütununda görebilirsiniz. Yeni bir harita sürümünü etkinleştirmek için **Tablo haritası sürümleri**'ni seçip en son sürümü seçin ve ardından seçili sürümü kaydedin. Kullanıma hazır tablo haritasını özelleştirdiyseniz, değişiklikleri yeniden uygulayın. Daha fazla bilgi için bkz. [Uygulama Yaşam Döngüsü Yönetimi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)

Eşlemeyi başlatırken bir sorunla karşılaşırsanız, Çift Yazma sorun giderme kılavuzunun [Eşlemelerde eksik tablo sütunu sorunları](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) bölümündeki yönergeleri izleyin.

## <a name="quality-updates"></a>Kalite güncelleştirmeleri

### <a name="project-operations-on-dataverse"></a>Dataverse üzerinde Project Operations

| Özellik alanı | Referans numarası | Kalite güncelleştirmeleri |
| --- | --- | --- |
| Dağıtım ve Yapılandırma | Kategori 2761472 | Project Operations yükleme hatası işlenir. |
| Fatura ve Fiyatlandırma | Kategori 2746940 | Taşeron satır adı en fazla 100 karakter uzunluğunda olmalıdır. |
| Fatura ve Fiyatlandırma | Kategori 2739162 | Müşterilerin, gerçek değerler kılavuz görünümünde şerit düğmelerini görebilmeleri gerekir. |
| Proje Planlama ve İzleme | Kategori 2730318 | Proje konusunun desteklenmeyen karakterleri için doğrulama güncelleştirildi. |
| Fatura ve Fiyatlandırma | Kategori 2705361 | Faturalanan satış kilometre taşı proje izleme alanlarına dahil edilmelidir. |
| Fatura ve Fiyatlandırma | Kategori 2675880 | Bir projenin iş tabanlı olmayan bir sözleşme satırına bağlanmasını engelleyin. |
| Fatura ve Fiyatlandırma | Kategori 2664396 | Teklif fiyat listesi, teklif olmadan kaydedilirse, teklifin boş olamayacağını belirten bir hata olması gerekir. |
| Fatura ve Fiyatlandırma | Kategori 2184019 | **Görev tabanlı faturalama** sekmesi, hiçbir çalışan sözleşmesi veya teklifi olmayan projeler için gösterilmemelidir. |
| Zaman ve Gider | Kategori 2754459 | Yinelenen zamanlama bulut akışı etkin olmadığında, başlık gösterilir ve zaman uyumsuz işleme atlanır. |
| Fatura ve Fiyatlandırma | Kategori 2724391 | Proje sözleşmesi bölünmüş fatura kuralında bir müşteri değeri eksik olduğunda yanlış özel durum oluşur. |
| Fatura ve Fiyatlandırma | Kategori 2708638 | Malzeme Kullanımları ve Malzeme Kullanım Onayları'nda kılavuz araması kullanılarak arama yapılırken kayıt bulunamadı.|
| Fatura ve Fiyatlandırma | Kategori 2686977 | Fatura oluşturma sırasında fatura satırı için doğrulama engellenir. |
| Fatura ve Fiyatlandırma | Kategori 2683032 | Borçlandırılabilir rollerin ve kategorilerin kopyalanması 5000 kaydın ötesine ölçeklenmez.|
| Fatura ve Fiyatlandırma | Kategori 2673363 | Bir proje için hem İşçilik hem de Gider tahmin değerleri ile gerçek değerleri var olduğunda, Proje Maliyet Tüketimi Yüzdesi bozulur. |

### <a name="project-management-and-accounting-in-finance"></a>Finance'ta proje yönetimi ve muhasebe

Bu güncelleştirmeye dahil edilen hata düzeltmeleri hakkında bilgi için Microsoft Dynamics Lifecycle Services'te (LCS) oturum açın ve [şu BB makalesini](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438) görüntüleyin.

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Özellikler, gelecek sürümde varsayılan olarak açıktır

Aşağıdaki tabloda, 10.0.29 sürümünde varsayılan olarak açık özellikler listelenmektedir. Açık olarak etkinleştirilmiş çoğu özellik, [Özellik yönetiminde](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) kapatılabilir. Gelecekte, otomatik olarak açık olan bazı özellikler özellik yönetiminden kaldırılabilir ve zorunlu hale gelir. Bu değişiklik, müşterilerin geçerli işlevleri kullanmalarını sağlar; böylece iyileştirmeler, eklendikçe geçerli işlevsellik üzerinde oluşturulabilir. Özellikler, temel olarak belirlenmedikçe, hiçbir zaman bir yıldan daha kısa sürede otomatik olarak etkinleştirilmez.

| Özellik adı | Etkinleştirme tarihi | Özelliğin eklenme tarihi | Özellik durumu | Modül |
| --- | --- | --- |--- |--- |
| Fonlama kural tahsisatına göre saat hareketine göre ayarlamayı etkinleştir | 16 Eylül 2022 | 7 Ekim 2020 | Varsayılan olarak açık | Proje yönetimi ve muhasebe |
| Proje satınalma siparişi peşinat fatura ters işlemi özelliği | 16 Eylül 2022 | 6 Ekim 2021 | Varsayılan olarak açık | Proje yönetimi ve muhasebe |
| Kaynak tabanlı/stoklanmayan senaryolar için Project Operations kullanırken fatura teklif satırlarını silme | 16 Eylül 2022 | 6 Ekim 2021 | Varsayılan olarak açık | Proje yönetimi ve muhasebe |
| Deftere nakledilen bir proje hareketinde hesap oluşturmayı ayarlama | 16 Eylül 2022 | 10 Mayıs 2020 | Varsayılan olarak açık | Proje yönetimi ve muhasebe |
| Proje için varsayılan muhasebe kurulumunu etkinleştir | 16 Eylül 2022 | 19 Şubat 2020 | Varsayılan olarak açık | Proje yönetimi ve muhasebe |
| Bir proje için birden çok sözleşme satırını etkinleştirme | 16 Eylül 2022 | 29 Haziran 2020 | Varsayılan olarak açık | Proje yönetimi ve muhasebe |
| Geçerli onay durumu düzenlemeye izin vermiyorsa Proje Saati günlüklerini salt okunur yap | 16 Eylül 2022 | 6 Ekim 2021 | Varsayılan olarak açık | Proje yönetimi ve muhasebe |
| Satınalma satırları güncelleştirildiğinde ve satınalma siparişi değişikliği yönetimi parametresi etkin olduğunda satış satırlarını satınalma satırlarından eşitlemeye izin ver | 16 Eylül 2022 | 7 Ekim 2020 | Varsayılan olarak açık | Proje yönetimi ve muhasebe |
| Dynamics 365 Customer Engagement'ta Project Operations'ı etkinleştirme | 16 Eylül 2022 | 29 Haziran 2020 | Varsayılan olarak açık | Proje yönetimi ve muhasebe |
| Proje hareketi tersine çevirme düzeltme özelliği | 16 Eylül 2022 | 13 Temmuz 2020 | Varsayılan olarak açık | Proje yönetimi ve muhasebe |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>Yaklaşan sürümde zorunlu hale gelen özellikler

Aşağıdaki tabloda, 10.0.29 sürümü ve sonrasında zorunlu özellikler listelenmektedir.

| Özellik adı | Etkinleştirme tarihi | Özelliğin eklenme tarihi | Özellik durumu | Modül |
| --- | --- | --- | --- | --- |
| Finansman kaynağı üzerinde, döviz kurunu yuvarlamadan taahhüt edilen değer hesapla | 16 Eylül 2022 | 14 Haziran 2020 | Zorunlu | Proje yönetimi ve muhasebe |
| Özgün hareket olarak aynı genel muhasebe hesabıyla proje düzeltme deftere naklini etkinleştir | 16 Eylül 2022 | 14 Haziran 2020 | Zorunlu | Proje yönetimi ve muhasebe |
| Proje sözleşme taahhüt edilen tutar ayrıntısı | 16 Eylül 2022 | 31 Ağustos 2019 | Zorunlu | Proje yönetimi ve muhasebe |
| Proje fatura teklifi oluşturma sırasında kaynağa göre sıralamayı etkinleştir | 16 Eylül 2022 | 31 Ağustos 2019 | Zorunlu | Proje yönetimi ve muhasebe |
