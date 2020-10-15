---
title: Gider yönetiminde KDV'den düşme
description: Bu konuda, uygun katma değer vergisi (KDV) işlemlerinde para iadelerini almayı açıklar.
author: suvaidya
manager: AnnBe
ms.date: 10/10/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 2c20e4a7fa9748e03bf1729fc2f7bdbfc2f292d1
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908694"
---
# <a name="vat-recovery-in-expense-management"></a>Gider yönetiminde KDV'den düşme

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Uygun katma değer vergisi (KDV) işlemlerinde para iadelerini almak için bir şirket veya kuruluşun doğru bilgileri tanımlaması, toplaması, doğrulaması ve göndermesi gerekir. Bu süreç birden fazla görev içerir ve şirketinizin büyüklüğüne bağlı olarak birkaç çalışanı veya rolü içerebilir.

**Gider yönetimi** modülünde, KDV'yi düşmek için aşağıdaki önkoşulların tamamlanması gerekir:

- Gider kategorilerine tahsis edilen ülkeler/bölgeler için vergi kodları oluşturulmalıdır.
- Her vergi kodu için bir satış vergisi grubu oluşturulmalıdır.
- Her satış vergisi grubu için bir öğe satış vergisi kodu oluşturulmalıdır.

Önkoşullar tamamlandıktan sonra KDV işlemleriyle ilgili para iadelerini istemek için aşağıdaki adımların tamamlanması gerekir.

1. Gider raporunda, uygun KDV para iadelerini belirlemek için kredi kartı işlemleriyle ilgili vergi bilgilerini girin.
2. Tüm vergi bilgilerinin eksiksiz olduğunu doğrulayın ve ardından gider raporunu gönderin.
3. Uluslararası KDV'den düşme işlemi için uygun olan giderleri işleyin.
4. Uluslararası vergiden düşme para iadelerini dosyalamak için KDV'den düşme verilerini üçüncü taraf satıcıya gönderin.
5. Yurtiçi KDV'den düşme için giderleri işleyin.

Aşağıdaki bölümlerde, Contoso çalışanlarının her adımı nasıl tamamladığını gösteren örnekler sağlanmaktadır.

## <a name="enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>Uygun KDV para iadelerini belirlemek için kredi kartı işlemleriyle ilgili vergi bilgilerini girin

Amerika Birleşik Devletleri'nde bir Contoso satış temsilcisi olan Nancy, kısa süre önce Birleşik Krallık'a yaptığı bir satış seyahatinden dönmüştür. Nancy seyahati sırasında yemek için bazı kişisel kredi kartı harcamaları yapar. Nancy şimdi giderleri mutabık kılmak için bir gider raporu oluşturmalıdır.

Nancy bilgileri gider raporuna girdiğinde **Gider raporu düzenleme** sayfasında **Ülke/bölge** alanında **Birleşik Krallık**'ı seçer. Satış vergisi grupları listesi, yalnızca Birleşik Krallık için geçerli olan grupları gösterecek şekilde filtrelenir. Nancy **Birleşik Krallık 001** satış vergisi grubunu seçer ve ardından satış vergisi grubu için **Yemek**'i seçer. Bundan sonra Nancy konaklama için yeni bir işlem ekler. Birleşik Krallık'ta konaklama için yalnızca bir satış vergisi grubu ve bir öğe satış vergisi grubu olduğundan, bu bilgiler Nancy'nin gider raporunda otomatik olarak doldurulur.

Contoso ilkesine göre, tüm giderlerde eşleşen bir makbuz olmalıdır. Bu nedenle, Nancy gider raporunu kaydettiğinde gider raporunda listelediği her işlem için bir makbuz eklemesi gerektiğini belirten bir ileti alır. Nancy, gider raporuna her işlem makbuzunun dijital bir görüntüsünü eklediğini doğrular ve ardından raporunu onay için gönderir. Daha sonra kağıt makbuzları arka ofis işleme takımına gönderir. Bu takım, KDV'den düşme verilerini Contoso için uluslararası KDV'den düşme iadelerini dosyalayan üçüncü taraf satıcıya gönderir.

