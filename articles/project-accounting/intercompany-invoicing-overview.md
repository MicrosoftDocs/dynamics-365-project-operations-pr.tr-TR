---
title: Şirketler arası faturalamaya genel bakış
description: Bu konu, projeler için şirketler arası faturalandırma hakkında bilgi ve örnekler sağlar.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 670b5d15ecf1ef7dcc034064e625814cbe6d54b0
ms.sourcegitcommit: addbe0647619413e85e7cde80f6a21db95ab623e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595571"
---
# <a name="intercompany-invoicing-overview"></a><span data-ttu-id="e6488-103">Şirketler arası faturalamaya genel bakış</span><span class="sxs-lookup"><span data-stu-id="e6488-103">Intercompany invoicing overview</span></span>

<span data-ttu-id="e6488-104">_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="e6488-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="e6488-105">Kuruluşunuzun, projeler için ürünleri ve servisleri birbirine aktarabilecek birden çok bölümü, yan kuruluşları ve diğer tüzel kişilikler olabilir.</span><span class="sxs-lookup"><span data-stu-id="e6488-105">Your organization might have multiple divisions, subsidiaries, and other legal entities that transfer products and services to each other for projects.</span></span> <span data-ttu-id="e6488-106">Hizmet veya ürün sağlayan tüzel kişiliğe *ödünç veren tüzel kişilik* denir.</span><span class="sxs-lookup"><span data-stu-id="e6488-106">The legal entity that provides the service or product is called the *lending legal entity*.</span></span> <span data-ttu-id="e6488-107">Hizmet veya ürün alan tüzel kişiliğe *ödünç alan tüzel kişilik* denir.</span><span class="sxs-lookup"><span data-stu-id="e6488-107">The legal entity that receives the service or product is called the *borrowing legal entity*.</span></span>

<span data-ttu-id="e6488-108">Aşağıdaki resimde iki tüzel kişilik olan Contoso Robotics USA (ödünç alan tüzel kişilik) ve Contoso Robotics UK şirketlerinin (ödünç veren tüzel kişilik) müşterisi olan Adventure Works'e bir proje sunmak için kaynakları paylaştığı tipik bir senaryo gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="e6488-108">The following illustration shows a typical scenario where two legal entities, Contoso Robotics USA (the borrowing legal entity) and Contoso Robotics UK (the lending legal entity) share resources to deliver a project for the customer, Adventure works.</span></span> <span data-ttu-id="e6488-109">Bu senaryoda, işi Adventure Works'e teslim etmesi için Contoso Robotics USA ile sözleşme imzalanmıştır.</span><span class="sxs-lookup"><span data-stu-id="e6488-109">For this scenario, Contoso Robotics USA is contracted to deliver the work to Adventure Works.</span></span>

![Şirketler arası faturalama](./media/IntercompanyScenario.png) 

<span data-ttu-id="e6488-111">Dynamics 365 Project Operations, şirketler arası hareketleri işlemek için aşağıdaki akışı kullanır:</span><span class="sxs-lookup"><span data-stu-id="e6488-111">Dynamics 365 Project Operations uses the following flow to process intercompany transactions:</span></span>

1. <span data-ttu-id="e6488-112">Ödünç veren tüzel kişilikten gelen kaynaklar, ödünç alan tüzel kişilikteki projelere karşılık olarak zaman ve gider ayırarak şirketler arası zaman veya gider işlemlerini kaydeder.</span><span class="sxs-lookup"><span data-stu-id="e6488-112">Resources from the lending legal entity record intercompany time or expense transactions by booking time and expense against projects in the borrowing legal entity.</span></span>
2. <span data-ttu-id="e6488-113">Ödünç alan şirketin birim maliyet fiyat listesi kullanılarak zaman ve gider maliyetleri ödünç veren şirkete kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="e6488-113">Time and expense costs are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
3. <span data-ttu-id="e6488-114">Şirketler arası faturalanmayan satış işlemleri, ödünç alan firmanın birim maliyet fiyat listesi kullanılarak ödünç veren şirkette kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="e6488-114">Intercompany unbilled sale transactions are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
4. <span data-ttu-id="e6488-115">Faturalanmayan gelir, proje sözleşmesi satış fiyat listesi kullanılarak ödünç alan firmaya kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="e6488-115">Unbilled revenue is recorded in the borrowing company using the project contract sales price list.</span></span> <span data-ttu-id="e6488-116">Faturalanmayan gelir kaydedildiğinde müşteriye faturalanabilir.</span><span class="sxs-lookup"><span data-stu-id="e6488-116">The customer can be billed when unbilled revenue is recorded.</span></span> <span data-ttu-id="e6488-117">Müşterinin, şirketler arası fatura işlemlerinin tamamlanmasını beklemesi gerekmez.</span><span class="sxs-lookup"><span data-stu-id="e6488-117">The customer doesn't have to wait until intercompany invoice processing is complete.</span></span>
5. <span data-ttu-id="e6488-118">Şirketler arası müşteri faturaları, ödünç veren şirkette dönemsel olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="e6488-118">Intercompany customer invoices are created on a periodic basis in the lending company.</span></span> <span data-ttu-id="e6488-119">Faturalar el ile veya dönemsel otomatik bir işlem kullanılarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="e6488-119">The invoices are created manually or by using a periodic automated process.</span></span> <span data-ttu-id="e6488-120">Ödünç alan her tüzel kişilik için tek bir fatura oluşturulabileceği gibi proje bazında ayrı faturalar da oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="e6488-120">A single invoice can be created for each borrowing legal entity or separate invoices can be created by project.</span></span>
6. <span data-ttu-id="e6488-121">Şirketler arası müşteri faturası, ödünç veren tüzel kişiliğe nakledildiğinde, ödünç alan tüzel kişilikte karşılık gelen bekleyen satıcı faturası oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="e6488-121">When the intercompany customer invoice is posted in the lending legal entity, the corresponding pending vendor invoice is created in the borrowing legal entity.</span></span> <span data-ttu-id="e6488-122">Beklemede olan satıcı faturasındaki maliyetler, fatura deftere nakledildiğinde proje alt defterine kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="e6488-122">The costs in the pending vendor invoice will be recorded to the project subledger when the invoice is posted.</span></span>

<span data-ttu-id="e6488-123">Aşağıdaki diyagramda muhasebe olayları ve genel muhasebeye nakledilmesi beklenen kayıtlar ile ilgili şirketler arası faturalama gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="e6488-123">The following diagram illustrates intercompany invoicing as it relates to accounting events and expected postings to the general ledger.</span></span>

![Şirketler arası akış](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a><span data-ttu-id="e6488-125">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="e6488-125">Additional resources</span></span>

- [<span data-ttu-id="e6488-126">Şirketler arası faturalamayı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="e6488-126">Configure intercompany invoicing</span></span>](configure-intercompany-invoicing.md)
- [<span data-ttu-id="e6488-127">Şirketler arası işlemleri kaydetme</span><span class="sxs-lookup"><span data-stu-id="e6488-127">Record intercompany transactions</span></span>](create-intercompany-transactions.md)
- [<span data-ttu-id="e6488-128">Şirketler arası müşteri ve satıcı faturaları oluşturma</span><span class="sxs-lookup"><span data-stu-id="e6488-128">Create intercompany customer and vendor invoices</span></span>](create-intercompany-customer-vendor-invoices.md)
