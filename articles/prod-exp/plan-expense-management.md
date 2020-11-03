---
title: Gider yönetimini yapılandırma
description: Bu makalede, Microsoft Dynamics 365 Finance'ta gider yönetimini yapılandırmadan önce planlama sürecinde yapmanız gereken hususlar ve kararlar açıklanmaktadır .
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e2291515cc154fb5b34ca5802135791958bea1e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086472"
---
# <a name="configure-expense-management"></a><span data-ttu-id="b4dc7-103">Gider yönetimini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="b4dc7-103">Configure expense management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b4dc7-104">Bu makalede, gider yönetimini yapılandırmadan önce planlama sürecinde yapmanız gereken hususlar ve kararlar açıklanmaktadır .</span><span class="sxs-lookup"><span data-stu-id="b4dc7-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management.</span></span> <span data-ttu-id="b4dc7-105">Gider yönetiminde, ödeme yöntemleri, seyahat talepleri, gider raporları, ilkeler gibi bilgileri saklayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="b4dc7-106">Giderleri yönetmek için yapılandırmanızı planlarken yaptığınız kararların çoğu kuruluşunuzun hiyerarşisine ve mali yapısına göre olduğundan, bu alanlar için planlama belgelerine başvurmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="b4dc7-107">Şirketler arası giderler</span><span class="sxs-lookup"><span data-stu-id="b4dc7-107">Intercompany expenses</span></span>

<span data-ttu-id="b4dc7-108">Şirketlerarası giderleri etkinleştirdiğinizde, yasal varlıklara ve çalışanlara, başka bir tüzel kişiliizin adına gider neden olmaz ve kuruluşunuz içindeki yasal iş tüzel kişiliızdan ödeme toplayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="b4dc7-109">Örneğin, yasal varlık olan bir çalışan, yasal B varlığı için bir projeyi tamamlar ve proje seyahat ile ilgili giderleri de bu şekilde bir yer doğurur.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="b4dc7-110">Şirketlerarası giderler etkinleştirilmişse, çalışan geçerli bir varlık B 'ye gideri gönderecek bir gider raporu dosyalayarak, giderin yasal varlık A tarafından ödenmesi gerekir. Kuruluşunuzun birden çok varlık yoksa, şirketlerarası giderleri etkinleştirmek zorunda kalmamıştır.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="b4dc7-111">**Karar:** Şirketlerarası giderleri etkinleştirmek istiyor musunuz?</span><span class="sxs-lookup"><span data-stu-id="b4dc7-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="b4dc7-112">Finansal yönetim</span><span class="sxs-lookup"><span data-stu-id="b4dc7-112">Financial management</span></span>

<span data-ttu-id="b4dc7-113">Gider yönetimi, organizasyonunuzun mali yönetimiyle sıkı bir şekilde tümleşiktir.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="b4dc7-114">Gider yönetiminde kullandığınız büyük ihtimalle kuruluşunuzun mali hakkında yapmış olduğunuz kararlara göre yapılır.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="b4dc7-115">Aşağıdaki bölümlerde, organizasyonunuzun liderli takımınızdaki finansal karar ve kılavuza göre planlama ve karar gerektiren çeşitli alanlar açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="b4dc7-116">Harcırahlar</span><span class="sxs-lookup"><span data-stu-id="b4dc7-116">Per diems</span></span>

<span data-ttu-id="b4dc7-117">Kuruluşunuzun sağladığı her bir dıems için çalışanı tanımlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="b4dc7-118">Yemek, konaklama ve diğer arızi masraflar gibi giderleri kapsamak için her bir harcırah genellikle kullanılır, ancak kuruluşunuzun sundukları harcırah indirimleri için kurallar oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="b4dc7-119">Harcırah oranları yılın dönemini, seyahat edilen yeri veya her ikisini temel alabilir.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="b4dc7-120">Harcırah kuralı oluşturduğunuzda, bir çalışana ikram olarak sunulan yemekler veya hizmetler olduğunda harcırah oranının bir yüzdesinin kesilmesini belirleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="b4dc7-121">Ayrıca bir çalışanın seyahatinde uygulanabilecek harcırah oranı için en düşük ve en yüksek çalışma saatlerini de ayarlamak için harcırah başına fiyat katmanlarını tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="b4dc7-122">**Karar:**</span><span class="sxs-lookup"><span data-stu-id="b4dc7-122">**Decisions:**</span></span>

