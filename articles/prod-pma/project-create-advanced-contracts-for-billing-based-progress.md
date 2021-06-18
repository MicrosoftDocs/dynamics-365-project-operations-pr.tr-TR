---
title: İlerleme durumuna göre faturalama için gelişmiş sözleşmeler oluşturma
description: Bu konu, tamamlanan çalışmanın yüzdesine göre müşterilere fatura oluşturabilmek için proje sözleşmelerinin nasıl oluşturulacağını açıklar.
author: RadhikaRS
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 3b445488100e0a8335a05505405953b173ff836c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999695"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a><span data-ttu-id="1de78-103">İlerleme durumuna göre faturalama için gelişmiş sözleşmeler oluşturma</span><span class="sxs-lookup"><span data-stu-id="1de78-103">Create advanced contracts for billing based on progress</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="1de78-104">Bu konu, tamamlanan çalışmanın yüzdesine göre müşterilere fatura oluşturabilmek için proje sözleşmelerinin nasıl oluşturulacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="1de78-104">This topic explains how to create project contracts so that you can create invoices for customers, based on a percentage of completed work.</span></span> <span data-ttu-id="1de78-105">Fatura tutarları, proje için ayarladığınız çalışmanın bütçe kategorileri için otomatik olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="1de78-105">Invoice amounts are automatically calculated for the budget categories of work that you set up for a project.</span></span> <span data-ttu-id="1de78-106">Fatura zamanlaması, müşteriyle proje sözleşmesini görüşülediğinizde ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="1de78-106">The invoice timing is set when you negotiate the project contract with the customer.</span></span>

<span data-ttu-id="1de78-107">Bir sözleşme, ilişkili proje ve proje için ayarladığınız çalışma bütçe kategorileri için fatura tutarlarını hesaplayan faturalama kurallarını hesaplamak için bu konu yordamları kullanın.</span><span class="sxs-lookup"><span data-stu-id="1de78-107">Use the procedures in this topic to set up a contract, an associated project, and the billing rules that calculate invoice amounts for the budget categories of work that you set up for the project.</span></span>

<span data-ttu-id="1de78-108">Sözleşmeyi ve projeyi oluşturduktan sonra, projenin ayrıntılarını ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1de78-108">After you've created the contract and the project, you can set up the details of the project.</span></span> <span data-ttu-id="1de78-109">Örneğin, aktiviteleri tanımlayabilir ve projeye çalışanlar atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1de78-109">For example, you can define activities and assign workers to the project.</span></span>

## <a name="example"></a><span data-ttu-id="1de78-110">Örnek</span><span class="sxs-lookup"><span data-stu-id="1de78-110">Example</span></span>

<span data-ttu-id="1de78-111">Kuruluşunuz bir yazılım geliştirme firması.</span><span class="sxs-lookup"><span data-stu-id="1de78-111">Your organization is a software development firm.</span></span> <span data-ttu-id="1de78-112">Bir müşteri için bordro hesap paketi geliştirmeyi, toplam 20.000 ABD Doları (USD) için geliştirmeye karşı kabul etmiş olursunuz.</span><span class="sxs-lookup"><span data-stu-id="1de78-112">You agree to develop a payroll accounting package for a customer for a total fee of 20,000 US dollars (USD).</span></span> <span data-ttu-id="1de78-113">Kuruluşunuz, projenin belirli yüzdelerini tamamlatıkça müşteriyi faturalamaya kabul eder.</span><span class="sxs-lookup"><span data-stu-id="1de78-113">Your organization agrees to invoice the customer as you complete specific percentages of the project.</span></span> <span data-ttu-id="1de78-114">Çalışma için aşağıdaki proje kategorilerini ayarlarsınız, böylece bunları faturalandırma sürecinde kullanabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="1de78-114">You set up the following project categories for the work, so that you can use them in the billing process:</span></span>

- <span data-ttu-id="1de78-115">Danışmanlık Hizmetleri</span><span class="sxs-lookup"><span data-stu-id="1de78-115">Consulting</span></span>
- <span data-ttu-id="1de78-116">Tasarla</span><span class="sxs-lookup"><span data-stu-id="1de78-116">Design</span></span>
- <span data-ttu-id="1de78-117">Yükleme</span><span class="sxs-lookup"><span data-stu-id="1de78-117">Installation</span></span>

