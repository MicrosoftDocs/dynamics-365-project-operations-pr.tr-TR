---
title: Proje tabanlı sözleşme satırında fatura zamanlamaları oluşturma - lite
description: Bu konu, fatura zamanlamaları ve kilometre taşları oluşturma hakkında bilgi sağlar.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: dc0cf92ed7af0353baa0f93fc7fb69e02905f805eb04a7b4c7bc99cfe59da62a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006090"
---
# <a name="create-invoice-schedules-on-a-project-based-contract-line---lite"></a>Proje tabanlı sözleşme satırında fatura zamanlamaları oluşturma - lite

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Proje tabanlı sözleşme satırında fatura zamanlaması ekleyebilirsiniz. Yalnızca, sözleşmenin bir proje sözleşmesi oluşturmak için kazanılarak faturalandırılmasına izin verilir. Fatura zamanlamaları, proje tabanlı bir sözleşme satırının taslak faturalarının otomatik olarak oluşturulmasına izin verir. Faturaları her zaman el ile oluşturmayı planlıyorsanız, proje tabanlı bir sözleşme satırında veya bir sözleşme satırında fatura zamanlamaları oluşturmayı atlayabilirsiniz.

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-contract-line"></a>Proje tabanlı sözleşme satırı için zaman ve materyal fatura zamanlaması oluşturma

Proje tabanlı sözleşme satırının saati ve malzeme faturalama yöntemi oldğuunda, tarih tabanlı fatura zamanlaması oluşturur. Otomatik olarak tarih tabanlı fatura zamanlaması oluşturmak için aşağıdaki adımları tamamlayın.

1. Fatura sıklığını ayarlamak için **Ayarlar** > **Fatura frekanslara** gidin.
2. Proje sözleşmesini açın ve **Özet** sekmesinde, istenen teslimat tarihini ayarlayın.
3. Tarih tabanlı fatura zamanlaması oluşturmak istediğiniz zaman ve malzeme sözleşmesi satırını açın. 
4. **Fatura çizelgesi** sekmesinde, bir faturalama başlangıç tarihi ve fatura sıklığını seçin. 
5. Alt ızgarada, **Fatura Zamanlaması Oluştur**'u seçin.

    Sistem fatura zamanlamasını aşağıdaki alan bilgileriyle birlikte oluşturur:

    - **Fatura çalışma tarihi**, Fatura sıklığı temelinde bir tarih olarak ayarlanır.
    - **İşlem durdurma tarihi**, **Fatura Çalıştırma Tarihi**'nden önceki gün olarak ayarlanır.
    - **Çalıştırma Durumu**, **Çalışmadı** olarak otomatik ayarlanır. Otomatik fatura oluşturma işi, belirli bir **fatura çalışma tarihi** için çalıştırıldığında, bu alanı **Çalıştırma Başarılı** veya **Çalıştırılamadı** olarak güncelleştirir.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-contract-line"></a>Proje tabanlı sözleşme satırında sabit fiyatlı fatura zamanlaması oluşturma

Proje tabanlı bir sözleşme satırı sabit fiyatlı faturalandırma yöntemine sahip olduğunda kilometre taşına dayalı bir fatura çizelgesi oluşturabilirsiniz. Takvim dönemi için eşit olarak dağıtan sabit bir kilometre taşları kümesi için kilometre taşı tabanlı bir fatura zamanlaması oluşturmak üzere aşağıdaki adımları izleyin.

