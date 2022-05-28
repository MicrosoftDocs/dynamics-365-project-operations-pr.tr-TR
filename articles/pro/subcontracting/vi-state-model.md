---
title: Satıcı faturasında durum geçişleri
description: Bu konuda, Microsoft Dynamics 365 Project Operations'taki bir satıcı faturasında durum geçişleri açıklanmaktadır.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7efb52621ee325d5025dfad0b45218d1fe20a063
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584712"
---
# <a name="state-transitions-on-a-vendor-invoice"></a>Satıcı faturasında durum geçişleri

[!include [banner](../../includes/dataverse-preview.md)]

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Bu konuda, Microsoft Dynamics 365 Project Operations'taki bir satıcı faturasında durum geçişleri açıklanmaktadır. Şu durumlar kullanılır: **Taslak**, **İncelemede**, **Onaylandı**, **Beklemede** ve **İptal edildi**.

Aşağıdaki çizimlerde bu geçişler gösterilmiştir:

![Alt sözleşme durumu geçiş modeli.](../media/VI_State_Model.jpg)

Aşağıdaki tablo, Project Operations'taki bir satıcı faturası yaşam döngüsünde her durumun neyi temsil ettiğini açıklar.

| State | Description | İzin verilen geçişler |
| --- | --- | --- |
| Taslak | Bu durum, satıcı faturasının başlangıç durumudur. Satırlar ve fiyatlandırma değişikliğe tabidir. Bu durumdaki bir satıcı faturası düzenlenemez veya silinemez. | Devam ediyor |
| İncelemede | Bu durum, satıcı faturasının işleme durumunu temsil eder. En az bir satıcı faturası satırı, **Devam ediyor** doğrulama durumu içerir. | Onaylandı, Beklemede |
| Onaylandı | Bu durum, uygulamanın her satıcı faturası satırı için maliyet gerçek değerlerini oluşturduğu, satıcı faturasının aşamasını temsil eder. Satıcı faturası satırlarıyla eşleşen bağlantılı maliyet gerçek değerleri ters çevrildi ve bu satıcı faturası satırlarındaki maliyet gerçek değerleri ile değiştirildi. Bu durumdaki bir satıcı faturası düzenlenemez veya silinemez. Onaylanan bir satıcı faturasını iptal etmek için **İptal** düğmesini kullanabilirsiniz. İptal eylemi, Onayla eyleminin etkisini tersine çevirir. | İptal edildi |
| Beklemede | <p>Bu durum, fatura veya satıcının durumundaki bir sorun nedeniyle satıcı faturasının taşınamadığı bir satıcı faturası aşamasını temsil eder. Bu durumdaki bir satıcı faturası onaylanamaz, iptal edilemez, düzenlenemez veya silinemez.</p><p>Satıcı faturasını **Taslak** veya **İncelemede** durumuna taşımak için Yeniden aç eylemini kullanabilirsiniz. Satıcı faturasındaki en az bir satırının doğrulama durumu **Devam ediyor** veya **Tamamlandı** ise satıcı faturası **İncelemede** durumunda yenden açılır. Satıcı faturasındaki tüm satırların doğrulama durumu **Başlatılmadı** ise satıcı faturası **Taslak** durumunda yeniden açılır.</p> | Taslak, İncelemede |
| İptal edildi | Bu durum, alt sözleşmedeki kaynakların gerçek malzeme teslimi ve/veya çalışması artık gerekmediği bir taşeron aşamasını temsil eder. Bu durumdaki bir alt sözleşme, kaynak ve malzemeler için proje gereksinimlerini tahmin etmek personel sağlamak amacıyla kullanılamaz ve ayrıca bir projedeki zaman, gider ve malzeme kullanımına atıfta bulunamaz. Bu durumdaki bir alt sözleşme düzenlenemez veya silinemez. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
