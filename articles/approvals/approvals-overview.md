---
title: Onaylara genel bakış
description: Bu konuda, Project Operations'ta onaylar ile çalışma hakkında bilgiler sağlanmaktadır.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 37994422e9146765076fdbb77f5c763b4f1d0802
ms.sourcegitcommit: 2cf93d8bf0be5b61a739195a41334c34d910e9ba
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961190"
---
# <a name="approvals-overview"></a>Onaylara genel bakış

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Zaman ve Gider gönderimleri onay iş akışı aracılığıyla taşınır. Girişler onaylandıktan sonra işlemler gerçek değerler olarak kaydedilir veya süre, zamanlamada ayrılır.

## <a name="approvals-workflow"></a>Onaylar iş akışı
Zaman veya gider girişi oluşturup gönderdiğinizde bir onay girişi oluşturulur. Projeyi onaylayan veya yöneticiniz girişinizi inceler ve onaylar. Giriş bir projeyle ilgiliyse onaylandığında gerçek değerler oluşturulur. Bu, maliyetin ve faturanın izlenmesini sağlar. 

## <a name="approve-an-entry"></a>Girişi onaylama
**Onaylar** formu, farklı onay türlerini görüntüleyebilmeniz için farklı görünümler arasında geçiş yapmanızı sağlar.
  
1. **Onaylar** formuna gidin ve **Giderler**, **Zaman** veya **Geri Çağırmalar**'ı seçin.
2. Her onayı inceleyin ve onaylamak istediklerinizi seçin.
3. Seçili girişleri onaylamak için **Onayla**'yı seçin.
Sistem bu girişleri işler ve gerçek değerler ya da bir ayırma işlemi oluşturur.

## <a name="reject-an-entry"></a>Girişi reddetme
Projeyi onaylayan olarak, bir girişi düzeltmesi için kullanıcıya tekrar göndermeniz gerekebilir.
  
1. **Onaylar** formuna gidin ve reddedilecek girişi seçin. 
2. **Reddet**'i seçin.
3. İsteğe Bağlı: Girişin reddedilme nedeni hakkında kullanıcıyı bilgilendirmek için **Reddetme Yorumları** iletişim kutusuna bir yorum ekleyin.
4. **Tamam**'ı seçin. Giriş kullanıcıya geri gönderilir.
  
## <a name="recall-entries"></a>Girişleri geri çağırma
Bir noktada, gönderilen bir girişi geri çağırmanız gerekebilir. Giriş onaylanmadıysa hemen geri gönderilir. Ancak onaylanmış bir giriş önemli bir etkiye neden olabilir. Projeyi onaylayanın, Gerçek Değerler'de işlemi geri almak için geri çağırmayı onaylaması gerekir.

## <a name="specify-project-approvers"></a>Projeyi onaylayanları belirleme
Her projede birkaç proje takımı üyesi vardır. Takım üyelerinden hangilerinin aynı zamanda Projeyi onaylayanlar olacağını belirleyebilirsiniz.

1. **Projeler** formuna gidin ve listeden projeyi açın.
2. **Takım** sekmesinde, Projeyi onaylayan olacak takım üyesini belirleyin ve ardından **Düzenle**'yi seçin.
3. **Projeyi Onaylayan** alanını **Evet** olarak ayarlayın.
4. **Kaydet**'i seçin.
5. Başka Projeyi onaylayanlar eklemek için 2-4 arası adımları tekrarlayın.

## <a name="configure-the-users-manager"></a>Kullanıcının yöneticisini yapılandırma

1. **Ayarlar** > **Güvenlik** > **Kullanıcılar**'a gidin.
2. Yönetici olarak atayacağınız kullanıcıyı seçin ve **Kuruluş Bilgileri** alanında, listeden yöneticiyi seçin. 
3. **Kaydet**'i seçin.