- <span data-ttu-id="b4dc7-123">Birinci ve son günler için varsayılan harcırah kuralları:</span><span class="sxs-lookup"><span data-stu-id="b4dc7-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="b4dc7-124">Bir çalışanın bir güne talep alabileceği ve yine de harcırah alabileceği en az saat sayısı nedir?</span><span class="sxs-lookup"><span data-stu-id="b4dc7-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="b4dc7-125">İlk gün ve geçen gün için faturalara sunulan tutarda bir azaltma var mı?</span><span class="sxs-lookup"><span data-stu-id="b4dc7-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="b4dc7-126">Bir azaltma varsa, bu azalma oranı nedir?</span><span class="sxs-lookup"><span data-stu-id="b4dc7-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="b4dc7-127">İlk gün ve geçen gün otel için faturalara sunulan tutarda bir azaltma var mı?</span><span class="sxs-lookup"><span data-stu-id="b4dc7-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="b4dc7-128">Bir azaltma varsa, bu azalma oranı nedir?</span><span class="sxs-lookup"><span data-stu-id="b4dc7-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="b4dc7-129">İlk gün ve geçen günoluşan diğer giderlerde faturalara sunulan tutarda bir azaltma var mı?</span><span class="sxs-lookup"><span data-stu-id="b4dc7-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="b4dc7-130">Bir azaltma varsa, bu azalma oranı nedir?</span><span class="sxs-lookup"><span data-stu-id="b4dc7-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="b4dc7-131">Varsayılan Harcırah kuralları:</span><span class="sxs-lookup"><span data-stu-id="b4dc7-131">Default per diem rules:</span></span>

    - <span data-ttu-id="b4dc7-132">Örneğin yemeğin her biri için harcırah indirimi alanında bir yüzde indirimi var mıdır?</span><span class="sxs-lookup"><span data-stu-id="b4dc7-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="b4dc7-133">Bir azaltma varsa, her öğün için bu azalma oranı nedir?</span><span class="sxs-lookup"><span data-stu-id="b4dc7-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="b4dc7-134">Her gün, seyahat başına veya her gün için yemekler sayısına göre hesaplanan yemek indirimi mu?</span><span class="sxs-lookup"><span data-stu-id="b4dc7-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="b4dc7-135">Harcırah miktarları düzenli şekilde yuvarlansın mı yoksa yuvarlanır mı?</span><span class="sxs-lookup"><span data-stu-id="b4dc7-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="b4dc7-136">Her zaman 24 saatlik bir dönemde veya takvim gününde hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="b4dc7-137">Şu konuma dayalı harcırah kuralları:</span><span class="sxs-lookup"><span data-stu-id="b4dc7-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="b4dc7-138">Harcırah oranları yerleşime göre farklılık gösterir mi?</span><span class="sxs-lookup"><span data-stu-id="b4dc7-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="b4dc7-139">Hangi konumlar dahil edilir?</span><span class="sxs-lookup"><span data-stu-id="b4dc7-139">What locations are included?</span></span>
    - <span data-ttu-id="b4dc7-140">Harcırah oranları konuma göre değişecekse her konum için aşağıdaki gider türleri için hangi yüzde tutarı sunulur:</span><span class="sxs-lookup"><span data-stu-id="b4dc7-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="b4dc7-141">Yemekler</span><span class="sxs-lookup"><span data-stu-id="b4dc7-141">Meals</span></span>
        - <span data-ttu-id="b4dc7-142">Otel</span><span class="sxs-lookup"><span data-stu-id="b4dc7-142">Hotel</span></span>
        - <span data-ttu-id="b4dc7-143">Diğer Giderler</span><span class="sxs-lookup"><span data-stu-id="b4dc7-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="b4dc7-144">Gider yönetimi günlükleri ve hesapları</span><span class="sxs-lookup"><span data-stu-id="b4dc7-144">Expense management journals and accounts</span></span>

<span data-ttu-id="b4dc7-145">Gider yönetimi için birden çok günlük ve firma kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="b4dc7-146">Örneğin, nakit avanslar ve kredi kartı itirazlarına yönelik aynı hesabın kullanılıp kullanılmadığını belirlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="b4dc7-147">**Karar:**</span><span class="sxs-lookup"><span data-stu-id="b4dc7-147">**Decisions:**</span></span>

