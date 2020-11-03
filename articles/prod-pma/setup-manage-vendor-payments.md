---
title: Ödeme alındığında ödenen satıcı ödemelerini ayarlama ve kullanma
description: Bu konu, müşteri ödemelerini temel alarak kısmi satıcı ödemelerini serbest bırakmak için ödemeli ödeme (pwp) koşullarının nasıl oluşturulacağı açıklanmaktadır.
author: RadhikaRS
manager: AnnBe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: e872c4a2d35cef4cddc6851615c6c4d73b4e9d9a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086303"
---
# <a name="set-up-and-use-pay-when-paid-vendor-payments"></a>Ödeme alındığında ödenen satıcı ödemelerini ayarlama ve kullanma

[!include [banner](../includes/banner.md)]

Bir satıcıyı taşeron olarak çalışacak şekilde onayladığınızda, müşteriniz proje için size ödeme yapana kadar ödemeyi satıcıya vermek isteyebilirsiniz. Bu senaryoyu desteklemek için, satınalma siparişi (PO) satıcıyla ayarlarken ödemeli (PWP) ödeme koşulları ayarlayabilirsiniz.

Örneğin, bir müşteri proje faturasında bir miktar ödeme yaparken, satıcı fatura tutarının bir kısmını veya tümünü serbest bırakabilirsiniz. Müşteriden, ilgili ödemenin yüzdesini aldıktan sonra satıcının ödeme olacağını belirten PWP şartlarını ayarlamanız yeterlidir. Müşteriden kısmi ödeme alırsanız, ilgili satıcı faturalarının bazılarını ödeme için el ile serbest bırakabilirsiniz.

Aşağıdaki örnek, PWP terimleri kullanıldığında süreci özetler.

## <a name="example"></a>Örnek

Kuruluşunuz, yazılımın yüklü olduğu, bilgisayar başına 150,00 ABD Doları (USD) olan 100 sahip bilgisayarlar için müşteri sağlamaya kabul eder. Daha sonra yazılımın yüklü olduğu bilgisayarları size sağlamak için bir satıcı işe alırsınız. Sözleşmeye göre, müşteri kuruluşunuzu ödemeden önce bilgisayarların kalitesini onaylaması gerekir. Kuruluşunuzun ilkesi, müşteri sizi ödeene kadar satıcılara ödeme yapmak için kullanılır. Bu nedenle, projeyi %100 PWP yüzdesine sahip olacak şekilde ayarlarsınız.

Satıcı, 10,000.00 USD için bir faturayla birlikte yazılımın yüklü olduğu 100 bilgisayar gönderir. PWP terimleri projeniz için ayarlandığı için, satıcı bilgisayarların alınması üzerine ödeme yapmayın. Bunun yerine, 15,000.00 için bir faturayla birlikte bilgisayarları müşteriye gönderirsiniz. Müşteri, bilgisayarları inceler ve Proje faturasının tam tutarını onaylar.

Müşteriden tam ödeme aldıktan sonra, satıcı 10,000.00 ödeyin, tüm satıcı faturaları tutarı.

## <a name="set-up-pwp-terms-for-a-project"></a>Proje için PWP şartlarını ayarlama

Bir proje için PWP şartlarını ayarlarken, satıcıya ödeme yapmadan önce, müşterinin size proje için ödemesi gereken minimum tutarı yüzde olarak belirtmeniz gerekir. Eşik tutarı, projenin müşteri faturalarında otomatik olarak hesaplanır. PWP terimlerine ait eşik yüzdesini ayarlamak için bu adımları izleyin.

1. **Proje yönetimi ve muhasebe** \> **Projeler** \> **Tüm projeler** bölümüne gidin.
2. PWP şartlarını ayarlamak istediğiniz projeyi bulun ve açın.
3. **Satıcı anlaşmaları** hızlı sekmesinde **satır ekle** 'yi seçin.
3. **Hesap kodu alanında** , aşağıdakilerden birini seçin:

    - **Tablo** : PWP koşulları tek bir satıcı için uygulanır.
    - **Grup** : PWP koşulları bir satıcı grubundaki tüm satıcılar için uygulanır.
    - **Tümü** : PWP koşulları tüm satıcılara uygulanır.

