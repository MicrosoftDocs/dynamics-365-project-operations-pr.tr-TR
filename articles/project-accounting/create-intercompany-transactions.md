---
title: Şirketler arası işlemler oluşturma
description: Bu konu, şirketler arası işlemlerin nasıl oluşturulacağı hakkında bilgi sağlar.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0a9d34d69ff59f0cb470bb852d8a80ecaedf6544
ms.sourcegitcommit: addbe0647619413e85e7cde80f6a21db95ab623e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595573"
---
# <a name="create-intercompany-transactions"></a>Şirketler arası işlemler oluşturma

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Şirketler arası işlemler, bir şirkete veya kuruluş birimine ait olan proje sözleşmesinde kaynaklar farklı bir şirketin ya da kuruluş biriminin parçasıyken bu sözleşmedeki zaman ve gider işlemleridir.

Şirketler arası bir işlem onaylandığında aşağıdaki fiili işlemler oluşturulur:

| **İşlem türü** | **Uygulanan fiyat listesi** | **İşlem para birimi** |
| --- | --- | --- |
| Maliyet | Sözleşme birimi maliyet fiyat listesi | Fiyat satırındaki para birimi |
| Faturalanmayan satış. Bunlar yalnızca faturalama türü, zaman ve malzemenin olduğu bir sözleşme satırıyla ilişkili gerçek tutarlar için oluşturulur. | Sözleşme projesi satış fiyat listesi | Sözleşme para birimi |
| Kaynak belirleme birimi maliyeti | Kaynak belirleme birimi maliyet fiyat listesi | Fiyat satırındaki para birimi |
| Kuruluşlar arası birim satış | Sözleşme birimi maliyet fiyat listesi | Fiyat satırındaki para birimi |

Maliyet, kaynak belirleme birimi maliyeti ve kuruluşlar arası birim satış işlemi fiyatlandırma ve para birimi, **kuruluş birimi** tarafından yönetilir. Bu, uygulamanızda şirketleri ve kuruluş birimlerini nasıl yapılandıracağınıza karar verirken unutmamanız açısından önemlidir.

Fırsat, teklif, proje sözleşmesi ve proje kayıtları oluşturduğunuzda sistem, sözleşme birimi para biriminin sözleşme şirketi muhasebe para birimiyle aynı olduğunu doğrular. Aynı olmadıklarında bu kayıtlar oluşturulamaz. Kuruluş birimi para birimi, Dynamics 365 Project Operations'ta **Dataverse** > **Ayarlar** > **Kuruluş birimleri**'ne giderek tanımlanır. Şirketin muhasebe para birimi, Dynamics 365 Finance'te **Genel muhasebe** > **Genel muhasebe ayarı** > **Genel muhasebe**'ye giderek tanımlanır. Para birimi, Genel Muhasebe Defterleri Çift Yazma eşlemesini kullanarak Dataverse ortamınızla eşitlenir.

Sistem, aşağıdaki durumlarda kaynak belirleme birimi maliyetini ve kuruluşlar arası birim satış gerçek tutarlarını oluşturur:

  - Kaynak belirleme birimi, sözleşme biriminden farklı olduğunda
  - Kaynak belirleme şirketi, sözleşme şirketinden farklı olduğunda

Ancak yalnızca sözleşme şirketinden farklı bir kaynak belirleme şirketine sahip işlemler, ek muhasebe için Dynamics 365 Finance ortamına aktarılır.

Proje gerçek tutarları için muhasebe, Finance'te Project Operations entegrasyon günlüğünde kaydedilir. Sistem aşağıdaki yevmiye defteri satırlarını oluşturur.

| **İşlem türü** | **Tüzel kişilik** | **Deftere nakilde proje işlemi oluşturur** | **Varsayılan olarak mali boyutlar** | **Varsayılan faturalama satış vergisi grubu ve faturalama öğesi satış vergisi grubu** |
| --- | --- | --- | --- | --- |
| Maliyet | Entegrasyon günlüğüne eklenmez | Yok | Yok | Yok |
| Faturalanmayan satış | Ödünç alan tüzel kişilik entegrasyon günlüğü | Evet | Project | **Faturalama satış vergisi grubu**: **Sözleşme müşterisine** göre <br/> **Faturalama öğesi satış vergisi grubu**: Yevmiye defteri satırındaki geçerli tüzel kişilik proje kategorisinden |
| Kaynak belirleme birimi maliyeti | Ödünç veren tüzel kişilik entegrasyon günlüğü | No | Şirketler arası müşteri | **Faturalama satış vergisi grubu**: **Şirketler arası müşteriye** göre <br/> **Faturalama öğesi satış vergisi grubu**: Yevmiye defteri satırındaki geçerli tüzel kişilik proje kategorisinden |
| Kuruluşlar arası satış | Ödünç veren tüzel kişilik entegrasyon günlüğü | No | Şirketler arası müşteri | **Faturalama satış vergisi grubu**: **Şirketler arası müşteriye** göre <br/> **Faturalama öğesi satış vergisi grubu**: Yevmiye defteri satırındaki geçerli tüzel kişilik proje kategorisinden |

### <a name="example-intercompany-transactions"></a>Örnek: Şirketler arası işlemler

GBPM'de çalışan geliştirici Molly Clark, proje yöneticisi tarafından onaylanan bir USPM Adventure Works projesi için 10 saatlik çalışma kaydeder. GBPM'de geliştirici maliyeti saatlik 88 GBP'dir. GBPM, USPM'ye geliştirici saati başına 120 USD faturalama yapar. USPM, GBPM kaynağı tarafından yapılan iş için müşterisi Adventure Works'e 200 USD faturalama yapar. Daha fazla bilgi için bkz. [Şirketler arası faturalamayı yapılandırma](configure-intercompany-invoicing.md).

