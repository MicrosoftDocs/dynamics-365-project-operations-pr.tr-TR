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
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="5e890-103">Fiyatlandırma boyutlarına genel bakış</span><span class="sxs-lookup"><span data-stu-id="5e890-103">Pricing dimensions overview</span></span>

<span data-ttu-id="5e890-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="5e890-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5e890-105">İnsan kaynaklarında fiyatlandırma ve maliyetlerin ayarlanması için kullanılan boyutlar iki kategoriye ayrılır:</span><span class="sxs-lookup"><span data-stu-id="5e890-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="5e890-106">Kişiler</span><span class="sxs-lookup"><span data-stu-id="5e890-106">People</span></span>
- <span data-ttu-id="5e890-107">Planlanan iş</span><span class="sxs-lookup"><span data-stu-id="5e890-107">Planned work</span></span>

<span data-ttu-id="5e890-108">Bu nedenle, iki tür fiyatlandırma boyutu değeri vardır:</span><span class="sxs-lookup"><span data-stu-id="5e890-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="5e890-109">**Seçenek kümeleri**: Bir değerler kümesi için sabit numaralandırmalar olan boyutlar.</span><span class="sxs-lookup"><span data-stu-id="5e890-109">**Option sets**: Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="5e890-110">**Varlık tabanlı değerler**: Değişken değer kümesi olabilecek boyutlar.</span><span class="sxs-lookup"><span data-stu-id="5e890-110">**Entity-based values**: Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="5e890-111">Fiyatlandırma boyutları</span><span class="sxs-lookup"><span data-stu-id="5e890-111">Pricing dimensions</span></span>

<span data-ttu-id="5e890-112">Dynamics 365 Project Operations varsayılan bir fiyatlandırma boyutları kümesiyle sevk eder.</span><span class="sxs-lookup"><span data-stu-id="5e890-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="5e890-113">Fiyatlandırma boyutlarını **Project Operations** > **Parametreler**'e giderek görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5e890-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="5e890-114">Parametre kaydında, **Tutar tabanlı fiyatlandırma boyutları** sekmesinde, rolün (**msdyn_resourcecategory**) ve kaynak kuruluş biriminin (**msdyn_organizationalunit**) **Satış için geçerli** ve **Maliyet için geçerli** alanlarının **Evet** olarak ayarlanmış olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="5e890-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="5e890-115">Bu alanlar etkinleştirildiğinde her rol ve kuruluş birimi birleşimi için fiyatı ve maliyeti ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5e890-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

<span data-ttu-id="5e890-116">Kaynaklarınız için ek öznitelikleri kullanarak fiyat veya maliyet almanız gerekiyorsa, özelleştirilmiş alanlar, varlıklar ve boyutlar oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5e890-116">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span>

## <a name="pricing-human-resource-time"></a><span data-ttu-id="5e890-117">İnsan kaynağı zamanını fiyatlandırma</span><span class="sxs-lookup"><span data-stu-id="5e890-117">Pricing human resource time</span></span>
<span data-ttu-id="5e890-118">Bir kuruluşun insan kaynağı zamanını nasıl fiyatlandırdığı genellikle kuruluşun karlılığını doğrudan etkileyen önemli bir stratejik husustur.</span><span class="sxs-lookup"><span data-stu-id="5e890-118">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="5e890-119">Kuruluşunuz, insan kaynağı süresi için fatura ve maliyet oranlarını nasıl ayarlamak istediğini belirlediğinde, finans takımları ve uygulama liderleriyle birlikte çalışın.</span><span class="sxs-lookup"><span data-stu-id="5e890-119">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="5e890-120">Fiyatlandırma için dikkate alınan diğer hususlar, geçerli fiyatlandırma boyutları olmayan ancak kuruluşunuz için bir fiyatlandırma boyutu olarak uygulanan alanları veya varlıkları yeniden kullanmayı içerir.</span><span class="sxs-lookup"><span data-stu-id="5e890-120">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="5e890-121">**İşlem Kategorisi** (**msdyn_transactioncategory**) ve **Ayrılabilir Kaynak** (**bookableresource**) gibi alanlar aday boyutlara örnektir.</span><span class="sxs-lookup"><span data-stu-id="5e890-121">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="5e890-122">Fiyatlandırma boyutunuzun bir tablo mu yoksa seçenek kümesi mi olacağını da unutmayın.</span><span class="sxs-lookup"><span data-stu-id="5e890-122">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="5e890-123">Bir boyutun değerlerinde 10 veya 12'yi aşacak değişiklikler öngörüyorsanız ve bu değerler üzerinde ek özniteliklere gereksinim varsa, seçenek kümesi yerine bir varlık oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5e890-123">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="5e890-124">Bir seçenek kümesini yönetmek için (değer ekleme veya kaldırma gibi) bir yönetici veya geliştirici gerekir ancak tabloya yeni satırlar eklemek çoğu kullanıcı tarafından yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="5e890-124">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="5e890-125">Aşağıdaki örnekte, kaynağın ait olduğu rol ve kaynak kuruluş birimine dayalı olarak ayarlanan fatura oranları gösterilir.</span><span class="sxs-lookup"><span data-stu-id="5e890-125">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="5e890-126">Maliyet oranları genellikle çalışanın maaş bandına ve ait olduğu kuruluş birimine göre yapılır.</span><span class="sxs-lookup"><span data-stu-id="5e890-126">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="5e890-127">Bu örnekte, fatura oranı ve maliyet oranı tabloları aşağıdaki gibi olacaktır.</span><span class="sxs-lookup"><span data-stu-id="5e890-127">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="5e890-128">**Örnek fatura oranları**</span><span class="sxs-lookup"><span data-stu-id="5e890-128">**Sample bill rates**</span></span>

