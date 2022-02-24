---
title: Kredi kartı tümleştirmesini ayarlama
description: Bu konu, giderle ilgili kredi kartı hareketleriyle çalışma konusunda bilgi vermektedir.
author: suvaidya
manager: AnnBe
ms.date: 04/02/2021
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
ms.openlocfilehash: 72ff98f5985af4362cde3c9914e0d20247f1f09a
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866707"
---
# <a name="set-up-credit-card-integration"></a>Kredi kartı tümleştirmesini ayarlama

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Gider ile ilgili kredi kartı hareketleri, otomatik olarak yinelenen zamanlamayla içe alınacak şekilde ayarlanabilir. Alternatif olarak, hareketler gerektiği zaman el ile alınabilir. Kredi kartı hareketleri, kredi kartı hareketleri veri varlığı aracılığıyla içe aktarılır.

## <a name="import-credit-card-transactions"></a>Kredi kartı hareketlerini alma

Kredi kartı hareketlerini içe aktarmak için şu adımları izleyin:

1. **Kredi kartı hareketleri** sayfasında, **Hareketleri içe aktar**'ı seçin. Veri yönetimini ilk defa açıyorsanız, devam edebilmeniz için sistemin veri varlıklarının listesini güncelleştirmesi gerekir.
2. **Ad** alanına, içe aktarma işi için benzersiz bir açıklama girin.
3. **Kaynak veri biçimi** alanında, alınacak kredi kartı hareketlerinin bulunduğu dosyanın biçimini seçin.
4. **Yükle**'yi seçin ve ardından alınacak dosyayı bulup seçin.
5. Dosya karşıya yüklendikten sonra, kutucukta **Haritayı görüntüle** bağlantısını seçerek kredi kartı hareketi dosyasının ve kredi kartı hareketleri veri varlığındaki sütunların eşlemesini doğrulayın. Eşleme hataları varsa veya eşlemeyi değiştirmek istiyorsanız, **Görselleştirme eşleme** sekmesinden veya **Eşleme ayrıntıları** sekmesinden eşleme ile ilgili değişiklikleri yapın.
6. Kredi kartı hareketlerini otomatikleştirmek için **Yinelenen veri işi oluştur** öğesini seçin. Daha sonra, kredi kartı hareketlerinin hangi sıklıkta alınması gerektiğini tanımlayan yineleme ayarını yapabilirsiniz. Tamamladığınızda, **Tamam** öğesini seçin.
7. Seçilen dosyayı hemen almak için **Al**'ı seçin.
8. İçeri aktarma işlemi sırasında hatalar oluşursa başarılı bir içe aktarma işlemini sağlamak için düzeltmek zorunda olduğunuz hataları görmek üzere yürütme günlüğü veya hazırlama verilerini görüntüleyebilirsiniz.

> [!NOTE]
> Birden çok dosya biçimini içeri aktarmanız gerekiyorsa her biçim türü için ayrı bir içe aktarma işi oluşturmanız gerekir.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>İşten ayrılan çalışanlar için kredi kartı hareketlerini yeniden atama

Çalışan kaydı sonlandırıldıktan sonra, çalışanın Active Directory Domain Services (AD DS) hesabı devre dışı bırakılır. Ancak, hala gider kaydedilmesi ve geri ödenmesi gereken etkin kredi kartı hareketleri olabilir. **Kredi kartı hareketleri** sayfasında, çalışanın işine son verildiği kredi kartı hareketleri için ilgili çalışanı yeniden atayabilirsiniz.

Bir veya daha fazla kredi kartı hareketi seçin ve sonra **Hareketleri yeniden ata**'yı seçin. Ardından, kredi kartı hareketleri atamak için başka bir çalışan seçebilirsiniz. Kredi kartı hareketleri yeniden atandığında, bir gider raporu için seçilebilir ve normal gider raporu yeniden ödeme sürecinde ödenmesi mümkündür.

## <a name="delete-credit-card-transactions"></a>Kredi kartı hareketlerini silme 

Bazı durumlarda, kredi kartı hareketleri içe aktarıldıktan sonra bazı hareketlerin silinmesi gerekebilir. Bunun nedeni, hareketlerin yinelenmesi veya verilerin doğru olmaması olabilir. Yöneticiler, **"Kredi kartı hareketlerini sil"** özelliğini kullanarak bir gider raporuna **iliştirilmemiş** kredi kartı hareketlerini seçebilir ve silebilir. 

1. **Dönemsel görevler** > **Kredi kartı hareketlerini sil**'e gidin.
2. **Filtre**'yi seçin ve dahil edilecek kayıtları tanımlamak için gerekli bilgileri girin.
3. Kayıtları silmek için **Tamam**'ı seçin. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
