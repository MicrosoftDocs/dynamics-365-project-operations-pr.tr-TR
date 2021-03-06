---
title: Müşteri adaylarını (Pro) yönetme
description: Bu konuda, proje tabanlı müşteri adaylarını (pro) yönetme hakkında bilgiler sağlanmaktadır.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 005e36811643b0b1e98a686792cf39125ae97949
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896350"
---
# <a name="manage-leads-pro"></a>Müşteri adaylarını (Pro) yönetme

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Proje tabanlı müşteri adayları, Project Operations'ta yönetilebilir ve uygun bulunabilir. Müşteri adayı yönetimi süreci, iş tabanlı müşteri adayları oluşturmayı ve bu müşteri adaylarını uygun bulmayı içerir. 

## <a name="list-of-project-sales-leads"></a>Proje satış müşteri adayları listesi

**Satış** bölümündeki sol gezinti bölmesinde, sistemdeki tüm müşteri adayı kayıtlarının listesini görüntülemek için **Müşteri Adayları** listesi sayfasını açın. Gösterilen müşteri adayı listesi, iş tabanlı müşteri adayları ile Dynamics 365 Sales veya Dynamics 365 Field Service uygulamasına da sahipseniz oluşturulabilecek diğer müşteri adayı türlerinden oluşur.

Yalnızca proje tabanlı müşteri adaylarını görmek için **Tür** değerinde bir filtre oluşturarak filtrelenmiş görünüm elde edebilirsiniz. Örneğin, yalnızca iş tabanlı müşteri adaylarını göstermeyi seçebilirsiniz.

## <a name="creating-a-new-lead-for-a-project-based-deal"></a>Proje tabanlı anlaşma için yeni bir müşteri adayı oluşturma

Proje tabanlı müşteri adayı uygun bulunduğunda bir fırsat ve bir firma oluşturulur. Proje tabanlı fırsat, Fırsat aşamasında satış takibi etkinliklerinin başlangıç noktasıdır. Proje tabanlı fırsatlar, proje çalışmasının satışı için gerekli olan benzersiz özelliklere sahiptir. Bu özellikler şunlardır:

- Zaman ve malzeme ve Sabit Fiyatlı faturalama yöntemleri
- İnsan kaynakları, giderler ve projelerde ortaya çıkan malzeme için birden çok tarihte etkin fiyat listeleri.

Otomatik olarak bir fırsat oluşturmak üzere uygun bulunan müşteri adayı için **Tür** özniteliğini **İş tabanlı** olarak ayarlayın. Farklı bir tür seçerseniz müşteri adayı, uygun bulunduğunda proje tabanlı bir fırsat oluşturmaz. Proje tabanlı fırsat oluşturulmazsa projeye özgü özellikler, aşağı yönlü satış süreçlerinde kullanılamaz.

Aşağıdaki tabloda, bir müşteri adayının önemli alan bilgileri ve bu alanların aşağı yönlü etkileri bulunmaktadır.

| **Alan** | **Konum** | **İlgi, amaç ve kılavuz** | **Aşağı yönlü etki** |
| --- | --- | --- | --- |
| Başlık | Genel sekmesi | Bu metin alanı, anlaşma için kısa bir açıklama içermelidir. | Müşteri adayının konusu varsayılan olarak Fırsatın konusu ve Teklif ve Proje sözleşmesinin adıdır. |
| Tür | Genel sekmesi | Bu seçenek kümesi alanında aşağıdaki seçenekler bulunur:</br>- İş tabanlı (yalnızca Project Operations yüklendiğinde kullanılabilir)</br>- Öğe tabanlı (yalnızca Project Operations ve Sales yüklendiğinde kullanılabilir)</br>- Servis bakımı tabanlı (Field Service yüklendiğinde kullanılabilir) | Bu alanın değeri müşteri adayında **İş tabanlı** olarak ayarlandığında müşteri adayı, Proje Tabanlı Fırsat oluşturmak için uygun bulunur. Bu anlaşma için aşağı yönlü satış sürecinde projeye özgü tüm uzantıları ve işlevleri etkinleştirmek için proje tabanlı bir fırsat gerekir. |
| Ad | Genel sekmesi | Destekçi adayının ilgili kişisinin adı | Müşteri adayı uygun bulunduğunda bir firma, ilgili kişi ve fırsat oluşturulur. İlgili kişinin adı, buradaki değer kümesidir. |
| Soyadı | Genel sekmesi | Destekçi adayın ilgili kişisinin soyadı | Müşteri adayı uygun bulunduğunda bir firma, ilgili kişi ve fırsat oluşturulur. İlgili kişinin soyadı, buradaki değer kümesidir. |
| Şirket | Genel sekmesi | Destekçi aday müşterinin şirketinin adı | Müşteri adayı uygun bulunduğunda bir firma, ilgili kişi ve fırsat oluşturulur. Oluşturulan firmanın adı, buradaki değer kümesidir. |
| Para birimi | Ayrıntılar sekmesi | Destekçi aday müşterinin para birimi | Müşteri adayı uygun bulunduğunda bir firma, ilgili kişi ve fırsat oluşturulur. Oluşturulan firmanın para birimi, buradaki değer kümesidir. |

## <a name="qualify-a-new-project-based-lead"></a>Yeni proje tabanlı müşteri adayını uygun bulma

**Tür** değeri **İş tabanlı** olarak ayarlanan müşteri adaylarına proje tabanlı müşteri adayı adı verilir. Proje tabanlı müşteri adayı uygun bulunduğunda aşağıdakiler oluşturulur:

- Müşteri adayındaki **Şirket** alanını kullanan bir firma.
- Müşteri adayının **Ad** ve **Soyadı** alanlarındaki değerlere bağlı olarak firma ile ilişkilendirilen bir ilgili kişi kaydı.
- **Tür** alanı &quot;**İş tabanlı** olarak ayarlanmış proje tabanlı bir fırsat.

Müşteri adaylarını uygun bulma hakkında daha ayrıntılı bilgi için bkz. [Müşteri adaylarını uygun bulma veya dönüştürme](https://docs.microsoft.com/dynamics365/sales-enterprise/qualify-lead-convert-opportunity-sales).

## <a name="business-process-flow-for-project-based-deals"></a>Proje tabanlı anlaşmalar için iş süreci akışı

Project Operations'ta proje tabanlı anlaşmalar için aşağıdaki iş süreci akışları desteklenir:

- Müşteri Adayından Fırsata iş süreci
- Fırsat satış süreci

Müşteri Adayından Fırsata iş süreci aşağıdaki aşamaları destekler:

| Aşama adı | Eşlenen varlık | İşlev |
| --- | --- | --- |
| Nitelikli Hale Getir | Müşteri adayı | Firma, ilgili kişi ve fırsat oluşturmak için müşteri adayını uygun bulun. |
| Geliştir | Fırsat | Mevcut çalışmalar, önemli paydaşlar ve rekabet hakkında daha fazla bilgi eklemek için fırsatı geliştirin. |
| Teklif Et | Fırsat | Teklifi geliştirin ve dahili inceleme takımından onay alın. |
| Kapat | Fırsat | Anlaşmaya varmak için fırsatı kazanın. |
