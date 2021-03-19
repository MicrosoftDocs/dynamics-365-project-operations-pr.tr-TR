---
title: Proje tabanlı teklif satırlarındaki fatura zamanlamaları
description: Bu konuda, teklif satırları için fatura zamanlamaları ve kilometre taşları oluşturma hakkında bilgiler sağlanmaktadır.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 506de5217de48814d6b8f03a10c7c8648c575198
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278307"
---
# <a name="invoice-schedules-on-project-based-quote-lines"></a>Proje tabanlı teklif satırlarındaki fatura zamanlamaları

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Proje tabanlı teklif satırı, fatura zamanlamasını ifade etme özelliği sunar. Bu, uygulama bir Teklif satırına bağlı olduğunda projeyi faturalamayı desteklemediğinden teklif aşaması sırasında isteğe bağlıdır. Faturalamaya ancak teklif kazanıldıktan sonra izin verilir. Teklif aşaması sırasında fatura zamanlaması oluşturmanın tek aşağı yönlü etkisi, bu fatura zamanlamasının proje tabanlı sözleşme satırı üzerine kopyalanmasıdır. Teklif aşaması sırasında fatura zamanlaması oluşturmazsanız bunu proje tabanlı sözleşme satırında yapabilirsiniz.

Genel olarak, fatura zamanlamalarının amacı, proje tabanlı sözleşme satırı için taslak faturaların otomatik olarak oluşturulmasına izin vermektir. 

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-quote-line"></a>Proje tabanlı teklif satırı için Zaman ve malzeme fatura zamanlaması oluşturma

Proje tabanlı teklif satırı için faturalama yöntemi, Zaman ve malzeme olduğunda sistem, tarih tabanlı fatura zamanlaması oluşturur. Otomatik olarak tarih tabanlı fatura zamanlaması oluşturmak için aşağıdaki adımları tamamlayın.

1. **Ayarlar** > **fatura sıklıkları**'na gidin ve bir fatura sıklığı ayarlayın.
2. **Teklifler** sayfasında, Proje teklifini açın ve **Özet** sekmesinde, istenen teslim tarihini ayarlayın.
3. Tarih tabanlı fatura zamanlaması oluşturmanız için gereken zaman ve malzeme teklif satırını açın. 
4. **Fatura Zamanlaması** sekmesinde, **Faturalama başlangıcı** ve **Fatura Sıklığı** alanlarında değerler seçin. 
5. Alt ızgarada, **Fatura Zamanlaması Oluştur**'u seçin.
6. Uygulama, fatura zamanlamasını aşağıdaki şekilde ayarlanan **Fatura Çalıştırma Tarihi**, **İşlem Durdurma Tarihi** ve **Çalıştırma Durumu** alanlarıyla birlikte oluşturur:

    - **Fatura Çalıştırma Tarihi**, tarihin fatura sıklığına bağlı olarak belirlenmesiyle ayarlanır.
    - **İşlem durdurma tarihi**, **Fatura Çalıştırma Tarihi**'nden önceki gün olarak ayarlanır.
    - **Çalıştırma Durumu**, **Çalışmadı** olarak otomatik ayarlanır. Otomatik fatura oluşturma işi, belirli bir fatura çalışma tarihi için çalıştırıldığında, bu alanı **Çalıştırma Başarılı** veya **Çalıştırılamadı** olarak güncelleştirir.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-quote-line"></a>Proje tabanlı teklif satırı için Sabit fiyatlı fatura zamanlaması oluşturma

Proje tabanlı teklif satırında bir **Sabit** faturalama yöntemi olduğunda sistem, kilometre taşı tabanlı fatura zamanlaması oluşturur. Takvim döneminde eşit olarak dağıtılan sabit bir kilometre taşı kümesi için bu zamanlamayı otomatik oluşturmak üzere aşağıdaki adımları tamamlayın.

1. **Ayarlar** > **fatura sıklıkları**'na gidin ve bir fatura sıklığı ayarlayın.
2. **Teklifler** sayfasında, Proje teklifini açın ve **Özet** sekmesinde, istenen teslim tarihini ayarlayın.
3. Kilometre taşı zamanlaması oluşturmak için ihtiyacınız olan sabit fiyatlı teklif satırını açın. 
4. **Fatura Zamanlaması** sekmesinde, **Faturalama başlangıcı** ve **Fatura Sıklığı** alanlarında değerler seçin. 
5. Alt ızgarada, **Düzenli Kilometre Taşları Oluştur**'u seçin.
6. Uygulama, fatura zamanlamasını bir kilometre taşı adı, tarihi ve tutarı ile oluşturur.

    - Kilometre taşı adı, tarihin fatura sıklığına bağlı olarak belirlenmesiyle ayarlanır.
    - Kilometre taşı tarihi, tarihin fatura sıklığına bağlı olarak belirlenmesiyle ayarlanır.
    - Kilometre taşı tutarı, proje tabanlı teklif satırındaki teklif tutarının, sıklık ve faturalama başlangıcı ve istenen teslim tarihlerine göre belirlenen kilometre taşı sayısına bölünmesiyle hesaplanır.
    - Teklif satırında ayrıca tahmini vergi tutarı varsa düzenli kilometre taşları oluştururken bu değer, her kilometre taşı arasında eşit olarak bölünür.

### <a name="manually-create-milestones"></a>Kilometre taşlarını el ile oluşturma

Sabit fiyatlı kilometre taşları, düzenli aralıklarla bölünmediğinde de el ile oluşturulabilir. Kilometre taşını el ile oluşturmak için:

Kilometre taşı oluşturmak için ihtiyacınız olan Sabit fiyatlı teklif satırını açın. **Fatura çizelgesi** sekmesinde, alt ızgarada, **+ Yeni teklif satırı kilometre taşı oluştur**'u seçin ve aşağıdaki tabloya göre gerekli bilgileri girin.

| **Alan** | **Konum** | **Açıklama** | **Aşağı yönlü etki** |
| --- | --- | --- | --- |
| Kilometre taşı adı | Hızlı oluştur | Kilometre taşının adı. | Bu, proje sözleşme satırı kilometre taşına ve faturaya doldurulur |
| Proje Görevi | Hızlı oluştur | Kilometre taşı, proje görevine bağlıysa bu başvuruyu görev durumuna göre kilometre taşı durumu olarak ayarlanan özel mantık eklemek için kullanabilirsiniz. | Uygulamada bir görev için bu başvurunun aşağı yönlü etkisi yoktur. |
| Kilometre taşı tarihi | Hızlı oluştur | Otomatik fatura oluşturma işleminin, bu kilometre taşının durumunun faturalama için dikkate alınması amacıyla araması gereken tarihi ayarlayın. | Bu, proje sözleşme satırı kilometre taşına ve faturaya doldurulur. |
| Fatura durumu | Hızlı oluştur | Kilometre taşı oluşturulduğunda, bu durum her zaman **Faturalama için hazır değil** olarak ayarlanır. | Bu, proje sözleşme satırı kilometre taşına ve faturaya doldurulur. |
| Satır Tutarı | Hızlı oluştur | Müşteriye faturalanacak kilometre taşının tutarı veya değeri. | Bu, proje sözleşme satırı kilometre taşına ve faturaya doldurulur. |
| Vergi | Hızlı oluştur | Kilometre taşına uygulanacak vergi tutarı. | Bu, proje sözleşme satırı kilometre taşına ve faturaya doldurulur. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]