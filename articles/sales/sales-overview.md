---
title: Satış süreçlerine genel bakış
description: Bu konu, temel satış süreçleri hakkında bilgi sağlar.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 09/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app: ''
ms.openlocfilehash: e66d96a940f3b22d5d1f3372d2b6767a4482d925
ms.sourcegitcommit: 7750485f8685a2ca5e1b3c165ead24a3b583c447
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2020
ms.locfileid: "3892454"
---
# <a name="sales-processes-overview"></a><span data-ttu-id="0602c-103">Satış süreçlerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="0602c-103">Sales processes overview</span></span>

<span data-ttu-id="0602c-104">Proje tabanlı bir kuruluşta kullanılan satış süreçleri, ürün tabanlı bir kuruluşta kullanılan satış süreçleriyle farklılık gösterir.</span><span class="sxs-lookup"><span data-stu-id="0602c-104">The sales processes that are used in a project-based organization differ from the sales processes that are used in a product-based organization.</span></span> <span data-ttu-id="0602c-105">Proje tabanlı kuruluşların satış döngülerinin uzun olmasından ve her bir anlaşma için teklifleri analiz etmek ve oluşturmak üzere özel tahmin teknikleri gerektirmesinden kaynaklanır.</span><span class="sxs-lookup"><span data-stu-id="0602c-105">This is because the sales cycles for project-based organizations are longer and require customized estimate techniques to analyze and create quotes for each deal.</span></span> <span data-ttu-id="0602c-106">Dynamics 365 Project Operations, satış işleminde kullanılan aşağıdaki işlevlerden bazılarını kullanır.</span><span class="sxs-lookup"><span data-stu-id="0602c-106">Dynamics 365 Project Operations uses some of the following functionality that is used in a sales process:</span></span>

- <span data-ttu-id="0602c-107">Müşteri adayı kaydı, satış işlemini izlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="0602c-107">A Lead record is used to track the sales process.</span></span>
- <span data-ttu-id="0602c-108">Uygun müşteri adayları fırsat olarak izlenir.</span><span class="sxs-lookup"><span data-stu-id="0602c-108">Qualifying leads are tracked as opportunities.</span></span>
- <span data-ttu-id="0602c-109">Bir fırsat için tüm ilgili yapılara erişilebilirdir.</span><span class="sxs-lookup"><span data-stu-id="0602c-109">All related artifacts for an opportunity are accessible.</span></span> <span data-ttu-id="0602c-110">Bu yapılar satış takımı, paydaşlar, olasılık, derecelendirme, satış aşamaları ve iş süreçlerini içerir.</span><span class="sxs-lookup"><span data-stu-id="0602c-110">These artifacts include the sales team, stakeholders, probability, rating, sales stages, and business processes.</span></span>
- <span data-ttu-id="0602c-111">Fırsat için birden çok teklif oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="0602c-111">Multiple quotes are created for an opportunity.</span></span>
- <span data-ttu-id="0602c-112">Bir teklif, bir satış siparişi oluşturmak için statüsü **Kazanıldı olarak kapatıldı** olarak değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="0602c-112">A quote is given the status, **Closed as Won** to create a sales order.</span></span> <span data-ttu-id="0602c-113">Project Operations'da, satış siparişi özelleştirilir ve proje sözleşmesi olarak adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="0602c-113">In Project Operations, the sales order is customized and called a project contract.</span></span>

## <a name="estimate-a-sale"></a><span data-ttu-id="0602c-114">Satış tahmini</span><span class="sxs-lookup"><span data-stu-id="0602c-114">Estimate a sale</span></span>
<span data-ttu-id="0602c-115">Bir satışın değeri, önceden teslim edilmiş projeler ve projelerin karmaşıklığı temel alınarak tahmin edilebilir.</span><span class="sxs-lookup"><span data-stu-id="0602c-115">The value of a sale can be estimated based on projects that have previously been delivered and the complexity of the projects.</span></span> <span data-ttu-id="0602c-116">Önceki projelerle ilgili uzantıları içeren projeler veya satıcı uzmanlığının yüksek olduğu ve tanınmış çalışma şablonları kullanılan projeler için, daha basit bir tahmin süreci kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0602c-116">For projects that involve extensions to previous projects, or projects where the vendor's expertise is high and well-known work templates are used, you can use a simpler estimation process.</span></span> <span data-ttu-id="0602c-117">Daha karmaşık projelerin genellikle daha uzun satın alma süreci bulunur.</span><span class="sxs-lookup"><span data-stu-id="0602c-117">More complex projects usually have a longer purchase process.</span></span> <span data-ttu-id="0602c-118">Bu nedenle, satış tahmini işleminde daha fazla aşama vardır.</span><span class="sxs-lookup"><span data-stu-id="0602c-118">Therefore, there are more stages in the sales estimation process.</span></span> <span data-ttu-id="0602c-119">Sürecin başlarında, satış takımı teklif edilen her farklı iş bileşeni için yüksek düzeyli bir tahmin oluşturmak için hesap yöneticileri ve konu uzmanlarının (SME) girişini kullanır.</span><span class="sxs-lookup"><span data-stu-id="0602c-119">Early in the process, the sales team uses the input of account managers and subject matter experts (SMEs) to create a high-level estimate for each distinct component of work that is quoted.</span></span> <span data-ttu-id="0602c-120">Bu çalışma bileşenleri, teklif satırlarıyla gösterilir.</span><span class="sxs-lookup"><span data-stu-id="0602c-120">These components of work are represented by quote lines.</span></span> 

