---
title: Ekim 2022'deki yenlikler - Kaynağı/stoğu tutulmayan öğeleri temel alan senaryolar için Project Operations
description: Bu makale, kaynak/stoğu tutulmayanları temel alan senaryolar için Microsoft Dynamics 365 Project Operations'ın Ekim 2022 sürümünde kullanılabilen kalite güncelleştirmeleri hakkında bilgi sağlar.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 392a12d6954c2390e5bad8e8e36cf58b7a1d0749
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806652"
---
# <a name="whats-new-october-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Ekim 2022'deki yenlikler - Kaynağı/stoğu tutulmayan öğeleri temel alan senaryolar için Project Operations

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Bu makale aşağıdaki Microsoft Dynamics 365 Project Operations bileşenleri ve sürümleri için geçerlidir:

- Dataverse ortamı sürümü 4.57.0.176'da Project Operations
- Dynamics 365 Finance ortamı sürümü 10.0.30'da proje yönetimi ve muhasebe

## <a name="features-included-in-this-release"></a>Bu sürümde yer alan özellikler

| Özellik alanı | Özellik adı | Daha fazla bilgi |
| --- | --- | --- |
| Proje Planlama ve İzleme | **Project Operations Harici Zamanlama**<br>Harici zamanlama modu, müşterilerin yerel Dataverse API'lerini kullanarak Project for the Web sınırları olmadan, iş kırılım yapıları (İKY'ler) ile ilgili varlıklar oluşturmasına güncelleştirmesine ve silmesine olanak sağlar. | [Harici Zamanlama](/dynamics365/project-operations/project-management/external-scheduling) |
| Dağıtım ve Yapılandırma | <p>**Müşterilerin dağıtım türünü seçmelerine izin ver**<br>Project Operations için ürün odaklı güncelleştirmeler (PDU), Çift yazma temel ve düzenleme çözümleri ortama yüklendiğinde, Project Operations Çift Yazma çözümünü otomatik olarak yüklemek için kullanılır.</p><p>Bu özellik, Proje parametrelerine yeni bir **Çözüm yükseltme davranışı** parametresi getirir. Bu parametre **yalnızca Lite** olarak ayarlandığında PUD'lar, Çift yazma temel ve düzenleme çözümleri ortama yüklenmiş olsa bile Project Operations Çift Yazma çözümünü otomatik olarak yüklemez. Bu davranış, satış siparişlerini finans ve operasyon uygulamalarına tümleştirmek için Çift yazma çözümü kullanmayı planlayan ancak Project Operations'ı Lite modunda (diğer bir deyişle finans ve operasyon uygulamalarına tümleştirmeden) kullanmak isteyen müşteriler için yararlıdır.</p> | |
| Fatura ve Fiyatlandırma | <p>**Tümleştirilmiş ortamlardaki gider faturalandıralınmamış satış işlemi için para birimi dönüştürmesi**<br>Finans ve operasyon uygulamalarıyla tümleştirilmiş Project Operations (yani, kaynak/stoğu tutulmayan dağıtım türünde) kullanan müşteriler için döviz kurları genellikle finans ve operasyon uygulamalarında yönetilir. Ancak, müşteri faturalandırıldığında bir gider kategrosinin "maliyetine" veya "Maliyet üzerinde kar payı" fiyat hesaplama yöntemi kullanılarak fiyatlandırılması gerekiyorsa, satış tutarının hesaplamak için kullanılan döviz tutarı, finans ve operasyon uygulamalarındaki döviz kurlarını değil Dataverse'deki döviz kurlarını kullanır.</p><p>Bu özellik, Proje parametrelerine yeni bir **Para birimi dönüştürme davranışı** parametresi getirir. Bu parametre **Geri dönüş ile genişletildi** olarak ayarlandığında, gider işlemlerindeki faturalanmamış satış tutarları finans ve operasyon uygulamalarındaki döviz kurları kullanılarak hesaplanır.</p> | |

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations çift yazma eşlemesi güncellemeleri

Bu sürümde Project Operations çift yazma eşlemeleri için güncelleştirme yoktur. Project Operations çift yazma eşlemelerinin geçerli listesi ve sürümleri için bkz. [Project Operations çift yazma eşleme sürümleri](../environment/resource-dual-write-maps.md).

