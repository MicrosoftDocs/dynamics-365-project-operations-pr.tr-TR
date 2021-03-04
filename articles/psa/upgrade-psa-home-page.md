---
title: Yükseltme giriş sayfası
description: Bu konu, Dynamics 365 Project Service Automation uygulamasındaki yeni ve değiştirilen özellikler hakkında önemli bilgileri nerede bulabileceğinizi ve en yeni sürüme yükseltme işlemini gösterir.
manager: kfend
ms.prod: ''
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
author: rumant
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e30da3a5ade6d8bafcdc45801b830196841997bf
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150107"
---
# <a name="upgrade-home-page"></a><span data-ttu-id="0cd3b-103">Yükseltme giriş sayfası</span><span class="sxs-lookup"><span data-stu-id="0cd3b-103">Upgrade home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a><span data-ttu-id="0cd3b-104">PSA sürüm 2.x veya 1.x'ten sürüm 3.x'e yükseltme</span><span class="sxs-lookup"><span data-stu-id="0cd3b-104">Upgrade from PSA version 2.x or 1.x to version 3.x</span></span>

### <a name="new-instances"></a><span data-ttu-id="0cd3b-105">Yeni kurulumlar</span><span class="sxs-lookup"><span data-stu-id="0cd3b-105">New instances</span></span>

<span data-ttu-id="0cd3b-106">17 Mayıs 2019 tarihinden itibaren yeni kurulum hazırlanırken Project Service Automation seçildiğinde sürüm 3.x varsayılan olarak yüklenir.</span><span class="sxs-lookup"><span data-stu-id="0cd3b-106">As of May 17, 2019, when Project Service Automation is selected during the provisioning of a new instance, version 3.x is installed by default.</span></span>

### <a name="existing-instances"></a><span data-ttu-id="0cd3b-107">Var olan kurulumlar</span><span class="sxs-lookup"><span data-stu-id="0cd3b-107">Existing instances</span></span>

<span data-ttu-id="0cd3b-108">Daha önce, PSA sürüm 2.x kurulumuna sahip olan ve PSA'nın Birleşik istemci arabirimi tabanlı (UCI) sürümü olan sürüm 3.x'e yükseltmesi gereken müşterilerin, Microsoft Desteği'ne başvurması ve kurulumlarının ayrıntılarını sağlamaları gerekir. Böylece destek, kurulumu sürüm 3.x'e yükseltmek için etkinleştirebilir.</span><span class="sxs-lookup"><span data-stu-id="0cd3b-108">Previously, customers who have an instance of PSA version 2.x and needed to upgrade to version 3.x, which is the Unified client interface-based (UCI) version of PSA, had to contact Microsoft Support and provide the details of their instance so that support could enable the instance for upgrade to version 3.x.</span></span> <span data-ttu-id="0cd3b-109">1 Mart 2020 tarihinden itibaren, PSA sürüm 2.x kurulumuna sahip olan ve PSA'nın Birleşik istemci arabirimi tabanlı (UCI) sürümü olan sürüm 3.x'e yükseltmesi gereken müşteriler, Microsoft Desteği'ne başvurmak zorunda kalmadan kurulumlarını doğrudan Yönetici portalından yükseltebilir.</span><span class="sxs-lookup"><span data-stu-id="0cd3b-109">As of March 1, 2020, customers who have an instance of PSA version 2.x and need to upgrade to version 3.x, will able to upgrade their instances directly from the Admin portal without having to contact Microsoft Support.</span></span>  

