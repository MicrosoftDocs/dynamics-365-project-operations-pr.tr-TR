---
title: Proje kaynak zamanlaması performansı
description: Bu konu, çok sayıda proje için kaynak zamanlama performansının nasıl artıracağı hakkında bilgi sağlar.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 34c31570778f9b64c23387112cf56fa1139cd0fd
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289033"
---
# <a name="project-resource-scheduling-performance"></a>Proje kaynak zamanlaması performansı

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


Kaynak zamanlamalamayla ilgili performans konuları, proje sayısı binlerce'a ulaştığında oluşabilir. Kaynak zamanlama performansını iyileştirmek için, kullanıcıların kaynak kullanılabilirlik formunu başlatmak için gereken zamanı azaltmaya olanak sağlayan bir özellik bulunmaktadır. Bu, özellikle kaynak kapasitesi toplama eşitleme işlemini kaldırır ve kaynak aramasını hızlandırmak için **resprojectresource** tablosunu kullanır. **Resrollup** tablosunun artık kullanılmayacağını unutmayın.

> [!IMPORTANT]
> Kaynak kapasitesi toplama ya da **ResProjectResource** tablosundaki bir bağımlılık varsa bu özelliği kullanmayın.

## <a name="enable-resource-scheduling-performance-enhancement"></a>Kaynak zamanlama performans geliştirmesini etkinleştir
Kaynak zamanlama performans geliştirmesini etkinleştirmek için aşağıdaki adımları izleyin.

1. **Özellik yönetimi** > **tümü**'ne gidin ve özellik listesinde, **Proje kaynak zamanlaması performans geliştirmesi özelliğini etkinleştir** seçeneğini belirleyin.
2. **Şİmdi Etkinleştir**'i seçin.

> [!NOTE]
> Bu özelliği listede bulamazsanız, Listeyi yenilemek için **Güncelleştirmeleri denetle**'ii seçin.

3. Tarayıcınızı yenileyin ve ardından **Proje yönetimi ve muhasebe** > **dönemsel** > **Proje kaynakları** > **Tüm şirketlerdeki kaynak takvimleri kapasitesini eşitleyin**'e gidin.
4. Önceki verileri kaldırmak için **varolan kapasite kayıtlarını** **Evet** 'e ayarlayın. Artımlı veri oluşturmak istiyorsanız, bunu **Hayır** olarak ayarlayın.
5. **Dönem kodu** alanında, verilerin oluşturulması gereken dönemi seçin. Bir dönem kodu seçerseniz, bir başlangıç ve bitiş tarihinin tanımlanıp tanımlanmaması gerekmez.
6. **Dönem kodu** alanını boş bırakırsanız, veri oluşturmak için belirli başlangıç ve bitiş tarihlerini seçin.
7. **Tamam**'ı seçin.

 > [!NOTE]
 > Bu, genel verileri ortamınızdaki tüm şirketler arasında **ResCalendarCapacity** tablosuna dağıtır, bu nedenle toplu işlemin yalnızca bir yasal varlıkta çalıştırılması yeterlidir. Bu toplu işlemdeki veriler, kaynak kapasitesini ilişkilendirilmiş takvimle hesaplamak için gereklidir.

8. **Proje yönetimi ve hesap** > **dönemsel** > **Proje kaynakları** > **Proje kaynaklarını tüm şirketlere göre doldurun**'a gidin ve **Tamam**'ı seçin. Bu, **resprojectresource**, **rescalendardatetimerange** ve **ResEffectiveDateTimeRange** tablolarındaki genel veriler için veri yükseltme komut dosyası. **PSAPRojSchedRole.RootActivity** alanının değerleri de güncelleştirilir. Bu çalıştırılmadıysa, kaynak zamanlama işlemlerini yürütmeye çalıştığınızda bir uyarı alırsınız.
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a>Kaynak zamanlama performans geliştirmesini kapatın

1. **Özellik yönetimi** > **tümü**'ne gidin ve **Proje kaynak zamanlaması performans geliştirmesi özelliğini etkinleştir** seçeneğini arayın.
2. Özelliğini seçin ve **devre dışı bırak** düğmesini seçin.
3. Tarayıcınızı yenileyin.
4. **Proje yönetimi ve muhasebe** > **Dönemlik** > **Kapasite eşitlemesi** > **Kaynağın kapasite toplamalarını eşitle** seçeneklerini belirleyin.
5. **Kapasite toplama eşitleme** sayfasında, önceki verileri kaldırmak için **varolan kapasite kayıtlarını** **Evet** olarak ayarlayın. Artımlı veri oluşturmak istiyorsanız, bunu **Hayır** olarak ayarlayın.
6. **Dönem kodu** alanında, verilerin oluşturulması gereken dönemi seçin. Bir dönem kodu seçerseniz, bir başlangıç ve bitiş tarihinin tanımlanıp tanımlanmaması gerekmez.
7. **Dönem kodu** alanını boş bırakırsanız, veri oluşturmak için belirli başlangıç ve bitiş tarihlerini seçin.
8. **Tamam**'ı seçin.

> [!NOTE]
> Bu, genel verileri ortamınızdaki tüm şirketler arasında **ResRollup** tablosuna dağıtır, bu nedenle toplu işlemin yalnızca bir yasal varlıkta çalıştırılması yeterlidir. Bu toplu işlem, tüm **Kaynak kullanılabilirliği** görünümleri için gereklidir. Bu toplu iş çalışmazsa, **ResRollup** verileri uçarak üzerinde oluşturulur ve bu da zaman alabilir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]