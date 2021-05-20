---
title: Bekleyen satıcı faturası kullanarak stoğu tutulmayan malzemeleri satın alma
description: Bu konu, beklemedeki satıcı faturalarının nasıl kaydedilecek açıklanmaktadır.
author: sigitac
manager: tfehr
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7a706f419443dcdf92ce3b247d719943272907d0
ms.sourcegitcommit: 7468d668c48c1d87934aab9a034decd51e56dec6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880694"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a><span data-ttu-id="09d86-103">Bekleyen satıcı faturası kullanarak stoğu tutulmayan malzemeleri satın alma</span><span class="sxs-lookup"><span data-stu-id="09d86-103">Purchase non-stocked materials using a pending vendor invoice</span></span>

<span data-ttu-id="09d86-104">_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="09d86-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="09d86-105">Bir proje için bir şirket için stoklanmayan malzemeleri hazırlarken maliyetler projeye yönelik olarak hemen kaydedilebilir.</span><span class="sxs-lookup"><span data-stu-id="09d86-105">As a company procures non-stocked materials for a project, the costs can be immediately recorded against the project.</span></span> 

<span data-ttu-id="09d86-106">Örneğin, Contoso Robotics ABD, donanım yenileme projesi gerçekleştiriyor ve yazılım lisanslarına ihtiyacı var.</span><span class="sxs-lookup"><span data-stu-id="09d86-106">For example, Contoso Robotics US is performing an equipment renewal project and needs software licenses.</span></span> <span data-ttu-id="09d86-107">Bu lisanslar, üçüncü taraf bir satıcıdan tedarik ediliyor.</span><span class="sxs-lookup"><span data-stu-id="09d86-107">These licenses are procured from a third-party vendor.</span></span>  <span data-ttu-id="09d86-108">Dynamics 365 Finance Uygulamasını kullanarak borç hesapları memuru bir bekleyen satıcı fatura belgesini kaydeder ve donanım yenileme projesine doğrudan lisans maliyetlerini ekler.</span><span class="sxs-lookup"><span data-stu-id="09d86-108">Using Dynamics 365 Finance, the Accounts payable clerk records a pending vendor invoice document and attributes the license costs directly against the equipment renewal project.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="09d86-109">Bu konu açıklanan işlevleri kullanmadan önce gerekli yapılandırmaları gözden geçirin ve uygulayın.</span><span class="sxs-lookup"><span data-stu-id="09d86-109">Before you use the functionality described in this topic, review and apply the required configurations.</span></span> <span data-ttu-id="09d86-110">Daha fazla bilgi için bkz. [Stoklanmayan malzemeleri ve bekleyen satıcı faturalarını etkinleştirme](configure-materials-nonstocked.md).</span><span class="sxs-lookup"><span data-stu-id="09d86-110">For more information, see [Enable non-stocked materials and pending vendor invoices](configure-materials-nonstocked.md).</span></span> 

## <a name="post-a-project-related-pending-vendor-invoice"></a><span data-ttu-id="09d86-111">Projeyle ilgili bir bekleyen satıcı faturasını deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="09d86-111">Post a project-related pending vendor invoice</span></span> 

<span data-ttu-id="09d86-112">Bekleyen satıcı faturaları, **bekleyen satıcı faturaları** sayfasında (**Borç hesapları** > **faturalar** > **bekleyen satıcı faturaları**) kaydedilebilir.</span><span class="sxs-lookup"><span data-stu-id="09d86-112">Pending vendor invoices can be recorded on the **Pending vendor invoices** page (**Accounts payable** > **Invoices** > **Pending vendor invoices**).</span></span> <span data-ttu-id="09d86-113">Projeyle ilgili bekleyen satıcı faturasını deftere nakletmek için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="09d86-113">Complete the following steps to post a project-related pending vendor invoice:</span></span>

