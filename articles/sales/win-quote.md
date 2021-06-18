---
title: Teklifi kapatma
description: Bu konuda, Project Operations'ta teklifleri kapatma hakkında bilgiler sağlanmaktadır.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3f46bf61bc3e492a648d65e86750a25609d5ab7a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995960"
---
# <a name="close-a-quote"></a><span data-ttu-id="a85ac-103">Teklifi kapatma</span><span class="sxs-lookup"><span data-stu-id="a85ac-103">Close a quote</span></span>

<span data-ttu-id="a85ac-104">_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="a85ac-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="a85ac-105">Proje teklifi Kazanıldı veya Kaybedildi olarak kapatılabilir.</span><span class="sxs-lookup"><span data-stu-id="a85ac-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="a85ac-106">Microsoft Dynamics 365 Project Operations'ta tekliflerde Etkinleştirme ve Düzeltme işlevleri desteklenmediğinden bir taslak teklifi kapatabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a85ac-106">Because the functions Activate and Revise are not supported on quotes in Microsoft Dynamics 365 Project Operations, you can close a draft quote.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="a85ac-107">Teklifi Kazanıldı olarak kapatma</span><span class="sxs-lookup"><span data-stu-id="a85ac-107">Close a quote as Won</span></span>

<span data-ttu-id="a85ac-108">Proje teklifini Kazanıldı olarak kapatmak teklifin durumunu **Kapalı** ve durum açıklamasını **Kazanıldı** olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a85ac-108">Closing a project quote as Won will set the status of the quote to **Closed** and status reason to **Won**.</span></span> <span data-ttu-id="a85ac-109">Tekliflerin kapatılması teklifi salt okunur yapar ve tüm teklif bilgileriyle bir taslak proje sözleşmesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a85ac-109">Closing the quotes makes it read-only and creates a draft project contract with all the quote information.</span></span> <span data-ttu-id="a85ac-110">Kapatılan bir teklif yeniden açılamayacağından, teklifi kapatmadan önce bir onay iletişim kutusu değişikliklerinizi onaylatacaktır.</span><span class="sxs-lookup"><span data-stu-id="a85ac-110">Because a closed quote can't be reopened, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="a85ac-111">Proje teklifinden oluşturulan proje sözleşmesi, Project Operations'ın Proje yönetimi ve muhasebe modülünde de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="a85ac-111">The project contract created from a project quote is also made available in the Project management and accounting module of Project Operations.</span></span> <span data-ttu-id="a85ac-112">Proje sözleşmesi, herhangi bir satırında bir projeye eşlenmemişse bu proje sözleşmesi, etkin olmayan bir proje sözleşmesi olarak kullanıma sunulur ve bir proje, sözleşme satırlarından en az birine eşlendiğinde etkin olur.</span><span class="sxs-lookup"><span data-stu-id="a85ac-112">If a project contract is not mapped to a project on any of its lines, this project contract is made available as an inactive project contract and becomes active as soon as a project is mapped to at least one of its contract lines.</span></span>

<span data-ttu-id="a85ac-113">Teklif bir fırsata eklenirse fırsatla ilgili diğer tüm proje teklifleri otomatik olarak Kaybedildi olarak kapatılır.</span><span class="sxs-lookup"><span data-stu-id="a85ac-113">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="a85ac-114">Teklifi Kazanıldı olarak kapatmanın finansal etkisi</span><span class="sxs-lookup"><span data-stu-id="a85ac-114">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="a85ac-115">Taslak teklife ekliyken bir projeye kaydedilen süre için herhangi bir gerçek değer varsa yalnızca zaman veya giderin maliyeti kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="a85ac-115">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="a85ac-116">Teklif Kazanıldı olarak kapatıldıktan sonra uygulama, eski maliyet gerçek değerlerini tersine çevirerek maliyetleri yeniden düzenler ve yeni maliyet gerçek değerlerini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a85ac-116">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="a85ac-117">Uygulama, ilgili proje sözleşme satırının Faturalama yöntemine göre bu maliyet gerçek değerlerini işler.</span><span class="sxs-lookup"><span data-stu-id="a85ac-117">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="a85ac-118">Maliyet gerçek değerleri bir zaman ve malzeme sözleşme satırına başvuruyorsa sistem, teklifin kapatıldığı ve proje sözleşmesinin oluşturulduğu andaki ilgili faturalanmamış satış gerçek değerlerini otomatik olarak oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a85ac-118">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="a85ac-119">Maliyet gerçek değerleri sabit fiyatlı bir sözleşme satırına başvuruyorsa uygulama, proje sözleşmesi müşterileri için bölünmüş fatura kurallarına göre maliyet gerçek değerlerini yeniden işlemeyi durdurur.</span><span class="sxs-lookup"><span data-stu-id="a85ac-119">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

<span data-ttu-id="a85ac-120">Yeniden işlenmiş tüm gerçek değerler, Proje muhasebecisinin incelemesi, güncelleştirmesi ve Genel muhasebeye göndermesi için Proje yönetimi ve muhasebe modülünde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="a85ac-120">All reprocessed actuals are available in the Project management and accounting module for the Project accountant to review, update, and post to the General ledger.</span></span> 

## <a name="close-a-quote-as-lost"></a><span data-ttu-id="a85ac-121">Teklifi Kaybedildi olarak kapatma</span><span class="sxs-lookup"><span data-stu-id="a85ac-121">Close a quote as Lost</span></span>

<span data-ttu-id="a85ac-122">Proje teklifinin Kaybedildi olarak kapatılması, durumu **Kapalı** ve durum açıklamasını **Kaybedildi** olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a85ac-122">Closing a project quote as Lost will set the status to **Closed** and status reason to **Lost**.</span></span> <span data-ttu-id="a85ac-123">Teklifin kapatılması onu salt okunur yapar.</span><span class="sxs-lookup"><span data-stu-id="a85ac-123">Closing the quote makes it read-only.</span></span> <span data-ttu-id="a85ac-124">Kapatılan bir teklif yeniden açılamayacağından, teklifi kapatmadan önce bir onay iletişim kutusu değişikliklerinizi onaylatacaktır.</span><span class="sxs-lookup"><span data-stu-id="a85ac-124">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="a85ac-125">Kaybedildi olarak kapatılan proje teklifinin herhangi bir satırında başvurulan bir proje varsa bu proje de Kapalı olarak işaretlenir ve o günden sonraki tüm kaynak ayırmaları iptal edilir.</span><span class="sxs-lookup"><span data-stu-id="a85ac-125">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="a85ac-126">Project Operations'ta bir teklifin Kazanıldı veya Kaybedildi olarak kapatılması, Fırsat'ın bu durumunu etkilemez ve fırsat el ile kapatılana kadar açık kalır.</span><span class="sxs-lookup"><span data-stu-id="a85ac-126">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]