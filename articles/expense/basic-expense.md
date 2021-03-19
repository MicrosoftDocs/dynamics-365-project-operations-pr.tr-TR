---
title: Gider girişi (Lite)
description: Bu konuda, bir Lite dağıtımında gider girişiyle nasıl çalışılacağı hakkında bilgiler sağlanmaktadır.
author: stsporen
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 539d0ba6be6f49a6f0509595a0776ef67135496d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276777"
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