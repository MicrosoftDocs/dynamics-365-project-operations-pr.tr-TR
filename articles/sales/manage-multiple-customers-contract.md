---
title: Sözleşme sözleşmelerindeki birden çok müşteriyi yönetme
description: Bu konu bir proje sözleşmesinde birden çok müşteriyi yönetme hakkında bilgi sağlar.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1adb786c36d43a148e8c5a8b25ded5a997557119f7e6e9e2248935ad4ed211d5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992095"
---
# <a name="manage-multiple-customers-on-project-contracts"></a>Sözleşme sözleşmelerindeki birden çok müşteriyi yönetme

Bu konu bir proje sözleşmesinde birden çok müşteriyi yönetme hakkında bilgi sağlar. Bir anlaşmayı finanse etmek için birden fazla müşteriye yönelik sözleşmeli anlaşma gerektiğinde bir proje sözleşmesi kullanabilirsiniz. **Proje Sözleşmesi** sayfasında **Özet** sekmesi, anlaşma için birincil müşteri hakkında bilgiler içerir. Anlaşmaya katılan diğer müşteriler, **Müşteriler** sekmesine eklenebilir.

Proje sözleşmesinin **Müşteriler** sekmesindeki tüm sözleşme müşterileri varsayılan olarak, proje sözleşmesi için oluşturulan yeni proje tabanlı sözleşme satırlarındaki sözleşme satırı müşterileri olur. Mevcut proje tabanlı sözleşme satırları, daha sonra oluşturulan yeni sözleşme müşterisi kayıtlarını devralmaz.

Sözleşme kazanılmadan önce istediğiniz zaman sözleşme ve sözleşme satırı müşterilerini ekleyebilir, güncelleştirebilir veya silebilirsiniz. Proje sözleşmesinde bir müşteri, **Müşteriler** sayfasında sahibi olan şirket veya tüzel kişilikte müşteri olarak ayarlanmalıdır. Tüzel kişilikler, Dynamics 365 Project Operations'ın **Proje yönetimi ve muhasebe** modülünde ayarlanır ve Project Operations'ın **Proje Satış** ve **Teslimat** modüllerinde şirketler olarak kullanılabilir.

## <a name="primary-customers"></a>Birincil müşteriler

Proje sözleşmesinin **Özet** sekmesindeki potansiyel müşteri, sözleşmenin birincil müşterisidir. Sözleşme müşteri listesindeki birincil müşteriyi güncelleştiremezsiniz. Sözleşmedeki müşteri listesinden birincil müşteriyi silmeye çalışırsanız sözleşmede birincil müşteri kaydının silinemediğini belirten bir hata oluşur. Bunun yerine, proje sözleşmesinin **Özet** sekmesinde **Potansiyel Müşteri** alanındaki müşteriyi değiştirin. Bu alanı güncelleştirdiğinizde yeni seçilen müşteri, **Birincil** bayrağının **Evet** olarak ayarlanmasıyla yeni bir sözleşme müşterisi olarak eklenir. Önceki birincil müşteri hala sözleşmedeki bir müşteridir ancak artık birincil müşteri değildir.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Sözleşme oluşturma, güncelleştirme veya silme müşteri kaydı

**Sözleşme** sayfasının **Sözleşme Müşterileri** sekmesinden bir sözleşme müşterisi oluşturabilir, güncelleştirebilir veya silebilirsiniz. Aşağıdaki alanlar, proje sözleşmesinin sözleşme müşterisi kaydında yer alır.