- <span data-ttu-id="b4dc7-148">Hangi muhasebe günlüğünün nakledildiği gider raporları onaylandı?</span><span class="sxs-lookup"><span data-stu-id="b4dc7-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="b4dc7-149">Nakit avanslar için hangi hesap kullanılır?</span><span class="sxs-lookup"><span data-stu-id="b4dc7-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="b4dc7-150">Nakit avanslar hemen deftere nakledilsin mi?</span><span class="sxs-lookup"><span data-stu-id="b4dc7-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="b4dc7-151">Ödeme yöntemleri</span><span class="sxs-lookup"><span data-stu-id="b4dc7-151">Payment methods</span></span>

<span data-ttu-id="b4dc7-152">Çalışanların sizin işiniz için ücret almasına izin verdiğinizde, çalışanların kullanmalarına izin verilen ödeme yöntemlerini tanımlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="b4dc7-153">Örneğin, çalışanların nakit veya şirket kredi kartı kullanmasına izin verirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="b4dc7-154">Ayrıca çalışanların kişisel kredi kartı kullanmalarına izin verebilir ve ardından çalışanları reimburse.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="b4dc7-155">İzin verdiğiniz her ödeme yöntemi için aşağıdaki kararları almanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="b4dc7-156">**Karar:**</span><span class="sxs-lookup"><span data-stu-id="b4dc7-156">**Decisions:**</span></span>

- <span data-ttu-id="b4dc7-157">Hangi ödeme yöntemlerine izin verilir?</span><span class="sxs-lookup"><span data-stu-id="b4dc7-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="b4dc7-158">Ödeme yöntemi masraflarına kim sahip?</span><span class="sxs-lookup"><span data-stu-id="b4dc7-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="b4dc7-159">Mahsup hesap türü var mı?</span><span class="sxs-lookup"><span data-stu-id="b4dc7-159">Is there an offset account type?</span></span> <span data-ttu-id="b4dc7-160">Mahsup hesap türü varsa nedir?</span><span class="sxs-lookup"><span data-stu-id="b4dc7-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="b4dc7-161">Mahsup hesap türü varsa hesap nedir?</span><span class="sxs-lookup"><span data-stu-id="b4dc7-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="b4dc7-162">Ödeme yöntemi bir kredi kartınsa, ödeme yöntemi yalnızca içe aktarılan hareketlerle kullanılmalı mı?</span><span class="sxs-lookup"><span data-stu-id="b4dc7-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="b4dc7-163">Gider kategorileri ve paylaşılan kategorileri</span><span class="sxs-lookup"><span data-stu-id="b4dc7-163">Expense categories and shared categories</span></span>

<span data-ttu-id="b4dc7-164">Çalışanlar gider raporları oluşturduğunda, kaydettikleri her gider, bir gider kategorisiyle ilişkilendirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="b4dc7-165">Gider kategorileri, kuruluşunuzdaki tüzel kişilikler arasında paylaşılabilen paylaşılan kategorilerden türetilir.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="b4dc7-166">Bu kategoriler kuruluşunuzun tanımlanma biçimine bağlı olarak, proje yönetimi ve hesap işlemleri için de paylaşılabilir.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="b4dc7-167">Kuruluşunuzun tanımını ve uygulama takımının rehberliğini temel alarak Gider yönetiminde kullanılan kategorilerin yalnızca Gider yönetiminde mi kullanılacağını yoksa roje yönetimi ile muhasebe ve Gider yönetimi arasında mı paylaşılacağını belirlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="b4dc7-168">Bu kategoriler Proje ve Gider veya Proje ve Üretim arasında paylaşılabilir, Gider ve Üretim aasında paylaşılamaz.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="b4dc7-169">Her bir masraf kategorisi için aşağıdaki kararları almanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="b4dc7-170">**Karar:**</span><span class="sxs-lookup"><span data-stu-id="b4dc7-170">**Decisions:**</span></span>

