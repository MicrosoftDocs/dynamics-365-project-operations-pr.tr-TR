---
title: Gider ilkelerini tanımla
description: Gider raporlarını ve seyahat taleplerini girerken ve gönderirken çalışanlarınızın izlemesi gereken gider ilkelerini tanımlayabilirsiniz.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fa108db9aa0d2a22c35d2d046917ddae1f3842c1
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001900"
---
# <a name="define-expense-policies"></a><span data-ttu-id="de7fd-103">Gider ilkelerini tanımla</span><span class="sxs-lookup"><span data-stu-id="de7fd-103">Define expense policies</span></span>

<span data-ttu-id="de7fd-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="de7fd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="de7fd-105">Gider raporlarını ve seyahat taleplerini girerken ve gönderirken çalışanlarınızın izlemesi gereken ilkeleri tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="de7fd-105">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="de7fd-106">Gider ilkelerinin uygulanması, giderleri etkin şekilde yönetmenize yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="de7fd-106">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="de7fd-107">Örneğin, New York şehrinde otel giderleri için, gecelik giderin 250 doları aşmaması gerektiğini bildiren bir ilke ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="de7fd-107">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="de7fd-108">Bir çalışan, oda fiyatının bu tutarı aştığı bir gider raporu veya seyahat talebi gönderdiğinde, sistem</span><span class="sxs-lookup"><span data-stu-id="de7fd-108">If a worker submits an expense report or travel requisition where the room rate exceeds this amount, the system will notify the</span></span>         
<span data-ttu-id="de7fd-109">çalışanın gider için ilkede belirtilen miktarın aşıldığı konusunda uyarır.</span><span class="sxs-lookup"><span data-stu-id="de7fd-109">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="de7fd-110">İlkeyi tanımlarken çalışanın alacağı iletiyi </span><span class="sxs-lookup"><span data-stu-id="de7fd-110">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="de7fd-111">yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="de7fd-111">define the policy.</span></span>      
        
<span data-ttu-id="de7fd-112">Üç tür ilke tanımlayabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="de7fd-112">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="de7fd-113">**Uyarı**: Çalışanın bir gider raporu ya da seyahat talebi göndermesine izin verir, ancak gider tüm onaylayanlar ve daha sonra </span><span class="sxs-lookup"><span data-stu-id="de7fd-113">**Warning**: Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>         
  <span data-ttu-id="de7fd-114">raporlama için işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="de7fd-114">for later reporting.</span></span>        

- <span data-ttu-id="de7fd-115">**Hata**: Çalışanın, gider raporunu veya seyahat talebini göndermeden önce gideri ilkeye uygun olarak gözden geçirmesi istenir.</span><span class="sxs-lookup"><span data-stu-id="de7fd-115">**Error**: Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>        
 
 - <span data-ttu-id="de7fd-116">**Gerekçe**: Gider raporunu veya seyahat talebini göndermeden önce çalışan veya yöneticinin ilkede belirtilen tutarın aşılması konusunda bir gerekçe girmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="de7fd-116">**Justification**: Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="de7fd-117">İlke ipuçları</span><span class="sxs-lookup"><span data-stu-id="de7fd-117">Policy tips</span></span>
<span data-ttu-id="de7fd-118">Burada, gider yönetimi konusunda yeni ilkeler oluştururken size yardımcı olabilecek birkaç öneriye yer verilmektedir:</span><span class="sxs-lookup"><span data-stu-id="de7fd-118">Here are a few suggestions that can assist you when creating new policies for expense management:</span></span> 

- <span data-ttu-id="de7fd-119">İlkeler tarih etkindir; giderin gerçekleştiği tarihten sonraki bir tarihte oluşturulmuşsa ilkenin geçerli olmayacağı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="de7fd-119">Policies are date effective which means a policy won't take effect if it's created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="de7fd-120">Örneğin, bugün yemek giderinin 50 doları aşmayacağı şekilde yeni bir ilke oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="de7fd-120">For example, you create a new policy today to enforce a maximum meal expense of $50.</span></span> <span data-ttu-id="de7fd-121">Dün girilen tüm var olan giderler bu ilkeye göre denetlenmez.</span><span class="sxs-lookup"><span data-stu-id="de7fd-121">Any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
- <span data-ttu-id="de7fd-122">Dökümü alınabilecek bir gider kategorisi için ilke oluştururken, masraf satırı türü için bir koşul eklemeyi gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="de7fd-122">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="de7fd-123">Makbuz istenmesi gibi bazı ilkeler, dökümü bulunmayan satırlar için anlamlı olmayabilir.</span><span class="sxs-lookup"><span data-stu-id="de7fd-123">Some policies, such as requiring a receipt, may not make sense for itemized lines.</span></span> <span data-ttu-id="de7fd-124">Bu durumda ilke yalnızca başlık satırına veya dökümü alınmamış bir satıra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="de7fd-124">In this situation, the policy only is applied to the header line or a non-itemized line.</span></span> 
- <span data-ttu-id="de7fd-125">Gider yönetimi ilkeleri varsayılan olarak kaynak varlığa göre değerlendirilir.</span><span class="sxs-lookup"><span data-stu-id="de7fd-125">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="de7fd-126">Şirketler arası senaryolarda, bu ilkeyi hedef varlığa (ödünç alan varlık yerine) göre değerlendirilecek şekilde ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="de7fd-126">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="de7fd-127">İlkeleri hedef varlığa göre çalıştırmak için, **Özellik yönetimi** çalışma alanındaki **Gider ilkesini ödünç alan tüzel kişiye göre değerlendir** özelliğini etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="de7fd-127">To run the policies against the destination entity, turn on the **Evaluate Expense policy against borrowing legal entity** feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="de7fd-128">İlkeler ne zaman değerlendirilir</span><span class="sxs-lookup"><span data-stu-id="de7fd-128">When to evaluate policies</span></span>

<span data-ttu-id="de7fd-129">Gider yönetimi parametrelerinde, bir satır kaydedildiğinde veya gider raporu gönderildiğinde gider yönetimi ilkelerini değerlendirmeyi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="de7fd-129">In expense management parameters, you can select to evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="de7fd-130">Bir satır kaydedildiğinde değerlendirmeyi seçerseniz, kullanıcılar gider raporlarının hepsini aynı anda tamamlamak için ne yapmaları gerektiği konusunda daha önceden görünürlüğe sahip olur.</span><span class="sxs-lookup"><span data-stu-id="de7fd-130">If you choose to evaluate when a line is saved, users will have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="de7fd-131">Aksi takdirde, iş akışına gönderim sırasında ilke değerlendirmesini erteleyebilir ve sonda da doğrulayarak zaman kazanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="de7fd-131">Otherwise, you can delay policy evaluation and save time by validating at the end, during the submission to workflow.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]