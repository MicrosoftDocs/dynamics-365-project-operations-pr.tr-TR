---
title: Fiyatlandırma ve maliyetlendirme boyutları giriş sayfası
description: Bu konu fiyatlandırma boyutlarına genel bir bakış sağlar.
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 7dbee508cea074a8c443506d280a1b52eb698202
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593636"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>Fiyatlandırma ve maliyetlendirme boyutları giriş sayfası

[!include [banner](../includes/psa-now-project-operations.md)]

Proje tabanlı kuruluşlarda işçi ücretlerini ve maliyetleri ayarlamak için kullanılan boyutlar aşağıdaki özniteliklerden etkilenir:

- Deneyimlerine, rollerine veya coğrafi konumlarına benzer şekilde iş yapan insanlar
- Karmaşıklığına veya gün içindeki saatine benzer şekilde gerçekleştirilecek işler

İşin ve işi gerçekleştirmesi gereken kişilerin bu özniteliklerinin genel yapısına bakıldığında Project Service Automation'da iki tür fiyatlandırma boyut değeri vardır: 

- **Seçenek kümeleri**: Bir değerler kümesi için sabit numaralandırmalar olan öznitelikler.
- **Varlık tabanlı değerler**: Sınırlı olan ancak zaman içinde değişebilen değişken değer kümesi olabilecek öznitelikler.

## <a name="pricing-dimensions"></a>Fiyatlandırma boyutları

PSA varsayılan fiyatlandırma boyutları kümesiyle gelir. Bunları, **Project Service** > **Parametreler**'e giderek görüntüleyebilirsiniz. Parametre kaydında, **Tutar tabanlı fiyatlandırma boyutları** sekmesinde, rolün (**msdyn_resourcecategory**) ve kaynak kuruluş biriminin (**msdyn_organizationalunit**) **Satış için geçerli** ve **Maliyet için geçerli** alanlarının **Evet** olarak ayarlanmış olduğunu doğrulayın. Bu, her rol ve kuruluş birimi birleşimi için fiyatı ve maliyeti ayarlamanıza olanak sağlar.

!["Satış için geçerli" seçeneğinin vurgulandığı Project Service parametreleri ekran görüntüsü.](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> PSA sürüm 3'ten önce fiyatlandırma boyutları olarak rol ve kuruluş biriminin kullanıma hazır alanlarını kullanıyorduysanız belirgin bir değişiklik olmayacaktır. Project Service'ı her zamanki gibi kullanmaya devam edebilirsiniz. 

Kaynaklarınız için ek öznitelikleri kullanarak fiyat veya maliyet almanız gerekiyorsa, özelleştirilmiş alanlar, varlıklar ve boyutlar oluşturabilirsiniz. Daha fazla bilgi için aşağıdaki konulara bakın ancak yordamları aşağıda listelendikleri sırada tamamlamanız gerektiğini unutmayın:

- [Özel alanlar ve varlıklar oluşturma](create-custom-fields-entities.md)
- [Fiyat ayarına ve işlem varlıklarına özel alan ekleme](field-references.md)
- [Özel alanları fiyatlandırma boyutları olarak ayarlama ](set-up-pricing-dimensions.md)
- [Yeni fiyatlandırma boyutları dahil etmek için eklenti özniteliklerini güncelleştirme](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a>İnsan kaynağı zamanını fiyatlandırma
Bir kuruluşun insan kaynağı zamanını nasıl fiyatlandırdığı genellikle kuruluşun karlılığını doğrudan etkileyen önemli bir stratejik husustur. Kuruluşunuz, insan kaynağı süresi için fatura ve maliyet oranlarını nasıl ayarlamak istediğini belirlediğinde, finans takımları ve uygulama liderleriyle birlikte çalışın.

Fiyatlandırma için dikkate alınan diğer hususlar, geçerli fiyatlandırma boyutları olmayan ancak kuruluşunuz için bir fiyatlandırma boyutu olarak uygulanan alanları veya varlıkları yeniden kullanmayı içerir. **İşlem Kategorisi** (**msdyn_transactioncategory**) ve **Ayrılabilir Kaynak** (**bookableresource**) gibi alanlar aday boyutlara örnektir. 

Fiyatlandırma boyutunuzun bir tablo mu yoksa seçenek kümesi mi olacağını da unutmayın. Bir boyutun değerlerinde 10 veya 12'den fazla değişiklik öngörüyorsanız ve bu değerler üzerinde ek özniteliklere gereksinim varsa seçenek kümesi yerine bir varlık oluşturun. Bir seçenek kümesini yönetmek için (değer ekleme veya kaldırma gibi) bir yönetici veya geliştirici gerekir ancak tabloya yeni satırlar eklemek çoğu iş kullanıcısı tarafından yapılabilir.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
