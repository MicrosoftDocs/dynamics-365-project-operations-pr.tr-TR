---
title: Proje sözleşmeleri
description: Bu konuda, çeşitli projeler ve finansman kaynaklar için oluşturabileceğiniz proje sözleşmeleri ve sözleşmeleri nasıl yönetebileceğiniz ve proje müşterilerine nasıl faturalandırabileceğiniz ile ilgili örnekler verilmiştir.
author: KimANelson
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 854ddfe6db93b7e93a4ee640268a9c8f254f24e7
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756666"
---
# <a name="project-contracts"></a><span data-ttu-id="072df-103">Proje sözleşmeleri</span><span class="sxs-lookup"><span data-stu-id="072df-103">Project contracts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="072df-104">Bu makalede, çeşitli projeler ve finansman kaynaklar için oluşturabileceğiniz proje sözleşmeleri ve sözleşmeleri nasıl yönetebileceğiniz ve proje müşterilerine nasıl faturalandırabileceğiniz ile ilgili örnekler verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="072df-104">This article provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers.</span></span>

<span data-ttu-id="072df-105">Proje sözleşmesi için oluşturduğunuz proje türü, proje müşterilerine faturalandırmak için kullanılacak yöntemi belirler.</span><span class="sxs-lookup"><span data-stu-id="072df-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="072df-106">Bir proje sözleşmesini ve ilgili projeyi değiştirebilirsiniz, ancak proje türünü değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="072df-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="072df-107">Bir proje sözleşmesini kullanarak, bir veya daha fazla projeyi aynı anda faturalandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="072df-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="072df-108">Proje sözleşmesi ayrıca bir proje yapısındaki her alt proje için tutarlı bir faturalama yordamının sağlanmasına yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="072df-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="072df-109">Faturalandırılacak her projenin bir proje sözleşmesiyle ilişkilendirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="072df-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="072df-110">Bir proje sözleşmesinin ayarları, bu proje sözleşmesiyle ilişkili tüm projelere ve alt projelere uygulanır.</span><span class="sxs-lookup"><span data-stu-id="072df-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="072df-111">Proje sözleşmesi bir veya daha fazla finansman kaynağını belirtebilir.</span><span class="sxs-lookup"><span data-stu-id="072df-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="072df-112">Bu nedenle, faturalamayı birden çok finansman arasında paylaştırabilir, finansman kaynaklarının belirtilen bir tutardan daha fazla faturalanmaması için finansman sınırlarını ayarlayabilir ve masrafların tahsil edilmesi ile ilgili finansman kurallarını yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="072df-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="072df-113">Proje sözleşmeleri için finansman</span><span class="sxs-lookup"><span data-stu-id="072df-113">Funding for project contracts</span></span>
<span data-ttu-id="072df-114">Bazı proje sözleşmeleri birden çok tarafın proje maliyetlerinin finansmanına yönelik sorumluluğu paylaştığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="072df-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="072df-115">İşte bazı örnekler:</span><span class="sxs-lookup"><span data-stu-id="072df-115">Here are some examples:</span></span>

