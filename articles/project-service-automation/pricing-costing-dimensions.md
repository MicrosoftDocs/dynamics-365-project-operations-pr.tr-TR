---
title: Fiyatlandırma ve maliyetlendirme boyutları giriş sayfası
description: Bu konu fiyatlandırma boyutlarına genel bir bakış sağlar.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 425d7bb8-9015-4f67-b9c9-cf3602e9afe8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 2379d0d2e038f28a1a8df87a851e9bf7db7fe33f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756617"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>Fiyatlandırma ve maliyetlendirme boyutları giriş sayfası

İnsan kaynaklarında fiyatlandırma ve maliyetlerin ayarlanması için kullanılan boyutlar iki kategoriye ayrılır:

- Kişiler
- Planlanan iş

Bu nedenle, Project Service Automation'da (PSA) iki tür fiyatlandırma boyutu değeri vardır: 

- **Seçenek kümeleri** - Bir değerler kümesi için sabit numaralandırmalar olan boyutlar.
- **Varlık tabanlı değerler** - Değişken değer kümesi olabilecek boyutlar.

## <a name="pricing-dimensions"></a>Fiyatlandırma boyutları

PSA varsayılan fiyatlandırma boyutları kümesiyle gelir. Bunları, **Project Service** > **Parametreler**'e giderek görüntüleyebilirsiniz. Parametre kaydında, **Tutar tabanlı fiyatlandırma boyutları** sekmesinde, rolün (**msdyn_resourcecategory**) ve kaynak kuruluş biriminin (**msdyn_organizationalunit**) **Satış için geçerli** ve **Maliyet için geçerli** alanlarının **Evet** olarak ayarlanmış olduğunu doğrulayın. Bu, her rol ve kuruluş birimi birleşimi için fiyatı ve maliyeti ayarlamanıza olanak sağlar.

!["Satış için geçerli" seçeneğinin vurgulandığı Project Service parametreleri ekran görüntüsü](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> PSA sürüm 3'ten önce fiyatlandırma boyutları olarak rol ve kuruluş biriminin kullanıma hazır alanlarını kullanıyorduysanız belirgin bir değişiklik olmayacaktır. Project Service'ı her zamanki gibi kullanmaya devam edebilirsiniz. 

Kaynaklarınız için ek öznitelikleri kullanarak fiyat veya maliyet almanız gerekiyorsa, özelleştirilmiş alanlar, varlıklar ve boyutlar oluşturabilirsiniz. Daha fazla bilgi için aşağıdaki konulara bakın ancak yordamları aşağıda listelendikleri sırada tamamlamanız gerektiğini unutmayın:

- [Özel alanlar ve varlıklar oluşturma](create-custom-fields-entities.md)
- [Fiyat ayarına ve işlem varlıklarına özel alan ekleme](field-references.md)
- [Özel alanları fiyatlandırma boyutları olarak ayarlama](set-up-pricing-dimensions.md)
- [Yeni fiyatlandırma boyutları dahil etmek için eklenti özniteliklerini güncelleştirme](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a>İnsan kaynağı zamanını fiyatlandırma
Bir kuruluşun insan kaynağı zamanını nasıl fiyatlandırdığı genellikle kuruluşun karlılığını doğrudan etkileyen önemli bir stratejik husustur. Kuruluşunuz, insan kaynağı süresi için fatura ve maliyet oranlarını nasıl ayarlamak istediğini belirlediğinde, finans takımları ve uygulama liderleriyle birlikte çalışın.

Fiyatlandırma için dikkate alınan diğer hususlar, geçerli fiyatlandırma boyutları olmayan ancak kuruluşunuz için bir fiyatlandırma boyutu olarak uygulanan alanları veya varlıkları yeniden kullanmayı içerir. **İşlem Kategorisi** (**msdyn_transactioncategory**) ve **Ayrılabilir Kaynak** (**bookableresource**) gibi alanlar aday boyutlara örnektir. 

Fiyatlandırma boyutunuzun bir tablo mu yoksa seçenek kümesi mi olacağını da dikkate almanız gerekir. Bir boyutun değerlerinde 10 veya 12'yi aşacak değişiklikler öngörüyorsanız ve bu değerler üzerinde ek özniteliklere gereksinim varsa, seçenek kümesi yerine bir varlık oluşturabilirsiniz. Bir seçenek kümesini yönetmek için (değer ekleme veya kaldırma gibi) bir yönetici veya geliştirici gerekir ancak tabloya yeni satırlar eklemek çoğu kullanıcı tarafından yapılabilir.

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
