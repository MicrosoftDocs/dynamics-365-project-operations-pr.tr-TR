---
title: Project Service Automation'dan Project Operations'a proje zamanlama dönüştürme işlemi
description: Bu makale, Microsoft Dynamics 365 Project Service Automation'dan Dynamics 365 Project Operations'a gerçekleştirilen özellik değişikliklerine genel bir bakış sağlar.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/07/2022
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
ms.openlocfilehash: 84a40fcc9a8561c4ade0be175b08f701f3196508
ms.sourcegitcommit: 28004d38800782540fa5642d41f8fe0f6e2d9fa5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2022
ms.locfileid: "9642593"
---
# <a name="project-service-automation-to-project-operations-project-scheduling-conversion-process"></a>Project Service Automation'dan Project Operations'a proje zamanlama dönüştürme işlemi

Bir proje, Microsoft Dynamics 365 Project Service Automation 3.X'ten Dynamics 365 Project Operations Lite'a başarılı bir şekilde yükseltildikten sonra görev ızgarası iş kırılım yapısında (WBS) projeleri düzenlemek mümkün olmaz. Müşteriler görevle ilgili tüm ayrıntıları sağlamak için yeni alanların eklendiği izleme kılavuzundaki WBS'yi gözden geçirebilecektir. WBS'de yapılan düzenlemelerin gerekli olduğu projelerde, Project for the Web zamanlama deneyimi için uygun projeleri seçici olarak dönüştürebilirsiniz.

## <a name="project-conversion-process"></a>Proje dönüştürme süreci

Projeyi dönüştürmek için aşağıdaki adımları izleyin.

1. Projenin ana sayfasını açın ve eylem bölmesinde **Dönüştür**'ü seçin.
1. Onay iletisi kutusunda **Tamam** seçeneğini belirleyerek proje dönüştürmesini başlatın. Aşağıdaki eylemler meydana gelir:

    1. Projenin ana sayfa durumlarında görünen bir ileti çubuğu şu mesajı gösterir: "Proje zamanlaması dönüştürülüyor. Dönüştürme işlemi tamamlanana kadar projede değişiklik yapamazsınız. "
    1. Proje listesine yeniden yönlendiriliyorsunuz.

    Proje dönüştürme işlemi tamamlandıktan sonra aşağıdaki eylemler gerçekleşir:

    1. Atanan proje yöneticisi uygulamanın sağ tarafında bir bildirim alır.
    1. Dönüştürmenin devam ettiğini bildiren ileti çubuğu kaldırılır.
    1. **Zamanlama** sekmesi, Project for the Web'in yeni zamanlama deneyimini gösterir. Uygun lisansları ve güvenlik rollerine sahip herhangi bir Kullanıcı WBS'yi düzenleyebilir.
    1. **Zamanlama altyapısı** alanı **Project for the Web** olarak güncelleştirilir.
    1. **Dönüştür** düğmesi eylem bölmesinden kaldırılır.

> [!IMPORTANT]
> Projelerin toplu dönüştürülmesine izin verilmez. Aynı anda büyük bir proje birimini güncelleştirme girişimleri kısıtlanacak. Bu sınırlama, tüm müşteriler için yüksek performansın sağlanmasına yardımcı olur.

## <a name="manual-tasks-vs-automatic-tasks"></a>El ile yapılan görevler ve otomatik görevler

Bir ortam, Project Service Automation'dan Project Operations'a yükseltildiğinde, WBS'deki tüm görevler otomatik olarak zamanlanmış kabul edilir. El ile zamanlanmış görevler kavramı Project for the Web'de yoktur. Ancak, yeni projeler oluştururken [zamanlama modu](/project-management/scheduling-modes.md) ayarını kullanarak projeleriniz için tercih edilen zamanlama davranışını tanımlayabilirsiniz.

## <a name="restricted-operations-for-pre-conversion-projects"></a>Dönüştürme öncesi projeler için sınırlı operasyonlar

Bu bölümde, projeler dönüştürülmedikleri zaman bekleyebileceğiniz işlevsel farklılıklar ana hatlarıyla açıklanmaktadır.

### <a name="copy-project"></a>Projeyi kopyala

**Kopyalama** işlemi yalnızca dönüştürülen projelerde desteklenir. Yükseltilen projeler dönüştürme işleminden önce kopyalanamaz.

### <a name="move-project"></a>Projeyi taşı

Projenin başlangıç tarihindeki bir değişiklik, proje dönüştürülmediği sürece görevlerin başlangıcını orantılı olarak taşımaz.

## <a name="frequently-asked-questions"></a>Sık sorulan sorular

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>Yükseltme tamamlandıktan sonra oluşturulan dönüştürülen projeler ve yeni projeler arasındaki farklar nelerdir?

Ortam yükseltildikten sonra dönüştürülen projeler için, çizelgeye yalnızca proje takvimini dikkate almaya yönlendiren bir bayrak ayarlanır. Bu davranış, Project Service Automation'daki davranışla eşleşir. Ancak, yükseltmeden sonra oluşturulan yeni projeler için bayrak ayarlanmayacaktır. Bu nedenle, zamanlama, görevlere atanan kaynakların çalışma saatlerini dikkate alır.

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>Projemin dönüştürülmediğinde ne yapmam gerekir?

Projeniz dönüştürülemezse, ilk adım WBS ile ilgili ortak sorunları belirlemek için hata günlüklerini gözden geçirmeniz gerekir. Günlükler, üzerinde eylem yapabileceğiniz belirli bir hatayı belirtmezse, servis talebinin daha fazla gözden geçirilip geçirilmeyeceğini müşteri desteğine başvurun.

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>İş kapanışlarının Project for the Web'de nasıl ele alınır?

Project for the Web, kuruluşun organizasyon düzeyinde tanımladığı işletmenin kapanışlarını dikkate göstermez. Ancak, belirli bir çalışma saati şablonunda tanımlı olan diğer gün türlerine göre daha fazla olur.

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Project for the Web ile ilgili sınırlamalar nelerdir?

Bkz. [Bir proje için iş kırılım yapısı oluşturma: Proje Kısıtlamaları](/project-management/create-wbs#project-limitations.md).

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>Maliyet ve satış tahminlerimde değişiklik yapılmasını bekleyebilir miyim?

Kaynak atama dağılımlarının yeniden hesaplandığı veya kaynak projeden farklı bir tarih sınırına düştüklerinde nadir olarak, satış ve maliyet tahminlerindeki farklılıkları görebilirsiniz. Yükseltme işleminin parçası olarak, olası herhangi bir zamanlama değişikliğini anlayabilmeleri için müşterilerin temsili örnek bir proje kümesini sınaması beklenir.
