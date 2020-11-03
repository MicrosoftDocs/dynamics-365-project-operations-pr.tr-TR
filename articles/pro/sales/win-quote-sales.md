---
title: Teklifleri kapatma
description: Bu konuda, Project Operations'ta bir teklifi kapatma hakkında bilgiler sağlanmaktadır.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cc3b2cdeb1ac46b7d927c1f96e94e9154d3eebf8
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086245"
---
# <a name="close-quotes"></a><span data-ttu-id="c8750-103">Teklifleri kapatma</span><span class="sxs-lookup"><span data-stu-id="c8750-103">Close quotes</span></span> 

<span data-ttu-id="c8750-104">_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_</span><span class="sxs-lookup"><span data-stu-id="c8750-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c8750-105">Proje teklifi Kazanıldı veya Kaybedildi olarak kapatılabilir.</span><span class="sxs-lookup"><span data-stu-id="c8750-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="c8750-106">Tekliflerde Etkinleştirme ve Düzeltme işlemleri Microsoft Dynamics 365 Project Operations'ta desteklenmediğinden bir taslak teklif kapatılabilir.</span><span class="sxs-lookup"><span data-stu-id="c8750-106">The Activate and Revise operations on quotes is not supported in Microsoft Dynamics 365 Project Operations, so a draft quote can be closed.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="c8750-107">Teklifi Kazanıldı olarak kapatma</span><span class="sxs-lookup"><span data-stu-id="c8750-107">Close a quote as Won</span></span>

<span data-ttu-id="c8750-108">Proje teklifinin Kazanıldı olarak kapatılması, teklifin durumunu Kapalı ve durum açıklamasını Kazanıldı olarak ayarlanmış şekilde kapatır.</span><span class="sxs-lookup"><span data-stu-id="c8750-108">Closing a project quote as Won will close the quote with the status set to Closed and the status reason set to Won.</span></span> <span data-ttu-id="c8750-109">Teklifin kapatılması, proje teklifini salt okunur yapar ve teklif bilgilerini içeren bir taslak proje sözleşmesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c8750-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="c8750-110">Kapalı bir teklif yeniden açılamadığından ve değişiklikler geri alınamadığından değişiklikler yapılmadan önce bir onay iletişim kutusu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="c8750-110">Because a closed quote can't be reopened, a confirmation dialog There is a confirmation dialog before the changes are done since a closed quote cannot be re-opened and the changes are irreversible.</span></span>

<span data-ttu-id="c8750-111">Teklif bir fırsata eklenirse fırsatla ilgili diğer tüm proje teklifleri otomatik olarak Kaybedildi olarak kapatılır.</span><span class="sxs-lookup"><span data-stu-id="c8750-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="c8750-112">Teklifi Kazanıldı olarak kapatmanın finansal etkisi</span><span class="sxs-lookup"><span data-stu-id="c8750-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="c8750-113">Taslak teklife ekliyken bir projeye kaydedilen süre için herhangi bir gerçek değer varsa yalnızca zaman veya giderin maliyeti kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="c8750-113">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="c8750-114">Teklif Kazanıldı olarak kapatıldıktan sonra uygulama, eski maliyet gerçek değerlerini tersine çevirerek maliyetleri yeniden düzenler ve yeni maliyet gerçek değerlerini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c8750-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="c8750-115">Uygulama, ilgili proje sözleşme satırının Faturalama yöntemine göre bu maliyet gerçek değerlerini işler.</span><span class="sxs-lookup"><span data-stu-id="c8750-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="c8750-116">Maliyet gerçek değerleri bir zaman ve malzeme sözleşme satırına başvuruyorsa sistem, teklifin kapatıldığı ve proje sözleşmesinin oluşturulduğu andaki ilgili faturalanmamış satış gerçek değerlerini otomatik olarak oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c8750-116">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="c8750-117">Maliyet gerçek değerleri sabit fiyatlı bir sözleşme satırına başvuruyorsa uygulama, proje sözleşmesi müşterileri için bölünmüş fatura kurallarına göre maliyet gerçek değerlerini yeniden işlemeyi durdurur.</span><span class="sxs-lookup"><span data-stu-id="c8750-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="c8750-118">Teklifi kaybedildi olarak kapatma:</span><span class="sxs-lookup"><span data-stu-id="c8750-118">Closing a quote as lost:</span></span>

<span data-ttu-id="c8750-119">Proje teklifinin Kaybedildi olarak kapatılması, durumu Kapalı ve durum açıklamasını Kaybedildi olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c8750-119">Closing a project quote as Lost will set the status to Closed and status reason to Lost.</span></span> <span data-ttu-id="c8750-120">Teklifin kapatılması, proje teklifini salt okunur yapar.</span><span class="sxs-lookup"><span data-stu-id="c8750-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="c8750-121">Kapatılan bir teklif yeniden açılamayacağından, teklifi kapatmadan önce bir onay iletişim kutusu değişikliklerinizi onaylatacaktır.</span><span class="sxs-lookup"><span data-stu-id="c8750-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="c8750-122">Kaybedildi olarak kapatılan proje teklifinin herhangi bir satırında başvurulan bir proje varsa bu proje de Kapalı olarak işaretlenir ve o günden sonraki tüm kaynak ayırmaları iptal edilir.</span><span class="sxs-lookup"><span data-stu-id="c8750-122">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="c8750-123">Project Operations'ta bir teklifin Kazanıldı veya Kaybedildi olarak kapatılması, Fırsat'ın bu durumunu etkilemez ve fırsat el ile kapatılana kadar açık kalır.</span><span class="sxs-lookup"><span data-stu-id="c8750-123">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
