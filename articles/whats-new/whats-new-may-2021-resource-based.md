---
title: Mayıs 2021 - Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations konusundaki yenilikler
description: Bu makale, kaynak/stoğu tutulmayan öğeleri temel alan senaryolar için Project Operations Mayıs 2021 sürümünde yer alan kalite güncelleştirmeleri hakkında bilgi sağlar.
author: sigitac
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 425b0eb78b5f03d4b0da9a792d6e33fc96adf060
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930434"
---
# <a name="whats-new-may-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Mayıs 2021 - Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations konusundaki yenilikler

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Bu makale aşağıdaki Dynamics 365 Project Operations bileşenleri ve sürümleri için geçerlidir:

- Dynamics 365 Dataverse ortamı 4.10.0.186 sürümünde Project Operations
- Finans ve Operasyon uygulamaları ortamları sürüm 10.0.18'de proje yönetimi ve muhasebe

## <a name="features-included-in-this-release"></a>Bu sürümde yer alan özellikler

Bu sürümde aşağıdaki özellikler yer almaktadır:

- [Zamanlama modları ](../project-management/scheduling-modes.md) :  Proje yöneticileri bir projenin sabit süre, sabit çalışma veya sabit birimler zamanlama modu kullanılarak yönetilmesi gerekip gerekmediğini tanımlayabilir.
- [Mesafe oranı katmanlarını kullanarak mesafeyi ayarlama](../expense/set-up-mileage.md) : Çalışan gider raporları için mesafe oranı katmanlarını güncelleştirin.

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations çift yazma eşlemesi güncellemeleri

Aşağıdaki listede Project Operations 2021 Mayıs Sürümünde değiştirilmiş veya eklenmiş olan çift yazılır eşlemeler gösterilmektedir.

| Varlık eşlemesi | Güncellenmiş sürüm | Açıklamalar |
| --- | --- | --- |
| Proje Finansmanı kaynağı (msdyn\_projectcontractsplitbillingrules) | 1.0.0.2 | Proje sözleşmesi müşteri ödeme koşullarını eşitleme. |
| Proje faturası teklif performansı V2 (faturalar) | 1.0.0.3 | Proforma fatura ödeme koşullarını eşitleme. |
| Project Operations tümleştirme projesi satıcı faturası satırı dışa aktarma varlığı (msdyn\_projectvendorinvoicelines) | 1.0.0.1 | Kalite güncelleştirmeleri |
| Projeler V2 (msdyn\_projects) | 1.0.0.2 | Kalite güncelleştirmeleri |

Her zaman ortamınızda eşlemenin en son sürümünü çalıştırmalı ve Project Operations Dataverse çözümünüzü ve Finans ve Operasyon uygulamaları çözümü sürümünüzü güncelleştirirken tüm ilgili tablo eşlemelerini etkinleştirmelisiniz. Haritanın en son sürümü etkinleştirilmemişse belirli özellikler ve yetenekler doğru çalışmayabilir. Haritanın etkin sürümünü  **çift yazma** sayfasındaki  **Sürüm**  sütununda görebilirsiniz. Yeni bir harita sürümünü etkinleştirmek için **Tablo haritası sürümleri**'ni seçip en son sürümü seçin ve ardından seçili sürümü kaydedin. Kutulu bir tablo haritasını özelleştirdiyseniz, değişiklikleri yeniden uygulayın. Daha fazla bilgi için bkz. [Uygulama Yaşam Döngüsü Yönetimi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)

Eşlemeyi başlatma ile ilgili bir sorunla karşılaşırsanız, çift yazma sorun giderme kılavuzunun [Haritalarda eksik tablo sütunları sorunu](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) başlıklı yönergeleri izleyin.

## <a name="quality-updates"></a>Kalite güncelleştirmeleri

### <a name="project-operations-on-dataverse"></a>Dataverse üzerinde Project Operations

