---
title: İş kırılım yapısı için yükseltme hususları
description: Bu konu, iş kırılım yapısını Project Service Automation 2.x'ten 3.x'e yükseltme hakkında bilgi sağlar.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
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
ms.openlocfilehash: 169dc24f0d1ae151ea5927123fb738221de88250
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086406"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a>İş kırılım yapısı için yükseltme hususları
Bu konu, iş kırılım yapısını Project Service Automation 2.x'ten 3.x'e yükseltme hakkında bilgi sağlar. Bu konu, Project Service Automation (PSA) uygulamasında bir projenin başarılı yükseltme için gereken durumunu tanımlar. Ayrıca yükseltme işleminin başarısız olmasına neden olacak yaygın engelleme koşulları hakkında da bilgi verilmektedir. Proje görevlerini ve bir proje zamanlaması içindeki işlevlerini tanımlama hakkında daha fazla bilgi için [Proje zamanlamaları](project-creating.md) bölümüne bakın.

## <a name="key-entities"></a>Önemli varlıklar
Kaynaklarla yüklü doğru bir iş kırılım yapısı için aşağıdaki varlıklar gereklidir:

- [Proje](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [Proje Takımı](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [Proje Görevi](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [Kaynak Atamaları](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [Proje Görevi Bağımlılığı](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [Ayrılabilir Kaynaklar](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

Kaynağı yüklü bir iş kırılım yapısını tanımlamak için aşağıdaki adımları tamamlamanız gerekir:

1. Yeni bir proje oluşturun. Yeni proje oluşturma hakkında daha fazla bilgi için [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project) bölümüne bakın.
2. Bir veya daha fazla görev oluşturun. Görev oluşturma hakkında daha fazla bilgi için [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask) bölümüne bakın.
3. Görev bağımlılıklarını tanımlayın. Daha fazla bilgi için bkz. [Proje Görevi Bağımlılığı](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).
4. Proje takım üyelerini projeye atayın. Daha fazla bilgi için [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam) bölümüne bakın.
5. Proje takım üyelerini görevlere atayın. Daha fazla bilgi için [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment) bölümüne bakın.

## <a name="project-team-relationships"></a>Proje takım ilişkileri

Başarılı bir yükseltme yapıldığından emin olmak için aşağıdaki ilişkilerin doğru şekilde korunması gerekir:
- Tüm proje takım üyeleri bir ayrılabilir kaynakla ilişkili olmalıdır.
- Tüm proje takım üyeleri aynı projeyle ilişkili olmalıdır. 

## <a name="project-task-relationships"></a>Proje görev ilişkileri
Başarılı bir yükseltme yapıldığından emin olmak için aşağıdaki ilişkilerin doğru şekilde korunması gerekir:

- İlgili tüm görevlerin aynı projeyle ilişkili olmalıdır.
- Her satır görevinin bir ana görevi olmalıdır.
- Her görevin bir ana projesi olmalıdır.

### <a name="valid-conditions"></a>Geçerli koşullar

- Tüm görev süreleri, bir saat değerine eşit veya bu değerden çok (> =) ve 1.800.000 dakikadan (1.250 gün) az olmalıdır.*
- Tüm görevlerin başlangıç tarihi 01/01/2000 tarihinden önce olmalıdır.*
- Tüm görevlerin başlangıç tarihi şimdiki tarihten en geç 17 yıldan sonrası olmalıdır.*
- Tüm görevlerin başlangıç tarihi bitiş tarihinden önce veya bu tarih olmalıdır.
- Sınıflandırmalardaki tüm hareket türlerinin (Gider, Malzeme, Vergi ve Süre) **Varsayılan Birim** ve **Birim Grubu** değeri olmalıdır.
- Harflerle yazılan tarih biçimleri kullanılmamalıdır.

### <a name="potential-mitigation-steps"></a>Potansiyel risk azaltma adımları
- Proje kimliğini içermeyen Proje görevlerini tanımlamak için Gelişmiş Bul seçeneğini kullanın.
- Zamanlanmış sürenin 1.800.000'den fazla olduğu proje görevlerini tanımlamak için Gelişmiş Bul seçeneğini kullanın.
- Veri değişikliği yapmadan önce, verilerin hatalı duruma geçmesine neden olabilecek varlıkla ilişkili tüm özelleştirmeleri araştırmanız gerekir. Bu özelleştirmeler, veriyle ilgili herhangi bir güncelleştirme yapmadan önce incelenmelidir.
- Sahipsiz kalan tanımlı görevler için, gerekli değillerse veya doğru ana projeyle ilişkilendirilmeleri gerekiyorsa bu görevleri silebilirsiniz.
- Sürenin 1.250 günden fazla olduğu tüm görevlerde uygunsa, toplam süreyi temsil etmesi için ek görevler ekleyebilirsiniz.

> [!NOTE]
> Müşteri ilişkileri yönetiminin (CRM) yalnızca 7.320 yineleme genişletmesini desteklemesi nedeniyle yıldız (\*) işareti olan öğelerin sınırları vardır. Bu sınırın altında kalmanız gerekir.

## <a name="resource-assignment-relationships"></a>Kaynak Atama ilişkileri
Başarılı bir yükseltme yapıldığından emin olmak için aşağıdaki ilişkilerin doğru şekilde korunması gerekir:

- Bir iş kırılım yapısındaki tüm Kaynak Atamaları aynı projeyle ilişkili olmalıdır.
- Bir iş kırılım yapısındaki tüm Kaynak Atamaları aynı projedeki proje takım üyeleriyle ilişkili olmalıdır.

### <a name="potential-mitigation-steps"></a>Potansiyel risk azaltma adımları
- Yukarıda açıklanan koşulların dışında kalan tüm görevleri tanımlayın.  
- Artık geçerli olmayan tüm Kaynak Atamaları silinmelidir.

## <a name="project-task-dependency-relationships"></a>Proje görevi bağımlılığı durumu
Başarılı bir yükseltme yapıldığından emin olmak için aşağıdaki ilişkilerin doğru şekilde korunması gerekir:

- Tüm proje görevi bağımlılıkları aynı projeyle ilişkili olmalıdır.
- Bir görev için aynı bağımlılığa birden başvuru yapılamaz.
