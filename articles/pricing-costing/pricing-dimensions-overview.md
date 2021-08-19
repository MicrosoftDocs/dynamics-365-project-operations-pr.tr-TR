---
title: Fiyatlandırma boyutlarına genel bakış
description: Bu konu, Dynamics 365 Project Operations'ta fiyatlandırma boyutları hakkında bilgi sağlar.
author: rumant
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 4b3b71c0b64a24f6914c70c4383eee654e7d4947ececaf9b4e6394f45a081a4c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001995"
---
# <a name="pricing-dimensions-overview"></a>Fiyatlandırma boyutlarına genel bakış

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

İnsan kaynaklarında fiyatlandırma ve maliyetlerin ayarlanması için kullanılan boyutlar iki kategoriye ayrılır:

- Kişiler
- Planlanan iş

Bu nedenle, iki tür fiyatlandırma boyutu değeri vardır:

- **Seçenek kümeleri**: Bir değerler kümesi için sabit numaralandırmalar olan boyutlar.
- **Varlık tabanlı değerler**: Değişken değer kümesi olabilecek boyutlar.

## <a name="pricing-dimensions"></a>Fiyatlandırma boyutları

Dynamics 365 Project Operations, varsayılan fiyatlandırma boyutları kümesiyle gelir. Fiyatlandırma boyutlarını **Project Operations** > **Parametreler**'e giderek görüntüleyebilirsiniz. Parametre kaydında, **Tutar tabanlı fiyatlandırma boyutları** sekmesinde, rolün (**msdyn_resourcecategory**) ve kaynak kuruluş biriminin (**msdyn_organizationalunit**) **Satış için geçerli** ve **Maliyet için geçerli** alanlarının **Evet** olarak ayarlanmış olduğunu doğrulayın. Bu alanlar etkinleştirildiğinde her rol ve kuruluş birimi birleşimi için fiyatı ve maliyeti ayarlayabilirsiniz.

!["Satış için geçerli" seçeneğinin vurgulandığı Project Service parametreleri ekran görüntüsü.](media/PS-OOB-parameters.png)

Kaynaklarınız için ek öznitelikleri kullanarak fiyat veya maliyet almanız gerekiyorsa, özelleştirilmiş alanlar, varlıklar ve boyutlar oluşturabilirsiniz. Daha fazla bilgi için aşağıdaki konulara bakın. 
  
  > [!NOTE]
  > Yordamların listelendikleri sırayla tamamlanması gerekir.

1. [Özel fiyatlandırma boyutları için çözüm oluşturma](../sales/create-solution-custompd.md)
2. [Özel alanlar ve varlıklar oluşturma](create-custom-fields-entities-pricing-dimensions.md)
3. [Fiyat ayarı ve geçiş varlıklarına özel alanlar ekleme ](add-custom-fields-price-setup-transactional-entities.md)
4. [Özel alanları fiyatlandırma boyutları olarak ayarlama ](set-up-custom-fields-pricing-dimensions.md)
5. [Yeni fiyatlandırma boyutları dahil etmek için eklenti özniteliklerini güncelleştirme](update-plugin-attributes-pd.md)


## <a name="pricing-human-resource-time"></a>İnsan kaynağı zamanını fiyatlandırma
Bir kuruluşun insan kaynağı zamanını nasıl fiyatlandırdığı genellikle kuruluşun karlılığını doğrudan etkileyen önemli bir stratejik husustur. Kuruluşunuz, insan kaynağı süresi için fatura ve maliyet oranlarını nasıl ayarlamak istediğini belirlediğinde, finans takımları ve uygulama liderleriyle birlikte çalışın.

Fiyatlandırma için dikkate alınan diğer hususlar, geçerli fiyatlandırma boyutları olmayan ancak kuruluşunuz için bir fiyatlandırma boyutu olarak uygulanan alanları veya varlıkları yeniden kullanmayı içerir. **İşlem Kategorisi** (**msdyn_transactioncategory**) ve **Ayrılabilir Kaynak** (**bookableresource**) gibi alanlar aday boyutlara örnektir. 

Fiyatlandırma boyutunuzun bir tablo mu yoksa seçenek kümesi mi olacağını da unutmayın. Bir boyutun değerlerinde 10 veya 12'yi aşacak değişiklikler öngörüyorsanız ve bu değerler üzerinde ek özniteliklere gereksinim varsa, seçenek kümesi yerine bir varlık oluşturabilirsiniz. Bir seçenek kümesini yönetmek için (değer ekleme veya kaldırma gibi) bir yönetici veya geliştirici gerekir ancak tabloya yeni satırlar eklemek çoğu kullanıcı tarafından yapılabilir.

Aşağıdaki örnekte, kaynağın ait olduğu rol ve kaynak kuruluş birimine dayalı olarak ayarlanan fatura oranları gösterilir. Maliyet oranları genellikle çalışanın maaş bandına ve ait olduğu kuruluş birimine göre yapılır. Bu örnekte, fatura oranı ve maliyet oranı tabloları aşağıdaki gibi olacaktır.

**Örnek fatura oranları**

| Rol        | Kuruluş Birimi    |Birim      |Fiyat      |Para birimi  |
| ------------|-------------|----------|----------:|----------|
| Geliştirici   | Contoso ABD  |Saat | 200|USD     |
| Geliştirici   | Contoso Hindistan |Saat|   112|USD     |


**Örnek maliyet oranları**

| Maaş bandı     | Kuruluş Birimi    |Birim      |Fiyat      |Para birimi  |
| ----------------|-------------|----------|----------:|----------|
| My company_Band1 | Contoso ABD  |Saat | 145|USD     |
| My company_Band2 | Contoso Hindistan |Saat|   67|USD     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]