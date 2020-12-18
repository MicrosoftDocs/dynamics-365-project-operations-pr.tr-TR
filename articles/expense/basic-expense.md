---
title: Gider girişi (Lite)
description: Bu konuda, bir Lite dağıtımında gider girişiyle nasıl çalışılacağı hakkında bilgiler sağlanmaktadır.
author: stsporen
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d87094882751f0751a8d9d539fa4cdcfc6b7b0d7
ms.sourcegitcommit: 16c442258ba24c79076cf5877a0f3c1f51a85f61
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/20/2020
ms.locfileid: "4590970"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="de011-103">Gider girişi (Lite)</span><span class="sxs-lookup"><span data-stu-id="de011-103">Expense entry (lite)</span></span>

<span data-ttu-id="de011-104">_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_</span><span class="sxs-lookup"><span data-stu-id="de011-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="de011-105">Temel veya Lite, gider yönetimi basit giderleri kaydetme özelliğidir.</span><span class="sxs-lookup"><span data-stu-id="de011-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="de011-106">Bir projenin giderlerini kaydettiğinizde, proje onaylayanı bu giderleri inceleyip onaylar.</span><span class="sxs-lookup"><span data-stu-id="de011-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="de011-107">Dynamics 365 Project Operations'ta gider özellikleri hakkında daha fazla bilgi için bkz. [Gidere genel bakış](expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="de011-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="de011-108">Temel gider yakalama</span><span class="sxs-lookup"><span data-stu-id="de011-108">Capture a basic expense</span></span>

<span data-ttu-id="de011-109">Giderlerinizi, onaylayana gönderebilmek için yakalayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="de011-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="de011-110">**Giderler**'e gidin ve **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="de011-110">Go to **Expenses**, and select **New**.</span></span>
2. <span data-ttu-id="de011-111">**Yeni Gider** sayfasında, gerekli gider bilgilerini girin ve ardından **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="de011-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="de011-112">Temel gider gönderme</span><span class="sxs-lookup"><span data-stu-id="de011-112">Submit a basic expense</span></span>

<span data-ttu-id="de011-113">Tüm giderlerinizi yakalamayı tamamladıktan ve onaylanmak üzere hazırladıktan sonra, giderleri göndermeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="de011-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="de011-114">**Giderler**'e gidin ve bir gider seçin.</span><span class="sxs-lookup"><span data-stu-id="de011-114">Go to **Expenses**, and select an expense.</span></span> <span data-ttu-id="de011-115">Alternatif olarak, başlıktaki onay kutusunu kullanarak tüm giderleri seçin.</span><span class="sxs-lookup"><span data-stu-id="de011-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="de011-116">**Gönder**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="de011-116">Select **Submit**.</span></span> <span data-ttu-id="de011-117">Sistem, seçili girişleri işler ve gider onay istekleri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="de011-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="add-an-attachment"></a><span data-ttu-id="de011-118">Bir ek ekle</span><span class="sxs-lookup"><span data-stu-id="de011-118">Add an attachment</span></span>

<span data-ttu-id="de011-119">Onaylayana, gideriniz hakkında ek belgeler sağlamanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="de011-119">You may have to provide the approver with additional documentation about your expense.</span></span> <span data-ttu-id="de011-120">Gider girişinin zaman çizelgesinde bir makbuz ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="de011-120">You can attach a receipt in the timeline of the expense entry.</span></span> <span data-ttu-id="de011-121">**Zaman Çizelgesi** bölümünde **Düzenle** seçeneğini belirleyin ve makbuzunuzu eklemek için ataş simgesini seçin.</span><span class="sxs-lookup"><span data-stu-id="de011-121">Select **Edit** and in the **Timeline** section, and then select the paperclip icon to attach your receipt.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="de011-122">Temel gideri geri çekme</span><span class="sxs-lookup"><span data-stu-id="de011-122">Recall a basic expense</span></span>

<span data-ttu-id="de011-123">Bir gideri yanlışlıkla gönderdiğinizde, bunu geri çekebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="de011-123">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="de011-124">Gider girişini geri çekmek için gereken süre, onay aşamasına bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="de011-124">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="de011-125">Onaylayan kişi girişi henüz onaylamadıysa, geri çekme hemen gerçekleşebilir.</span><span class="sxs-lookup"><span data-stu-id="de011-125">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="de011-126">Ancak, giriş zaten onaylanmışsa onaylayandan geri çekmeyi onaylaması ve işlemleri geri alması istenir.</span><span class="sxs-lookup"><span data-stu-id="de011-126">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="de011-127">**Giderler**'e gidin ve ardından gider listesinde, geri çekilecek gideri seçin.</span><span class="sxs-lookup"><span data-stu-id="de011-127">Go to **Expenses**, and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="de011-128">**Geri çek**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="de011-128">Select **Recall**.</span></span> <span data-ttu-id="de011-129">Gider girişi henüz onaylanmadıysa sistem bunu hemen geri çeker.</span><span class="sxs-lookup"><span data-stu-id="de011-129">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="de011-130">Gider girişi zaten onaylanmışsa onaylayanı, gideri geri almak istediğinizi onaylayan kişiye bildirmek için bir geri çekme isteği oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="de011-130">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="de011-131">Bundan sonra, onaylayan geri alma işleminin yapılabileceğini onaylar ve giriş iade edilir.</span><span class="sxs-lookup"><span data-stu-id="de011-131">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="de011-132">Temel gideri silme</span><span class="sxs-lookup"><span data-stu-id="de011-132">Delete a basic expense</span></span>

<span data-ttu-id="de011-133">Henüz gönderilmeyen giderler silinebilir.</span><span class="sxs-lookup"><span data-stu-id="de011-133">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="de011-134">Zaten gönderilmiş bir gideri silmek için öncelikle geri çekmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="de011-134">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="de011-135">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="de011-135">See also</span></span>

- [<span data-ttu-id="de011-136">Onaylara genel bakış</span><span class="sxs-lookup"><span data-stu-id="de011-136">Approvals overview</span></span>](../approvals/approvals-overview.md)
