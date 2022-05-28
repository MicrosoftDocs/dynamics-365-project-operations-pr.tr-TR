---
title: Düzeltme günlükleri oluşturma ve onaylama
description: Bu konu, düzeltme günlüklerini oluşturma ve onaylama hakkında bilgi sağlar.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: c15db854e3d130150ad7afc707a126b37c57f62d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582827"
---
# <a name="create-and-confirm-correction-journals"></a>Düzeltme günlükleri oluşturma ve onaylama

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Bazen bir zaman veya gider girişi yanlış girilebilir. Örneğin bir danışman, zaman girişi oluştururken yanlış tarih seçebilir veya bir masraf girerken yanlış bir proje seçebilir. Bir danışman gönderilen girişleri güncelleştirmezse arka uç yöneticisi bir proje için gerçek değerleri doğrudan düzeltebilir.

## <a name="correct-approved-time-entries"></a>Onaylanan zaman girişlerini düzeltme     

Bir projeyle ilgili tek veya birden fazla zaman girişini düzeltmek için aşağıdaki adımları uygulayın.

1. **Satış** alanında **İşlemler**' i ve ardından **Onaylanan Zaman**'ı seçin. 

2. **Onaylanan Zaman** listesinde, düzeltmek için bir veya daha fazla onaylanmış zaman girişini bulun ve seçin. İlgili girişleri bulmak için filtreyi kullanabilirsiniz. Örneğin, bir Proje kimliğine filtre uygulayabilir ve bu proje kimliğine sahip tüm onaylanmış zaman girişlerini seçebilirsiniz.

3. **Girişleri düzelt**'i seçin. Atanan türü **Zaman düzeltmesi** olan yeni bir düzeltme günlüğü otomatik olarak oluşturulur. Seçtiğiniz girişler günlüğe eklenir. 

4. **Yeni Günlük** sayfasında, düzeltme günlüğünüz için bir **Açıklama** girin ve sonra **Zaman Girişi Düzeltmeleri** sekmesini seçin.  

5. **Zaman Girişleri için Yeni Değerler** bölümünde, doğru bilgilere sahip olan alanları gereken şekilde güncelleştirin. Örneğin, atanan projeyi veya ayrılabilir kaynağı değiştirebilirsiniz.

6. **Önizleme** yi seçin. İletişim kutusunda **Tamam**'ı seçin. **Günlük satırları** sekmesinde, ters işlem yapılmış seçili zaman girişleri ve oluşturulan düzeltilmiş ilgili satırlarla ilgili orijinal gerçek değerlerin listesini görüntüleyebilirsiniz. Ek düzeltmelerin yapılması gerekiyorsa, 5. ve 6. adımı yineleyin. 

    > [!NOTE]
    > Tüm düzeltilen gerçek değerler **Zaman Girişleri için yeni değerler** bölümünde seçtiğinizle aynı değerlere sahip olacaktır.

7. Düzeltmeler beklendiği gibi görünüyorsa **Onayla**'yı seçin. İletişim kutusunda **Tamam**'ı seçin.

8. **Satış** alanına dönün, **Projeler**'i seçin ve ardından zaman girişlerini güncelleştirdiğiniz projeyi açın. 

9. **Projeler** sayfasında, **Gerçek değerler** sekmesinde, yaptığınız değişiklikleri görüntüleyin. 

    > [!NOTE]
    > **Gerçek değerler** sekmesi görünmüyorsa, **İlgili** > **Gerçek değerler**'i seçin.  

10. **Gerçek Değer İlişkili Görünümü** listesinde, karşılık gelen düzeltilmiş zaman girişleri gibi tersine çevrilen orijinal zaman girişlerinin hala listelendiğini görebilirsiniz. 

 
## <a name="correct-approved-expense-entries"></a>Onaylanan gider girişlerini düzeltme

Bir veya daha fazla gider girişini düzeltmek için aşağıdaki adımları uygulayın. 

1. **Satış** alanında, sol gezinti panosunda **İşlemler**'in altından **Onaylanan Giderler**'i seçin.

2. **Onaylanan Giderler** listesinde, düzeltmek istediğiniz projeyi ve **Girişler düzelt**'i seçin. Atanan **Gider düzeltmesi** türüyle yeni bir düzeltme günlüğü otomatik olarak oluşturulur. 

