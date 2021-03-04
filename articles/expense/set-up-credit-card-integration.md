---
title: Kredi kartı tümleştirmesini ayarlama
description: Bu konu, gider ile ilgili kredi kartı hareketlerinin nasıl alınacağını ve saklanacağını açıklar.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: e0004f9096ea8a03745dbfce35fe0d32d3d707f6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120882"
---
# <a name="set-up-credit-card-integration"></a>Kredi kartı tümleştirmesini ayarlama

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Gider ile ilgili kredi kartı hareketleri, otomatik olarak yinelenen zamanlamayla içe alınacak şekilde ayarlanabilir. Alternatif olarak, hareketler gerektiği zaman el ile alınabilir. Kredi kartı hareketleri kredi kartı hareketleri veri varlığı aracılığıyla alınır.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]