---
title: "Ekim 2022'deki Yenilikler: Project Operations lite dağıtımı"
description: Bu makale, Microsoft Dynamics 365 Project Operations lite dağıtımının Ekim 2022 sürümünde kullanılabilen kalite güncelleştirmeleri hakkında bilgi sağlar.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: b6975e1f8645721fc03239b355b117eb664785f0
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806657"
---
# <a name="whats-new-october-2022---project-operations-lite-deployment"></a>Ekim 2022'deki Yenilikler: Project Operations lite dağıtımı

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Bu makale aşağıdaki Microsoft Dynamics 365 Project Operations bileşenleri ve sürümleri için geçerlidir:

- Dataverse ortamı sürümü 4.57.0.176'da Project Operations

## <a name="features-included-in-this-release"></a>Bu sürümde yer alan özellikler

| Özellik alanı | Özellik adı | Daha fazla bilgi |
| --- | --- | --- |
| Proje Planlama ve İzleme | **Project Operations Harici Zamanlama**<br>Harici zamanlama modu, müşterilerin yerel Dataverse API'lerini kullanarak Project for the Web sınırları olmadan, iş kırılım yapıları (İKY'ler) ile ilgili varlıklar oluşturmasına güncelleştirmesine ve silmesine olanak sağlar. | [Harici Zamanlama](/dynamics365/project-operations/project-management/external-scheduling) |
| Dağıtım ve Yapılandırma | <p>**Müşterilerin dağıtım türünü seçmelerine izin ver**<br>Project Operations için ürün odaklı güncelleştirmeler (PDU), Çift yazma temel ve düzenleme çözümleri ortama yüklendiğinde, Project Operations Çift Yazma çözümünü otomatik olarak yüklemek için kullanılır.</p><p>Bu özellik, Proje parametrelerine yeni bir **Çözüm yükseltme davranışı** parametresi getirir. Bu parametre **yalnızca Lite** olarak ayarlandığında PUD'lar, Çift yazma temel ve düzenleme çözümleri ortama yüklenmiş olsa bile Project Operations Çift Yazma çözümünü otomatik olarak yüklemez. Bu davranış, satış siparişlerini finans ve operasyon uygulamalarına tümleştirmek için Çift yazma çözümü kullanmayı planlayan ancak Project Operations'ı Lite modunda (diğer bir deyişle finans ve operasyon uygulamalarına tümleştirmeden) kullanmak isteyen müşteriler için yararlıdır.</p> | |

## <a name="quality-updates"></a>Kalite güncelleştirmeleri

| Özellik alanı | Referans numarası | Kalite güncelleştirmeleri |
| --- | --- | --- |
| Fatura ve Fiyatlandırma | Kategori 2316317 | Sistem, borçlandırılabilir işlemleri olmayan fatura oluşturulmasını sağlar. |
| Fatura ve Fiyatlandırma | Kategori 2737300 | Forma erişilmeden önce Müşteri alanı kullanılabilirliğini doğrulayın. |
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
| Kaynak Yönetimi | Kategori 2751560 | Kaynak Gereksinimde Tutarsız Tercih Edilen Kuruluş Birimleri. |
| Alt sözleşme | Kategori 2907231 | Satıcı faturalarının işlem aşaması ilerlemesi devam edemiyor. |
| Zaman ve Gider | Kategori 2867363 | Kayıtlar onay için kuyruğa atıldıklarında Onay görünümü için Devamsızlıklar/Tatillere düşemez. |
| Zaman ve Gider | Kategori 2894405 | TESA: Kullanılmayan POC dizini uyum sorunlarına neden oluyor. |