-   <span data-ttu-id="072df-116">Birden çok bölümü bulunan büyük bir müşteri projenin finansmanını bölümler arasında paylaştırmak ister.</span><span class="sxs-lookup"><span data-stu-id="072df-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="072df-117">Şirketiniz, büyük bir projenin maliyetlerini dış bir kuruluşla paylaşır.</span><span class="sxs-lookup"><span data-stu-id="072df-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="072df-118">Bir yol projesi iki belediye tarafından finanse edilir.</span><span class="sxs-lookup"><span data-stu-id="072df-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="072df-119">Bir köprü projesi, bir devlet hibesi ve özel bir şirket tarafından finanse edilir.</span><span class="sxs-lookup"><span data-stu-id="072df-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="072df-120">Dynamics 365 Finance uygulamasında, tek bir hareketin veya tüm projenin faturalamasını, birden çok müşteri, hibe veya kuruluş arasında bölebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="072df-120">In Dynamics 365 Finance, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="072df-121">Birden çok finans kaynağı olan projelerde, gelişmiş bir finansman projesinin fonlarına katkıda bulunan tüm taraflar, finansman kaynakları olarak anılır.</span><span class="sxs-lookup"><span data-stu-id="072df-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="072df-122">Bir müşteri, kuruluş veya hibe finansman kaynağı olarak tanımlandıktan sonra, bir veya daha fazla finansman kuralına atanabilir.</span><span class="sxs-lookup"><span data-stu-id="072df-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="072df-123">Finansman kuralları masrafların bir proje için çeşitli finansman kaynaklarına nasıl tahsis edileceğini belirleyen ölçütleri içerir.</span><span class="sxs-lookup"><span data-stu-id="072df-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="072df-124">Satınalma taleplerinde ve satın alma siparişlerinde görüldüğü gibi stoku bulunan maddeler bölünemediği için, maliyet tutarı dağıtım sırasında birden çok finansman kaynağı arasında bölünemez.</span><span class="sxs-lookup"><span data-stu-id="072df-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="072df-125">Bu nedenle, finansman kaynak değeri stok çıkışı deftere nakledilene kadar 0 (sıfır) olarak kalır.</span><span class="sxs-lookup"><span data-stu-id="072df-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="072df-126">Stok çıkışı deftere nakledildiğinde, maliyet tutarı, projeyle ilgili hesap dağıtım kurallarına göre dağıtılır.</span><span class="sxs-lookup"><span data-stu-id="072df-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="072df-127">Burada, birden çok finansman kaynağı arasında faturalamayı kolaylaştırmak için gerçekleştirebileceğiniz bazı adımlar yer alır:</span><span class="sxs-lookup"><span data-stu-id="072df-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="072df-128">Bir proje için girilen tüm hareketlerin proje sözleşmesiyle aynı satış para birimini kullanmasını belirtin.</span><span class="sxs-lookup"><span data-stu-id="072df-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="072df-129">Finansman kaynağına bir proje ile ilişki olarak belirtilen tutardan daha fazla faturalandırılmaması için, finansman sınırları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="072df-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="072df-130">Her çalışan, madde, kategori, kategori grubu ve hareket türü (veya tüm hareket türleri için) için finansman kurallarını ve finansman sınırlarını yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="072df-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="072df-131">Her finansman kuralının geçerli olduğu dönemi tanımlamak için isteğe bağlı başlangıç ve bitiş tarihlerini seçin.</span><span class="sxs-lookup"><span data-stu-id="072df-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="072df-132">Her finansman kaynağının sorumlu olduğu yüzdeyi belirtin.</span><span class="sxs-lookup"><span data-stu-id="072df-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="072df-133">Finansman tahsisat hesaplamalarının neden olduğu yuvarlama farklarından hangi finansman kaynağının sorumlu olacağını belirtin.</span><span class="sxs-lookup"><span data-stu-id="072df-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="072df-134">Proje maliyetlerinin harici müşterilere nasıl faturalanacağını ve dahili kuruluşlardan nasıl ücret alınacağını belirleyen kurallar ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="072df-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="072df-135">Ek finansman elde edilene veya maliyetleri içeride üstlenmeye karar verene kadar bekletilen finansman hesabındaki hareketleri kaydedin.</span><span class="sxs-lookup"><span data-stu-id="072df-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="072df-136">Bir hareketle ilişkilendirilecek vergi grubunu belirlemek için projede bir vergi grubu ataması aranır.</span><span class="sxs-lookup"><span data-stu-id="072df-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="072df-137">Proje düzeyinde herhangi bir vergi grubu ataması yapılmadığında, proje sözleşmesi aranır.</span><span class="sxs-lookup"><span data-stu-id="072df-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="072df-138">Örnek: birden çok finansman kaynağı (basit)</span><span class="sxs-lookup"><span data-stu-id="072df-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="072df-139">Aşağıdaki tabloda, birden çok finansman kaynağı arasında finansman tahsisatını yönetmeye yönelik senaryolar verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="072df-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="072df-140">Bu senaryolar aşağıdaki varsayımlara dayanır:</span><span class="sxs-lookup"><span data-stu-id="072df-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="072df-141">Öncelik ayarları, diğer finansman kural ölçütlerinin uygulanabilmesi için fonların tahsisine göre ayrılır.</span><span class="sxs-lookup"><span data-stu-id="072df-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="072df-142">Finansman kuralının geçerli olduğu dönemini tanımlamak için herhangi bir tarih aralığı belirtilmedi.</span><span class="sxs-lookup"><span data-stu-id="072df-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="072df-143"><strong>Senaryo</strong></span><span class="sxs-lookup"><span data-stu-id="072df-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="072df-144"><strong>Finansman kaynağı</strong></span><span class="sxs-lookup"><span data-stu-id="072df-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="072df-145"><strong>Tahsisat yüzdesi</strong></span><span class="sxs-lookup"><span data-stu-id="072df-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="072df-146"><strong>Tahsisat önceliği</strong></span><span class="sxs-lookup"><span data-stu-id="072df-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="072df-147">Fonları tükenene kadar maliyetleri bir finansman kaynağına, ardından fonları tükenene kadar ikinci bir finansman kaynağına, sonrasında kalan maliyetleri de üçüncü bir finansman kaynağına tahsis etmek istersiniz.</span><span class="sxs-lookup"><span data-stu-id="072df-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="072df-148">Finansman kaynağı 1</span><span class="sxs-lookup"><span data-stu-id="072df-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="072df-149">Finansman kaynağı 2</span><span class="sxs-lookup"><span data-stu-id="072df-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="072df-150">Finansman kaynağı 3</span><span class="sxs-lookup"><span data-stu-id="072df-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="072df-151">100%</span><span class="sxs-lookup"><span data-stu-id="072df-151">100%</span></span></li>
<li><span data-ttu-id="072df-152">100%</span><span class="sxs-lookup"><span data-stu-id="072df-152">100%</span></span></li>
<li><span data-ttu-id="072df-153">100%</span><span class="sxs-lookup"><span data-stu-id="072df-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="072df-154">1</span><span class="sxs-lookup"><span data-stu-id="072df-154">1</span></span></li>
<li><span data-ttu-id="072df-155">2</span><span class="sxs-lookup"><span data-stu-id="072df-155">2</span></span></li>
<li><span data-ttu-id="072df-156">3</span><span class="sxs-lookup"><span data-stu-id="072df-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="072df-157">Maliyetin yüzde 75'ini bir finansman kaynağına ve yüzde 25'ini de ikinci bir finansman kaynağına tahsis etmek istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="072df-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="072df-158">Bu kaynaklardan biri tükendiğinde, kalan maliyetleri üçüncü bir finansman kaynağından ödemek istersiniz.</span><span class="sxs-lookup"><span data-stu-id="072df-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="072df-159">Finansman kaynağı 1</span><span class="sxs-lookup"><span data-stu-id="072df-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="072df-160">Finansman kaynağı 2</span><span class="sxs-lookup"><span data-stu-id="072df-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="072df-161">Finansman kaynağı 3</span><span class="sxs-lookup"><span data-stu-id="072df-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="072df-162">%75</span><span class="sxs-lookup"><span data-stu-id="072df-162">75%</span></span></li>
<li><span data-ttu-id="072df-163">%25</span><span class="sxs-lookup"><span data-stu-id="072df-163">25%</span></span></li>
<li><span data-ttu-id="072df-164">100%</span><span class="sxs-lookup"><span data-stu-id="072df-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="072df-165">1</span><span class="sxs-lookup"><span data-stu-id="072df-165">1</span></span></li>
<li><span data-ttu-id="072df-166">1</span><span class="sxs-lookup"><span data-stu-id="072df-166">1</span></span></li>
<li><span data-ttu-id="072df-167">2</span><span class="sxs-lookup"><span data-stu-id="072df-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="072df-168">Maliyetin yüzde 75'ini bir finansman kaynağına ve yüzde 25'ini de ikinci bir finansman kaynağına tahsis etmek istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="072df-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="072df-169">Bu finansman kaynaklarından biri tükendiğinde, kalan maliyetleri üçüncü ve dördünce finansman kaynakları arasında bölmek istersiniz.</span><span class="sxs-lookup"><span data-stu-id="072df-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="072df-170">Finansman kaynağı 1</span><span class="sxs-lookup"><span data-stu-id="072df-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="072df-171">Finansman kaynağı 2</span><span class="sxs-lookup"><span data-stu-id="072df-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="072df-172">Finansman kaynağı 3</span><span class="sxs-lookup"><span data-stu-id="072df-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="072df-173">Finansman kaynağı 4</span><span class="sxs-lookup"><span data-stu-id="072df-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="072df-174">%75</span><span class="sxs-lookup"><span data-stu-id="072df-174">75%</span></span></li>
<li><span data-ttu-id="072df-175">%25</span><span class="sxs-lookup"><span data-stu-id="072df-175">25%</span></span></li>
<li><span data-ttu-id="072df-176">%50</span><span class="sxs-lookup"><span data-stu-id="072df-176">50%</span></span></li>
<li><span data-ttu-id="072df-177">%50</span><span class="sxs-lookup"><span data-stu-id="072df-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="072df-178">1</span><span class="sxs-lookup"><span data-stu-id="072df-178">1</span></span></li>
<li><span data-ttu-id="072df-179">1</span><span class="sxs-lookup"><span data-stu-id="072df-179">1</span></span></li>
<li><span data-ttu-id="072df-180">2</span><span class="sxs-lookup"><span data-stu-id="072df-180">2</span></span></li>
<li><span data-ttu-id="072df-181">2</span><span class="sxs-lookup"><span data-stu-id="072df-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="072df-182">Maliyetin ilk yüzde 25'ini bir finansman kaynağına ve kalanı da ikinci bir finansman kaynağına tahsis etmek istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="072df-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="072df-183">Finansman kaynağı 1</span><span class="sxs-lookup"><span data-stu-id="072df-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="072df-184">Finansman kaynağı 2</span><span class="sxs-lookup"><span data-stu-id="072df-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="072df-185">%25</span><span class="sxs-lookup"><span data-stu-id="072df-185">25%</span></span></li>
<li><span data-ttu-id="072df-186">100%</span><span class="sxs-lookup"><span data-stu-id="072df-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="072df-187">1</span><span class="sxs-lookup"><span data-stu-id="072df-187">1</span></span></li>
<li><span data-ttu-id="072df-188">2</span><span class="sxs-lookup"><span data-stu-id="072df-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="072df-189">Örnek: birden çok finansman kaynağı (karmaşık)</span><span class="sxs-lookup"><span data-stu-id="072df-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="072df-190">Aşağıdaki sırada kullanmak istediğiniz üç finansman kaynağınız var:</span><span class="sxs-lookup"><span data-stu-id="072df-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="072df-191">Finansman kaynağı 2 tükenene kadar finansman kaynağı 2 ve finansman kaynağı 3'ü kullanın.</span><span class="sxs-lookup"><span data-stu-id="072df-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="072df-192">Finansman kaynağı 3 tükenene kadar kullanmaya devam edin.</span><span class="sxs-lookup"><span data-stu-id="072df-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="072df-193">Finansman kaynağı 3 tükendikten sonra finansman kaynağı 1'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="072df-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="072df-194">Bunu başarmak için önce aşağıdakileri yapmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="072df-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="072df-195">İlgili miktarlar için finansman kaynağı 2 ve finansman kaynağı 3 için finansman sınırlarını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="072df-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="072df-196">Aşağıdaki finansman kuralını oluşturun:</span><span class="sxs-lookup"><span data-stu-id="072df-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="072df-197">Kural 1 (Öncelik 1): Hareketlerin %50'sini finansman kaynağı 2'ye ve %50'sini de finansman kaynağı 3'e tahsis edin.</span><span class="sxs-lookup"><span data-stu-id="072df-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="072df-198">Kural 2 (Öncelik 2): Hareketlerin %100'ünü finansman kaynağı 3'e tahsis edin.</span><span class="sxs-lookup"><span data-stu-id="072df-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="072df-199">Kural 3 (Öncelik 3): Hareketlerin %100'ünü finansman kaynağı 1'e tahsis edin.</span><span class="sxs-lookup"><span data-stu-id="072df-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="072df-200">Kurallar ve sınırlar doğrultusunda hareketlere uygulanıp uygulanmayacağı denetlendiğinden bu kurulum işe yarar.</span><span class="sxs-lookup"><span data-stu-id="072df-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="072df-201">Hareket için belirli bir kural veya sınır uygulanmıyorsa Tüm hareketler kuralı uygulanır.</span><span class="sxs-lookup"><span data-stu-id="072df-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="072df-202">Tüm hareketler kuralı tüm hareketlerle eşleşir.</span><span class="sxs-lookup"><span data-stu-id="072df-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="072df-203">Bir hareketle eşleşen bir kural bulunursa, ancak eşleşme ayarlanan herhangi bir sınır için denetlendikten sonra o kuralda tahsis edilmiş yüzde değeri öncelikle uygulanır.</span><span class="sxs-lookup"><span data-stu-id="072df-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="072df-204">Bir sınır karşılanıyorsa ve bir finansman kaynağı tükenmişse, finansman sınırı ile ilişkilendirilmiş olan finansman kuralı gözardı edilir ve program uygulanacak sonraki kuralı denetler.</span><span class="sxs-lookup"><span data-stu-id="072df-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="072df-205">Bazı durumlardaysa, bir işlemin yalnızca bir kısmı bir kural altında tahsis edilebilir.</span><span class="sxs-lookup"><span data-stu-id="072df-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="072df-206">Hareket tahsis edildiğinde sınıra ulaşıldığı için bu durum oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="072df-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="072df-207">Bu durumda, yalnızca belirli bir tutar bir kurala (örneğin, her finansman kaynağı için yüzde 50) göre tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="072df-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="072df-208">Bu bölümde daha önce açıklandığı gibi, kural 1'deki durumdur.</span><span class="sxs-lookup"><span data-stu-id="072df-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="072df-209">Kalan tutar, dizideki bir sonraki kurala göre tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="072df-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="072df-210">Aşağıdaki tabloda bu senaryo daha ayrıntılı olarak incelenmiştir.</span><span class="sxs-lookup"><span data-stu-id="072df-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="072df-211"><strong>Odak</strong></span><span class="sxs-lookup"><span data-stu-id="072df-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="072df-212"><strong>Ayrıntılar</strong></span><span class="sxs-lookup"><span data-stu-id="072df-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="072df-213">Finansman kuralları</span><span class="sxs-lookup"><span data-stu-id="072df-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="072df-214">Kural 1 (Öncelik 1): Tüm hareketler.</span><span class="sxs-lookup"><span data-stu-id="072df-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="072df-215">Finansman kaynağı 2 ve finansman kaynağı 3'e %50'şer tahsis edin.</span><span class="sxs-lookup"><span data-stu-id="072df-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="072df-216">Kural 2 (Öncelik 2): Tüm hareketler.</span><span class="sxs-lookup"><span data-stu-id="072df-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="072df-217">Finansman kaynağı 3'e %100 tahsis edin.</span><span class="sxs-lookup"><span data-stu-id="072df-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="072df-218">Kural 3 (Öncelik 2): Tüm hareketler.</span><span class="sxs-lookup"><span data-stu-id="072df-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="072df-219">Finansman kaynağı 1'e %100 tahsis edin.</span><span class="sxs-lookup"><span data-stu-id="072df-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="072df-220">Finansman sınırları</span><span class="sxs-lookup"><span data-stu-id="072df-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="072df-221">Finansman kaynağı 1 sınırı = 10.000,00</span><span class="sxs-lookup"><span data-stu-id="072df-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="072df-222">Finansman kaynağı 2 sınırı = 500,00</span><span class="sxs-lookup"><span data-stu-id="072df-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="072df-223">Finansman kaynağı 3 sınırı = 750,00</span><span class="sxs-lookup"><span data-stu-id="072df-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="072df-224">İşlem 1</span><span class="sxs-lookup"><span data-stu-id="072df-224">Transaction 1</span></span></td>
<td><span data-ttu-id="072df-225"><strong>Hareket tutarı:</strong> 100,00<strong> Finansman:</strong> Hareket yalnızca kural 1 uygulandıktan sonra tam olarak ödendiğinden hareket yalnızca kural1'e göre ödenir.</span><span class="sxs-lookup"><span data-stu-id="072df-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="072df-226">Hareket, finansman kaynağı 2 ve finansman kaynağı 3 arasında eşit şekilde finanse edilir.</span><span class="sxs-lookup"><span data-stu-id="072df-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="072df-227">Finansman kaynağı 2: 50,00</span><span class="sxs-lookup"><span data-stu-id="072df-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="072df-228">Finansman kaynağı 3: 50,00</span><span class="sxs-lookup"><span data-stu-id="072df-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="072df-229">İşlem 2</span><span class="sxs-lookup"><span data-stu-id="072df-229">Transaction 2</span></span></td>
<td><span data-ttu-id="072df-230"><strong>Hareket miktarı:</strong> 5.000,00<strong> Finansman:</strong> Hareket üç kurala göre ödenir.</span><span class="sxs-lookup"><span data-stu-id="072df-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.</span></span> <span data-ttu-id="072df-231"><strong>Kural 1</strong>
</span><span class="sxs-lookup"><span data-stu-id="072df-231"><strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="072df-232">Finansman kaynağı 2: 450,00</span><span class="sxs-lookup"><span data-stu-id="072df-232">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="072df-233">Finansman kaynağı 3: 450,00</span><span class="sxs-lookup"><span data-stu-id="072df-233">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="072df-234">
<strong>Kural 2</strong>
</span><span class="sxs-lookup"><span data-stu-id="072df-234">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="072df-235">finansman Kaynağı 3: 250,00 (= 750,00 – 50,00 – 450,00)</span><span class="sxs-lookup"><span data-stu-id="072df-235">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="072df-236">
<strong>Kural 3</strong>
</span><span class="sxs-lookup"><span data-stu-id="072df-236">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="072df-237">Finansman kaynağı 1: 3.850,00 (= 5.000,00 – 450,00 – 450,00 – 250,00)</span><span class="sxs-lookup"><span data-stu-id="072df-237">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="072df-238">Her finansman kaynağına dağıtılan toplam fon</span><span class="sxs-lookup"><span data-stu-id="072df-238">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="072df-239">Finansman kaynağı 1: 3.850,00</span><span class="sxs-lookup"><span data-stu-id="072df-239">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="072df-240">Finansman kaynağı 2: 500,00</span><span class="sxs-lookup"><span data-stu-id="072df-240">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="072df-241">Finansman kaynağı 3: 750,00</span><span class="sxs-lookup"><span data-stu-id="072df-241">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="072df-242">Fatura kuralları</span><span class="sxs-lookup"><span data-stu-id="072df-242">Billing rules</span></span>
<span data-ttu-id="072df-243">Müşteriyle bir proje sözleşmesi üzerinde anlaştığınızda, bir projedeki işi müşteriye nasıl ve ne zaman faturalayabileceğinizi tanımlarsınız.</span><span class="sxs-lookup"><span data-stu-id="072df-243">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="072df-244">Proje sözleşmesini ve projesini ayarladıktan sonra, proje için faturalama kurallarını ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="072df-244">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="072df-245">Fatura kuralları, proje sözleşmesinde belirtilen proje koşullarına dayanır.</span><span class="sxs-lookup"><span data-stu-id="072df-245">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="072df-246">Oluşturabileceğiniz faturalama kuralları, proje sözleşmesinin koşullarına ve Saat ve malzeme ya da Sabit fiyatlı gibi faturalama kuralıyla ilişkilendirdiğiniz proje türüne bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="072df-246">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="072df-247">Bir proje sözleşmesi için birden çok faturalama kuralı oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="072df-247">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="072df-248">Ayrıca, aynı proje sözleşmesiyle ilişkilendirilmiş ve aynı fatura koşullarına sahip birden çok projeye faturalama kuralı atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="072df-248">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="072df-249">Aşağıdaki faturalama kuralı türlerini ayarlayabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="072df-249">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="072df-250">**Sevkiyat birimi**: Bir teslimat birimini tamamladığınızda müşteriye fatura edin.</span><span class="sxs-lookup"><span data-stu-id="072df-250">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="072df-251">Sözleşmede teslimat birimlerini tanımlarsınız.</span><span class="sxs-lookup"><span data-stu-id="072df-251">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="072df-252">**İlerleme**: Projenin belirtilen bir yüzdesini tamamladığınızda bir müşteriye faturalayın.</span><span class="sxs-lookup"><span data-stu-id="072df-252">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="072df-253">Tamamlanan çalışma yüzdesini otomatik olarak hesaplamak için bir faturalama kuralı ayarlayabilir veya tamamlanan çalışma yüzdesini ve müşteriyi faturalanacak miktarı el ile hesaplayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="072df-253">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="072df-254">**Kilometre taşı**: Kilometre taşına ulaşıldığında proje kilometre taşına ilişkin tüm miktarı bir müşteriye fatura edin.</span><span class="sxs-lookup"><span data-stu-id="072df-254">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="072df-255">**Ücret**: Servislerinizi ve tipik olarak servis ücretinin bir yüzdesinden oluşan yönetim ücretini müşteriye fatura edin.</span><span class="sxs-lookup"><span data-stu-id="072df-255">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="072df-256">**Zaman ve malzeme**: Bir projede kullanılan zamanın ve malzemelerin değerini müşteriye faturalayın.</span><span class="sxs-lookup"><span data-stu-id="072df-256">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="072df-257">Tüm faturalama kuralı türleri için, bir proje üzerinde anlaşılan bir aşamaya ulaşılana kadar müşteri faturalarından kesilecek bir bekletme yüzdesi belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="072df-257">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="072df-258">Ödeme bekletme yüzdesi proje sözleşmesinde belirtilir.</span><span class="sxs-lookup"><span data-stu-id="072df-258">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="072df-259">Tutar, bir müşteri faturasındaki satırların toplam değeri temel alınarak hesaplanır ve bunlardan çıkarılır.</span><span class="sxs-lookup"><span data-stu-id="072df-259">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="072df-260">**Zaman ve malzeme** ve **İlerleme** fatura kuralları için borçlandırılabilir kategoriler atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="072df-260">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="072df-261">Borçlandırılabilir kategoriler, müşteri faturalarına eklenmesi gereken hareketleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="072df-261">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="072df-262">Müşteriyi faturalamaya hazır olduğunuzda, proje için faturalanacak tutar faturalandırma kurallarına göre hesaplanır ve proje faturası teklifi üretilir.</span><span class="sxs-lookup"><span data-stu-id="072df-262">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="072df-263">Aşağıdaki bölümlerde, bir proje için faturalama kurallarının nasıl ayarlanacağını ve yönetileceğini örnekler verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="072df-263">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="072df-264">Örnek: teslim edilen birim sayısına bağlı bir faturalama kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="072df-264">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="072df-265">Kuruluşunuz, eğitim oturumu başına 10.000 maliyetinde müşterinin çalışanlarına toplam beş eğitim oturumu sağlamak üzere bir anlaşma yapar.</span><span class="sxs-lookup"><span data-stu-id="072df-265">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="072df-266">Her eğitim oturumundan sonra müşteriye faturalarsınız.</span><span class="sxs-lookup"><span data-stu-id="072df-266">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="072df-267">Sözleşme için faturalama kurallarını ayarladığınızda, aşağıdaki değerleri kullanın:</span><span class="sxs-lookup"><span data-stu-id="072df-267">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="072df-268">Teslimat birimi bir eğitim oturumudur.</span><span class="sxs-lookup"><span data-stu-id="072df-268">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="072df-269">Birim fiyat, eğitim oturumu başına 10.000'dir.</span><span class="sxs-lookup"><span data-stu-id="072df-269">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="072df-270">Toplam birim sayısı beş eğitim oturumudur.</span><span class="sxs-lookup"><span data-stu-id="072df-270">The total number of units is five training sessions.</span></span>

