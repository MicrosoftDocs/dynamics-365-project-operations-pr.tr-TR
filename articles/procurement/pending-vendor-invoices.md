---
title: Bekleyen satıcı faturası kullanarak stoğu tutulmayan malzemeleri satın alma
description: Bu konu, beklemedeki satıcı faturalarının nasıl kaydedilecek açıklanmaktadır.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2ce9f244eaa549742aeb55024ca9ef4d82cde1bd4a5b9c7f8c762cf72e0da83f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009060"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a>Bekleyen satıcı faturası kullanarak stoğu tutulmayan malzemeleri satın alma

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Bir proje için bir şirket için stoklanmayan malzemeleri hazırlarken maliyetler projeye yönelik olarak hemen kaydedilebilir. 

Örneğin, Contoso Robotics ABD, donanım yenileme projesi gerçekleştiriyor ve yazılım lisanslarına ihtiyacı var. Bu lisanslar, üçüncü taraf bir satıcıdan tedarik ediliyor.  Dynamics 365 Finance Uygulamasını kullanarak borç hesapları memuru bir bekleyen satıcı fatura belgesini kaydeder ve donanım yenileme projesine doğrudan lisans maliyetlerini ekler. 

> [!IMPORTANT]
> Bu konu açıklanan işlevleri kullanmadan önce gerekli yapılandırmaları gözden geçirin ve uygulayın. Daha fazla bilgi için bkz. [Stoklanmayan malzemeleri ve bekleyen satıcı faturalarını etkinleştirme](configure-materials-nonstocked.md). 

## <a name="post-a-project-related-pending-vendor-invoice"></a>Projeyle ilgili bir bekleyen satıcı faturasını deftere nakletme 

Bekleyen satıcı faturaları, **bekleyen satıcı faturaları** sayfasında (**Borç hesapları** > **faturalar** > **bekleyen satıcı faturaları**) kaydedilebilir. Projeyle ilgili bekleyen satıcı faturasını deftere nakletmek için aşağıdaki adımları izleyin:

1. **Borç hesapları** > **faturalar**'a gidin ve **Yeni**'yi seçin. 
2. **Fatura hesabı** alanında bir satıcı seçin ve **numara** alanına satıcı fatura tanımlamasını girin.
3. Satıcı faturasına bir satır ekleyin ve **madde numarası** alanında, satıcıdan satın alınan Stoklanmayan maddeyi seçin. 

    > [!NOTE]
    > Bir satın alma kategorisine dayanan satıcı fatura satırları projeye karşı kaydedilemez. 
    
5. Satın alınan miktarı ekleyin. Sistem birim fiyatı, Stoklanmayan madde fiyatı yapılandırmasını temel alarak dolduracaktır. 
6. Satırdaki toplam tutarı ve diğer gerekli ayrıntıları doğrulayın.
7. Satır ayrıntılarında **Proje** sekmesinde, bu öğenin kaydedileceği projenin kimliğini seçin.
8. İsteğe bağlı olarak, aktivite numarasını seçin ve proje kategorisi ve satır özelliğini güncelleştirin.
9. Bekleyen satıcı faturasını deftere nakledin. Fatura deftere nakledildiğinde, sistem kayıtları:
    
    - Satıcı bakiye tutarı.
    - Satış Vergisi Tutarı.
    - Projeye yönelik maliyet, satın alma entegrasyonu hesabına kaydedilir.
    - Dataverse'de projenin fiili işlemi. Bu işlem [Project Operations tümleştirme günlüğü](../project-accounting/project-operations-integration-journal.md) kullanılarak daha sonra işlenir. Bu günlüğün deftere nakledilmesi, satın alma entegrasyonu hesabındaki tutarı proje maliyet hesabına taşır.
