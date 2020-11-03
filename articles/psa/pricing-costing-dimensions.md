---
title: Fiyatlandırma ve maliyetlendirme boyutları giriş sayfası
description: Bu konu fiyatlandırma boyutlarına genel bir bakış sağlar.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 515a2e2e518614884b414ca43702e8bfea2c6919
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086365"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="64959-103">Fiyatlandırma ve maliyetlendirme boyutları giriş sayfası</span><span class="sxs-lookup"><span data-stu-id="64959-103">Pricing and costing dimensions home page</span></span>

<span data-ttu-id="64959-104">Proje tabanlı kuruluşlarda işçi ücretlerini ve maliyetleri ayarlamak için kullanılan boyutlar aşağıdaki özniteliklerden etkilenir:</span><span class="sxs-lookup"><span data-stu-id="64959-104">The dimensions used to set labor pricing and costing in project-based organizations are influenced by the following attributes:</span></span>

- <span data-ttu-id="64959-105">Deneyimlerine, rollerine veya coğrafi konumlarına benzer şekilde iş yapan insanlar</span><span class="sxs-lookup"><span data-stu-id="64959-105">People doing work similar to their experience, role, or geography</span></span>
- <span data-ttu-id="64959-106">Karmaşıklığına veya gün içindeki saatine benzer şekilde gerçekleştirilecek işler</span><span class="sxs-lookup"><span data-stu-id="64959-106">Work to be performed similar to its complexity or time of day</span></span>

<span data-ttu-id="64959-107">İşin ve işi gerçekleştirmesi gereken kişilerin bu özniteliklerinin genel yapısına bakıldığında Project Service Automation'da iki tür fiyatlandırma boyut değeri vardır:</span><span class="sxs-lookup"><span data-stu-id="64959-107">Given the typical nature of these attrubutes of the work and the people required to perform the work, there are two types of pricing dimension values available in Project Service Automation:</span></span> 

- <span data-ttu-id="64959-108">**Seçenek kümeleri** : Bir değerler kümesi için sabit numaralandırmalar olan öznitelikler.</span><span class="sxs-lookup"><span data-stu-id="64959-108">**Option sets** - Attributes that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="64959-109">**Varlık tabanlı değerler** : Sınırlı olan ancak zaman içinde değişebilen değişken değer kümesi olabilecek öznitelikler.</span><span class="sxs-lookup"><span data-stu-id="64959-109">**Entity-based values** - Attributes that can have a varied set of values that are finite but can change over time.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="64959-110">Fiyatlandırma boyutları</span><span class="sxs-lookup"><span data-stu-id="64959-110">Pricing dimensions</span></span>

<span data-ttu-id="64959-111">PSA varsayılan fiyatlandırma boyutları kümesiyle gelir.</span><span class="sxs-lookup"><span data-stu-id="64959-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="64959-112">Bunları, **Project Service** > **Parametreler** 'e giderek görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="64959-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="64959-113">Parametre kaydında, **Tutar tabanlı fiyatlandırma boyutları** sekmesinde, rolün ( **msdyn_resourcecategory** ) ve kaynak kuruluş biriminin ( **msdyn_organizationalunit** ) **Satış için geçerli** ve **Maliyet için geçerli** alanlarının **Evet** olarak ayarlanmış olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="64959-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="64959-114">Bu, her rol ve kuruluş birimi birleşimi için fiyatı ve maliyeti ayarlamanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="64959-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