<span data-ttu-id="1de78-118">Her kategori için tamamlanan çalışma yüzdesinin fatura tutarlarını otomatik olarak hesaplayan fatura kurallarını ayarlarsınız.</span><span class="sxs-lookup"><span data-stu-id="1de78-118">You also set up billing rules that automatically calculate the invoice amounts for the percentage of project work that is completed in each category.</span></span>

<span data-ttu-id="1de78-119">Bütçe Yöneticisi Proje kategorileri için bir bütçe oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1de78-119">The budget manager creates a budget for the project categories.</span></span> <span data-ttu-id="1de78-120">Tamamlanan çalışmanın tutarı otomatik olarak, bütçelenen tutarlarla Karşılaştırılacak fiili çalışma yüzdesi olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="1de78-120">The amount of completed work is automatically calculated as a percentage of actual work in comparison to the budgeted amounts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1de78-121">Ön koşullar</span><span class="sxs-lookup"><span data-stu-id="1de78-121">Prerequisites</span></span>

<span data-ttu-id="1de78-122">Faturalandırma kuralları kullanan bir proje oluşturmadan önce, fatura kuralları için numara serilerini ve ilerlemeyi deftere nakletmek için kullanılan bir ücret günlüğünü ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="1de78-122">Before you create a project that uses billing rules, you must set up the number sequences for billing rules and a fee journal that is used to post progress billings.</span></span>

1. <span data-ttu-id="1de78-123">**Proje yönetimi ve muhasebe** \> **Kurulum** \> **Proje yönetimi ve muhasebe parametreleri** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="1de78-123">Go to **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>
2. <span data-ttu-id="1de78-124">**Proje yönetimi ve hesap oluşturma parametreleri** sayfasında, **Numara serileri** sekmesinde, fatura kuralları oluşturulduğunda kullanmak istediğiniz numara serisini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="1de78-124">On the **Project management and accounting parameters** page, on the **Number sequences** tab, set up the number sequence that you want to use when billing rules are created.</span></span>
3. <span data-ttu-id="1de78-125">**Proje yönetimi ve muhasebe** \> **Günlükler** \> **Ücret** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="1de78-125">Go to **Project management and accounting** \> **Journals** \> **Fee**.</span></span>
4. <span data-ttu-id="1de78-126">**Ücret günlüğü** sayfasında, **Yeni**'yi seçin ve günlük adını girin.</span><span class="sxs-lookup"><span data-stu-id="1de78-126">On the **Fee journal** page, select **New**, and enter the journal name.</span></span>

## <a name="create-a-contract-for-progress-billings"></a><span data-ttu-id="1de78-127">Sürmekte olan faturalama için sözleşme oluşturma</span><span class="sxs-lookup"><span data-stu-id="1de78-127">Create a contract for progress billings</span></span>

<span data-ttu-id="1de78-128">Sabit fiyatlı bir proje için Proje sözleşmesi oluşturmak için bu yordamı kullanın.</span><span class="sxs-lookup"><span data-stu-id="1de78-128">Use this procedure to create a project contract for a fixed-price project.</span></span> <span data-ttu-id="1de78-129">Proje üzerinde tamamlanan çalışma belirtilen yüzdeye ulaştığında proje faturası oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="1de78-129">You create a project invoice when the work that is completed on the project reaches a specified percentage.</span></span>

