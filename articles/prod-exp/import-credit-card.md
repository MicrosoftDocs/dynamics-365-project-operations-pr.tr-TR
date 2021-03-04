---
title: Kredi kartı işlemlerini içeri aktarma ve saklama
description: Bu konu, gider ile ilgili kredi kartı hareketlerinin nasıl alınacağını ve saklanacağını açıklar. Bu hareketler, yinelenen bir zamanlamada otomatik olarak alınmak üzere ayarlanabilir veya gerektiği şekilde el ile alınırlar.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 7bf75c13bb190c7b992aa516f1593d886dfa604d
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960451"
---
# <a name="import-and-maintain-credit-card-transactions"></a>Kredi kartı işlemlerini içeri aktarma ve saklama

Gider ile ilgili kredi kartı hareketleri, otomatik olarak yinelenen zamanlamayla içe alınacak şekilde ayarlanabilir. Alternatif olarak, hareketler gerektiği zaman el ile alınabilir. Kredi kartı hareketleri kredi kartı hareketleri veri varlığı aracılığıyla alınır.

Veri varlıkları hakkında daha fazla bilgi için bkz [Veri varlıkları](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).

## <a name="import-credit-card-transactions"></a>Kredi kartı hareketlerini alma

1. **Kredi kartı hareketleri** sayfasında, **Hareketleri içe aktar**'ı seçin. Veri yönetimini ilk defa açıyorsanız, devam edebilmeniz için sistemin veri varlıklarının listesini güncelleştirmesi gerekir.
2. **Ad** alanına, alma işine ait benzersiz bir açıklama girin.
3. **Kaynak veri biçimi** alanında, alınacak kredi kartı hareketlerinin bulunduğu dosyanın biçimini seçin.
4. **Yükle**'yi seçin ve ardından alınacak dosyayı bulup seçin.
5. Dosya karşıya yüklendikten sonra, kutucukta **Haritayı görüntüle** bağlantısını seçerek Kredi kartı hareketi dosyasının ve kredi kartı hareketleri veri varlığındaki sütunların eşlemesini doğrulayın. Eşleme hataları varsa veya eşlemeyi değiştirmek istiyorsanız, **Görselleştirme eşleme** sekmesinden veya **Eşleme ayrıntıları** sekmesinden eşleme ile ilgili değişiklikleri yapın.
6. Kredi kartı hareketlerini otomatikleştirmek için **Yinelenen veri işi oluştur** öğesini seçin. Daha sonra, kredi kartı hareketlerinin hangi sıklıkta alınması gerektiğini tanımlayan yineleme ayarını yapabilirsiniz. Tamamladığınızda, **Tamam** öğesini seçin.
7. Seçilen dosyayı hemen almak için **Al**'ı seçin.
8. Alma işlemi sırasında hatalar oluşursa, başarılı bir alma işleminin yapılmasını sağlamak için için düzeltmek zorunda olduğunuz hataları görmek üzere yürütme günlüğünü veya hazırlama verilerini görüntüleyebilirsiniz.

> [!NOTE]
> Birden çok dosya biçimi almanız gerekiyorsa, her biçim türü için ayrı alma işleri oluşturmanız gerekir.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>İşten ayrılan çalışanlar için kredi kartı hareketlerini yeniden atama

Çalışan kaydı sonlandırıldıktan sonra, çalışanın Active Directory Domain Services (AD DS) hesabı devre dışı bırakılır. Ancak, hala gider kaydedilmesi ve geri ödenmesi gereken etkin kredi kartı hareketleri olabilir. **Kredi kartı hareketleri** sayfasından, ilişkili çalışanın işten ayrıldığı durumda çalışana herhangi bir kredi kartı hareketi için yeniden atama yapabilirsiniz.

Bir veya daha fazla kredi kartı hareketi seçin ve sonra **Hareketleri yeniden ata**'yı seçin. Ardından, kredi kartı hareketleri atamak için başka bir çalışan seçebilirsiniz. Kredi kartı hareketleri yeniden atandığında, bir gider raporu için seçilebilir ve normal gider raporu yeniden ödeme sürecinde ödenmesi mümkündür.