> [!NOTE]
> <span data-ttu-id="0cd3b-110">PSA sürüm 3. x önemli değişiklikler içerir.</span><span class="sxs-lookup"><span data-stu-id="0cd3b-110">PSA version 3.x includes significant changes.</span></span> <span data-ttu-id="0cd3b-111">Daha iyi bir kullanıcı deneyimi sağlamaya yardımcı olmak için Birleşik Arabirim çerçevesi üzerine kurulmuştur.</span><span class="sxs-lookup"><span data-stu-id="0cd3b-111">It has been built on the Unified Interface framework to help provide an improved user experience.</span></span> <span data-ttu-id="0cd3b-112">Yeniden tasarlanan uygulama tutarlı, tek tip bir kullanıcı arabirimi (UI) sağlar ve tüm ekran boyutlarında veya cihazlarda en iyi görüntüleme için dinamik tasarım ilkelerini takip eder.</span><span class="sxs-lookup"><span data-stu-id="0cd3b-112">The redesigned app delivers a consistent, uniform user interface (UI), and it follows responsive design principles for optimal viewing on any screen size or device.</span></span> <span data-ttu-id="0cd3b-113">Uygulamanın tamamında başka değişiklikler de yapılmıştır.</span><span class="sxs-lookup"><span data-stu-id="0cd3b-113">There have been other changes throughout the application.</span></span> <span data-ttu-id="0cd3b-114">Değiştirilen bazı alanlar arasında fiyatlandırma, kaynak ayırma ve atama, zaman, giderler ve onaylar verilebilir.</span><span class="sxs-lookup"><span data-stu-id="0cd3b-114">Some of the areas that have been changed include pricing, booking and assigning resources, time, expenses, and approvals.</span></span>

<span data-ttu-id="0cd3b-115">Yükseltme işlemini başlatmadan önce aşağıdaki görevleri tamamlamanızı öneririz:</span><span class="sxs-lookup"><span data-stu-id="0cd3b-115">Before you begin the upgrade process, we recommend that you complete the following tasks:</span></span>

- <span data-ttu-id="0cd3b-116">Dynamics 365 Field Service ve Project Service Automation uygulamalarının tanımlanmış kurulumda yüklü olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="0cd3b-116">Verify whether both Dynamics 365 Field Service and Project Service Automation are installed on the identified instance.</span></span> <span data-ttu-id="0cd3b-117">Her iki çözüm de yüklüyse, kurulumun düzenli olarak kullanımını sürdürmeden önce yükseltmeyi planlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="0cd3b-117">If both solutions are installed, you should plan to upgrade both before you resume regular use of the instance.</span></span>
- <span data-ttu-id="0cd3b-118">Aşağıdaki konuları dikkatle gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="0cd3b-118">Carefully review the following topics.</span></span> <span data-ttu-id="0cd3b-119">Sürümler arasındaki değişiklikleri tanımak ve anlamak, yükseltme işleminde yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="0cd3b-119">Awareness and understanding of the changes between versions will help you with the upgrade process.</span></span> <span data-ttu-id="0cd3b-120">Bu konular sürümünüzü 3.x'e yükseltmeyi planlarken dikkate almanız gereken hususlar ve önerilerle birlikte PSA'daki önemli değişiklikler hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="0cd3b-120">These topics provide information about the major changes in PSA, together with considerations and recommendations for planning your upgrade to version 3.x.</span></span>

    - [<span data-ttu-id="0cd3b-121">Project Service Automation sürüm 3'teki yenilikler veya değişiklikler</span><span class="sxs-lookup"><span data-stu-id="0cd3b-121">What's new or changed in Project Service Automation version 3</span></span>](whats-new-changed-v3.md)
    - [<span data-ttu-id="0cd3b-122">Yükseltme hususları - Project Service Automation sürüm 2.x veya 1.x'den sürüm 3'e</span><span class="sxs-lookup"><span data-stu-id="0cd3b-122">Upgrade considerations - Project Service Automation version 2.x or 1.x to version 3</span></span>](upgrade-v3.md)

- <span data-ttu-id="0cd3b-123">Üretim kurulumunuzu yükseltmeden önce uygulamanızdaki değişiklikleri değerlendirmek için korumalı alan kurulumunuzu yükseltin.</span><span class="sxs-lookup"><span data-stu-id="0cd3b-123">Upgrade your sandbox instance to evaluate the changes in your implementation before you upgrade your production instance.</span></span>

