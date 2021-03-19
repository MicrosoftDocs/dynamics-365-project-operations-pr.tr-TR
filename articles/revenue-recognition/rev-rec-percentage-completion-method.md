---
title: Sabit fiyat geliri tahmin projeleri
description: Bu konu, projelerdeki sabit fiyat geliri hakkında bilgi sağlar.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7cf4d7853f7fedaeeeba99bc589f39989b924423
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278937"
---
# <a name="fixed-price-revenue-estimate-projects"></a><span data-ttu-id="80e41-103">Sabit fiyat geliri tahmin projeleri</span><span class="sxs-lookup"><span data-stu-id="80e41-103">Fixed price revenue estimate projects</span></span> 

<span data-ttu-id="80e41-104">_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="80e41-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="80e41-105">Microsoft Dataverse üzerindeki Dynamics 365 Project Operations uygulamasında aşağıdaki özniteliklere sahip bir proje sözleşme satırı oluşturduğunuzda sistem, otomatik olarak sabit fiyatlı bir gelir tahmini projesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="80e41-105">When you create a project contract line with the following attributes in Dynamics 365 Project Operations on Microsoft Dataverse, the system automatically creates a fixed price revenue estimate project.</span></span> <span data-ttu-id="80e41-106">Bu projedeki bilgiler, aşağıdakileri temel alır:</span><span class="sxs-lookup"><span data-stu-id="80e41-106">The information in this project is based on the following:</span></span>

  - <span data-ttu-id="80e41-107">Sabit fiyatlı bir faturalama yöntemi.</span><span class="sxs-lookup"><span data-stu-id="80e41-107">A fixed price billing method.</span></span>
  - <span data-ttu-id="80e41-108">İlişkili bir proje.</span><span class="sxs-lookup"><span data-stu-id="80e41-108">An associated project.</span></span>
  - <span data-ttu-id="80e41-109">**Proje sözleşmesi satırı** sayfasındaki **Fatura zamanlaması** sekmesinde tanımlanan en az bir kilometre taşı.</span><span class="sxs-lookup"><span data-stu-id="80e41-109">At least one milestone defined on the **Invoice schedule** tab on the **Project contract line** page.</span></span>

## <a name="review-fixed-price-revenue-estimates-projects"></a><span data-ttu-id="80e41-110">Sabit fiyatlı gelir tahminleri projelerini inceleme</span><span class="sxs-lookup"><span data-stu-id="80e41-110">Review fixed price revenue estimates projects</span></span>
<span data-ttu-id="80e41-111">Sabit fiyatlı gelir tahminleri projelerini incelemek için aşağıdaki adımları tamamlayın:</span><span class="sxs-lookup"><span data-stu-id="80e41-111">To review fixed price revenue estimates projects, complete the following steps:</span></span>

1. <span data-ttu-id="80e41-112">Dynamics 365 Finance ortamında, **Proje yönetimi ve muhasebesi** > **Projeler** > **Sabit fiyatlı gelir tahmini projeleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="80e41-112">In the Dynamics 365 Finance environment, go to **Projects management and accounting** > **Projects** > **Fixed price revenue estimate projects**.</span></span>
2. <span data-ttu-id="80e41-113">Görüntülemek istediğiniz projeyi seçin ve kaydı açmak ve projenin ayrıntılarını incelemek için **Tahmin proje kodu**'nu çift tıklayın.</span><span class="sxs-lookup"><span data-stu-id="80e41-113">Select the project that you want to view and double-click the **Estimate project ID** to open the record and review the details of the project.</span></span>
3. <span data-ttu-id="80e41-114">**Proje** sekmesini genişletin. **Seçilen projeler** ızgarasında bir proje görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="80e41-114">Expand the **Project** tab. You will see one project in the **Selected projects** grid.</span></span> <span data-ttu-id="80e41-115">Sistem bunu varsayılan proje olarak kullanır çünkü bu, proje sözleşme satırı ile ilişkilendirilmiş bir projedir.</span><span class="sxs-lookup"><span data-stu-id="80e41-115">The system uses this as default project because it is the project associated to the project contract line.</span></span> 
4. <span data-ttu-id="80e41-116">İlişkilendirmeyi değiştirmek için ek projeler seçin ve bunları **Seçilen projeler** ızgarasına ekleyin.</span><span class="sxs-lookup"><span data-stu-id="80e41-116">To change the association, select additional projects and add them to the **Selected projects** grid.</span></span> <span data-ttu-id="80e41-117">Bu ızgarada birden çok proje seçilirse seçilen tüm projeler için projenin tamamlanma yüzdesi ve gelir tahminleri birlikte hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="80e41-117">If multiple projects are selected in this grid, the project percentage completion and revenue estimates are calculated together for of the all selected projects.</span></span>

  <span data-ttu-id="80e41-118">Proje maliyeti, gelir profili, maliyet şablonu ve dönem kodu el ile ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="80e41-118">Project cost, revenue profile, cost template, and the period code can be set manually.</span></span> <span data-ttu-id="80e41-119">Bunlar, el ile ayarlanmazlarsa değerler, proje maliyeti ve gelir profilleri için yapılandırılmış kurallar kullanılarak proje için ilk tahmin hesaplaması sırasında ayarlanan değerlere varsayılan olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="80e41-119">If they aren't set manually, the values default during the first estimate calculation for the project using the rules configured for project cost and revenue profiles.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]