---
title: Project Operations'da entegrasyon günlüğü
description: Bu konu, Project Operations'ta tümleştirme günlüğüyle çalışma hakkında bilgi sağlar.
author: sigitac
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0021147530d1aa9f82cc54ca8c92b9977c1eea2c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287262"
---
# <a name="integration-journal-in-project-operations"></a>Project Operations'da entegrasyon günlüğü

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Zaman ve gider girişleri bir projeyle ilgili olarak tamamlanan çalışmanın işlemsel görünümünü temsil eden **Fiili** hareketler oluşturur. Dynamics 365 Project Operations bir araçla ilgili olarak hareketleri incelemek ve muhasebe özniteliklerini gerektiği gibi ayarlamak için muhasebeciler sağlar. Gözden geçirme ve ayarlamalar tamamlandıktan sonra, hareketler proje alt muhasebeye ve genel muhasebeye nakledilir. Muhasebeci, **Project Operations tümleştirme** günlüğü (**Dynamics 365 Finance** > **Proje yönetimi ve muhasebe** > **günlükler** > **Project Operations tümleştirme** günlüğü) kullanılarak bu aktiviteleri gerçekleştirebilir.

![Tümleştirme günlüğü akışı](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Project Operations'da entegrasyon günlüğünde kayıt oluşturma

Project Operations Tümleştirme Günlüğündeki kayıtlar dönemsel işlem kullanılarak oluşturulur, **hazırlama tablosundan alınır**. Bu işlemi, **Dynamics 365 Finance** > **Proje yönetimi ve muhasebe** > **Periyodik** > **Project Operations Tümleştirmesi** > **Hazırlama tablosundan alma**'ya giderek çalıştırabilirsiniz. İşlemi etkileşimli olarak çalıştırabilir veya gerektiği gibi arka planda çalışacak şekilde yapılandırabilirsiniz.

Dönemsel işlem çalıştığında, henüz Project Operations tümleştirme günlüğüne eklenmemiş olan gerçek değerler bulunur. Her fiili hareket için bir günlük satırı oluşturulur.
**Project Operations Entegrasyon günlüğündeki periyot ünitesi** alanında (**Finance** > **Proje yönetimi ve muhasebe** > **Kurulum** > **Proje yönetimi ve muhasebe parametreleri**, **Dynamics 365 Customer Engagement** sekmesinde Project Operations) seçilen değere bağlı olarak yevmiye defteri satırlarını ayrı yevmiye defterlerine ayırır. Bu alan için olası değerler şunlardır:

  - **Günler**: Gerçek tutarlar, işlem tarihine göre gruplandırılır. Her gün için ayrı bir günlük oluşturulur.
  - **Aylar**: Gerçek değerler takvim ayına göre gruplandırılır. Her ay için ayrı bir günlük oluşturulur.
  - **Yıllar**: Gerçek değerler takvim yılına göre gruplandırılır. Her yıl için ayrı bir günlük oluşturulur.
  - **Tümü**: tüm fiili hareketler aynı tümleştirme günlüğüne dahil edilir. Periyodik işlem çalışırken günlük kullanılamıyorsa, örneğin günlük hareketleri deftere nakletme sürecinizde ise yeni bir günlük oluşturulur.

Günlük satırları proje fiili değerleri temel alınarak oluşturulur. Aşağıdaki listede, daha fazla sayıda varsayılan ve dönüşüm kuralı yer almaktadır:

  - Her proje fiili hareketinin Project Operations tümleştirme günlüğünde bir satırı vardır. Zaman ve malzeme faturalama türü için maliyet ve faturalanmış olmayan satış hareketleri ayrı satırlarda gösterilir.
  - **Tarih** alanı hareketin tarihini temsil eder. **Muhasebe tarihi** alanı hareketin genel muhasebeye kaydedildiği tarihi temsil eder. Hesap tarihi [kapatılmış bir mali dönemse](https://docs.microsoft.com/dynamics365/finance/general-ledger/close-general-ledger-at-period-end) ve **Hesaplama tarihini açık genel muhasebe dönemi olarak ayarla** parametresi **Proje yönetimi ve hesap oluşturma parametreleri** sayfasının **mali** sekmesinde sistem hareketin hesap tarihini sonraki açık defter periyodunda yer alan ilk tarihe ayarlar.
  - **Fiş** alanı her fiili hareketin fiş numarasını gösterir. Fiş numarası serisi **Proje yönetimi ve hesap oluşturma parametreleri** sayfasında **Numara serileri** sekmesinde tanımlanır. Her satıra yeni bir numara atanır. Fiş deftere nakledildikten sonra, **Fiş hareketi** sayfasında **ilgili fişler** seçilerek maliyet ve faturalanmış olmayan satış hareketinin nasıl ilişkili olduğunu görebilirsiniz .
  - **Kategori** alanı, ilgili proje fiili için işlem kategorisine göre proje hareketini ve Varsayılanlarını temsil eder.
    - **Hareket kategorisi** Proje gerçeğinde ayarlandıysa ve belirli bir tüzel kişilideki ilgili **proje kategorisi** varsa, kategori varsayılan olarak bu proje kategorisini alır.
    - **Hareket kategorisi** Proje gerçeğinde ayarlanmamışsa, sistem **Proje yönetimi ve muhasebe parametreleri** sayfasından **Dynamics 365 Customer Engagement'ta Project Operations** sekmesinde **proje kategori Varsayılanları** alanındaki değeri kullanır.
  - **Kaynak** alanı, bu hareketle ilgili proje kaynağını gösterir. Kaynak, müşterilere yapılan Proje Fatura tekliflerinde başvuru olarak kullanılır.
  - **Döviz Kuru** alanı, Dynamics 365 Finance'te ayarlanan **Döviz Kuru değeri** ayarlanır. Döviz kuru ayarı eksikse, **Hazırlama tablosundan alma** periyodik işlemi alınan alma işlemi kaydı bir günlüğe eklemez ve iş yürütme günlüğüne bir hata iletisi eklenir.
  - **Satır özelliği** alanı, proje gerçek tutarlarındaki faturalama türünü gösterir. Satır özelliği ve faturalama türü eşlemesi, **Proje yönetimi ve muhasebe parametreleri** sayfasında **Dynamics 365 Customer Engagement'ta Project Operations** sekmesinde tanımlanır.

Project Operations tümleştirme günlüğü satırlarında yalnızca aşağıdaki muhasebe öznitelikleri güncelleştirilebilir:

- **Faturalama satış vergisi grubu** ve **Fatura madde satış vergisi grubu**
- **Mali boyutlar** (**Tutarları dağıt** eylemini kullanarak)

Tümleştirme günlüğü satırları silinebilir, ancak deftere nakledilmemiş satırlar, **Hazırlama tablosundan alma** periyodik işleminden yeniden çalıştırdıktan sonra günlükte yeniden eklenir .

Tümleştirme günlüğünü deftere naklederken bir proje alt defteri ve genel muhasebe hareketleri oluşturulur. Bunlar, akış yönündeki müşteri faturalaması, gelir kabulü ve mali raporlamalar için kullanılır.


[!INCLUDE[footer-include](../includes/footer-banner.md)]