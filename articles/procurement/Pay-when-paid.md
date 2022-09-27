---
title: Ödeme yapılırken ödenen satıcı ödemeleri
description: Bu konuda, ödeme yapılırken ödeme (PWP) senaryosunun nasıl kullanılacağı açıklanmaktadır.
author: mukumarm
ms.date: 08/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: mukumarm
ms.openlocfilehash: d1fe8d92663b31b22dc405fc1f3e06d976e6c5dc
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/16/2022
ms.locfileid: "9525349"
---
# <a name="pay-when-paid-vendor-payments"></a>Ödeme yapılırken ödenen satıcı ödemeleri

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Bu konuda, ödeme yapılırken ödeme (PWP) senaryosunun nasıl kullanılacağı açıklanmaktadır.

## <a name="create-a-purchase-order-that-has-pwp-terms"></a>PWP koşullarına sahip bir satınalma siparişi oluşturma

Bir satıcıdan bir faturayı deftere naklettiğinizde, satıcı PWP terimlerine tabi olursa, bu terimler satınalma siparişi (PO) satırlarında gösterilir. PWP koşullarına sahip bir PO oluşturmak için aşağıdaki adımları izleyin.

1. Microsoft Dynamics 365 Finance'te, aşağıdaki adımlardan birini izleyin:

    - **Satın alma ve kaynak** \> **satınalma siparişleri** \> **tüm satınalma siparişleri** bölümüne gidin. Eylem Bölmesi'nden **Yeni** seçin. **Satınalma siparişi oluştur** iletişim kutusunda, projede PWP koşullarının ayarlandığı satıcıyı seçin, diğer gerekli bilgileri girin ve **Tamam**'ı seçin.
    - **Proje yönetimi ve muhasebe** \> **Projeler** \> **Tüm projeler** bölümüne gidin. Eylem Bölmesi'nde **Yönet** sekmesinde **Öğe görevi**'ni seçin. Satınalma siparişini seçin. Projede PWP koşullarının ayarlandığı satıcıyı ve ardından **Tamam**'ı seçin.

2. **Satınalma siparişi** sayfasındaki **Satınalma siparişi satırları** hızlı sekmesinde, **Satır ekle**'yi seçerek yeni bir satınalma siparişi satırı oluşturun.
3. Öğe numarasını veya tedarik kategorisini seçip gerekli diğer ayrıntıları girin. Satıcının satınalma siparişi satırı ayrıntılarını gözden geçirin.

    **Ödeme yaparken ödeme** seçeneği otomatik olarak seçilir ve **PWP eşik yüzdesi** alanındaki değer **Projeler** sayfasındaki **PWP eşik yüzdesi** alanından otomatik olarak kopyalanır.

4. Bir PO satırı için satıcıya PWP şartları uygulamak istemiyorsanız, **ödeme yapılırken öde** seçeneğini temizleyin. Bu durumda, satınalma siparişi satırının **PWP eşik yüzdesi** alanı **0** (sıfır) olarak ayarlanır.
5. Eylem bölmesindeki, **Satınalma siparişi** sayfasında, **Satınalma** sekmesinde, **Onayla**'yı seçerek satınalma siparişini onaylayın.
6. Satınalma siparişinin faturasını oluşturmak için Eylem Bölmesi'nde, **Fatura** sekmesindeki **Fatura** seçeneğini belirleyin.

## <a name="create-a-project-invoice-proposal"></a>Proje faturası teklifi oluşturma

Proje faturası teklifleri müşteri için proje faturaları oluşturmada kullanılır. PWP senaryosunda, satıcı ödemeleri PWP ayarlarına göre, müşterinin ödemelerine bağlıdır. Ancak, müşteri ödemesi olmadan ödemeleri istediğiniz zaman serbest bırakmanızı sağlayan seçenekler de vardır. Müşteriye bir proje faturası oluşturmak için aşağıdaki adımları izleyin.

1. Müşteri etkileşimi uygulamalarında, **Proje**\> **Projeler** seçeneğine gidip projeyi seçin.
2. **Gerçek Değerler** sekmesinde, **Faturalandırılmamış satışlar** hareket türüne sahip satınalma siparişi tarafından oluşturulan gerçek değer satırını seçin. Ardından, **Faturalama için hazır**'ı seçin.
3. **Satışlar** \> **Satışlar** \> **Proje sözleşmesi**'ne gidin ve proje sözleşmesini seçin.
4. Müşteri faturasını oluşturmak için Eylem Bölmesi'nde **Fatura**'yı seçin.
5. Finance'te, **Proje yönetimi ve muhasebe** \> **Periyodik** \> **Hazırlama tablosundan alma**'ya gidin ve Project Operations tümleştirme günlüğünü oluşturmak için **Tamam**'ı seçin.
6. **Proje yönetimi ve muhasebe** \> **Proje faturaları** \> **Proje faturası teklifi**'ne gidin ve proje için oluşturulan fatura teklifini deftere nakletmek üzere **Deftere Naklet**'i seçin.

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Bir müşteri ödemesini güncelleştirme ve satıcıya ödeme yapma

Bir satıcı bir proje üzerinde çalışmasını tamamladığında ve size bir fatura gönderdiğinde, proje durumu ve müşteri faturalarını gözden geçirerek, tüm projede PWP şartlarının karşılanıp karşılanmadığını belirleyebilirsiniz. Satıcının PWP şartları karşılanıyorsa, projenin müşteri ödemelerini temel alarak, satıcı faturasındaki hangi satırların ödeme yapılacağını belirleyebilirsiniz. PWP koşulları karşılanmasa da satıcıya ücret ödemeniz gerektiğine karar verirseniz, satıcı faturasındaki PWP şartlarını **ödemeli sayfasını ödeyle geçersiz kılabilirsiniz**.

1. Finance'te **Proje yönetimi ve muhasebe** \> **Projeler** \> **Tüm projeler**'e gidin ve projeyi seçin.
2. Eylem Bölmesi'nde, **Denetim**'i, ardından **Satıcı faturaları**'nı seçerek proje için oluşturulan tüm satıcı faturalarını görüntüleyebilirsiniz.
3. **Ödemeleri ödemeli yapan satıcı faturaları** sayfasında arama alanına, gözden geçirmek istediğiniz satıcı faturasını bulmak için değerleri girin ve **Arama**'yı seçin.
4. Yalnızca PWP faturalarını görüntülemek için **Ödeme yapılırken öde** seçeneğini belirleyin.
5. **Satıcı Fatura satırları** hızlı sekmesinde, ödeme için serbest bırakmak istediğiniz satırları seçin.
6. **Satıcı ödemesini serbest bırak**'ı seçin. **Ödeme yapılırken öde** seçeneği temizlenirse ve **ödeme için hazır** alanının değeri **Evet** olarak değiştirilir.