| **Özellik alanı** | **Referans numarası** | **Kalite güncelleştirmeleri** |
| --- | --- | --- |
| Fatura ve Fiyatlandırma | 2227635 | **Birim grubu** ve **Birim** alanlarındaki değerler, **Malzeme Tahminleri** ızgarasındaki üründen varsayılan olarak alınır. |
| Fatura ve Fiyatlandırma | 2234127 | **Görev kimliği** alanı artık bir satıcı faturası deftere nakledildiğinde Dataverse proje fiili değerine doğru şekilde tümleştirilir. |
| Fatura ve Fiyatlandırma | 2235564 | Günlük satırının kaydedilmesi, günlük satırı girişinde görüntülenen para biriminin, kaydettikten sonra varsayılan para birimiyle eşleşmesini sağlar. |
| Fatura ve Fiyatlandırma | 2246671 | Faturalama sırasında bir hareketi borçlandırılamayan hale getirme, özgün faturalanmayan satış kaydını tersine çevirir ve borçlandırılamayan olarak yeni bir faturalandırılmamış satış kaydı oluşturur. |
| Fatura ve Fiyatlandırma | 2264042 | Çalışma ortamında geçerli olmayan bir fatura düzeltme ayrıntısı varsa, geçerli fatura düzeltmesi engellenmemelidir. |
| Fatura ve Fiyatlandırma | 2146367 | Proje fatura başlığı çift yazma eşlemesi, ödeme şartlarını içerecek şekilde genişletilmiştir. |
|   Fırsat yönetimi | 2086888 | Bir teklifi, borçlandırılabilir rollere ve yeni kopyalanan bir teklifin kategorilerine kopyalamadan önce devre dışı bırakılan roller ve kategoriler eklemeyin. |
|   Fırsat yönetimi | 2234376 | Salt okunur alanlar, **Malzeme Tahminleri** ızgarasında soluk görünür. |
|   Fırsat yönetimi | 2238337 | Bir ilgili kişiye dayanan teklif, bir proje fiyat listesiyle ilişkilendirilmemiş olsa da kaydedilebilir. |
|   Fırsat yönetimi | 2239810 | Bir teklifin kayıp olarak kapatılması, ilişkili projeyi de kapatır ve tüm rezervasyonları iptal eder. |
| Proje Planlama ve İzleme | 2099559 | **Proje görevleri** ızgarası açılmadan önce sistem durumu için daha fazla doğrulama eklendi. |
| Proje Planlama ve İzleme | 2178987 | **Proje** sayfasında **Sonraki Aşama** seçilirken ortaya çıkan geçici bir hata düzeltildi. |
| Kaynak Yönetimi | 2224817 | Ayırmaları uzatmayı varsayılan olarak doğru ayırma durumuna ayarlama işlevselliği. |
| Zaman girişi | 2202476 | **Zaman girişi** sayfası artık tepki ızgarası denetimini kullanır ve ızgaranın yanlış hizalanması gibi sorunları giderir. |
| Zaman girişi | 2223377 | Zaman girişi, kullanılabilirlik açısından karışıklık oluşmasını önlemek için **Ayrılabilir Kaynak** sayfasındaki **İlgili** bölümden gizlenir. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Dynamics 365 Finance'ta proje yönetimi ve muhasebe

| Özellik alanı | Referans numarası | Kalite güncelleştirmeleri |
| --- | --- | --- |
| Proje yönetimi ve muhasebe | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Project Operations'ta Kaynağa dayalı senaryolar: Bir tümleştirme hatası nedeniyle bir teklifi dönüştüremezsiniz. |
| Proje yönetimi ve muhasebe | [546604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546604) | Project Operations: Çakışan sözleşme satırları ve hareket türleri kontrolü nedeniyle bir sözleşme satırını bir Proje kimliğiyle ilişkilendirmeyi denediğinizde bir hata iletisi görüntülenir. |
| Proje yönetimi ve muhasebe | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity**, finansman kaynağı fatura adresini farklı bir müşteriden ayarlar. |
| Seyahat ve Gider | [480451](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480451) | Mesafe ayarı ile ilgili bir deftere nakil hatası gerçekleşebilir. |
| Seyahat ve Gider | [522084](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522084) | Yabancı para birimi masraf işlemleri için **Kişisel olarak ayır** işlevi çalışmıyor. |
| Seyahat ve Gider | [523938](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523938) | Yetkililer kaynak olarak ayarlanmış olsa da, gider kategorisi açılan değerleri yetkililer için yanlış kategorileri gösteriyor. |
| Seyahat ve Gider | [539266](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539266) | **Kaynak/Kategori doğrulama** hatası nedeniyle şirketlerarası gider raporunu kaydedemezsiniz. |
| Seyahat ve Gider | [532610](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532610) | Gider raporu deftere nakilde yanlış mesafe oranı hesaplaması satırları Böl. |
| Seyahat ve Gider | [537404](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537404) | Satış vergisi dahil olduğunda şirketlerarası gider raporunu deftere nakletmeyen ve ödeme yöntemindeki mahsup hesap türü **çalışandır**. |
| Seyahat ve Gider | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | Geri alınan **TrvRequisitionLine** veri varlığı ve benzersiz dizin ilişkilidir. |
| Seyahat ve Gider | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | Gider raporu, kaynak belge satır oluşturmayı ve güncelleştirmesini destekler. |
| Seyahat ve Gider | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | Satış vergisi, hedef tüzel kişiliğine nakledildiyse şirketlerarası senaryoda yanlış alt muhasebe günlüğü gösteriliyordur. |
| Seyahat ve Gider | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | Project Operations: Gider tahminleri Dataverse'den silindiğinde Finans'tan silinmez. |
| Seyahat ve Gider | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Bir masraf kategorisi, proje dışı bir kategorideyse **Giderler** sayfasında seçilen mali boyutlar, gider raporuna kopyalanmaz. |