## <a name="verify-tax-information-and-post-an-expense-report"></a>Vergi bilgilerini doğrulama ve gider raporu gönderme

Contoso'nun Borç hesabı koordinatörü April, bir gider raporu göndermeden önce eksik olan tüm vergi bilgilerini girmelidir. **Gider raporu ayrıntıları** sayfasını açar ve Nancy'nin onaylanmış gider raporunu görür. Ardından April, işlemlerin ayrıntılarını görüntülemek için gider raporunu açar. Nancy'nin işlemlerden biri için bir öğe satış vergisi grubunu girmediğini görür. Bu bilgiler sağlanmadığından April, gider raporunu gönderemez. Bu nedenle, Gider yönetiminde **Vergi yapılandırmaları** sayfasına bakar ve ülke/bölge ve işlem türü için uygun öğe satış vergisi grubunu bulur. April artık gider raporunu genel muhasebeye gönderebilir.

April, gider raporunu gönderdiğinde bir KDV'den düşülebilir iş öğesi oluşturulur. Bu iş öğesi, arka ofis işleme takımının bir üyesine atanır. April, gönderme işleminin başarılı olduğunu onaylayan bir ileti alır. Bu ileti, vergiden düşme için belirlenen KDV işlemlerinin sayısını da listeler.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Uluslararası KDV'den düşme işlemi için uygun olan giderleri işleme

Contoso'nun arka ofis işleme takımının bir üyesi olan Arnie, KDV'den düşme için gereken tüm bilgilerin gider raporlarına dahil edildiğini doğrulamaktan sorumludur. **Gider vergisinden düşme** sayfasını açar ve Nancy'nin gönderdiği gider raporunu seçer. Arnie ardından gereken tüm makbuzların eklendiğini ve doğru satış vergisi grubu ve öğe satış vergisi kodlarının girildiğini doğrular.

Arnie, kağıt makbuzları Nancy'den aldığında bunları dijital makbuzlara göre doğrular ve ardından gider raporunun durumunu **Vergiden düşmeye hazır** olarak değiştirir.

## <a name="send-vat-recovery-data-to-the-third-party-vendor"></a>Üçüncü taraf satıcıya KDV'den düşme verilerini gönderme

Arnie, gider raporu verilerini KDV'den düşme iadelerini dosyalayacak üçüncü taraf satıcıya göndermeye hazır olduğunda, **Gider vergisinden düşme** sayfasını açar. Sayfayı yalnızca **Vergiden düşmeye hazır** olarak işaretlenmiş gider raporlarını gösterecek şekilde filtreler. Arnie ardından **Dosya** &gt; **Excel'e Aktar**'ı seçer. Gider raporlarından alınan KDV bilgileri, Microsoft Excel çalışma sayfasına dışarı aktarılır. Arnie bu çalışma sayfasını üçüncü taraf satıcıya gönderir ve kağıt makbuzların kurye ile gönderildiğini belirten bir ileti ekler.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Yurtiçi KDV'den düşme için giderleri işleme

Arnie, gider raporu işlemlerinin KDV'den düşme için uygun olduğunu ve dijital makbuzların raporlara eklendiğini doğrulamalıdır. Yurtiçi vergiden düşmeye uygun giderleri işlemeye başlamak için Arnie, **Gider vergisinden düşme** sayfasını açar ve doğrulama gerektiren gider raporunu seçer. Makbuzların çalışan yerine şirket adına olduğunu doğrular. (KDV'den düşme için makbuzların şirket adına olması gerekir.) Arnie ardından doğru satış vergisi grubu ve öğe satış vergisi kodlarının girildiğini doğrular.

Arnie kağıt makbuzları aldığında, gider raporunun durumunu **Vergiden düşmeye hazır** olarak değiştirir. Ardından iadeyi ilgili vergi yetkilisine sunabilir. Bu örnekte, Amerika Birleşik Devletleri'nde ilgili vergi yetkilisi, Gelirler Dairesidir (IRS).
