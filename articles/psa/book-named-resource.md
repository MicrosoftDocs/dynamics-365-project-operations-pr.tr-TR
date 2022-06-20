---
title: Kaynak gereksinimlerinden adlandırılmış kaynakları ayırma
description: Bu makale, genel bir kaynak gereksinimi için adlandırılmış kaynakları ayırma hakkında bilgi sağlar.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 9598490da1905227e517da8ba90f8ffd1df88566
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916266"
---
# <a name="book-named-resources-from-resource-requirements"></a>Kaynak gereksinimlerinden adlandırılmış kaynakları ayırma

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Kaynak gereksinimi olan genel kaynağı değiştirmek için adlandırılmış bir kaynak kullanabilirsiniz.

1. Project Service Automation'da (PSA) **Projeler** sayfasında **Takım** sekmesine tıklayın.
2. Listeden kaynak gereksinimi olan genel kaynağı seçin ve ardından **Ayır**'a tıklayın. Veya, kaynak gereksinimini açıp **Ayır**'a tıklayın.


![Genel takım üyesi ayırma.](media/RM-how-to-14.png)


3. **Zamanlama Yardımcısı** sayfasında, proje takımınıza ayırmak için adlandırılmış bir kaynak seçin ve ardından **Ayır**'a tıklayın.

![Zamanlama yardımcısını kullanarak genel takım üyesi ayırma.](media/RM-how-to-15.png)

Ayırma işlemi tamamlandığında ve bir adlandırılmış kaynak tarafından gerçekleştirildiğinde, genel kaynak adlandırılan kaynakla değiştirilir.

![Genel takım üyesinin yerine geçen adlandırılmış takım üyesi.](media/RM-how-to-16.png)

Zamanlamadaki atamalar da adlandırılan kaynakla güncelleştirilir.

![Proje görevlerine atanan adlandırılmış takım üyesi.](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Bir genel kaynağı birden çok adlandırılmış kaynakla karşılama
Bir genel kaynak için bir gereksinimin birden çok adlandırılmış kaynakla karşılama, tek bir adlandırılmış kaynak atamaya benzerdir. Örneğin, süresi beş gün olan ve 120 saat çalışma gerektiren bir görev var. Bu görev, haftasa beş gün günde sekiz saat çalışan bir kaynakla tamamlanamaz. 

![Beş gün boyunca 120 saatlik çalışma gerektiren bir görev.](media/RM-how-to-21.png)

Gereksinim beş gün boyunca 120 saat robotik mühendisliği içindir, bu da günde 24 saat çalışma gerektirir.

![Günlük gereksinim.](media/RM-how-to-22.png)

Bu, genel bir kaynak isteğini yerine getirmek için birden çok adlandırılmış kaynağın gerekli olduğu durum için bir örnektir. Gereksinimi karşılamak için birden fazla kaynak ayırmanız gerekir.

![Gereksinimi karşılamak için birden fazla kaynak ayırma.](media/RM-how-to-23.png)

Bu senaryodaki ana fark genel kaynağın göreve atanan takımda kalması ve ayrılan adlandırılmış kaynak takım üyelerinin pozisyonun parçası olarak atanmamasıdır. Proje yöneticisi, işi gerektiği gibi adlandırılmış kaynaklara atayabilir. **Mutabakat** görünümü, proje yöneticisinin ayırmaları birden çok görev ataması için birden çok kaynak arasında bölmesine yardımcı olabilir. Gereksinim oluşturan bir görev paketinizin olduğu ve proje yöneticisinin bunu atamak isteme amacının tahmin edilmesinin gerektiği gibi yukarıdaki basit örnekten daha karmaşık senaryolar olabileceğinden bu otomatik olarak gerçekleştirilmez. Sistem amacı anlayamadığından varsayımlar amaçlanandan farklı olabilir ve yanlış veya öngörülemeyen sonuçlara yol açabilir. Öngörülebilir sonuç, proje yöneticisi **Mutabakat** görünümünü kullanarak kaynakları bilerek oluşturana kadar genel kaynağın atanmış kalmasıdır.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
