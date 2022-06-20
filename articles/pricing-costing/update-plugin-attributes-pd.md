---
title: Eklenti özniteliklerini yeni fiyatlandırma boyutlarıyla güncelleştirme
description: Bu makale, fiyatlandırma boyutları için eklenti özniteliklerini güncelleştirme hakkında bilgi sağlar.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2ae502fea533d9f199ef5ee1cc85b623f08cbd84
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920038"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a>Eklenti özniteliklerini yeni fiyatlandırma boyutlarıyla güncelleştirme

Bu makale, fiyatlandırma boyutları için eklenti özniteliklerini güncelleştirme hakkında bilgi sağlar.

> [!NOTE]
> Bu makale yalnızca Dynamics 365 Project Operations uygulamasındaki teklif ve sözleşme özelliklerine uygulanabilir.

## <a name="prerequisites"></a>Önkoşullar
Bu makaledeki adımları tamamlamadan önce, aşağıdaki makalelerde bulunan yordamları tamamlamış olmalısınız:

  - [Özel alanlar ve varlıklar oluşturma](create-custom-fields-entities-pricing-dimensions.md) 
  - [Fiyat ayarı ve geçiş varlıklarına özel alanlar ekleme ](add-custom-fields-price-setup-transactional-entities.md)
  - [Özel alanları fiyatlandırma boyutları olarak ayarlama](set-up-custom-fields-pricing-dimensions.md). 
  
Bu yordamları tamamlamadıysanız tamamlayın ve ardından bu makaleye geri dönün.

## <a name="register-a-plug-in"></a>Eklentiyi kaydetme
Proje teklif satırı için **Teklif Satırı** sayfasında bir teklif satırı ayrıntısı oluşturulduğunda sistem, iki tahmin satırı oluşturur. Satırlardan biri tahminin maliyet tarafı diğer satır ise satış tarafı içindir. Bu, proje sözleşme satırları için de aynıdır.

Maliyet tarafındaki miktar veya alanda bir değişiklik yaptığınızda, bu değişiklik satış tarafında da yapılır. Bu mümkündür çünkü Quotelinedetail ve contractline ayrıntı varlıkları üzerindeki PreOperation eklentileri, işlemin maliyet tarafına özgü özniteliklerini satış tarafına bağlar. Satış tarafındaki fiyatlandırma boyutu değerlerinde yapılan değişikliklerin maliyet tarafında da yapılması gerekiyorsa fiyatlandırma boyutunda değişiklik yapıldıktan sonra aşağıdaki eklentilerin yeniden kaydedilmesi gerekir.

Güncelleştirilecek ve yeniden kaydedilecek eklentiler şunlardır:

- PreOperationContractLineDetailUpdate - **msdyn_orderlinetransaction güncelleştirmesi**
- PreOperationQuoteLineDetailUpdate - **msdyn_quotelinetransaction güncelleştirmeleri**

Eklentileri güncelleştirmek ve yeniden kaydetmek için aşağıdaki adımları tamamlayın.

1. **PluginRegistrationTool**'u açın ve Project Operations Dataverse ortamınıza bağlanın.
2. **Ara**'yı seçin ve güncelleştirilecek eklentinin ilk birkaç harfini yazın.
3. Bulunan eklentiyi seçin ve ardından **Ana Formda Seç** seçeneğini belirleyin.
4. **msdyn_orderlinetransaction güncelleştirmesi** adımını seçin, sağ tıklayın ve ardından **Güncelleştir**'i seçin.
5. **Güncelleştirme** iletişim sayfasında, filtreleme özniteliklerindeki üç noktayı (**...**) seçin.
6. Filtreleme öznitelikleri penceresi açılır ve varlıktaki tüm özniteliklerin ve fiyatlandırma boyutlarının bir listesini sağlar. Fiyatlandırma boyutu öznitelikleri için onay kutularını seçin.
7. Sayfayı kapatmak için **Tamam**'ı seçin ve ardından **Güncelleştirme Adımı**'nı seçin.
8. İkinci eklenti **PreOperationQuoteLineDetail** için 2 ile 7 arasındaki adımları tekrarlayın. Bu eklenti için **msdyn_quotelinetransaction güncelleştirmesi** adımını güncelleştirmeniz gerekir.
9. **PluginRegistrationTool**'u kapatın.


[!INCLUDE[footer-include](../includes/footer-banner.md)]