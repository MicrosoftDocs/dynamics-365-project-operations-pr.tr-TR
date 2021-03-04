---
title: Zamanlama panosundan bir proje ayırma oluşturma
description: Bu konu zamanlama panosundan bir proje kaydı oluşturma hakkında bilgi sağlar.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 7032af78168c742ac64cb2a7174cabcbda579ff8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146552"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a>Zamanlama panosundan bir proje ayırma oluşturma

[!include [banner](../includes/psa-now-project-operations.md)]

Bir kaynağı bir projeye projenin **Takım** sekmesinden doğrudan ayırarak veya bir genel takım üyesi atamasından bir kaynak gereksinimi oluşturup, oluşturulan gereksinimi bir proje takımı üyesiyle karşılayarak ayırabilirsiniz.

Kaynağı projeye doğrudan Zamanlama panosundan da ayırabilirsiniz. Bunu yapmanın üç yolu vardır:

- **Oluşturulan bir kaynak gereksiniminden ayırma:** Genel bir kaynak oluşturduktan ve bir proje içinde görevler atadıktan sonra bir kaynak gereksinimi oluşturabilirsiniz.

- **Birincil gereksinimden ayırma:** Birincil gereksinimler **Proje** sekmesindeki Zamanlama panosunda görünür. 

- **Yeni bir kaynak gereksiniminden ayırma:** Sıfırdan bir kaynak gereksinimi oluşturabilir ve bunu bir projeyle ilişkilendirebilirsiniz. Zamanlama panosunda, kaynak gereksinimi **Açık Gereksinimler** sekmesinde görünür.

## <a name="book-from-a-generated-resource-requirement"></a>Oluşturulan bir kaynak gereksiniminden ayırma

Genel bir kaynak oluşturup bir projedeki bir veya birden fazla göreve atayabilirsiniz. Ardından, genel takım üyesinden bir kaynak gereksinimi oluşturun. 

1.  Zamanlama panosunda, bu kaynak **Açık Gereksinimler** sekmesinde görünür. Çok sayıda açık gereksiniminiz varsa kılavuzda sütun filtreleri kullanmanız gerekebilir. 

    ![Zamanlama panosunda Gereksinimleri Aç sekmesi](media/FAQ-Project-Booking-Schedule-Board-1.png "Ayırmalar ve atamalar tablosunun ekran görüntüsü")

2. Gereksinimi seçin. **Kullanılabilirliği Bul** sekmesi, seçili satırın üst kısmında görünür.
 
3. Sekmeyi seçtiğinizde, Zamanlama panosunun Zamanlama Yardımcısı modu açılır ve kaynak gereksinimini karşılayan kullanılabilir kaynakları filtreler. Bundan sonra, bir kaynağı ayırabilirsiniz.

4. Ayrıca, seçilen satırı Zamanlama panosunun alt kısmından sürükleyip yukarıdaki kılavuzda bir kaynak hücresine bırakabilirsiniz. Bıraktığınız zaman sağ taraftaki **Kaynak Ayırma Oluştur** panelini açar.

    **Ayır** seçilince, kaynak proje takımına ayrılır.

![Kaynak Ayırma Oluştur paneli](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a>Birincil Gereksinimden ayırma

Project Service'te bir proje oluşturulunca, otomatik olarak Birincil Gereksinim adı verilen bir kaynak gereksinimi oluşturulur. Birincil Gereksinim, bir gereksinim üretmeden veya sıfırdan bir gereksinim oluşturmadan, Zamanlama panosuyla bir kaynağı hızlı bir şekilde ayırmak için kullanılan boş bir gereksinimdir. Gereksinim boş olduğundan, tahsisat yöntemi ve varsa saatlerin yanı sıra tarihleri belirtmeniz gerekir. 

1. Birincil Gereksinimle bir kaynak ayırmak için, Zamanlama panosunda **Proje** sekmesini seçin. Çok sayıda projeniz varsa, **Proje** sütununda sütun filtresi kullanmanız gerekebilir.

   ![Zamanlama panosunda sütun filtreleri](media/FAQ-Project-Booking-Schedule-Board-2.png "Ayırmalar ve atamalar tablosunun ekran görüntüsü")

2. Yalnızca ad olarak proje adını taşıyan ve süresi sıfır (0) olan gereksinimi seçin.

3. Satırda görünen **Kullanılabilirliği Bul** sekmesini seçin. Bu, Zamanlama panosunu Zamanlama Yardımcısı moduna sokar ve projeye ayrılabilecek kullanılabilir kaynakları gösterir.

4. **Birincil Gereksinim** sıfır (0) süreli ve boş bir gereksinim olduğu için, bir kaynağı seçer ve ayırırken, **Kaynak Ayırmayı Oluştur** panelinde süreyi ayarlamanız gerekir.

5. Zamanlama panosunun alt kısmındaki **Proje Birincil Gereksinimini** de seçebilir ve sürükleyip bir kaynakta bırakarak ayırabilirsiniz.
 
    **Birincil Gereksinim** sıfır (0) süreli ve boş bir gereksinim olduğu için, bir kaynağı seçer ve ayırırken **Kaynak Ayırmayı Oluştur** panelinde süreyi ayarlamanız gerekir.
 
    Zamanlama panosunda **Birincil Gereksinimden** bir kaynak ayırırken, kaynağı herhangi bir atama olmadan proje takımına eklersiniz.
 
## <a name="book-from-a-new-resource-requirement"></a>Yeni bir kaynak gereksiniminden ayırma
Yeni bir kaynak gereksiniminden ayırma gerçekleştirmek için aşağıdaki adımları izleyin. 

1. **Kaynak Gereksinimleri**'ne gidin ve ardından **Yeni**'yi seçerek yeni bir kaynak gereksinimi oluşturun.

2. **Proje** sekmesinde, gereksinimi projeyle ilişkilendirmek için bir proje seçin.
 
    Zamanlama panosunda, yeni oluşturulan bu gereksinim karşılayabileceğiniz bir **Açık Gereksinim** olarak görünür.

3. Proje takımına eklemek için kaynağı ayırın.

4. Kaynak artık ayrıldığı için, görevleri el ile atamanız gerekir.



[!INCLUDE[footer-include](../includes/footer-banner.md)]