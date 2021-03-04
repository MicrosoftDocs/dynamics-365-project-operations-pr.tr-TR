---
title: Ürün tabanlı sözleşme satırlarını maliyetlendirin - lite
description: Bu konu oluşturma hakkında bilgi sağlar
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a81c972f36179621f0547c24fc53d294485f638c
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764483"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="c4e76-103">Ürün tabanlı sözleşme satırlarını maliyetlendirin - lite</span><span class="sxs-lookup"><span data-stu-id="c4e76-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="c4e76-104">_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_</span><span class="sxs-lookup"><span data-stu-id="c4e76-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="c4e76-105">Dynamics 365 Project Operations uygulamasındaki ürün tabanlı sözleşme satırları, satış sonrası karlılık hesaplamaları için ürünün maliyet fiyatını depolayan **Maliyet Fiyatı** alanını içerir.</span><span class="sxs-lookup"><span data-stu-id="c4e76-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="c4e76-106">Katalog ürünü için ürün tabanlı sözleşme satırı oluşturulduğunda, satırın maliyeti varsayılan olarak ürün kataloğundaki **Standart Maliyet** alanından alınır.</span><span class="sxs-lookup"><span data-stu-id="c4e76-106">When a product-based contract line is created for a catalog product, the cost of the line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="c4e76-107">Ürün kataloğundaki **standart maliyet** alanı Kuruluşun temel para birimi cinsinden ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="c4e76-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="c4e76-108">Birim maliyet, sözleşme satırında varsayılan olarak kullanıldığında, sözleşmedeki satış para birimine dönüştürülür.</span><span class="sxs-lookup"><span data-stu-id="c4e76-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="c4e76-109">Ürün tabanlı sözleşme satırındaki birim maliyet</span><span class="sxs-lookup"><span data-stu-id="c4e76-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="c4e76-110">Ürün tabanlı sözleşme satırında birim maliyete sahip olmanın amacı bir ürünün her satışta farklı maliyetlere sahip olabilmesine izin vermektir.</span><span class="sxs-lookup"><span data-stu-id="c4e76-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="c4e76-111">Her zaman gerekli olmasa da, ürün maliyetine tedarikçiye göre iskonto uygulanabilecek belirli senaryolar vardır.</span><span class="sxs-lookup"><span data-stu-id="c4e76-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="c4e76-112">Aşağıdaki senaryoyu inceleyin:</span><span class="sxs-lookup"><span data-stu-id="c4e76-112">Consider the following scenario:</span></span>

<span data-ttu-id="c4e76-113">Fabrikam Robotics, A Datum Corporation'ın montaj hatlarına robotik kollar kuruyor.</span><span class="sxs-lookup"><span data-stu-id="c4e76-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="c4e76-114">Fabrikam, kurulum hizmetleri sağlar ancak robotik kollar Trey Research'tendir.</span><span class="sxs-lookup"><span data-stu-id="c4e76-114">Fabrikam provides installation services but the robotic arms are from Trey Research.</span></span> <span data-ttu-id="c4e76-115">Adatum Corporation firmasına robotik kolların kurulumu, Trey Research şirketi yeni bir endüstriye açılan kapıysa Trey, Fabrikam'a bu anlaşma için özel bir iskonto sunabilir.</span><span class="sxs-lookup"><span data-stu-id="c4e76-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="c4e76-116">Bu durumda Fabrikam, Robotic Arms için bir ürün tabanlı sözleşme satırı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c4e76-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms.</span></span> <span data-ttu-id="c4e76-117">Bu sözleşme için birim başına maliyet girilir.</span><span class="sxs-lookup"><span data-stu-id="c4e76-117">A per unit cost is entered for this contract.</span></span> <span data-ttu-id="c4e76-118">Maliyet, Trey Research'ün robotik kollarının maliyetinden farklıdır.</span><span class="sxs-lookup"><span data-stu-id="c4e76-118">The cost is different from the cost of robotic arms from Trey Research.</span></span>
