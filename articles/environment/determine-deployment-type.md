---
title: Dağıtım türleri
description: Bu konuda, şirketiniz için doğru Project Operations dağıtım türünü belirlemenize yardımcı olacak bilgiler sağlanmaktadır.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949118"
---
# <a name="deployment-types"></a><span data-ttu-id="a1722-103">Dağıtım türleri</span><span class="sxs-lookup"><span data-stu-id="a1722-103">Deployment types</span></span>

<span data-ttu-id="a1722-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="a1722-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a1722-105">Lisansı satın aldıktan sonra, [Destekli yükleme akışını](https://aka.ms/provisionprojectoperations) kullanarak en iyi Dynamics 365 Project Operations dağıtım modelini belirlemeye başlayın.</span><span class="sxs-lookup"><span data-stu-id="a1722-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="a1722-106">Destekli yükleme akışını tamamladıktan sonra, yükleme işleminizi tamamlamak üzere doğru yönetim portalına yönlendirilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a1722-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="a1722-107">Yüklemeyi tamamlamak için aşağıdaki dağıtım ayrıntılarına bakın.</span><span class="sxs-lookup"><span data-stu-id="a1722-107">See the deployment details below to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="a1722-108">Dynamics 365 Project Service Automation kullanan mevcut Dynamics müşterileri</span><span class="sxs-lookup"><span data-stu-id="a1722-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="a1722-109">Project Operations, Project Service Automation ile birlikte gönderilen özellikleri içerir.</span><span class="sxs-lookup"><span data-stu-id="a1722-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="a1722-110">Gelecekte bu müşteriler için bir yükseltme yolu yayımlanacaktır.</span><span class="sxs-lookup"><span data-stu-id="a1722-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="a1722-111">Proje yönetimi ve muhasebe kullanan mevcut Dynamics 365 Finance müşterileri</span><span class="sxs-lookup"><span data-stu-id="a1722-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="a1722-112">Proje yönetimi ve muhasebe işlevini kullanan mevcut Finance müşterileri bu işlevi olduğu gibi kullanmaya devam edebilir.</span><span class="sxs-lookup"><span data-stu-id="a1722-112">Existing customers of Finance who use the Project management and accounting functionality can continue use this as is.</span></span> <span data-ttu-id="a1722-113">Bkz. [Stoklu/üretim siparişi senaryoları için Project Operations](#pma).</span><span class="sxs-lookup"><span data-stu-id="a1722-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>

<span data-ttu-id="a1722-114">Project Operations gereksinimlerinize uygun birden çok dağıtım seçeneğini destekler.</span><span class="sxs-lookup"><span data-stu-id="a1722-114">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="a1722-115">İster yeni ister eski bir Dynamics 365 müşterisi olun, Project Operations ihtiyaçlarınızı destekleyebilir.</span><span class="sxs-lookup"><span data-stu-id="a1722-115">Whether you are a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="a1722-116">[Dağıtım anketimiz](https://aka.ms/provisionprojectoperations) doğru dağıtımı belirlemenize yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="a1722-116">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="a1722-117">Sonuçlar sizi aşağıdaki dağıtım türlerinden birine yönlendirir:</span><span class="sxs-lookup"><span data-stu-id="a1722-117">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="a1722-118">Lite dağıtımı: Anlaşmadan proforma faturaya</span><span class="sxs-lookup"><span data-stu-id="a1722-118">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="a1722-119">Kaynağı/stoğu tutulmayanlara ait senaryolar için Project Operations</span><span class="sxs-lookup"><span data-stu-id="a1722-119">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="a1722-120">Stoklu/üretim siparişi senaryoları için Project Operations</span><span class="sxs-lookup"><span data-stu-id="a1722-120">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="a1722-121">Project Operations, tüzel kişilik düzeyindeki yapılandırmalar aracılığıyla aynı ortamda stoklu/üretim siparişi senaryolarını ve stoğu tutulmayan/kaynak tabanlı senaryoları destekler.</span><span class="sxs-lookup"><span data-stu-id="a1722-121">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="a1722-122">Örneğin, Contoso ABD üretim tesislerinde stoklu/üretim siparişi özelliklerini (Tüzel kişilik = Contoso Manufacturing United States) ve Birleşik Krallık'taki Contoso Robotics Arms servis tesisinde stoğu tutulmayan/kaynak tabanlı özellikleri (Tüzel kişilik = Contoso Robotics United Kingdom) kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="a1722-122">For example, Contoso can leverage stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States) and non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="a1722-123"><a name="lite"><a/>Lite dağıtımı: anlaşmadan proforma faturaya</span><span class="sxs-lookup"><span data-stu-id="a1722-123"><a name="lite"><a/>Lite deployment - deal to proforma invoicing</span></span>
<span data-ttu-id="a1722-124">Lite dağıtımı aşağıdaki özellikleri içerir:</span><span class="sxs-lookup"><span data-stu-id="a1722-124">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="a1722-125">Web için Microsoft Project kullanarak proje planlama</span><span class="sxs-lookup"><span data-stu-id="a1722-125">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="a1722-126">Çok boyutlu fiyatlandırma</span><span class="sxs-lookup"><span data-stu-id="a1722-126">Multi-dimensional pricing</span></span>
- <span data-ttu-id="a1722-127">Birleşik Kaynak Yönetimi</span><span class="sxs-lookup"><span data-stu-id="a1722-127">Unified Resource Management</span></span>
- <span data-ttu-id="a1722-128">Zaman İzleme</span><span class="sxs-lookup"><span data-stu-id="a1722-128">Time Tracking</span></span>
- <span data-ttu-id="a1722-129">Temel Gider</span><span class="sxs-lookup"><span data-stu-id="a1722-129">Basic Expense</span></span>
- <span data-ttu-id="a1722-130">Fatura Teklifi</span><span class="sxs-lookup"><span data-stu-id="a1722-130">Invoice Proposal</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="a1722-131">Dağıtım adımları:</span><span class="sxs-lookup"><span data-stu-id="a1722-131">Deployment steps:</span></span>
<span data-ttu-id="a1722-132">[Dağıtım anketini](https://aka.ms/provisionprojectoperations) kullanarak en iyi Project Operations dağıtım yöntemini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="a1722-132">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="a1722-133">Bu dağıtım için bkz. [Önizleme aboneliğine kaydolma](lite-preview-subscription-sign-up.md) ve [Yeni ortam sağlama](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="a1722-133">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="a1722-134"><a name="integrated"><a/>Kaynağı/stoğu tutulmayanlara ait senaryolar için Project Operations</span><span class="sxs-lookup"><span data-stu-id="a1722-134"><a name="integrated"><a/>Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="a1722-135">Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations aşağıdaki özellikleri içerir:</span><span class="sxs-lookup"><span data-stu-id="a1722-135">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="a1722-136">Web için Microsoft Project kullanarak proje planlama</span><span class="sxs-lookup"><span data-stu-id="a1722-136">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="a1722-137">Çok boyutlu fiyatlandırma</span><span class="sxs-lookup"><span data-stu-id="a1722-137">Multi-dimensional pricing</span></span>
- <span data-ttu-id="a1722-138">Birleşik Kaynak Yönetimi</span><span class="sxs-lookup"><span data-stu-id="a1722-138">Unified Resource Management</span></span>
- <span data-ttu-id="a1722-139">Zaman İzleme</span><span class="sxs-lookup"><span data-stu-id="a1722-139">Time Tracking</span></span>
- <span data-ttu-id="a1722-140">Temel Gider</span><span class="sxs-lookup"><span data-stu-id="a1722-140">Basic Expense</span></span>
- <span data-ttu-id="a1722-141">Tam Gider</span><span class="sxs-lookup"><span data-stu-id="a1722-141">Full Expense</span></span>
- <span data-ttu-id="a1722-142">Makbuz OCR'si</span><span class="sxs-lookup"><span data-stu-id="a1722-142">Receipt OCR</span></span>
- <span data-ttu-id="a1722-143">Tam Faturalama</span><span class="sxs-lookup"><span data-stu-id="a1722-143">Full Invoicing</span></span>
- <span data-ttu-id="a1722-144">Gelir Tanıma</span><span class="sxs-lookup"><span data-stu-id="a1722-144">Revenue Recognition</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="a1722-145">Dağıtım adımları:</span><span class="sxs-lookup"><span data-stu-id="a1722-145">Deployment steps:</span></span>
<span data-ttu-id="a1722-146">[Dağıtım anketini](https://aka.ms/provisionprojectoperations) kullanarak en iyi Project Operations dağıtım yöntemini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="a1722-146">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="a1722-147">Bu dağıtım için bkz. [Önizleme aboneliğine kaydolma](resource-sign-up-preview-subscription.md) ve [Yeni ortam sağlama](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="a1722-147">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="a1722-148">Stoklu/üretim siparişi senaryoları için Project Operations</span><span class="sxs-lookup"><span data-stu-id="a1722-148">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="a1722-149">İKY kullanarak proje planlama</span><span class="sxs-lookup"><span data-stu-id="a1722-149">Project planning using WBS</span></span>
- <span data-ttu-id="a1722-150">Kaynak Yönetimi</span><span class="sxs-lookup"><span data-stu-id="a1722-150">Resource Management</span></span>
- <span data-ttu-id="a1722-151">Zaman İzleme</span><span class="sxs-lookup"><span data-stu-id="a1722-151">Time Tracking</span></span>
- <span data-ttu-id="a1722-152">Tam Gider</span><span class="sxs-lookup"><span data-stu-id="a1722-152">Full Expense</span></span>
- <span data-ttu-id="a1722-153">Makbuz OCR'si</span><span class="sxs-lookup"><span data-stu-id="a1722-153">Receipt OCR</span></span>
- <span data-ttu-id="a1722-154">Tam Faturalama</span><span class="sxs-lookup"><span data-stu-id="a1722-154">Full Invoicing</span></span>
- <span data-ttu-id="a1722-155">Gelir Tanıma</span><span class="sxs-lookup"><span data-stu-id="a1722-155">Revenue Recognition</span></span>
- <span data-ttu-id="a1722-156">Üretim Siparişleri</span><span class="sxs-lookup"><span data-stu-id="a1722-156">Production Orders</span></span>
- <span data-ttu-id="a1722-157">Malzeme desteği</span><span class="sxs-lookup"><span data-stu-id="a1722-157">Materials support</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="a1722-158">Dağıtım adımları:</span><span class="sxs-lookup"><span data-stu-id="a1722-158">Deployment steps:</span></span>
<span data-ttu-id="a1722-159">[Dağıtım anketini](https://aka.ms/provisionprojectoperations) kullanarak en iyi Project Operations dağıtım yöntemini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="a1722-159">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="a1722-160">Bu dağıtım için bkz. [Önizleme aboneliğine kaydolma](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) ve [Yeni ortam sağlama](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="a1722-160">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 



