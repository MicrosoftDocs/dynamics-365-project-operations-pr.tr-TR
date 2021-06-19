---
title: Gelir tanımaya genel bakış
description: Bu konu Project Operations'ta gelir tanıma hakkında bilgi sağlar.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f5f962572c6ec0298d2d91d33f83e4120a498a6f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013780"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="928be-103">Gelir tanımaya genel bakış</span><span class="sxs-lookup"><span data-stu-id="928be-103">Revenue recognition overview</span></span>

<span data-ttu-id="928be-104">_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="928be-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="928be-105">Dynamics 365 Project Operations uygulamasında gelir tanıma ilkeleri, bir proje veya projenin bir kısmı için seçilen faturalama yöntemine göre değişiklik gösterir.</span><span class="sxs-lookup"><span data-stu-id="928be-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="928be-106">Bu konu Project Operations'ta gelir tanıma hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="928be-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="928be-107">Zaman ve malzeme faturalama yöntemi kullanılarak muhasebeleştirilen işlemler</span><span class="sxs-lookup"><span data-stu-id="928be-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="928be-108">Maliyet ve gelir tanıma birbirine bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="928be-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="928be-109">İşlem maliyeti ve faturalanmayan satışlar [Project Operations Entegrasyon günlüğü](../project-accounting/project-operations-integration-journal.md) kullanılarak gönderilir.</span><span class="sxs-lookup"><span data-stu-id="928be-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="928be-110">Proje maliyeti ve gelir profili, faturalanmayan satış işlemlerinin genel muhasebeye gönderilip gönderilmediğini belirler.</span><span class="sxs-lookup"><span data-stu-id="928be-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="928be-111">**Gelir tahakkuku** seçilirse sistem, gönderim sırasında **WIP satış değeri** ve **Tahakkuk eden gelir satış değeri** hesaplarını kullanır.</span><span class="sxs-lookup"><span data-stu-id="928be-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="928be-112">Aşağıda bu yöntemin bir örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="928be-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="928be-113">İşlem türü</span><span class="sxs-lookup"><span data-stu-id="928be-113">Transaction type</span></span> | <span data-ttu-id="928be-114">Banka/Kredi</span><span class="sxs-lookup"><span data-stu-id="928be-114">Debit/Credit</span></span> | <span data-ttu-id="928be-115">Miktar</span><span class="sxs-lookup"><span data-stu-id="928be-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="928be-116">WIP Satış değeri</span><span class="sxs-lookup"><span data-stu-id="928be-116">WIP Sales value</span></span> | <span data-ttu-id="928be-117">Banka</span><span class="sxs-lookup"><span data-stu-id="928be-117">Debit</span></span> | <span data-ttu-id="928be-118">100</span><span class="sxs-lookup"><span data-stu-id="928be-118">100</span></span> |
  | <span data-ttu-id="928be-119">Tahakkuk eden gelir satış değeri</span><span class="sxs-lookup"><span data-stu-id="928be-119">Accrued revenue sales value</span></span> | <span data-ttu-id="928be-120">Kredi</span><span class="sxs-lookup"><span data-stu-id="928be-120">Credit</span></span> | <span data-ttu-id="928be-121">100</span><span class="sxs-lookup"><span data-stu-id="928be-121">100</span></span> |

- <span data-ttu-id="928be-122">Gelir, faturalama sırasında tanınır.</span><span class="sxs-lookup"><span data-stu-id="928be-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="928be-123">Sistem, gönderim sırasında **Faturalanan gelir** hesabını kullanır.</span><span class="sxs-lookup"><span data-stu-id="928be-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="928be-124">Aşağıda bu yöntemin bir örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="928be-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="928be-125">İşlem türü</span><span class="sxs-lookup"><span data-stu-id="928be-125">Transaction type</span></span> | <span data-ttu-id="928be-126">Banka/Kredi</span><span class="sxs-lookup"><span data-stu-id="928be-126">Debit/Credit</span></span> | <span data-ttu-id="928be-127">Miktar</span><span class="sxs-lookup"><span data-stu-id="928be-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="928be-128">Müşteri bakiyesi</span><span class="sxs-lookup"><span data-stu-id="928be-128">Customer balance</span></span> | <span data-ttu-id="928be-129">Banka</span><span class="sxs-lookup"><span data-stu-id="928be-129">Debit</span></span> | <span data-ttu-id="928be-130">120</span><span class="sxs-lookup"><span data-stu-id="928be-130">120</span></span> |
  | <span data-ttu-id="928be-131">Satış vergisi borçları</span><span class="sxs-lookup"><span data-stu-id="928be-131">Sales tax payable</span></span> | <span data-ttu-id="928be-132">Kredi</span><span class="sxs-lookup"><span data-stu-id="928be-132">Credit</span></span> | <span data-ttu-id="928be-133">20</span><span class="sxs-lookup"><span data-stu-id="928be-133">20</span></span> |
  | <span data-ttu-id="928be-134">Faturalanan Gelir</span><span class="sxs-lookup"><span data-stu-id="928be-134">Invoiced Revenue</span></span> | <span data-ttu-id="928be-135">Kredi</span><span class="sxs-lookup"><span data-stu-id="928be-135">Credit</span></span> | <span data-ttu-id="928be-136">100</span><span class="sxs-lookup"><span data-stu-id="928be-136">100</span></span> |

