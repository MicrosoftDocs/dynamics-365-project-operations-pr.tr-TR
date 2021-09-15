---
title: Alt sözleşme satırı kilometre taşları
description: Bu konu, satıcıyla yapılan alt sözleşme için kilometre taşı tabanlı bir fatura zamanlamasının nasıl oluşturulacağını ve yönetileceğini açıklamaktadır.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3301e5a627e4842009fcd5e352f1b76fd3053ee3
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323800"
---
# <a name="subcontract-line-milestones"></a>Alt sözleşme satırı kilometre taşları

[!include [banner](../../includes/dataverse-preview.md)]

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Dynamics 365 Project Operations'da, sabit fiyatlı faturalama yöntemine sahip bir alt sözleşme satırı, satıcıyla bir kilometre taşı tabanlı fatura zamanlaması belirtebilir.

Satıcı faturalaması için kilometre taşları, ayarlanmış bir sıklık kullanılarak otomatik olarak oluşturulabilir veya bunları el ile oluşturabilirsiniz.

## <a name="automatically-create-a-milestone-based-invoice-schedule-for-a-subcontract-line"></a>Alt sözleşme satırı için kilometre taşı tabanlı fatura zamanlamasını otomatik olarak oluşturma

Eşit olarak dağıtılmış kilometre taşları sabit kümesi için kilometre taşı tabanlı bir fatura zamanlaması oluşturmak üzere aşağıdaki adımları izleyin.

1. **Ayarlar** > **Fatura Sıklığı**'na gidin ve alt sözleşme satırları için fatura sıklığını ayarlayın.
2. **Alt sözleşmeler** sayfasını açın, çalışmak istediğiniz alt sözleşmeyi açın ve ardından kilometre taşı zamanlaması oluşturacağınız sabit fiyatlı alt sözleşme satırını açın.
3. **Alt Sözleşme Satırı Kilometre Taşları** sekmesinde, **Düzenli Kilometre Taşları Oluştur**'u seçin.
4. İletişim kutusunda, bir tarih aralığı, kilometre taşı sayısı ve fatura sıklığı girin veya seçin. Başlangıç tarihi veya kilometre taşlarının sayısını ve fatura sıklığını veya başlangıç tarihini ya da bitiş tarihini ve fatura sıklığını seçebilirsiniz. Bitiş tarihini ve kilometre taşı sayısını seçemezsiniz.
Sistem, bu bilgileri kullanarak **Kilometre taşları** ızgarasında gösterilen kilometre taşlarını ve kayıtları oluşturur.

   - **Kilometre Taşı Adı** - Kilometre taşının adı, fatura sıklığına göre kilometre taşının tarihine ayarlanır.
   - **Kilometre Taşı Tarihi** - Fatura sıklığını temel alan tarih.
   - **Kilometre Taşı Tutarı** - Alt sözleşme satırındaki alt toplam tutarı kilometre taşları sayısına bölünerek hesaplanır.

Alt sözleşme satırının **Tahmini Vergi Tutarı** alanında bir değeri varsa, düzenli kilometre taşları oluşturulurken bu değer her kilometre taşına eşit olarak eklenir.

Alt sözleşme satırı kilometre taşları tutarı toplamının alt sözleşme satırı değerine eşit olması gerekir. Eşit değillerse bir hata oluşur. Kilometre taşı ve vergi tutarlarını oluşturarak, düzenleyerek veya silerek hatayı düzeltebilir ve kilometre taşı toplamının alt sözleşme satırı değerine eşit olduğunu doğrulayabilirsiniz. Değişiklikler yapıldıktan sonra, daha fazla hata olmadığından emin olmak için sayfayı kaydedin ve yenileyin.

## <a name="manually-create-subcontract-line-milestones"></a>Alt sözleşme satırı kilometre taşlarını el ile oluşturma

Bir alt sözleşme satırındaki sabit fiyatlı kilometre taşları, düzenli olarak bölünmeyecekse el ile oluşturulabilir. Bir alt sözleşme satırı kilometre taşını el ile oluşturmak için aşağıdaki adımları izleyin.

1. Gezinti bölmesinde, **Alt sözleşmeler**'i seçin ve çalışmak istediğiniz bir alt sözleşmeyi açın.
2. Kilometre taşı oluşturmak istediğiniz sabit fiyatlı alt sözleşme satırını açın.
3. **Alt sözleşme satırı kilometre taşları** sekmesinde, alt ızgarada **+ Yeni Alt Sözleşme Satırı Kilometre Taşı**'nı seçin.
4. **Yeni Alt Sözleşme Satırı Kilometre Taşı** sayfasında, aşağıdaki tabloya göre gerekli bilgileri girin.

    | Alan | Açıklama |
    | --- | --- |
    | Kilometre Taşı Adı | Kilometre taşının adı. |
    | Açıklama | Kilometre taşı açıklaması.  |
    | Kilometre Taşı Tarihi | Otomatik fatura oluşturma işleminin, faturalama için değerlendirmek üzere bu kilometre taşının durumuna bakması gereken tarih. Bu değer, bu alt sözleşme için faturalama sırasında satıcı fatura satırına dahil edilir. |
    | Sayı | Müşteriye Faturalanacak kilometre taşına ait tutar veya değer. Bu değer, bu alt sözleşme için faturalama sırasında satıcı fatura satırına dahil edilir. |
    | Vergi | Kilometre taşına uygulanan vergi tutarı. Bu değer, bu alt sözleşme için faturalama sırasında satıcı fatura satırına dahil edilir. |
    | Vergi sonrası tutar | Bu salt okunur alan Tutar + Vergi olarak hesaplanır. Bu değer, bu alt sözleşme için faturalama sırasında satıcı fatura satırına dahil edilir. |
    | Fatura Durumu | Kilometre taşı oluşturulduğunda, bu durum her zaman **Faturalama için hazır değil** olarak ayarlanır.  Durum **Faturalamak için hazır** olduğunda, satıcı faturası oluşturma işlemi satıcı faturasındaki bu kilometre taşını içerir. |

5. **Kaydet ve Kapat**'ı seçin.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]