<span data-ttu-id="0602c-121">Teklifin üst düzey tahminini oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0602c-121">You can create a high-level estimate of the quote.</span></span> <span data-ttu-id="0602c-122">Bu üst düzey tahmin en sonunda standartlaştırılmış proje şablonları kullanarak oluşturduğunuz proje planına dayalı daha ayrıntılı bir tahminle değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="0602c-122">Eventually, this high-level estimate will be replaced by a more detailed estimate that is based on a project plan that you create by using the standardized project templates.</span></span> <span data-ttu-id="0602c-123">Bu şablonlar bir zamanlama oluşturmanıza ve teklifte ve bileşenlerinde (teklif satırları) parasal değerleri belirlemenize yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="0602c-123">These templates help you build a schedule and determine monetary values on the quote and its components (quote lines).</span></span> 

<span data-ttu-id="0602c-124">Bir proje için birden çok teklif oluşturabilir ve bunları tek bir fırsat kaydına gruplayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0602c-124">You can create multiple quotes for a project and group them under a single opportunity record.</span></span> <span data-ttu-id="0602c-125">Sonuç olarak, bu tekliflerden biri **Kazanıldı olarak kapatıldı** şeklinde işaretlenir ve broje sözleşmesi ya da iş beyanı (SOW) oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="0602c-125">Eventually, one of the quotes is marked **Closed as Won**, and a project contract or statement of work (SOW) is created.</span></span> <span data-ttu-id="0602c-126">Proje sözleşmesi, müşteri tarafından teslimat için kabul edilen her bileşen (sözleşme satırı) için sözleşme değerini içerir.</span><span class="sxs-lookup"><span data-stu-id="0602c-126">A project contract holds the contracted value for each component (contract line) that is accepted by the customer for delivery.</span></span> <span data-ttu-id="0602c-127">Bir iş beyanı genellikle Microsoft Word belgesi olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="0602c-127">An SOW is usually created as a Microsoft Word document.</span></span> <span data-ttu-id="0602c-128">Projenin teslimatı sırasında müşteriye gönderilen tüm faturalar proje sözleşmesine veya iş beyanına referansta bulunur.</span><span class="sxs-lookup"><span data-stu-id="0602c-128">All invoices that are sent to the customer over the course of the project's delivery reference the project contract or SOW.</span></span>

<span data-ttu-id="0602c-129">Ayrıca, bir teklif kazanıldığında bir proje sözleşmesi oluşturulacak şekilde, bir fırsat kaydı altında alternatif teklifler oluşturabilir veya sistemi ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0602c-129">You can also create alternate quotes under one opportunity record or set up the system so that a project contract is created when a quote is won.</span></span> <span data-ttu-id="0602c-130">Bu durumda, proje sözleşme kaydına iş beyanını temsil eden bir Word belgesi ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0602c-130">In this case, you can attach a Word document that represents the SOW to the project contract record.</span></span>

## <a name="configure-the-sales-process"></a><span data-ttu-id="0602c-131">Satış sürecini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="0602c-131">Configure the sales process</span></span>
<span data-ttu-id="0602c-132">Satış sürecinizi yapılandırmak için, iş süreci akışlarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0602c-132">You can use business process flows to configure your sales process.</span></span> <span data-ttu-id="0602c-133">Bu akışlar, satış sürecinin aşamalarında ileri doğru hareket etmek için kılavuzlu bir görsel arabirim sağlar.</span><span class="sxs-lookup"><span data-stu-id="0602c-133">These flows provide a guided visual interface to move deals forward through the stages of the sales process.</span></span>

