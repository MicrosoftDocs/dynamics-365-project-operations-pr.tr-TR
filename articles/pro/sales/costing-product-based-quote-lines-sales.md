---
title: Ürün tabanlı teklif satırlarını maliyetlendirme
description: Bu konuda, ürün tabanlı bir teklif satırına bir maliyet fiyatı uygulama hakkında bilgiler sağlanmaktadır.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c08ac3b0f24dda19489bad6e667a50b67b8ce3ec
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273672"
---
# <a name="costing-product-based-quote-lines"></a><span data-ttu-id="134b3-103">Ürün tabanlı teklif satırlarını maliyetlendirme</span><span class="sxs-lookup"><span data-stu-id="134b3-103">Costing product-based quote lines</span></span>

<span data-ttu-id="134b3-104">_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="134b3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="134b3-105">Dynamics 365 Project Operations'ta proje tabanlı teklif satırlarında bir **Maliyet Fiyatı** alanı da vardır.</span><span class="sxs-lookup"><span data-stu-id="134b3-105">Product-based quote lines in Dynamics 365 Project Operations also have a **Cost Price** field.</span></span> <span data-ttu-id="134b3-106">Bu alan, teklif satırındaki ürünün maliyet fiyatını izlemek ve aşağı yönlü karlılık hesaplamaları için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="134b3-106">This field is used to track the cost price for the product on the quote line and for downstream profitability calculations.</span></span>

<span data-ttu-id="134b3-107">Katalog ürünü için ürün tabanlı bir teklif satırı oluşturulduğunda, ürün tabanlı teklif satırının maliyeti, varsayılan olarak ürün kataloğundaki **Standart Maliyet** alanından alınır.</span><span class="sxs-lookup"><span data-stu-id="134b3-107">When a product-based quote line is created for a catalog product, the cost of the product-based quote line is defaulted from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="134b3-108">Ürün kataloğundaki standart maliyet alanı Kuruluşun temel para birimi cinsinden ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="134b3-108">The standard cost field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="134b3-109">Ürün tabanlı teklif satırındaki varsayılan birim maliyeti teklifte, satış para birimine dönüştürülür.</span><span class="sxs-lookup"><span data-stu-id="134b3-109">The default unit cost on the product-based quote line is converted to the sales currency on the quote.</span></span>

## <a name="unit-cost-on-a-product-based-quote-line"></a><span data-ttu-id="134b3-110">Ürün tabanlı teklif satırındaki birim maliyet</span><span class="sxs-lookup"><span data-stu-id="134b3-110">Unit cost on a product-based quote line</span></span>

<span data-ttu-id="134b3-111">Ürün tabanlı teklif satırında birim maliyete sahip olmanın amacı bir ürünün her satışta farklı maliyetlere sahip olabilmesine izin vermektir.</span><span class="sxs-lookup"><span data-stu-id="134b3-111">The purpose of having a unit cost on a product-based quote line is to allow for different costs for a product for each sale.</span></span> <span data-ttu-id="134b3-112">Bu tipik bir senaryo değildir ancak bazen, nihai satışın müşterisine bağlı olarak ürünün maliyeti tedarikçi tarafından düşürülebilir.</span><span class="sxs-lookup"><span data-stu-id="134b3-112">This is not a typical scenario, but sometimes the cost of the product may be discounted by the supplier depending on the customer of the final sale.</span></span>

<span data-ttu-id="134b3-113">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="134b3-113">For example:</span></span>

<span data-ttu-id="134b3-114">Fabrikam Robotics, A Datum Corporation'ın montaj hatlarına robotik kollar kuruyor.</span><span class="sxs-lookup"><span data-stu-id="134b3-114">Fabrikam Robotics is installing robotic arms at A Datum Corporation's assembly lines.</span></span> <span data-ttu-id="134b3-115">Fabrikam, kurulum hizmetleri sağlıyor ancak robotik kollar, Trey Robotics şirketinden sağlanıyor.</span><span class="sxs-lookup"><span data-stu-id="134b3-115">Fabrikam provides installation services but the robotic arms are procured from Trey robotics.</span></span> <span data-ttu-id="134b3-116">A Datum Corporation firmasına robotik kolların kurulumu, Trey şirketinin robotik kolları için yeni bir endüstriye açılan kapıysa Trey, Fabrikam'a bu anlaşma için özel bir iskonto sunabilir.</span><span class="sxs-lookup"><span data-stu-id="134b3-116">If the installation of robotic arms at A Datum Corporation opens a new industry vertical for Trey's robotic arms, Trey could give a special discount for this deal to Fabrikam.</span></span>

<span data-ttu-id="134b3-117">Bu durumda Fabrikam, Robotik Kollar için ürün tabanlı teklif satırı oluşturur ve bu teklif için birim başına özel bir maliyet girer.</span><span class="sxs-lookup"><span data-stu-id="134b3-117">In this case, Fabrikam will create product-based quote line for Robotic Arms and input a special per unit cost for this quote.</span></span> <span data-ttu-id="134b3-118">Bu maliyet, Trey Robotik Kollarının standart maliyetinden farklıdır.</span><span class="sxs-lookup"><span data-stu-id="134b3-118">This cost is different from the standard cost of Trey Robotic Arms.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]