<span data-ttu-id="072df-271">Bir eğitim oturumunu tamamladığınızda, teslim edilen ilk birim için 10.000'lik bir fatura oluşturabilir ve faturayı müşteriye gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="072df-271">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="072df-272">Örnek: projeye ait belirtilen tamamlama yüzdesine bağlı bir faturala kuralı oluşturma (el ile hesaplama)</span><span class="sxs-lookup"><span data-stu-id="072df-272">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="072df-273">Yazılım danışmanlık firması olan kuruluşunuz, müşterinin geliştirdiği ürünün bir parçasını geliştirmek için müşteriyle bir anlaşma yapar.</span><span class="sxs-lookup"><span data-stu-id="072df-273">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="072df-274">Kuruluşunuz yazılım kodunu altı ay boyunca teslim etmeyi kabul eder.</span><span class="sxs-lookup"><span data-stu-id="072df-274">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="072df-275">Müşteri, iş için kuruluşunuza toplam 100.000 ödeme yapmayı kabul eder.</span><span class="sxs-lookup"><span data-stu-id="072df-275">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="072df-276">Sözleşmede belirtildiği gibi, proje üzerinde tamamlanan çalışma yüzdesine göre müşteriye faturalamak için bir faturalama kuralı oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="072df-276">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="072df-277">İlk ayın sonunda, tamamlanan çalışma yüzdesini belirlemek için müşteriyle toplantı yaparsınız.</span><span class="sxs-lookup"><span data-stu-id="072df-277">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="072df-278">Müşterinizle projeyi gözden geçirdikten sonra, projenin yüzde 15'nin tamamlanmış olduğuna karar verirsiniz.</span><span class="sxs-lookup"><span data-stu-id="072df-278">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="072df-279">100.000'in %15'i olan 15.000'lik bir fatura oluşturarak müşteriye gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="072df-279">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="072df-280">Örnek: projeye ait belirtilen tamamlama yüzdesine bağlı bir faturala kuralı oluşturma (otomatik hesaplama)</span><span class="sxs-lookup"><span data-stu-id="072df-280">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="072df-281">Yazılım geliştirme firması olan kuruluşunuz, bir müşteri için 30.000 değerinde bir bordro muhasebe paketi geliştirmeyi kabul eder.</span><span class="sxs-lookup"><span data-stu-id="072df-281">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="072df-282">Müşteri, iş için kuruluşunuza tamamlanan işin yüzdesine göre ödeme yapmayı kabul eder.</span><span class="sxs-lookup"><span data-stu-id="072df-282">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="072df-283">Proje maliyetlerinin 20.000 olduğunu tahmin ediyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="072df-283">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="072df-284">Proje sözleşmesi, faturalandırma sürecinde kullandığınız iş kategorilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="072df-284">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="072df-285">Her kategori için tamamlanan çalışma yüzdesinin fatura tutarlarını otomatik olarak hesaplayan fatura kurallarını ayarlarsınız.</span><span class="sxs-lookup"><span data-stu-id="072df-285">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="072df-286">Her kategori için bir bütçe ayarlarsınız:</span><span class="sxs-lookup"><span data-stu-id="072df-286">You set up a budget for each category:</span></span>

