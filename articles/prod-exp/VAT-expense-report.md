---
title: KDV kurtarma
description: Bu konuda katma değer vergisi (KDV) işlemlerinde para iadelerini geir almayı açıklar.
author: saraschi2
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76706fd8ced58063b05bc8ebe4b25c1dddbf0890e72e9c7194d17ff2937dc8ca
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986065"
---
# <a name="vat-recovery"></a>KDV kurtarma 

Uygun katma değer vergisi (KDV) işlemlerinde para iadelerini almak için bir şirket veya kuruluşun doğru bilgileri tanımlaması, toplaması, doğrulaması ve göndermesi gerekir. Bu süreç birden fazla görev içerir ve şirketinizin büyüklüğüne bağlı olarak birkaç çalışanı veya rolü içerebilir.

Gider yönetimi modülünde, KDV'yi düşmek için aşağıdaki önkoşulların tamamlanması gerekir:

- Gider kategorilerine tahsis edilen ülkeler/bölgeler için vergi kodları oluşturulmalıdır.
- Her vergi kodu için bir satış vergisi grubu oluşturulmalıdır.
- Her satış vergisi grubu için bir öğe satış vergisi kodu oluşturulmalıdır.

Önkoşullar tamamlandıktan sonra KDV işlemleriyle ilgili para iadelerini istemek için aşağıdaki adımların tamamlanması gerekir.

1. Gider raporunda, uygun KDV para iadelerini belirlemek için kredi kartı işlemleriyle ilgili vergi bilgilerini girin.
2. Tüm vergi bilgilerinin eksiksiz olduğunu doğrulayın ve ardından gider raporunu gönderin.
3. Uluslararası KDV'den düşme işlemi için uygun olan giderleri işleyin.
4. Uluslararası vergiden düşme para iadelerini dosyalamak için KDV'den düşme verilerini üçüncü taraf satıcıya gönderin.
5. Yurtiçi KDV'den düşme için giderleri işleyin.

Aşağıdaki bölümlerde, Contoso çalışanların her adımı nasıl tamamladığını gösteren örnekler sağlanmıştır.

## <a name="on-an-expense-report-enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>Gider raporunda, uygun KDV para iadelerini belirlemek için kredi kartı işlemleriyle ilgili vergi bilgilerini girin.

ABD'de yer alan Contoso'da satış temsilcisi olan İpek, yakın zamanda Birleşik Krallık'a yaptığı bir satış gezisinden döndü. Nancy seyahati sırasında yemek için bazı kişisel kredi kartı harcamaları yapar. Nancy şimdi giderleri mutabık kılmak için bir gider raporu oluşturmalıdır.

Nancy bilgileri gider raporuna girdiğinde **Gider raporu düzenleme** sayfasında **Ülke/bölge** alanında **Birleşik Krallık**'ı seçer. Satış vergisi grupları listesi, yalnızca Birleşik Krallık için geçerli olan grupları gösterecek şekilde filtrelenir. Nancy **Birleşik Krallık 001** satış vergisi grubunu seçer ve ardından satış vergisi grubu için **Yemek**'i seçer. Bundan sonra Nancy konaklama için yeni bir işlem ekler. Birleşik Krallık'ta konaklama için yalnızca bir satış vergisi grubu ve bir öğe satış vergisi grubu olduğundan, bu bilgiler Nancy'nin gider raporunda otomatik olarak doldurulur.

Contoso ilkelerine göre, tüm giderlerin eşleşen bir makbuzu olmalıdır. Bu nedenle, Nancy gider raporunu kaydettiğinde gider raporunda listelediği her işlem için bir makbuz eklemesi gerektiğini belirten bir ileti alır. Nancy, gider raporuna her işlem makbuzunun dijital bir görüntüsünü eklediğini doğrular ve ardından raporunu onay için gönderir. Daha sonra kağıt makbuzları arka ofis işleme takımına gönderir. Bu takım, KDV kurtarma verilerini, Contoso için uluslararası KDV kurtarmalarını dosyalayan üçün taraf satıcıya gönderecektir.