1. <span data-ttu-id="09d86-114">**Borç hesapları** > **faturalar**'a gidin ve **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="09d86-114">Go to **Accounts payable** > **Invoices** and select **New**.</span></span> 
2. <span data-ttu-id="09d86-115">**Fatura hesabı** alanında bir satıcı seçin ve **numara** alanına satıcı fatura tanımlamasını girin.</span><span class="sxs-lookup"><span data-stu-id="09d86-115">In the **Invoice account** field, select a vendor and in the **Number** field, enter the vendor invoice identification.</span></span>
3. <span data-ttu-id="09d86-116">Satıcı faturasına bir satır ekleyin ve **madde numarası** alanında, satıcıdan satın alınan Stoklanmayan maddeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="09d86-116">Add a line to the vendor invoice and in the **Item number** field, select the non-stocked item purchased from the vendor.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="09d86-117">Bir satın alma kategorisine dayanan satıcı fatura satırları projeye karşı kaydedilemez.</span><span class="sxs-lookup"><span data-stu-id="09d86-117">Vendor invoice lines that are based on a procurement category can't be recorded against the project.</span></span> 
    
5. <span data-ttu-id="09d86-118">Satın alınan miktarı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="09d86-118">Add the quantity purchased.</span></span> <span data-ttu-id="09d86-119">Sistem birim fiyatı, Stoklanmayan madde fiyatı yapılandırmasını temel alarak dolduracaktır.</span><span class="sxs-lookup"><span data-stu-id="09d86-119">The system will populate the unit price based on the non-stocked item price configuration.</span></span> 
6. <span data-ttu-id="09d86-120">Satırdaki toplam tutarı ve diğer gerekli ayrıntıları doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="09d86-120">Verify the total amount and other required details on the line.</span></span>
7. <span data-ttu-id="09d86-121">Satır ayrıntılarında **Proje** sekmesinde, bu öğenin kaydedileceği projenin kimliğini seçin.</span><span class="sxs-lookup"><span data-stu-id="09d86-121">On the line details, on the **Project** tab, select the ID of the project that this item will be recorded to.</span></span>
8. <span data-ttu-id="09d86-122">İsteğe bağlı olarak, aktivite numarasını seçin ve proje kategorisi ve satır özelliğini güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="09d86-122">Optionally, select the activity number, and update the project category and line property.</span></span>
9. <span data-ttu-id="09d86-123">Bekleyen satıcı faturasını deftere nakledin.</span><span class="sxs-lookup"><span data-stu-id="09d86-123">Post pending vendor invoice.</span></span> <span data-ttu-id="09d86-124">Fatura deftere nakledildiğinde, sistem kayıtları:</span><span class="sxs-lookup"><span data-stu-id="09d86-124">When the invoice is posted, the system records:</span></span>
    
    - <span data-ttu-id="09d86-125">Satıcı bakiye tutarı.</span><span class="sxs-lookup"><span data-stu-id="09d86-125">The vendor balance amount.</span></span>
    - <span data-ttu-id="09d86-126">Satış Vergisi Tutarı.</span><span class="sxs-lookup"><span data-stu-id="09d86-126">The sales tax amount.</span></span>
    - <span data-ttu-id="09d86-127">Projeye yönelik maliyet, satın alma entegrasyonu hesabına kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="09d86-127">The cost against the project is recorded to the procurement integration account.</span></span>
    - <span data-ttu-id="09d86-128">Dataverse'de projenin fiili işlemi.</span><span class="sxs-lookup"><span data-stu-id="09d86-128">The project actual transaction in Dataverse.</span></span> <span data-ttu-id="09d86-129">Bu işlem [Project Operations tümleştirme günlüğü](../project-accounting/project-operations-integration-journal.md) kullanılarak daha sonra işlenir.</span><span class="sxs-lookup"><span data-stu-id="09d86-129">This transaction is further processed using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="09d86-130">Bu günlüğün deftere nakledilmesi, satın alma entegrasyonu hesabındaki tutarı proje maliyet hesabına taşır.</span><span class="sxs-lookup"><span data-stu-id="09d86-130">Posting this journal moves the amount from the procurement integration account to the project cost account.</span></span>
