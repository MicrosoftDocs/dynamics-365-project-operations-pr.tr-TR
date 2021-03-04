---
title: Web uygulamasında göreve nasıl ayrılabilir kaynak atarım?
description: Kullanılabilir kaynakları atayabileceğiniz yöntemlere genel bakış.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 27a93c41243f300cadb632c697672180e5a3817b
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146597"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a>Web uygulamasında (Project Service uygulaması v2.x) bir göreve nasıl bir ayrılabilir kaynak atayabilirim?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Project Service'te bir göreve kaynak atamak için iki yol vardır. Bir kaynağı bir takım üyesi olarak ayırabilir ve ardından bir göreve atayabilirsiniz. Veya görevlerde rol atamayla genel bir takım üyesi oluşturabilir, bir takım kurabilir ve adlandırılmış bir kaynakla, destekleyici gereksinimleri karşılayabilirsiniz.

Bir göreve bir ayrılabilir kaynak atamak istiyorsanız, ayrılabilir kaynak takım üyesinin yeterli kullanılabilir ayırmalara sahip olması gerektiğini unutmayın. Ayırmanın durumu Kesin Ayırma ve taahhüt türü Taahhüt Edildi olmalıdır. Kaynak için yeterli ayırma yoksa, Project Service atamayı kaldırır ve aşağıdaki hata iletisini görüntüler:

*Göreve kaynak atanamıyor - Aşağıdaki kaynakta veya kaynaklarda proje için yeterli saat ayrılmamış*

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Bir kaynağı bir takım üyesi olarak ayırın ve ardından kaynağı bir göreve atayın.

Bu yöntemle bir kaynağı proje takımına ekler ve ardından proje zamanlamasındaki kaynağa görevler atarsınız. Bunu aşağıda belirtildiği şekilde yapabilirsiniz:
1.  Takım üyesi kılavuzunda **Yeni**'yi seçerek yeni bir takım üyesi ekleyin.
2.  Takım Üyesi Hızlı Oluştur ekranında, ayrılabilir kaynağın adını seçin ve rol ayarlayın.
3.  **Başlangıç** ve **Bitiş** tarihlerini seçin.

    > [!div class="mx-imgBorder"] 
    > ![Takım üyesi ekleme ekran görüntüsü](media/FAQ-Resources-to-Tasks2-1.png "Takım üyesi ekleme ekran görüntüsü")
 
4.  Kaynak ayırma için aşağıdaki tahsisat yöntemlerinden birini seçin:
    - **Tam Kapasite**, belirtilen başlangıç ve bitiş tarihleri için kaynağın tam kapasitesini ayırır.
    - **Yüzde Kapasite**, belirtilen başlangıç ve bitiş tarihleri için kaynak kapasitesinin bir yüzdesini ayırır.
    - **Saatlere Göre - Eşit Dağıt**, kaynağı, belirtilen sayıda saatler için ayırır ve belirtilen başlangıç ve bitiş tarihleri arasında her güne eşit olarak dağıtır.
    - **Saatlere Göre - Ön Yük**, kaynağı, belirtilen sayıda saatler için ayırır ve günlük saat sayısını, belirtilen başlangıç ve bitiş tarihleri arasında ön yükler.

    **Hiçbiri** seçeneğini belirtmeyin çünkü kaynağı takıma ekler ancak kaynağın kapasitesini kullanan herhangi bir ayırma oluşturmaz.
5.  **Kaydet**'i seçin.

    Ayırmada, bu kaynağı atadığınız görevlerin tarih aralığını ve çalışılması gereken saat sayısını kapsayacak kadar saat olması gerektiğini unutmayın. Bu değerler örtüşmüyorsa, kaynağı göreve atayamazsınız.

6.  Görevin iş kırılım yapısında (İKY), kaynak hücresinin açılan listesine tıklayın. Bunun ardından: 

    1. **Ekle**'yi seçin.
    2. **Kaynaklar** altındaki açılan listeyi ve bu listeden, yukarıda eklediğiniz takım üyesini seçin.
    3. **Tamam** seçeneğini işaretleyin. Takım üyesi göreve atanır.

    > [!div class="mx-imgBorder"] 
    > ![İKY ile kaynak ekleme ekran görüntüsü](media/FAQ-Resources-to-Tasks2-2.png "İKY ile kaynak ekleme ekran görüntüsü")
 
Takım üyesi ızgarasında, Atanan Saat Sayısı altında kaynağın atanmış toplam saat sayısını göreceksiniz. Bu değer, kaynak için ayrılan saat sayısından az veya ona eşit olacaktır. 

> [!div class="mx-imgBorder"] 
> ![Kaynak için atanan saat sayısı ekran görüntüsü](media/FAQ-Resources-to-Tasks2-3.png "Kaynak için atanan saat sayısı ekran görüntüsü")
 
