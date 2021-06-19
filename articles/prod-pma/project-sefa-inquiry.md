---
title: Federal ödüller sorgulaması hakkında harcamaların zamanlaması
description: Bu konu, Federal ödüller sorgulaması hakkında harcamaların zamanlaması hakkında bilgi sağlar.
author: velofog
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: a16b0fb097124e26da09e220a1239cd6df303f98
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010090"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a>Federal ödüller sorgulaması hakkında harcamaların zamanlaması

[!include [banner](../includes/banner.md)]

Yönetim ve Döngüsel Bütçe Ofisi A-133'e göre, federal fonlar alan kurumlar, tek denetimler olarak da bilinen denetim gereksinimlerine tabidir. Denetim işlemi, bir yineleme temeline göre gelirler ve harcamaların gelir ve harcamaları hakkında rapor vermek için kullanılır. Tek denetim raporunun bir bölümü, Federal Ödülleri (SEFA) harcamaları için zamanlama içerir.

Federal ödüllere yönelik harcamaların zamanlaması, Federal yerli yardım (CFDA) başlığı ve numarasını, ihracat numarasını, ihracat yılını, fonlar sunan Federal acenteleri ve geçiş varlığının adını içerir. Sorgu belirli bir döneme ait olur. Genellikle bu dönem, bir mali yıl olan mali ekstre periyodu ile aynıdır.

Sorgu, seçili tarih aralığında İzdüşüm tarihleri olan onayları içerir. Sorgulama işleminin **izin verici Kurumu** sütunu izin müşterisini veya doğrudan bir izin için de verici Kurumu gösterir. Doğrudan bir atama için, **doğrudan acentesi** sütunu müşteri ver'i gösterir. Doğrudan bir atama için, **doğrudan acentesi** sütunu müşteri ver'i gösterir.

## <a name="set-up-the-cfda-clusters"></a>CFDA kümelerini ayarlama

Federal ödüller sorgulaması için harcamaların zamanlamasında CFDA numaralarıyla ilişkilendirilebileceği CFDA kümeleri ayarlamanız gerekir.

1. **Proje yönetimi ve Muhasebe \>Kurulum \> İzinler \> Federal yerli yardım kümeleri katalogu**'na gidin.
2. CFDA kümesi oluşturmak için **Yeni** seçeneğini belirleyin.
3. Küme adını girin.
4. Yaptığınız değişiklikleri kaydetmek için **Kaydet**'i seçin.

## <a name="set-up-cfda-numbers"></a>CFDA numaralarını ayarla

Federal ödüller sorgulaması için harcamaların zamanlamasına dahil edilen ve izinlere eklenebilecek CFDA numaraları ayarlamanız gerekir.

1. **Proje yönetimi ve Muhasebe \>Kurulum \> İzinler \> Federal yerli yardım numaraları katalogu**'na gidin.
2. CFDA numarası oluşturmak için **Yeni** seçeneğini belirleyin.
3. **Numara** kutusuna CFDA numarasını girin.
4. **Sekme** tuşuna basın.
5. **Açıklama** kutusuna CFDA başlığını girin.
6. **Sekme** tuşuna basın.
7. İsteğe bağlı: **Program kümesi** alanına uygun CFDA kümesini ekleyin.
8. Yaptığınız değişiklikleri kaydetmek için **Kaydet**'i seçin.

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Federal ödüller sorgulaması hakkında harcamaların zamanlamasını bildirmek için onayları ayarlayın.

1. **Proje yönetimi ve muhasebe \> İzinler \> İzinler**'e gidin ve varolan bir izin öğesini seçin.
2. **Kurulum** hızlı sekmesinde,**Federal Yerli Yardım Kataloğu** alanında CFDA numarasını atayın. İzin üzerindeki CFDA numarası, örneğin raporlama için, CFDA kümesini belirler.
3. **İlgili kişi bilgileri** hızlı sekmesinde, aşağıdaki adımları izleyerek izin veren bilgilerini girin:

    1. **Müşteri izni** alanında, izinden sorumlu olan müşteriyi girin. Varolan bir izin için, bu bilgiler zaten girilmiş olabilir.
    2. Müşterinin karar veren müşteri olup olmadığını belirtin. İzin müşterisi bir fonlayıcı ise, **doğrudan** onay kutusunu temizlenmiş olarak bırakın. Başka bir müşteri fon veren olursa ve para harcamaktan ve izlemeyle müşteri sorumluysanız, **doğrudan** onay kutusunu seçin.

4. Önceki adımda **Doğrudan** onay kutusunu seçtiyseniz, **İzin veren Kurum** alanında, izni sağlayan müşteriyi girin. İzin veren Kurumu ve izin müşterisi aynı müşteri olamaz.

İşte size bir pass-through verme örneği:

Federal kamu sektörü bir eyalet için bir altyapı projesi almıştır. Federal kamu kurumu, eyalete harcanacak para verdi. Bu durumda, Federal Kamu Kurumu izin verici kurumdur ve eyalet de izin müşterisidir.

> [!NOTE] 
> Özelliği ilk açtığınızda, ilk CFDA numaraları izinlerdeki mevcut numaralar kullanılarak girilir.

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a>İzin türüne dayalı olarak SEFA raporlamasına izin verir.

1. **Proje yönetimi ve muhasebe \> Kurulum \> İzinler \> İzin türleri** bölümüne gidin.
2. **Varsayılan bilgiler** hızlı sekmesinde, **Federal Ödüller Sorgusunun Masraflar Zamanlaması Dışında Bırak** onay kutusunu seçin.
3. Yaptığınız değişiklikleri kaydetmek için **Kaydet**'i seçin.

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Federal ödüller sorgulaması hakkında harcamaların zamanlamasını çalıştır

1. **Proje yönetimi ve hesap \> Sorgulama ve raporlar \> İzin sorgusu \> Federal ödüllere yönelik harcamaları için zamanlama**'ya gidin.
2. **Parametreler** bölümünde şu adımları izleyin:

    1. **Tarih aralığı** alanında, tarih aralığına ait kodu seçin. Alternatif olarak, **Başlangıç tarihi** ve **bitiş tarihi** alanlarında, tarih aralığını tanımlayın.
    2. İsteğe bağlı: sorgulamayı yalnızca ödeme hareketlerini eklemek Için, **yalnızca faturalandı gelir dahil et** seçeneğini **Evet** olarak ayarlayın.

## <a name="columns"></a>Sütunlar

Federal ödüllere yönelik harcamaların zamanlaması aşağıdaki sütunları içerir:

- Federal yerli yardım kümesi adı kataloğu
- İzin veren kurum
- Geçiş kurumu
- İzin adı
- İzin kimliği
- İzin Uygulaması Kimliği
- Federal yerli yardım kataloğu
- Girişler
- Masraflar


[!INCLUDE[footer-include](../includes/footer-banner.md)]