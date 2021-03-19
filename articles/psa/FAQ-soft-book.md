---
title: Kaynağı geçici ayırma
description: Bu konu, proje takımı üyelerini geçici olarak zamanlama veya geçici ayırmayla ilgili bilgi sağlar.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/25/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.app:
- ProjectOperations
ms.openlocfilehash: 1d2044692d1c6d694a1365be76dd8e7ddafd376d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286002"
---
# <a name="soft-book-a-resource"></a>Kaynağı geçici ayırma

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Kaynağı projeye atamayı planladığınızı göstermek için bir proje takımına geçici olarak zamanlayabilir veya "geçici ayırabilirsiniz". Geçici ayırmalar bir kaynağın kullanılabilir kapasitesini tüketmez ve geçici olarak ayrılmış takım üyelerini proje görevlerine atayabilirsiniz. Bununla birlikte, geçici ayırma bir kaynağın kapasitesini tüketmediğinden, aynı dönemdeki diğer görevler için kaynağı "kesin ayırabilirsiniz". Genel kaynaklar geçici ayrılamaz ve geçici ayırma, genel kaynak isteğini karşılayamaz.

Geçici ayrılan proje takımı üyeleri **Proje** sayfasının **Takım** sekmesinde listelenir ve **Adlandırılmış Kaynaklar** görünümündeki **Geçici Ayrılan Saat Sayısı** sütununda geçici ayrılmış saatler gösterilir. Geçici ayrılmış takım üyeleri, Zamanlama panosunda da listelenir. Üyeler geçici ayrıldığı için, Zamanlama panosunda bu kaynaklar için herhangi bir kapasite tüketimi gösterilmez. Geçici ayrılan süre **Mutabakat** sekmesinde ve **Mutabakat** sekmesindeki **Ayırmaları Uzat** alanında görünmez. 

Bir takım üyesini bir projeye geçici ayırmak için iki yol vardır: Zamanlama panosundan doğrudan veya **Takım** sekmesinde takım üyesini ekleyerek. 

## <a name="soft-book-from-the-schedule-board"></a>Zamanlama panosundan geçici ayırma
Zamanlama panosundan kaynağı geçici ayarlamak için aşağıdaki adımları izleyin. 

1. Zamanlama panosunu açın ve **Ayırma Gereksinimleri** panelinde **Proje** sekmesini seçin.
2. Kaynağı geçici ayırmak istediğiniz projeyi bulun. Listede çok sayıda proje varsa, **Proje** sütun başlığını seçin ve ardından bir veya daha fazla proje aramak için filtreyi kullanın.
3. Projeyi seçin, sürükleyin ve kaynağın zaman kılavuzuna bırakın.
5. **Kaynak Ayırma Oluştur** panosunda başlangıç ve bitiş tarihini ayarlayın, **Kayıt Durumunu** **Geçici** olarak ayarlayın ve ardından saatleri ayarlayın. 
6. **Ayır**'a tıklayın. Kaynak artık **Takım** sekmesinde proje için bir kaynak olarak görünür. **Adlandırılmış Takım Üyesi** görünümünde, geçici ayrılan saat sayısını **Geçici Ayrılan Saat Sayısı** sütununda görürsünüz.

> [!NOTE]
> Artık geçici ayrılanları **Zamanlama** sekmesindeki görevlere atayabilirsiniz. **Mutabakat** sekmesinde kaynak, görev atamasına göre bir ayırma eksikliği gösterir çünkü **Mutabakat** sekmesinde yalnızca kesin ayırmalar dikkate alınır. Kaynak atamalarına göre kesin ayırma eksikliğini önlemek için, kaynağı kesin ayırırken **Ayırmaları Uzat** özelliğini kullanabilirsiniz. Kaynağın geçici ayırmasını **Ayırmaları Koru**'yu kullanarak el ile iptal etmeniz gerekecektir.

## <a name="soft-book-on-the-team-tab"></a>Takım sekmesinde geçici ayırma

