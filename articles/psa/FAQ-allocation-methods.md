---
title: Project Service Automation'nda ayırma yöntemlerinin ayrılması
description: Bu konu, ayırma tahsisatlarına yönelik farklı yollarla ilgili bilgi sağlar.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 295da428ce15e7775450dfa94e96047f200bdede
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086318"
---
# <a name="booking-allocation-methods-in-project-service-automation"></a>Project Service Automation'nda ayırma yöntemlerinin ayrılması

İster **Takım** sekmesinde bir projeye doğrudan bir takım üyesi ekleyin, ister Zamanlama panosundan bir projeye veya gereksinime bir kaynak ayırın, kullanabileceğiniz birkaç farklı ayırma tahsisat yöntemi vardır. Bu konuda, her bir yöntemin işleyişi ve hangi yöntemlerin kaynaklarda fazladan ayırmaya yol açabileceği açıklanmaktadır.

## <a name="full-capacity"></a>Tam Kapasite 
Tam Kapasite yöntemi, belirtilen başlangıç ve bitiş tarihleri için kaynağın tam kapasitesini ayırır. Örneğin bir kaynak için haftada beş gün, günde sekiz saatlik bir takvim ayarı varsa, beş iş gününü kapsayan bir başlangıç ve bitiş tarihi ayarlanınca kaynak 40 saat olarak ayrılır. Ayırma, kaynağın kalan kapasitesi dikkate alınmadan yapılır. Bir kaynak bu süre boyunca başka projelerde ayrılmışsa, 40 saat, ek saatler olarak ayrılır ve bu, fazladan ayırmalara neden olabilir.

## <a name="remaining-capacity"></a>Kalan Kapasite
Kalan Kapasite yöntemi ancak Zamanlama panosunu kullanarak doğrudan bir projeye ayırdığınız zaman kullanılabilir. Bu yöntem, kaynağın, belirtilen tarih aralığındaki kullanılabilecek kapasitesini ayırır. Örneğin bir kaynağın haftada 40 saatlik bir kapasitesi varsa ve 10 saati ayrılmışsa, aynı hafta için ayırmanın sonucu, o haftanın kalan 30 saatlik kapasitesini ayırma olur.

## <a name="percentage-capacity"></a>Yüzde Kapasite
Yüzde Kapasite yöntemi, belirtilen başlangıç ve bitiş tarihlerine ilişkin kapasitenin bir yüzdesi için kaynak ayırır. Örneğin bir kaynak için haftada beş gün, günde sekiz saatlik bir takvim ayarı varsa, %50 kapasiteyle beş iş gününü kapsayan bir başlangıç ve bitiş tarihi ayarlanınca kaynak 20 saat olarak ayrılır. Her güne düşen tek tek ayırmalar, döneme eşit olarak yayılır (bu örnekte günde dört saattir). Ayırma, kaynağın kalan kapasitesi dikkate alınmadan yapılır. Kaynak bu süre boyunca diğer projelerde ayrılmışsa, 20 saat ek saatler olarak ayrılır ve bu, fazladan ayırmalara neden olabilir.

## <a name="evenly-distribute-hours"></a>Saatleri Eşit Dağıt
Saatleri Eşit Dağıt yöntemi, kaynağı, belirtilen sayıda saatler için ayırır ve belirtilen başlangıç ve bitiş tarihleri arasında zamaı her güne eşit olarak dağıtır. Örneğin beş günlük bir dönemde 20 saat için bir kaynak ayırırsanız, bu yöntem 20 saati günde dört saat şeklinde eşit olarak dağıtır. Ayırma, kaynağın kalan kapasitesi dikkate alınmadan yapılır. Kaynak bu süre boyunca diğer projelerde ayrılmışsa, 20 saat ek saatler olarak ayrılır ve bu, fazladan ayırmalara neden olabilir.

## <a name="front-load-hours"></a>Saatleri Ön Yükle
Ön Yük Saatleri yöntemi kaynağı, belirtilen sayıda saatler için ayırır ve günlük saat sayısını, belirtilen başlangıç ve bitiş tarihleri arasında ön yükler. Ön yükleme, kaynağın kullanılabilir kapasitesini "ilk alınan ilk tüketilir" düzeniyle tüketir. Örneğin bir kaynağın çalışma zamanlaması haftada beş gün ve günde sekiz saatse ve kaynağa ilişkin bir ayırma yoksa, kaynağın beş günlük süre boyunca 20 saat için ayrılması aşağıdaki günlük ayırma düzenini verir: 

|         Ayırma İşlemleri          |    1. Gün    |    2. Gün    |    3. Gün    |    4. Gün    |    5. Gün    |    Toplam    |
|---------------------------|-------------|-------------|-------------|-------------|-------------|-------------|
|    Varolan ayırmalar    |    0        |    0        |    0        |    0        |    0        |    0        |
|    Yeni ayırma          |    8        |    8        |    4        |    0        |    0        |    20       |

Ön yükleme yönteminde, varolan ayırmalar ve kullanılabilir kapasite dikkate alınır. Örneğin, çalışma haftasında aynı kaynak için zaten 20 saatlik ayırma varsa, yeni ayırmalar, kalan kapasiteyi aşağıdaki gibi kullanır:

|   Ayırma İşlemleri          | 1. Gün | 2. Gün | 3. Gün | 4. Gün | 5. Gün | Toplam |
|---------------------|-------|-------|-------|-------|-------|-------|
| Varolan ayırmalar | 8     | 8     | 4     | 0     | 0     | 20    |
| Yeni ayırma       | 0     | 0     | 4     | 8     | 8     | 20    |

Kullanılabilir kapasite göz önünde bulundurulduğu için, ayırmanın kullanabileceği kadar kaynak kapasitesi kalmadıysa bir hata iletisi alabilirsiniz Bu yöntemde fazladan ayırma yapamazsınız.

## <a name="none"></a>Yok
Hiçbiri yöntemi ancak bir projede **Takım** sekmesinden ayırma yaptığınız zaman kullanılabilir. Bu yöntem, kaynağı projede bir takım üyesi olarak ekler ancak kaynağın kapasitesini kullanan herhangi bir ayırma oluşturmaz. Bu yöntem, bir proje oluşturulduğunda, varsayılan proje yöneticisi takım üyesi eklenirken kullanılır. Projeyi oluşturan proje yöneticisi kullanıcı projeye varsayılan olarak eklenir ve böylece proje varlık kaydının bir sahibi olur ve projede bir onaylayan yer alır. Bu kullanıcının herhangi bir ayırması olmadığı için, kaynak ayırmak istiyorsanız ya bunu silip farklı bir tahsisat yöntemiyle yeniden ekleyebilirsiniz veya kaynağı görevlere ekleyip, **Mutabakat** sekmesinde **Ayırmaları Uzat** 'ı kullanarak atamalar için ayırmalar oluşturabilirsiniz.

## <a name="allocation-methods-that-lead-to-overbooking"></a>Fazladan ayırmaya neden olan tahsisat yöntemleri
Özetlemek gerekirse, kaynak zaten başka projelerde (veya başka iş emirleri ya da zamanlanabilir varlıklar için) ayrıldıysa, aşağıdaki tahsisat yöntemleri fazladan ayırmaya neden olur:

- Tam Kapasite
- Yüzde Kapasite
- Saatleri Eşit Dağıt

Bu üç ayırma yönteminden birini kullanırken, fazladan kaynak ayırma bildirimi almazsınız. Fazladan ayırmayı düzeltmek için Zamanlama panosunu kullanmanız gerekecektir.
