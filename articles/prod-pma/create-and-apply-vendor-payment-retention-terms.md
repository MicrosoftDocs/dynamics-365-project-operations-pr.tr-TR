---
title: Satıcı ödemesini elde tutma koşullarını oluşturma ve uygulama
description: Bu konu, satıcı ödemeleri için bekletme koşullarının nasıl oluşturulacağı ve korunacağı hakkında bilgiler sağlar.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 1970a24a5073de6af43db1f1c068332c9ba9c8fe
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086461"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="f2db9-103">Satıcı ödemesini elde tutma koşullarını oluşturma ve uygulama</span><span class="sxs-lookup"><span data-stu-id="f2db9-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="f2db9-104">Bir proje için satıcı ödemesi tutma koşullarının ayarlanması, organizasyonunuz bir satıcıya yapılan ödemelerin bir kısmını korumak istediğinde faydalıdır.</span><span class="sxs-lookup"><span data-stu-id="f2db9-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="f2db9-105">Örneğin, ürün teslimatı beklentilerinize uygun olana kadar bir satıcıya ödeme tutmak istediğinizde.</span><span class="sxs-lookup"><span data-stu-id="f2db9-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="f2db9-106">Satıcı ödeme elde tutma koşulları, bir satıcı sözleşmesi üzerinde anlaşdığınızda belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="f2db9-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="f2db9-107">Satıcı ödemesini elde tutma koşullarını oluşturma</span><span class="sxs-lookup"><span data-stu-id="f2db9-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="f2db9-108">Bekletmeyle ilgili satıcı ödemesi yüzdesini ve serbest bırakılacak daha önceden tutulan tutarların yüzdesini girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f2db9-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="f2db9-109">Sözleşme belirtilen tamamlanma durumuna ulaşıncaya kadar, tutarlar satıcı faturalarında otomatik olarak korunur.</span><span class="sxs-lookup"><span data-stu-id="f2db9-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="f2db9-110">Bekletme şartlarını ayarladıktan sonra, bunları o satıcı için herhangi bir projeye uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f2db9-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="f2db9-111">Satıcı ödemeleri için Bekletme koşulları ayarlamak ve bakımını yapmak için aşağıdaki adımları kullanın.</span><span class="sxs-lookup"><span data-stu-id="f2db9-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="f2db9-112">**Proje yönetimi ve muhasebe** > **Elde tutma** > **satıcı ödeme Bekletme koşulları** 'na gidin.</span><span class="sxs-lookup"><span data-stu-id="f2db9-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="f2db9-113">Yeni bir satıcı bekletme terimi eklemek için **Yeni** 'ye gidin.</span><span class="sxs-lookup"><span data-stu-id="f2db9-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="f2db9-114">Yeni terime ait **kural kimliği** değeri otomatik olarak girilir.</span><span class="sxs-lookup"><span data-stu-id="f2db9-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="f2db9-115">**Açıklama** alanına kısa bir açıklama girin ve **şartlar** Hızlı sekmesinde, aşağıdakilere ait terim değerlerini girmek için **satır ekle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f2db9-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="f2db9-116">**Teslim edilen birimlerin yüzdesi** : Terimin tamamlanma yüzdesini girin.</span><span class="sxs-lookup"><span data-stu-id="f2db9-116">**Percentage of units delivered** : Enter a percentage of completion for the term.</span></span> <span data-ttu-id="f2db9-117">Proje tamamlanma durumu, belirtilen yüzdeye ulaşıncaya kadar, tutarlar satıcı faturalarında otomatik olarak korunur.</span><span class="sxs-lookup"><span data-stu-id="f2db9-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="f2db9-118">Örneğin, 50,00 girerseniz, proje yüzde 50 tamamlanıncaya kadar tutarlar korunur.</span><span class="sxs-lookup"><span data-stu-id="f2db9-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="f2db9-119">**Tutulacak yüzde** : korunacak satıcı fatura tutarının yüzdesini girin.</span><span class="sxs-lookup"><span data-stu-id="f2db9-119">**Percentage to retain** : Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="f2db9-120">Örneğin, 10,00 girerseniz, satıcı faturasındaki tutarın yüzde 10'u proje **teslim edilen birim yüzdesi** alanında ayarlandığı gibi tamamlanma yüzdesine ulaşıncaya kadar tutulur.</span><span class="sxs-lookup"><span data-stu-id="f2db9-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="f2db9-121">**Serbest bırakma yüzdesi** : Seçili proje düzeyi için serbest bırakılacak daha önceden tutulan tutarların yüzdesini girmek için **Satır ekle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f2db9-121">**Percentage to release** : Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="f2db9-122">Farklı proje tamamlama düzeyleri için birden çok kilometre taşınız varsa, her bir bekletme kuralı için ayrı bir satıcı bekletme terimi satırı girin.</span><span class="sxs-lookup"><span data-stu-id="f2db9-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="f2db9-123">Her satır, proje tamamlamada atanan her düzey için farklı bir bekletme yüzdesi ve farklı bir sürüm yüzdesi belirtebilir.</span><span class="sxs-lookup"><span data-stu-id="f2db9-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="f2db9-124">Bİr satıcı için satıcı elde tutma şartları oluşturduktan sonra şartları projeye uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f2db9-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="f2db9-125">Bir projeye satıcı Bekletme koşulları Uygula</span><span class="sxs-lookup"><span data-stu-id="f2db9-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="f2db9-126">**Proje yönetimi ve muhasebe** > **projeler** > **tüm projeler** 'e gidin ve proje listesi sayfasından bir proje açın.</span><span class="sxs-lookup"><span data-stu-id="f2db9-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="f2db9-127">**Satıcı anlaşmaları** hızlı sekmesinde **satır ekle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f2db9-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="f2db9-128">**Hesap kodu alanında** , aşağıdakilerden birini seçin:</span><span class="sxs-lookup"><span data-stu-id="f2db9-128">In the **Account code field** , select one of the following options:</span></span> 

   - <span data-ttu-id="f2db9-129">**Tablo** : satıcı Bekletme koşulları tek bir satıcı için uygulanır.</span><span class="sxs-lookup"><span data-stu-id="f2db9-129">**Table** : The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="f2db9-130">**Grup** : satıcı Bekletme koşulları bir satıcı grubundaki tüm satıcılar için uygulanır.</span><span class="sxs-lookup"><span data-stu-id="f2db9-130">**Group** : The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="f2db9-131">**Tümü** : Satıcı Bekletme koşulları tüm satıcılara uygulanır.</span><span class="sxs-lookup"><span data-stu-id="f2db9-131">**All** : The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="f2db9-132">**Satıcı/satıcı grubu alanında** , satıcı bekletme koşullarının uygulanacağı satıcı veya satıcı grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="f2db9-132">In the **Vendor/Vendor group field** , select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="f2db9-133">Önceki adımda **tümü** seçeneğini belirlediyseniz , bu alan kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="f2db9-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="f2db9-134">**Satıcı Bekletme koşulları** alanında, önceki yordamda oluşturduğunuz bekletme koşullarını seçin.</span><span class="sxs-lookup"><span data-stu-id="f2db9-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="f2db9-135">Projenin satıcı için ayarlanmış ödeme ödemesi (PWP) koşulları varsa, proje için eşik yüzdesini **PWP eşik yüzdesi** alanına girin.</span><span class="sxs-lookup"><span data-stu-id="f2db9-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="f2db9-136">Satıcı Bekletme koşulları, satıcı için oluşturduğunuz satınalma siparişlerinde de görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="f2db9-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>
