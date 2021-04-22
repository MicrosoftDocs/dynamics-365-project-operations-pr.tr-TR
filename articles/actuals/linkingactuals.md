---
title: Gerçek değerleri özgün kayıtlara bağlama
description: Bu konu, gerçek değerlerin zaman girişi, gider girişi veya malzeme kullanım günlükleri gibi orijinal kayıtlara nasıl bağlanabileceğini açıklar.
author: rumant
manager: tfehr
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 545775c4eae6c3dc689f264e7f662471c17b2340
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852613"
---
# <a name="link-actuals-to-original-records"></a>Gerçek değerleri özgün kayıtlara bağlama

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_


Dynamics 365 Project Operations'ta, *iş işlemi* herhangi bir varlıkla temsil edilmeyen soyut bir kavramdır. Ancak, varlıklardaki bazı ortak alanlar ve işlemler, iş işlemleri kavramını kullanacak şekilde tasarlanmıştır. Aşağıdaki varlıklar bu kavramı kullanır:

- Teklif satırı ayrıntıları
- Sözleşme satırı ayrıntıları
- Tahmin satırları
- Yevmiye defteri satırları
- Gerçekler

Bu varlıkların **Teklif satırı ayrıntıları**, **Sözleşme satırı ayrıntıları** ve **Tahmin satırları** proje yaşam döngüsünün tahmini aşamalarıyla eşleştirilir. **Yevmiye defteri satırları** ve **Gerçek değerler varlıkları** proje yaşam döngüsünde yürütme aşamasına eşlenir.

Project Operations, bu beş varlığın kayıtlarını iş hareketleri olarak ele alır. Tek fark, tahmin aşamalarıyla eşlenen varlıklardaki kayıtların mali tahminler olarak değerlendirilmesine karşın, yürütme aşamasına eşlenen varlıklardaki kayıtlar önceden gerçekleşmiş olan mali olgular olarak değerlendirilmesidir.

## <a name="concepts-that-are-unique-to-business-transactions"></a>İş işlemlerine özgü kavramlar.
Aşağıdaki kavramlar, iş işlemleri kavramına özeldir:

- İşlem türü
- İşlem sınıfı
- İşlem kaynağı
- İşlem bağlantısı

### <a name="transaction-type"></a>İşlem türü

İşlem türü bir projedeki mali etkinin zamanlamasını ve bağlamını gösterir. Bu, Project Operations'ta aşağıdaki desteklenen değerlere sahip olan bir seçenek kümesi tarafından temsil edilir:

  - Maliyet
  - Proje sözleşmesi
  - Faturalanmayan satış
  - Faturalanan satış
  - Kuruluşlar arası satış
  - Kaynak belirleme birimi maliyeti

### <a name="transaction-class"></a>İşlem sınıfı

İşlem sınıfı, projelerde oluşan farklı maliyet türlerini gösterir. Bu, Project Operations'ta aşağıdaki desteklenen değerlere sahip olan bir seçenek kümesi tarafından temsil edilir:

  - Zaman
  - Gider
  - Malzeme
  - Ücret
  - Kilometre taşı
  - Vergi

**Kilometre taşı** genellikle iş mantığı tarafından Project Operations içindeki sabit fiyatlı faturalama için kullanılır.

### <a name="transaction-origin"></a>İşlem kaynağı

**Hareket kaynağı**, her iş işleminin kaynağını depolayan bir varlıktır. Bir proje devam ederken, her iş hareketi başka bir iş hareketinin başlamasına neden olur ve bu zincir böyle devam eder. Hareket kaynağı varlığı, raporlama ve izleme özelliklerine yardımcı olmak için her hareketin kaynağıyla ilgili verileri depolamak üzere tasarlanmıştır. 

### <a name="transaction-connection"></a>İşlem bağlantısı

**Hareket bağlantısı** maliyet ve ilgili satış gerçek değerleri gibi iki benzer iş hareketi arasındaki ilişkiyi veya fatura onayı veya fatura düzeltmeleri gibi faturalama etkinlikleriyle tetiklenen tersine işlemleri depolayan bir varlıktır.

**Hareket kaynağı** ve **Hareket bağlantısı**, iş işlemleri ve belirli bir iş işleme neden olan eylemler arasındaki ilişkileri izlemenize yardımcı olur.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Örnek: İşlem kaynağı İşlem bağlantısıyla birlikte nasıl çalışır?

Aşağıdaki örnekte, bir Project Operations proje yaşam döngüsünde zaman girişlerinin tipik olarak nasıl işlendiği gösterilmektedir.

> ![Project Service yaşam döngüsünde zaman girişlerini işleme](media/basic-guide-17.png)
 
1. Bir zaman girişinin gönderilmesi, iki yevmiye defteri satırı oluşturulmasına neden olur: maliyet için bir satır ve faturalanmamış satışlar için bir satır.
2. Bir zaman girişinin nihai onayı iki gerçek değer oluşturulmasına neden olur: maliyet için bir gerçek değer ve de faturalanmamış satışlar için bir gerçek değer.
3. Yeni bir proje faturası oluşturulduğunda, fatura satırı işlemi faturalanmamış satış fiili değerindeki veriler kullanılarak oluşturulur. 
4. Fatura onaylandıktan sonra, iki yeni gerçek değer oluşturulur: faturalanmamış bir satış ters işlemi gerçek değeri ve faturalanmış satışlar gerçek değeri.

Bu olayların her biri, **Hareket kaynağı** ve **Hareket bağlantısı** varlıklarında bir kayıt oluşturur. Bu yeni kayıtlar; zaman girişi, yevmiye defteri satırı, gerçek değerler ve fatura satırı ayrıntıları genelinde oluşturulan kayıtlar arasında bir ilişki geçmişi oluşturmanıza yardımcı olur.

Aşağıdaki tabloda, iş akışı için **Hareket kaynağı** varlığındaki kayıtlar gösterilmektedir.

| Olay                        | Kaynak                   | Kaynak türü                       | İşlem                       | İşlem türü         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| Zaman Girişi Gönderimi        | Zaman Girişi Kayıt GUID'i   | Zaman Girişi                        | Yevmiye Defteri Satırı Kayıt GUID'i (maliyet)   | Yevmiye Defteri Satırı             |
| Zaman girşi Kayıt GUID'i       | Zaman Girişi               | Yevmiye Defteri Satırı Kayıt GUID'i (satış)  | Yevmiye Defteri Satırı                      |                          |
| Zaman Onayı                | Yevmiye Defteri Satırı Kayıt GUID'i | Yevmiye Defteri Satırı                      | Faturalanmayan Satış Kaydı GUID'i        | Gerçek                   |
| Zaman girşi Kayıt GUID'i       | Zaman Girişi               | Faturalanmayan Satış Kaydı GUID'i        | Gerçek                            |                          |
| Yevmiye Defteri Satırı Kayıt GUID'i     | Yevmiye Defteri Satırı             | Maliyet Fiili Değeri Kayıt GUID'i           | Gerçek                            |                          |
| Zaman girşi Kayıt GUID'i       | Zaman Girişi               | Maliyet Fiili Değeri Kayıt GUID'i           | Gerçek                            |                          |
| Fatura Oluşturma             | Zaman Girişi Kayıt GUID'i   | Zaman Girişi                        | Fatura Satırı İşlem GUID'i     | Fatura Satırı İşlemi |
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

Aşağıdaki tabloda, iş akışı için **Hareket bağlantısı** varlığındaki kayıtlar gösterilmektedir.

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
