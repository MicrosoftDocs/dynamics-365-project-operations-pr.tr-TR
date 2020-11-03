---
title: Uygulamanın 2.x sürümünde kaynakları nasıl "geçici ayırabilirim"?
description: Bu makalede Project Service'le proje takımı üyelerinin nasıl geçici ayrılabileceği açıklanmaktadır.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 9e5d1c91f8ea98117583996552c2f2834be9c537
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086347"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a>Web uygulamasında (Project Service uygulama sürümü 2.x) kaynakları nasıl "geçici ayırabilirim"?

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Kaynağı bir projeye atamayı planladığınızı göstermek için bir proje takımına geçici olarak zamanlayabilir veya "geçici ayırabilirsiniz". Geçici ayırmalar bir kaynağın kullanılabilir kapasitesini tüketmez. Geçici ayrılan takım üyeleri, proje görevlerine atanamaz. Görevlere yalnızca durumu Kesin Ayrılmış ve taahhüt türü Taahhüt Edildi olan kaynaklar görevlere atanabilir (atama çalışma niceliğini kapsayacak kadar ayırma saat sayısı içerdiklerini varsayıyoruz).

Geçici ayrılan proje takımı üyeleri, Takım Üyesi kılavuzunda, geçici ayrılmış saatleri Geçici Ayırma sütununda belirtilmiş halde görünür. Üyeler zamanlama panosunda da görünür. Geçici ayırma, bir kaynağın kapasitesini tüketmediği için, bunlar için de herhangi bir kapasite tüketimi söz konusu değildir.

Bir takım üyesini bir projeye Project Service 2.x sürümüyle geçici olarak ayırmanın üç yolu vardır. Geçici ayırmayı, zamanlama panosuyla, Ayırma İşlemlerini Koru özelliğini kullanarak veya genel bir kaynak oluşturarak yapabilirsiniz. Bu yöntemler aşağıda açıklanmaktadır.

## <a name="soft-book-with-the-schedule-board"></a>Zamanlama panosuyla geçici ayırma

Geçici ayırmayı zamanlama panosuyla yapmak için şu prosedürü izleyin: 
1. Zamanlama panosunu açın.
2. Zamanlama panosunun alt tarafındaki Ayırma Gereksinimleri panelinde Proje sekmesini seçin.
3. Üzerinde bir kaynağı geçici ayırmak istediğiniz projeyi bulun. Çok sayıda projeniz varsa Proje sütun başlığına tıklayın ve filtreyi kullanarak projenizi bulun.
4. Projeye tıklayıp sürükleyin ve kaynağın zaman kılavuzuna bırakın.
5. Bu, sağ taraftaki Kaynak Ayırma Oluştur panelini açar. Başlangıç ve bitiş tarihini ayarlayın, Ayırma Durumunu Geçici olarak seçin ve saatleri belirleyin. 
6. Ayır'a tıklayın.
7. Projeye dönüldüğünde, kaynak, saatleri Geçici Ayırma sütununda geçici ayrılmış halde bir takım üyesi olarak görünür.

Bunları iş kırılım yapısındaki (İKY) görevlere atayamazsınız çünkü kaynaklar, atanacak takımda kesin olarak ayrılmış olmalıdır.

## <a name="soft-book-using-the-maintain-bookings-feature"></a>Ayırmaları Koru özelliğini kullanarak geçici ayırma

Geçici ayırmayı Ayırmaları Koru özelliğiyle yapmak için şu prosedürü izleyin:
1. Takım üyesi kılavuzunda Yeni'ye tıklayın.
2. Ayrılabilir kaynağı, rolü, başlangıç/bitiş tarihlerini seçin.
3. Hiçbiri dışındaki bir tahsisat yöntemini seçin:
- Tam Kapasite
- Yüzde Kapasite
- Saatlere Göre - Eşit Dağıt
- Saatlere Göre - Ön yük
4. Kaydet 'i tıklatın. Kaynağı takım kılavuzunda, saatleri Kesin olarak belirtilmiş halde görürsünüz.
5. Ayırmaları Koru'ya tıklayarak, kaynağın ayırmalarını koruyun.
6. Zamanlama panosu açılınca, kaynağı genişleterek ayırmalarını görünür hale getirin. Ayırmayı Kesin olarak belirtilmiş halde görürsünüz.
7. Ayırmaya sağ tıklayın, Durumu Değiştir altında Geçici Ayırma'yı ve ardından Geçici'yi seçin. Ayırma durumu artık Geçici'dir.
8. Zamanlama panosunu kapattıktan sonra, takım üyesi kılavuzunda kaynağın saatlerinin Kesin'den Geçici'ye çevrildiğini görürsünüz.
Bir kaynağı takıma kesin olarak ayırıp İKY'deki görevlere atarsanız, Kesin olan durumu Geçici'ye çevirmek için Ayırmaları Koru'yu kullandığınız zaman, o kaynağın görevlerinden atamaları kaldıracağını çünkü yalnızca kesin olarak ayrılan kaynakların görevlere atanabileceğini unutmayın.

## <a name="soft-book-by-creating-a-generic-resource"></a>Genel kaynak oluşturarak geçici ayırma

Genel kaynak takım üyesi üreterek, zamanlama panosuyla veya Kaynak İsteği'yle karşılayarak ve ayırma sırasında türü değiştirerek bir geçici ayırma oluşturabilirsiniz.
Bunu yapmak için aşağıdaki prosedürü kullanın:

1. Proje İKY'sinde, rolleri, genel takım üyelerini oluşturmak istediğiniz görevlere atayın.
2. Proje Takımı Oluştur'a tıklayın.
3. Proje takımı üyesi kılavuzunda genel kaynağı seçin ve Ayır'a tıklayın.
4. Zamanlama panosunda, ayırmayı istediğiniz kaynağı seçin.
5. Zamanlama panosunun Kaynak Ayırma Oluştur panelinde, Ayırma Durumunu değiştirip Geçici yapın.
6. Ayır'a veya Ayır ve Çık'a tıklayın.

Zamanlama panosunu kapattıktan sonra, takıma eklenen seçili kaynağı, Geçici ayarlanmış saat ve atanmış saat bilgileriyle birlikte görürsünüz. Ayrıca, genel kaynağın, takımda, görevlerin geçici ayrılmış bir takım üyesine atandığına ilişkin bir gösterge olarak kaldığını da görürsünüz.

Geçici olarak ayrılmış bir takım üyesi kaynağını, görevlere atayabilmeniz için kesin olarak ayrılmış bir takım üyesine çevirmeye hazır olunca aşağıdakileri yapın:

1. Kaynağı seçin ve Ayırmaları Koru'ya tıklayın.
2. Zamanlama panosu açılınca, kaynağı genişleterek ayırmalarını görünür hale getirin. Ayırmayı Geçici şeklinde işaretlenmiş olarak görürsünüz.
3. Ayırmaya sağ tıklayın, Durumu Değiştir altında Kesin Ayırma'yı ve ardından Kesin'i seçin. Ayırma durumu artık Kesin'dir.
4. Zamanlama panosunu kapattıktan sonra, takım üyesi kılavuzunda kaynağın saatlerinin Geçici'den Kesin'e çevrildiğini görürsünüz. Artık, kaynağı görevlere atayabilirsiniz (kesin ayrılmış saatler ve görev çalışma saatlerinin atama için tutarlı olması koşuluyla). Yukarıdaki madde 3'te genel kaynak karşılama adımlarını izlediyseniz, geçici ayrılmış ayrılabilir kaynağın durumunu değiştirip Kesin yaptığınız zaman genel takım üyesinin takımdan kaldırılacağını unutmayın.
