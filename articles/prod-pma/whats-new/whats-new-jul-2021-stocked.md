---
title: Stoklu/ürün tabanlı senaryolar için Project Operations'da Temmuz 2021'deki yenilikler veya değişiklikler
description: Bu konu stoklu/üretim tabanlı senaryolar için Project Operations'ın Temmuz 2021 sürümünde bulunan kalite güncelleştirmeleri hakkında bilgi sağlar.
author: andchoi
ms.date: 07/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: andchoi
ms.openlocfilehash: dadcf3e9fa8432fb66f76b7c2f0fdb98bc00511d93984ea98fa30b4fc03fa426
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992725"
---
# <a name="whats-new-or-changed-in-project-operations-july-2021-for-stockedproduction-based-scenarios"></a>Stoklu/ürün tabanlı senaryolar için Project Operations'da Temmuz 2021'deki yenilikler veya değişiklikler

_**Şunlar için Geçerlidir:** Stoklu/Ürün tabanlı senaryolar için Project Operations_

Bu konu aşağıdaki Dynamics 365 Project Operations bileşenleri ve sürümleri için geçerlidir:

- Dynamics 365 Finance uygulama ortamı sürüm 10.0.20'te proje yönetimi ve hesaplaması
 
### <a name="quality-updates"></a>Kalite güncelleştirmeleri
                                                                                                                                                                                  