-   <span data-ttu-id="072df-287">**Geliştirme**: 15.000'lik maliyeti ve 20.000'lik gelir</span><span class="sxs-lookup"><span data-stu-id="072df-287">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="072df-288">**Yükleme**: 5.000'lik maliyet ve 10.000'lik gelir</span><span class="sxs-lookup"><span data-stu-id="072df-288">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="072df-289">Bir müşteri faturasını ilk kez oluşturduğunuzda, fatura tutarı otomatik olarak aşağıdaki bilgiler temel alınarak hesaplanır:</span><span class="sxs-lookup"><span data-stu-id="072df-289">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="072df-290">Bir ay sonra, projedeki çalışan proje için bir zaman çizelgesi gönderir.</span><span class="sxs-lookup"><span data-stu-id="072df-290">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="072df-291">Çalışanın saatlerinin maliyeti, geliştirme için 5.000 ve yükleme için 1.000'dir.</span><span class="sxs-lookup"><span data-stu-id="072df-291">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="072df-292">Geliştirme çalışması yüzde 33 tamamlandı (5.000 gerçek maliyet/15.000 bütçe maliyeti) ve yükleme çalışması yüzde 20 tamamlandı (1.000 gerçek maliyet/5000 bütçe maliyeti).</span><span class="sxs-lookup"><span data-stu-id="072df-292">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="072df-293">8.667'lik fatura tutarı otomatik olarak hesaplanır (20.000'in %33'ü + 10.000'in %20'si).</span><span class="sxs-lookup"><span data-stu-id="072df-293">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="072df-294">8.667'lik bir fatura oluşturarak müşteriye gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="072df-294">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="072df-295">Örnek: üzerinde anlaşmaya varılan kilometre taşları esas alınarak bir faturalama kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="072df-295">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="072df-296">Yönetim danışmalığı firması olan kuruluşunuz, müşterinin satış yapmayı planladığı bir tüketici ürünü için pazar araştırması yapmayı kabul eder.</span><span class="sxs-lookup"><span data-stu-id="072df-296">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="072df-297">Müşteri, Mart'tan başlayarak üç aylık süre için servislerinizi kullanmayı ve kuruluşunuza 50.000'lik ödeme yapmayı kabul eder.</span><span class="sxs-lookup"><span data-stu-id="072df-297">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="072df-298">Projenin üç kilometre taşı vardır:</span><span class="sxs-lookup"><span data-stu-id="072df-298">The project has three milestones:</span></span>

