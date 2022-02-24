---
title: Zamanlama yardımcısına genel bakış
description: Bu konuda, kaynakları ayırmak için Zamanlama yardımcısı ile çalışma hakkında bilgiler sağlanmaktadır.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: da551e805f395e466952df1dbb7d193bdddba358
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086180"
---
# <a name="schedule-assistant-overview"></a>Zamanlama yardımcısına genel bakış

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Zamanlama yardımcısı, Proje yöneticisi tarafından tanımlanan gereksinimlere göre kaynakları ayırmak için kullanılır. Zamanlama yardımcısı, kaynağı bulmak için kaynak gereksiniminde sağlanan parametreleri kullanır. Zamanlama yardımcısı, zaman aralıkları veya gerekli beceriler gibi ilgili gereksinimlerle eşleşen kaynaklar önerir.

Uygun kaynaklar tanımlandıktan sonra Kaynak veya Proje yöneticisi, iş için kaynağı ayırabilir.

## <a name="prerequisites"></a>Ön koşullar

Zamanlama yardımcısı, Universal Resource Scheduling çözümünün bir parçasıdır. Bu çözüm, Dynamics 365 Project Operations, Dynamics 365 Field Service ve Dynamics 365 Customer Service uygulamalarına dahildir ve bunlarla birlikte yüklenir.

## <a name="matching-requirements-and-resources"></a>Eşleştirme gereksinimleri ve kaynaklar

Oluşturulan kaynak gereksinimi, aşağıdaki gibi ayrıntıları temel alır:

-   Özellikler
-   Roller
-   Departmanlar
-   Kaynak tercihleri
-   Çalışma sınırları
-   Saat dilimi

Zamanlama yardımcısı, bu ayrıntıları kaynakları filtrelemek için kullanır.

## <a name="launch-the-schedule-assistant"></a>Zamanlama yardımcısını başlatma

Zamanlama yardımcısını başlatmanın iki yolu vardır. Karma modu kullanıyorsanız takım üyesi ızgarasında, karşılanmayan kaynak gereksinimi olan herhangi bir takım üyesini seçip ardından **Ayır**'ı seçebilirsiniz. Merkezi modu kullanıyorsanız Kaynak yöneticisi kaynağı bulup seçer.

## <a name="schedule-assistant-filters"></a>Zamanlama yardımcısı filtreleri

Zamanlama yardımcısı çalıştırıldıktan sonra kaynak gereksiniminin ayrıntıları, sol bölmede filtrelenmiş değerler olarak görüntülenir. Kaynak yöneticisi veya Proje yöneticisi, zamanlama gereksinimlerini karşılamak için filtreleri ayarlayarak sonuçlarda hassas ayar yapabilir.

Filtre bölmesi, aşağıdakiler dahil işle ilgili seçenekleri gösterir:

-   İş başlangıcı ve bitişi
-   Özellikler
-   Roller
-   Kuruluş birimleri
-   Kaynak atayan şirket
-   Kaynak türleri
-   Tercih edilen kaynaklar