<span data-ttu-id="0602c-134">Örneğin, şirketiniz satış sürecinde aşağıdaki altı aşama bulunabilir:</span><span class="sxs-lookup"><span data-stu-id="0602c-134">For example, your company might have the following six stages in the sales process:</span></span>

1. <span data-ttu-id="0602c-135">Nitelikli Hale Getir</span><span class="sxs-lookup"><span data-stu-id="0602c-135">Qualify</span></span>
2. <span data-ttu-id="0602c-136">Tahmin</span><span class="sxs-lookup"><span data-stu-id="0602c-136">Estimate</span></span>
3. <span data-ttu-id="0602c-137">Dahili inceleme</span><span class="sxs-lookup"><span data-stu-id="0602c-137">Internal review</span></span>
4. <span data-ttu-id="0602c-138">Sözleşme</span><span class="sxs-lookup"><span data-stu-id="0602c-138">Contract</span></span>
5. <span data-ttu-id="0602c-139">Teslim Et</span><span class="sxs-lookup"><span data-stu-id="0602c-139">Deliver</span></span>
6. <span data-ttu-id="0602c-140">Kapat</span><span class="sxs-lookup"><span data-stu-id="0602c-140">Close</span></span>
 
<span data-ttu-id="0602c-141">Kuruluşunuz geliştikçe aynı anlaşmayı temsil etmek için farklı varlıklar kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="0602c-141">Your organization might use different entities to represent the same deal as it evolves.</span></span> <span data-ttu-id="0602c-142">Satış sürecinin başlarında, bir anlaşma Fırsat varlığı ile temsil edilir.</span><span class="sxs-lookup"><span data-stu-id="0602c-142">Early in the sales process, a deal is represented by the Opportunity entity.</span></span> <span data-ttu-id="0602c-143">Zaman geçtikçe ve daha fazla ayrıntı ortaya çıktığında, bir veya daha fazla teklif oluşturmak için yüksek düzeyde tahminler kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0602c-143">As time passes and more details emerge, you might use high-level estimates to create one or more quotes.</span></span> <span data-ttu-id="0602c-144">Bu tekliflerinden biri dahili ve müşteri paydaşları tarafından gözden geçirilirse, Teklif varlığı anlaşmayı temsil eder.</span><span class="sxs-lookup"><span data-stu-id="0602c-144">If one of these quotes is reviewed by internal and customer stakeholders, the Quote entity represents the deal.</span></span> <span data-ttu-id="0602c-145">Müşteri teklifi kabul ettikten sonra, bir proje sözleşmesi veya iş beyanı anlaşmayı temsil eder.</span><span class="sxs-lookup"><span data-stu-id="0602c-145">After the customer accepts the quote, a project contract or SOW represents the deal.</span></span> <span data-ttu-id="0602c-146">Bu davranışı desteklemek için, iş süreci akışları yapılandırılır ve böylece süreçteki her aşama farklı bir veritabanı tablosuna bağlanır.</span><span class="sxs-lookup"><span data-stu-id="0602c-146">To support this behavior, BPFs are structured so that each stage in the process is linked to a different database table.</span></span>

<span data-ttu-id="0602c-147">Satış sürecindeki **Uygun bul** aşaması bir Fırsat varlığıyla desteklenebilir.</span><span class="sxs-lookup"><span data-stu-id="0602c-147">The **Qualify** stage in the sales process can be backed by an Opportunity entity.</span></span> <span data-ttu-id="0602c-148">**Tahmin** ve **Dahili İnceleme** aşamaları bir Teklif varlığıyla desteklenebilir.</span><span class="sxs-lookup"><span data-stu-id="0602c-148">The **Estimate** and **Internal Review** stages can be backed by a Quote entity.</span></span> <span data-ttu-id="0602c-149">**Sözleşme**, **Teslimat** ve **Kapatma** aşamaları, bir Proje Sözleşmesi varlığı tarafından desteklenebilir.</span><span class="sxs-lookup"><span data-stu-id="0602c-149">The **Contract**, **Delivery**, and **Close** stages can be backed by a Project Contract entity.</span></span>

