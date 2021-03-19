---
title: Gelir tanımaya genel bakış
description: Bu konu Project Operations'ta gelir tanıma hakkında bilgi sağlar.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5e77a0442f634a50f8099fadec42ff400fee0e81
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278892"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="2a843-103">Gelir tanımaya genel bakış</span><span class="sxs-lookup"><span data-stu-id="2a843-103">Revenue recognition overview</span></span>

<span data-ttu-id="2a843-104">_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="2a843-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="2a843-105">Dynamics 365 Project Operations uygulamasında gelir tanıma ilkeleri, bir proje veya projenin bir kısmı için seçilen faturalama yöntemine göre değişiklik gösterir.</span><span class="sxs-lookup"><span data-stu-id="2a843-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="2a843-106">Bu konu Project Operations'ta gelir tanıma hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="2a843-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="2a843-107">Zaman ve malzeme faturalama yöntemi kullanılarak muhasebeleştirilen işlemler</span><span class="sxs-lookup"><span data-stu-id="2a843-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="2a843-108">Maliyet ve gelir tanıma birbirine bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="2a843-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="2a843-109">İşlem maliyeti ve faturalanmayan satışlar [Project Operations Entegrasyon günlüğü](../project-accounting/project-operations-integration-journal.md) kullanılarak gönderilir.</span><span class="sxs-lookup"><span data-stu-id="2a843-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="2a843-110">Proje maliyeti ve gelir profili, faturalanmayan satış işlemlerinin genel muhasebeye gönderilip gönderilmediğini belirler.</span><span class="sxs-lookup"><span data-stu-id="2a843-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="2a843-111">**Gelir tahakkuku** seçilirse sistem, gönderim sırasında **WIP satış değeri** ve **Tahakkuk eden gelir satış değeri** hesaplarını kullanır.</span><span class="sxs-lookup"><span data-stu-id="2a843-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="2a843-112">Aşağıda bu yöntemin bir örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="2a843-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="2a843-113">İşlem türü</span><span class="sxs-lookup"><span data-stu-id="2a843-113">Transaction type</span></span> | <span data-ttu-id="2a843-114">Banka/Kredi</span><span class="sxs-lookup"><span data-stu-id="2a843-114">Debit/Credit</span></span> | <span data-ttu-id="2a843-115">Miktar</span><span class="sxs-lookup"><span data-stu-id="2a843-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="2a843-116">WIP Satış değeri</span><span class="sxs-lookup"><span data-stu-id="2a843-116">WIP Sales value</span></span> | <span data-ttu-id="2a843-117">Banka</span><span class="sxs-lookup"><span data-stu-id="2a843-117">Debit</span></span> | <span data-ttu-id="2a843-118">100</span><span class="sxs-lookup"><span data-stu-id="2a843-118">100</span></span> |
  | <span data-ttu-id="2a843-119">Tahakkuk eden gelir satış değeri</span><span class="sxs-lookup"><span data-stu-id="2a843-119">Accrued revenue sales value</span></span> | <span data-ttu-id="2a843-120">Kredi</span><span class="sxs-lookup"><span data-stu-id="2a843-120">Credit</span></span> | <span data-ttu-id="2a843-121">100</span><span class="sxs-lookup"><span data-stu-id="2a843-121">100</span></span> |

- <span data-ttu-id="2a843-122">Gelir, faturalama sırasında tanınır.</span><span class="sxs-lookup"><span data-stu-id="2a843-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="2a843-123">Sistem, gönderim sırasında **Faturalanan gelir** hesabını kullanır.</span><span class="sxs-lookup"><span data-stu-id="2a843-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="2a843-124">Aşağıda bu yöntemin bir örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="2a843-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="2a843-125">İşlem türü</span><span class="sxs-lookup"><span data-stu-id="2a843-125">Transaction type</span></span> | <span data-ttu-id="2a843-126">Banka/Kredi</span><span class="sxs-lookup"><span data-stu-id="2a843-126">Debit/Credit</span></span> | <span data-ttu-id="2a843-127">Miktar</span><span class="sxs-lookup"><span data-stu-id="2a843-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="2a843-128">Müşteri bakiyesi</span><span class="sxs-lookup"><span data-stu-id="2a843-128">Customer balance</span></span> | <span data-ttu-id="2a843-129">Banka</span><span class="sxs-lookup"><span data-stu-id="2a843-129">Debit</span></span> | <span data-ttu-id="2a843-130">120</span><span class="sxs-lookup"><span data-stu-id="2a843-130">120</span></span> |
  | <span data-ttu-id="2a843-131">Satış vergisi borçları</span><span class="sxs-lookup"><span data-stu-id="2a843-131">Sales tax payable</span></span> | <span data-ttu-id="2a843-132">Kredi</span><span class="sxs-lookup"><span data-stu-id="2a843-132">Credit</span></span> | <span data-ttu-id="2a843-133">20</span><span class="sxs-lookup"><span data-stu-id="2a843-133">20</span></span> |
  | <span data-ttu-id="2a843-134">Faturalanan Gelir</span><span class="sxs-lookup"><span data-stu-id="2a843-134">Invoiced Revenue</span></span> | <span data-ttu-id="2a843-135">Kredi</span><span class="sxs-lookup"><span data-stu-id="2a843-135">Credit</span></span> | <span data-ttu-id="2a843-136">100</span><span class="sxs-lookup"><span data-stu-id="2a843-136">100</span></span> |