Takım üyelerini **Takım** sekmesinde doğrudan ekleyebilir ve **Ayırmaları Koru** özelliğiyle, ayırma durumlarını **Kesin**'den **Geçici**'ye çevirebilirsiniz. Bu yolla bir takım üyesi eklediğiniz zaman, tahsisat yöntemi olarak **Hiçbiri**'ni seçmediğiniz sürece sonuç her zaman kesin ayırma olacaktır.

Bu yöntemi kullanmak için aşağıdaki adımları uygulayın.

1. **Proje** sayfasında, **Takım** sekmesinde, **Yeni**'ye tıklayın.
2. Ayrılabilir kaynağı, rolü ve başlangıç/bitiş tarihlerini seçin.
3. **Hiçbiri** dışındaki bir tahsisat yöntemini seçin:
4. **Kaydet**'i seçin. Kılavuzda kaynağı ve **Kesin Ayrılan Saat Sayısı** sütununda kaynağın saat sayısını görürsünüz.
5. **Ayırmaları Koru**'yu seçerek, kaynağın ayırmalarını koruyun.
6. Zamanlama panosu açılınca, kaynağı genişleterek ayırmalarını görünür hale getirin. Ayırmayı **Kesin** olarak belirtilmiş halde görürsünüz.
7. Ayırmaya sağ tıklayın, **Durumu Değiştir** altında **Geçici Ayırma** \> **Geçici**'yi seçin. Ayırma durumu artık **Geçici**'dir.
8. Zamanlama panosunu kapattıktan sonra, **Adlandırılmış Takım Üyeleri** görünümüne baktığınız zaman, **Takım** sekmesi kılavuzunda, kaynağın saat sayısının **Kesin Ayrılan Saat Sayısı** sütunundan **Geçici Ayrılan Saat Sayısı** sütununa geçtiğini göreceksiniz.

> [!NOTE]
> **Kesin** olan durumu **Geçici**'ye çevirmek için **Ayırmaları Koru**'yu kullandığınızda Bir kaynağı takıma kesin olarak ayırıp zamanlamadaki görevlere atarsanız o kaynağın görev atamalarını koruyacağını unutmayın. Bununla birlikte, **Mutabakat** sekmesinde, kaynakta bir ayırma eksikliği olacaktır çünkü ayırmaların atamalara göre mutabakatı yapılırken yalnızca kesin ayırmalar hesaba katılır. Kaynak atamalarına göre kesin ayırma eksikliğini önlemek için, kaynağı kesin ayırırken **Mutabakat** sekmesindeki **Ayırmaları Uzat** özelliğini kullanabilirsiniz. Kaynağın geçici ayırmasını **Ayırmaları Koru**'yu kullanarak iptal etmeniz gerekecektir.

Geçici olarak ayrılmış bir takım üyesi kaynağını, kesin olarak ayrılmış bir takım üyesine çevirmeye hazır olunca aşağıdakileri yapın:

1. Zamanlama panosunda, kaynağı genişleterek ayırmalarını görünür hale getirin. Ayırmayı **Geçici** şeklinde görürsünüz.
2. Ayırmaya sağ tıklayın, **Durumu Değiştir** altında **Kesin Ayırma** \> **Kesin**'i seçin. Ayırma durumu artık **Kesin**'dir.
3. Zamanlama panosunu kapattıktan sonra projeye dönün ve **Takım** sekmesini açın; **Adlandırılmış Takım Üyeleri** görünümünde, **Takım** sekmesinde, kaynağın saat sayısının **Geçici Ayrılan Saat Sayısı** sütunundan **Kesin Ayrılan Saat Sayısı** sütununa geçtiğini görürsünüz. Kaynak görevlere atandıysa, ayırmaları artık kesin olduğu için, **Mutabakat** sekmesinde bir ayırma eksikliği göstermeyecektir.



[!INCLUDE[footer-include](../includes/footer-banner.md)]