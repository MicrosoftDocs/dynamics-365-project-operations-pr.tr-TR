---
title: Bir projenin durumunu izle
description: Project Service'ta bir projenin durumunu izleme
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 70d07c98bd9432712e939445dbf867b96642f5ba
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086410"
---
# <a name="track-a-projects-status-project-service"></a>Bir projenin durumunu izleme (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Bir istemcinin projesinin ilerleme durumunu izlemek için [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] kullanın.  

Katılım ilerledikçe, proje aşamaları katılım aşamasını yansıtmak için güncelleştirilir:  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   **Yeni**    | Bir proje oluşturduğunuzda, aşama **Yeni** olarak ayarlanmaktadır. Projeyi bir şablondan oluşturduysanız, bu aşamada proje zamanlama, tahminler ve takım verilerine sahip olabilir. Aksi takdirde, projenin taslağı olacaktır ve diğer proje bileşenlerinin geri kalanını el ile girmeniz gerekecektir. |
|  **Teklif**   |      Bir projeyi teklifle ilişkilendirdiğinizde veya tekliften oluşturduğunuzda, proje aşaması **Teklif** olarak ayarlanır ve tahmini başlangıç ve bitiş tarihleri de güncelleştirilir. Proje teklif aşamasındayken, teklif hakkındaki ayrıntılar **Proje** sayfasındaki **Satış** sekmesinde görüntülenir.      |
|   **Plan**   |                                     Bir projeyle ilişkili teklifi kazandığınızda ve katılım sözleşme aşamasında ilerlediğinde, proje aşaması **Plan** olarak güncelleştirilir. Sözleşme ayrıntıları **Proje** sayfasındaki **Satış** sekmesinde görüntülenir.                                      |
| **Tamamla** |                    Proje işi tamamlandığında, aşamayı **Tamamlandı** olarak değiştirebilirsiniz. Proje aşamasını tamamlandı olarak ayarlandığında, işin %100 tamamlanmış olduğu ancak projenin herhangi bir bekleme süresi veya gider girdilerinin kaydedilmesi için açık tutulduğu anlaşılır.                     |
|  **Kapat**   |           Proje ile ilgili tüm işlemler kaydedildiğinde ve başka bir şeyin eklenmesini beklemediğinizde, aşamayı el ile **Kapat** olarak ayarlayabilirsiniz. Projede **Kapat** olarak ayarlandığında, proje üzerinde daha fazla işlem yapamazsınız ve proje salt okunur olacaktır.           |

## <a name="to-track-a-projects-status"></a>Bir projenin durumunu izlemek için  

1.  **Project Service > Projeler** 'e gidin.  

2.  Üzerinde çalışmak istediğiniz projeye tıklayın.  

3.  Ekranın en üstünde bulunan çubukta, proje adının yanındaki aşağı oku seçin ve ardından **Proje İzleme** 'ye tıklayın.  

4.  Görev listesi üzerindeki açılan listede **Çalışma İzleme** veya **Maliyet İzleme** 'yi seçin.  

5.  Herhangi bir görevi düzenlemek için çift tıklayın. Bir görevin zaman ve ilerlemesini değiştirmek için Gantt grafiğindeki çubukları taşıyabilir veya yeniden boyutlandırabilirsiniz.  

### <a name="see-also"></a>Ayrıca bkz.  
 [Proje Yöneticisi Kılavuzu](../psa/project-manager-guide.md)
