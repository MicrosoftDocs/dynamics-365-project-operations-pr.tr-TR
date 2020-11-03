---
title: Dağıtım türünüzü belirleme
description: Bu konuda, şirketiniz için doğru Project Operations dağıtım türünü belirlemenize yardımcı olacak bilgiler sağlanmaktadır.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 564f2878553fe3904a7c47c7e80a3b57c763a3b2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086328"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="6cc99-103">Dağıtım türünüzü belirleme</span><span class="sxs-lookup"><span data-stu-id="6cc99-103">Determine your deployment type</span></span>

<span data-ttu-id="6cc99-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="6cc99-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6cc99-105">Lisansı satın aldıktan sonra, [Destekli yükleme akışını](https://aka.ms/provisionprojectoperations) kullanarak en iyi Dynamics 365 Project Operations dağıtım modelini belirlemeye başlayın.</span><span class="sxs-lookup"><span data-stu-id="6cc99-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="6cc99-106">Destekli yükleme akışını tamamladıktan sonra, yükleme işleminizi tamamlamak üzere doğru yönetim portalına yönlendirilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6cc99-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="6cc99-107">Yüklemeyi tamamlamak için aşağıdaki dağıtım ayrıntılarına bakın.</span><span class="sxs-lookup"><span data-stu-id="6cc99-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="6cc99-108">Dynamics 365 Project Service Automation kullanan mevcut Dynamics müşterileri</span><span class="sxs-lookup"><span data-stu-id="6cc99-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="6cc99-109">Project Operations, Project Service Automation ile birlikte gönderilen özellikleri içerir.</span><span class="sxs-lookup"><span data-stu-id="6cc99-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="6cc99-110">Gelecekte bu müşteriler için bir yükseltme yolu yayımlanacaktır.</span><span class="sxs-lookup"><span data-stu-id="6cc99-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="6cc99-111">Proje yönetimi ve muhasebe kullanan mevcut Dynamics 365 Finance müşterileri</span><span class="sxs-lookup"><span data-stu-id="6cc99-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="6cc99-112">Proje yönetimi ve muhasebe işlevini kullanan mevcut Finance müşterileri bu işlevi olduğu gibi kullanmaya devam edebilir.</span><span class="sxs-lookup"><span data-stu-id="6cc99-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use this as is.</span></span> <span data-ttu-id="6cc99-113">Bkz. [Stoklu/üretim siparişi senaryoları için Project Operations](#pma).</span><span class="sxs-lookup"><span data-stu-id="6cc99-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="6cc99-114">Dağıtım türleri</span><span class="sxs-lookup"><span data-stu-id="6cc99-114">Deployment types</span></span>
<span data-ttu-id="6cc99-115">Project Operations gereksinimlerinize uygun birden çok dağıtım seçeneğini destekler.</span><span class="sxs-lookup"><span data-stu-id="6cc99-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="6cc99-116">İster yeni ister eski bir Dynamics 365 müşterisi olun, Project Operations ihtiyaçlarınızı destekleyebilir.</span><span class="sxs-lookup"><span data-stu-id="6cc99-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="6cc99-117">[Dağıtım anketimiz](https://aka.ms/provisionprojectoperations) doğru dağıtımı belirlemenize yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="6cc99-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="6cc99-118">Sonuçlar sizi aşağıdaki dağıtım türlerinden birine yönlendirir:</span><span class="sxs-lookup"><span data-stu-id="6cc99-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="6cc99-119">Lite dağıtımı: Anlaşmadan proforma faturaya</span><span class="sxs-lookup"><span data-stu-id="6cc99-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="6cc99-120">Kaynağı/stoğu tutulmayanlara ait senaryolar için Project Operations</span><span class="sxs-lookup"><span data-stu-id="6cc99-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="6cc99-121">Stoklu/üretim siparişi senaryoları için Project Operations</span><span class="sxs-lookup"><span data-stu-id="6cc99-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="6cc99-122">Project Operations, tüzel kişilik düzeyindeki yapılandırmalar aracılığıyla aynı ortamda stoklu/üretim siparişi senaryolarını ve stoğu tutulmayan/kaynak tabanlı senaryoları destekler.</span><span class="sxs-lookup"><span data-stu-id="6cc99-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="6cc99-123">Örneğin, Contoso ABD üretim olanaklarındaki (yasal varlık = Contoso Manufacturing ABD) stoklarındaki stoğu/üretim emri yeteneklerini kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="6cc99-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="6cc99-124">Contoso, Stoklanmayan/kaynak tabanlı özelliklerini ABD 'deki Contoso Robotics Arms (yasal varlık = Contoso Robotics Birleşik Krallık) içinde kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="6cc99-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="6cc99-125">Lite dağıtımı: anlaşmadan proforma faturaya</span><span class="sxs-lookup"><span data-stu-id="6cc99-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="6cc99-126">Lite dağıtımı aşağıdaki özellikleri içerir:</span><span class="sxs-lookup"><span data-stu-id="6cc99-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="6cc99-127">Web için Microsoft Project kullanarak proje planlama</span><span class="sxs-lookup"><span data-stu-id="6cc99-127">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="6cc99-128">Çok boyutlu fiyatlandırma</span><span class="sxs-lookup"><span data-stu-id="6cc99-128">Multi-dimensional pricing</span></span>
- <span data-ttu-id="6cc99-129">Birleşik Kaynak Yönetimi</span><span class="sxs-lookup"><span data-stu-id="6cc99-129">Unified Resource Management</span></span>
- <span data-ttu-id="6cc99-130">Zaman İzleme</span><span class="sxs-lookup"><span data-stu-id="6cc99-130">Time Tracking</span></span>
- <span data-ttu-id="6cc99-131">Temel Gider</span><span class="sxs-lookup"><span data-stu-id="6cc99-131">Basic Expense</span></span>
- <span data-ttu-id="6cc99-132">Fatura Teklifi</span><span class="sxs-lookup"><span data-stu-id="6cc99-132">Invoice Proposal</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="6cc99-133">Dağıtım adımları</span><span class="sxs-lookup"><span data-stu-id="6cc99-133">Deployment steps</span></span>
<span data-ttu-id="6cc99-134">[Dağıtım anketini](https://aka.ms/provisionprojectoperations) kullanarak en iyi Project Operations dağıtım yöntemini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="6cc99-134">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="6cc99-135">Bu dağıtım için bkz. [Önizleme aboneliğine kaydolma](lite-preview-subscription-sign-up.md) ve [Yeni ortam sağlama](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="6cc99-135">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="6cc99-136">Kaynağı/stoğu tutulmayanlara ait senaryolar için Project Operations</span><span class="sxs-lookup"><span data-stu-id="6cc99-136">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="6cc99-137">Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations aşağıdaki özellikleri içerir:</span><span class="sxs-lookup"><span data-stu-id="6cc99-137">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="6cc99-138">Web için Microsoft Project kullanarak proje planlama</span><span class="sxs-lookup"><span data-stu-id="6cc99-138">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="6cc99-139">Çok boyutlu fiyatlandırma</span><span class="sxs-lookup"><span data-stu-id="6cc99-139">Multi-dimensional pricing</span></span>
- <span data-ttu-id="6cc99-140">Birleşik Kaynak Yönetimi</span><span class="sxs-lookup"><span data-stu-id="6cc99-140">Unified Resource Management</span></span>
- <span data-ttu-id="6cc99-141">Zaman İzleme</span><span class="sxs-lookup"><span data-stu-id="6cc99-141">Time Tracking</span></span>
- <span data-ttu-id="6cc99-142">Temel Gider</span><span class="sxs-lookup"><span data-stu-id="6cc99-142">Basic Expense</span></span>
- <span data-ttu-id="6cc99-143">Tam Gider</span><span class="sxs-lookup"><span data-stu-id="6cc99-143">Full Expense</span></span>
- <span data-ttu-id="6cc99-144">Makbuz OCR'si</span><span class="sxs-lookup"><span data-stu-id="6cc99-144">Receipt OCR</span></span>
- <span data-ttu-id="6cc99-145">Tam Faturalama</span><span class="sxs-lookup"><span data-stu-id="6cc99-145">Full Invoicing</span></span>
- <span data-ttu-id="6cc99-146">Gelir Tanıma</span><span class="sxs-lookup"><span data-stu-id="6cc99-146">Revenue Recognition</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="6cc99-147">Dağıtım adımları</span><span class="sxs-lookup"><span data-stu-id="6cc99-147">Deployment steps</span></span>
<span data-ttu-id="6cc99-148">[Dağıtım anketini](https://aka.ms/provisionprojectoperations) kullanarak en iyi Project Operations dağıtım yöntemini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="6cc99-148">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="6cc99-149">Bu dağıtım için bkz. [Önizleme aboneliğine kaydolma](resource-sign-up-preview-subscription.md) ve [Yeni ortam sağlama](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="6cc99-149">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="6cc99-150">Stoklu/üretim siparişi senaryoları için Project Operations</span><span class="sxs-lookup"><span data-stu-id="6cc99-150">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="6cc99-151">İKY kullanarak proje planlama</span><span class="sxs-lookup"><span data-stu-id="6cc99-151">Project planning using WBS</span></span>
- <span data-ttu-id="6cc99-152">Kaynak Yönetimi</span><span class="sxs-lookup"><span data-stu-id="6cc99-152">Resource Management</span></span>
- <span data-ttu-id="6cc99-153">Zaman İzleme</span><span class="sxs-lookup"><span data-stu-id="6cc99-153">Time Tracking</span></span>
- <span data-ttu-id="6cc99-154">Tam Gider</span><span class="sxs-lookup"><span data-stu-id="6cc99-154">Full Expense</span></span>
- <span data-ttu-id="6cc99-155">Makbuz OCR'si</span><span class="sxs-lookup"><span data-stu-id="6cc99-155">Receipt OCR</span></span>
- <span data-ttu-id="6cc99-156">Tam Faturalama</span><span class="sxs-lookup"><span data-stu-id="6cc99-156">Full Invoicing</span></span>
- <span data-ttu-id="6cc99-157">Gelir Tanıma</span><span class="sxs-lookup"><span data-stu-id="6cc99-157">Revenue Recognition</span></span>
- <span data-ttu-id="6cc99-158">Üretim Siparişleri</span><span class="sxs-lookup"><span data-stu-id="6cc99-158">Production Orders</span></span>
- <span data-ttu-id="6cc99-159">Malzeme desteği</span><span class="sxs-lookup"><span data-stu-id="6cc99-159">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="6cc99-160">Dağıtım adımları</span><span class="sxs-lookup"><span data-stu-id="6cc99-160">Deployment steps</span></span>
<span data-ttu-id="6cc99-161">[Dağıtım anketini](https://aka.ms/provisionprojectoperations) kullanarak en iyi Project Operations dağıtım yöntemini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="6cc99-161">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="6cc99-162">Bu dağıtım için bkz. [Önizleme aboneliğine kaydolma](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) ve [Yeni ortam sağlama](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="6cc99-162">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

