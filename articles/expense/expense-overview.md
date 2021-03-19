---
title: Gidere genel bakış
description: Bu konuda, Project Operations içindeki Gider özellikleri hakkında bilgiler sağlanmaktadır.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c4e2f441e1c4b1bcba5bca292b8075b4334a004d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276597"
---
# <a name="expense-home-page"></a><span data-ttu-id="f23b7-103">Gider giriş sayfası</span><span class="sxs-lookup"><span data-stu-id="f23b7-103">Expense home page</span></span>

<span data-ttu-id="f23b7-104">_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="f23b7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="f23b7-105">Dynamics 365 Project Operations, giderleri işleme yeteneğini destekler.</span><span class="sxs-lookup"><span data-stu-id="f23b7-105">Dynamics 365 Project Operations supports the ability to process expenses.</span></span> <span data-ttu-id="f23b7-106">Giderler, ilkelerden, işlem kategorilerinden ve onaylardan oluşan bir özelleştirilebilir iş akışı kullanarak projeler olsa da olmasa da işlenebilir.</span><span class="sxs-lookup"><span data-stu-id="f23b7-106">Expense processing occurs with or without projects by using a customizable workflow of policies, transaction categories, and approvals.</span></span>

<span data-ttu-id="f23b7-107">Project Operations'ta, Gider için desteklenen iki dağıtım modeli vardır:</span><span class="sxs-lookup"><span data-stu-id="f23b7-107">In Project Operations, there are two supported deployment models for Expense:</span></span> 

- <span data-ttu-id="f23b7-108">**Tam**: Tam dağıtım **Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations** veya **Üretim emrini temel alan senaryolar için Project Operations** ile kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="f23b7-108">**Full**: Full deployment is available for **Project Operations for resource/non-stocked based scenarios** or **Project Operations for production order-based scenarios**.</span></span>
- <span data-ttu-id="f23b7-109">**Temel**: Temel dağıtım, **Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations** ve **Lite dağıtımı: anlaşmadan proforma faturaya** ile kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="f23b7-109">**Basic**: Basic deployment is available for **Project Operations for resource/non-stocked based scenarios** and **Lite deployment – deal to proforma invoicing**.</span></span>

## <a name="full"></a><span data-ttu-id="f23b7-110">Tam</span><span class="sxs-lookup"><span data-stu-id="f23b7-110">Full</span></span> 
<span data-ttu-id="f23b7-111">Tam Gider dağıtımı, ilkeler oluşturma becerisini içeren eksiksiz bir ilke uygulaması sağlar, örneğin:</span><span class="sxs-lookup"><span data-stu-id="f23b7-111">Full Expense deployment provides a complete policy enforcement that includes the ability to create policies, such as:</span></span>

  - <span data-ttu-id="f23b7-112">Gider kategorisi limitleri</span><span class="sxs-lookup"><span data-stu-id="f23b7-112">Expense category limits</span></span>
  - <span data-ttu-id="f23b7-113">Seyahat</span><span class="sxs-lookup"><span data-stu-id="f23b7-113">Travel</span></span>
  - <span data-ttu-id="f23b7-114">Harcırah</span><span class="sxs-lookup"><span data-stu-id="f23b7-114">Per diem</span></span>
  - <span data-ttu-id="f23b7-115">Kredi kartı içeri aktarmaları</span><span class="sxs-lookup"><span data-stu-id="f23b7-115">Credit card imports</span></span>
  - <span data-ttu-id="f23b7-116">Makbuz optik karakteri tanıma</span><span class="sxs-lookup"><span data-stu-id="f23b7-116">Receipt optical character recognition</span></span>

## <a name="basic"></a><span data-ttu-id="f23b7-117">Temel</span><span class="sxs-lookup"><span data-stu-id="f23b7-117">Basic</span></span> 
<span data-ttu-id="f23b7-118">Temel Gider dağıtım senaryosu yalnızca bir projedeki temel giderleri kaydetmenize izin verir.</span><span class="sxs-lookup"><span data-stu-id="f23b7-118">Basic Expense deployment scenario only allows you to record basic expenses against a project.</span></span> 

<span data-ttu-id="f23b7-119">Daha fazla bilgi için bkz. [Gider girişi (lite)](basic-expense.md)</span><span class="sxs-lookup"><span data-stu-id="f23b7-119">For more information, see [Expense entry (lite)](basic-expense.md)</span></span>

## <a name="determine-your-expense-deployment"></a><span data-ttu-id="f23b7-120">Gider dağıtımınızı belirleme</span><span class="sxs-lookup"><span data-stu-id="f23b7-120">Determine your Expense deployment</span></span>
<span data-ttu-id="f23b7-121">Temel Gider yönetim dağıtımını çalıştırıp çalıştırmadığınızı belirlemek için adres URL'sinin **.crm.dynamics.com** ile bittiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="f23b7-121">To determine if you're running the Basic Expense management deployment, verify that the address URL ends with **.crm.dynamics.com**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]