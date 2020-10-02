---
title: Otomatik fatura oluşturmayı yapılandırma
description: Bu konu, sistemi otomatik olarak faturaları oluşturmak üzere yapılandırmak ile ilgili bilgi sağlar.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 764fd4568619e4f5676ee3cbf7fce14ffb069548
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898150"
---
# <a name="configure-automated-invoice-creation"></a><span data-ttu-id="43258-103">Otomatik fatura oluşturmayı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="43258-103">Configure automated invoice creation</span></span>

<span data-ttu-id="43258-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="43258-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="43258-105">Proje Operations'da otomatik bir fatura çalıştırması yapılandırmak için aşağıdaki adımları uygulayın.</span><span class="sxs-lookup"><span data-stu-id="43258-105">Complete the following steps to configure an automated invoice run in Project operations.</span></span>

1. <span data-ttu-id="43258-106">**Ayarlar** \> **Toplu işler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="43258-106">Go to **Settings** \> **Batch jobs**.</span></span>
2. <span data-ttu-id="43258-107">Bir toplu iş oluşturun ve **Project operations fatura oluştur** olarak adlandırın.</span><span class="sxs-lookup"><span data-stu-id="43258-107">Create a batch job, and name it **Project operations create invoices**.</span></span> <span data-ttu-id="43258-108">Toplu işin adı "faturaları oluştur" terimini içermelidir.</span><span class="sxs-lookup"><span data-stu-id="43258-108">The name of the batch job must include the term "create invoices."</span></span>
3. <span data-ttu-id="43258-109">**İş türü** alanında **Hiçbiri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="43258-109">In the **Job type** field, select **None**.</span></span> <span data-ttu-id="43258-110">Varsayılan olarak, **Günlük Sıklık**ve **Etkin** seçenekleri **Evet** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="43258-110">By default, the **Frequency Daily** and **Is Active** options are set to **Yes**.</span></span>
4. <span data-ttu-id="43258-111">**İş Akışı Çalıştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="43258-111">Select **Run Workflow**.</span></span> <span data-ttu-id="43258-112">**Kayıt Ara** iletişim kutusunda üç iş akışı görürsünüz:</span><span class="sxs-lookup"><span data-stu-id="43258-112">In the **Look Up Record** dialog box, you will see three workflows:</span></span>

    - <span data-ttu-id="43258-113">ProcessRunCaller</span><span class="sxs-lookup"><span data-stu-id="43258-113">ProcessRunCaller</span></span>
    - <span data-ttu-id="43258-114">ProcessRunner</span><span class="sxs-lookup"><span data-stu-id="43258-114">ProcessRunner</span></span>
    - <span data-ttu-id="43258-115">UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="43258-115">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="43258-116">**ProcessRunCaller**'ı ve ardından **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="43258-116">Select **ProcessRunCaller**, and then select **Add**.</span></span>
