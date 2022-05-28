---
title: Bekleyen bir satıcı faturası kullanarak stoğu tutulmayan malzemeleri veya tedarik kategorilerini satın alma
description: Bu konu, beklemedeki satıcı faturalarının nasıl kaydedilecek açıklanmaktadır.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e81f7a54e304ae6fc9a9f2637124579b6e7b54e9
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/18/2022
ms.locfileid: "8612681"
---
# <a name="purchase-non-stocked-materials-or-procurement-categories-using-a-pending-vendor-invoice"></a>Bekleyen bir satıcı faturası kullanarak stoğu tutulmayan malzemeleri veya tedarik kategorilerini satın alma

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Şirket bir proje için stoğu tutulmayan malzeme veya tedarik kategorileri tedarik ettiğinden maliyetler projeye karşılık anında kaydedilebilir. 

Örneğin, Contoso Robotics ABD bir donanım yenileme projesi yürütmektedir ve yazılım lisanlarına ihtiyacı vardır. Bu lisanslar, üçüncü taraf bir satıcıdan tedarik ediliyor.  Borç hesapları memuru, Dynamics 365 Finance kullanarak bekleyen bir satıcı faturası belgesi kaydeder ve lisans maliyetlerini doğrudan ekipman yenileme projesiyle ilişkilendirir. 

> [!IMPORTANT]
> Bu konu açıklanan işlevleri kullanmadan önce gerekli yapılandırmaları gözden geçirin ve uygulayın. Daha fazla bilgi için bkz. [Stoğu tutulmayan malzemeleri ve bekleyen satıcı faturalarını etkinleştirme](configure-materials-nonstocked.md) ve [Tedarik kategorilerini proje satın alma siparişlerinde ve bekleyen satıcı faturalarında kullanma](configure-procurement-categories.md)

## <a name="post-a-project-related-pending-vendor-invoice"></a>Projeyle ilgili bir bekleyen satıcı faturasını deftere nakletme 

Bekleyen satıcı faturaları, **bekleyen satıcı faturaları** sayfasında (**Borç hesapları** > **faturalar** > **bekleyen satıcı faturaları**) kaydedilebilir. Projeyle ilgili bekleyen satıcı faturasını deftere nakletmek için aşağıdaki adımları izleyin:

1. **Borç hesapları** > **Faturalar**'a gidin ve **Yeni**'yi seçin. 
1. **Fatura hesabı** alanında, satıcı seçin ve ardından **Sayı** alanında satıcı faturası tanımlamasını girin.
1. Satıcı faturasına satır ekleyin ve ardından **Madde numarası** alanında satıcıdan satın alınmış stoğu tutulmayan maddeyi seçin. Alternatif olarak, **Tedarik kategorisi** alanında satıcıdan satın alınmış tedarik kategorisini seçin.   
1. Satın alınmış miktarı ekleyin. Sistem, stoğu tutulmayan madde fiyatı yapılandırmasına göre birim fiyatı doldurur. 
1. Satırdaki toplam tutarı ve diğer gerekli ayrıntıları doğrulayın.
1. Satır ayrıntılarında, **Proje** sekmesinde bu maddenin kaydedileceği projenin kimliğini seçin.
1. İsteğe bağlı: Etkinlik numarasını seçin ve proje kategorisi ve satır özelliğini güncelleştirin.
1. Bekleyen satıcı faturasını nakledin. Fatura nakledildiğinde sistem aşağıdaki bilgileri kaydeder:
    
    - Satıcı bakiye tutarı.
    - Satış Vergisi Tutarı.
    - Projeye yönelik maliyet, satın alma entegrasyonu hesabına kaydedilir.
    - Dataverse'deki proje filli maliyeti işlemi.  Bu işlem [Project Operations tümleştirme günlüğü](../project-accounting/project-operations-integration-journal.md) kullanılarak daha sonra işlenir. Bu günlüğün deftere nakledilmesi, satın alma entegrasyonu hesabındaki tutarı proje maliyet hesabına taşır. 
    - Zaman ve malzeme faturalama yöntemi kullanılarak proje müşterisine faturalanan satınalmalar. Ayrıca, Dataverse'de satınalmalar için faturalanmamış satış işlemleri oluşturulur. Dataverse'deki ürün fiyat listesi faturalandırılmamış satış işleminin satış fiyatları ve tutarları için kullanılır.
