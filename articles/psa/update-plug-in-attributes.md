---
title: Yeni fiyatlandırma boyutları dahil etmek için eklenti özniteliklerini güncelleştirme
description: Bu konu, fiyatlandırma boyutları için eklenti özniteliklerini güncelleştirme hakkında bilgi sağlar.
author: Rumant
manager: kfend
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.service: project-operations
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 603b0e9a10dc2fe23c9fa0fa7065bc3f500dc540
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147092"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a>Yeni fiyatlandırma boyutları dahil etmek için eklenti özniteliklerini güncelleştirme

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> Project Service Automation (PSA) Teklif Verme ve Sözleşme özelliklerini kullanmıyorsanız bu konuyu atlayabilirsiniz.

Bu konu [Özel alanlar ve varlıklar oluşturma](create-custom-fields-entities.md), [Fiyat ayarına ve işlem varlıklarına özel alan ekleme](field-references.md) ve [Özel alanları fiyatlandırma boyutları olarak ayarlama](set-up-pricing-dimensions.md) konu başlıklarındaki yordamları tamamladığınızı varsayar. Bu yordamları tamamlamadıysanız geri dönüp tamamlayın ve ardından bu konuya geri dönün.

Proje teklif satırı için **Teklif Satırı** sayfasında bir teklif satırı ayrıntısı oluşturulduğunda, sistem arka planda iki tahmin satırı oluşturur: tahminin maliyet tarafı için bir satır ve satış tarafı için bir satır. Bu, proje sözleşme satırları için de aynıdır.

Maliyet tarafındaki miktar veya alanda bir değişiklik yaptığınızda, bu değişiklik satış tarafına doldurulur. Bu, fiyatlandırma boyutlarında bir değişiklik yapıldıktan sonra yeniden kaydedilmesi gereken aşağıdaki eklentiler sayesinde mümkündür.

- PreOperationContractLineDetailUpdate - Güncelleştirmeler **msdyn_orderlinetransaction**.
- PreOperationQuoteLineDetailUpdate; Güncelleştirmeler **msdyn_quotelinetransaction**.

Aşağıdaki adımlar, eklentileri kaydetme işleminde size yardımcı olur.

1. **PluginRegistrationTool**'u açın ve çevrimiçi kurulumunuza bağlanın.
2. **Ara**'ya tıklayın ve güncelleştirilecek eklentiyi arayın.

 ![Arama ağacının ekran görüntüsü](media/PRT-1.png)

3. Bulunan eklentiyi seçin ve ardından **Ana Formda Seç**'e tıklayın.

4. Güncelleştirilecek eklentinin adımını seçin, sağ tıklayın ve ardından **Güncelleştir**'i seçin.

 ![Güncelleştirilecek eklentinin ekran görüntüsü](media/PRT-2.png)
 
5. Güncelleştirme penceresinde, filtreleme özniteliklerindeki üç noktaya (**...**) tıklayın.

 ![Var olan adım yapılandırma bilgilerini güncelleştirmenin ekran görüntüsü](media/PRT-3.png)
 
6. Fiyatlandırma özniteliği onay kutularını seçin.

 ![Fiyatlandırma öznitelikleri için onay kutusu seçimini gösteren ekran görüntüsü](media/PRT-4.png)

7. Sayfayı kapatmak için **Tamam**'a tıklayın ve ardından **Güncelleştirme Adımı**'nı seçin.

 !["Güncelleştirme Adımı" düğmesinin gösterildiği ekran görüntüsü](media/PRT-5.png)
 
8. İkinci eklenti için bu işlemi tekrarlayın: **PreOperationQuoteLineDetail; msdyn_quotelinetransaction Güncelleştirmesi**.

9. Eklenti kaydı aracını kapatın.



[!INCLUDE[footer-include](../includes/footer-banner.md)]