- <span data-ttu-id="928be-137">Faturalanan satışlar gönderildiğinde gelir tahakkuk etmişse sistem, faturalamada tahakkuk eden geliri tersine çevirir.</span><span class="sxs-lookup"><span data-stu-id="928be-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="928be-138">İşlem türü</span><span class="sxs-lookup"><span data-stu-id="928be-138">Transaction type</span></span> | <span data-ttu-id="928be-139">Banka/Kredi</span><span class="sxs-lookup"><span data-stu-id="928be-139">Debit/Credit</span></span> | <span data-ttu-id="928be-140">Miktar</span><span class="sxs-lookup"><span data-stu-id="928be-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="928be-141">WIP Satış değeri</span><span class="sxs-lookup"><span data-stu-id="928be-141">WIP Sales value</span></span> | <span data-ttu-id="928be-142">Kredi</span><span class="sxs-lookup"><span data-stu-id="928be-142">Credit</span></span> | <span data-ttu-id="928be-143">100</span><span class="sxs-lookup"><span data-stu-id="928be-143">100</span></span> |
  | <span data-ttu-id="928be-144">Tahakkuk eden gelir satış değeri</span><span class="sxs-lookup"><span data-stu-id="928be-144">Accrued revenue sales value</span></span> | <span data-ttu-id="928be-145">Banka</span><span class="sxs-lookup"><span data-stu-id="928be-145">Debit</span></span> | <span data-ttu-id="928be-146">100</span><span class="sxs-lookup"><span data-stu-id="928be-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="928be-147">Sabit fiyatlı faturalama yöntemi kullanılarak muhasebeleştirilen işlemler</span><span class="sxs-lookup"><span data-stu-id="928be-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="928be-148">Maliyet ve gelir tanıma birbirinden ayrıdır.</span><span class="sxs-lookup"><span data-stu-id="928be-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="928be-149">İşlem maliyeti [Project Operations Entegrasyon günlüğü](../project-accounting/project-operations-integration-journal.md) kullanılarak gönderilir.</span><span class="sxs-lookup"><span data-stu-id="928be-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="928be-150">Faturalanmayan satış işlemleri oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="928be-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="928be-151">Proje maliyeti ve gelir profili **Proje tamamlama hesaplamaları için kullanılan ilke**, **WIP yok** olarak ayarlanmışsa gelir, faturalama sırasında tanınabilir.</span><span class="sxs-lookup"><span data-stu-id="928be-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="928be-152">Bu yöntemi yalnızca kısa vadeli, basit projeler için kullanın.</span><span class="sxs-lookup"><span data-stu-id="928be-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="928be-153">Gelir, **Tamamlanan sözleşme** veya **Tamamlanma yüzdesi gelir tanıma** yöntemiyle sabit fiyatlı gelir tahminleri kullanılarak tanınır.</span><span class="sxs-lookup"><span data-stu-id="928be-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="928be-154">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="928be-154">Additional resources</span></span>
[<span data-ttu-id="928be-155">Faturalanabilir projeler için muhasebeyi yapılandırma makalesi</span><span class="sxs-lookup"><span data-stu-id="928be-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="928be-156">Sabit fiyat geliri tahmin projeleri</span><span class="sxs-lookup"><span data-stu-id="928be-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="928be-157">Gelir tahminlerini yönetme</span><span class="sxs-lookup"><span data-stu-id="928be-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="928be-158">Tamamlama maliyeti yöntemleri</span><span class="sxs-lookup"><span data-stu-id="928be-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]