-   <span data-ttu-id="072df-299">Aşama 1: tüketici verisi toplama – 31 Mart</span><span class="sxs-lookup"><span data-stu-id="072df-299">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="072df-300">Kilometre taşı 2: tüketici verilerini çözümleme – 30 Nisan</span><span class="sxs-lookup"><span data-stu-id="072df-300">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="072df-301">Kilometre taşı 3: bir ürün uygulanabilirlik teklifi sunma – 31 Mayıs</span><span class="sxs-lookup"><span data-stu-id="072df-301">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="072df-302">Müşteri ilk kilometre taşı için kuruluşunuza 10.000, ikinci kilometre taşına için 20.000 ve üçüncü kilometre taşı için 20.000 ödemeyi kabul eder.</span><span class="sxs-lookup"><span data-stu-id="072df-302">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="072df-303">Proje sözleşmesini ayarlarken, tamamlanan kilometre taşına göre müşteriye faturalandırmayı kabul edersiniz.</span><span class="sxs-lookup"><span data-stu-id="072df-303">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="072df-304">Fatura kuralı ayarı aşağıdaki adımları içerir:</span><span class="sxs-lookup"><span data-stu-id="072df-304">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="072df-305">Proje kilometre taşlarını tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="072df-305">Define the project milestones.</span></span>
-   <span data-ttu-id="072df-306">Her kilometre taşı tamamlandığında müşteriye faturalamak için tutarı tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="072df-306">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="072df-307">İlk kilometre taşı 31 Mart'ta tamamlandığında kilometre taşını tamamlandı olarak işaretleyip 10.000 için bir fatura oluşturup müşteriye gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="072df-307">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="072df-308">Kilometre taşı tamamlandı olarak işaretlenmezse kilometre taşına yönelik fatura oluşturamazsınız.</span><span class="sxs-lookup"><span data-stu-id="072df-308">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="072df-309">Örnek: servisler ve yönetim ücretini temel alan bir ödeme kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="072df-309">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="072df-310">Yönetim danışmanlığı firması olan kuruluşunuz, perakende şirketi müşterisinin geliştirdiği ürünün uygulanabilirliğini değerlendirmek için pazar araştırması gerçekleştirmeyi kabul eder.</span><span class="sxs-lookup"><span data-stu-id="072df-310">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="072df-311">Anlaşmanın koşullarında, zaman ve malzeme temeli üzerinde araştırma yapan en önemli üç yönetim danışmanınız ile servislerinizi gerçekleştireceğiniz belirtiliyor.</span><span class="sxs-lookup"><span data-stu-id="072df-311">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="072df-312">Müşteri saatlik 100 ile projede tahsil edilen danışmanlık saatleri için yüzde 10 yönetim ücretini ödemeyi kabul eder.</span><span class="sxs-lookup"><span data-stu-id="072df-312">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="072df-313">Proje sözleşmesini ayarladığınızda, projede tahsil edilen danışmanlık saatlerine bir yüzde 10 yönetim ücreti eklemek için bir faturalandırma kuralı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="072df-313">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="072df-314">Müşteriye bir fatura oluşturduğunuzda, müşteri danışmanlık saatlerinin maliyetine ek olarak %10 yönetim ücreti faturalandırılır.</span><span class="sxs-lookup"><span data-stu-id="072df-314">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="072df-315">Örneğin, üç danışman proje üzerinde toplam 200 saat çalıştıysa, aşağıdaki hesaplama temel alınarak 22.000 için bir fatura oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="072df-315">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="072df-316">Saatlik 100 olmak üzere 200 saat = 20.000</span><span class="sxs-lookup"><span data-stu-id="072df-316">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="072df-317">Yüzde 10 yönetim ücreti = 2.000</span><span class="sxs-lookup"><span data-stu-id="072df-317">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="072df-318">Toplam fatura tutarı = 22.000</span><span class="sxs-lookup"><span data-stu-id="072df-318">Total invoice amount = 22,000</span></span>

