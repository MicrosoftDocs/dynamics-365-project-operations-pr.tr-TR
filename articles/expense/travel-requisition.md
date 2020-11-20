---
title: Seyahat talepleri
description: Bu konuda, seyahat talepleri hakkında bilgiler sağlanmaktadır.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 46a678ac4486c99f11d74dbac07dedd08364cb2f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123762"
---
# <a name="travel-requisitions"></a><span data-ttu-id="0a473-103">Seyahat talepleri</span><span class="sxs-lookup"><span data-stu-id="0a473-103">Travel requisitions</span></span>

<span data-ttu-id="0a473-104">_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="0a473-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="0a473-105">Seyahat talebi, seyahat amacıyla oluşacak giderleri listeler.</span><span class="sxs-lookup"><span data-stu-id="0a473-105">A travel requisition lists the expenses that will be incurred for the purpose of travel.</span></span> <span data-ttu-id="0a473-106">Seyahat talebi, incelenmek üzere gönderilir ve giderleri yetkilendirmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="0a473-106">A travel requisition is submitted for review and can be used to authorize expenses.</span></span>

<span data-ttu-id="0a473-107">Kuruluştan tahsil edilecek giderleri oluşturmadan önce seyahat talebi göndermeniz gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="0a473-107">You may be required to submit a travel requisition before you incur any expense that is charged to the organization.</span></span> <span data-ttu-id="0a473-108">Bu gereksinim, giderleri şirket kredi kartından ödediğinizde, nakit avans olarak aldığınız nakdi harcadığınızda ya da kuruluşun tazmin edeceği cepten yapılan harcamalar durumunda da geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="0a473-108">This requirement applies, regardless of whether you charge expenses to a corporate credit card, spend cash that you received from a cash advance, or incur out-of-pocket expenses that will be reimbursed by the organization.</span></span>

<span data-ttu-id="0a473-109">Seyahat talepleri ve ilkeler, kuruluşun giderlerini yönetmeye yardımcı olmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="0a473-109">Travel requisitions and policies can be used to help manage organization expenditures.</span></span> <span data-ttu-id="0a473-110">Örneğin, kuruluşunuz seyahat yapılmasını gerektiren bir sabit fiyatlı projede çalışıyorsa projenin takım üyelerinin seyahat giderleri proje bütçesini aşmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="0a473-110">For example, if your organization is working on a fixed-price project that requires travel, the travel expenses of the project's team members must fit within the project budget.</span></span> <span data-ttu-id="0a473-111">Seyahat giderlerinin harcanmadan önce onaylanmasını gerektirerek kuruluşun projenin bütçeyi aşmamasını sağlamasına yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="0a473-111">By requiring that travel expenses be approved before they are incurred, the organization can help make sure that the project remains within budget.</span></span>

## <a name="configuration"></a><span data-ttu-id="0a473-112">Yapılandırma</span><span class="sxs-lookup"><span data-stu-id="0a473-112">Configuration</span></span> 

<span data-ttu-id="0a473-113">Seyahat Talepleri, Gider Yönetimi Parametreleri'ndeki "Seyahatin önceden yetkilendirilmesi zorunludur" seçeneğini etkinleştirerek "zorunlu" olarak yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="0a473-113">Travel Requisitions can be configured as "mandatory" by enabling the "Pre-authorization of travel is mandatory" parameter in Expense Management Parameters.</span></span> 

## <a name="create-and-submit-a-travel-requisition"></a><span data-ttu-id="0a473-114">Seyahat talebi oluşturma ve gönderme</span><span class="sxs-lookup"><span data-stu-id="0a473-114">Create and submit a travel requisition</span></span>

