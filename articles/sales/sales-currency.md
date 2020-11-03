---
title: Para birimi
description: Bu konu, Project Operations'da para birimi türlerinin nasıl ekleneceği ve kaldırılacağı hakkında bilgi sağlar.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1db7e76dbb220954b9f9088b2168eed1a1902abc
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086356"
---
# <a name="currency"></a>Para birimi

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Para birimleri, ürün kataloğundaki ürünlerin fiyatlarını ve satış siparişleri gibi işlemlerin maliyetini belirler. Müşterileriniz çeşitli coğrafyalara yayılmışsa işlemlerinizi yönetmek için onların para birimlerini ekleyin. Bugünkü ve gelecekteki iş gereksinimlerinize en uygun olan para birimlerini ekleyin.  

> [!NOTE]
> Ortamınız bir Common Data Service ortamıysa, Power Platform yönetim merkezindesinizdir ve **Para Birimleri** sayfasını ( **Ortamlar** > [ortam seç] > **Ayarlar** > **İş** > **Para birimleri** ) seçtiğinizde bu sayfa boştur. Bunun nedeni, para birimi ayarlamanın Common Data Service ortamlarında desteklenmemesidir.

## <a name="add-a-currency"></a>Para birimi ekleme  
Bu yordama başlamadan önce, güvenlik rolünüzün sistem yöneticisi izinleri içerdiğinden emin olun. 

1. Power Platform yönetim merkezinde bir ortam seçin. 
2. **Ayarlar** > **İş** 'i seçin.
3. **Para Birimleri** 'ni seçin.  
4. **Yeni** 'yi seçin.  
5. Bilgileri gerektiği gibi doldurun.  


   |          Alan          |                                                                                                                                                                                                                                                                                                                                                                            Açıklama                                                                                                                                                                                                                                                                                                                                                                            |
   |-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |    **Para Birimi Türü**    | - **Sistem** - Dynamics 365'teki model yönetimli uygulamalar içindeki kullanılabilir para birimlerini kullanmak isterseniz bu seçeneği belirleyin. Para birimini aramak için **Ara** düğmesini seçin. Para birimi seçtiğinizde **Para Birimi Adı** ve **Para Birimi Simgesi** seçilen para birimine otomatik olarak eklenir.<br />- **Özel** - Dynamics 365'teki model yönetimli uygulamalar içinde bulunmayan para birimlerini kullanmak isterseniz bir para birimi ekleyin. Bu durumda **Para Birimi Kodu** , **Para Birimi Duyarlığı** , **Para Birimi Adı** , **Para Birimi Simgesi** ve **Para Birimi Dönüştürme** değerlerini el ile girmeniz gerekir. |
   |    **Para Birimi Kodu**    |                                                                                                                                                                                                                                                                                                                                            Para birimi için kısa gösterim. Örneğin, ABD Doları için **USD**.                                                                                                                                                                                                                                                                                                                                            |
   | **Para Birimi Duyarlığı**  |                                                                                                                                                                                  Para birimi için kullanmak istediğiniz ondalık basamak sayısını yazın.  0 ile 4 arasında bir değer ekleyebilirsiniz. **Not:** **Sistem Ayarları** iletişim kutusuna bir duyarlılık değeri ayarladıysanız burada, o değer görünür.                                                                                                                                                                                  |
   |    **Para Birimi Adı**    |                                                                                                                                                                                                                                         Dynamics 365'teki model yönetimli uygulamalar içinde kullanılabilir olan para birimleri listesinden bir para birimi seçtiyseniz seçili kod için para birimi burada görüntülenir. Para birimi türü olarak **Özel** seçtiyseniz para birimi adını yazın.                                                                                                                                                                                                                                          |
   |   **Para Birimi Sembolü**   |                                                                                                                                                                                                                                                                      Kullanılabilir para birimleri listesinden bir para birimi kodu seçtiyseniz seçili kodun simgesi burada görüntülenir. Para birimi türü olarak **Özel** seçtiyseniz yeni para biriminin simgesini girin.                                                                                                                                                                                                                                                                       |
   | **Para Birimi Dönüştürme** |                                                                                                                                                                                                                                     Seçilen para biriminin bir ABD doları cinsinden değerini yazın. Bu, seçilen para biriminin temel para birimine dönüştürülme tutarıdır. **Önemli** : İşlemlerinizde doğru olmayan hesaplamaları önlemek için bu değeri gerektiği kadar sık güncelleştirdiğinizden emin olun.                                                                                                                                                                                                                                      |


6. İşlemi tamamladığınızda, komut çubuğunda **Kaydet** 'i veya **Kaydet ve Kapat** 'ı seçin.  

   > [!TIP]
   >  Para birimini düzenlemek için para birimini seçin ve ardından yeni değerleri girin veya seçin.  

## <a name="delete-a-currency"></a>Para birimini silme  

1. Power Platform yönetim merkezinde bir ortam seçin. 
2. **Ayarlar** > **İş** 'i seçin.
3. **Para Birimleri** 'ni seçin.  
4. Görüntülenen para birimleri listesinden silmek istediğiniz para birimini seçin.  
5. **Sil** 'i seçin.  
6. Silme işlemini onaylayın.  

> [!IMPORTANT]
>  Diğer kayıtlar tarafından kullanılan para birimlerini silemezsiniz, yalnızca devre dışı bırakabilirsiniz. Para birimi kayıtlarını devre dışı bırakmak fırsatlar veya siparişler gibi var olan kayıtlardaki para birimi bilgilerini kaldırmaz. Ancak devre dışı bırakılan para birimini yeni işlemler için seçemezsiniz.  
