---
title: Şirketler arası faturalamaya genel bakış
description: Bu konu, projeler için şirketler arası faturalandırma hakkında bilgi ve örnekler sağlar.
author: sigitac
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: c1dcf642f79ce64cb83285ac6dc6d7eaf815145c
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369400"
---
# <a name="intercompany-invoicing-overview"></a><span data-ttu-id="2b136-103">Şirketler arası faturalamaya genel bakış</span><span class="sxs-lookup"><span data-stu-id="2b136-103">Intercompany invoicing overview</span></span>

<span data-ttu-id="2b136-104">_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="2b136-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="2b136-105">Kuruluşunuzun, projeler için ürünleri ve servisleri birbirine aktarabilecek birden çok bölümü, yan kuruluşları ve diğer tüzel kişilikler olabilir.</span><span class="sxs-lookup"><span data-stu-id="2b136-105">Your organization might have multiple divisions, subsidiaries, and other legal entities that transfer products and services to each other for projects.</span></span> <span data-ttu-id="2b136-106">Hizmet veya ürün sağlayan tüzel kişiliğe *ödünç veren tüzel kişilik* denir.</span><span class="sxs-lookup"><span data-stu-id="2b136-106">The legal entity that provides the service or product is called the *lending legal entity*.</span></span> <span data-ttu-id="2b136-107">Hizmet veya ürün alan tüzel kişiliğe *ödünç alan tüzel kişilik* denir.</span><span class="sxs-lookup"><span data-stu-id="2b136-107">The legal entity that receives the service or product is called the *borrowing legal entity*.</span></span>

<span data-ttu-id="2b136-108">Aşağıdaki resimde, Contoso Robotics ABD (ödünç alan tüzel kişilik) ve Contoso Robotics UK (ödünç veren tüzel kişilik) adlı iki tüzel kişiliğin Adventure works müşterisine bir projeyi teslim etmek için kaynakları paylaştığı tipik bir senaryo gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="2b136-108">The following illustration shows a typical scenario where two legal entities, Contoso Robotics USA (the borrowing legal entity) and Contoso Robotics UK (the lending legal entity) share resources to deliver a project for the customer, Adventure works.</span></span> <span data-ttu-id="2b136-109">Bu senaryoda Contoso Robotics ABD, işi Adventure Works'e teslim etmek üzere sözleşme yapmıştır.</span><span class="sxs-lookup"><span data-stu-id="2b136-109">For this scenario, Contoso Robotics USA is contracted to deliver the work to Adventure Works.</span></span>

![Şirketler arası faturalama](./media/IntercompanyScenario.png) 

<span data-ttu-id="2b136-111">Dynamics 365 Project Operations, şirketler arası hareketleri işlemek için aşağıdaki akışı kullanır:</span><span class="sxs-lookup"><span data-stu-id="2b136-111">Dynamics 365 Project Operations uses the following flow to process intercompany transactions:</span></span>

1. <span data-ttu-id="2b136-112">Ödünç veren tüzel kişilikten gelen kaynaklar, ödünç alan tüzel kişilikteki projelere karşılık olarak zaman ve gider ayırarak şirketler arası zaman veya gider işlemlerini kaydeder.</span><span class="sxs-lookup"><span data-stu-id="2b136-112">Resources from the lending legal entity record intercompany time or expense transactions by booking time and expense against projects in the borrowing legal entity.</span></span>
2. <span data-ttu-id="2b136-113">Ödünç alan şirketin birim maliyet fiyat listesi kullanılarak zaman ve gider maliyetleri ödünç veren şirkete kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="2b136-113">Time and expense costs are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
3. <span data-ttu-id="2b136-114">Şirketler arası faturalanmayan satış işlemleri, ödünç alan firmanın birim maliyet fiyat listesi kullanılarak ödünç veren şirkette kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="2b136-114">Intercompany unbilled sale transactions are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
4. <span data-ttu-id="2b136-115">Faturalanmayan gelir, proje sözleşmesi satış fiyat listesi kullanılarak ödünç alan firmaya kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="2b136-115">Unbilled revenue is recorded in the borrowing company using the project contract sales price list.</span></span> <span data-ttu-id="2b136-116">Faturalanmayan gelir kaydedildiğinde müşteriye faturalanabilir.</span><span class="sxs-lookup"><span data-stu-id="2b136-116">The customer can be billed when unbilled revenue is recorded.</span></span> <span data-ttu-id="2b136-117">Müşterinin, şirketler arası fatura işlemlerinin tamamlanmasını beklemesi gerekmez.</span><span class="sxs-lookup"><span data-stu-id="2b136-117">The customer doesn't have to wait until intercompany invoice processing is complete.</span></span>
5. <span data-ttu-id="2b136-118">Şirketler arası müşteri faturaları, ödünç veren şirkette dönemsel olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="2b136-118">Intercompany customer invoices are created on a periodic basis in the lending company.</span></span> <span data-ttu-id="2b136-119">Faturalar el ile veya dönemsel otomatik bir işlem kullanılarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="2b136-119">The invoices are created manually or by using a periodic automated process.</span></span> <span data-ttu-id="2b136-120">Ödünç alan her tüzel kişilik için tek bir fatura oluşturulabileceği gibi proje bazında ayrı faturalar da oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="2b136-120">A single invoice can be created for each borrowing legal entity or separate invoices can be created by project.</span></span>
6. <span data-ttu-id="2b136-121">Şirketler arası müşteri faturası, ödünç veren tüzel kişiliğe nakledildiğinde, ödünç alan tüzel kişilikte karşılık gelen bekleyen satıcı faturası oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="2b136-121">When the intercompany customer invoice is posted in the lending legal entity, the corresponding pending vendor invoice is created in the borrowing legal entity.</span></span> <span data-ttu-id="2b136-122">Beklemede olan satıcı faturasındaki maliyetler, fatura deftere nakledildiğinde proje alt defterine kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="2b136-122">The costs in the pending vendor invoice will be recorded to the project subledger when the invoice is posted.</span></span>

<span data-ttu-id="2b136-123">Aşağıdaki diyagramda muhasebe olayları ve genel muhasebeye nakledilmesi beklenen kayıtlar ile ilgili şirketler arası faturalama gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="2b136-123">The following diagram illustrates intercompany invoicing as it relates to accounting events and expected postings to the general ledger.</span></span>

![Şirketler arası akış](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a><span data-ttu-id="2b136-125">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="2b136-125">Additional resources</span></span>

- [<span data-ttu-id="2b136-126">Şirketler arası faturalamayı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="2b136-126">Configure intercompany invoicing</span></span>](configure-intercompany-invoicing.md)
- [<span data-ttu-id="2b136-127">Şirketler arası işlemleri kaydetme</span><span class="sxs-lookup"><span data-stu-id="2b136-127">Record intercompany transactions</span></span>](create-intercompany-transactions.md)
- [<span data-ttu-id="2b136-128">Şirketler arası müşteri ve satıcı faturaları oluşturma</span><span class="sxs-lookup"><span data-stu-id="2b136-128">Create intercompany customer and vendor invoices</span></span>](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]