## <a name="make-sure-that-all-tax-information-is-complete-and-then-post-the-expense-report"></a>Tüm vergi bilgilerinin eksiksiz olduğunu doğrulayın ve ardından gider raporunu gönderin

Contoso'da borç hesabı koordinatörü olan Nisan'ın, rapor deftere nakledilmeden önce bir gider raporunda eksik olan vergi bilgilerini girmesi gerekiyor. **Gider raporu ayrıntıları** sayfasını açar ve Nancy'nin onaylanmış gider raporunu görür. Ardından April, işlemlerin ayrıntılarını görüntülemek için gider raporunu açar. Nancy'nin işlemlerden biri için bir öğe satış vergisi grubunu girmediğini görür. Bu bilgiler sağlanmadığından April, gider raporunu gönderemez. Bu nedenle, Gider yönetiminde **Vergi yapılandırmaları** sayfasına bakar ve ülke/bölge ve işlem türü için uygun öğe satış vergisi grubunu bulur. April artık gider raporunu genel muhasebeye gönderebilir.

April, gider raporunu gönderdiğinde bir KDV'den düşülebilir iş öğesi oluşturulur. Bu iş öğesi, arka ofis işleme takımının bir üyesine atanır. April, gönderme işleminin başarılı olduğunu onaylayan bir ileti alır. Bu ileti, vergiden düşme için belirlenen KDV işlemlerinin sayısını da listeler.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Uluslararası KDV'den düşme işlemi için uygun olan giderleri işleme

Contoso'nun arka ofis işleme takımının bir üyesi olan Arnie, KDV kurtarma için gerekli tüm bilgilerin gider raporlarına dahil edildiğini onaylamaktan sorumludur. **Gider vergisinden düşme** sayfasını açar ve Nancy'nin gönderdiği gider raporunu seçer. Arnie ardından gereken tüm makbuzların eklendiğini ve doğru satış vergisi grubu ve öğe satış vergisi kodlarının girildiğini doğrular.

Arnie, kağıt makbuzları Nancy'den aldığında bunları dijital makbuzlara göre doğrular ve ardından gider raporunun durumunu **Vergiden düşmeye hazır** olarak değiştirir.

## <a name="send-vat-recovery-data-to-the-third-party-vendor-to-file-international-recovery-returns"></a>Uluslararası vergiden düşme para iadelerini dosyalamak için KDV'den düşme verilerini üçüncü taraf satıcıya gönderin.

Arnie, gider raporu verilerini KDV'den düşme iadelerini dosyalayacak üçüncü taraf satıcıya göndermeye hazır olduğunda, **Gider vergisinden düşme** sayfasını açar. Sayfayı yalnızca **Vergiden düşmeye hazır** olarak işaretlenmiş gider raporlarını gösterecek şekilde filtreler. Arnie ardından **Dosya** &gt; **Excel'e Aktar**'ı seçer. Gider raporlarından alınan KDV bilgileri, Microsoft Excel çalışma sayfasına dışarı aktarılır. Arnie bu çalışma sayfasını üçüncü taraf satıcıya gönderir ve kağıt makbuzların kurye ile gönderildiğini belirten bir ileti ekler.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Yurtiçi KDV'den düşme için giderleri işleme

Arnie, gider raporu işlemlerinin KDV'den düşme için uygun olduğunu ve dijital makbuzların raporlara eklendiğini doğrulamalıdır. Yurtiçi vergiden düşmeye uygun giderleri işlemeye başlamak için Arnie, **Gider vergisinden düşme** sayfasını açar ve doğrulama gerektiren gider raporunu seçer. Makbuzların çalışan yerine şirket adına olduğunu doğrular. KDV kurtarması için, makbuzların şirketin adında olması gerekir. Bu daha sonra, doğru satış vergisi grubu ve madde satış vergisi kodlarının uygulandığını onaylar.

Arnie kağıt makbuzları aldığında, gider raporunun durumunu **Vergiden düşmeye hazır** olarak değiştirir. Ardından iadeyi ilgili vergi yetkilisine sunabilir. Bu örnekte, Amerika Birleşik Devletleri'nde ilgili vergi yetkilisi, Gelirler Dairesidir (IRS).


[!INCLUDE[footer-include](../includes/footer-banner.md)]