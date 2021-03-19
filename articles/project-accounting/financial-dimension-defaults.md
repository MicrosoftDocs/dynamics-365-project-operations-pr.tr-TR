---
title: Mali boyut varsayılanları
description: Bu konu mali boyutun varsayılan ayarlarının nasıl ayarlanacağı hakkında bilgi sağlar.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: eec85b83cad4cd8fb6e0ec9c026c6a571bccf7f2
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287397"
---
# <a name="financial-dimension-defaults"></a><span data-ttu-id="d036f-103">Mali boyut varsayılanları</span><span class="sxs-lookup"><span data-stu-id="d036f-103">Financial dimension defaults</span></span>

<span data-ttu-id="d036f-104">_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="d036f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="d036f-105">Dynamics 365 Project Operations, proje alt defteri ve genel muhasebe işlemleri hakkında ek içgörüler sunmak için Dynamics 365 Finance uygulamasındaki [Mali boyutlar](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) çerçevesini kullanır.</span><span class="sxs-lookup"><span data-stu-id="d036f-105">Dynamics 365 Project Operations uses the [Financial dimensions](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) framework in Dynamics 365 Finance to provide additional insights on project subledger and general ledger transactions.</span></span>

<span data-ttu-id="d036f-106">Varsayılan mali boyutlar bir müşteri üzerinde kaynak, aşama, proje sözleşme satırı veya proje gibi davranan bir proje için ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="d036f-106">Default financial dimensions can be set on a customer, project funding source, milestone, project contract line, or project.</span></span>

## <a name="define-default-financial-dimensions-for-a-customer"></a><span data-ttu-id="d036f-107">Bir müşteri için varsayılan mali boyutlar tanımlama</span><span class="sxs-lookup"><span data-stu-id="d036f-107">Define default financial dimensions for a customer</span></span>

<span data-ttu-id="d036f-108">Müşteri boyutu Varsayılanları Finance'de belirtilmiştir.</span><span class="sxs-lookup"><span data-stu-id="d036f-108">Customer dimension defaults are specified in Finance.</span></span> <span data-ttu-id="d036f-109">Boyut varsayılanlarını ayarlamak için aşağıdaki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="d036f-109">Complete the following steps to set dimension defaults.</span></span>

1. <span data-ttu-id="d036f-110">**Alacak hesapları** > **Müşteriler** > **Tüm müşteriler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="d036f-110">Go to **Accounts receivable** > **Customers** > **All customers**.</span></span>
2. <span data-ttu-id="d036f-111">**Mali Boyutlar** sekmesindeki **müşteriler** sayfasında belirli bir müşterinin mali boyut değerlerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d036f-111">On the **Customers** page, on the **Financial dimensions** tab, set the financial dimension values for specific customer.</span></span>

## <a name="define-default-financial-dimensions-for-project-contracts"></a><span data-ttu-id="d036f-112">Proje sözleşmeleri için varsayılan mali boyutlar tanımlama</span><span class="sxs-lookup"><span data-stu-id="d036f-112">Define default financial dimensions for project contracts</span></span>

<span data-ttu-id="d036f-113">Proje sözleşmeleri Common Data Service (CDS) uygulamasında oluşturulur ve sürdürülür.</span><span class="sxs-lookup"><span data-stu-id="d036f-113">Project contracts are created and maintained in Common Data Service (CDS).</span></span> <span data-ttu-id="d036f-114">Proje sözleşmelerinin muhasebe öznitelikleri, Finance uygulamasındaki **Proje yönetimi ve muhasebe** modülünde ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="d036f-114">Accounting attributes for project contracts are set in the **Project management and accounting** module in Finance.</span></span>

### <a name="set-financial-dimensions-for-a-project-funding-source"></a><span data-ttu-id="d036f-115">Proje fonlama kaynağı için mali boyutlar ayarlama</span><span class="sxs-lookup"><span data-stu-id="d036f-115">Set financial dimensions for a project funding source</span></span>

1. <span data-ttu-id="d036f-116">**Proje yönetimi ve muhasebe** > **Projeler** > **Proje sözleşmeleri** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="d036f-116">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="d036f-117">Güncelleştirmek istediğiniz kaydı seçin ve **Proje sözleşmesi** sekmesinde **varsayılan hesaplamayı göster**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d036f-117">Select the record you want to update, and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="d036f-118">**İlgili bilgileri** genişletin ve **finansman kaynakları** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="d036f-118">Expand **Related information** and select the **Funding sources** tab.</span></span>
4. <span data-ttu-id="d036f-119">Mali boyut varsayılanlarını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d036f-119">Set the financial dimension defaults.</span></span> <span data-ttu-id="d036f-120">Mali boyutların müşteri hesabından varsayılan olarak değiştiğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="d036f-120">Notice that the financial dimensions default from the customer account.</span></span>

