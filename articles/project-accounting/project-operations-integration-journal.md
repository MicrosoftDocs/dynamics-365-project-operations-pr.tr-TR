---
title: Project Operations'da tümleştirme günlüğü
description: Bu makale, Project Operations'ta Entegrasyon günlüğü ile çalışma hakkında bilgi sağlar.
author: sigitac
ms.date: 06/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d6f1709c4bf44cfd45516d9ac74b30d4817bb653
ms.sourcegitcommit: a5a1d81d2fe0a6f684e79859fcddf45e913d76bc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/01/2022
ms.locfileid: "9106299"
---
# <a name="integration-journal-in-project-operations"></a>Project Operations'da tümleştirme günlüğü

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Zaman, gider, ücret ve materyal girişleri, bir projeyle ilgili tamamlanan çalışmanın operasyonel görünümünü temsil eden **Gerçek** işlemler oluşturur. Dynamics 365 Project Operations, işlemleri incelemek ve muhasebe özniteliklerini ihtiyaç duyulduğu şekilde ayarlamak için bir araç ile birlikte muhasebeciler sağlar. İnceleme ve ayarlamalar tamamlandıktan sonra işlemler, Proje yardımcı defterine ve Genel deftere nakledilir. Muhasebeciler, **Project Operations Tümleştirme** günlüğü (**Dynamics 365 Finance** > **Proje yönetimi ve muhasebe** > **Günlükler** > **Project Operations Tümleştirme** günlüğünü kullanarak bu etkinlikleri gerçekleştirebilir.

![Tümleştirme günlüğü akışı.](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Project Operations'da tümleştirme günlüğünde kayıt oluşturma

Project Operations Tümleştirme Günlüğü'ndeki kayıtlar, periyodik süreç kullanılarak oluşturulur, **Hazırlama tablosundan içe aktar**. Bu işlemi, **Dynamics 365 Finance** > **Proje yönetimi ve muhasebe** > **Dönemsel** > **Project Operations Tümleştirmesi** > **Hazırlama tablosundan içe aktar** bölümüne giderek gerçekleştirebilirsiniz. İşlemi etkileşimli olarak çalıştırabilir veya gerektiği gibi arka planda çalışacak şekilde yapılandırabilirsiniz.

Periyodik süreç çalıştığında Project Operations tümleştirme günlüğüne henüz eklenmemiş olan gerçek değerler bulunur. Her gerçek işlem için bir günlük satırı oluşturulur.
Sistem, yevmiye defteri satırlarını **Project Operations Tümleştirme günlüğü** alanında (**Finans** > **Proje yönetimi ve muhasebe** > **Kurulum** > **Proje yönetimi ve muhasebe parametreleri**, **Dynamics 365 Customer Engagement üzerinde Project Operations** sekmesi) seçili olan değere göre aynı yevmiye defterlerine gruplar. Bu alan için olası değerler şunlardır:

  - **Günler**: Gerçek tutarlar, işlem tarihine göre gruplandırılır. Her gün için ayrı bir günlük oluşturulur.
  - **Aylar**: Gerçek değerler takvim ayına göre gruplandırılır. Her ay için ayrı bir günlük oluşturulur.
  - **Yıllar**: Gerçek değerler takvim yılına göre gruplandırılır. Her yıl için ayrı bir günlük oluşturulur.
  - **Tümü**: Tüm gerçek işlemler aynı tümleştirme günlüğüne dahil edilir. Periyodik süreç çalışırken günlük kullanılamıyorsa, örneğin günlük hareketleri deftere nakletme sürecindeyse ise yeni bir günlük oluşturulur.

Günlük satırları, proje gerçek değerleri temel alınarak oluşturulur. Aşağıdaki listede daha fazla önemli varsayılan ve dönüşüm kuralı yer almaktadır:

  - Her proje gerçek işleminin Project Operations tümleştirme günlüğünde bir satırı vardır. Zaman ve malzeme faturalama türü için maliyet ve faturalandırılmamış satış işlemleri ayrı satırlarda gösterilir.
  - **Tarih** alanı işlem tarihini ifade eder. **Muhasebe tarihi** alanı, işlemin deftere kaydedildiği tarihi ifade eder. Muhasebe tarihi [kapatılmış bir mali dönem](/dynamics365/finance/general-ledger/close-general-ledger-at-period-end) içindeyse ve **Muhasebe tarihini açık defter dönemi olarak ayarla** parametresi **Proje yönetimi ve hesap oluşturma parametreleri** sayfasının **Finansal** sekmesinde ayarlandıysa sistem, işlemin muhasebe tarihini bir sonraki açık kayıt defteri döneminin ilk tarihine ayarlar.
  - **Makbuz** alanı, gerçek işlemlerin makbuz numaralarını gösterir. Makbuz numarası sırası, **Proje yönetimi ve muhasebe parametreleri** sayfasında **Numara sıraları** sekmesinde tanımlanır. Her satıra yeni bir numara atanır. Makbuz nakledildikten sonra **Makbuz işlemi** sayfasında **İlgili makbuzlar** seçeneği belirlenerek maliyet ve faturalandırılmamış satış işleminin nasıl ilişkili olduğunu görüntüleyebilirsiniz.
  - **Kategori** alanı, ilgili proje fiili için işlem kategorisine göre proje hareketini ve Varsayılanlarını temsil eder.
    - **Hareket kategorisi** Proje gerçek değerinde ayarlandıysa ve belirli bir tüzel kişilideki ilgili **proje kategorisi** varsa, kategori varsayılan olarak bu proje kategorisini alır.
    - Proje gerçek değerlerinde **İşlem kategorisi** ayarlanmadıysa sistem, **Proje yönetimi ve muhasebe parametreleri** sayfasında bulunan **Dynamics 365 Customer Engagement üzerinde Project Operations** sekmesinin **Proje kategorisi varsayılanları** alanındaki değeri kullanır.
  - **Kaynak** alanı, bu işlemle ilgili proje kaynağını ifade eder. Kaynak, müşterilere yapılan Proje fatura tekliflerinde başvuru olarak kullanılır.
  - **Döviz kuru** alanı, varsayılan olarak Dynamics 365 Finance uygulamasında ayarlanan **Döviz kuru** değerini alır. Döviz kuru ayarı eksikse **Hazırlamadan içer aktarma** periyodik süreci, kaydı bir günlüğe eklemez ve iş yürütme günlüğüne bir hata iletisi eklenir.
  - **Satır özelliği** alanı, proje gerçek değerlerindeki faturalama türünü ifade eder. Satır özelliği ve faturalama türü eşlemesi, **Proje yönetimi ve muhasebe parametreleri** sayfasındaki **Dynamics 365 Customer Engagement üzerinde Project Operations** sekmesinde tanımlanır.

Project Operations tümleştirme günlüğü satırlarında yalnızca aşağıdaki muhasebe öznitelikleri güncelleştirilebilir:

- **Faturalama satış vergisi grubu** ve **Fatura kalemi satış vergisi grubu**
- **Mali boyutlar** (**Tutarları dağıt** eylemini kullanarak)

Entegrasyon günlük satırları silinebilir. Ancak deftere nakledilmemiş satırlar, **Hazırlamadan içe aktar** periyodik sürecini yeniden çalıştırdıktan sonra yeniden günlüğe eklenir.

### <a name="post-the-project-operations-integration-journal"></a>Project Operations entegrasyon günlüğünü deftere naklet

Tümleştirme günlüğünü naklederken proje yardımcı defteri ve genel kayıt defteri işlemleri oluşturulur. Bunlar, akış yönündeki müşteri faturalandırması, gelir kabulü ve mali raporlamalar için kullanılır.

Seçilen Project Operations tümleştirme günlüğü, Project Operations tümleştirme günlüğü sayfasındaki **Deftere naklet** kullanılarak deftere nakledilebilir. Tüm Günlükler, **Periyodikler** > **Project Operations tümleştirme** > **Project Operations tümleştirme günlüğünü deftere naklet** üzerinden otomatik olarak deftere nakledilebilir.

Defter nakli, etkileşimli olarak veya bir toplu işte gerçekleştirilebilir. 100 satırdan fazla satırı olan tüm günlüklerin otomatik olarak bir toplu işlem içinde deftere nakledilmesini unutmayın. Bir toplu işte çok sayıda satıra sahip olan günlükler deftere nakledildiğinde, **Özellik yönetimi** çalışma alanındaki **Project Operations tümleştirme günlüğünü toplu görev kullanarak deftere naklet** özelliğini daha iyi performans için kullanın. 

#### <a name="transfer-all-lines-that-have-posting-errors-to-a-new-journal"></a>Deftere nakil hataları olan tüm satırları yeni bir günlüğe aktar

> [!NOTE]
> Bu özelliği kullanmak için, **Özellik yönetimi** çalışma alanındaki **Yeni Project Operations entegrasyon günlüğüne tüm deftere nakil hatalarına sahip satırları naklet** özelliğini etkinleştirin.

Project Operations tümleştirme günlüğüne nakil sırasında sistem günlükteki her satırı doğrular. Sistem hatasız tüm satırları nakleder ve deftere nakil hataları bulunan tüm satırlar için yeni bir günlük oluşturur. Deftere nakil hata satırı olan günlükleri incelemek için **Proje yönetimi ve muhasebe** > **Günlükler** > **Project Operations tümleştirme günlüğü**'ne gidin ve **Orijinal günlük** alanını kullanarak günlükleri filtreleyin.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
