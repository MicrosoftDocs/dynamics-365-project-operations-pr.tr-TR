---
title: Proje tabanlı sözleşme satırında fatura zamanlaması oluşturma
description: Bu konuda, sözleşme satırları için fatura zamanlamaları ve kilometre taşları oluşturma hakkında bilgiler sağlanmaktadır.
author: rumant
manager: Annbe
ms.date: 10/17/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 674f4ccced3d0e3178799f60d9f95a2ec27cd153
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180801"
---
# <a name="create-an-invoice-schedule-on-a-project-based-contract-line"></a>Proje tabanlı sözleşme satırında fatura zamanlaması oluşturma 

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Proje tabanlı sözleşme satırında fatura zamanlaması oluşturabilirsiniz. Yalnızca, sözleşmenin kazanılan ve siz bir proje sözleşmesi oluştururken faturalamaya izin verilir. Fatura çizelgesi, proje tabanlı bir sözleşme satırının otomatik olarak oluşturulmasını sağlayan taslak faturalarına izin verir. Ancak faturaları yalnızca el ile oluşturursanız, sözleşme satırlarında fatura zamanlamaları oluşturmayı atlayabilirsiniz.

## <a name="create-a-time-and-material-invoice-schedule-for-a-contract-line"></a>Sözleşme satırı için Zaman ve malzeme fatura zamanlaması oluşturma

Proje tabanlı sözleşme satırının saati ve malzeme faturalama yöntemi oldğuunda, tarih tabanlı fatura zamanlaması oluşturur. Otomatik olarak tarih tabanlı fatura zamanlaması oluşturmak için aşağıdaki adımları tamamlayın.

1. **Ayarlar** > **fatura sıklıkları**'na gidin ve bir fatura sıklığı ayarlayın.
2. Proje sözleşmesi kaydına gidin ve **Özet** sekmesinde, **istenen teslim tarihi** alanında bir tarih seçin.
3. Tarih tabanlı fatura zamanlaması oluşturmanız için gereken **zaman ve malzeme** teklif satırını açın. 
4. **Fatura Zamanlaması** sekmesinde, Faturalama başlangıcı ve Fatura Sıklığı alanlarında değerler seçin.
5. Alt ızgarada, **Fatura Zamanlaması Oluştur**'u seçin. Fatura zamanlamasını aşağıdaki şekilde ayarlanan **Fatura Çalıştırma Tarihi**, **İşlem Durdurma Tarihi** ve **Çalıştırma Durumu** alanlarıyla birlikte oluşturur:

    - **Fatura Çalıştırma Tarihi:** Tarihin fatura sıklığına bağlı olarak belirlenmesiyle ayarlanır.
    - **İşlem durdurma tarihi**: Fatura çalıştırma tarihinden önceki gün.
    - **Çalıştırma Durumu**: **Çalışmadı** olarak otomatik ayarlanır. Otomatik fatura oluşturma işi, belirli bir fatura çalışma tarihi için çalıştırıldığında, bu alanı **Çalıştırma Başarılı** veya **Çalıştırılamadı** olarak güncelleştirir.

## <a name="create-a-fixed-price-invoice-schedule-for-a-contract-line"></a>Sözleşme satırı için Sabit fiyatlı fatura zamanlaması oluşturma

Sözleşme satırında bir Sabit faturalama yöntemi olduğunda sistem, kilometre taşı tabanlı fatura zamanlaması oluşturur. 

> [!NOTE]
> Sözleşme satırıyla eşleştirilmiş bir proje yoksa, bir sözleşme satırında kilometre taşları oluşturulamaz.

Takvim döneminde eşit olarak dağıtılan sabit bir kilometre taşı kümesi için bu zamanlamayı otomatik oluşturmak üzere aşağıdaki adımları tamamlayın.