| <span data-ttu-id="5e890-129">Rol</span><span class="sxs-lookup"><span data-stu-id="5e890-129">Role</span></span>        | <span data-ttu-id="5e890-130">Kuruluş Birimi</span><span class="sxs-lookup"><span data-stu-id="5e890-130">Org Unit</span></span>    |<span data-ttu-id="5e890-131">Birim</span><span class="sxs-lookup"><span data-stu-id="5e890-131">Unit</span></span>      |<span data-ttu-id="5e890-132">Fiyat</span><span class="sxs-lookup"><span data-stu-id="5e890-132">Price</span></span>      |<span data-ttu-id="5e890-133">Para Birimi</span><span class="sxs-lookup"><span data-stu-id="5e890-133">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="5e890-134">Geliştirici</span><span class="sxs-lookup"><span data-stu-id="5e890-134">Developer</span></span>   | <span data-ttu-id="5e890-135">Contoso ABD</span><span class="sxs-lookup"><span data-stu-id="5e890-135">Contoso US</span></span>  |<span data-ttu-id="5e890-136">Hour</span><span class="sxs-lookup"><span data-stu-id="5e890-136">Hour</span></span> | <span data-ttu-id="5e890-137">200</span><span class="sxs-lookup"><span data-stu-id="5e890-137">200</span></span>|<span data-ttu-id="5e890-138">USD</span><span class="sxs-lookup"><span data-stu-id="5e890-138">USD</span></span>     |
| <span data-ttu-id="5e890-139">Geliştirici</span><span class="sxs-lookup"><span data-stu-id="5e890-139">Developer</span></span>   | <span data-ttu-id="5e890-140">Contoso Hindistan</span><span class="sxs-lookup"><span data-stu-id="5e890-140">Contoso India</span></span> |<span data-ttu-id="5e890-141">Hour</span><span class="sxs-lookup"><span data-stu-id="5e890-141">Hour</span></span>|   <span data-ttu-id="5e890-142">112</span><span class="sxs-lookup"><span data-stu-id="5e890-142">112</span></span>|<span data-ttu-id="5e890-143">USD</span><span class="sxs-lookup"><span data-stu-id="5e890-143">USD</span></span>     |


<span data-ttu-id="5e890-144">**Örnek maliyet oranları**</span><span class="sxs-lookup"><span data-stu-id="5e890-144">**Sample cost rates**</span></span>

| <span data-ttu-id="5e890-145">Maaş bandı</span><span class="sxs-lookup"><span data-stu-id="5e890-145">Salary Band</span></span>     | <span data-ttu-id="5e890-146">Kuruluş Birimi</span><span class="sxs-lookup"><span data-stu-id="5e890-146">Org Unit</span></span>    |<span data-ttu-id="5e890-147">Birim</span><span class="sxs-lookup"><span data-stu-id="5e890-147">Unit</span></span>      |<span data-ttu-id="5e890-148">Fiyat</span><span class="sxs-lookup"><span data-stu-id="5e890-148">Price</span></span>      |<span data-ttu-id="5e890-149">Para Birimi</span><span class="sxs-lookup"><span data-stu-id="5e890-149">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="5e890-150">My company_Band1</span><span class="sxs-lookup"><span data-stu-id="5e890-150">My company_Band1</span></span> | <span data-ttu-id="5e890-151">Contoso ABD</span><span class="sxs-lookup"><span data-stu-id="5e890-151">Contoso US</span></span>  |<span data-ttu-id="5e890-152">Hour</span><span class="sxs-lookup"><span data-stu-id="5e890-152">Hour</span></span> | <span data-ttu-id="5e890-153">145</span><span class="sxs-lookup"><span data-stu-id="5e890-153">145</span></span>|<span data-ttu-id="5e890-154">USD</span><span class="sxs-lookup"><span data-stu-id="5e890-154">USD</span></span>     |
| <span data-ttu-id="5e890-155">My company_Band2</span><span class="sxs-lookup"><span data-stu-id="5e890-155">My company_Band2</span></span> | <span data-ttu-id="5e890-156">Contoso Hindistan</span><span class="sxs-lookup"><span data-stu-id="5e890-156">Contoso India</span></span> |<span data-ttu-id="5e890-157">Hour</span><span class="sxs-lookup"><span data-stu-id="5e890-157">Hour</span></span>|   <span data-ttu-id="5e890-158">67</span><span class="sxs-lookup"><span data-stu-id="5e890-158">67</span></span>|<span data-ttu-id="5e890-159">USD</span><span class="sxs-lookup"><span data-stu-id="5e890-159">USD</span></span>     |
