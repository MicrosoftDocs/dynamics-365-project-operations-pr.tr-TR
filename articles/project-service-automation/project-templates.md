---
title: Proje şablonları
description: Bu konu, hızlı proje kurulumu için proje şablonlarının nasıl kullanılacağı hakkında bilgi sağlar.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: f0161bf9-af4c-4a21-b767-ac20a8e30688
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5a3112c2eef9525946314bdb587c44904557fa52
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756609"
---
# <a name="project-templates"></a>Proje şablonları 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Proje şablonu bir projeye hızlı ve kolay bir şekilde başlamanıza yardımcı olan önceden tanımlanmış bir çerçevedir. Tek bir tıklamayla yeni bir proje oluşturmak için önceden tanımlanmış bir şablon kullanabilirsiniz. Projelerde olduğu gibi proje şablonları için ön koşulları tanımlamanız gerekir. Her proje şablonu için bir proje takvimi tanımlamanız gerekir ve şablondaki bileşenlerin yararlı verileri olması için roller ve fiyat listelerinin kuruluşta önceden tanımlanmış olması gereklidir.

Proje şablonu üç bileşenden oluşur: zamanlama, proje tahminleri ve proje takımı üyeleri.

## <a name="schedule"></a>Zamanlama

Proje şablonundaki bir zamanlama, projedeki zamanlamayla aynı bileşen kümesine sahiptir. Bir görev hiyerarşisi oluşturabilir, rolleri görevlerle ilişkilendirebilir, zamanlama öznitelikleri tanımlayabilir ve bağımlılıkları ayarlayabilirsiniz. Proje şablonundaki bir zamanlama her görev için görev modlarını da destekler. Bu nedenle zamanlama altyapısını destekler. Proje takvimini projeyle ilişkilendirmeniz gerekir. Çalışma zamanlaması oluşturduğunuzda bir proje şablonu ile bir proje arasında fark yoktur.

## <a name="project-estimates"></a>Proje tahminleri

Proje şablonundaki proje tahminleri, projedeki proje tahminleriyle aynı şekilde çalışır. Ancak maliyet ve satış fiyatları, parametrelerde tanımlanan varsayılan maliyet ve satış fiyatı listelerinden alınır.

## <a name="creating-a-project-from-a-template"></a>Şablondan bir proje oluşturma
 
Proje şablonundan proje oluşturmanın çeşitli yolları vardır:

- Tekliften bir proje oluşturduğunuzda **Hızlı Oluştur: Proje** iletişim kutusundan bir proje şablonu seçebilirsiniz.

> ![Hızlı Oluştur: Proje iletişim kutusu](media/project-11.png)

- **Yeni Proje**'yi seçerek bir proje oluşturduğunuzda kayıt kaydedilmeden önce **Proje** sayfası görüntülenir. **Şablon Seç** alanında, kuruluşta önceden tanımlanmış proje şablonlarından birini seçin.
- **Şablon Varlığı** sayfasındaki **Şablondan Proje Oluştur**'u kullanın.

## <a name="copying-components-of-template-to-project"></a>Şablon bileşenlerini projeye kopyalama

Proje şablonunun bileşenlerini bir projeye kopyaladığınızda projedeki ayarlara bağlı olarak birkaç geçersiz kılma oluşabilir.

### <a name="copying-the-schedule"></a>Zamanlamayı kopyalama

Proje şablonundan zamanlama kopyaladığınızda proje, şablondan farklı bir proje takvimine sahipse projenin takvimindeki çalışma saatleri görev zamanlamasına uygulanır. Bu şekilde zamanlama, destekleyici proje takvimiyle eşleşecek şekilde ayarlanır. Benzer şekilde, zamanlamadaki ilk görev, projenin başlangıç tarihini alır ve şablonda belirtilen süre ve bağımlılıkları temel alarak hiyerarşinin geri kalanının zamanlaması güncelleştirilir. 

### <a name="copying-project-estimates"></a>Proje tahminlerini kopyalama 

Proje tahmini satırları arasında kopyalama yaptığınızda fiyat listeleri güncelleştirilir. Maliyet fiyatı listesinde bu güncelleştirmeler projenin sahip olduğu birimi temel alır. Satış fiyatı listesinde bunlar müşteriyi temel alır. Satış varlığıyla ilişkilendirilen projelerde birim maliyeti ve satış fiyatları bu fiyat listelerine göre belirlenir.

### <a name="copying-a-project-team"></a>Proje takımını kopyalama

Proje takımı proje şablonundan bir projeye kopyalandığında genel kaynaklar, şablonda tanımlanan beceriler ve uzmanlıklarla birlikte kopyalanır. Genel kaynak atamaları da proje şablonunda olduğu gibi korunur. Adlandırılmış kaynaklar proje şablonlarında desteklenmez.