<span data-ttu-id="072df-319">Ücretlerin vergisi müşteriye yansıtılıyorsa proje sözleşmesinde bir satış vergisi grubu seçerseniz, satış vergisi grubu otomatik olarak ücretler için oluşturulan faturalama kuralına girilir.</span><span class="sxs-lookup"><span data-stu-id="072df-319">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="072df-320">Örnek: zaman ve malzeme değeri için bir faturalama kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="072df-320">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="072df-321">Yazılım danışmanlık firması olan kuruluşunuz, bir yazılım geliştirme projesi üzerinde gelecek altı ay boyunca müşteri için çalışacak beş teknik danışman sağlamayı kabul eder.</span><span class="sxs-lookup"><span data-stu-id="072df-321">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="072df-322">Müşteri her bir danışmanlık saati için 150 ve ofis malzemelerinin maliyetini ödemeyi kabul eder.</span><span class="sxs-lookup"><span data-stu-id="072df-322">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="072df-323">Kuruluşunuz her ayın sonunda müşteriye bir fatura gönderir.</span><span class="sxs-lookup"><span data-stu-id="072df-323">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="072df-324">Proje sözleşmesini ayarlarken, proje üzerinde zaman ve malzeme için her ay müşteriye faturalamayı kabul etmiş olursunuz.</span><span class="sxs-lookup"><span data-stu-id="072df-324">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="072df-325">Aşağıdaki bilgileri içeren bir faturalama kuralı oluşturursunuz:</span><span class="sxs-lookup"><span data-stu-id="072df-325">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="072df-326">Sözleşme dönemi altı aydır.</span><span class="sxs-lookup"><span data-stu-id="072df-326">The contract period is six months.</span></span>
-   <span data-ttu-id="072df-327">Danışmanlık süresi saatlik 150 olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="072df-327">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="072df-328">Ofis tedariklerinin maliyeti faturalandırılır ve projenin toplam maliyeti 10.000'i aşmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="072df-328">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="072df-329">Proje sırasında her takvim ayının sonunda bir müşteri faturası oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="072df-329">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="072df-330">İlk ay boyunca, projedeki danışmanlar tarafından toplam 800 saat kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="072df-330">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="072df-331">Projede kullanılan ofis malzemelerinin maliyeti 2.000'dir.</span><span class="sxs-lookup"><span data-stu-id="072df-331">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="072df-332">Bu nedenle, ayın sonunda, saatlik 150 olmak üzere 800 saatlik iş ve 2.000'lik ofis malzemeleri için hesaplanan 122.000 için bir fatura oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="072df-332">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>