1. **Ayarlar** > **fatura sıklıkları**'na gidin ve bir fatura sıklığı ayarlayın.
2. Proje sözleşmesi kaydına gidin ve **Özet** sekmesinde, **istenen teslim tarihi** alanında bir tarih seçin.
3. Kilometre taşı zamanlaması oluşturmak için ihtiyacınız olan **sabit fiyatlı** teklif satırını açın. **Faturalandırma Dönüm Noktaları** sekmesinde, Faturalama başlangıcı ve Fatura Sıklığı alanlarında değerler seçin. 
4. Alt ızgarada, **Düzenli Kilometre Taşları Oluştur**'u seçin. Fatura çizelgesi, **kilometre taşı adı**, **kilometre taşı tarihi** ve **kilometre taşı tutarı** alanları aşağıdaki gibi ayarlanmış olarak oluşturulur:

    - **Dönüm noktası adı:** Tarihin fatura sıklığına bağlı olarak belirlenmesiyle ayarlanır.
    - **Dönüm noktası tarihi:** Tarihin fatura sıklığına bağlı olarak belirlenmesiyle ayarlanır.
    - **Kilometre taşı tutarı**: Sözleşme satırındaki teklif tutarının, sıklık ve faturalama başlangıcı ve istenen teslim tarihlerine göre belirlenen kilometre taşı sayısına bölünmesiyle hesaplanır.

    Sözleşme satırının **Tahmini KDV Tutarı** alanında bir değeri varsa bu alan dönemsel kilometre taşları oluştururken aynı zamanda her kilometre taşına da gönderilir.

Fatura kilometre taşları, sözleşme satırının sözleşmeli değerine eşit olmalıdır. Böyle bir program yoksa, **sözleşme satırı** sayfasında bir hata iletisi alırsınız. Hatayı, fatura dönüm değerlerinin satır için kilometre taşları oluşturarak, düzenleyerek veya silerek bu sözleşme yapan değerin toplamını doğrulayarak düzeltebilirsiniz. Değişiklikler yapıldıktan sonra, hatayı kaldırmak için sayfayı yenileyin.

### <a name="manually-create-milestones"></a>Kilometre taşlarını el ile oluşturma

Sabit fiyatlı kilometre taşları, düzenli aralıklarla bölünmediğinde de el ile oluşturulabilir. Manuel olarak dönüm noktası oluşturmak için aşağıdaki adımları tamamlayın.

1. Kilometre taşı oluşturduğunuz sabit fiyatlı sözleşme satırını açın ve **fatura çizelgesi** sekmesinde, alt ızgarada, **+ yeni sözleşme satırı kilometre taşı oluştur**'u seçin. 
2. **Kilometre taşı oluşturma** sayfasında, aşağıdaki tabloya göre gerekli bilgileri girin.

| Alan | Konum | Veri Akışı Açıklaması | Aşağı yönlü etki |
| --- | --- | --- | --- |
| Kilometre Taşı Adı | Hızlı Oluştur | Kilometre taşının adına ait metin alanı. | Bu, proje sözleşme satırı kilometre taşına ve faturaya doldurulur. |
| Proje Görevi | Hızlı Oluştur | Kilometre taşı, proje görevine bağlıysa bu başvuruyu görev durumuna göre kilometre taşı durumu olarak ayarlanan özel mantık eklemek için kullanabilirsiniz. | Uygulamada bir görev için bu başvurunun aşağı yönlü etkisi yoktur. |
| Kilometre Taşı Tarihi | Hızlı Oluştur | Otomatik fatura oluşturma işleminin, bu kilometre taşının durumunun faturalama için dikkate alınması amacıyla araması gereken tarihi ayarlayın. | Bu, proje sözleşme satırı kilometre taşına ve faturaya doldurulur. |
| Fatura Durumu | Hızlı Oluştur | Kilometre taşı oluşturulduğunda, bu durum her zaman **Faturalama için hazır değil** veya **Başlamadı** olarak ayarlanır. | Bu, proje sözleşme satırı kilometre taşına ve faturaya doldurulur. |
| Satır Tutarı | Hızlı Oluştur | Müşteriye faturalanacak kilometre taşının tutarı veya değeri. | Bu, proje sözleşme satırı kilometre taşına ve faturaya doldurulur. |
| Vergi | Hızlı Oluştur | Kilometre taşına uygulanan vergi tutarı. | Bu, proje sözleşme satırı kilometre taşına ve faturaya doldurulur. |

3. **Kaydet ve Kapat**'ı seçin.
