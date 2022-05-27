---
title: Project Service Automation Güncelleştirme Sürümü 16, V3'teki yenilikler veya değişiklikler
description: Bu konuda, Project Service Automation, Güncelleştirme Sürümü 16, V3'teki özellikler ve düzeltmeler listelenir.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: 5651f8b3a2ddf406fcfd7a4e21901c53789fa4ed
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577398"
---
# <a name="project-service-automation-update-release-16-v3"></a>Project Service Automation, Güncelleştirme Sürümü 16, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Dynamics 365 için Project Service Automation uygulamasına yönelik en son güncelleştirmeyi duyurmaktan mutluluk duyuyoruz. Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir.  Bu sürüm Dynamics 365 9.x ile uyumludur. Bu sürüme güncelleştirmek için Dynamics 365 online Yönetim Merkezi'ni ziyaret edin ve çözümler sayfasından güncelleştirmeyi yükleyin. Daha fazla bilgi için bkz. [Tercih Edilen Çözümü Yükleme, Güncelleştirme](/dynamics365/project-service/upgrade-psa-home-page) bölümüne bakın.
Bu konuda, PSA V3, Güncelleştirme Sürümü 16'te yeni veya değiştirilmiş özellikler ve düzeltmeler listelenir. Bu sürüm, V3.10.6.34 derleme numarasına sahiptir ve Ocak 2020 tarihinde kendi kendine güncelleştirme ile genel kullanıma sunulmuştur.


## <a name="update-release-16"></a>Güncelleştirme Sürümü 16

### <a name="bug-fixes"></a>Hata düzeltmeleri

-   Zaman ve Gider

    -   Düzeltildi: Silinen zaman ve gider girişlerini onay için göndermeye çalışan kullanıcılar artık ilgili hata iletileri alacak.

-   Proje Yönetimi

    -   Düzeltildi: Şablonlarda takım üyeleri için tanımlanan kaynak belirleme birimleri, şablonlarla yeni projeye uygulanır.

    -   Düzeltildi: Kayıt sahipliği yeniden atama işlemi geliştirildi.

    -   Düzeltildi: Kopyalanma sürecindeki projelerin tüm kopyalama işlemleri tamamlanana kadar kopyalanmasına izin verilmeyecek.

-   Kaynak Yönetimi

    -   Düzeltildi: Ayırmaları uzatma işlemi artık kısa süreleri düzgün şekilde işliyor ve uzatılan ayırmalar için sıfır saat oluşturmuyor.

    -   Düzeltildi: Mutabakat görünümü artık proje saat dilimi +5:30 GMT olduğunda ve kullanıcının saati farklı olduğunda işliyor.

-   Sales

    -   Düzeltildi: Bir sözleşme satırına eşlenen bir proje kaldırıldığında ve yeni bir proje eşlendiğinde, yeni projedeki gerçek kayıtlar sözleşme satırında tanımlanan faturalama ve fiyatlandırma kurallarına göre yeniden değerlendirilmiyordu. Bu sorun, bu sürümde giderildi. Yeni eşlenen projedeki fiyatlandırma ve gerçek değer kayıtları tersine çevrilecek ve sözleşme satırının fiyatlandırma ve faturalama kurallarına göre doğru şekilde yeniden oluşturulacaktır. Eşlenmeyen projenin gerçek kayıtları da yeniden değerlendirilecek ve sonuç olarak yeniden oluşturulacaktır.

    -   Düzeltildi: Null değerlerin kalıcı olmamasını sağlamak için tahmin satırının **Tutar** alanına ek doğrulama eklendi.

    -   Düzeltildi: Bir projede gerçek değerler güncelleştirildiğinde, kullanıcıların gerçek değerleri yeniden eşitlemesine olanak sağlamak için proje ana formuna bir yenileme düğmesi eklendi.

    -   Düzeltildi: Kullanıcılar 2.X'ten 3. X'e yükseltme yaptığında, proje adı için NULL değerine sahip projelere izin verilecektir.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
