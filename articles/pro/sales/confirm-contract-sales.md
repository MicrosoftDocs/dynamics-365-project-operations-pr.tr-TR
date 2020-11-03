---
title: Proje sözleşmesi onaylama
description: Bu konu, proje işlemlerinde bir sözleşmenin nasıl onaylanacağı hakkında bilgi verir.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: babce9c64098a9c87072786d914d2340251a8986
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086444"
---
# <a name="confirm-a-project-contract"></a><span data-ttu-id="46bce-103">Proje sözleşmesi onaylama</span><span class="sxs-lookup"><span data-stu-id="46bce-103">Confirm a project contract</span></span>

<span data-ttu-id="46bce-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="46bce-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="46bce-105">Dynamics 365 Project Operations Proje sözleşmesi, **Onaylanma** nedeni ile etkin olabilir veya **kaybedilme** nedeni ile kapatılabilir.</span><span class="sxs-lookup"><span data-stu-id="46bce-105">A project contract in Dynamics 365 Project Operations can be active with a reason of **Confirmed** , or closed with a reason of **Lost**.</span></span> <span data-ttu-id="46bce-106">Bir proje sözleşmesini onaylamadığınızda, durum **taslak** durumundan **etkin** durumuna güncelleştirilir ve durum açıklaması **Onaylandı** şeklindedir.</span><span class="sxs-lookup"><span data-stu-id="46bce-106">When you confirm a project contract, the status updates from **Draft** to **Active** and the status reason is **Confirmed**.</span></span> <span data-ttu-id="46bce-107">Etkin veya kapanmış bir sözleşme düzenlenemez veya yeniden açılamaz.</span><span class="sxs-lookup"><span data-stu-id="46bce-107">An active or closed contract can't be edited or reopened.</span></span> 

### <a name="financial-impact-of-confirming-a-project-contract"></a><span data-ttu-id="46bce-108">Bir proje sözleşmesini onaylama hakkında finansal etki</span><span class="sxs-lookup"><span data-stu-id="46bce-108">Financial impact of confirming a project contract</span></span>

<span data-ttu-id="46bce-109">Proje sözleşmesi onaylandıktan sonra uygulama, eski maliyet gerçek değerlerini tersine çevirerek maliyetleri yeniden düzenler ve yeni maliyet gerçek değerlerini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="46bce-109">After a project contract is confirmed, the application recalculates the costs by reversing the older cost actuals and creating new cost actuals.</span></span> <span data-ttu-id="46bce-110">Yeni maliyet fiileri, ardından Faturalama yöntemine göre bu maliyet gerçek değerlerini işler.</span><span class="sxs-lookup"><span data-stu-id="46bce-110">The new cost actuals are then processed based on the billing method of the associated project contract line.</span></span> <span data-ttu-id="46bce-111">Maliyet gerçek tutarları bir zaman ve malzeme sözleşme satırına başvuruda varsa, uygulama ilgili faturalandırılmaz satış fiili değerlerini otomatik olarak yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="46bce-111">If the cost actuals reference a Time and Material contract line, the application automatically re-creates corresponding unbilled sales actuals.</span></span> <span data-ttu-id="46bce-112">Maliyet gerçek değerleri sabit bir fiyat sözleşmesi satırına başvuru içeriyorsa, uygulama maliyet gerçek değerlerini yeniden işlemeye durur.</span><span class="sxs-lookup"><span data-stu-id="46bce-112">If the cost actuals reference a Fixed Price contract line, the application stops reprocessing the cost actuals.</span></span>

<span data-ttu-id="46bce-113">En fazla sınırlara tabi olmayan sınırlar, kurulum ve fiyatlarda fiyatlandırma ve maliyetlendirme değerlendirilir ve teyid işleminin parçası olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="46bce-113">Not-to-exceed limits, chargeability setup, and pricing and costing on the actuals is evaluated and then updated as part of the confirmations process.</span></span>

## <a name="close-a-project-contract-as-lost"></a><span data-ttu-id="46bce-114">Proje Sözleşmesini kayıp olarak kapat</span><span class="sxs-lookup"><span data-stu-id="46bce-114">Close a project contract as lost</span></span>

<span data-ttu-id="46bce-115">Bir proje sözleşmesini kayıp olarak kapattığınızda, sözleşmenin durumu, **kapalı** olarak güncelleştirilir ve durum açıklaması **kayıp** olur.</span><span class="sxs-lookup"><span data-stu-id="46bce-115">When you close a project contract as lost, the contract status is updated to **Closed** and the status reason is **Lost**.</span></span> <span data-ttu-id="46bce-116">Proje sözleşmesi salt okunur olur.</span><span class="sxs-lookup"><span data-stu-id="46bce-116">The project contract becomes read-only.</span></span> <span data-ttu-id="46bce-117">Kapatılan bir proje sözleşmesini yeniden açamazsınız, değişiklikler tamamlanmadan önce bir onay kutusu sağlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="46bce-117">A confirmation dialog is provided before the changes are complete because you can't reopen a closed project contract.</span></span>

<span data-ttu-id="46bce-118">Kaybedilen Proje sözleşmesi, satırlarındaki bir projeye başvuru içeriyorsa, bu proje de kapatıldığı gibi işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="46bce-118">If the project contract that is closed as lost references a project on its lines, that project is also marked as closed.</span></span> <span data-ttu-id="46bce-119">Bu günden ileriye doğru kaynak kayıtları iptal edilir.</span><span class="sxs-lookup"><span data-stu-id="46bce-119">Any resource bookings from that day forward are canceled.</span></span> <span data-ttu-id="46bce-120">Proje sözleşmesindeki fatura üzerinde bulunmayan ve faturalanmamış satış fiili değerleri ters işlem uygulanacak.</span><span class="sxs-lookup"><span data-stu-id="46bce-120">Any unbilled sales actuals on the project contract that aren't already on an invoice, will be reversed.</span></span>

> [!NOTE]
> <span data-ttu-id="46bce-121">Dynamics 365 Project Operations, bir proje sözleşmesini kayıp olarak kapatmak, ilişkilendirilmiş fırsatın durumunu etkilemez.</span><span class="sxs-lookup"><span data-stu-id="46bce-121">In Dynamics 365 Project Operations, closing a project contract as lost will not impact that status of the associated opportunity.</span></span> <span data-ttu-id="46bce-122">Fırsat açık kalacak ve el ile kapatılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="46bce-122">The opportunity will remain open and must be manually closed.</span></span>