1. <span data-ttu-id="1de78-130">**Proje yönetimi ve muhasebe** \> **Projeler** \> **Proje sözleşmeleri** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="1de78-130">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="1de78-131">**Proje Sözleşmesi** ayrıntıları sayfasında **Yeni**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="1de78-131">On the **Project contracts** page, select **New**.</span></span>
3. <span data-ttu-id="1de78-132">**Yeni Proje sözleşmesi** iletişim kutusunda aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="1de78-132">In the **New project contract** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="1de78-133">**Ad**</span><span class="sxs-lookup"><span data-stu-id="1de78-133">**Name**</span></span>
    - <span data-ttu-id="1de78-134">**Fonlama Türü**</span><span class="sxs-lookup"><span data-stu-id="1de78-134">**Funding type**</span></span>
    - <span data-ttu-id="1de78-135">**Finansman kaynağı**</span><span class="sxs-lookup"><span data-stu-id="1de78-135">**Funding source**</span></span>
    - <span data-ttu-id="1de78-136">**Satış para birimi** – Varsayılan olarak, proje sözleşmesiyle ilişkili müşteri faturaları için bu para birimi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1de78-136">**Sales currency** – By default, this currency is used for customer invoices that are associated with the project contract.</span></span> <span data-ttu-id="1de78-137">Ancak, belirli bir müşteri faturasındaki satış para birimini değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1de78-137">However, you can change the sales currency on a specific customer invoice.</span></span>

4. <span data-ttu-id="1de78-138">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1de78-138">Select **OK**.</span></span> <span data-ttu-id="1de78-139">Bilgiler **Proje sözleşmeleri** sayfasının üstbilgisine kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="1de78-139">The information is copied to the header of the **Project contracts** page.</span></span>
5. <span data-ttu-id="1de78-140">**Proje sözleşmeleri** sayfasında, proje için gerekli kalan bilgileri doldurun.</span><span class="sxs-lookup"><span data-stu-id="1de78-140">On the **Project contracts** page, fill in the rest of the required information for the project.</span></span>

## <a name="create-a-project-for-progress-billings"></a><span data-ttu-id="1de78-141">Sürmekte olan faturalama için proje oluşturma</span><span class="sxs-lookup"><span data-stu-id="1de78-141">Create a project for progress billings</span></span>

<span data-ttu-id="1de78-142">Proje sözleşmesiyle ilişkili proje ve alt projeler oluşturmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="1de78-142">Follow these steps to create a project and any subprojects that are associated with a project contract.</span></span>

1. <span data-ttu-id="1de78-143">**Proje yönetimi ve muhasebe** \> **Projeler** \> **Tüm projeler** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="1de78-143">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="1de78-144">**TÜm projeler** sayfasında **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1de78-144">On the **All projects** page, select **New**.</span></span>
3. <span data-ttu-id="1de78-145">**Yeni proje** iletişim kutusunda, **Proje türü** alanında, **Saat ve malzeme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1de78-145">In the **New project** dialog box, in the **Project type** field, select **Time and material**.</span></span>
4. <span data-ttu-id="1de78-146">Proje grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="1de78-146">Select a project group.</span></span> <span data-ttu-id="1de78-147">Proje grubu, gruba atanan projelerle ilgili deftere nakil bilgilerini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="1de78-147">A project group defines the posting information for the projects that are assigned to the group.</span></span>
5. <span data-ttu-id="1de78-148">**Proje oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="1de78-148">Select **Create project**.</span></span>
6. <span data-ttu-id="1de78-149">Proje oluşturulduktan sonra, proje aşamasını **işlem sürüyor** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="1de78-149">After the project is created, set the project stage to **In process**.</span></span>

## <a name="create-a-budget-for-a-project"></a><span data-ttu-id="1de78-150">Proje için bütçe oluşturma</span><span class="sxs-lookup"><span data-stu-id="1de78-150">Create a budget for a project</span></span>

<span data-ttu-id="1de78-151">Bütçe kategorileri, her kategori için tamamlanan çalışma yüzdesinin fatura tutarlarını otomatik olarak hesaplar.</span><span class="sxs-lookup"><span data-stu-id="1de78-151">Budget categories are used to automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="1de78-152">Tahmini maliyetlerin bütçe kategorilerini oluşturmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="1de78-152">Follow these steps to create budget categories for the estimated costs.</span></span>

1. <span data-ttu-id="1de78-153">**Proje yönetimi ve muhasebe** \> **Projeler** \> **Tüm projeler** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="1de78-153">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="1de78-154">**Tüm projeler** sayfasında, istediğiniz projeyi seçin ve açın.</span><span class="sxs-lookup"><span data-stu-id="1de78-154">On the **All projects** page, select and open the project that you want.</span></span>
3. <span data-ttu-id="1de78-155">**Projeler** sayfasında, eylem bölmesinde, **plan** sekmesinde, **Bütçe** grubunda **Proje bütçesi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="1de78-155">On the **Projects** page, on the Action Pane, on the **Plan** tab, in the **Budget** group, select **Project budget**.</span></span>
4. <span data-ttu-id="1de78-156">**Proje bütçesi** sayfasında, projedeki her bir kategori için tahmini bir maliyet girin.</span><span class="sxs-lookup"><span data-stu-id="1de78-156">On the **Project budget** page, enter an estimated cost for each category in the project.</span></span>

