---
title: Onaylara genel bakış
description: Bu konuda, Project Operations'ta onaylar ile çalışma hakkında bilgiler sağlanmaktadır.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 37994422e9146765076fdbb77f5c763b4f1d0802
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086184"
---
# <a name="approvals-overview"></a><span data-ttu-id="dc223-103">Onaylara genel bakış</span><span class="sxs-lookup"><span data-stu-id="dc223-103">Approvals overview</span></span>

<span data-ttu-id="dc223-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="dc223-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="dc223-105">Zaman ve Gider gönderimleri onay iş akışı aracılığıyla taşınır.</span><span class="sxs-lookup"><span data-stu-id="dc223-105">Time and Expense submissions move through an approval workflow.</span></span> <span data-ttu-id="dc223-106">Girişler onaylandıktan sonra işlemler gerçek değerler olarak kaydedilir veya süre, zamanlamada ayrılır.</span><span class="sxs-lookup"><span data-stu-id="dc223-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="dc223-107">Onaylar iş akışı</span><span class="sxs-lookup"><span data-stu-id="dc223-107">Approvals workflow</span></span>
<span data-ttu-id="dc223-108">Zaman veya gider girişi oluşturup gönderdiğinizde bir onay girişi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="dc223-108">When you create and submit a time or expense entry, an approval entry is created.</span></span> <span data-ttu-id="dc223-109">Projeyi onaylayan veya yöneticiniz girişinizi inceler ve onaylar.</span><span class="sxs-lookup"><span data-stu-id="dc223-109">The Project approver or your manager reviews and approves your entry.</span></span> <span data-ttu-id="dc223-110">Giriş bir projeyle ilgiliyse onaylandığında gerçek değerler oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="dc223-110">If the entry is related to a project, when it's approved, the actuals will be created.</span></span> <span data-ttu-id="dc223-111">Bu, maliyetin ve faturanın izlenmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="dc223-111">This allows the cost and billing to be tracked.</span></span> 

## <a name="approve-an-entry"></a><span data-ttu-id="dc223-112">Girişi onaylama</span><span class="sxs-lookup"><span data-stu-id="dc223-112">Approve an entry</span></span>
<span data-ttu-id="dc223-113">**Onaylar** formu, farklı onay türlerini görüntüleyebilmeniz için farklı görünümler arasında geçiş yapmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="dc223-113">The **Approvals** form allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="dc223-114">**Onaylar** formuna gidin ve **Giderler** , **Zaman** veya **Geri Çağırmalar** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="dc223-114">Go to the **Approvals** form and select **Expenses** , **Time** , or **Recalls**.</span></span>
2. <span data-ttu-id="dc223-115">Her onayı inceleyin ve onaylamak istediklerinizi seçin.</span><span class="sxs-lookup"><span data-stu-id="dc223-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="dc223-116">Seçili girişleri onaylamak için **Onayla** 'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="dc223-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="dc223-117">Sistem bu girişleri işler ve gerçek değerler ya da bir ayırma işlemi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dc223-117">The system will process these entries and create actuals or a booking.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="dc223-118">Girişi reddetme</span><span class="sxs-lookup"><span data-stu-id="dc223-118">Reject an entry</span></span>
<span data-ttu-id="dc223-119">Projeyi onaylayan olarak, bir girişi düzeltmesi için kullanıcıya tekrar göndermeniz gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="dc223-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="dc223-120">**Onaylar** formuna gidin ve reddedilecek girişi seçin.</span><span class="sxs-lookup"><span data-stu-id="dc223-120">Go to the **Approvals** form and select the entry to reject.</span></span> 
2. <span data-ttu-id="dc223-121">**Reddet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="dc223-121">Select **Reject**.</span></span>
3. <span data-ttu-id="dc223-122">İsteğe Bağlı: Girişin reddedilme nedeni hakkında kullanıcıyı bilgilendirmek için **Reddetme Yorumları** iletişim kutusuna bir yorum ekleyin.</span><span class="sxs-lookup"><span data-stu-id="dc223-122">Optional - Add a comment in the **Rejection Comments** dialog to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="dc223-123">**Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="dc223-123">Select **OK**.</span></span> <span data-ttu-id="dc223-124">Giriş kullanıcıya geri gönderilir.</span><span class="sxs-lookup"><span data-stu-id="dc223-124">The entry will be returned to the user.</span></span>
  
## <a name="recall-entries"></a><span data-ttu-id="dc223-125">Girişleri geri çağırma</span><span class="sxs-lookup"><span data-stu-id="dc223-125">Recall entries</span></span>
<span data-ttu-id="dc223-126">Bir noktada, gönderilen bir girişi geri çağırmanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="dc223-126">At some point, you might need to recall a submitted entry.</span></span> <span data-ttu-id="dc223-127">Giriş onaylanmadıysa hemen geri gönderilir.</span><span class="sxs-lookup"><span data-stu-id="dc223-127">If the entry has not been approved, it will be returned immediately.</span></span> <span data-ttu-id="dc223-128">Ancak onaylanmış bir giriş önemli bir etkiye neden olabilir.</span><span class="sxs-lookup"><span data-stu-id="dc223-128">An approved entry however, may have a material impact.</span></span> <span data-ttu-id="dc223-129">Projeyi onaylayanın, Gerçek Değerler'de işlemi geri almak için geri çağırmayı onaylaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="dc223-129">The Project approver is required to approve the recall in order to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="dc223-130">Projeyi onaylayanları belirleme</span><span class="sxs-lookup"><span data-stu-id="dc223-130">Specify Project approvers</span></span>
<span data-ttu-id="dc223-131">Her projede birkaç proje takımı üyesi vardır.</span><span class="sxs-lookup"><span data-stu-id="dc223-131">Each project has a number of project team members.</span></span> <span data-ttu-id="dc223-132">Takım üyelerinden hangilerinin aynı zamanda Projeyi onaylayanlar olacağını belirleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dc223-132">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="dc223-133">**Projeler** formuna gidin ve listeden projeyi açın.</span><span class="sxs-lookup"><span data-stu-id="dc223-133">Go to the **Projects** form and open the project from the list.</span></span>
2. <span data-ttu-id="dc223-134">**Takım** sekmesinde, Projeyi onaylayan olacak takım üyesini belirleyin ve ardından **Düzenle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="dc223-134">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="dc223-135">**Projeyi Onaylayan** alanını **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="dc223-135">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="dc223-136">**Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="dc223-136">Select **Save**.</span></span>
5. <span data-ttu-id="dc223-137">Başka Projeyi onaylayanlar eklemek için 2-4 arası adımları tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="dc223-137">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="dc223-138">Kullanıcının yöneticisini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="dc223-138">Configure the user's manager</span></span>

1. <span data-ttu-id="dc223-139">**Ayarlar** > **Güvenlik** > **Kullanıcılar** 'a gidin.</span><span class="sxs-lookup"><span data-stu-id="dc223-139">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="dc223-140">Yönetici olarak atayacağınız kullanıcıyı seçin ve **Kuruluş Bilgileri** alanında, listeden yöneticiyi seçin.</span><span class="sxs-lookup"><span data-stu-id="dc223-140">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="dc223-141">**Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="dc223-141">Select **Save**.</span></span>

