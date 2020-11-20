---
title: Fiyatlandırma boyutlarına genel bakış
description: Bu konu, Dynamics 365 Project Operations içindeki fiyatlandırma boyutları hakkında bilgi sağlar.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: ec2e350e0e4c28ea1c9540d70c83fdf0a75dc408
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128487"
---
# <a name="pricing-dimensions-overview"></a>Fiyatlandırma boyutlarına genel bakış

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

İnsan kaynaklarında fiyatlandırma ve maliyetlerin ayarlanması için kullanılan boyutlar iki kategoriye ayrılır:

- Kişiler
- Planlanan iş

Bu nedenle, iki tür fiyatlandırma boyutu değeri vardır:

- **Seçenek kümeleri**: Bir değerler kümesi için sabit numaralandırmalar olan boyutlar.
- **Varlık tabanlı değerler**: Değişken değer kümesi olabilecek boyutlar.

## <a name="pricing-dimensions"></a>Fiyatlandırma boyutları

Dynamics 365 Project Operations varsayılan bir fiyatlandırma boyutları kümesiyle sevk eder. Fiyatlandırma boyutlarını **Project Operations** > **Parametreler**'e giderek görüntüleyebilirsiniz. Parametre kaydında, **Tutar tabanlı fiyatlandırma boyutları** sekmesinde, rolün (**msdyn_resourcecategory**) ve kaynak kuruluş biriminin (**msdyn_organizationalunit**) **Satış için geçerli** ve **Maliyet için geçerli** alanlarının **Evet** olarak ayarlanmış olduğunu doğrulayın. Bu alanlar etkinleştirildiğinde her rol ve kuruluş birimi birleşimi için fiyatı ve maliyeti ayarlayabilirsiniz.

Kaynaklarınız için ek öznitelikleri kullanarak fiyat veya maliyet almanız gerekiyorsa, özelleştirilmiş alanlar, varlıklar ve boyutlar oluşturabilirsiniz.

## <a name="pricing-human-resource-time"></a>İnsan kaynağı zamanını fiyatlandırma
Bir kuruluşun insan kaynağı zamanını nasıl fiyatlandırdığı genellikle kuruluşun karlılığını doğrudan etkileyen önemli bir stratejik husustur. Kuruluşunuz, insan kaynağı süresi için fatura ve maliyet oranlarını nasıl ayarlamak istediğini belirlediğinde, finans takımları ve uygulama liderleriyle birlikte çalışın.

Fiyatlandırma için dikkate alınan diğer hususlar, geçerli fiyatlandırma boyutları olmayan ancak kuruluşunuz için bir fiyatlandırma boyutu olarak uygulanan alanları veya varlıkları yeniden kullanmayı içerir. **İşlem Kategorisi** (**msdyn_transactioncategory**) ve **Ayrılabilir Kaynak** (**bookableresource**) gibi alanlar aday boyutlara örnektir. 

Fiyatlandırma boyutunuzun bir tablo mu yoksa seçenek kümesi mi olacağını da unutmayın. Bir boyutun değerlerinde 10 veya 12'yi aşacak değişiklikler öngörüyorsanız ve bu değerler üzerinde ek özniteliklere gereksinim varsa, seçenek kümesi yerine bir varlık oluşturabilirsiniz. Bir seçenek kümesini yönetmek için (değer ekleme veya kaldırma gibi) bir yönetici veya geliştirici gerekir ancak tabloya yeni satırlar eklemek çoğu kullanıcı tarafından yapılabilir.

Aşağıdaki örnekte, kaynağın ait olduğu rol ve kaynak kuruluş birimine dayalı olarak ayarlanan fatura oranları gösterilir. Maliyet oranları genellikle çalışanın maaş bandına ve ait olduğu kuruluş birimine göre yapılır. Bu örnekte, fatura oranı ve maliyet oranı tabloları aşağıdaki gibi olacaktır.

**Örnek fatura oranları**

| Rol        | Kuruluş Birimi    |Birim      |Fiyat      |Para Birimi  |
| ------------|-------------|----------|----------:|----------|
| Geliştirici   | Contoso ABD  |Hour | 200|USD     |
| Geliştirici   | Contoso Hindistan |Hour|   112|USD     |


**Örnek maliyet oranları**

| Maaş bandı     | Kuruluş Birimi    |Birim      |Fiyat      |Para Birimi  |
| ----------------|-------------|----------|----------:|----------|
| My company_Band1 | Contoso ABD  |Hour | 145|USD     |
| My company_Band2 | Contoso Hindistan |Hour|   67|USD     |
