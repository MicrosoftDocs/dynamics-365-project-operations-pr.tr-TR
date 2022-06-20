---
title: Project Operations'da tümleştirme günlüğü
description: Bu makale, Project Operations'ta Entegrasyon günlüğü ile çalışma hakkında bilgi sağlar.
author: sigitac
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: befb1756ad77708805f3cbb06168b93e44296df0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923902"
---
# <a name="integration-journal-in-project-operations"></a>Project Operations'da tümleştirme günlüğü

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Zaman ve gider girişleri, bir projeyle ilgili tamamlanan çalışmanın operasyonel görünümünü temsil eden **Gerçek** işlemler oluşturur. Dynamics 365 Project Operations, işlemleri incelemek ve muhasebe özniteliklerini ihtiyaç duyulduğu şekilde ayarlamak için bir araç ile birlikte muhasebeciler sağlar. İnceleme ve ayarlamalar tamamlandıktan sonra işlemler, Proje yardımcı defterine ve Genel deftere nakledilir. Muhasebeciler, **Project Operations Tümleştirme** günlüğü (**Dynamics 365 Finance** > **Proje yönetimi ve muhasebe** > **Günlükler** > **Project Operations Tümleştirme** günlüğünü kullanarak bu etkinlikleri gerçekleştirebilir.

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

Tümleştirme günlüğü satırları silinebilir, ancak deftere nakledilmemiş satırlar, **Hazırlamadan içe aktar** periyodik sürecini yeniden çalıştırdıktan sonra yeniden günlüğe eklenir.

Tümleştirme günlüğünü naklederken proje yardımcı defteri ve genel kayıt defteri işlemleri oluşturulur. Bunlar, akış yönündeki müşteri faturalandırması, gelir kabulü ve mali raporlamalar için kullanılır.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
