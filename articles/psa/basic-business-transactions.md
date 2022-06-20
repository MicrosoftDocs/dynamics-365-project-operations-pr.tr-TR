---
title: İş işlemleri
description: Bu makale, iş işlemleri hakkında bilgi sağlar.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: rumant
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
ms.openlocfilehash: 07002890e0474dbdaf979d9dcdf064e9c382a0f9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927030"
---
# <a name="business-transactions"></a>İş işlemleri

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation'da, *iş işlemi* herhangi bir varlıkla temsil edilmeyen bir soyut kavramdır. Ancak, varlıklardaki bazı ortak alanlar ve işlemler, iş işlemleri kavramını kullanacak şekilde tasarlanmıştır. Aşağıdaki varlıklar bu soyutlamayı kullanır:

- Teklif satırı ayrıntıları
- Sözleşme satırı ayrıntıları
- Tahmin satırları
- Yevmiye defteri satırları
- Gerçek değerler

Bu varlıkların Teklif satırı ayrıntıları, Sözleşme satırı ayrıntıları ve Tahmin satırları proje yaşam döngüsünün tahmini aşamalarıyla eşleştirilir. Yevmiye defteri satırları ve Fiili değerler varlıkları proje yaşam döngüsünde yürütme aşamasına eşlenir.

PSA, bu beş varlığın kayıtlarını iş işlemleri olarak ele alır. Tek fark, tahmin aşamalarıyla eşlenen varlıklardaki kayıtların mali tahminler olarak değerlendirilmesine karşın, yürütme aşamasına eşlenen varlıklardaki kayıtlar önceden gerçekleşmiş olan mali olgular olarak değerlendirilmesidir.