4. Önceki adımda **tablo** veya **grup** seçeneğini belirlediyseniz, **satıcı/satıcı grubu** alanında, PWP şartlarını uyguladığınız satıcı veya satıcı grubunu seçin. Önceki adımda **tümü** seçeneğini belirlediyseniz, **satıcı/satıcı grubu** alanı düzenlenemez.
5. Satıcı Bekletme koşulları projede satıcı için ayarlanmışsa, **satıcı bekletme şartları** alanında, bekletme koşullarının kural kimliğini seçin.
6. **PWP eşik yüzdesi** alanına proje için eşik yüzdesini girin. Proje için girdiğiniz yüzde, siz satıcıya ödeme yapmadan önce müşterinin size ödemesi gereken minimum tutarı tanımlar.

## <a name="create-a-po-that-has-pwp-terms"></a>PWP koşulları bulunan bir PO oluşturma

Bir satıcıdan bir faturayı deftere naklettiğinizde, satıcı PWP terimlerine tabi olursa, bu terimler PO satırlarında gösterilir. PWP koşullarına sahip bir PO oluşturmak için aşağıdaki adımları izleyin.

1. **Satın alma ve kaynak** \> **satınalma siparişleri** \> **tüm satınalma siparişleri** bölümüne gidin.
2. Eylem Bölmesi'nden **Yeni** seçin. Ardından, **Satınalma siparişi oluştur** iletişim kutusunda, gerekli bilgileri girin ve **Tamam** 'ı seçin.

    Alternatif olarak, **tüm satınalma siparişleri** listesi sayfasında varolan BIR Po öğesini açın.

4. **Satınalma siparişi** sayfasında, **Satınalma siparişi satırları** hızlı sekmesinde, satıcıyla ilgili SS satırının ayrıntılarını gözden geçirin. **Ödeme yaparken ödeme** seçeneği otomatik olarak seçilir ve **PWP eşik yüzdesi** alanındaki değer **Projeler** sayfasındaki **PWP eşik yüzdesi** alanından otomatik olarak kopyalanır.
6. Bir PO satırı için satıcıya PWP şartları uygulamak istemiyorsanız, **ödeme yapılırken öde** seçeneğini temizleyin. Bu durumda, PO satırının **PWP eşik yüzdesi** alanı 0 (sıfır) olarak ayarlanır.

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Bir müşteri ödemesini güncelleştirme ve satıcıya ödeme yapma

Bir satıcı bir proje üzerinde çalışmasını tamamladığında ve size bir fatura gönderdiğinde, proje durumu ve müşteri faturalarını gözden geçirerek, tüm projede PWP şart olup olmadığını belirleyebilirsiniz. Satıcının PWP şartları karşılanıyorsa, projenin müşteri ödemelerini temel alarak, satıcı faturasındaki hangi satırların ödeme yapılacağını belirleyebilirsiniz. PWP koşulları karşılanmasa da satıcıya ücret ödemeniz gerektiğine karar verirseniz, satıcı faturasındaki PWP şartlarını **ödemeli sayfasını ödeyle geçersiz kılabilirsiniz**.

1. **Proje yönetimi ve hesaplama** \> **sorgulamalar ve raporlar** \>**bekletme sorguları** \> **ödeme yaptığınızda ödemesine sahip satıcı faturası** 'na gidin.
2. **Ödemeleri ödemeli yapan satıcı faturaları** sayfasında arama alanına, gözden geçirmek istediğiniz satıcı faturasını bulmak için değerleri girin ve **Arama** 'yı seçin.
3. **Satıcı Fatura satırları** hızlı sekmesinde, değiştirmek istediğiniz satırları seçin.
4. Fatura satırında **ödeme koşulları karşılanıyorsa** öde **satıcı ödemesini serbest bırak** 'ı seçin. **Ödeme yapılırken öde** seçeneği temizlenirse ve **ödeme için hazır** alanının değeri **Evet** olarak değiştirilir.
