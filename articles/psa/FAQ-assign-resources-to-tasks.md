---
title: Göreve kaynak atama
description: Bu konu, görevlere kaynak atama hakkında bilgi sağlar.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: 77f13d1e96b76dfea241fbf7a67d5676582f0235
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086513"
---
# <a name="assign-a-resource-to-a-task"></a>Göreve kaynak atama

Microsoft Dynamics 365 Project Service Automation'ta bir göreve kaynak atamak için üç yol vardır.

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Bir kaynağı bir takım üyesi olarak ayırın ve ardından kaynağı bir göreve atayın.

Bir kaynağı proje takımına ekleyebilir ve ardından kaynağı proje zamanlamasındaki görevlere atayabilirsiniz.

1. **Takım üyesi** sekmesinde **Yeni** 'yi seçerek yeni bir takım üyesi ekleyin. 

2. Ayrılabilir kaynağın adını seçip bir rol ayarlayabileceğiniz **Takım Üyesi Hızlı Oluştur** panelini açılır. 

    Kaynak ayırma için aşağıdaki tahsisat yöntemlerinden birini seçin:

    - **Tam Kapasite** , belirtilen başlangıç ve bitiş tarihleri için kaynağın tam kapasitesini ayırır.
    - **Yüzde Kapasite** , belirtilen başlangıç ve bitiş tarihleri için kaynak kapasitesinin bir yüzdesini ayırır.
    - **Saatlere Göre - Eşit Dağıt** , kaynağı, belirtilen sayıda saatler için ayırır ve belirtilen başlangıç ve bitiş tarihleri arasında her güne eşit olarak dağıtır.
    - **Saatlere Göre - Ön Yük** , kaynağı, belirtilen sayıda saatler için ayırır ve günlük saat sayısını, belirtilen başlangıç ve bitiş tarihleri arasında ön yükler.
    - **Hiçbiri** , kaynağı takıma ekler ancak kaynağın kapasitesini kullanan herhangi bir ayırma oluşturmaz.

3. Bir görevin **Zamanlama** kılavuzunda, kaynak hücresindeki **Kaynak** simgesini ve ardından **Takım Üyeleri** altından az önce eklediğiniz takım üyesini seçin. 

> [!NOTE]
> **Takım Üyesi** ve **Mutabakat** sekmelerinde kaynak ayrılan ve atanan saatleri gösterir. Saatlerin aynı olması gerekir ama ayırmalar ve atamalar gibi kesin bir şekilde eşleştirilmiş olmaları gerekmez. **Mutabakat** sekmesi, bunlar farklı olduğu zaman (örneğin, kaynağa, ayırdığınız saat sayısından daha fazla saat sayısı atadığınız zaman) size ayrıntıları verir. Gerekirse, kaynağın ayırmalarını artırarak veya atamayı değiştirerek bilgileri düzeltebilirsiniz.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Görev atamayla genel bir takım üyesi oluşturma

Görev atama aracılığıyla genel bir takım üyesi oluşturduğunuzda, görevlerde nihai olarak çalışmasını istediğiniz adlandırılmış kaynağın temel özelliklerini açıklayan bir yer tutucu veya genel kaynak oluşturabilirsiniz. Bunun ardından, adlandırılmış kaynağı aramak ve ayırmak için kullanılan bir gereksinim oluşturursunuz (veya gereksinimi kullanma isteği gönderirsiniz).

1. Görevin **Zamanlama** kılavuzunda, kaynak hücresindeki **Kaynak** simgesini seçin.

2. Yer tutucu kaynağın adı olarak işlev görecek bir ad yazın. Örneğin, Program Yöneticisi.

3. **Oluştur** 'u seçin ve **Proje Takımı Üyesi Hızlı Oluştur** alanında, genel kaynak için rolü ayarlayın.

4. Görevin **Kaynak Seçicisinde** kaynağı seçerek, bu yer tutucu kaynağa görevler atamaya devam edebilirsiniz. Bunlar **Takım Üyeleri** altında listelenir.

5. Genel kaynak atamayı tamamladıktan sonra, **Takım** sekmesinde genel kaynağı seçin ve **Gereksinim Oluştur** 'u seçerek, genel kaynak için bir kaynak gereksinimi oluşturun.

6. Genel kaynak için **Ayır** 'ı seçin. Bunun ardından, gerçek bir kaynağı bulmak ve ayırmak için Zamanlama panosunu kullanabilirsiniz. Ayrıca, gereksinimi, bir kaynak yöneticisi tarafından karşılanması için gönderebilirsiniz.

7. Genel kaynak, adlandırılmış bir kaynakla karşılandığı zaman, genel kaynak takımdan kaldırılır ve genel kaynağın görev atamaları, genel kaynağın kaynak gereksinimini karşılayan adlandırılmış kaynağa atanır.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Tüm ayrılabilir kaynaklar listesinden, adlandırılmış bir kaynak atama

Tüm ayrılabilir kaynakları arayıp bir göreve atamak için **Kaynak Seçicideki** arama kutusunu kullanabilirsiniz.

Bu şekilde atanan kaynaklar, herhangi bir ayırma olmadan takıma eklenir. Bu, takım üyesi eklenmesine ve tahsisat yöntemi olarak Hiçbirini seçmeye benzer. Kaynak **Takım** sekmesinde ve **Mutabakat** sekmesinde yalnızca atamaları ve ayırma eksiği olan kaynaklar olarak görüntülenir. Kullanılmalarını istiyorsanız, bunları ayırın.

1. Görevin **Zamanlama** kılavuzunda, kaynak hücresindeki **Kaynak** simgesini seçin.

2. Bir ad yazmaya başlayın. Ad için arama sonuçları, **Diğer Kaynaklar** altındaki **Kaynak Seçicide** görüntülenir.

3. Göreve atamak istediğiniz kaynağı seçin.

