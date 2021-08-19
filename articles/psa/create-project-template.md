---
title: Bir proje şablonu oluştur
description: Project Service'ta proje şablonu oluşturma
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 1423dfedccfdc471662581707b4441c9ed477f7c0811ccf3905af8c59f774f77
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6990880"
---
# <a name="create-a-project-template-project-service"></a>Proje şablonu oluşturma (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Şirketiniz düzenli olarak benzer türlerde projelere teklif sunuyorsa proje şablonları zamandan tasarruf sağlar. Belirli bir proje türü için standart roller kümesi ve saat cinsinden tahmini süreler sağlar. Firma yöneticileri ve proje yöneticileri bir proje şablonunu temel alarak projeler oluşturabilir veya şablonu kopyalayarak kendi şablonlarını oluşturabilirler.  
  
## <a name="components-of-project-template"></a>Proje şablonu bileşenleri
 Bir proje şablonu şu üç bileşenden oluşur:  
  
- **İş kırılım yapısı**: Proje şablonundaki iş kırılım yapısı, projedeki bileşenlerle aynı bileşen kümesine sahiptir. Bir görev hiyerarşisi oluşturabilir, rolleri görevle ilişkilendirebilir, zamanlama öznitelikleri tanımlayabilir, bağımlılıkları ayarlayabilir ve tüm verileri Gantt'ta görüntüleyebilirsiniz. Proje şablonlarındaki iş kırılım yapısı ayrıca her bir görevin görev modlarını da destekler. İş zamanlamasının oluşturulması açısından bir proje şablonu ile bir proje arasında hiçbir fark yoktur.  
  
- **Proje tahminleri**: Şablonlardaki proje tahminleri, projedekilerle aynı şekilde çalışır, ancak maliyet ve satış fiyatlarının varsayılan yapılması için fiyat listeleri daima [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] parametrelerinde tanımlanan varsayılan maliyet ve satış fiyatı listeleridir. İşlevin geri kalanı bir projede olduğu gibidir.  
  
- **Proje ekibi oluşumu**: Bir proje şablonu için bir proje ekibi oluşturulurken bir şablonda adlandırılmış bir kaynak ayıramazsınız. Bir genel kaynak kümesi oluşturmak için iş kırılım yapısında **Proje Ekibi Oluştur** işlevini kullanabilirsiniz. Ayrıca, genel kaynaklar için gerekli nitelikleri ve yeterlilikleri belirleyebilirsiniz. Genel bir kaynak yerine proje şablonlarındaki ayrılabilir bir kaynak kullanamazsınız.  
  
## <a name="create-a-project-from-a-template"></a>Şablondan bir proje oluşturun  
 Aşağıdaki adımları takip ederek bir şablondan proje oluşturabilirsiniz:  
  
-   Tekliften bir proje oluştururken proje hızlı oluşturma formundan bir proje şablonu seçebilirsiniz.  
  
-   **Yeni Proje** düğmesine tıklayarak bir proje oluşturduğunuzda proje formu, kaydı kayıt etmenizden önce görüntülenir. Buradan, şirketinizin ön tanımlı proje şablonları listesinden seçim yapmak için **Bir şablon seç** alanına tıklayabilirsiniz.  
  
-   Şablondan bir proje oluşturmak için **Proje Şablonu** sayfasındaki **Bir şablondan proje oluştur** düğmesine tıklayın.  
  
## <a name="copying-components-of-a-template-to-a-project"></a>Bir şablonun bileşenlerinin bir projeye kopyalanması  
 Bir şablonun bileşenlerini bir projeye kopyalarken dikkat etmeniz gereken birkaç husus vardır.  
  
 **Bir iş kırılım yapısının kopyalanması**: Bir proje şablonundan iş kırılım yapısı kopyaladığınızda proje, şablondan farklı bir proje takvimine sahipse, proje takviminin çalışma saatleri görevlerin zamanlamasına uygulanır. Bu da zamanlamayı destekleyici proje takvimine göre ayarlar. Benzer şekilde, iş kırılım yapısındaki ilk görev, projenin başlangıç tarihini alır, böylece görev hiyerarşi zamanlamasının geri kalan kısmı, şablonun iş kırılım yapısında belirtilen süreye ve bağımlılıklara dayalı olarak güncellenir.  
  
 **Proje tahminlerinin kopyalanması**: Proje tahmin satırlarını kopyalarken fiyat listeleri, maliyet fiyatı listesi için projenin ve satış fiyatı listesi için müşterinin geçerli birimine dayalı olarak güncellenir. Birim maliyet ve satış fiyatları bir satış varlığıyla ilişkilendirilen projelerde bu fiyat listelerine göre belirlenir.  
  
 **Bir proje ekibinin kopyalanması**: Proje ekibini bir şablondan projeye kopyaladığınızda genel kaynaklar, şablonda tanımlanan nitelikler ve yeterliliklerle birlikte kopyalanır. Genel kaynak atamaları da proje şablonunda olduğu gibi tutulur.  
  
### <a name="see-also"></a>Ayrıca bkz.  
 [Proje Yöneticisi Kılavuzu](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]