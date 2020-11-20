---
title: Dahili projeler için muhasebeyi yapılandırma
description: Bu konu, proje işlemlerinde dahili projeler için muhasebe uygulamaları ayarlama hakkında bilgi sağlar.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ea04178d4327ccd701ab431f172463a13a55154e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132402"
---
# <a name="configure-accounting-for-internal-projects"></a><span data-ttu-id="dc3dd-103">Dahili projeler için muhasebeyi yapılandırma</span><span class="sxs-lookup"><span data-stu-id="dc3dd-103">Configure accounting for internal projects</span></span>

<span data-ttu-id="dc3dd-104">_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="dc3dd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="dc3dd-105">Dahili projeler, şirketlerin müşteriye faturalanmayan faaliyetlerle ilgili maliyeti izlemesine olanak verir.</span><span class="sxs-lookup"><span data-stu-id="dc3dd-105">Internal projects allow companies track cost related to activities that aren't being billed to a customer.</span></span> <span data-ttu-id="dc3dd-106">Dahili proje örnekleri şunlardır:</span><span class="sxs-lookup"><span data-stu-id="dc3dd-106">Examples of internal projects include:</span></span>

- <span data-ttu-id="dc3dd-107">Mobil uygulama gibi bir ürün geliştirme ve geliştirmeyle ilişkili maliyeti izleme.</span><span class="sxs-lookup"><span data-stu-id="dc3dd-107">Developing a product, such as a mobile app, and tracking the cost associated with the development.</span></span>
- <span data-ttu-id="dc3dd-108">Satış öncesi süresi ve gideri yönetme.</span><span class="sxs-lookup"><span data-stu-id="dc3dd-108">Managing pre-sale time and expense.</span></span> <span data-ttu-id="dc3dd-109">Bu satış öncesi dahili proje, teklif kazanıldığında daha sonra faturalandırılabilir bir projeye dönüştürülebilir.</span><span class="sxs-lookup"><span data-stu-id="dc3dd-109">This pre-sale internal project can be converted later to a billable project if quote is won.</span></span>

<span data-ttu-id="dc3dd-110">Dynamics 365 Project Operations'da bir sözleşmeyle ilişkilendirilmemiş herhangi bir proje dahili olarak kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="dc3dd-110">Any project not associated with a contract in Dynamics 365 Project Operations is treated as internal.</span></span> <span data-ttu-id="dc3dd-111">Proje maliyet ve gelir profilleri, proje için muhasebe kurallarını belirlemek için kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="dc3dd-111">Project cost and revenue profiles aren't used to determine accounting rules for the project.</span></span> <span data-ttu-id="dc3dd-112">Dahili proje maliyeti her zaman kar ve zarar ilkeleri kullanılarak deftere nakledilir.</span><span class="sxs-lookup"><span data-stu-id="dc3dd-112">Internal project cost is always posted using profit and loss principles.</span></span> <span data-ttu-id="dc3dd-113">**Defter Nakli Kurulumu** sayfasında deftere nakiller için genel muhasebe hesapları tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="dc3dd-113">Ledger accounts for postings are defined on the **Ledger posting setup** page.</span></span>

- <span data-ttu-id="dc3dd-114">Zaman hareketleri, **Maliyet** hesabının borçlandırılması ve **Bordro tahsisatı** hesabında alacaklandırılması yoluyla deftere nakledilir.</span><span class="sxs-lookup"><span data-stu-id="dc3dd-114">Time transactions are posted by debiting the **Cost** account and crediting the **Payroll allocation** account.</span></span>
- <span data-ttu-id="dc3dd-115">Gider hareketleri, **Maliyet** hesabının borçlandırılması ve **Gider için ofset hesabı** alacaklandırılması yoluyla deftere nakledilir.</span><span class="sxs-lookup"><span data-stu-id="dc3dd-115">Expense transactions are posted by debiting the **Cost** account and crediting the **Offset account for expense**.</span></span>

<span data-ttu-id="dc3dd-116">Hareketler projeye nakledildikten sonra, proje bir proje sözleşmesiyle ilişkilendirilmişse, sistem tüm birikmiş hareketleri ters çevirir ve yeni faturalandırılabilir hareketler oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dc3dd-116">After transactions are posted to the project, if the project is associated with a project contract, the system reverses all accumulated transactions and creates new billable transactions.</span></span> <span data-ttu-id="dc3dd-117">Faturalandırılabilir hareketler, ilgili proje maliyet ve gelir profili ' nde tanımlanan hesap kurallarını izler.</span><span class="sxs-lookup"><span data-stu-id="dc3dd-117">The billable transactions follow the accounting rules defined in respective Project cost and revenue profile.</span></span>