Kaynağa atamaya çalıştığınız görev kaynak ayırmalarının bitiş tarihinden sonra başlıyorsa, kaynak açılan listede görünmez.

Kaynakta atanmamış kapasite kaldıysa, ayrılan saat sayısından daha fazla saat sayısına bir kaynak atayabileceğinizi unutmayın. Bu durumda kaynak, kısmen atanmış (yalnızca ayırmaları kadar) bir kaynak olacaktır. İş kırılım yapısına Personelsiz Saatler sütununu ekleyerek, kalan atanmamış görev saati sayısını görebilirsiniz.

Kaynaklar ayrılmış saat sayısına atanırsa (ayrılan saat sayısı, atanan saat sayısına eşitse), bunları başka görevlere atamaya çalıştığınız zaman aşağıdaki hata iletisini görürsünüz:

*Göreve kaynak atanamıyor - Aşağıdaki kaynakta veya kaynaklarda proje için yeterli saat ayrılmamış.*

Buna ek olarak, projeyi oluşturduğunuz sırada, takıma eklenen varsayılan proje yöneticisi takım üyesi hiç ayırma olmadan eklenir ve herhangi bir göreve atanamaz. Bunlar görevler için kaynak açılan listesinde görünmez.

Bu kaynağı atamak isterseniz, takımdan kaldırıp, Hiçbiri dışındaki bir tahsisat yöntemiyle yeniden eklemeniz gerekir. Proje oluşturulurken bunların takıma eklenme nedeni, projede varsayılan olarak en az bir proje onaylayanı bulunmasını sağlamaktır.

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a>Görevlerde rol atamayla genel bir takım üyesi oluşturma

Bu yöntem, görevler için kaynaklarda yeterli ayırma olmasını sağlar. Önce, rolleri görevlere atadıktan sonra bir takım oluşturarak, görevlerde nihai olarak çalışmasını istediğiniz adlandırılmış kaynağın temel özelliklerini açıklayan bir yer tutucu veya genel kaynak oluşturun. Bunu aşağıda belirtildiği şekilde yapabilirsiniz:

1. İş kırılım yapısında bir görev seçin.
2. Kaynak hücresindeki **Atanan Rol** açılan liste simgesini seçin.
3. **Rol** açılan listesini ve ardından, genel kaynak için rolü seçin.
4. **Tamam** seçeneğini işaretleyin.

    > [!div class="mx-imgBorder"] 
    > ![Kaynak eklemek için İKY kullanma ekran görüntüsü](media/FAQ-Resources-to-Tasks2-4.png "Kaynak eklemek için İKY kullanma ekran görüntüsü")
 
İKY'de görevlere rolleri atama işleminizi tamamladıktan sonra **Proje Takımı Oluştur**'u seçin. Project Service, görev atamalarını toplayarak rollere, kaynak belirleme kuruluş birimlerine ve proje takvimine göre en az sayıda genel takım üyesi oluşturur.

> [!div class="mx-imgBorder"] 
> ![Proje takımı oluşturma ekran görüntüsü](media/FAQ-Resources-to-Tasks2-5.png "Proje takımı oluşturma ekran görüntüsü")
 
Takım Üyesi kılavuzunda, Genel Kaynak türündeki kaynakları rol ve konum adıyla görürsünüz. İşi tamamlamak için bir role iki kaynak gerekiyorsa, Takım Oluştur özelliği iki takım üyesi oluşturur ve ikisini ayırt etmek için pozisyon adı kullanır.

> [!div class="mx-imgBorder"] 
> ![İki genel kaynak ekleme ekran görüntüsü](media/FAQ-Resources-to-Tasks2-6.png "İki genel kaynak ekleme ekran görüntüsü")
 
Genel takım üyesi için destekleyici kaynak gereksinimini, Kaynak Gereksinimi altındaki bağlantıyı seçerek açabilirsiniz.

> [!div class="mx-imgBorder"] 
> ![Destekleyici kaynak gereksinimi açma ekran görüntüsü](media/FAQ-Resources-to-Tasks2-7.png "Destekleyici kaynak gereksinimi açma ekran görüntüsü")

Genel kaynak için **Ayır**'ı seçtikten sonra, zamanlama panosunu kullanarak gerçek bir kaynak bulup ayırabilirsiniz. Ayrıca, gereksinimi, bir kaynak yöneticisi tarafından karşılanması için **İsteği Gönder**'i seçerek gönderebilirsiniz.

Genel kaynak, adlandırılmış bir kaynakla karşılandığı zaman, genel kaynak takımdan kaldırılır ve genel kaynağın görev atamaları, genel kaynağın kaynak gereksinimini karşılayan adlandırılmış kaynağa atanır.
 

