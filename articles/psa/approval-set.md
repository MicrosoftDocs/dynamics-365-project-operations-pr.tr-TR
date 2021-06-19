---
title: Onay kümeleri
description: Bu konu; onay kümesi, istekler ve bu işlemlerin alt kümeleri hakkında bilgi sağlar.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ac73313420029ece740d0bdb9c21c7abaa9defc6
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116895"
---
# <a name="approval-sets"></a><span data-ttu-id="01f65-103">Onay kümeleri</span><span class="sxs-lookup"><span data-stu-id="01f65-103">Approval sets</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="01f65-104">Onay kümeleri, onaylama isteklerini işlemlerin daha küçük alt kümeleri olarak gruplandırır.</span><span class="sxs-lookup"><span data-stu-id="01f65-104">Approval sets group approval requests together into smaller subsets of operations.</span></span> <span data-ttu-id="01f65-105">Bu gruplandırma, onayların Projeye göre sıralı işlenmesine ve yeniden deneme ve sıralama yapılmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="01f65-105">This grouping allows approvals to be processed in order by Project and allows for retrying and sequencing.</span></span> <span data-ttu-id="01f65-106">Gruplandırma, büyük miktarda onaylama için onay işlemenin güvenilirliğini ve izlenebilirliğini artırır.</span><span class="sxs-lookup"><span data-stu-id="01f65-106">Grouping improves the reliability and traceability of approval processing for large volumes of approvals.</span></span>

<span data-ttu-id="01f65-107">Onay kümeleri, ilgili kayıtların genel işlenme durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="01f65-107">Approval sets indicate the overall processing state of their related records.</span></span> <span data-ttu-id="01f65-108">Onay kaydı bir onay kümesi kullanılarak işlendiğinde, kayıt **Gönderildi** durumundan **Onaylandı** durumuna taşınır ve onay kümesiyle bağlantısı kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="01f65-108">When an approval record is processed using an approval set, the record moves from **Submitted** to **Approved**, and is unlinked from the approval set.</span></span> <span data-ttu-id="01f65-109">Bir kayıt onaylanmak üzere gönderildiğinde başarısız olursa, kayıt **Gönderildi** durumunda kalır ve onay kümesi başarısız olarak işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="01f65-109">If a record fails when it is submitted for approval, the record remains in a status of **Submitted** and the approval set is marked as failed.</span></span> <span data-ttu-id="01f65-110">Onay kümesi, hatanın hata mesajını günlüğe kaydeder.</span><span class="sxs-lookup"><span data-stu-id="01f65-110">The approval set logs the error message of the failure.</span></span>

## <a name="processing-approvals-and-approval-sets"></a><span data-ttu-id="01f65-111">Onayları ve onay kümelerini işleme</span><span class="sxs-lookup"><span data-stu-id="01f65-111">Processing approvals and approval sets</span></span>
<span data-ttu-id="01f65-112">İşlenmek üzere kuyruğa alınmış onaylar, **İşlenen Onaylar** görünümünde görünür.</span><span class="sxs-lookup"><span data-stu-id="01f65-112">Approvals that are queued for processing are visible in the **Processing Approvals** view.</span></span> <span data-ttu-id="01f65-113">Sistem, önceki denemeler başarısız olduysa bir onayı yeniden denemek de dahil olmak üzere, tüm girişleri birçok defa zaman uyumsuz olarak işlemeye çalışır.</span><span class="sxs-lookup"><span data-stu-id="01f65-113">The system tries to process all the entries multiple times asynchronously, including retrying an approval if previous attempts failed.</span></span>

<span data-ttu-id="01f65-114">**Onay Kümesi Yaşam Süresi** alanı, başarısız olarak işaretlenmeden önce kümeyi işlemek için kalan deneme sayısını kaydeder.</span><span class="sxs-lookup"><span data-stu-id="01f65-114">The **Approval Set Lifetime** field records the number of attempts left to process the set before it's marked as failed.</span></span>

