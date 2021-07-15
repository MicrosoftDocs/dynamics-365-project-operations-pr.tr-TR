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
ms.openlocfilehash: e8d62dcf9975e5427926210a881dec2c256f1b8b
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368500"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="f7812-103">Fiyatlandırma boyutlarına genel bakış</span><span class="sxs-lookup"><span data-stu-id="f7812-103">Pricing dimensions overview</span></span>

<span data-ttu-id="f7812-104">_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="f7812-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f7812-105">İnsan kaynaklarında fiyatlandırma ve maliyetlerin ayarlanması için kullanılan boyutlar iki kategoriye ayrılır:</span><span class="sxs-lookup"><span data-stu-id="f7812-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="f7812-106">Kişiler</span><span class="sxs-lookup"><span data-stu-id="f7812-106">People</span></span>
- <span data-ttu-id="f7812-107">Planlanan iş</span><span class="sxs-lookup"><span data-stu-id="f7812-107">Planned work</span></span>

<span data-ttu-id="f7812-108">Bu nedenle, iki tür fiyatlandırma boyutu değeri vardır:</span><span class="sxs-lookup"><span data-stu-id="f7812-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="f7812-109">**Seçenek kümeleri**: Bir değerler kümesi için sabit numaralandırmalar olan boyutlar.</span><span class="sxs-lookup"><span data-stu-id="f7812-109">**Option sets**: Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="f7812-110">**Varlık tabanlı değerler**: Değişken değer kümesi olabilecek boyutlar.</span><span class="sxs-lookup"><span data-stu-id="f7812-110">**Entity-based values**: Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="f7812-111">Fiyatlandırma boyutları</span><span class="sxs-lookup"><span data-stu-id="f7812-111">Pricing dimensions</span></span>

<span data-ttu-id="f7812-112">Dynamics 365 Project Operations, varsayılan fiyatlandırma boyutları kümesiyle gelir.</span><span class="sxs-lookup"><span data-stu-id="f7812-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="f7812-113">Fiyatlandırma boyutlarını **Project Operations** > **Parametreler**'e giderek görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f7812-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="f7812-114">Parametre kaydında, **Tutar tabanlı fiyatlandırma boyutları** sekmesinde, rolün (**msdyn_resourcecategory**) ve kaynak kuruluş biriminin (**msdyn_organizationalunit**) **Satış için geçerli** ve **Maliyet için geçerli** alanlarının **Evet** olarak ayarlanmış olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="f7812-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="f7812-115">Bu alanlar etkinleştirildiğinde her rol ve kuruluş birimi birleşimi için fiyatı ve maliyeti ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f7812-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

!["Satış için geçerli" seçeneğinin vurgulandığı Project Service parametreleri ekran görüntüsü](media/PS-OOB-parameters.png)

<span data-ttu-id="f7812-117">Kaynaklarınız için ek öznitelikleri kullanarak fiyat veya maliyet almanız gerekiyorsa, özelleştirilmiş alanlar, varlıklar ve boyutlar oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f7812-117">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="f7812-118">Daha fazla bilgi için aşağıdaki konulara bakın.</span><span class="sxs-lookup"><span data-stu-id="f7812-118">For more information, see the following topics.</span></span> 
  
  > [!NOTE]
  > <span data-ttu-id="f7812-119">Yordamların listelendikleri sırayla tamamlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="f7812-119">The procedures must be completed in the order they are listed.</span></span>

1. [<span data-ttu-id="f7812-120">Özel fiyatlandırma boyutları için çözüm oluşturma</span><span class="sxs-lookup"><span data-stu-id="f7812-120">Create a solution for custom pricing dimensions</span></span>](../sales/create-solution-custompd.md)
2. [<span data-ttu-id="f7812-121">Özel alanlar ve varlıklar oluşturma</span><span class="sxs-lookup"><span data-stu-id="f7812-121">Create custom fields and entities</span></span>](create-custom-fields-entities-pricing-dimensions.md)
3. [<span data-ttu-id="f7812-122">Fiyat ayarı ve geçiş varlıklarına özel alanlar ekleme </span><span class="sxs-lookup"><span data-stu-id="f7812-122">Add custom fields to price setup and transactional entities</span></span>](add-custom-fields-price-setup-transactional-entities.md)
4. [<span data-ttu-id="f7812-123">Özel alanları fiyatlandırma boyutları olarak ayarlama </span><span class="sxs-lookup"><span data-stu-id="f7812-123">Set up custom fields as pricing dimensions</span></span>](set-up-custom-fields-pricing-dimensions.md)
5. [<span data-ttu-id="f7812-124">Yeni fiyatlandırma boyutları dahil etmek için eklenti özniteliklerini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="f7812-124">Update plug-in attributes to include new pricing dimensions</span></span>](update-plugin-attributes-pd.md)