Her zaman ortamınızda eşlemenin en son sürümünü çalıştırın ve Project Operations Dataverse çözümünüzü ve Finance çözümü sürümünüzü güncelleştirirken tüm ilgili tablo eşlemelerini etkinleştirin. Haritanın en son sürümü etkinleştirilmemişse bazı özellikler ve yetenekler doğru çalışmayabilir. Haritanın etkin sürümünü **çift yazma** sayfasındaki **sürüm** sütununda görebilirsiniz. Yeni bir harita sürümünü etkinleştirmek için **Tablo haritası sürümleri**'ni seçip en son sürümü seçin ve ardından seçili sürümü kaydedin. Kullanıma hazır tablo haritasını özelleştirdiyseniz, değişiklikleri yeniden uygulayın. Daha fazla bilgi için bkz. [Uygulama Yaşam Döngüsü Yönetimi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)

Eşlemeyi başlatırken bir sorunla karşılaşırsanız, Çift Yazma sorun giderme kılavuzunun [Eşlemelerde eksik tablo sütunu sorunları](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) bölümündeki yönergeleri izleyin.

## <a name="quality-updates"></a>Kalite güncelleştirmeleri

### <a name="project-operations-on-dataverse"></a>Dataverse üzerinde Project Operations

| Özellik alanı | Referans numarası | Kalite güncelleştirmeleri |
| --- | --- | --- |
| Fatura ve Fiyatlandırma | Kategori 2316317 | Sistem, borçlandırılabilir işlemleri olmayan fatura oluşturulmasını sağlar. |
| Fatura ve Fiyatlandırma | Kategori 2737300 | Forma erişilmeden önce **Müşteri** alanı kullanılabilirliğini doğrulayın. |
| Fatura ve Fiyatlandırma | Kategori 2744948 | Faturalandırma yöntemi için null bir denetim ekleyin. |
| Fatura ve Fiyatlandırma | Kategori 2763515 | Faturanın satış sözleşmesi eksik olduğunda null başvuru hatası tanıtıcısı. |
| Fatura ve Fiyatlandırma | Kategori 2844301 | Bir hata nedeniyle toplu fatura oluşturma işlemi başarısız oldu. |
| Fatura ve Fiyatlandırma | Kategori 2845869 | Kuruluş Hizmetinin hatalı depolanması. |
| Fatura ve Fiyatlandırma | Kategori 2853729 | Faturalama türü değiştirildiğinde Rol ve Fiyat ayrıntıları güncelleştirilir. |
| Fatura ve Fiyatlandırma | Kategori 2940350 | Fiili değerler fiyatlandırıldığı zaman, yalnızca etkin fiyat listeleri otomatik olarak girilmelidir. |
| Dağıtım ve Yapılandırma | Kategori 3001206 | msdyn\_replaylogheader varlığı, Müşteri Kuruluşlarının yükseltilmesini önlüyor. |
| Fırsat Yönetimi | Kategori 2755582 | Bölünmüş Fatura Kuralı Yardımcısı'nda null başvuru özel durumları tanıtıcısı. |
| Fırsat Yönetimi | Kategori 2761477 | Bölünmüş faturalama kullanıldığında, bir kilometre taşının silinmesi (başlık) sahipsiz kilometre taşları kalmasına neden olur. |
| Fırsat Yönetimi | Kategori 2767595 | Ana formda bir malzeme kullanım kaydı açıldığında, kayıt için ayrılabilir kaynak oturum açmış olan kullanıcı olarak değiştirilir. |
| Proje Planlama ve İzleme | Kategori 2790384 | Bekleyen OperationSet zaman aşımı çok kısa. |
| Proje Planlama ve İzleme | Kategori 2957840 | Görevler kaydedilemiyor ve sütunlar Tümleşik Project Operations'taki **Görevler** sayfasına eklenemiyor. |
| Kaynak Yönetimi | Kategori 2751560 | Kaynak Gereksinimde Tutarsız Tercih Edilen Kuruluş Birimleri. |
| Alt sözleşme | Kategori 2853245 | Bir sözleşme satırı zaten satıcı faturası satırına bağlı olduğunda Satıcı Fatura Satırı fiili değerleri eşleştirmesi doğrulama durumunu güncelleştirmez. |
| Alt sözleşme | Kategori 2907231 | Satıcı faturalarının işlem aşaması ilerlemesi devam edemiyor. |
| Zaman ve Gider | Kategori 2867363 | Kayıtlar onay için kuyruğa atıldıklarında Onay görünümü için Devamsızlıklar/Tatillere düşemez. |
| Zaman ve Gider | Kategori 2894405 | TESA: Kullanılmayan POC dizini uyum sorunlarına neden oluyor. |

### <a name="project-management-and-accounting-in-finance"></a>Finance'ta proje yönetimi ve muhasebe

Bu güncelleştirmeye dahil edilen hata düzeltmeleri hakkında bilgi için Microsoft Dynamics Lifecycle Services'te oturum açın ve [şu BB makalesini](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468) görüntüleyin.
