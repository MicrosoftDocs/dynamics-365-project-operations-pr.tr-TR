---
title: Kasım 2020 Yenilikler - Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations
description: Bu makale, kaynak/stoğu tutulmayan öğeleri temel alan senaryolar için Project Operations Kasım 2020 sürümünde yer alan kalite güncelleştirmeleri hakkında bilgi sağlar.
author: sigitac
ms.date: 10/30/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b98c968a040c14f4d11c350885e2cbb984596c48
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923442"
---
# <a name="whats-new-november-2020---project-operations-for-resourcenon-stocked-based-scenarios"></a>Kasım 2020 Yenilikler - Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Bu makale aşağıdaki Dynamics 365 Project Operations bileşenleri ve sürümleri için geçerlidir:

- CDS ortamıdna Project Operations sürüm 4.4.0.70
- Dynamics 365 Finance ortamı sürümü 10.0.14'te proje yönetimi ve muhasebe

## <a name="updates-to-project-operations-for-resource-non-stocked-based-scenarios"></a>Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations güncellemeleri

### <a name="project-operations-on-cds"></a>CDS'de Project Operations

| Özellik alanı                 | Referans numarası | Kalite güncelleştirmeleri                                                                                                                                                                    |
|------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   Fırsat yönetimi       | Kategori 2036993          | Teklif satırı türü **Tüm görevler** olduğunda, tahmini satır ve kaynak atama sözleşme satırları kazanan tekliflere güncelleştirilir.                                                 |
| Fatura ve fiyatlandırma          | Kategori 2070392          | Faturadaki proje sözleşme satırları, **fatura hareketlerini yenileme** her seçiliyse artar.                                                                         |
| Proje planlama             | Kategori 2043336          | Bir proje takım üyesi kaydı silinemiyor.                                                                                                                                  |
| Proje planlama             | Kategori 2046013          | Yükleme sırasında, tahmin sırasında etiket sütunları için tutarsız davranış, zaman aşamalı tür değişikliği.                                                                                   |
| Proje planlama             | Kategori 2046647          | Proje ekibi üyelerinden kaynak gereksinimleri oluşturulurken başlangıç ve bitiş saatleri bir saat olarak kapalı durumdadır.                                                                      |
| Proje planlama             | Kategori 2053879          | (Gelecekteki CD dağıtımı başına) PublishUnassignedAssignments, "The   value passed for ConditionOperator.In is   empty" hatası oluştuğunda bir görevi kaydetme girişimini keser.                       |
| Proje planlama             | Kategori 2055501          | **Proje başlangıç tarihi** boş bırakılırsa zamanlamadaki bir arıza neden olur.                                                                                                      |
| Proje planlama             | Kategori 2066817          | **Görevler** sekmesindeki Kişi Seçici'yi kullanan genel bir kaynak oluşturamaz.                                                                                                   |
| Proje planlama             | Kategori 2067034          | **Ayrıntıları görüntüle** düğmesi **görev ayrıntıları** sayfasında kullanılamaz.                                                                                                       |
| Kaynak yönetimi          | Kategori 2046667          | Genel ekip üyeleri, tüm kaynaklar karşılandıktan sonra da silinmezler.                                                                                                    |
| Zaman ve hızlı gider girişi | Kategori 2047499          | Zaman girişi sayfasındaki **yeni** düğmesi **Yeni e-posta imza** sayfasını açar.                                                                                               |
| Zaman ve hızlı gider girişi | Kategori 2059859          | Masraf girişi oluştururken beklenmeyen açılır pencere açılır.                                                                                                                         |
| Diğer                        | Kategori 2044181          | (Satın alma siparişini kaldırma) - msdyn_ProjectServiceCore_Patch ve msdyn Project servis çekirdek çözümlerini kaldırmaya çalıştığınızda "Kayıt kullanılamıyor" hatası oluşuyor.  |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Dynamics 365 Finance'ta proje yönetimi ve muhasebe