## <a name="pricing-human-resource-time"></a><span data-ttu-id="f7812-125">İnsan kaynağı zamanını fiyatlandırma</span><span class="sxs-lookup"><span data-stu-id="f7812-125">Pricing human resource time</span></span>
<span data-ttu-id="f7812-126">Bir kuruluşun insan kaynağı zamanını nasıl fiyatlandırdığı genellikle kuruluşun karlılığını doğrudan etkileyen önemli bir stratejik husustur.</span><span class="sxs-lookup"><span data-stu-id="f7812-126">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="f7812-127">Kuruluşunuz, insan kaynağı süresi için fatura ve maliyet oranlarını nasıl ayarlamak istediğini belirlediğinde, finans takımları ve uygulama liderleriyle birlikte çalışın.</span><span class="sxs-lookup"><span data-stu-id="f7812-127">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="f7812-128">Fiyatlandırma için dikkate alınan diğer hususlar, geçerli fiyatlandırma boyutları olmayan ancak kuruluşunuz için bir fiyatlandırma boyutu olarak uygulanan alanları veya varlıkları yeniden kullanmayı içerir.</span><span class="sxs-lookup"><span data-stu-id="f7812-128">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="f7812-129">**İşlem Kategorisi** (**msdyn_transactioncategory**) ve **Ayrılabilir Kaynak** (**bookableresource**) gibi alanlar aday boyutlara örnektir.</span><span class="sxs-lookup"><span data-stu-id="f7812-129">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="f7812-130">Fiyatlandırma boyutunuzun bir tablo mu yoksa seçenek kümesi mi olacağını da unutmayın.</span><span class="sxs-lookup"><span data-stu-id="f7812-130">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="f7812-131">Bir boyutun değerlerinde 10 veya 12'yi aşacak değişiklikler öngörüyorsanız ve bu değerler üzerinde ek özniteliklere gereksinim varsa, seçenek kümesi yerine bir varlık oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f7812-131">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="f7812-132">Bir seçenek kümesini yönetmek için (değer ekleme veya kaldırma gibi) bir yönetici veya geliştirici gerekir ancak tabloya yeni satırlar eklemek çoğu kullanıcı tarafından yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="f7812-132">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="f7812-133">Aşağıdaki örnekte, kaynağın ait olduğu rol ve kaynak kuruluş birimine dayalı olarak ayarlanan fatura oranları gösterilir.</span><span class="sxs-lookup"><span data-stu-id="f7812-133">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="f7812-134">Maliyet oranları genellikle çalışanın maaş bandına ve ait olduğu kuruluş birimine göre yapılır.</span><span class="sxs-lookup"><span data-stu-id="f7812-134">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="f7812-135">Bu örnekte, fatura oranı ve maliyet oranı tabloları aşağıdaki gibi olacaktır.</span><span class="sxs-lookup"><span data-stu-id="f7812-135">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="f7812-136">**Örnek fatura oranları**</span><span class="sxs-lookup"><span data-stu-id="f7812-136">**Sample bill rates**</span></span>

