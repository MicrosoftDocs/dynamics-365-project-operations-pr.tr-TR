---
title: Satıcı faturası tümleştirmesi
description: Bu konu, Project Operations'ta satıcı faturası tümleştirmesi hakkında bilgi sağlar.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 538a2694591f1d0d368ee0ffeed9bdf12cb47420c3d0571f75185fe433f23436
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986515"
---
# <a name="vendor-invoice-integration"></a>Satıcı faturası tümleştirmesi

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Dynamics 365 Project Operations'da projeyle ilgili satın alma, **Borç hesapları** > **faturalar** > **Bekleyen satıcı faturaları**'na giderek ve bekleyen bir satıcı fatura belgesi kullanılarak kaydedilebilir. Daha fazla bilgi için bkz. [Bekleyen satıcı faturası kullanarak stoğu tutulmayan malzemeleri satın alma](../procurement/pending-vendor-invoices.md).

> [!IMPORTANT]
> Bu konu açıklanan işlevleri kullanmadan önce gerekli yapılandırmaları gözden geçirin ve uygulayın. Daha fazla bilgi için bkz. [Stoklanmayan malzemeleri ve bekleyen satıcı faturalarını etkinleştirme](../procurement/configure-materials-nonstocked.md).

Project Operations'da projeyle ilgili satıcı faturaları, özel deftere nakil kuralları kullanılarak deftere nakledilir:

- Projeyle ilgili maliyet (kurtarılamayan KDV dahil), doğrudan genel muhasebedeki proje maliyet hesabına nakledilmemiştir. Bunun yerine, maliyet **satın alma entegrasyonu hesabına** nakledilir. Bu hesap, **Dynamics 365 Customer Engagement'ta Project Operations** sekmesindeki **Proje yönetimi ve hesap** > **kurulum** > **Proje yönetimi ve muhasebe parametreleri**'nde yapılandırılır.
- Çift yazma, satıcı fatura ayrıntılarını Microsoft Dataverse'e aşağıdaki tablo haritalarını kullanarak eşitler:

     - **Project Operations tümleştirme projesi satıcı fatura verme varlığı (msdyn_projectvendorinvoices)**: Bu tablo Haritası satıcı fatura başlığı bilgilerini eşitler. Yalnızca proje kimliği içeren en az bir satırlı satıcı faturaları Dataverse ile eşitlenir.
     - **Project Operations tümleştirme projesi satıcı fatura satır verme varlığı (msdyn_projectvendorinvoicelines)**: Bu tablo Haritası satıcı fatura başlığı satır bilgilerini eşitler. Yalnızca proje kimliği içeren satırlar Dataverse ile eşitlenir .

     > [!NOTE]
     > Dataverse Uygulamasındaki satıcı fatura ayrıntıları düzenlenemez.

Vergi alt raporu, satıcı alt muhasebe ve diğer mali defter nakilleri, satıcı faturasının deftere nakledildiği sırada Dynamics 365 Finance'e uygun olarak kaydedilir.

![Satıcı faturası tümleştirmesi.](media/DW7VendorInvoice.png)

Dataverse'de bir **satıcı fatura** varlığına kayıtlar yazıldığında, kayıtların otomatikleştirilmiş onay işlemi başlar. Gerekirse, otomatik onay işlemi durumu **Gelişmiş ayarlar** > **sistem** > **sistemi işlerine** giderek Dataverse'te gözden geçirilebilir. Onay tamamlandıktan sonra, sistem **Gerçek değerler** varlığında malzeme hareketi sınıf kayıtları oluşturur.

Malzemeyle ilgili fiili değerler daha sonra çift yazma tablo eşlemesi, **Project Operations gerçek değerlerle tümleştirilmesine (msdyn_actuals)** işlenir . Daha fazla bilgi için bkz. [Proje tahminleri ve gerçek değerler](resource-dual-write-estimates-actuals.md).

Periyodik işlem, **Hazırlamadan içe aktar**, satıcı faturasıyla ilgili Project Operations tümleştirme günlüğü satırları oluşturur. Mahsup hesabı varsayılan olarak satın alma entegrasyonu hesabıdır. Tümleştirme günlüğü nakledildiğinde, satıcı fatura hareketi için hesap bakiyesi temizlenir ve satır tutarı proje maliyeti hesabına taşınır. Ayrıca, aşağı akış ve gelir kabulü amaçları için proje alt muhasebe hareketleri de oluşturulur.