---
title: İşlem bağlantıları - Farklı işlem türlerinin gerçek değerlerini bağlama
description: Bu konuda, kârlılığı, faturalama biriktirme listesini ve faturalanmış ile faturalanmamış gelir hesaplamalarının karşılaştırılmasını izlemeye yardımcı olmak üzere farklı türlerdeki gerçek değerleri bağlamak için bir işlem bağlantısının nasıl kullanıldığı açıklanmaktadır.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2e8d75a69e27619e6a21f0fe61e2c656e94017b0
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580802"
---
# <a name="transaction-connections---link-actuals-of-different-transaction-types"></a>İşlem bağlantıları - Farklı işlem türlerinin gerçek değerlerini bağlama

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

İşlem bağlantısı kayıtları, teklif veya satış öncesi aşamasından sözleşme aşaması, onaylar ve/veya geri çekmeler, faturalama ve potansiyel olarak alacak veya düzeltici faturalamaya kadar yaşam döngüsünde zaman, gider veya malzeme kullanımı hareketleri gibi farklı türlerdeki gerçek değerleri bağlamak için oluşturulur.

Aşağıdaki örnekte, bir Project Operations proje yaşam döngüsünde zaman girişlerinin tipik olarak nasıl işlendiği gösterilmektedir.

> ![Project Operations'ta zaman girişlerini işleme.](media/basic-guide-17.png)

Project Operations proje yaşam döngüsündeki zaman girişlerinin işlenmesi şu adımlarla gerçekleştirilir: 

1. Bir zaman girişinin gönderilmesi iki yevmiye defteri satırı oluşturulmasına neden olur: biri maliyet diğeri de faturalanmamış satış içindir. 
2. Bir zaman girişinin nihai onayı iki gerçek değer oluşturulmasına neden olur: biri maliyet diğeri de faturalanmamış satış içindir. Bu 2 gerçek değer işlem bağlantıları kullanılarak bağlanır.
3. Kullanıcı bir proje faturası oluşturduğunda, fatura satırı işlemi faturalanmamış satış fiili değerindeki veriler kullanılarak oluşturulur.
4. Fatura onaylandığında iki yeni gerçek değer oluşturulur: faturalanmamış satış ters işlemi ve faturalanmış satış gerçek değeri. Faturalanmamış satış ters işlemi ve orijinal faturalanmamış gerçek değeri, işlem bağlantılarını tersine çevirme kullanılarak bağlanır. Faturalanmış satışlar ve orijinal faturalanmamış satış gerçek değerleri, önceki biriktirme listesi veya devam eden iş (WIP) geliri ile şu anda faturalanmış gelir arasındaki bağlantıları göstermek için de bağlanır.   

İşleme iş akışındaki her etkinlik, **İşlem bağlantısı** tablosunda kayıt oluşturmayı tetikler. Bu, zaman girişi, yevmiye defteri satırı, gerçek değer ve fatura satırı ayrıntılarında oluşturulan kayıtlar arasındaki ilişkilerin izlenebilmesine yardımcı olur.

Aşağıdaki tabloda, önceki iş akışı için **İşlem bağlantısı** varlığındaki kayıtlar gösterilmektedir.

|Olay                   |İşlem 1                 |İşlem 1 rolü |İşlem 1 türü       |İşlem 2          |İşlem 2 rolü |İşlem 2 türü |
|------------------------|------------------------------|---------------|-----------------------------|-----------------------------|-------------------|-------------------|
|Zaman Girişi Gönderimi   |Yevmiye Defteri Satırı (Satış) GUID'i     |Faturalanmayan Satış |msdyn_journalline            |Yevmiye Defteri Satırı (maliyet) GUID'i     |Maliyet            |msdyn_journalline  |
|Zaman Onayı           |Faturalanmamış Fiili Değer (Satış) GUID'i  |Faturalanmayan Satış |msdyn_actual                 |Fiili Değer (maliyet) GUID'i       |Maliyet            |msdyn_actual       |
|Fatura Oluşturma        |Fatura Satırı Ayrıntısı GUID'i      |Faturalanan Satış   |msdyn_invoicelinetransaction |Faturalanmamış Satış Fiili Değeri GUID'i   |Faturalanmamış Satış  |msdyn_actual       |
|Fatura Onayı    |Tersine Çevirme Fiili Değeri GUID'i         |Tersine çevirme      |msdyn_actual                 |Orijinal faturalanmamış satış GUID'i |Orijinal        |msdyn_actual       |
|                        |Faturalanan Satış GUID'i             |Faturalanan Satış   |msdyn_actual                 |Faturalanmamış Satış Fiili Değeri GUID'i   |Faturalanmayan Satış  |msdyn_actual       |
|Taslak Fatura Düzeltmesi |Fatura Satırı İşlem GUID'i|Değiştirme      |msdyn_invoicelinetransaction |Faturalanan Satış GUID'i            |Orijinal        |msdyn_actual       |
|Fatura Düzeltmesini Onayla|Faturalanan Satış Tersine Çevirme GUID'i  |Tersine çevirme      |msdyn_actual                 |Faturalanan Satış GUID'i            |Orijinal        |msdyn_actual       |
|                        |Yeni Faturalanmamış Satış GUID'i |Değiştirme            |msdyn_actual                 |Faturalanan Satış GUID'i            |Orijinal        |msdyn_actual       |


Aşağıdaki resimde, Project Operations'ta zaman girişleri örneği kullanılarak çeşitli etkinliklerde farklı gerçek değerler arasında oluşturulan bağlantılar gösterilmektedir.

> ![Project Operations'ta farklı türdeki gerçek değerleri birbirine bağlama.](media/TransactionConnections.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