| <span data-ttu-id="f7812-137">Rol</span><span class="sxs-lookup"><span data-stu-id="f7812-137">Role</span></span>        | <span data-ttu-id="f7812-138">Kuruluş Birimi</span><span class="sxs-lookup"><span data-stu-id="f7812-138">Org Unit</span></span>    |<span data-ttu-id="f7812-139">Birim</span><span class="sxs-lookup"><span data-stu-id="f7812-139">Unit</span></span>      |<span data-ttu-id="f7812-140">Fiyat</span><span class="sxs-lookup"><span data-stu-id="f7812-140">Price</span></span>      |<span data-ttu-id="f7812-141">Para birimi</span><span class="sxs-lookup"><span data-stu-id="f7812-141">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="f7812-142">Geliştirici</span><span class="sxs-lookup"><span data-stu-id="f7812-142">Developer</span></span>   | <span data-ttu-id="f7812-143">Contoso ABD</span><span class="sxs-lookup"><span data-stu-id="f7812-143">Contoso US</span></span>  |<span data-ttu-id="f7812-144">Saat</span><span class="sxs-lookup"><span data-stu-id="f7812-144">Hour</span></span> | <span data-ttu-id="f7812-145">200</span><span class="sxs-lookup"><span data-stu-id="f7812-145">200</span></span>|<span data-ttu-id="f7812-146">USD</span><span class="sxs-lookup"><span data-stu-id="f7812-146">USD</span></span>     |
| <span data-ttu-id="f7812-147">Geliştirici</span><span class="sxs-lookup"><span data-stu-id="f7812-147">Developer</span></span>   | <span data-ttu-id="f7812-148">Contoso Hindistan</span><span class="sxs-lookup"><span data-stu-id="f7812-148">Contoso India</span></span> |<span data-ttu-id="f7812-149">Saat</span><span class="sxs-lookup"><span data-stu-id="f7812-149">Hour</span></span>|   <span data-ttu-id="f7812-150">112</span><span class="sxs-lookup"><span data-stu-id="f7812-150">112</span></span>|<span data-ttu-id="f7812-151">USD</span><span class="sxs-lookup"><span data-stu-id="f7812-151">USD</span></span>     |


<span data-ttu-id="f7812-152">**Örnek maliyet oranları**</span><span class="sxs-lookup"><span data-stu-id="f7812-152">**Sample cost rates**</span></span>

| <span data-ttu-id="f7812-153">Maaş bandı</span><span class="sxs-lookup"><span data-stu-id="f7812-153">Salary Band</span></span>     | <span data-ttu-id="f7812-154">Kuruluş Birimi</span><span class="sxs-lookup"><span data-stu-id="f7812-154">Org Unit</span></span>    |<span data-ttu-id="f7812-155">Birim</span><span class="sxs-lookup"><span data-stu-id="f7812-155">Unit</span></span>      |<span data-ttu-id="f7812-156">Fiyat</span><span class="sxs-lookup"><span data-stu-id="f7812-156">Price</span></span>      |<span data-ttu-id="f7812-157">Para birimi</span><span class="sxs-lookup"><span data-stu-id="f7812-157">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="f7812-158">My company_Band1</span><span class="sxs-lookup"><span data-stu-id="f7812-158">My company_Band1</span></span> | <span data-ttu-id="f7812-159">Contoso ABD</span><span class="sxs-lookup"><span data-stu-id="f7812-159">Contoso US</span></span>  |<span data-ttu-id="f7812-160">Saat</span><span class="sxs-lookup"><span data-stu-id="f7812-160">Hour</span></span> | <span data-ttu-id="f7812-161">145</span><span class="sxs-lookup"><span data-stu-id="f7812-161">145</span></span>|<span data-ttu-id="f7812-162">USD</span><span class="sxs-lookup"><span data-stu-id="f7812-162">USD</span></span>     |
| <span data-ttu-id="f7812-163">My company_Band2</span><span class="sxs-lookup"><span data-stu-id="f7812-163">My company_Band2</span></span> | <span data-ttu-id="f7812-164">Contoso Hindistan</span><span class="sxs-lookup"><span data-stu-id="f7812-164">Contoso India</span></span> |<span data-ttu-id="f7812-165">Saat</span><span class="sxs-lookup"><span data-stu-id="f7812-165">Hour</span></span>|   <span data-ttu-id="f7812-166">67</span><span class="sxs-lookup"><span data-stu-id="f7812-166">67</span></span>|<span data-ttu-id="f7812-167">USD</span><span class="sxs-lookup"><span data-stu-id="f7812-167">USD</span></span>     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]