| Özellik alanı        | Referans numarası | Kalite güncelleştirmeleri                                                                                                                                                            |
|---------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Gelir tanıma | [451662](https://fix.lcs.dynamics.com/Issue/Details/?bugId=451662)           | Sözleşme yabancı bir para birimi kullanırken ve tamamlanma durumu için çalışma ilerlemesi yüzdesi tamamlandığında proje tahmin yüzdesi yanlış.                     |
| Gelir tanıma | [469894](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469894)           | **Gerçek maliyet** tamamlama yöntemiyle yapılan tahminler deftere nakledilemiyor.                                                                                                    |
| Gelir tanıma | [485439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485439)           | Şirket para birimi ve hareket para birimi farklı olduğunda bir fiş dengesizliği hatası nedeniyle eliminasyon başarısız olur.                                              |
| Gider yönetimi  | [456882](https://fix.lcs.dynamics.com/Issue/Details/?bugId=456822)           | Yönetici olmayan kullanıcılar için, **proje kimliği** ve **gider kategorisi** gibi gider satırı sütunları için arama değerleri veri Bağlayıcısı çerçevesinde düzgün görüntülenmeyebilir. |
| Gider yönetimi  | [469300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469300)           | Satır özelliği varsayılan, gider kategorileri için gösterilmiyor.                                                                                                         |
| Gider yönetimi  | [469302](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469302)           | Gider tümleştirmesi, gider raporundan satır özelliğini içermelidir.                                                                                             |
| Faturalama           | [462499](https://fix.lcs.dynamics.com/Issue/Details/?bugId=462499)           | FD bileşiminin doğrulanmadığını belirten bir hata iletisi nedeniyle, proje fatura teklifleri deftere nakledilemediğinden.                                                    |
| Faturalama           | [470614](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470614)           | **Fatura** Ayrıntıları sayfasındaki hareketleri görüntüleyemez.                                                                                                              |
| Faturalama           | [480070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480070)           | Fatura teklif satırları silinebilir.                                                                                                                                  |
| Proje muhasebesi  | [470293](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470293)           | **Tahmin** menüsü öğeleri **Proje** listesi sayfasında görünmez.                                                                                                   |
| Proje muhasebesi  | [475873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475873)           | **Proje ekstresi**   > **hareketleri ve tahmini** açılamıyor.                                                                                                       |
| Proje muhasebesi  | [475879](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475879)           | **Muhasebeyi ayarla**, faturalanan proje hareketleri için etkin değildir.                                                                                                  |
| Proje muhasebesi  | [480962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480962)           | **Tümleştirme** günlüğü nakledildiğinde, **ProjCDSActualsImport** tablosunda hesap ayrıntıları dahil edilmez.                                                  |
| Proje muhasebesi  | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558)           | Kaynak atamasını kaldırıp yeniden eklediğinizde proje tahmin girişinin iki katına çıkar.                                                                            |
| Proje muhasebesi  | [502019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=502019)           | Bir proje kimliği bağlantısı seçilmesi CDS derin bağlantı URL'sini açmaz.                                                                                                         |
| Proje muhasebesi  | [505458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505458)           | CDS'deki görevin başlangıç tarihini güncelleştiremez.                                                                                                                           |
| Proje muhasebesi  | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041)           | Özelliğini etkinleştirmek, CDS tümleştirmesi olmadan birden çok sözleşme hattı yapılamaz.                                                                                   |

### <a name="regulatory-updates"></a>Mevzuat güncelleştirmeleri
Finans ve Operasyon uygulamalarında düzenleme güncelleştirmeleri hakkında bilgi için [Mevzuat güncelleştirmeleri](/dynamics365/finance/localizations/regulatory-updates) bölümüne göz atın. Ayrıca LCS'de oturum açıp planlı mevzuat güncelleştirmelerini sorun arama aracını kullanarak görüntüleyebilirsiniz. Sorun arama, ülkeye, özellik türüne ve sürümüne göre arama yapmanızı sağlar.


[!INCLUDE[footer-include](../includes/footer-banner.md)]