---
title: Project Operations dağıtın - lite
description: Bu konuda, Project Operations Lite dağıtımını (anlaşmadan proforma faturaya) yükleme hakkında bilgiler sağlanmaktadır.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d4ef905f875ac8af7b2d70c3e64506558bdea1ed
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642207"
---
# <a name="deploy-project-operations---lite"></a><span data-ttu-id="08665-103">Project Operations dağıtın - lite</span><span class="sxs-lookup"><span data-stu-id="08665-103">Deploy Project Operations - lite</span></span>

<span data-ttu-id="08665-104">_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_</span><span class="sxs-lookup"><span data-stu-id="08665-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="08665-105">Project Operations birden çok dağıtım modelini destekler.</span><span class="sxs-lookup"><span data-stu-id="08665-105">Project Operations supports multiple deployment models.</span></span> <span data-ttu-id="08665-106">En iyi dağıtım modelini belirlemek için bkz. [Dağıtım türleri](determine-deployment-type.md).</span><span class="sxs-lookup"><span data-stu-id="08665-106">To determine the best deployment model, see [Deployment types](determine-deployment-type.md).</span></span>


> [!IMPORTANT]
> <span data-ttu-id="08665-107">Bu dağıtım (Lite dağıtımı) anlaşmadan proforma faturaya, **Common Data Service-yalnızca Project Operations dağıtımı** ile sonuçlanır.</span><span class="sxs-lookup"><span data-stu-id="08665-107">This deployment, Lite deployment – deal to proforma invoicing, results in a **Common Data Service-only deployment of Project Operations**.</span></span>

- [<span data-ttu-id="08665-108">Project Operations'ı yeni bir CDS ortamına yükleme</span><span class="sxs-lookup"><span data-stu-id="08665-108">Install Project Operations into a new CDS environment</span></span>](#new)
- [<span data-ttu-id="08665-109">Var olan bir CDS ortamına yükleme</span><span class="sxs-lookup"><span data-stu-id="08665-109">Install into an existing CDS environment</span></span>](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a><span data-ttu-id="08665-110">Project Operations'ı yeni bir CDS ortamına yükleme</span><span class="sxs-lookup"><span data-stu-id="08665-110">Install Project Operations to a new CDS environment</span></span>

1. <span data-ttu-id="08665-111">Project Operations lisansına sahip [Genel Yönetici veya Power Platform Yöneticisi](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) olarak [PowerPlatform yönetim merkezi](https://admin.powerplatform.com)'nde yeni bir CDS ortamı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="08665-111">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, create a new CDS environment in the [PowerPlatform admin center](https://admin.powerplatform.com).</span></span> <span data-ttu-id="08665-112">**CDS veritabanı** ve **Dynamics 365 Uygulamaları**'nın etkinleştirildiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="08665-112">Make sure that **CDS database** and **Dynamics 365 Apps** are enabled.</span></span> <span data-ttu-id="08665-113">Daha fazla bilgi için bkz. [Power Platform yönetim merkezinde ortamlar oluşturma ve yönetme](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span><span class="sxs-lookup"><span data-stu-id="08665-113">For more information, see [Create and manage environments in the Power Platform admin center](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span></span>
2. <span data-ttu-id="08665-114">Dynamics 365 uygulamaları dağıtım listesinden **Microsoft Dynamics 365 Project Operations**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="08665-114">Select **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span>


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a><span data-ttu-id="08665-115">Project Operations'ı var olan bir CDS ortamına yükleme</span><span class="sxs-lookup"><span data-stu-id="08665-115">Install Project Operations to an existing CDS environment</span></span>

1. <span data-ttu-id="08665-116">Project Operations lisansına sahip [Genel Yönetici Power Platform Yöneticisi](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) olarak Project Operations'ı yüklemek istediğiniz [PowerPlatform yönetim merkezi](https://admin.powerplatform.com)'nde ortamı bulun.</span><span class="sxs-lookup"><span data-stu-id="08665-116">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, locate the environment in the [PowerPlatform admin center](https://admin.powerplatform.com) where you want to install Project Operations.</span></span>
2. <span data-ttu-id="08665-117">Dynamics 365 uygulamaları dağıtım listesinden **Microsoft Dynamics 365 Project Operations**'ı yükleyin.</span><span class="sxs-lookup"><span data-stu-id="08665-117">Install **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span> <span data-ttu-id="08665-118">Daha fazla bilgi için bkz. [Dynamics 365 uygulamalarını yönetme](https://docs.microsoft.com/power-platform/admin/manage-apps).</span><span class="sxs-lookup"><span data-stu-id="08665-118">For more information, see [Manage Dynamics 365 apps](https://docs.microsoft.com/power-platform/admin/manage-apps).</span></span>