!["Satış için geçerli" seçeneğinin vurgulandığı Project Service parametreleri ekran görüntüsü](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="64959-116">PSA sürüm 3'ten önce fiyatlandırma boyutları olarak rol ve kuruluş biriminin kullanıma hazır alanlarını kullanıyorduysanız belirgin bir değişiklik olmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="64959-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="64959-117">Project Service'ı her zamanki gibi kullanmaya devam edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="64959-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="64959-118">Kaynaklarınız için ek öznitelikleri kullanarak fiyat veya maliyet almanız gerekiyorsa, özelleştirilmiş alanlar, varlıklar ve boyutlar oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="64959-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="64959-119">Daha fazla bilgi için aşağıdaki konulara bakın ancak yordamları aşağıda listelendikleri sırada tamamlamanız gerektiğini unutmayın:</span><span class="sxs-lookup"><span data-stu-id="64959-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="64959-120">Özel alanlar ve varlıklar oluşturma</span><span class="sxs-lookup"><span data-stu-id="64959-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="64959-121">Fiyat ayarına ve işlem varlıklarına özel alan ekleme</span><span class="sxs-lookup"><span data-stu-id="64959-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="64959-122">Özel alanları fiyatlandırma boyutları olarak ayarlama </span><span class="sxs-lookup"><span data-stu-id="64959-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="64959-123">Yeni fiyatlandırma boyutları dahil etmek için eklenti özniteliklerini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="64959-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="64959-124">İnsan kaynağı zamanını fiyatlandırma</span><span class="sxs-lookup"><span data-stu-id="64959-124">Pricing human resource time</span></span>
<span data-ttu-id="64959-125">Bir kuruluşun insan kaynağı zamanını nasıl fiyatlandırdığı genellikle kuruluşun karlılığını doğrudan etkileyen önemli bir stratejik husustur.</span><span class="sxs-lookup"><span data-stu-id="64959-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="64959-126">Kuruluşunuz, insan kaynağı süresi için fatura ve maliyet oranlarını nasıl ayarlamak istediğini belirlediğinde, finans takımları ve uygulama liderleriyle birlikte çalışın.</span><span class="sxs-lookup"><span data-stu-id="64959-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="64959-127">Fiyatlandırma için dikkate alınan diğer hususlar, geçerli fiyatlandırma boyutları olmayan ancak kuruluşunuz için bir fiyatlandırma boyutu olarak uygulanan alanları veya varlıkları yeniden kullanmayı içerir.</span><span class="sxs-lookup"><span data-stu-id="64959-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="64959-128">**İşlem Kategorisi** ( **msdyn_transactioncategory** ) ve **Ayrılabilir Kaynak** ( **bookableresource** ) gibi alanlar aday boyutlara örnektir.</span><span class="sxs-lookup"><span data-stu-id="64959-128">Fields like **Transaction Category** ( **msdyn_transactioncategory** ) and **Bookable Resource** ( **bookableresource** ) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="64959-129">Fiyatlandırma boyutunuzun bir tablo mu yoksa seçenek kümesi mi olacağını da unutmayın.</span><span class="sxs-lookup"><span data-stu-id="64959-129">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="64959-130">Bir boyutun değerlerinde 10 veya 12'den fazla değişiklik öngörüyorsanız ve bu değerler üzerinde ek özniteliklere gereksinim varsa seçenek kümesi yerine bir varlık oluşturun.</span><span class="sxs-lookup"><span data-stu-id="64959-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, create an entity rather than an option set.</span></span> <span data-ttu-id="64959-131">Bir seçenek kümesini yönetmek için (değer ekleme veya kaldırma gibi) bir yönetici veya geliştirici gerekir ancak tabloya yeni satırlar eklemek çoğu iş kullanıcısı tarafından yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="64959-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most business users.</span></span>

<span data-ttu-id="64959-132">Aşağıdaki örnekte, kaynağın ait olduğu rol ve kaynak kuruluş birimine dayalı olarak ayarlanan fatura oranları gösterilir.</span><span class="sxs-lookup"><span data-stu-id="64959-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="64959-133">Maliyet oranları genellikle çalışanın maaş bandına ve ait olduğu kuruluş birimine göre yapılır.</span><span class="sxs-lookup"><span data-stu-id="64959-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="64959-134">Bu örnekte, fatura oranı ve maliyet oranı tabloları aşağıdaki gibi olacaktır.</span><span class="sxs-lookup"><span data-stu-id="64959-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="64959-135">**Örnek fatura oranları**</span><span class="sxs-lookup"><span data-stu-id="64959-135">**Sample bill rates**</span></span>

| <span data-ttu-id="64959-136">Rol</span><span class="sxs-lookup"><span data-stu-id="64959-136">Role</span></span>        | <span data-ttu-id="64959-137">Kuruluş Birimi</span><span class="sxs-lookup"><span data-stu-id="64959-137">Org Unit</span></span>    |<span data-ttu-id="64959-138">Birim</span><span class="sxs-lookup"><span data-stu-id="64959-138">Unit</span></span>      |<span data-ttu-id="64959-139">Fiyat</span><span class="sxs-lookup"><span data-stu-id="64959-139">Price</span></span>      |<span data-ttu-id="64959-140">Para Birimi</span><span class="sxs-lookup"><span data-stu-id="64959-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="64959-141">Geliştirici</span><span class="sxs-lookup"><span data-stu-id="64959-141">Developer</span></span>   | <span data-ttu-id="64959-142">Contoso ABD</span><span class="sxs-lookup"><span data-stu-id="64959-142">Contoso US</span></span>  |<span data-ttu-id="64959-143">Hour</span><span class="sxs-lookup"><span data-stu-id="64959-143">Hour</span></span> | <span data-ttu-id="64959-144">200</span><span class="sxs-lookup"><span data-stu-id="64959-144">200</span></span>|<span data-ttu-id="64959-145">USD</span><span class="sxs-lookup"><span data-stu-id="64959-145">USD</span></span>     |
| <span data-ttu-id="64959-146">Geliştirici</span><span class="sxs-lookup"><span data-stu-id="64959-146">Developer</span></span>   | <span data-ttu-id="64959-147">Contoso Hindistan</span><span class="sxs-lookup"><span data-stu-id="64959-147">Contoso India</span></span> |<span data-ttu-id="64959-148">Hour</span><span class="sxs-lookup"><span data-stu-id="64959-148">Hour</span></span>|   <span data-ttu-id="64959-149">112</span><span class="sxs-lookup"><span data-stu-id="64959-149">112</span></span>|<span data-ttu-id="64959-150">USD</span><span class="sxs-lookup"><span data-stu-id="64959-150">USD</span></span>     |


<span data-ttu-id="64959-151">**Örnek maliyet oranları**</span><span class="sxs-lookup"><span data-stu-id="64959-151">**Sample cost rates**</span></span>

| <span data-ttu-id="64959-152">Maaş bandı</span><span class="sxs-lookup"><span data-stu-id="64959-152">Salary Band</span></span>     | <span data-ttu-id="64959-153">Kuruluş Birimi</span><span class="sxs-lookup"><span data-stu-id="64959-153">Org Unit</span></span>    |<span data-ttu-id="64959-154">Birim</span><span class="sxs-lookup"><span data-stu-id="64959-154">Unit</span></span>      |<span data-ttu-id="64959-155">Fiyat</span><span class="sxs-lookup"><span data-stu-id="64959-155">Price</span></span>      |<span data-ttu-id="64959-156">Para Birimi</span><span class="sxs-lookup"><span data-stu-id="64959-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="64959-157">My company_Band1</span><span class="sxs-lookup"><span data-stu-id="64959-157">My company_Band1</span></span> | <span data-ttu-id="64959-158">Contoso ABD</span><span class="sxs-lookup"><span data-stu-id="64959-158">Contoso US</span></span>  |<span data-ttu-id="64959-159">Hour</span><span class="sxs-lookup"><span data-stu-id="64959-159">Hour</span></span> | <span data-ttu-id="64959-160">145</span><span class="sxs-lookup"><span data-stu-id="64959-160">145</span></span>|<span data-ttu-id="64959-161">USD</span><span class="sxs-lookup"><span data-stu-id="64959-161">USD</span></span>     |
| <span data-ttu-id="64959-162">My company_Band2</span><span class="sxs-lookup"><span data-stu-id="64959-162">My company_Band2</span></span> | <span data-ttu-id="64959-163">Contoso Hindistan</span><span class="sxs-lookup"><span data-stu-id="64959-163">Contoso India</span></span> |<span data-ttu-id="64959-164">Hour</span><span class="sxs-lookup"><span data-stu-id="64959-164">Hour</span></span>|   <span data-ttu-id="64959-165">67</span><span class="sxs-lookup"><span data-stu-id="64959-165">67</span></span>|<span data-ttu-id="64959-166">USD</span><span class="sxs-lookup"><span data-stu-id="64959-166">USD</span></span>     |