## <a name="create-billing-rules-for-progress-billings"></a><span data-ttu-id="1de78-157">Gelişim faturaları için fatura kuralları oluşturma</span><span class="sxs-lookup"><span data-stu-id="1de78-157">Create billing rules for progress billings</span></span>

1. <span data-ttu-id="1de78-158">**Proje yönetimi ve muhasebe** \> **Projeler** \> **Proje sözleşmeleri** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="1de78-158">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="1de78-159">**Proje Sözleşmeleri** sayfasında bir proje sözleşmesi açın.</span><span class="sxs-lookup"><span data-stu-id="1de78-159">On the **Project contracts** page, select and open a project contract.</span></span>
3. <span data-ttu-id="1de78-160">Proje Sözleşmesi sayfasında, **Faturalama kuralları** hızlı sekmesinde, **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1de78-160">On the project contract page, on the **Billing rules** FastTab, select **Add**.</span></span>
4. <span data-ttu-id="1de78-161">**Faturalama kuralı** sayfasında, **satır türü** alanında, **ilerleme**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="1de78-161">On the **Billing rule** page, in the **Line type** field, select **Progress**.</span></span>
5. <span data-ttu-id="1de78-162">**Faturalama kuralı satırı ayrıntıları** Hızlı sekmesinde, **sözleşme değeri** alanına sözleşmenin toplam değerini girin.</span><span class="sxs-lookup"><span data-stu-id="1de78-162">On the **Billing rule line details** FastTab, in the **Contract value** field, enter the total value of the contract.</span></span>
6. <span data-ttu-id="1de78-163">**Kategori** alanında, masraf hareketini deftere nakletmek için kategoriyi seçin.</span><span class="sxs-lookup"><span data-stu-id="1de78-163">In the **Category** field, select the category to post the fee transaction to.</span></span>
7. <span data-ttu-id="1de78-164">**Proje** alanında, bu fatura kuralının kullanıldığı projeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="1de78-164">In the **Project** field, select the project that uses this billing rule.</span></span>
8. <span data-ttu-id="1de78-165">İsteğe bağlı: fatura kuralını ek projelere atayın.</span><span class="sxs-lookup"><span data-stu-id="1de78-165">Optional: Assign the billing rule to additional projects.</span></span> <span data-ttu-id="1de78-166">**Proje** Hızlı sekmesinde, **kullanılabilir projeler** bölümünde bir proje seçin ve ardından projeyi **Seçili projeler** bölümüne eklemek için sağ ok düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="1de78-166">On the **Project** FastTab, in the **Available projects** section, select a project, and then select the right arrow button to add the project to the **Selected projects** section.</span></span>
9. <span data-ttu-id="1de78-167">İsteğe bağlı: müşterinin bir faturadaki ödemeler üzerinden tuttuğu yüzde tutarını hesaplayın.</span><span class="sxs-lookup"><span data-stu-id="1de78-167">Optional: Calculate the percentage amount that the customer withholds from payments on an invoice.</span></span> <span data-ttu-id="1de78-168">**Ödeme bekletme şartları** hızlı sekmesinde, komik kaynağı seçin ve sonra **bekletme yüzdesi** alanına bekletme yüzdesini girin.</span><span class="sxs-lookup"><span data-stu-id="1de78-168">On the **Payment retention terms** FastTab, select the funding source, and then, in the **Retention percentage** field, enter the retention percentage.</span></span>
10. <span data-ttu-id="1de78-169">Proje sözleşmesiyle ilgili ek faturalama kuralları oluşturmak için bu adımları yineleyin.</span><span class="sxs-lookup"><span data-stu-id="1de78-169">Repeat these steps to create additional billing rules for the project contract.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]