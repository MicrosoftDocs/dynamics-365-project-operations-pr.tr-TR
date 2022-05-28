---
title: Kaynak yöneticisi değişiklikleri (Project Service Automation 3.x)
description: Bu konu, Kaynak yönetimi alanındaki değişiklikler hakkında bilgi sağlar.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: d19b8b453c544bb4c6fd11a8b9f750cb08e0c168
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595522"
---
# <a name="resource-management-changes-project-service-automation-3x"></a>Kaynak yöneticisi değişiklikleri (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

Bu konunun bölümleri, Dynamics 365 Project Service Automation sürüm 3.x'in Kaynak yönetimi alanında yapılan değişiklikler hakkında bilgi sağlar.

## <a name="project-estimates"></a>Proje tahminleri

Proje tahminleri **msdyn\_projecttask** varlığını (**Proje Görevi**) temel almak yerine **msdyn\_resourceassignment** varlığını (**Kaynak Atama**) temel alır. Kaynak atamaları, görev zamanlama ve fiyatlandırma için "gerçek değerin kaynağı" haline geldi.

## <a name="line-tasks"></a>Satır görevleri

PSA 3.x'te satır görevleri güncel değildir (kullanım dışı). Atamalar artık satır görevleri yerine tüm görevi işaret eder.

Aşağıdaki örnek, "Test görevi" adlı bir görevin, A ve B takım üyelerine PSA'nın önceki sürümlerinde ve PSA 3.x'te nasıl atandığını gösterir.

- **PSA 3.x'ten önce:**

    - Test görevi

        - Test görevi – Satır görevi 1

            - A'ya Atama

        - Test görevi – Satır görevi 2

            - B'ye Atama

- **PSA 3.x:**

    - Test görevi

        - A'ya Atama
        - B'ye Atama

## <a name="unassigned-assignment"></a>Atanmamış atama

PSA 3.x'te atanmamış bir atama, bir **BOŞ** takım üyesine ve bir **BOŞ** kaynağa atanmış bir atamadır. Atanmamış atamalar birkaç senaryoda gerçekleşebilir:

- Bir görev oluşturulmuş ancak henüz herhangi bir takım üyesine atanmamışsa, atanmamış bir atama her zaman oluşturulur. 
- Bir görevdeki tüm atamalar kaldırılırsa bu görev için atanmamış bir atama yeniden oluşturulur.

## <a name="scheduling-fields-on-the-project-task-entity"></a>Proje Görevi varlığındaki zamanlama alanları

**msdyn\_projecttask** varlığındaki alanlar kullanım dışı bırakıldı veya **msdyn\_resourceassignment** varlığına taşındı ya da bu alanlara artık **msdyn\_projectteam** varlığından (**Proje Takım Üyesi**) başvuruluyor.

| msdyn\_projecttask (Proje Görevi) varlığındaki kullanım dışı alan | msdyn\_resourceassignment (Kaynak Atama) varlığındaki yeni alan | Açıklama |
|---|---|---|
| msdyn\_assignedresources | Yok | |
| msdyn\_assignedteammembers | Yok | |
| msdyn\_numberofresources | Yok | |
| msdyn\_scheduledhours | Yok | |
| msdyn\_effortcontour | msdyn\_plannedwork | Alanda saklanan JavaScript Nesne Gösterimi (JSON) veri yapısının biçimi değiştirildi. |

## <a name="schedule-contour"></a>Zamanlama sınırı

Zamanlama sınırı her **Kaynak Atama** varlığının (**msdyn\_resourceassignment**) **Planlanan İş** alanında (**msdyn\_plannedwork**) depolanır.

### <a name="structure"></a>Yapı

Zamanlama sınırının yeni yapısı, zamanlamanın her günü için tanımlanan esnek zaman dilimlerinden oluşur. Her zaman dilimi aşağıdaki özellikleri sahiptir:

- **Başlangıç**: Proje takvimine göre günün çalışma saatlerinin başlangıcı.
- **Bitiş**: Proje takvimine göre günün çalışma saatlerinin bitişi.
- **Saatler**: Günde atanan saat sayısı.

**Örnek**

Bu örnek, UTC-8 saat diliminde iş gününün sabah 9'dan akşam 5'e kadar olduğu bir proje takvimi kullanır.

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a>Otomatik zamanlama ve el ile zamanlama

Görev otomatik zamanlanmışsa saatler ön yüklemelidir ve görev süresi azaltılabilir.

**Örnek**

Aşağıdaki görev, üç günde 18 saat için otomatik zamanlanmıştır (3 Aralık 2018 - 5 Aralık 2018).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

Görev el ile zamanlanırsa saatler tüm tarihlere eşit olarak dağıtılır.

**Örnek**

Aşağıdaki görev, üç günde 18 saat için el ile zamanlanmıştır (3 Aralık 2018 - 5 Aralık 2018).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a>Atama birimi

PSA 3.x'te atama birimi kullanım dışı bırakıldı. Görev çalışma saatleri artık tüm atanan kaynaklar arasında her gün eşit olarak bölünür.

**Örnek**

Bu örnekte, görev iki kaynağa atanmıştır ve üç günde 36 saat için (3 Aralık 2018 - 5 Aralık 2018) otomatik olarak zamanlanır.

- Atama 1:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- Atama 2:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a>Fiyatlandırma boyutları

PSA 3.x'te, kaynağa özel fiyatlandırma boyutu alanları (**Rol** ve **Kuruluş Birimi**), **msdyn\_projecttask** varlığından kaldırılmıştır. Bu alanlar artık proje tahminleri üretildiğinde kaynak atamasının (**msdyn\_resourceassignment**) ilgili proje takımı üyesinden (**msdyn\_projectteam**) alınabilir. **msdyn\_projectteam** varlığına yeni bir alan (**msdyn\_organizationalunit**) eklendi.

| msdyn\_projecttask (Proje Görevi) varlığındaki kullanım dışı alan | Bunun yerine msdyn\_projectteam varlığından (Proje Takımı Üyesi) kullanılan alan |
|---|---|
| msdyn\_resourcecategory | msdyn\_resourcecategory |
| msdyn\_organizationalunit | msdyn\_organizationalunit |

## <a name="contours"></a>Sınırlar

Fiyatlandırma ve tahmin sınırı alanları **msdyn\_projecttask** varlığında kullanım dışı bırakılmıştır. Bunlar **msdyn\_resourceassignment** varlığına taşınmıştır.

| msdyn\_projecttask (Proje Görevi) varlığındaki kullanım dışı alan | msdyn\_resourceassignment (Kaynak Atama) varlığındaki yeni alan |
|---|---|
| msdyn\_costestimatecontour | msdyn\_plannedcostcontour |
| msdyn\_salesestimatecontour | msdyn\_plannedsalescontour |

Aşağıdaki alanlar **msdyn\_resourceassignment** varlığına eklenmiştir:

* msdyn\_plannedcost
* msdyn\_plannedsales

**msdyn\_projecttask** varlığındaki planlanan, gerçek ve kalan maliyet ve satışlar için aşağıdaki alanlar değişmemiştir:

* msdyn\_plannedcost
* msdyn\_plannedsales
* msdyn\_actualcost
* msdyn\_actualsales
* msdyn\_remainingcost
* msdyn\_remainingsales


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
