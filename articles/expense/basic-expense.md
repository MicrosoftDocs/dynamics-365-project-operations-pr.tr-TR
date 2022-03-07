---
title: Gider girişi (Lite)
description: Bu konuda, bir Lite dağıtımında gider girişiyle nasıl çalışılacağı hakkında bilgiler sağlanmaktadır.
author: stsporen
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 48bf86a5cee475708f93462dc154e21b36240023f0a94cf31c49e9a096951736
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007845"
---
# <a name="expense-entry-lite"></a>Gider girişi (Lite)

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Temel veya Lite, gider yönetimi basit giderleri kaydetme özelliğidir. Bir projenin giderlerini kaydettiğinizde, proje onaylayanı bu giderleri inceleyip onaylar.

Dynamics 365 Project Operations'ta gider özellikleri hakkında daha fazla bilgi için bkz. [Gidere genel bakış](expense-overview.md).

## <a name="capture-a-basic-expense"></a>Temel gider yakalama

Giderlerinizi, onaylayana gönderebilmek için yakalayabilirsiniz.

1. **Giderler**'e gidin ve **Yeni**'yi seçin.
2. **Yeni Gider** sayfasında, gerekli gider bilgilerini girin ve ardından **Kaydet**'i seçin.

## <a name="submit-a-basic-expense"></a>Temel gider gönderme

Tüm giderlerinizi yakalamayı tamamladıktan ve onaylanmak üzere hazırladıktan sonra, giderleri göndermeniz gerekir.

1. **Giderler**'e gidin ve bir gider seçin. Alternatif olarak, başlıktaki onay kutusunu kullanarak tüm giderleri seçin.
2. **Gönder**'i seçin. Sistem, seçili girişleri işler ve gider onay istekleri oluşturur.

## <a name="add-an-attachment"></a>Bir ek ekle

Onaylayana, gideriniz hakkında ek belgeler sağlamanız gerekebilir. Gider girişinin zaman çizelgesinde bir makbuz ekleyebilirsiniz. **Zaman Çizelgesi** bölümünde **Düzenle** seçeneğini belirleyin ve makbuzunuzu eklemek için ataş simgesini seçin.

## <a name="recall-a-basic-expense"></a>Temel gideri geri çekme

Bir gideri yanlışlıkla gönderdiğinizde, bunu geri çekebilirsiniz. Gider girişini geri çekmek için gereken süre, onay aşamasına bağlıdır.  Onaylayan kişi girişi henüz onaylamadıysa, geri çekme hemen gerçekleşebilir. Ancak, giriş zaten onaylanmışsa onaylayandan geri çekmeyi onaylaması ve işlemleri geri alması istenir.

1. **Giderler**'e gidin ve ardından gider listesinde, geri çekilecek gideri seçin.
2. **Geri çek**'i seçin. Gider girişi henüz onaylanmadıysa sistem bunu hemen geri çeker. Gider girişi zaten onaylanmışsa onaylayanı, gideri geri almak istediğinizi onaylayan kişiye bildirmek için bir geri çekme isteği oluşturulur. Bundan sonra, onaylayan geri alma işleminin yapılabileceğini onaylar ve giriş iade edilir.

## <a name="delete-a-basic-expense"></a>Temel gideri silme

Henüz gönderilmeyen giderler silinebilir. Zaten gönderilmiş bir gideri silmek için öncelikle geri çekmeniz gerekir.

## <a name="see-also"></a>Ayrıca bkz.

- [Onaylara genel bakış](../approvals/approvals-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]