<span data-ttu-id="0cd3b-124">Daha önce sözü edilen konuları inceledikten sonra ve PSA sürüm 3.x'e veya UCI tabanlı sürüme yükseltmeye hazır olduğunuzda Yönetim merkezinde kullanılabilir yükseltmeyi yapmak için Microsoft destek birimine bir istek gönderin.</span><span class="sxs-lookup"><span data-stu-id="0cd3b-124">After you've reviewed the topics that were mentioned earlier and are ready to upgrade to PSA version 3.x or the UCI-based version, submit a request to Microsoft support to make the upgrade available from Admin center.</span></span> <span data-ttu-id="0cd3b-125">İsteğinize kurulumun ayrıntılarını ekleyin.</span><span class="sxs-lookup"><span data-stu-id="0cd3b-125">In your request, provide the details of your instance.</span></span>

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a><span data-ttu-id="0cd3b-126">Yeni oluşturulmuş kurulumunda PSA'nın eski sürümleri (PSA sürüm 2.x)</span><span class="sxs-lookup"><span data-stu-id="0cd3b-126">Older versions of PSA (PSA version 2.x) in a newly created instance</span></span>

<span data-ttu-id="0cd3b-127">17 Mayıs 2019 tarihinden itibaren tüm yeni kurulumlarda varsayılan istemci olarak UCI bulunacaktır.</span><span class="sxs-lookup"><span data-stu-id="0cd3b-127">As of May 17, 2019, all new instances will have UCI as the default client.</span></span> <span data-ttu-id="0cd3b-128">Bu değişikliğe uyum sağlamak üzere bu sürümler UCI istemcisiyle çalışacak şekilde tasarlandığından PSA sürüm 3.x ve Field Service sürüm 8.x varsayılan olarak sağlanacaktır.</span><span class="sxs-lookup"><span data-stu-id="0cd3b-128">For alignment with this change, PSA version 3.x and Field Service version 8.x will be provisioned by default, because these versions are designed to work with the UCI client.</span></span>

<span data-ttu-id="0cd3b-129">1 Mart 2020 tarihinden itibaren, Dynamics PSA müşterileri artık PSA'nın eski sürümleriyle (örneğin, PSA sürüm 2.x veya önceki) yeni bir ortam oluşturamaz.</span><span class="sxs-lookup"><span data-stu-id="0cd3b-129">Starting March 1, 2020, customers of Dynamics PSA will no longer be able to create a new environment with older versions of PSA, for example PSA version 2.x or lower.</span></span> <span data-ttu-id="0cd3b-130">Her yeni ortam, yalnızca PSA 3.x sürümü ile oluşturulabilecek.</span><span class="sxs-lookup"><span data-stu-id="0cd3b-130">Any new environment will be to get only version 3.x of PSA.</span></span>

> [!NOTE]
> <span data-ttu-id="0cd3b-131">Field Service ve PSA uygulamalarının eski sürümlerini kullanırken en iyi deneyim için bu sürümler UCI'de düzgün yüklenecek şekilde tasarlanmadığından **Sistem ayarları** sayfasına gidin ve **Yalnızca yeni Birleşik Arabirim'i kullan (önerilen)** alanı için **Hayır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="0cd3b-131">For the best experience when you use older versions of the Field Service and PSA applications, go to the **System settings** page and for the field, **Use the new Unified Interface only (recommended)** field, select **No** as these versions aren't designed to be correctly loaded in UCI.</span></span> <span data-ttu-id="0cd3b-132">UCI'yi kapattıktan sonra Field Service ve PSA'nın bu sürümlerini eski web istemcisini kullanarak açabilir ve çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0cd3b-132">After you have turned off UCI, you can open and run these versions of Field Service and PSA by using the old web client.</span></span> 