1. Fatura sıklığını ayarlamak için **Ayarlar** > **Fatura frekanslara** gidin.
2. Proje sözleşmesini açın ve **Özet** sekmesinde, istenen teslimat tarihini ayarlayın.
3. Kilometre taşı zamanlaması oluşturmak için gereken sabit fiyatlı sözleşme satırını açın. 
4. **Fatura çizelgesi** (Fatura Kilometre Taşları) sekmesinde, bir faturalama başlangıç tarihi ve fatura sıklığını seçin. 
5. Alt ızgarada, **Düzenli Kilometre Taşları Oluştur**'u seçin.

    Sistem fatura zamanlamasını aşağıdaki Kilometre Taşları bilgileriyle birlikte oluşturur.

    - **Kilometre taşı adı**, Fatura sıklığı temel alınarak dikte edilen tarihe ayarlanır.
    - **Kilometre taşı tarihi**, Fatura sıklığı temel alınarak dikte edilen tarihe ayarlanır.
    - **Kilometre taşı miktarı**, proje tabanlı sözleşme satırındaki sözleşme tutarı sıklık, faturalama başlangıcı ve istenen teslim tarihleri tarafından dikte edilmiş şekilde kilometre taşları sayısına bölünerek hesaplanır.
    - Sözleşme satırının **Tahmini KDV Tutarı** alanında bir değeri varsa bu alan dönemsel kilometre taşları oluştururken aynı zamanda her kilometre taşına de gönderilir.

Fatura kilometre taşları proje tabanlı sözleşme satırının sözleşme değerine eşit olmalıdır. Eşit değillerse bir hata oluşur. Bu hatayı, fatura dönüm değerlerinin, kilometre taşları oluşturarak, düzenleyerek veya silerek, satır için sözleşme yapan değerin toplamını doğrulayarak düzeltebilirsiniz. Değişiklikler yapıldıktan sonra, sayfayı yenileyin.

### <a name="manually-create-milestones"></a>Kilometre taşlarını el ile oluşturma

Sabit fiyatlı kilometre taşları, düzenli olarak bölünmeyeceği zaman el ile oluşturulabilir. Manuel olarak kilometre taşı oluşturmak için aşağıdaki adımları izleyin.

1. Kilometre taşı zamanlaması oluşturmak için gereken sabit fiyatlı sözleşme satırını açın. 
2. **Fatura çizelgesi** sekmesinde, alt ızgarada, **+ yeni sözleşme satırı kilometre taşı oluştur**'u seçin.
3. **Kilometre taşı oluşturma** formunda, aşağıdaki tabloya göre gerekli bilgileri girin. 

| Alan | Konum | Veri Akışı Açıklaması | Aşağı yönlü etki |
| --- | --- | --- | --- |
| Kilometre Taşı Adı | Hızlı Oluştur | Kilometre taşının adına ait metin alanı. | Bu alan, Proje sözleşmesi satır kilometre taşına ve faturaya dahil edilir. |
| Proje Görevi | Hızlı Oluştur | Kilometre taşı bir proje görevine bağlıysa, özel mantık eklemek ve görev durumuna göre kilometre taşı durumunu ayarlamak için bu başvuruyu kullanın. | Bu başvurunun bir göreve olumsuz etkisi yoktur. |
| Kilometre Taşı Tarihi | Hızlı Oluştur | Otomatik fatura oluşturma işleminin, bu kilometre taşına ait durumu, faturalama için kabul etmek üzere araması gerektiği tarih. | Bu, Proje sözleşmesi satır kilometre taşına ve faturaya dahil edilir. |
| Fatura Durumu | Hızlı Oluştur | Kilometre taşı oluşturulduğunda, bu durum her zaman **faturalama için hazır** veya **başlatılmamış** olarak ayarlanır. | Bu, Proje sözleşmesi satır kilometre taşına ve faturaya dahil edilir. |
| Satır Tutarı | Hızlı Oluştur | Müşteriye Faturalanacak kilometre taşına ait tutar veya değer. | Bu alan, Proje sözleşmesi satır kilometre taşına ve faturaya dahil edilir, |
| Vergi | Hızlı Oluştur | Kilometre taşına uygulanan vergi tutarı. | Bu, Proje sözleşmesi satır kilometre taşına ve faturaya dahil edilir. |

4. **Kaydet ve Kapat**'ı seçin.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]