## <a name="failed-approvals-and-approval-sets"></a><span data-ttu-id="01f65-115">Başarısız onaylar ve onay kümeleri</span><span class="sxs-lookup"><span data-stu-id="01f65-115">Failed approvals and approval sets</span></span>
<span data-ttu-id="01f65-116">**Başarısız Onaylar** görünümü, kullanıcı müdahalesi gerektiren tüm onayları listeler.</span><span class="sxs-lookup"><span data-stu-id="01f65-116">The **Failed Approvals** view lists all approvals that require user intervention.</span></span> <span data-ttu-id="01f65-117">Başarısızlığın nedenini belirlemek için ilgili onay kümesi günlüklerini açın.</span><span class="sxs-lookup"><span data-stu-id="01f65-117">Open the associated approval set logs to identify the cause of the failure.</span></span>
<span data-ttu-id="01f65-118">**Yeniden dene**'yi seçtiğinizde onay kümesi ömür sayısına ekleme yapılır, onay kümesi tekrar **İşleniyor** durumuna taşınır ve kalan kayıtları işlenmeye çalışılır.</span><span class="sxs-lookup"><span data-stu-id="01f65-118">Selecting **Retry** adds to the approval set lifetime count, moves the approval set back to a status of **Processing**, and attempts to process the remaining records.</span></span>

## <a name="configure-approval-sets"></a><span data-ttu-id="01f65-119">Onay kümelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="01f65-119">Configure approval sets</span></span>

###  <a name="enable-the-approval-sets-feature"></a><span data-ttu-id="01f65-120">Onay kümeleri özelliğini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="01f65-120">Enable the Approval sets feature</span></span>
<span data-ttu-id="01f65-121">Onay kümeleri özelliğini etkinleştirmeden önce, işlenmekte olan onay olmadığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="01f65-121">Before you enable the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="01f65-122">**Proje parametreleri** sayfasına gidin ve **Özellik Kontrolü** > **Modern Onayları Etkinleştir** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="01f65-122">Go to the **Project parameters** page and select **Feature Control** > **Enable Modern Approvals**.</span></span>

### <a name="turn-off-the-approval-sets-feature"></a><span data-ttu-id="01f65-123">Onay kümeleri özelliğini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="01f65-123">Turn off the Approval sets feature</span></span>
<span data-ttu-id="01f65-124">Onay kümeleri özelliğini devre dışı bırakmadan önce, işlenmekte olan onay olmadığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="01f65-124">Before you turn off the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="01f65-125">**Proje Parametreleri** sayfasına gidin ve **Özellik Kontrolü** > **Modern Onayları Devre Dışı Bırak** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="01f65-125">Go to the **Project Parameters** page and select **Feature Control** > **Disable Modern Approvals**.</span></span>

### <a name="configuring-the-asynchronous-threshold"></a><span data-ttu-id="01f65-126">Zaman uyumsuz eşiği yapılandırma</span><span class="sxs-lookup"><span data-stu-id="01f65-126">Configuring the asynchronous threshold</span></span> 
<span data-ttu-id="01f65-127">Onay kümeleri oluşturulduğunda, onay için seçilen kayıt sayısı belirtilen eşiği aştığında, işlem arka plana gider.</span><span class="sxs-lookup"><span data-stu-id="01f65-127">When approval sets are created, processing moves to the background when the selected number of records for approval exceeds the indicated threshold.</span></span> <span data-ttu-id="01f65-128">Onay işleminin zaman uyumlu mu zaman uyumsuz mu çalıştırılması gerektiğini belirlemek için **Zaman Uyumsuz Eşik** alanını kullanın.</span><span class="sxs-lookup"><span data-stu-id="01f65-128">Use the **Asynchronous Threshold** field to configure when approval processing should be run synchronously or asynchronously.</span></span>
<span data-ttu-id="01f65-129">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="01f65-129">Valid values are:</span></span>

  - <span data-ttu-id="01f65-130">Sıfır: Tüm istekler zaman uyumsuz olarak işlenmelidir.</span><span class="sxs-lookup"><span data-stu-id="01f65-130">Zero: All requests should be processed asynchronously.</span></span> 
  - <span data-ttu-id="01f65-131">Sıfırdan büyük sayılar: Onaylar, yalnızca gönderilen onay sayısı bu değeri aştığında zaman uyumsuz olarak işlenir.</span><span class="sxs-lookup"><span data-stu-id="01f65-131">Numbers greater than zero: Approvals are processed asynchronously only when the submitted number of approvals exceeds this value.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