### <a name="set-financial-dimensions-for-a-project-contract-line"></a><span data-ttu-id="d036f-121">Proje sözleşme satırı için mali boyutlar ayarlama</span><span class="sxs-lookup"><span data-stu-id="d036f-121">Set financial dimensions for a project contract line</span></span>

1. <span data-ttu-id="d036f-122">**Proje yönetimi ve muhasebe** > **Projeler** > **Proje sözleşmeleri** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="d036f-122">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="d036f-123">Güncelleştirmek istediğiniz kaydı seçin ve **Proje sözleşmesi** sekmesinde **varsayılan hesaplamayı göster**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d036f-123">Select the record you want to update and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="d036f-124">**İlgili bilgileri** genişletin ve **Sözleşme satırları** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="d036f-124">Expand **Related information** and select the **Contract lines** tab.</span></span>
4. <span data-ttu-id="d036f-125">Mali boyut varsayılanlarını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d036f-125">Set the financial dimension defaults.</span></span> <span data-ttu-id="d036f-126">Mali boyut Varsayılanları geçerlidir ve yalnızca sabit fiyatlı (kilometre taşı) sözleşme satırlarıyla kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="d036f-126">The financial dimension defaults are applicable and can be used only with Fixed price (milestone) contract lines.</span></span>

<span data-ttu-id="d036f-127">Bu varsayılanlar ilgili proje mahsup işlemlerinde ve fatura satırlarında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d036f-127">These defaults are used on related project on-account transactions and invoice lines.</span></span>

## <a name="define-default-financial-dimensions-for-projects"></a><span data-ttu-id="d036f-128">Projeler için varsayılan mali boyutlar tanımlama</span><span class="sxs-lookup"><span data-stu-id="d036f-128">Define default financial dimensions for projects</span></span>

<span data-ttu-id="d036f-129">Projeler, CDS uygulamasında oluşturulur ve sürdürülür.</span><span class="sxs-lookup"><span data-stu-id="d036f-129">Projects are created and maintained in CDS.</span></span> <span data-ttu-id="d036f-130">Projelerin muhasebe öznitelikleri, Finance uygulamasındaki **Proje yönetimi ve muhasebe** modülünde ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="d036f-130">Accounting attributes for projects are set in the **Project management and accounting** module in Finance.</span></span>

1. <span data-ttu-id="d036f-131">**Proje yönetimi ve muhasebe** > **Projeler** > **Tüm projeler** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="d036f-131">Go to **Project management and accounting** > **Projects** > **All projects**.</span></span>
2. <span data-ttu-id="d036f-132">Güncelleştirmek istediğiniz kaydı seçin ve **Proje** sekmesinde **varsayılan hesaplamayı göster**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d036f-132">Select the record that you want to update and on the **Project** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="d036f-133">**İlgili bilgileri** genişletin ve **Kurulum** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="d036f-133">Expand **Related information** and select the **Setup** tab.</span></span>
4. <span data-ttu-id="d036f-134">Mali boyut varsayılanlarını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d036f-134">Set the financial dimension defaults.</span></span> <span data-ttu-id="d036f-135">Mali boyutların müşteri hesabından varsayılan olarak değiştiğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="d036f-135">Notice that financial dimensions default from the customer account.</span></span> <span data-ttu-id="d036f-136">Proje birden çok proje sözleşmesi müşterisi bulunan bir sözleşme satırıyla ilişkilendirilmişse, birincil müşteri varsayılan mali boyutlara göre kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d036f-136">If the project is associated with a contract line with multiple project contract customers, the primary customer is used to default financial dimensions.</span></span>

<span data-ttu-id="d036f-137">Proje varsayılan mali boyutları **Project Operations tümleştirme günlüğündeki** ve ilgili proje fatura satırlarındaki zaman, masraf ve masraf işlemlerine yönelik günlük satırı varsayılanlarını ayarlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d036f-137">Project default financial dimensions are used to set journal line defaults for time, expense, and fee transactions in the **Project Operations Integration Journal** and on related project invoice lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]