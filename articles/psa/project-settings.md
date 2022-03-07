---
title: Proje ayarları
description: Bu konu, proje yönetim ayarları hakkında bilgi sağlar.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: c9b8659f3b7ee81d2e21ef52743debd521fa9bb9
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086487"
---
# <a name="project-settings"></a>Proje ayarları

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Proje planlama özelliklerine erişmek için aşağıdaki ayarları kullanın.

## <a name="work-template"></a>Word şablonu

Proje zamanlaması oluşturmak için günlük çalışma saatleri sayısını ve işletmenin kapalı olduğu tüm tarihleri tanımlayan bir proje takvimi şablonu oluşturun. Proje takvimi şablonu oluşturmak için bir iş şablonunu projenin **Takvim şablonu** alanıyla ilişkilendirin. İş şablonu oluşturmak için aşağıdaki adımları uygulayın.

1. PSA'da soldaki gezinme bölmesinde **Kaynaklar**'a tıklayın. 
2. **Kaynaklar** listesi sayfasında bir kullanıcı kaydı açın ve ardından **Çalışma Saatlerini Göster**'i seçin.

  > [!NOTE]
  > Tarayıcı sayfasında açılır pencerelere izin verdiğinizden emin olun. Bu, kaynak için ayarlanmış çalışma saatlerini görmenizi sağlar.
  
3. **Aylık Görünüm** sekmesinde **Ayarla**'ya tıklayın. Üç seçenekli bir liste görünür: 

  - Yeni Haftalık Zamanlama
  - Bir Gün için Çalışma Zamanlaması
  - Boş Zaman

> ![Seçenekleri ayarlama](media/project-13.png)

4. **Yeni Haftalık Zamanlama**'yı seçin ve ardından bu kaynak zamanlaması için seçenekleri ayarlayın. Yinelenen haftalık zamanlama, günlük saat parametreleri, işletme kapanışları ve daha fazlasını ayarlayabilirsiniz.
5. Tarih aralığını ayarlayın, **Kaydet**'i seçin ve ardından **Kapat**'a tıklayın. 
6. **Kaynaklar** listesi sayfasına geri dönün ve çalışma saatlerini ayarladığınız kaynağı seçin. 
7. İş şablonunu ayarlamak için **Takvimi Farklı Ayarla**'yı seçin. 
8. **İş Şablonu** iletişim kutusunda iş şablonu için bir ad girin ve ardından **Uygula**'yı seçin. 

Artık iş şablonunu proje takvimi şablonuyla ilişkilendirebilirsiniz.

## <a name="resource-roles"></a>Kaynak rolleri

*Kaynak rolü* terimi bir kişinin projede belirli bir görevler kümesini gerçekleştirmek için sahip olması gereken beceri, uzmanlık ve sertifikaları ifade eder. PSA, kaynağın ilişkili olduğu rolü temel alarak kaynağın zamanını maliyetini çıkarıp faturalamanızı sağlar. Her kuruluş **Project Service** menüsündeki sol gezintiyi kullanarak bu rolleri ayarlamalıdır.

Her kuruluş bu rolleri **Etkin Kaynak Kategorileri** sayfasında ayarlamalıdır. Bu sayfayı açmak için sol gezinti bölmesinde **Kaynak Rolleri**'ni seçin.

## <a name="price-lists"></a>Fiyat listeleri

Fiyat listeleri bir kuruluştaki kaynak rolleri için maliyet ve satış fiyatlarını, gider kategorilerini, ürünleri ve diğer öğeleri ayarlamanızı sağlar. Projenin teslim edilmesi gereken işi için mali tahminleri ayarlamadan önce destek maliyeti ve satış fiyat listesini oluşturmalısınız. Parametreler bölümünde kuruluşta oluşturulan tüm projeler için geçerli bir varsayılan maliyet ve satış fiyat listesi ayarlamalısınız. **Etkin Proje Parametreleri** sayfasında varsayılan bir maliyet ve satış fiyat listesi ayarladığınızdan emin olun.