6. <span data-ttu-id="43258-117">Sonraki iletişim kutusunda **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="43258-117">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="43258-118">**Uyku** iş akışının ardından **Süreç** iş akışı gelir.</span><span class="sxs-lookup"><span data-stu-id="43258-118">A **Sleep** workflow is followed by a **Process** workflow.</span></span>

    <span data-ttu-id="43258-119">Ayrıca, adım 5'te **ProcessRunner**'ı seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="43258-119">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="43258-120">Ardından **Tamam**'ı seçtiğinizde, bir **Süreç** iş akışının ardından bir **Uyku** iş akışı gelir.</span><span class="sxs-lookup"><span data-stu-id="43258-120">Then, when you select **OK**, a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="43258-121">**ProcessRunCaller** ve **ProcessRunner** iş akışları faturaları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="43258-121">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="43258-122">**ProcessRunCaller** **ProcessRunner**'ı çağırır.</span><span class="sxs-lookup"><span data-stu-id="43258-122">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="43258-123">**ProcessRunner**, faturaları gerçekte oluşturan iş akışıdır.</span><span class="sxs-lookup"><span data-stu-id="43258-123">**ProcessRunner** is the workflow that actually creates the invoices.</span></span> <span data-ttu-id="43258-124">Bu, fatura oluşturulması için gereken tüm sözleşme satırlarından geçer ve bu satırlar için faturalar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="43258-124">It goes through all the contract lines that invoices must be created for, and it creates invoices for those lines.</span></span> <span data-ttu-id="43258-125">Faturaların oluşturulması gereken sözleşme satırlarını belirlemek için, iş sözleşme satırları için fatura çalıştırma tarihlerine bakar.</span><span class="sxs-lookup"><span data-stu-id="43258-125">To determine the contract lines that invoices must be created for, the job looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="43258-126">Bir sözleşmeye ait olan sözleşme satırları aynı fatura çalıştırma tarihine sahipse, işlemler iki fatura satırı bulunan tek bir faturada birleştirilir.</span><span class="sxs-lookup"><span data-stu-id="43258-126">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="43258-127">Fatura oluşturulacak bir işlem yoksa, iş fatura oluşturmayı atlar.</span><span class="sxs-lookup"><span data-stu-id="43258-127">If there are no transactions to create invoices for, the job skips invoice creation.</span></span>

<span data-ttu-id="43258-128">**ProcessRunner** çalışması bittikten sonra, **ProcessRunCaller** öğesini çağırır, bitiş saati sağlar ve kapatılır.</span><span class="sxs-lookup"><span data-stu-id="43258-128">After **ProcessRunner** has finished running, it calls **ProcessRunCaller**, provides the end time, and is closed.</span></span> <span data-ttu-id="43258-129">**ProcessRunCaller** daha sonra belirtilen bitiş saatinden itibaren 24 saat çalışan bir zamanlayıcı başlatır.</span><span class="sxs-lookup"><span data-stu-id="43258-129">**ProcessRunCaller** then starts a timer that runs for 24 hours from the specified end time.</span></span> <span data-ttu-id="43258-130">Zamanlayıcının sonunda **ProcessRunCaller** kapatılır.</span><span class="sxs-lookup"><span data-stu-id="43258-130">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="43258-131">Fatura oluşturmaya yönelik toplu iş yinelenen bir iştir.</span><span class="sxs-lookup"><span data-stu-id="43258-131">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="43258-132">Bu toplu iş birçok defa çalıştırılırsa, işin birden çok kopyası oluşturulur ve hatalara yol açar.</span><span class="sxs-lookup"><span data-stu-id="43258-132">If this batch process is run many times, multiple instances of the job are created and cause errors.</span></span> <span data-ttu-id="43258-133">Bu nedenle, toplu işi yalnızca bir kez başlatmanız gerekir ve yalnızca çalışmayı durdurduğunda yeniden başlatılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="43258-133">Therefore, you should start the batch process only one time, and you should restart it only if it stops running.</span></span>

> [!NOTE]
> <span data-ttu-id="43258-134">Toplu faturalama yalnızca fatura zamanlamalarında yapılandırılan proje sözleşme satırlarında çalışır.</span><span class="sxs-lookup"><span data-stu-id="43258-134">Batch invoicing only runs for project contract lines that are configured by invoice schedules.</span></span> <span data-ttu-id="43258-135">Sabit fiyatlı fatura yöntemine sahip bir sözleşme satırının kilometre taşları yapılandırılmış olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="43258-135">A contract line with a fixed price billing method must have milestones configured.</span></span> <span data-ttu-id="43258-136">Zaman ve malzeme faturalama yöntemi içeren bir proje sözleşmesi satırı, ayarlanmış bir tarih tabanlı fatura çizelgesine gereksinim duyar.</span><span class="sxs-lookup"><span data-stu-id="43258-136">A project contract line with a time and material billing method will need a date-based invoice schedule set up.</span></span> <span data-ttu-id="43258-137">Aynı şekilde, proje tabanlı bir sözleşme satırı için de geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="43258-137">The same applies to a project-based contract line.</span></span>     
