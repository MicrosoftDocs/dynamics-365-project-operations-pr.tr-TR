---
title: Gider girişi (Lite)
description: Bu konuda, bir Lite dağıtımında gider girişiyle nasıl çalışılacağı hakkında bilgiler sağlanmaktadır.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 536c961593599df8e7e2986f92259b0e690eae8b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121107"
---
# <a name="expense-entry-lite"></a>Gider girişi (Lite)

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Temel veya Lite, gider yönetimi basit giderleri kaydetme özelliğidir. Bir projenin giderlerini kaydettiğinizde, proje onaylayanı bu giderleri inceleyip onaylar.

Dynamics 365 Project Operations uygulamasında gider özellikleri hakkında daha fazla bilgi için bkz. [Gidere genel bakış](expense-overview.md).

## <a name="capture-a-basic-expense"></a>Temel gider yakalama

Giderlerinizi, onaylayana gönderebilmek için yakalayabilirsiniz.

1. **Giderler**'e gidin ve **Yeni**'yi seçin.
2. **Yeni Gider** sayfasında, gerekli gider bilgilerini girin ve ardından **Kaydet**'i seçin.

## <a name="submit-a-basic-expense"></a>Temel gider gönderme

Tüm giderlerinizi yakalamayı tamamladıktan ve onaylanmak üzere hazırladıktan sonra, giderleri göndermeniz gerekir.

1. **Giderler**'e gidin ve bir gider seçin. Alternatif olarak, başlıktaki onay kutusunu kullanarak tüm giderleri seçin.
2. **Gönder**'i seçin. Sistem, seçili girişleri işler ve gider onay istekleri oluşturur.

## <a name="recall-a-basic-expense"></a>Temel gideri geri çekme

Bir gideri yanlışlıkla gönderdiğinizde, bunu geri çekebilirsiniz. Gider girişini geri çekmek için gereken süre, onay aşamasına bağlıdır.  Onaylayan kişi girişi henüz onaylamadıysa, geri çekme hemen gerçekleşebilir. Ancak, giriş zaten onaylanmışsa onaylayandan geri çekmeyi onaylaması ve işlemleri geri alması istenir.

1. **Giderler**'e gidin ve ardından gider listesinde, geri çekilecek gideri seçin.
2. **Geri çek**'i seçin. Gider girişi henüz onaylanmadıysa sistem bunu hemen geri çeker. Gider girişi zaten onaylanmışsa onaylayanı, gideri geri almak istediğinizi onaylayan kişiye bildirmek için bir geri çekme isteği oluşturulur. Bundan sonra, onaylayan geri alma işleminin yapılabileceğini onaylar ve giriş iade edilir.

## <a name="delete-a-basic-expense"></a>Temel gideri silme

Henüz gönderilmeyen giderler silinebilir. Zaten gönderilmiş bir gideri silmek için öncelikle geri çekmeniz gerekir.

## <a name="see-also"></a>Ayrıca bkz.

- [Onaylara genel bakış](../approvals/approvals-overview.md)