- <span data-ttu-id="b4dc7-171">Gider kategorisi nedir?</span><span class="sxs-lookup"><span data-stu-id="b4dc7-171">What is the expense category?</span></span> <span data-ttu-id="b4dc7-172">Örnekler arasında uçuşlar, otel veya kilometre kategorileri yer alır.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="b4dc7-173">Gider kategorisi, Proje yönetimi ve muhasebede de kullanılabilir mi?</span><span class="sxs-lookup"><span data-stu-id="b4dc7-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="b4dc7-174">Gider türü nedir?</span><span class="sxs-lookup"><span data-stu-id="b4dc7-174">What is the expense type?</span></span>
- <span data-ttu-id="b4dc7-175">Gider kategorisi için varsayılan ödeme yöntemi nedir?</span><span class="sxs-lookup"><span data-stu-id="b4dc7-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="b4dc7-176">Gider kategorisindeki giderlerin dökümünün alınması gerekir mi?</span><span class="sxs-lookup"><span data-stu-id="b4dc7-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="b4dc7-177">Gider kategorisi için ana varsayılan hesap nedir?</span><span class="sxs-lookup"><span data-stu-id="b4dc7-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="b4dc7-178">Gider kategorisi için varsayılan öğe satış vergisi grubu nedir?</span><span class="sxs-lookup"><span data-stu-id="b4dc7-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="b4dc7-179">Gider kategorisi için ek ödeme yöntemlerine izin verilir mi?</span><span class="sxs-lookup"><span data-stu-id="b4dc7-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="b4dc7-180">Ek ödeme yöntemlerine izin veriliyorsa nedir?</span><span class="sxs-lookup"><span data-stu-id="b4dc7-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="b4dc7-181">Bu gider kategorisinde alt kategoriler var mı?</span><span class="sxs-lookup"><span data-stu-id="b4dc7-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="b4dc7-182">Alt kategoriler varsa aşağıdaki kararları da vermeniz gerekir:</span><span class="sxs-lookup"><span data-stu-id="b4dc7-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="b4dc7-183">Vergiden düşmeden dışlanan alt kategoriler var mı?</span><span class="sxs-lookup"><span data-stu-id="b4dc7-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="b4dc7-184">Alt kategorilerin öğe satış vergisi grubu nedir?</span><span class="sxs-lookup"><span data-stu-id="b4dc7-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="b4dc7-185">Gider kategorisi proje yönetimi ve muhasebe 'de de kullanılıyorsa, kalan soruları yanıtlayın.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="b4dc7-186">Aksi takdirde, bir sonraki bölüme geçin.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="b4dc7-187">Aşağıdaki giderler için hangi maliyet hesapları kullanılır?</span><span class="sxs-lookup"><span data-stu-id="b4dc7-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="b4dc7-188">Maliyet</span><span class="sxs-lookup"><span data-stu-id="b4dc7-188">Cost</span></span>
    - <span data-ttu-id="b4dc7-189">Bordro tahsisatı</span><span class="sxs-lookup"><span data-stu-id="b4dc7-189">Payroll allocation</span></span>
    - <span data-ttu-id="b4dc7-190">WIP-maliyet değeri</span><span class="sxs-lookup"><span data-stu-id="b4dc7-190">WIP-cost value</span></span>
    - <span data-ttu-id="b4dc7-191">Maliyet-öğe</span><span class="sxs-lookup"><span data-stu-id="b4dc7-191">Cost-item</span></span>
    - <span data-ttu-id="b4dc7-192">WIP-maliyet değeri-öğe</span><span class="sxs-lookup"><span data-stu-id="b4dc7-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="b4dc7-193">Tahakkuk eden zarar</span><span class="sxs-lookup"><span data-stu-id="b4dc7-193">Accrued loss</span></span>
    - <span data-ttu-id="b4dc7-194">WIP-tahakkuk eden zarar</span><span class="sxs-lookup"><span data-stu-id="b4dc7-194">WIP-accrued loss</span></span>

