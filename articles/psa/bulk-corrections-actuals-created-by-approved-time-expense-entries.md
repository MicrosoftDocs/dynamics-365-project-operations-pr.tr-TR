---
title: Onaylanan zaman ve gider girişleri tarafından oluşturulan fiili değerlerin toplu düzeltmeleri
description: Bu konu, fatura tamamlanmadıysa bir yöneticinin önceden onaylanmış zaman veya gider girişlerinde nasıl tek veya toplu düzeltmeler yapabileceğini açıklar.
author: rumant
manager: AnnBe
ms.date: 04/02/2020
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
search.app:
- ProjectOperations
ms.openlocfilehash: 17d6648840e27a4e573985af2cdd74c4adf878e1
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290923"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a>Onaylanan zaman ve gider girişleri tarafından oluşturulan fiili değerlerin toplu düzeltmeleri

[!include [banner](../includes/psa-now-project-operations.md)]

Bazen bir zaman veya gider girişi yanlış girilebilir. Örneğin, bir danışman zaman girişi oluştururken yanlış tarih seçebilir veya bir gideri girerken sayıların yerini değiştirebilir. Danışman gönderilen girişlerde güncelleştirmeler yapamazsa, yönetici projeyle ilgili girişi doğrudan düzeltebilir.

Bu konudaki yordamları tamamlayabilmek için, Yönetici izinlerine sahip olmanız gerekir.

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

Örneğin, aşağıdaki grafikte, miktarı 8,00 olan ve Tutar sütununda listelenen borçları bulunan iki satır maddesi bulunur. Buna ek olarak, miktarı -8,00 olan ve Tutar sütununda alacak tutarı bulunan iki satır maddesi vardır. Bu düzeltmeler miktarı sıfıra getirir.

![Gerçek değer ilişkili görünümü listesi](https://github.com/MicrosoftDocs/dynamics-365-customer-engagement-pr/blob/bulk-corrections-actuals-created-by-approved-time-expense-entries.md/time-actuals.png)
 
## <a name="correct-approved-expense-entries"></a>Onaylanan gider girişlerini düzeltme

Bir veya daha fazla gider girişini düzeltmek için aşağıdaki adımları uygulayın. 

1. **Satış** alanında, sol gezinti panosunda **İşlemler**'in altından **Onaylanan Giderler**'i seçin.

2. **Onaylanan Giderler** listesinde, düzeltmek istediğiniz projeyi ve **Girişler düzelt**'i seçin. Atanan **Gider düzeltmesi** türüyle yeni bir düzeltme günlüğü otomatik olarak oluşturulur. 

3. **Yeni Günlük** sayfasında, düzeltme için bir **Açıklama** girin ve **Gider Düzeltmesi** sekmesindeki **Giderler için Yeni Değerler** bölümünde seçili gider satırları için düzeltmek istediğiniz veri alanlarını seçin. Örneğin, gideri başka bir **Projeye** atayabilir veya **Gider Kategorisi**, **Gider Tarihi** veya **Ayrılabilir Kaynak** öğesini düzeltebilirsiniz.

4. **Önizleme** yi seçin. İletişim kutusunda **Tamam**'ı seçin. 

5. **Günlük satırları** sekmesinde düzeltmeleri doğrulayın. Ters işlem yapılmış seçili gider girişleri ve oluşturulan düzeltilmiş ilgili satırlarla ilgili orijinal gerçek değerlerin listesini görüntüleyebilirsiniz.

6. Düzeltilen değerler beklendiği gibi görünüyorsa **Onayla**'yı seçin. İletişim kutusunda **Tamam**'ı seçin. Değerler beklendiği gibi görünmüyorsa, **Onaylanan Giderler** listesine dönmek için **İptal**'i seçin. 2 ile 5 adım arasındaki işlemleri yineleyin. 

> [!NOTE]
> Düzeltilen gerçek değerler **Giderler için yeni değerler** bölümünde seçtiğinizle aynı değerlere sahip olacaktır.

7. Düzeltme günlüğünü onayladıktan sonra, değişikliklerinizi görüntülemek için güncelleştirtiğiniz proje veya projelere tekrar gidin.  

8. Proje sayfasında, **Gerçek değerler** sekmesinde, **Gerçek Değerler İlişkili Görünümü**'nü gözden geçirin. Orijinal girişler ve düzeltilen girişler listelenir. Aşağıdaki grafik orijinal gider girişi tutarlarını ve karşılık gelen düzeltilmiş gider girişi tutarlarını gösterir. 

![Gider gerçek değerleri](https://user-images.githubusercontent.com/60806505/77122219-4cd52900-69fa-11ea-8349-ccd2ffebf640.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]