1. Project Operations'ta **Kaynaklar**'a gidin ve listeden **Molly Clark**'ı seçin. **Zamanlama** sekmesinde **Şirket** alanında **GBPM**'yi seçin.
2. Adventure Works için yeni müşteri kaydı oluşturmak üzere **Satış** > **Müşteriler**'e gidin ve **Yeni**'yi seçin.
    1. Şirketi **USPM** olarak ayarlayın.
    2. **İlişki türü**'nü **Müşteri** olarak ayarlayın.
    3. **Müşteri grubu 10 – Yerli**'yi seçin.
    4. Para birimini **USD** olarak ayarlayın.
    5. Kaydı kaydedin.
3. **Satış** > **Proje Sözleşmeleri**'ne gidin ve Adventure Works için yeni bir proje sözleşmesi oluşturun.
    1. Sahibi olan şirketi **USPM** olarak ve sözleşme birimini **Contoso Robotics US** olarak ayarlayın.
    2. Müşteri olarak Adventure Works'ü seçin.
    3. Bir ürün fiyat listesi seçin ve kaydı kaydedin.
    4. **Sözleşme Satırları** sekmesinde, yeni bir sözleşme satırı oluşturun. Bir ad ayarlayın ve faturalama yöntemi olarak **Zaman ve Malzemeler**'i seçin.
    5. Yeni bir proje oluşturun ve bu sözleşme satırıyla ilişkilendirin.
4. Kaynak olarak **Molly Clark** ile oturum açın. **Projeler** > **Zaman girişleri**'ne gidin ve Adventure Works projesi için bir zaman girişi oluşturun.
5. Proje yöneticisi olarak oturum açın. **Projeler** > **Onaylar**'a gidin ve Molly Clark tarafından günlüğe kaydedilen zaman girişi işlemini onaylayın.
6. Adventure Works projesine gidin ve **İlgili** > **Gerçek Tutarlar**'ı seçin. Aşağıdaki gerçek tutar işlemleri oluşturulur.

| **İşlem türü** | **Fiyat** | **İşlem para birimi** | **Tutar** |
| --- | --- | --- | --- |
| Maliyet | 120 | USD | 1200 |
| Faturalanmayan satış | 200 | USD | Kategori 2000 |
| Kaynak belirleme birimi maliyeti | Kategori 88 | GBP | 880 |
| Kuruluşlar arası birim satış | 120 | USD | 1200 |

7. USPM muhasebecisi olarak oturum açın. Project Operations'ın Finance kurulumunu açın ve **USPM** şirketini seçin. 
8. **Proje yönetimi ve muhasebe** > **Dönemsel** > **Customer Engagement'ta Project Operations** > **Hazırlamadan içeri aktar**'a gidin ve dönemsel işlemi çalıştırmayı seçin. Bu dönemsel işlem, Project Operations Entegrasyon günlüğünde doldurulur.
9. **Proje yönetimi ve muhasebe** > **Yevmiye Defterleri** > **Project Operations entegrasyon günlüğü**'ne gidin ve yevmiye defteri satırlarını inceleyin. Sistem aşağıdaki satırı oluşturur.

    | **İşlem türü** | **Fiyat** | **İşlem para birimi** | **Tutar** |
    | --- | --- | --- | --- |
    | Faturalanmayan satış | 200 | USD | Kategori 2000 |

    Sistem bu projenin gelir tahakkuku için ayarlanırsa aşağıdakiler deftere nakledilir:

    - Borç: Proje – WIP satış değeri 200 USD
    - Alacak: Proje – Tahakkuk Eden Gelir 200 USD

    Bu faturalanmayan satış artık faturalama için hazırdır. Adventure Works müşterisi için fatura, gerektiğinde mali olarak deftere nakledilebilir.

10. **GBPM** muhasebecisi olarak oturum açın. Project Operations'ın Finance kurulumunu ve **GBPM** şirketini açın. 
11. **Proje yönetimi ve muhasebe** > **Dönemsel** > **Customer Engagement'ta Project Operations** > **Hazırlamadan içeri aktar**'a gidin ve Project Operations Entegrasyon günlüğünde doldurmak için dönemsel işlemi çalıştırın.
12. **Proje yönetimi ve muhasebe** > **Yevmiye Defterleri** > **Project Operations entegrasyon günlüğü**'ne gidin ve satırları inceleyin. Sistem aşağıdaki satırları oluşturur.

    | **İşlem türü** | **Fiyat** | **İşlem para birimi** | **Tutar** |
    | --- | --- | --- | --- |
    | Kaynak belirleme birimi maliyeti | Kategori 88 | GBP | 880 |
    | Kuruluşlar arası birim satış | 120 | USD | 1200 |

    Bu kayıtların deftere nakledilmesi aşağıdaki fiş işlemlerine neden olur:

    - Borç: Proje maliyeti 88 GBP
    - Alacak: Bordro tahsisatı 88 GBP

    Sistem, şirketler arası gelir tahakkuku için ayarlanırsa aşağıdakiler deftere nakledilir:

    - Borç: Proje – WIP satış değeri 120 USD
    - Alacak: Proje – Tahakkuk Eden Gelir 120 USD

    Sistem artık şirketler arası müşteri faturası oluşturmaya hazırdır.
