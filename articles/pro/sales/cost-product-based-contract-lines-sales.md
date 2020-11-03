---
title: Ürün tabanlı sözleşme satırlarını maliyetlendirme
description: Bu konu oluşturma hakkında bilgi sağlar
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7dfb9425174dddee52f9ee64f7a963e48a6bca70
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/20/2020
ms.locfileid: "4086555"
---
# <a name="costing-product-based-contract-lines"></a><span data-ttu-id="5d58f-103">Ürün tabanlı sözleşme satırlarını maliyetlendirme</span><span class="sxs-lookup"><span data-stu-id="5d58f-103">Costing product-based contract lines</span></span>

<span data-ttu-id="5d58f-104">_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_</span><span class="sxs-lookup"><span data-stu-id="5d58f-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="5d58f-105">Dynamics 365 Project Operations'ta ürün tabanlı sözleşme satırları, ürünün akış yönündeki karlılık hesaplamaları için maliyet fiyatını depolayan **Maliyet fiyatı** alanını içerir.</span><span class="sxs-lookup"><span data-stu-id="5d58f-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="5d58f-106">Katalog ürünü için ürün tabanlı bir sözleşme satırı oluşturulduğunda, ürün tabanlı sözleşme satırının maliyeti, varsayılan olarak ürün kataloğundaki **Standart Maliyet** alanından alınır.</span><span class="sxs-lookup"><span data-stu-id="5d58f-106">When a product-based contract line is created for a catalog product, the cost of the product-based contract line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="5d58f-107">Ürün kataloğundaki **standart maliyet** alanı Kuruluşun temel para birimi cinsinden ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="5d58f-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="5d58f-108">Birim maliyet, sözleşme satırında varsayılan olarak kullanıldığında, sözleşmedeki satış para birimine dönüştürülür.</span><span class="sxs-lookup"><span data-stu-id="5d58f-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="5d58f-109">Ürün tabanlı sözleşme satırındaki birim maliyet</span><span class="sxs-lookup"><span data-stu-id="5d58f-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="5d58f-110">Ürün tabanlı sözleşme satırında birim maliyete sahip olmanın amacı bir ürünün her satışta farklı maliyetlere sahip olabilmesine izin vermektir.</span><span class="sxs-lookup"><span data-stu-id="5d58f-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="5d58f-111">Her zaman gerekli olmasa da, ürün maliyetine tedarikçiye göre iskonto uygulanabilecek belirli senaryolar vardır.</span><span class="sxs-lookup"><span data-stu-id="5d58f-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="5d58f-112">Aşağıdaki senaryoyu inceleyin:</span><span class="sxs-lookup"><span data-stu-id="5d58f-112">Consider the following scenario:</span></span>

<span data-ttu-id="5d58f-113">Fabrikam Robotics, A Datum Corporation'ın montaj hatlarına robotik kollar kuruyor.</span><span class="sxs-lookup"><span data-stu-id="5d58f-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="5d58f-114">Fabrikam, kurulum hizmetleri sağlıyor ancak robotik kollar, Trey Research şirketinden sağlanıyor.</span><span class="sxs-lookup"><span data-stu-id="5d58f-114">Fabrikam provides installation services but the robotic arms are procured from Trey Research.</span></span> <span data-ttu-id="5d58f-115">Adatum Corporation firmasına robotik kolların kurulumu, Trey Research şirketi yeni bir endüstriye açılan kapıysa Trey, Fabrikam'a bu anlaşma için özel bir iskonto sunabilir.</span><span class="sxs-lookup"><span data-stu-id="5d58f-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="5d58f-116">Bu durumda, Fabrikam, bu sözleşmenin birim maliyetini, Trey Research'den alınan Robot kolları standart maliyetinden farklı bir şekilde robot bir şekilde ve bir dizi maliyet için ürün tabanlı bir sözleşme satırı halinde oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5d58f-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms and inputs a per unit cost for this contract that is different from the standard cost of robotic arms from Trey Research.</span></span>