3. **Yeni Günlük** sayfasında, düzeltme için bir **Açıklama** girin ve **Gider Düzeltmesi** sekmesindeki **Giderler için Yeni Değerler** bölümünde seçili gider satırları için düzeltmek istediğiniz veri alanlarını seçin. Örneğin, gideri başka bir **Projeye** atayabilir veya **Gider Kategorisi**, **Gider Tarihi** veya **Ayrılabilir Kaynak** öğesini düzeltebilirsiniz.

4. **Önizleme** yi seçin. İletişim kutusunda **Tamam**'ı seçin. 

5. **Günlük satırları** sekmesinde düzeltmeleri doğrulayın. Ters işlem yapılmış seçili gider girişleri ve oluşturulan düzeltilmiş ilgili satırlarla ilgili orijinal gerçek değerlerin listesini görüntüleyebilirsiniz.

6. Düzeltilen değerler beklendiği gibi görünüyorsa **Onayla**'yı seçin. İletişim kutusunda **Tamam**'ı seçin. Değerler beklendiği gibi görünmüyorsa, **Onaylanan Giderler** listesine dönmek için **İptal**'i seçin. 2 ile 5 adım arasındaki işlemleri yineleyin. 

7. Düzeltme günlüğünü onayladıktan sonra, değişikliklerinizi görüntülemek için güncellediğiniz projeye veya projelere geri dönün.

8. Proje sayfasında, **Gerçek değerler** sekmesinde **İlişkilendirilmiş Asıl Görünüm** listesini inceleyin. Orijinal girişler ve düzeltilen girişler listelenir.


## <a name="correct-approved-material-usage-logs"></a>Doğru onaylanmış malzeme kullanım günlükleri

Bir veya daha fazla malzeme kullanım günlüğü girişini düzeltmek için aşağıdaki adımları tamamlayın.

1. **Satış** alanında, sol gezinti bölmesinde **İşlemler** altında **Gerçek değerler** seçeneğini belirleyin.

2. **Gerçek değerler** listesinde, **Malzeme** işlemi sınıfını seçmek için sütun filtrelerini kullanın, böylece yalnızca malzemeler için gerçek değerler gösterilir. Gösterilen gerçek değerleri daha da sınırlamak için diğer sütun filtrelerini kullanın. İstenen gerçek değerleri dizisini bulduktan sonra gerçek değerleri seçin ve ardından **Girişleri düzelt** öğesini seçin. Otomatik olarak yeni bir düzeltme günlüğü oluşturulur ve **Malzeme düzeltme** türü atanır.

3. **Yeni Günlük** sayfasındaki **Açıklama** alanına düzeltme için bir açıklama girin. Ardından, **Malzeme Düzeltmesi** sekmesinde, **Malzemelerin Yeni Değerleri** bölümünde seçilen malzeme satırlarını düzeltmek için veri alanlarını seçin. Örneğin, malzemeyi başka bir projeye atayabilir ya da ürün, malzeme tarihi veya alt sözleşmeyi düzeltebilirsiniz.

4. **Önizleme** yi seçin. Ardından, iletişim kutusunda **Tamam**'ı seçin.

5. **Yevmiye defteri satırları** sekmesinde, düzeltmeleri doğrulayın. Tersine çevrilmiş seçilen malzeme girişleriyle ve oluşturulan düzeltilmiş karşılık gelen satırlarla ilgili orijinal gerçek değerlerin bir listesini görüntüleyebilirsiniz.

6. Düzeltilen değerler beklendiği gibi görünüyorsa **Onayla**'yı seçin. Ardından, iletişim kutusunda **Tamam**'ı seçin. Değerler beklendiği gibi değilse **İptal** öğesini seçerek **Gerçek değerler** listesine geri dönün. Sonra 2 ile 5 arasındaki adımları tekrar edin.

7. Düzeltme günlüğünü onayladıktan sonra, değişikliklerinizi görüntülemek için güncellediğiniz projeye veya projelere geri dönün.

8. Proje sayfasında, **Gerçek değerler** sekmesinde **İlişkilendirilmiş Asıl Görünüm** listesini inceleyin. Orijinal girişler ve düzeltilen girişler listelenir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
