---
title: Gider ilkelerini ayarlama
description: Microsoft Dynamics 365 Finance'te Gider raporlarını ve seyahat taleplerini girerken ve gönderirken çalışanlarınızın izlemesi gereken gider ilkelerini tanımlayabilirsiniz.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9c014b0593a87ce50f09175b77d9cf498a65391e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271287"
---
# <a name="set-up-expense-policies"></a><span data-ttu-id="1a082-103">Gider ilkelerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="1a082-103">Set up expense policies</span></span>

<span data-ttu-id="1a082-104">Gider raporlarını ve seyahat taleplerini girerken ve gönderirken çalışanlarınızın izlemesi gereken ilkeleri tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1a082-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="1a082-105">Gider ilkelerinin uygulanması, giderleri etkin şekilde yönetmenize yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="1a082-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="1a082-106">Örneğin, New York şehrinde otel giderleri için, gecelik giderin 250 doları aşmaması gerektiğini bildiren bir ilke ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1a082-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="1a082-107">Bir çalışan, oda fiyatının bu tutarı aştığı bir gider raporu veya seyahat talebi gönderdiğinde, sistem</span><span class="sxs-lookup"><span data-stu-id="1a082-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="1a082-108">çalışanın gider için ilkede belirtilen miktarın aşıldığı konusunda uyarır.</span><span class="sxs-lookup"><span data-stu-id="1a082-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="1a082-109">İlkeyi tanımlarken çalışanın alacağı iletiyi </span><span class="sxs-lookup"><span data-stu-id="1a082-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="1a082-110">yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1a082-110">define the policy.</span></span>      
        
<span data-ttu-id="1a082-111">Üç tür ilke tanımlayabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="1a082-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="1a082-112">Uyarı: Çalışanın bir gider raporu ya da seyahat talebi göndermesine izin verir, ancak gider tüm onaylayanlar ve daha sonra </span><span class="sxs-lookup"><span data-stu-id="1a082-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="1a082-113">raporlama için işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="1a082-113">for later reporting.</span></span>        

- <span data-ttu-id="1a082-114">Hata: Çalışanın, gider raporunu veya seyahat talebini göndermeden önce gideri ilkeye uygun olarak gözden geçirmesi istenir.</span><span class="sxs-lookup"><span data-stu-id="1a082-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="1a082-115">Gerekçe: Gider raporunu veya seyahat talebini göndermeden önce çalışan veya yöneticinin ilkede belirtilen tutarın aşılması konusunda bir gerekçe girmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="1a082-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="1a082-116">İlke ipuçları</span><span class="sxs-lookup"><span data-stu-id="1a082-116">Policy tips</span></span>
<span data-ttu-id="1a082-117">Burada, gider yönetimi konusunda yeni ilkeler oluştururken size yardımcı olabilecek birkaç öneriye yer verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="1a082-117">Here are a few suggestions that can assist you when creating new policies for expense management.</span></span> 
* <span data-ttu-id="1a082-118">İlkeler tarih etkindir; giderin gerçekleştiği tarihten sonraki bir tarihte oluşturulmuşsa ilkenin geçerli olmayacağı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="1a082-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="1a082-119">Örneğin, $50 en fazla yemek gideri kullanmaya zorlamak için bugün yeni bir ilke oluşturuyorsanız, dün olarak girilen tüm varolan giderler bu ilkeye göre denetlenmez.</span><span class="sxs-lookup"><span data-stu-id="1a082-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="1a082-120">Dökümü alınabilecek bir gider kategorisi için ilke oluştururken, masraf satırı türü için bir koşul eklemeyi gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="1a082-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="1a082-121">Alındı bilgisi gerektirme gibi bazı ilkeler, dökümü bulunmayan satırlar için anlamlı olmayabilir ve yalnızca başlık satırına veya bir satır oluşturulmamış satıra uygulanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="1a082-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 
* <span data-ttu-id="1a082-122">Gider yönetimi ilkeleri varsayılan olarak kaynak varlığa göre değerlendirilir.</span><span class="sxs-lookup"><span data-stu-id="1a082-122">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="1a082-123">Şirketler arası senaryolarda, bu ilkeyi hedef varlığa (ödünç alan varlık yerine) göre değerlendirilecek şekilde ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1a082-123">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="1a082-124">İlkeleri hedef varlığa göre çalıştırmak için, **Özellik yönetimi** çalışma alanındaki "Gider ilkesini ödünç alan tüzel kişiye göre değerlendir" özelliğini etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="1a082-124">To run the policies against the destination entity, turn on the "Evaluate Expense policy against borrowing legal entity" feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="1a082-125">İlkeler ne zaman değerlendirilir</span><span class="sxs-lookup"><span data-stu-id="1a082-125">When to evaluate policies</span></span>

<span data-ttu-id="1a082-126">Gider yönetimi parametrelerinde, bir satır kaydedildiğinde veya gider raporu gönderildiğinde gider yönetimi ilkelerini değerlendirmeyi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1a082-126">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="1a082-127">Bir satır kaydedildiğinde değerlendirmeyi seçerseniz, kullanıcılar gider raporlarının hepsini aynı anda tamamlamak için ne yapmaları gerektiği konusunda daha önceden görünürlüğe sahip olur.</span><span class="sxs-lookup"><span data-stu-id="1a082-127">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="1a082-128">Aksi takdirde, iş akışına gönderim sırasında ilke değerlendirmesini erteleyebilir ve sonda da doğrulayarak zaman kazanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1a082-128">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]