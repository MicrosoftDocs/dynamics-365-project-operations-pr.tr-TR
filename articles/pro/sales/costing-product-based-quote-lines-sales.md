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
ms.openlocfilehash: d21ab159294cac66ffeb8abcf0943b4babd7b360
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4118955"
---
# <a name="costing-product-based-quote-lines"></a><span data-ttu-id="33616-103">Ürün tabanlı teklif satırlarını maliyetlendirme</span><span class="sxs-lookup"><span data-stu-id="33616-103">Costing product-based quote lines</span></span>

<span data-ttu-id="33616-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="33616-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="33616-105">Dynamics 365 Project Operations'taki ürün tabanlı teklif satırlarında bir **Maliyet Fiyatı** alanı da vardır.</span><span class="sxs-lookup"><span data-stu-id="33616-105">Product-based quote lines in Dynamics 365 Project Operations also have a **Cost Price** field.</span></span> <span data-ttu-id="33616-106">Bu alan, teklif satırındaki ürünün maliyet fiyatını izlemek ve aşağı yönlü karlılık hesaplamaları için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="33616-106">This field is used to track the cost price for the product on the quote line and for downstream profitability calculations.</span></span>

<span data-ttu-id="33616-107">Katalog ürünü için ürün tabanlı bir teklif satırı oluşturulduğunda, ürün tabanlı teklif satırının maliyeti, varsayılan olarak ürün kataloğundaki **Standart Maliyet** alanından alınır.</span><span class="sxs-lookup"><span data-stu-id="33616-107">When a product-based quote line is created for a catalog product, the cost of the product-based quote line is defaulted from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="33616-108">Ürün kataloğundaki standart maliyet alanı Kuruluşun temel para birimi cinsinden ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="33616-108">The standard cost field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="33616-109">Ürün tabanlı teklif satırındaki varsayılan birim maliyeti teklifte, satış para birimine dönüştürülür.</span><span class="sxs-lookup"><span data-stu-id="33616-109">The default unit cost on the product-based quote line is converted to the sales currency on the quote.</span></span>

## <a name="unit-cost-on-a-product-based-quote-line"></a><span data-ttu-id="33616-110">Ürün tabanlı teklif satırındaki birim maliyet</span><span class="sxs-lookup"><span data-stu-id="33616-110">Unit cost on a product-based quote line</span></span>

<span data-ttu-id="33616-111">Ürün tabanlı teklif satırında birim maliyete sahip olmanın amacı bir ürünün her satışta farklı maliyetlere sahip olabilmesine izin vermektir.</span><span class="sxs-lookup"><span data-stu-id="33616-111">The purpose of having a unit cost on a product-based quote line is to allow for different costs for a product for each sale.</span></span> <span data-ttu-id="33616-112">Bu tipik bir senaryo değildir ancak bazen, nihai satışın müşterisine bağlı olarak ürünün maliyeti tedarikçi tarafından düşürülebilir.</span><span class="sxs-lookup"><span data-stu-id="33616-112">This is not a typical scenario, but sometimes the cost of the product may be discounted by the supplier depending on the customer of the final sale.</span></span>

<span data-ttu-id="33616-113">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="33616-113">For example:</span></span>

<span data-ttu-id="33616-114">Fabrikam Robotics, A Datum Corporation'ın montaj hatlarına robotik kollar kuruyor.</span><span class="sxs-lookup"><span data-stu-id="33616-114">Fabrikam Robotics is installing robotic arms at A Datum Corporation's assembly lines.</span></span> <span data-ttu-id="33616-115">Fabrikam, kurulum hizmetleri sağlıyor ancak robotik kollar, Trey Robotics şirketinden sağlanıyor.</span><span class="sxs-lookup"><span data-stu-id="33616-115">Fabrikam provides installation services but the robotic arms are procured from Trey robotics.</span></span> <span data-ttu-id="33616-116">A Datum Corporation firmasına robotik kolların kurulumu, Trey şirketinin robotik kolları için yeni bir endüstriye açılan kapıysa Trey, Fabrikam'a bu anlaşma için özel bir iskonto sunabilir.</span><span class="sxs-lookup"><span data-stu-id="33616-116">If the installation of robotic arms at A Datum Corporation opens a new industry vertical for Trey's robotic arms, Trey could give a special discount for this deal to Fabrikam.</span></span>

<span data-ttu-id="33616-117">Bu durumda Fabrikam, Robotik Kollar için ürün tabanlı teklif satırı oluşturur ve bu teklif için birim başına özel bir maliyet girer.</span><span class="sxs-lookup"><span data-stu-id="33616-117">In this case, Fabrikam will create product-based quote line for Robotic Arms and input a special per unit cost for this quote.</span></span> <span data-ttu-id="33616-118">Bu maliyet, Trey Robotik Kollarının standart maliyetinden farklıdır.</span><span class="sxs-lookup"><span data-stu-id="33616-118">This cost is different from the standard cost of Trey Robotic Arms.</span></span>
