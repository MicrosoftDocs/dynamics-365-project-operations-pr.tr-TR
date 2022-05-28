---
title: İşlem kaynakları - Gerçek değerleri kaynaklarına bağlama
description: Bu konuda, gerçek değerleri zaman girişi, gider girişi veya malzeme kullanımı günlükleri gibi orijinal kaynak kayıtlarına bağlamak için işlem kaynakları kavramının nasıl kullanıldığı açıklanmaktadır.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 908f78f7d58ec4b18f37d03b6fa7c4e2295491fa
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584850"
---
# <a name="transaction-origins---link-actuals-to-their-source"></a>İşlem kaynakları - Gerçek değerleri kaynaklarına bağlama

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Gerçek değerleri, zaman girişleri, gider girişleri, malzeme kullanımı günlükleri ve proje faturaları gibi kaynaklara bağlamak için işlem kaynağı kayıtları oluşturulur.

Aşağıdaki örnekte, bir Project Operations proje yaşam döngüsünde zaman girişlerinin tipik olarak nasıl işlendiği gösterilmektedir.

> ![Project Operations'ta zaman girişlerini işleme.](media/basic-guide-17.png)
 
1. Bir zaman girişinin gönderilmesi iki yevmiye defteri satırı oluşturulmasına neden olur: biri maliyet diğeri de faturalanmamış satış içindir.
2. Bir zaman girişinin nihai onayı iki gerçek değer oluşturulmasına neden olur: biri maliyet diğeri de faturalanmamış satış içindir.
3. Kullanıcı bir proje faturası oluşturduğunda, fatura satırı işlemi faturalanmamış satış fiili değerindeki veriler kullanılarak oluşturulur.
4. Fatura onaylandıktan sonra, iki yeni fiili değer oluşturulur: faturalanmamış bir satış ters işlemi ve faturalanmış satış fiili değeri.

Bu işleme iş akışındaki her etkinlik, zaman girişi, yevmiye defteri satırı, gerçek değer ve fatura satırı ayrıntılarında oluşturulan bu kayıtlar arasındaki ilişkilerin izlenmesine yardımcı olmak için İşlem kaynağı varlığında kayıtların oluşturulmasını tetikler.

Aşağıdaki tabloda, önceki iş akışı için İşlem kaynağı varlığındaki kayıtlar gösterilmektedir.

| Olay                        | Kaynak                   | Kaynak türü                       | İşlem                       | İşlem türü         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| Zaman Girişi Gönderimi        | Zaman girşi Kayıt GUID'i   | Zaman Girişi                        | Yevmiye Defteri Satırı Kayıt GUID'i (maliyet)   | Yevmiye Defteri Satırı             |
| Zaman girşi Kayıt GUID'i       | Zaman Girişi               | Yevmiye Defteri Satırı Kayıt GUID'i (satış)  | Yevmiye Defteri Satırı                      |                          |
| Zaman Onayı                | Yevmiye Defteri Satırı Kayıt GUID'i | Yevmiye Defteri Satırı                      | Faturalanmayan Satış Kaydı GUID'i        | Gerçek                   |
| Zaman girşi Kayıt GUID'i       | Zaman Girişi               | Faturalanmayan Satış Kaydı GUID'i        | Gerçek                            |                          |
| Yevmiye Defteri Satırı Kayıt GUID'i     | Yevmiye Defteri Satırı             | Maliyet Fiili Değeri Kayıt GUID'i           | Gerçek                            |                          |
| Zaman girşi Kayıt GUID'i       | Zaman Girişi               | Maliyet Fiili Değeri Kayıt GUID'i           | Gerçek                            |                          |
| Fatura Oluşturma             | Zaman girşi Kayıt GUID'i   | Zaman Girişi                        | Fatura Satırı İşlem GUID'i     | Fatura Satırı İşlemi |
| Yevmiye Defteri Satırı Kayıt GUID'i     | Yevmiye Defteri Satırı             | Fatura Satırı İşlem GUID'i     | Fatura Satırı İşlemi          |                          |
| Fatura Onayı         | Fatura Satırı GUID'i        | Fatura Satırı                      | Faturalanmış Satış Kaydı GUID'i          | Gerçek                   |
| Fatura GUID'i                 | Fatura                  | Faturalanmış Satış Kaydı GUID'i          | Gerçek                            |                          |
| Fatura Satırı Ayrıntısı GUID'i     | Fatura Satırı Ayrıntısı      | Faturalanmış Satış Kaydı GUID'i          | Gerçek                            |                          |
| Zaman girşi Kayıt GUID'i       | Zaman Girişi               | Faturalanmış Satış Kaydı GUID'i          | Gerçek                            |                          |
| Yevmiye Defteri Satırı Kayıt GUID'i     | Yevmiye Defteri Satırı             | Faturalanmış Satış Kaydı GUID'i          | Gerçek                            |                          |
| Zaman girşi Kayıt GUID'i       | Zaman Girişi               | Faturalanmamış Satış Geri Çevirme GUID'i      | Gerçek                            |                          |
| Yevmiye Defteri Satırı Kayıt GUID'i     | Yevmiye Defteri Satırı             | Faturalanmamış Satış Geri Çevirme GUID'i      | Gerçek                            |                          |
| Taslak Fatura Düzeltmesi     | Eski Fatura Satırı Ayrıntısı GUID'i             | Fatura Satırı İşlemi          | Düzeltme Fatura Satırı Ayrıntısı GUID'i               | Fatura Satırı İşlemi |
| Eski Fatura Satırı GUID'i                  | Fatura Satırı             | Düzeltme Fatura Satırı Ayrıntısı GUID'i               | Fatura Satırı İşlemi          |                          |
| Eski Fatura GUID'i             | Fatura                  | Düzeltme Fatura Satırı Ayrıntısı GUID'i               | Fatura Satırı İşlemi          |                          |
| Zaman girşi Kayıt GUID'i       | Zaman Girişi               | Düzeltme Fatura Satırı Ayrıntısı GUID'i               | Fatura Satırı İşlemi          |                          |
| Yevmiye Defteri Satırı Kayıt GUID'i     | Yevmiye Defteri Satırı             | Düzeltme Fatura Satırı Ayrıntısı GUID'i               | Fatura Satırı İşlemi          |                          |
| Onaylanan fatura düzeltmesi | Eski Fatura Satırı Ayrıntısı GUID'i             | Fatura Satırı İşlemi          | Ters Faturalanan Satış Fiili Değeri GUID'i | Gerçek                   |
| Eski Fatura Satırı GUID'i                  | Fatura Satırı             | Ters Faturalanan Satış Fiili Değeri GUID'i | Gerçek                            |                          |
| Eski Fatura GUID'i             | Fatura                  | Ters Faturalanan Satış Fiili Değeri GUID'i | Gerçek                            |                          |
| Zaman girşi Kayıt GUID'i       | Zaman Girişi               | Ters Faturalanan Satış Fiili Değeri GUID'i | Gerçek                            |                          |
| Yevmiye Defteri Satırı Kayıt GUID'i     | Yevmiye Defteri Satırı             | Ters Faturalanan Satış Fiili Değeri GUID'i | Gerçek                            |                          |
| Eski Fatura Satırı Ayrıntısı GUID'i                 | Fatura Satırı İşlemi | Yeni Faturalanmamış Satış Fiili Değeri GUID'i    | Gerçek                            |                          |
| Eski Fatura Satırı GUID'i                  | Fatura Satırı             | Yeni Faturalanmamış Satış Fiili Değeri GUID'i    | Gerçek                            |                          |
| Eski Fatura GUID'i             | Fatura                  | Yeni Faturalanmamış Satış Fiili Değeri GUID'i    | Gerçek                            |                          |
| Zaman girşi Kayıt GUID'i       | Zaman Girişi               | Yeni Faturalanmamış Satış Fiili Değeri GUID'i    | Gerçek                            |                          |
| Yevmiye Defteri Satırı Kayıt GUID'i     | Yevmiye Defteri Satırı             | Yeni Faturalanmamış Satış Fiili Değeri GUID'i    | Gerçek                            |                          |
| Düzeltme Fatura Satırı Ayrıntısı GUID'i          | Fatura Satırı İşlemi | Yeni Faturalanmamış Satış Fiili Değeri GUID'i    | Gerçek                            |                          |
| Düzeltme Fatura Satırı GUID'i           | Fatura Satırı             | Yeni Faturalanmamış Satış Fiili Değeri GUID'i    | Gerçek                            |                          |
| Düzeltme Faturası GUID'i      | Fatura                  | Yeni Faturalanmamış Satış Fiili Değeri GUID'i    | Gerçek                            |                          |


Aşağıdaki resimde, Project Operations'ta zaman girişleri örneği kullanılarak çeşitli etkinliklerde gerçek değerler ve bunların kaynakları arasında oluşturulan bağlantılar gösterilmektedir.

> ![Project Operations'ta gerçek değerleri kaynak kayıtlarına bağlama.](media/TransactionOrigins.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