- <span data-ttu-id="b4dc7-195">Aşağıdakiler için hangi gelir hesapları kullanılır?</span><span class="sxs-lookup"><span data-stu-id="b4dc7-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="b4dc7-196">Faturalanan gelir</span><span class="sxs-lookup"><span data-stu-id="b4dc7-196">Invoiced revenue</span></span>
    - <span data-ttu-id="b4dc7-197">Tahakkuk eden gelir-satış değeri</span><span class="sxs-lookup"><span data-stu-id="b4dc7-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="b4dc7-198">WIP-satış değeri</span><span class="sxs-lookup"><span data-stu-id="b4dc7-198">WIP-sales value</span></span>
    - <span data-ttu-id="b4dc7-199">Tahakkuk eden gelir-üretim</span><span class="sxs-lookup"><span data-stu-id="b4dc7-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="b4dc7-200">WIP-üretim</span><span class="sxs-lookup"><span data-stu-id="b4dc7-200">WIP-production</span></span>
    - <span data-ttu-id="b4dc7-201">Tahakkuk eden gelir-kar</span><span class="sxs-lookup"><span data-stu-id="b4dc7-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="b4dc7-202">WIP-kar</span><span class="sxs-lookup"><span data-stu-id="b4dc7-202">WIP-profit</span></span>
    - <span data-ttu-id="b4dc7-203">Tahakkuk eden gelir-abonelik</span><span class="sxs-lookup"><span data-stu-id="b4dc7-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="b4dc7-204">WIP-abonelik</span><span class="sxs-lookup"><span data-stu-id="b4dc7-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="b4dc7-205">Vergiler</span><span class="sxs-lookup"><span data-stu-id="b4dc7-205">Taxes</span></span>

<span data-ttu-id="b4dc7-206">Giderle ilgili vergiler için, gider raporlarına nelerin dahil edildiğini veya etkinleştirildiğini belirlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="b4dc7-207">**Karar:**</span><span class="sxs-lookup"><span data-stu-id="b4dc7-207">**Decisions:**</span></span>

- <span data-ttu-id="b4dc7-208">Satış vergisi gider tutarlarına dahil edilsin mi?</span><span class="sxs-lookup"><span data-stu-id="b4dc7-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="b4dc7-209">Giderlere vergi kurtarmanın etkin olması gerekir mi?</span><span class="sxs-lookup"><span data-stu-id="b4dc7-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="b4dc7-210">Genel muhasebeyi planlarken, ABD satış vergisini uygulamaya karar verirseniz ve vergi kurallarını kullanacaksanız, giderlere vergi kurtarmayı etkinleştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="b4dc7-211">(ABD satış vergisini uygulamak ve vergi kurallarını kullanmak için, seçeneğini ayarlayın. **Satış vergisi vergilenmelerini kurallar** seçeneğini **Evet** olarak uygulayın.)</span><span class="sxs-lookup"><span data-stu-id="b4dc7-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="b4dc7-212">İlkeler</span><span class="sxs-lookup"><span data-stu-id="b4dc7-212">Policies</span></span>

<span data-ttu-id="b4dc7-213">Harcama raporu ilkelerini oluşturarak, organizasyonunuzun, çalışanlar adına giderler verirken zaman ve paradan tasarruf etmenize yardımcı olabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="b4dc7-214">İlkeler, çalışanların bütçe içinde kalacağı, gerekli tüm bilgileri sağladıkları ve yalnızca gereksinim duydukları para harcamasına yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="b4dc7-215">Oluşturduğunuz her gider raporu ilkesi ve her gider raporu onay ilkesi için aşağıdaki kararları almanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="b4dc7-216">**Karar:**</span><span class="sxs-lookup"><span data-stu-id="b4dc7-216">**Decisions:**</span></span>

- <span data-ttu-id="b4dc7-217">İlkenin adı ne?</span><span class="sxs-lookup"><span data-stu-id="b4dc7-217">What is the name of the policy?</span></span>
- <span data-ttu-id="b4dc7-218">Harcama ilkesi nedir?</span><span class="sxs-lookup"><span data-stu-id="b4dc7-218">What is the expense policy for?</span></span>
- <span data-ttu-id="b4dc7-219">Daha önce şirketlerarası giderleri etkinleştirmeye karar verirseniz, kuruluşunuzdaki hangi şirketler bu ilkeye uygulanır?</span><span class="sxs-lookup"><span data-stu-id="b4dc7-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="b4dc7-220">İlke ne zaman etkin olur?</span><span class="sxs-lookup"><span data-stu-id="b4dc7-220">When does the policy become effective?</span></span>
- <span data-ttu-id="b4dc7-221">İlke ne zaman zaman aşımına uğrayacak?</span><span class="sxs-lookup"><span data-stu-id="b4dc7-221">When does the policy expire?</span></span>
- <span data-ttu-id="b4dc7-222">İlke kuralı nedir?</span><span class="sxs-lookup"><span data-stu-id="b4dc7-222">What is the policy rule?</span></span>
- <span data-ttu-id="b4dc7-223">İlke kuralının sonucu ne?</span><span class="sxs-lookup"><span data-stu-id="b4dc7-223">What is the outcome of the policy rule?</span></span>