1. <span data-ttu-id="0a473-115">**Giderlerim: Seyahat Talebi**'ne gidin ve **Yeni Seyahat Talebi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="0a473-115">Go to **My expenses: Travel Requisition**, and select **New travel Requisition**.</span></span>
2. <span data-ttu-id="0a473-116">Talep için bir amaç ve hedef girin.</span><span class="sxs-lookup"><span data-stu-id="0a473-116">Enter a purpose and destination for the requisition.</span></span>
3. <span data-ttu-id="0a473-117">**Seyahat açıklaması** alanında, diğer ek bilgileri girin.</span><span class="sxs-lookup"><span data-stu-id="0a473-117">In the  **Travel description** field, enter any additional information.</span></span> 
4. <span data-ttu-id="0a473-118">Uçuş, yemek veya araç kiralama gibi beklenen giderlerin her biri için bir gider satırı öğesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0a473-118">For each of the expected expenses, such as Flight, meals, or car rental, create an expense line item.</span></span> <span data-ttu-id="0a473-119">Her giderin tahmini tarihini, tahmini tutarını ve para birimini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="0a473-119">Include the estimated date, estimated amount, and the currency for each expense.</span></span> 
5. <span data-ttu-id="0a473-120">Beklenen giderleri eklemeyi bitirdiğinizde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0a473-120">When you have finished adding the expected expenses, select **Save**.</span></span>
6. <span data-ttu-id="0a473-121">Seyahat talebini göndermeye hazır olduğunuzda **İş Akışı** > **Gönder**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0a473-121">When you are ready to submit the travel requisition, select **Workflow** > **Submit**.</span></span>

<span data-ttu-id="0a473-122">Onaylanan seyahat taleplerinizi **Giderlerim: Seyahat Talebi** altından görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0a473-122">You can view your approved travel requisitions under **My Expenses: Travel Requisition**.</span></span> 

## <a name="view-available-travel-requisitions"></a><span data-ttu-id="0a473-123">Kullanılabilir seyahat taleplerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="0a473-123">View available travel requisitions</span></span>

<span data-ttu-id="0a473-124">Tüm seyahat taleplerinizi **Giderlerim: Seyahat Talepleri** altından görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0a473-124">You can view all of your travel requisitions under **My Expenses: Travel Requisitions**.</span></span>

## <a name="approve-travel-requisitions"></a><span data-ttu-id="0a473-125">Seyahat taleplerini onaylama</span><span class="sxs-lookup"><span data-stu-id="0a473-125">Approve travel requisitions</span></span>

<span data-ttu-id="0a473-126">Onaylamak istediğiniz seyahat talebini seçin ve ardından **İş Akışı** > **Onayla** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="0a473-126">Select the travel requisition that you want to approve, and then select **Workflow** > **Approve**.</span></span>  

## <a name="submit-an-expense-report-using-your-approved-travel-requisition"></a><span data-ttu-id="0a473-127">Onaylanmış seyahat talebinizi kullanarak bir gider raporu gönderme</span><span class="sxs-lookup"><span data-stu-id="0a473-127">Submit an expense report using your approved travel requisition</span></span>

1. <span data-ttu-id="0a473-128">Yeni bir gider raporu oluşturun ve gider raporu başlığında, onaylanmış seyahat talepleri listesinden **Seyahat talebine eşle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="0a473-128">Create a new expense report and in the expense report header, and from the list of approved travel requisitions, select **Map to Travel requisition**.</span></span>
2. <span data-ttu-id="0a473-129">**Seyahat talebi tutarı** alanı, gider raporu başlığında otomatik olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="0a473-129">The **Travel requisition amount** field is automatically updated in the expense report header.</span></span>
3. <span data-ttu-id="0a473-130">Yolculuk için oluşan her gideri ekleyin.</span><span class="sxs-lookup"><span data-stu-id="0a473-130">Add each expense incurred for the trip.</span></span> <span data-ttu-id="0a473-131">**Önceden Yetkilendirilmiş** alanı etkinse belirli bir gider kategorisine ilişkin mutabık olunan tutar ve yetkilendirilmiş tutar güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="0a473-131">If the **Pre-authorized** field is enabled, the reconciled amount and authorized amount for the specific expense category will be updated.</span></span>

> [!NOTE]
> <span data-ttu-id="0a473-132">Gider raporunu, onaylanmış bir seyahat talebiyle eşlediğinizde işlem tutarı, yetkilendirilmiş tutardan daha fazla olamaz.</span><span class="sxs-lookup"><span data-stu-id="0a473-132">When you map an expense report to an approved travel requisition, the transaction amount can't be greater than the authorized amount.</span></span> 