| **Alan** | **Konum** | **Açıklama** | 
| --- | --- | --- | 
| Hesap | **Sözleşme Müşterileri** sekmesinde düzenlenebilir ızgara ve sözleşme müşterisi için ana sayfa ve hızlı oluşturma sayfası. | Tüm etkin firmaları listeler. Bu alan, kayıt oluşturulduktan sonra kilitlenir. Kaydı güncelleştirmek için silmeniz ve ardından yeniden oluşturmanız gerekir. Herhangi bir fiili değer kaydetmiş durumdaysanız veya sözleşme müşteri kaydı birincil müşteridir, kaydı silemezsiniz. Sözleşme satırı oluşturulduğunda sözleşme müşterileri, sözleşme satırı müşterileri olarak kopyalanır. |
| Fatura Bölme Yüzdesi | **Sözleşme Müşterileri** sekmesinde düzenlenebilir ızgara ve sözleşme müşterisi için ana sayfa ve hızlı oluşturma sayfası. | Sözleşme müşterisiyle ilişkilendirilmiş ve faturalanmamış her satış işleminin yüzdesini temsil eder. Yeni proje sözleşmesi satırları oluşturulduğunda fatura bölme yüzdesi, oluşturulan yeni sözleşme satırlarına ve proje sözleşme satırı müşterilerine kopyalanır. |
| Fatura İlgili Kişi Adı | **Sözleşme Müşterileri** sekmesinde düzenlenebilir ızgara ve sözleşme müşterisi için ana sayfa ve hızlı oluşturma sayfası. | Bu metin alanı, müşteri için fatura ilgili kişisini tanımlamak üzere kullanılmalıdır. Varsayılan değer, ilgili firma kaydından gelir. Sözleşme adı, müşteri için oluşturulan faturada **Fatura Yeri Sözleşme Adı**'na kopyalanır. |
| Fatura Adı | **Sözleşme Müşterileri** sekmesinde düzenlenebilir ızgara ve sözleşme müşterisi için ana sayfa ve hızlı oluşturma sayfası. | Müşteri için fatura ilgili kişisini tanımlamak üzere bu alanı kullanın. Varsayılan değer, ilgili firma kaydından gelir. Ad, müşteri için oluşturulan faturadaki **Fatura Yeri Sözleşme Adı** alanına kopyalanır. |
| Ödeme Koşulları | **Sözleşme Müşterileri** sekmesinde düzenlenebilir ızgara ve sözleşme müşterisi için ana sayfa ve hızlı oluşturma sayfası. | Varsayılan değer, ilgili firma kaydından gelir. Koşullar, müşteri için oluşturulan faturada **Fatura Yeri Sözleşme Adı**'na kopyalanır. |
| Sahibi Olan Şirket | **Proje Sözleşmesi Müşterileri** sekmesinde düzenlenebilir ızgara ve proje sözleşmesi müşterisi için ana sayfa ve hızlı oluşturma sayfası. | Müşterinin **Proje yönetimi ve muhasebe** modülünde ayarlandığı tüzel kişilik. Bu alan salt okunurdur ve proje sözleşmesinin sahibi olan şirkete ayarlanır.</br>**Firma** alanına eklenecek müşteri listesi, Project Operations'ın **Proje yönetimi ve muhasebe** modülündeki sahibi olan şirket alanından listeye zaten filtrelenmiştir. Sahibi olan şirket, Project Operations'ın **Proje yönetimi ve muhasebe** modülündeki tüzel kişiliğe eşittir. Projedeki tüm maliyetler ve gelir tahakkuku, sahibi olan şirketin genel muhasebesinde tutulur. |
| Yuvarlama | **Sözleşme Müşterileri** sekmesinde düzenlenebilir ızgara ve sözleşme müşterisi için ana sayfa ve hızlı oluşturma sayfası. | Müşterinin anlaşma için varsayılan bir yuvarlama müşterisi olup olmadığını gösterir. Proje sözleşmesinde yalnızca tek bir yuvarlama müşterisi olabilir. Maliyet ve faturalanmayan satış miktarı bölünüp yuvarlama farkına neden olduğunda bu fark, müşteriyle eşlenen gerçek tutara uygulanır. |
| Aşılamaz Limit | **Sözleşme Müşterileri** sekmesinde düzenlenebilir ızgara ve sözleşme müşterisi için ana sayfa ve hızlı oluşturma sayfası. | Etkileşim için müşteriye faturalanacak genel tutar için üzerinde anlaşılan bir sınır veya tavan olup olmadığını gösterir. Sözleşme müşterisi düzeyinde ayarlanan aşılamaz sınır, sözleşme müşterisine başvuran faturalanmayan satış gerçek tutarlarına göre hesaplanır. |

## <a name="edit-billing-split-percentages"></a>Fatura bölme yüzdelerini düzenleme

Izgarayı düzenleyerek fatura bölme yüzdelerini düzenleyebilirsiniz. Faturala bölme yüzdeleri toplamı yüzde 100 olmazsa bir hata oluşur. Fatura bölme yüzdesini düzenledikten sonra hatayı kaldırmak için **Proje Sözleşmesi** sayfasını yenileyin.

Ayrıca proje sözleşmesi müşterileri alt ızgarasında **Eşit Dağıt**'ı da seçebilirsiniz. Fatura bölmeleri, proje sözleşmesindeki tüm müşterilere eşit olarak tahsis edilir. Yuvarlama faktörü varsa bu faktör, yuvarlama müşterisine eklenir. Sözleşme müşterilerinden biri için her zaman **Yuvarlama** bayrağı **Evet** olarak ayarlanır. Bu müşteri, yuvarlama müşterisidir. Genel olarak yuvarlama müşterisi ayrıca sözleşmenin birincil müşteridir ancak bu gerekli değildir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]