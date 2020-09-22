---
title: Proje takımına adlandırılmış ayrılabilir kaynaklar ayırma ve görevler atama
description: Bu konu proje takımlarına adlandırılmış kaynaklar ayırma ve bunları görevlere atama hakkında bilgi sağlar.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: e947986a-e83a-42f4-813e-c82bdfbec33c
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 079ba299f912c75f9ed739d4b6aa3c63189d11d0
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756588"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a>Proje takımına adlandırılmış ayrılabilir kaynaklar ayırma ve görevler atama 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Bir adlandırılmış kaynağı proje ekibinize doğrudan takım üzerinde ayırarak ekleyebilirsiniz. Bunu yapmak için aşağıdaki adımları tamamlayın.

1. Project Service Automation'da, **Projeler**'e gidin ve ayırma yaptığınız projeyi seçerek açın.
2. **Proje** sayfasında, **Takım** sekmesinde, **Yeni**'ye tıklayın. 

![Takım sekmesinden bir takım üyesi ekleme](media/RM-how-to-1.png)

3. **Proje Takım Üyesi Hızlı Oluştur** iletişim kutusunda, ayrılabilir kaynağı seçin. **Rol** alanı, atanmış olan varsa kaynağın varsayılan rolüyle doldurulur. Gerekirse rolü değiştirebilirsiniz. 
4. Kaynağın gerekli olduğu başlangıç ve bitiş tarihlerini seçin ve kaynağın kapasitesinin tahsisat yöntemini seçin. 
5. Takım üyesinin bir proje onaylayanı olmasını istiyorsanız, **Proje Onaylayanı** alanında **Evet**'i seçin. Bu, takım üyesinin bu projeye ait gönderilen zaman ve gider girişlerini onaylayabileceği anlamına gelir. 
6. **Kaydet**'e tıklayın.

![Hızlı oluştur formunda takım üyesi ekleme](media/RM-how-to-2.png)


Artık, ayrılan kaynağı projedeki görevlere atayabilirsiniz. **Proje** sayfasında, görevleri yeni kaynağa atamak için **Zamanlama** sekmesine tıklayın. Görev kılavuzundaki **Kaynaklar** alanından başlatılan kaynak seçici, seçebileceğiniz takım üyelerini gösterir.

![Zamanlama sekmesindeki bir göreve takım üyesi atama](media/RM-how-to-3.png)

Project Service Automation (PSA) sürüm 3'te, kaynak ayırmaları ve görev atamaları sıkı bir şekilde eşitlenmez. Bu, zamanlamadaki kaynak seçiciyi kullandığınızda, proje üzerinde bulunan rezervasyon kapasitelerinden daha fazla saat için görevleri ekip üyelerine atayabilirsiniz.
Takım üyesi ayırmaları ve atamaları arasındaki farkları **Takım** sekmesinde veya **Kaynak Mutabakatı** sekmesinde görebilirsiniz. Ayrıca, kaynaklar için ayırmalar ve atamalar arasındaki farklılıkları daha ayrıntılı bir düzeyde mutabık kılabilirsiniz.

![Kaynak mutabakatı sekmesi](media/RM-how-to-4.png)

**Zamanlama** sekmesindeki kaynak seçiciyi proje takımının parçası olmayan ayrılabilir kaynakları aramak ve seçmek için de kullanabilirsiniz. Bunlar, kaynak seçicide **Diğer Kaynaklar** olarak gösterilir.

![Bir göreve takım dışı üye kaynağı atama](media/RM-how-to-5.png)

Bunu yaptığınızda, kaynak proje takımına eklenir ve göreve atanır, ancak herhangi bir ayırma oluşturulmaz.

![Atamaları olan ancak ayırmaları olmayan takım üyesi](media/RM-how-to-6.png)

Kaynağın kapasitesini projeye ayırmak için **Mutabakat** sekmesinin ayırmayı uzatma özelliğini veya **Zamanlama Panosu**'nu kullanabilirsiniz.

![Kaynak mutabakatı sekmesinde bir takım üyesi için ayırmaları uzatma](media/RM-how-to-7.png)

Bir takım üyesi projenize ayrıldıktan sonra, ayırmaları doğrudan yönetmek için ayırmaları sürdür özelliğini veya Zamanlama Panosunu kullanabilirsiniz.
