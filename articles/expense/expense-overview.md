---
title: Gidere genel bakış
description: Bu konuda, Project Operations içindeki Gider özellikleri hakkında bilgiler sağlanmaktadır.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 6da831fef5dba060b8019d7689645405c7ebdbed
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086204"
---
# <a name="expense-home-page"></a><span data-ttu-id="be14b-103">Gider giriş sayfası</span><span class="sxs-lookup"><span data-stu-id="be14b-103">Expense home page</span></span>

<span data-ttu-id="be14b-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="be14b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="be14b-105">Dynamics 365 Project Operations, giderleri işleme özelliğini destekler.</span><span class="sxs-lookup"><span data-stu-id="be14b-105">Dynamics 365 Project Operations supports the ability to process expenses.</span></span> <span data-ttu-id="be14b-106">Giderler, ilkelerden, işlem kategorilerinden ve onaylardan oluşan bir özelleştirilebilir iş akışı kullanarak projeler olsa da olmasa da işlenebilir.</span><span class="sxs-lookup"><span data-stu-id="be14b-106">Expense processing occurs with or without projects by using a customizable workflow of policies, transaction categories, and approvals.</span></span>

<span data-ttu-id="be14b-107">Project Operations'ta, Gider için desteklenen iki dağıtım modeli vardır:</span><span class="sxs-lookup"><span data-stu-id="be14b-107">In Project Operations, there are two supported deployment models for Expense:</span></span> 

- <span data-ttu-id="be14b-108">**Tam** : Tam dağıtım **Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations** veya **Üretim emrini temel alan senaryolar için Project Operations** ile kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="be14b-108">**Full** : Full deployment is available for **Project Operations for resource/non-stocked based scenarios** or **Project Operations for production order based scenarios**.</span></span>
- <span data-ttu-id="be14b-109">**Temel** : Temel dağıtım, **Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations** ve **Lite dağıtımı: anlaşmadan proforma faturaya** ile kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="be14b-109">**Basic** : Basic deployment is available for **Project Operations for resource/non-stocked based scenarios** and **Lite deployment – deal to proforma invoicing**.</span></span>

## <a name="full"></a><span data-ttu-id="be14b-110">Tam</span><span class="sxs-lookup"><span data-stu-id="be14b-110">Full</span></span> 
<span data-ttu-id="be14b-111">Tam Gider dağıtımı, ilke oluşturma özelliğini içeren tam bir ilke uygulaması sağlar. Örneğin:</span><span class="sxs-lookup"><span data-stu-id="be14b-111">Full Expense deployment provides a complete policy enforcement which includes the ability to create policies, such as:</span></span>

  - <span data-ttu-id="be14b-112">Gider kategorisi limitleri</span><span class="sxs-lookup"><span data-stu-id="be14b-112">Expense category limits</span></span>
  - <span data-ttu-id="be14b-113">Seyahat</span><span class="sxs-lookup"><span data-stu-id="be14b-113">Travel</span></span>
  - <span data-ttu-id="be14b-114">Harcırah</span><span class="sxs-lookup"><span data-stu-id="be14b-114">Per diem</span></span>
  - <span data-ttu-id="be14b-115">Kredi kartı içeri aktarmaları</span><span class="sxs-lookup"><span data-stu-id="be14b-115">Credit card imports</span></span>
  - <span data-ttu-id="be14b-116">Makbuz optik karakteri tanıma</span><span class="sxs-lookup"><span data-stu-id="be14b-116">Receipt optical character recognition</span></span>

## <a name="basic"></a><span data-ttu-id="be14b-117">Temel</span><span class="sxs-lookup"><span data-stu-id="be14b-117">Basic</span></span> 
<span data-ttu-id="be14b-118">Temel Gider dağıtım senaryosu yalnızca bir projedeki temel giderleri kaydetmenize izin verir.</span><span class="sxs-lookup"><span data-stu-id="be14b-118">Basic Expense deployment scenario only allows you to record basic expenses against a project.</span></span> 

<span data-ttu-id="be14b-119">Daha fazla bilgi için bkz. [Gider girişi (lite)](basic-expense.md)</span><span class="sxs-lookup"><span data-stu-id="be14b-119">For more information, see [Expense entry (lite)](basic-expense.md)</span></span>

## <a name="determine-your-expense-deployment"></a><span data-ttu-id="be14b-120">Gider dağıtımınızı belirleme</span><span class="sxs-lookup"><span data-stu-id="be14b-120">Determine your Expense deployment</span></span>
<span data-ttu-id="be14b-121">Temel Gider yönetim dağıtımını çalıştırıp çalıştırmadığınızı belirlemek için adres URL'sinin **.crm.dynamics.com** ile bittiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="be14b-121">To determine if you're running the Basic Expense management deployment, verify that the address URL ends with **.crm.dynamics.com**.</span></span> 