<span data-ttu-id="0602c-150">Anlaşmaşarı aşamalar arasında ilerlettiğinizde, süreç boyunca size yol göstermek için uygun varlık kaydını oluşturmanız istenir.</span><span class="sxs-lookup"><span data-stu-id="0602c-150">As you move deals through the stages, you're prompted to create the appropriate entity record to help and guide you through the process.</span></span> <span data-ttu-id="0602c-151">Aşamalar koşullu olabilir.</span><span class="sxs-lookup"><span data-stu-id="0602c-151">The stages can be conditional.</span></span> <span data-ttu-id="0602c-152">Örneğin, yalnızca teklif özel bir fiyat listesi kullanılması durumunda teklifin dahili olarak gözden geçirilmesini gerekli kılarsanız, bu koşulu iş sürecinin uygun aşamasında yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0602c-152">For example, if you require an internal review of a quote only if the quote uses a custom price list, you can configure that condition in the appropriate stage of the business process.</span></span> <span data-ttu-id="0602c-153">Ardından **Dahili İnceleme** aşaması yalnızca özel fiyat listesi kullanan teklifler için gösterilir.</span><span class="sxs-lookup"><span data-stu-id="0602c-153">The **Internal Review** stage is then shown only for quotes that use a custom price list.</span></span> <span data-ttu-id="0602c-154">Diğer tüm anlaşmalar ve teklifler için **Tahmin** aşamasının ardından **Sözleşme** aşaması gelir.</span><span class="sxs-lookup"><span data-stu-id="0602c-154">For all other deals and quotes, the **Estimate** stage is followed by the **Contract** stage.</span></span>

> [!NOTE]
> <span data-ttu-id="0602c-155">Project Operations'da Fırsat, Teklif, Sipariş ve Fatura varlık kayıtları için belirli sayfalar vardır.</span><span class="sxs-lookup"><span data-stu-id="0602c-155">Project Operations has specific pages for Opportunity, Quote, Order, and Invoice entity records.</span></span> <span data-ttu-id="0602c-156">Bu kayıtları, bu varlıkların proje bilgileri sayfalarını kullanarak oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="0602c-156">You must create these records using the project information pages for these entities.</span></span> <span data-ttu-id="0602c-157">Aksi takdirde, **Proje bilgileri** sayfasından kayıtları açamazsınız.</span><span class="sxs-lookup"><span data-stu-id="0602c-157">Otherwise, you won't be able to open the records from the **Project information** page.</span></span> <span data-ttu-id="0602c-158">**Proje bilgileri** sayfasından bir kayıt açmak isterseniz , kaydı silip bu varlık türlerinin her birine yönelik iş mantığının, kaydın **Tür** alanının doğru şekilde ayarlanmasını ve tüm zorunlu kavramların doğru şekilde başlatılmasını sağlayan **Proje bilgileri** sayfasını kullanarak yeniden oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="0602c-158">If you want to open a record from the **Project information** page, you must delete the record and recreate it using the **Project information** page where the business logic for each of these entity types ensures that the **Type** field of the record is set correctly, and all of the mandatory concepts are properly initialized.</span></span>


## <a name="track-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a><span data-ttu-id="0602c-159">Satış döngüsündeki tekliflerde ve proje planlarında incelemeleri izleme</span><span class="sxs-lookup"><span data-stu-id="0602c-159">Track revisions to quotes and project plans in the sales cycle</span></span>
<span data-ttu-id="0602c-160">Project Operations'da, teklife yapılan düzeltmeleri izleyemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="0602c-160">In Project Operations, you can't track revisions that are made to a quote.</span></span> <span data-ttu-id="0602c-161">Bunun yerine, varolan teklifi **Kaybedildi olarak kapatıldı** şeklinde işaretleyip yeni bir teklif oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="0602c-161">Instead, you must mark the existing quote **Closed as Lost** and then create a new quote.</span></span> <span data-ttu-id="0602c-162">Bir teklifi kopyalayabilir veya proje tabanlı teklifi çoğaltabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0602c-162">You can copy a quote or clone a project-based quote.</span></span>

## <a name="track-comments-and-approvals-of-quotes-and-project-contracts"></a><span data-ttu-id="0602c-163">Tekliflerin ve proje sözleşmelerinin açıklamalarını ve onaylarını izleme</span><span class="sxs-lookup"><span data-stu-id="0602c-163">Track comments and approvals of quotes and project contracts</span></span>
<span data-ttu-id="0602c-164">Tekliflerin ve proje sözleşmelerini inceleme ve onaylama işlemini, kayıt duvarını ve gönderileri kullanarak yönetebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0602c-164">You can manage the review and approval of quotes and project contracts by using the record wall and posts.</span></span> <span data-ttu-id="0602c-165">Kuruluşunuz, iş öğelerinin incelenmesi ve onaylanması ile ilgili bildirimlerini atamak, yeniden yönlendirmek, ilerletmek ve yönetmek için özel iş akışları ve eklentiler oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="0602c-165">Your organization can create custom workflows and plug-ins to assign, redirect, escalate, and manage notifications of review and the approval of work items.</span></span>