- <span data-ttu-id="2a843-137">Faturalanan satışlar gönderildiğinde gelir tahakkuk etmişse sistem, faturalamada tahakkuk eden geliri tersine çevirir.</span><span class="sxs-lookup"><span data-stu-id="2a843-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="2a843-138">İşlem türü</span><span class="sxs-lookup"><span data-stu-id="2a843-138">Transaction type</span></span> | <span data-ttu-id="2a843-139">Banka/Kredi</span><span class="sxs-lookup"><span data-stu-id="2a843-139">Debit/Credit</span></span> | <span data-ttu-id="2a843-140">Miktar</span><span class="sxs-lookup"><span data-stu-id="2a843-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="2a843-141">WIP Satış değeri</span><span class="sxs-lookup"><span data-stu-id="2a843-141">WIP Sales value</span></span> | <span data-ttu-id="2a843-142">Kredi</span><span class="sxs-lookup"><span data-stu-id="2a843-142">Credit</span></span> | <span data-ttu-id="2a843-143">100</span><span class="sxs-lookup"><span data-stu-id="2a843-143">100</span></span> |
  | <span data-ttu-id="2a843-144">Tahakkuk eden gelir satış değeri</span><span class="sxs-lookup"><span data-stu-id="2a843-144">Accrued revenue sales value</span></span> | <span data-ttu-id="2a843-145">Banka</span><span class="sxs-lookup"><span data-stu-id="2a843-145">Debit</span></span> | <span data-ttu-id="2a843-146">100</span><span class="sxs-lookup"><span data-stu-id="2a843-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="2a843-147">Sabit fiyatlı faturalama yöntemi kullanılarak muhasebeleştirilen işlemler</span><span class="sxs-lookup"><span data-stu-id="2a843-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="2a843-148">Maliyet ve gelir tanıma birbirinden ayrıdır.</span><span class="sxs-lookup"><span data-stu-id="2a843-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="2a843-149">İşlem maliyeti [Project Operations Entegrasyon günlüğü](../project-accounting/project-operations-integration-journal.md) kullanılarak gönderilir.</span><span class="sxs-lookup"><span data-stu-id="2a843-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="2a843-150">Faturalanmayan satış işlemleri oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="2a843-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="2a843-151">Proje maliyeti ve gelir profili **Proje tamamlama hesaplamaları için kullanılan ilke**, **WIP yok** olarak ayarlanmışsa gelir, faturalama sırasında tanınabilir.</span><span class="sxs-lookup"><span data-stu-id="2a843-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="2a843-152">Bu yöntemi yalnızca kısa vadeli, basit projeler için kullanın.</span><span class="sxs-lookup"><span data-stu-id="2a843-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="2a843-153">Gelir, **Tamamlanan sözleşme** veya **Tamamlanma yüzdesi gelir tanıma** yöntemiyle sabit fiyatlı gelir tahminleri kullanılarak tanınır.</span><span class="sxs-lookup"><span data-stu-id="2a843-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2a843-154">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="2a843-154">Additional resources</span></span>
[<span data-ttu-id="2a843-155">Faturalanabilir projeler için muhasebeyi yapılandırma makalesi</span><span class="sxs-lookup"><span data-stu-id="2a843-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="2a843-156">Sabit fiyat geliri tahmin projeleri</span><span class="sxs-lookup"><span data-stu-id="2a843-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="2a843-157">Gelir tahminlerini yönetme</span><span class="sxs-lookup"><span data-stu-id="2a843-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="2a843-158">Tamamlama maliyeti yöntemleri</span><span class="sxs-lookup"><span data-stu-id="2a843-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]