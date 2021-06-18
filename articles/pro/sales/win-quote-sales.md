---
title: Teklifi kapatma - lite
description: Bu konuda, Project Operations'ta bir teklifi kapatma hakkında bilgiler sağlanmaktadır.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 75345fed57dcbdb84f2a82587c7d0c152530c72b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994160"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="4400f-103">Teklifi kapatma - lite</span><span class="sxs-lookup"><span data-stu-id="4400f-103">Close a quote - lite</span></span>

<span data-ttu-id="4400f-104">_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_</span><span class="sxs-lookup"><span data-stu-id="4400f-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4400f-105">Proje teklifi Kazanıldı veya Kaybedildi olarak kapatılabilir.</span><span class="sxs-lookup"><span data-stu-id="4400f-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="4400f-106">Tekliflerdeki Etkinleştirme ve Düzeltme işlemleri Microsoft Dynamics 365 Project Operations uygulamasında desteklenmediği için taslak teklif kapatılabilir.</span><span class="sxs-lookup"><span data-stu-id="4400f-106">A draft quote can be closed because the Activate and Revise operations on quotes isn't supported in Microsoft Dynamics 365 Project Operations.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="4400f-107">Teklifi Kazanıldı olarak kapatma</span><span class="sxs-lookup"><span data-stu-id="4400f-107">Close a quote as Won</span></span>

<span data-ttu-id="4400f-108">Proje teklifini Kazandı olarak kapattığınızda durum Kapalı olarak ayarlanır ve durum açıklaması Kazanıldı olur.</span><span class="sxs-lookup"><span data-stu-id="4400f-108">When you close a project quote as Won, the status is set to Closed and the status reason is Won.</span></span> <span data-ttu-id="4400f-109">Teklifin kapatılması, proje teklifini salt okunur yapar ve teklif bilgilerini içeren bir taslak proje sözleşmesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4400f-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="4400f-110">Kapatılan bir teklif yeniden açılamadığı için bir onay iletişim kutusuyla değişikliklerinizi onaylamanız istenir.</span><span class="sxs-lookup"><span data-stu-id="4400f-110">Because a closed quote can't be reopened, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="4400f-111">Teklif bir fırsata eklenirse fırsatla ilgili diğer tüm proje teklifleri otomatik olarak Kaybedildi olarak kapatılır.</span><span class="sxs-lookup"><span data-stu-id="4400f-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="4400f-112">Teklifi Kazanıldı olarak kapatmanın finansal etkisi</span><span class="sxs-lookup"><span data-stu-id="4400f-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="4400f-113">Taslak teklife eklenmiş bir projede zaman için herhangi bir gerçek değer varsa yalnızca zamanın maliyeti veya gider kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="4400f-113">If there are any actuals for time on a project while is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="4400f-114">Teklif Kazanıldı olarak kapatıldıktan sonra uygulama, eski maliyet gerçek değerlerini tersine çevirerek maliyetleri yeniden düzenler ve yeni maliyet gerçek değerlerini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4400f-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="4400f-115">Uygulama, ilgili proje sözleşme satırının Faturalama yöntemine göre bu maliyet gerçek değerlerini işler.</span><span class="sxs-lookup"><span data-stu-id="4400f-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="4400f-116">Maliyet gerçek değerleri bir zaman ve malzeme sözleşmesi satırına başvuruyorsa teklif kapatıldığında ve proje sözleşmesi oluşturulduğunda karşılık gelen faturalanmamış satış gerçek değerleri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4400f-116">If the cost actuals reference a time and material contract line, corresponding unbilled sales actuals are created for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="4400f-117">Maliyet gerçek değerleri sabit fiyatlı bir sözleşme satırına başvuruyorsa uygulama, proje sözleşmesi müşterileri için bölünmüş fatura kurallarını temel alan maliyet gerçek değerlerini yeniden işlemeyi durdurur.</span><span class="sxs-lookup"><span data-stu-id="4400f-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals that are based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="4400f-118">Teklifi kaybedildi olarak kapatma:</span><span class="sxs-lookup"><span data-stu-id="4400f-118">Closing a quote as lost:</span></span>

<span data-ttu-id="4400f-119">Proje teklifini Kaybedildi olarak kapattığınızda durum, Kapalı olarak ayarlanır ve durum açıklaması Kaybedildi olur.</span><span class="sxs-lookup"><span data-stu-id="4400f-119">When you close a project quote as Lost, the status is set to Closed and status reason is Lost.</span></span> <span data-ttu-id="4400f-120">Teklifin kapatılması, proje teklifini salt okunur yapar.</span><span class="sxs-lookup"><span data-stu-id="4400f-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="4400f-121">Kapatılan bir teklif yeniden açılamayacağından, teklifi kapatmadan önce bir onay iletişim kutusu değişikliklerinizi onaylatacaktır.</span><span class="sxs-lookup"><span data-stu-id="4400f-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="4400f-122">Kaybedildi olarak kapatılan proje teklifi, herhangi bir satırında bir projeye başvuruyorsa bu proje de Kapalı olarak işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="4400f-122">If the project quote that is closed as Lost references a project on any of its lines, that project is also marked as Closed.</span></span> <span data-ttu-id="4400f-123">Bu günden ileriye doğru kaynak kayıtları iptal edilir.</span><span class="sxs-lookup"><span data-stu-id="4400f-123">Any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="4400f-124">Project Operations'ta bir teklifin Kazanıldı veya Kaybedildi olarak kapatılması, Fırsat'ın bu durumunu etkilemez ve fırsat el ile kapatılana kadar açık kalır.</span><span class="sxs-lookup"><span data-stu-id="4400f-124">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]