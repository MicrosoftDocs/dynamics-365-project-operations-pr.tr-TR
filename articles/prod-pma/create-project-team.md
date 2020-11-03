---
title: Proje takımı oluşturma
description: Bu konu, proje ekipleri oluşturma ve yönetme hakkında bilgi sağlar.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kdwns
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a7eb9101352afd27b527bf6b8acc6f92198f44ea
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086489"
---
# <a name="create-a-project-team"></a>Proje ekibi oluşturma

[!include [banner](../includes/banner.md)]

Bir projede önceden ayarlanmış rolleri kullanmak için proje yöneticisi rolleri projeyle ilişkilendirmelidir. Bir proje için birden çok rol atanabilir. Karışıklık oluşmasını engellemek için, bu roller ayırma sırasında otomatik olarak etiketlenir. Örneğin, proje yöneticisi üç yazılım mühendisine gereksinim duyduğunda, **yazılım mühendisi 1** , **yazılım mühendisi 2** ve **yazılım mühendisi 3** olarak olan etiketlenen üç yazılım mühendisi rolü otomatik olarak oluşturulur. Rol özellikleri rol için daha önceden ayarlanmışsa, özellikler kaynak araması sırasında filtre olarak uygulanır. Aramayı daha da sadeleştirmek için, ek özellikler gerektikçe eklenebilir.

Görünüm ayarları, kaynak kullanılabilirliğinin daha iyi bir görünümünü vermek için de özelleştirilebilir. Saatlik, günlük, haftalık, aylık, üç aylık ve yıllık kullanılabilirlik seçeneklerini gösterme seçenekleri vardır. Kaynaklar üzerinde kullanılabilir ve kalan kapasiteyi gösterme seçeneği de vardır. Bu seçenek, etkinlik veya kaynak kullanılabilirliği için kullanılabilir zamanı tahmin ederken zaman yönetimi için kullanışlıdır.

Proje yöneticisi sayfada bir rol seçebilir ve gereksinime uyan bir kaynak varsa, rolü doldurmak için bir kaynak ayırmayı seçer. Kaynakların planlama aşaması sırasında bu noktada ayrılmasının zorunlu olmadığını unutmayın. İKY oluştururken, proje için rolleri personelli kaynakla değiştirebilirsiniz. Roller İKY'de personelli kaynaklarla değiştirilmişse, kaynak kurulumu proje ekibi dökümünü ve zamanlamasını otomatik olarak güncelleştirir.

[![Rollerin ve gerçek kaynakların her ikisini de içeren proje ekibi dökümü](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Proje yöneticisinin **Kalan kapasite** , **Tam kapasite** , **Kapasite yüzdesi** ve **Saatleri belirt** gibi bir projeyle ilgili kaynağı belirlemek için çeşitli seçenekleri vardır. Bu ayırma seçenekleri, kaynak atamaları değiştirilirse istediğiniz zaman iptal edilebilir. İki tür ayırma desteklenir:

- **Kesin Ayırma** : Kaynak ayırma onaylanmıştır ve belirtilen süre boyunca görevlendirmede çalışma onaylanmıştır.
- **Geçici ayırma** : Kaynak ayırma geçici olarak belirtilen süre boyunca görevlendirmede çalışacak şekilde ayarlanmıştır onaylanmıştır.

Aşağıdaki yordamda, proje ekibinin nasıl oluşturulacağı açıklanmıştır:

## <a name="create-a-project-team"></a>Proje ekibi oluşturma

1. **Tüm projeler** liste sayfasında bir proje seçin ve sonra **Düzenle** 'yi seçin.
2. **Proje ekibi ve zamanlama** sekmesinde, **Zamanlama bitiş tarihi** alanına, zamanlama başlangıç tarihi artı bir ay girin. Örneğin, zamanlama başlangıç tarihi 24 Haziran 2017 (24.06.2017) ise, **24.07.2017** girin.
3. **Ekle** 'yi seçin.
4. **Projeye roller ekle** bölmesinde **Rol** alanından, **Kıdemli Proje Yöneticisi** 'ni seçin.
5. **Gerekli yetkinlikler** seçeneğini belirleyin.
6. **Özellikleri seç** sayfasında, Kıdemli proje yöneticisi rolü için önceden ayarladığınız özellikler varsayılan olarak seçilidir. **Tamam** 'ı seçin.
7. **Projeye rol ekle** sayfasında, **Kaynak sayısı** alanına **1** girin.
8. **Kaynak** alanında, arama gerekli yetkinliklere sahibi olan tüm kaynakları gösterir. **Daniel Goldschmidt** 'i seçin ve **Oluştur** 'u seçin.
9. **Proje** sayfasında **Ekle** 'yi seçin.
10. **Projeye roller ekle** bölmesinde **Rol** alanından, **Takım üyesi** 'ni seçin. **Kaynak sayısı** alanına, **5** girin.
11. **Oluştur** 'u seçin.
12. **Projeler** sayfasında **Kaynağı karşıla** 'yı seçin.

## <a name="monitor-project-teams"></a>Proje ekiplerini izleme
1. **Tüm projeler** sayfasında, **XYZ Yükseltme Aşama 2** projesinin **Proje kodu** bağlantısını seçin.
2. **Proje ekibi ve zamanlama** hızlı sekmesinde, listelenen proje kaynaklarının doğru olduğundan emin olun.
