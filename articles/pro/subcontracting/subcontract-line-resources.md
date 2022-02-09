---
title: Alt sözleşme satırı kaynakları
description: Bu konu, satıcı tarafından belirli bir alt sözleşme satırı için sağlanan ayrılmış kaynakların nasıl belirleneceğini açıklar.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4a929b985a51ab49d3e34ce4a5c277af4c05c216
ms.sourcegitcommit: d507a75a19c992a9421e4f3605162a2faa84a445
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2021
ms.locfileid: "7558481"
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
4. **Yeni Alt Sözleşme Satırı Kaynağı** sayfasında, gerekli bilgileri girin ve ardından **Kaydet ve Kapat**'ı seçin.

Aşağıdaki tabloda, alt sözleşme satırı kaynağındaki alanlar açıklanmaktadır.

| Alan | Açıklama | İşlevsel etki |
| ----- | ----------- | ----------------- |
| Ayrılabilir Kaynak | Alt sözleşme satırında kaynak olarak kullanmak istediğiniz **Sözleşmeli çalışan** türündeki ayrılabilir bir kaynak seçin.| Sözleşmeli çalışan için ayrılabilir kaynak oluşturmadıysanız bu alanı boş bırakın. Kaydı kaydettiğinizde, ayrılabilir bir kaynak oluşturulacaktır.  |
| Contact | Alt sözleşme satırı kaynağını varolan bir ilgili kişiden oluşturulabilirsiniz. Sistemdeki etkin ilgili kişilerin listesini görüntülemek için aramayı kullanın. Bu alt sözleşme satıcısına ait satıcı için bir ilgili kişi seçin. Seçtiğiniz ilgili kişi, alt sözleşmedeki satıcı için geçerli bir ilgili kişi değilse, alt sözleşme satırı kaynak kaydı kaydedilmez.| Seçilen ilgili kişi için kullanılabilir kaynak yoksa, alt sözleşme satırı kaynağını oluşturmadan önce sistem seçili kişi için bir ayrılabilir kaynak oluşturur. |
| Kullanıcı | Etkin bir kullanıcı seçerek bir alt sözleşme satırı kaynağı oluşturabilirsiniz. Sistemdeki etkin kullanıcıların listesini görüntülemek için aramayı kullanın.| Seçilen kullanıcı için kullanılabilir kaynak yoksa, alt sözleşme satırı kaynağını oluşturmadan önce sistem seçili kullanıcı için bir ayrılabilir kaynak oluşturur. |
| Başlangıç Tarihi | Alt sözleşme çalışan atamasının başlayacağı tarih.| Bu kaynak bu tarih aralığından önceki bir dönem için ayrılmışsa bir uyarı görüntülenir. |
| Bitiş Tarihi | Alt sözleşme çalışan atamasının sona ereceği tarih.| Bu kaynak bu tarih aralığından sonraki bir dönem için ayrılmışsa bir uyarı görüntülenir. |
| Çalışma | Bu alt sözleşme satırında sözleşmeli çalışan tarafından harcanacak toplam çalışma saati sayısı.| Bu kaynak, bu alt sözleşmede tahsis edilen çalışma dışında ayrılmışsa, bir uyarı oluşur. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]