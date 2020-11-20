---
title: Proje sözleşmelerini yönet
description: Bu konu proje tabanlı sözleşmeleri görüntüleme hakkında bilgi sağlar.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 441fbc378a423334f45bc65658811ef238515393
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177355"
---
# <a name="manage-project-contracts"></a><span data-ttu-id="a821b-103">Proje sözleşmelerini yönet</span><span class="sxs-lookup"><span data-stu-id="a821b-103">Manage project contracts</span></span>

<span data-ttu-id="a821b-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="a821b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a821b-105">Dynamics 365 Project Operations içindeki proje sözleşmeleri, bir projenin sözleşmede onaylanan taahhütleri ve faturalama ayrıntılarını yakalar ve yönetir.</span><span class="sxs-lookup"><span data-stu-id="a821b-105">Project contracts in Dynamics 365 Project Operations capture and manage the contractually agreed on commitments and billing details of a project.</span></span> <span data-ttu-id="a821b-106">Project Operations'da proje sözleşmesinin yapısı, aşağıdaki bileşenlerle proje tabanlı işler için tasarlanmıştır:</span><span class="sxs-lookup"><span data-stu-id="a821b-106">The structure of a project contract in Project Operations is tailored to project-based work with the following components:</span></span>

- <span data-ttu-id="a821b-107">Bir proje faturasında yüksek düzeyli bileşenler olarak sunulacak çalışmanın ayrı bileşenlerini tanımlayan sözleşme satırları.</span><span class="sxs-lookup"><span data-stu-id="a821b-107">Contract lines that identify the discrete components of work that will be presented as high-level components on a project invoice.</span></span>
- <span data-ttu-id="a821b-108">Her bir üst düzey bileşen veya sözleşme satırı için çalışmayı tanımlayan ve tahmin eden sözleşme satırı ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="a821b-108">Contract line details that identify and estimate the work for each high-level component or contract line.</span></span> <span data-ttu-id="a821b-109">Tahmin, sözleşme satırına bağlı çalışmanın zamanlamasını ve mali yönlerini içerir.</span><span class="sxs-lookup"><span data-stu-id="a821b-109">The estimate includes the schedule and the financial aspects for the work tied to the contract line.</span></span>
- <span data-ttu-id="a821b-110">Modelleri ve borçlandırılabilen bileşenler, her sözleşme satırı için faturalama düzenlemesini ve genel sözleşmeyi tutan her bir sözleşme satırı için ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="a821b-110">Contracting models and chargeable components are set up for each contract line that holds the billing arrangement for each contract line and the overall contract.</span></span>

## <a name="view-all-project-based-contracts"></a><span data-ttu-id="a821b-111">Tüm proje tabanlı sözleşmeleri görüntüleyin</span><span class="sxs-lookup"><span data-stu-id="a821b-111">View all project-based contracts</span></span>

<span data-ttu-id="a821b-112">Tüm proje sözleşmelerinin listesi, **sözleşmeler** listesi sayfasında görülebilir.</span><span class="sxs-lookup"><span data-stu-id="a821b-112">A list of all project contracts can be seen on the **Contracts** list page.</span></span> 

1. <span data-ttu-id="a821b-113">**Satış** > **Kişiler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="a821b-113">Go to **Sales** > **Contracts**.</span></span> <span data-ttu-id="a821b-114">Sistemdeki tüm proje Sözleşmelerinizin listesi gösterilir.</span><span class="sxs-lookup"><span data-stu-id="a821b-114">A list of all your project Contracts in the system are shown.</span></span> 
2. <span data-ttu-id="a821b-115">Diğer filtre uygulanmış görünümleri seçmek için **görünüm değiştiriciyi** (görünümün adının yanındaki açılan ok) seçin.</span><span class="sxs-lookup"><span data-stu-id="a821b-115">Select the **View switcher** (the drop-down arrow next to the name of the view) to select other filtered views.</span></span> <span data-ttu-id="a821b-116">Özel filtre ölçütlerinde kendi görünümlerinizi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a821b-116">You can create your own views with custom filter criteria.</span></span>

<span data-ttu-id="a821b-117">Sözleşmeler, bu liste sayfasından veya ayrıntı sayfalarından oluşturulabilir veya silinebilir.</span><span class="sxs-lookup"><span data-stu-id="a821b-117">Contracts can be created or deleted from this list page or detail pages.</span></span>