| Özellik alanı                      | Referans numarası| Kalite güncelleştirmeleri                                                                                                                                                                          |
|-----------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Proje yönetimi ve muhasebe | [485394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485394) | Satınalma siparişinden kaynaklanan maliyet taahhüdü kayıtları, satınalma siparişi satınalma talebi çıkışından serbest bırakılır bırakılmaz temizleniyor.                                                                           |
| Proje yönetimi ve muhasebe | [529602](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529602) | Bütçe doğrulaması, bir satınalma talebinde iki kez gerçekleşiyor. Bu yineleme, talebin kapatılamaması ve karşılık gelen satınalma siparişinin oluşturulamaması anlamına geliyor.                                                                                                                        |
| Proje yönetimi ve muhasebe | [539439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539439) | **Faturalanacak yüzde** kuralı yuvarlama sorunu nedeniyle tamamlanamadı.                                                                              |
| Proje yönetimi ve muhasebe | [540023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540023) | İşlemi ayarladığınızda ve yüzde değeri ondalıklara sahip olduğunda, maliyet ve satış fiyatı doğru ayarlanmıyor.                                      |
| Proje yönetimi ve muhasebe | [540927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540927) | Muhasebe kaynağı gezgini, farklı etkinliklere sahip birden çok zaman çizelgesi satırı için tek bir zaman çizelgesi satırına ilişkin saatleri gösteriyor.                                      |
| Proje yönetimi ve muhasebe | [541471](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541471) | Kaydedilen görünümler ve zaman çizelgesi satırı ayrıntısı kişiselleştirmesi, bir zaman çizelgesini açmaya çalışırken sistemin her zaman listedeki ilk zaman çizelgesinin ayrıntılarını açmasına neden oluyor.  |
| Proje yönetimi ve muhasebe | [548677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548677) | Proje kök düğümü kayboluyor ve içeri aktarmadan sonra iş kırılım yapısı kayıtları siliniyor.                                                                                             |
| Proje yönetimi ve muhasebe | [548999](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548999) | Maddeler, madde gereksiniminden kısmen alındığında ve çıkışı yapıldığında, sistem yanlış bütçe tüketim bakiyesini güncelleştiriyor. |
| Proje yönetimi ve muhasebe | [550959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550959) | Proje tutma satınalma siparişleri **Toplamlar** bölmesinde veya **Bekleyen fatura** ızgarasında toplamları doğru göstermiyor.                                                                  |
| Proje yönetimi ve muhasebe | [554593](https://fix.lcs.dynamics.com/Issue/Details/?bugId=554593) | Stok kapatıldığında, proje madde maliyeti ayarlamaları kar ve zarar hesabı yerine bakiye hesabına naklediliyor.                                                            |
| Proje yönetimi ve muhasebe | [557394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557394) | Deftere nakledilen bir proje işlemi fişi ve tahmin fişi muhasebe para birimi olarak USD kullanıyor ancak tutar CAD eşdeğeri olarak gösteriliyor.              |
| Proje yönetimi ve muhasebe | [560140](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560140) | Madde gereksinimi ve satınalma siparişi içeren taahhüt edilen maliyetler, kısmi ürün girişi ve kısmi faturalama içeren satınalma siparişi fatura işleminde hatalı.       |
| Proje yönetimi ve muhasebe | [560567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560567) | Proje düzeltmesi, dolaylı maliyetlere sahip satış tutarını doğru şekilde güncelleştirmiyor.                                                                                    |
| Proje yönetimi ve muhasebe | [561137](https://fix.lcs.dynamics.com/Issue/Details/?bugId=561137) | **Zaman Çizelgesi** tablosunda **Çalışan/Kaynak** görünümüyle tanımlanmış bir ilişki eksik.                                                                                   |
| Proje yönetimi ve muhasebe | [563330](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563330) | Şirketlerarası zaman çizelgesinin açılan menüsünden seçtiğinizde **Etkinlik numarası alanı** doldurulamıyor.                                                                 |
| Proje yönetimi ve muhasebe | [563840](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563840) | Şu sayfalara kişiselleştirilmiş bir **Amaç** veya **Etkinlik açıklaması** alanı ekleyemiyorsunuz: **Projeyle deftere nakledilen işlem**, **Fatura teklifi oluşturma** veya **Fatura teklifi**.  |
| Proje yönetimi ve muhasebe | [566348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566348) | Veri yönetimi (**ProjSalesItemRequirementEntity**) kullanarak madde gereksinimleri oluşturduğunuzda yanlış teslim tarihi denetimi sağlanıyor.                                              |
| Proje yönetimi ve muhasebe | [566544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566544) | Finance'ta bir proje sözleşmesi kimliği seçtiğinizde, Project Operations tümleşik ortamı, mevcut proje sözleşmesini açmak yerine yeni bir kayıt oluşturmak için sayfayı açıyor.                                                                                                                 |
| Proje yönetimi ve muhasebe | [567300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567300) |  "@SYS4083080" ("Girilen değerlere karşılık gelen benzersiz bir Çalışan kaydı bulunamıyor") etiketi Danca'ya çevrilmedi.                                |
| Proje yönetimi ve muhasebe | [569901](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569901) | **Madde satış vergisi grubu** alanı bir fatura teklifinde düzenlenemiyor.                                                                               |
| Proje yönetimi ve muhasebe | [557049](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557049) | Taahhüt edilen maliyet, düşürülemez vergi tutarlarıyla artırılıyor.                                                                                                    |
| Proje yönetimi ve muhasebe | [565080](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565080) | Birden çok proje ve farklı mali boyutlara sahip bir şirketler arası zaman çizelgesinin deftere nakledilmesi genel muhasebede beklenmeyen değerler oluşturuyor.                             |
| Proje yönetimi ve muhasebe | [567962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567962) | Fatura teklifi satırları, **Hazırlama aşamasından içeri aktar** periyodik işleminin aynı anda çalıştırılan birden çok örneği nedeniyle çoğaltılıyor.                                      |
| Proje yönetimi ve muhasebe | [571339](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571339) | Alacak dekontu fatura teklifi deftere nakil işleminde hata olduğundan fişteki işlemler arasında dengesizlik oluyor.    |
| Proje yönetimi ve muhasebe | [573567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573567) | Tutulan bekleyen faturalar serbest bırakıldıktan sonra projede taahhüt edilen maliyetler yanlış hale geliyor.                                                                             |
| Proje yönetimi ve muhasebe | [573886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573886) | Vergi para birimi şirketin para biriminden farklı olduğunda proje satış siparişi için alacak dekontu oluşturamazsınız.                                      |
| Proje yönetimi ve muhasebe | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Bir sözleşmeyi sildiğinizde, müşteriyle ilişkilendirilmiş adres de siliniyor.                                                                                     |
| Proje yönetimi ve muhasebe | [585811](https://fix.lcs.dynamics.com/Issue/Details/?bugId=585811) | Negatif zaman işlemi düzeltmesinden kaynaklanan bir fatura teklifi deftere nakledilemiyor.                                                                    |
| Seyahat ve Gider                  | [532075](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532075) | Vergi gider raporlarında farklı hesaplanıyor.                                                                                                                  |
| Seyahat ve Gider                  | [546450](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546450) | **DB72_Expense.updateTrvExpTransProjTransId()** sürüm güncelleştirmesi **trvExpTrans.ReferenceDataAreaId** öğesinin yeni numara sırası oluşturmasına izin vermiyor.                    |
| Seyahat ve Gider                  | [568805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568805) | Dosyalanan tutar zorunlu alanla birlikte gösterilemiyor.                                                                                                             |
| Seyahat ve Gider                  | [568831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568831) | Gider Yeniden Tasarlandı kullanıcı arabirimi kullanarak gider raporuna gider raporuna gider ekleme performansındaki iyileştirmeler.                                                            |
| Seyahat ve Gider                  | [570790](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570790) | Deftere nakledilen gider raporlarını silebilirsiniz.                                                                                           |
| Seyahat ve Gider                  | [571317](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571317) | Gider ilkesi iletisi birden çok kez görüntüleniyoe.                                                                                                       |
| Seyahat ve Gider                  | [573969](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573969) | **Ödeme yöntemi** alanı **Yeni gider** bölmesine dahil edildi.                                                                                                      |
| Seyahat ve Gider                  | [523557](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523557) | İş akışı bulunamazsa, **Gider belgesi durumunu Sıfırla** aracı gider raporu durumunu **Taslak** olarak sıfırlamalıdır. 

### <a name="regulatory-updates"></a>Mevzuat güncelleştirmeleri
Finance and Operations uygulamalara yönelik mevzuat güncelleştirmeleri hakkında bilgi için bkz. [Mevzuat güncelleştirmeleri](/dynamics365/finance/localizations/regulatory-updates). Ayrıca, Lifecycle Services'e (LCS) giriş yapabilir ve Sorun arama aracını kullanarak planlanan düzenleyici güncelleştirmeleri görüntüleyebilirsiniz. Sorun arama, ülkeye, özellik türüne ve sürümüne göre arama yapmanızı sağlar.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