Daha fazla bilgi için bkz. [Tahminler](estimates.md) ve [Fiili değerler](actuals.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>İş işlemlerine özgü kavramlar.
Aşağıdaki kavramlar, iş işlemleri kavramına özeldir:

- İşlem türü
- İşlem sınıfı
- İşlem kaynağı
- İşlem bağlantısı

### <a name="transaction-type"></a>İşlem türü

İşlem türü bir projedeki mali etkinin zamanlamasını ve bağlamını gösterir. Bu, PSA'da aşağıdaki desteklenen değerlere sahip olan bir seçenek kümesi tarafından temsil edilir:
- Maliyet
- Proje sözleşmesi
- Faturalanmayan satış
- Faturalanan satış
- Kuruluşlar arası satış
- Kaynak belirleme birimi maliyeti

### <a name="transaction-class"></a>İşlem sınıfı

İşlem sınıfı, projelerde oluşan farklı maliyet türlerini gösterir. Bu, PSA'da aşağıdaki desteklenen değerlere sahip olan bir seçenek kümesi tarafından temsil edilir:

- Time
- Gider
- Malzeme
- Ücret
- Kilometre taşı
- Vergi

**Kilometre taşı** değeri genellikle iş mantığı tarafından PSA içindeki sabit fiyatlı faturalama için kullanılır.

### <a name="transaction-origin"></a>İşlem kaynağı

İşlem kaynağı, her iş işleminin kaynağını depolayan bir varlıktır. Proje yürütmesi ilerledikçe, her iş işlemi bir başka iş işlemi oluşturacak olan bir başka bir iş işlemine yol açar ve bu şekilde devam eder. İşlem kaynağı varlığı, raporlamaya ve izlemeye yardımcı olmak amacıyla her işlemin kaynağıyla ilgili verileri depolamak için tasarlanmıştır. 

### <a name="transaction-connection"></a>İşlem bağlantısı

İşlem bağlantısı maliyet ve ilgili gerçek değerleri gibi iki benzer iş hareketi arasındaki ilişkiyi veya fatura onayı veya fatura düzeltmeleri gibi faturalama etkinlikleriyle tetiklenen tersine işlemleri depolayan bir varlıktır.

İşlem kaynağı ve işlem bağlantısı, iş işlemleri ve belirli bir iş işleminin oluşturulmasına neden olan eylemler arasındaki ilişkileri izlemenize yardımcı olur.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Örnek: İşlem kaynağı İşlem bağlantısıyla birlikte nasıl çalışır?

Aşağıdaki örnekte, bir PSA proje yaşam döngüsünde zaman girişlerinin tipik olarak nasıl işlendiği gösterilmektedir.

> ![Project Service yaşam döngüsünde zaman girişlerini işleme.](media/basic-guide-17.png)
 
1. Bir zaman girişinin gönderilmesi iki günlük satırı oluşturulmasına neden olur: biri maliyet diğeri de faturalandırmamış satış içindir.
2. Bir zaman girişinin nihai onayı iki fiili değer oluşturulmasına neden olur: biri maliyet diğeri de faturalandırmamış satış içindir.
3. Kullanıcı bir proje faturası oluşturduğunda, fatura satırı işlemi faturalanmamış satış fiili değerindeki veriler kullanılarak oluşturulur. 
4. Fatura onaylandıktan sonra, iki yeni fiili değer oluşturulur: faturalanmamış bir satış ters işlemi ve faturalanmış satış fiili değeri.

Bu olayların her biri zaman girişi, yevmiye günlüğ satırı, fiili değerler ve fatura satırı ayrıntılarında oluşturulan bu kayıtlar arasındaki ilişkilerin izlenebilmesine yardımcı olmak için İşlem kaynağı ve İşlem bağlantısı varlıklarında kayıtlar oluşturulmasını tetikler.

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

Aşağıdaki tabloda, önceki iş akışı için İşlem bağlantısı varlığındaki kayıtlar gösterilmektedir.

| Olay                          | İşlem 1                 | İşlem 1 rolü | İşlem 1 türü           | İşlem 2                | İşlem 2 rolü | İşlem 2 türü |
|--------------------------------|-------------------------------|--------------------|------------------------------|------------------------------|--------------------|--------------------|
| Zaman Girişi Gönderimi          | Yevmiye Defteri Satırı (Satış) GUID'i     | Faturalanmayan Satış     | msdyn_journalline            | Yevmiye Defteri Satırı (maliyet) GUID'i     | Maliyet               | msdyn_journalline  |
| Zaman Onayı                  | Faturalanmamış Fiili Değer (Satış) GUID'i  | Faturalanmayan Satış     | msdyn_actual                 | Fiili Değer (maliyet) GUID'i       | Maliyet               | msdyn_actual       |
| Fatura Oluşturma               | Fatura Satırı Ayrıntısı GUID'i      | Faturalanan Satış       | msdyn_invoicelinetransaction | Faturalanmamış Satış Fiili Değeri GUID'i   | Faturalanmamış Satış     | msdyn_actual       |
| Fatura Onayı           | Tersine Çevirme Fiili Değeri GUID'i         | Tersine çevirme          | msdyn_actual                 | Orijinal faturalanmamış satış GUID'i | Orijinal           | msdyn_actual       |
| Faturalanan Satış GUID'i              | Faturalanan Satış                  | msdyn_actual       | Faturalanmamış Satış Fiili Değeri GUID'i   | Faturalanmayan Satış               | msdyn_actual       |                    |
| Taslak Fatura Düzeltmesi       | Fatura Satırı İşlem GUID'i | Değiştirme          | msdyn_invoicelinetransaction | Faturalanan Satış GUID'i            | Orijinal           | msdyn_actual       |
| Fatura Düzeltmesini Onayla     | Faturalanan Satış Tersine Çevirme GUID'i    | Tersine çevirme          | msdyn_actual                 | Faturalanan Satış GUID'i            | Orijinal           | msdyn_actual       |
| Yeni Faturalanmamış Satış Fiili Değeri GUID'i | Değiştirme                     | msdyn_actual       | Faturalanan Satış GUID'i            | Orijinal                     | msdyn_actual       |                    |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
