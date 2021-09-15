---
title: Alt sözleşme satırı kaynakları
description: Bu konu, satıcı tarafından belirli bir alt sözleşme satırı için sağlanan ayrılmış kaynakların nasıl belirleneceğini açıklar.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 48440f82170bde7f0a0a45f8f9849d688b232949
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323395"
---
# <a name="subcontract-line-resources"></a>Alt sözleşme satırı kaynakları

[!include [banner](../../includes/dataverse-preview.md)]

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Dynamics 365 Project Operations'da satıcı, alt sözleşme satırında zaman için satın alınan kaynak kapasitesini sağlamak için kullanılacak kaynakları belirtebilir.

## <a name="create-subcontract-line-resources"></a>Alt sözleşme satırı kaynakları oluşturma

Alt sözleşme satırı kaynakları oluşturmak için aşağıdaki adımları uygulayın.

1. Gezinti bölmesinde, **Alt sözleşmeler**'i seçin ve çalışmak istediğiniz bir alt sözleşmeyi açın.
2. Satıcı kaynaklarını belirtmek istediğiniz zamana ilişkin alt sözleşme satırını açın.
3. **Alt Sözleşme Satırı Kaynakları** sekmesinde, alt ızgarada **+ Yeni Alt Sözleşme Satırı Kaynağı**'nı seçin.
4. **Yeni Alt Sözleşme Satırı Kilometre Taşı** sayfasında, gerekli bilgileri girin ve **Kaydet ve Kapat**'ı seçin.

Aşağıdaki tabloda, alt sözleşme satırı kaynağındaki alanlar açıklanmaktadır.

| Alan |  Açıklama |
| ----- | ------------ |
| Ayrılabilir Kaynak | Alt sözleşme satırında kaynak olarak kullanmak istediğiniz "Sözleşmeli çalışan" türündeki ayrılabilir bir kaynak seçin. Sözleşmeli çalışanı için henüz bir ayrılabilir kaynak oluşturmadıysanız bu alanı boş bırakın. Kaydı kaydettiğinizde ayrılabilir bir kaynak oluşturulur.  |
| Contact | **Ayrılabilir Kaynak** alanı boşsa, alt sözleşme satırı kaynağını mevcut bir ilgili kişiden oluşturabilirsiniz. Sistemdeki etkin ilgili kişilerin listesini görüntülemek için aramayı kullanın. Bu alt sözleşme satıcısına ait satıcı için bir ilgili kişi seçin. Seçtiğiniz ilgili kişi, kaydı kaydettiğinizde doğrulanır. Seçtiğiniz ilgili kişi geçerli bir ilgili kişi değilse, kaydınız kaydedilmez. Seçilen ilgili kişi için kullanılabilir kaynak yoksa, alt sözleşme satırı kaynağını oluşturmadan önce sistem seçili kişi için bir ayrılabilir kaynak oluşturur. |
| Kullanıcı | **Ayrılabilir Kaynak** alanı boşsa, etkin bir kullanıcı seçerek bir alt sözleşme satırı kaynağı oluşturabilirsiniz. Sistemdeki etkin kullanıcıların listesini görüntülemek için aramayı kullanın. Seçilen kullanıcı için kullanılabilir kaynak yoksa, alt sözleşme satırı kaynağını oluşturmadan önce sistem seçili kullanıcı için bir ayrılabilir kaynak oluşturur. |
| Başlangıç Tarihi | Alt sözleşme çalışan atamasının başlayacağı tarih. Bu kaynak bu tarih aralığından önceki bir dönem için ayrılmışsa bir uyarı görüntülenir. |
| Bitiş Tarihi | Alt sözleşme çalışan atamasının sona ereceği tarih. Bu kaynak bu tarih aralığından sonraki bir dönem için ayrılmışsa bir uyarı görüntülenir. |
| Çalışma | Alt sözleşme çalışanının bu alt sözleşme satırında harcayacağı çalışma saatlerinin toplam sayısı. Bu kaynak bu alt sözleşme için ayrılan çalışmadan fazlası için ayrılmışsa bir uyarı oluşur. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]