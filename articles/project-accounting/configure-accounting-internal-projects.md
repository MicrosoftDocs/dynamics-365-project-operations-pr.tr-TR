---
title: Dahili projeler için muhasebeyi yapılandırma
description: Bu konu, proje işlemlerinde dahili projeler için muhasebe uygulamaları ayarlama hakkında bilgi sağlar.
author: sigitac
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ad8b974ef75cb0a4e43af0aa254cec1bbcab154a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012880"
---
# <a name="configure-accounting-for-internal-projects"></a><span data-ttu-id="3a521-103">Dahili projeler için muhasebeyi yapılandırma</span><span class="sxs-lookup"><span data-stu-id="3a521-103">Configure accounting for internal projects</span></span>

<span data-ttu-id="3a521-104">_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="3a521-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="3a521-105">Dahili projeler, şirketlerin müşteriye faturalanmayan faaliyetlerle ilgili maliyeti izlemesine olanak verir.</span><span class="sxs-lookup"><span data-stu-id="3a521-105">Internal projects allow companies track cost related to activities that aren't being billed to a customer.</span></span> <span data-ttu-id="3a521-106">Dahili proje örnekleri şunlardır:</span><span class="sxs-lookup"><span data-stu-id="3a521-106">Examples of internal projects include:</span></span>

- <span data-ttu-id="3a521-107">Mobil uygulama gibi bir ürün geliştirme ve geliştirmeyle ilişkili maliyeti izleme.</span><span class="sxs-lookup"><span data-stu-id="3a521-107">Developing a product, such as a mobile app, and tracking the cost associated with the development.</span></span>
- <span data-ttu-id="3a521-108">Satış öncesi süresi ve gideri yönetme.</span><span class="sxs-lookup"><span data-stu-id="3a521-108">Managing pre-sale time and expense.</span></span> <span data-ttu-id="3a521-109">Bu satış öncesi dahili proje, teklif kazanıldığında daha sonra faturalandırılabilir bir projeye dönüştürülebilir.</span><span class="sxs-lookup"><span data-stu-id="3a521-109">This pre-sale internal project can be converted later to a billable project if quote is won.</span></span>

<span data-ttu-id="3a521-110">Dynamics 365 Project Operations'ta bir sözleşmeyle ilişkili olmayan projeler, dahili olarak görülür.</span><span class="sxs-lookup"><span data-stu-id="3a521-110">Any project not associated with a contract in Dynamics 365 Project Operations is treated as internal.</span></span> <span data-ttu-id="3a521-111">Proje maliyet ve gelir profilleri, proje için muhasebe kurallarını belirlemek için kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="3a521-111">Project cost and revenue profiles aren't used to determine accounting rules for the project.</span></span> <span data-ttu-id="3a521-112">Dahili proje maliyeti her zaman kar ve zarar ilkeleri kullanılarak deftere nakledilir.</span><span class="sxs-lookup"><span data-stu-id="3a521-112">Internal project cost is always posted using profit and loss principles.</span></span> <span data-ttu-id="3a521-113">**Defter Nakli Kurulumu** sayfasında deftere nakiller için genel muhasebe hesapları tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="3a521-113">Ledger accounts for postings are defined on the **Ledger posting setup** page.</span></span>

- <span data-ttu-id="3a521-114">Zaman hareketleri, **Maliyet** hesabının borçlandırılması ve **Bordro tahsisatı** hesabında alacaklandırılması yoluyla deftere nakledilir.</span><span class="sxs-lookup"><span data-stu-id="3a521-114">Time transactions are posted by debiting the **Cost** account and crediting the **Payroll allocation** account.</span></span>
- <span data-ttu-id="3a521-115">Gider hareketleri, **Maliyet** hesabının borçlandırılması ve **Gider için ofset hesabı** alacaklandırılması yoluyla deftere nakledilir.</span><span class="sxs-lookup"><span data-stu-id="3a521-115">Expense transactions are posted by debiting the **Cost** account and crediting the **Offset account for expense**.</span></span>
- <span data-ttu-id="3a521-116">Madde hareketleri, **Maliyet** hesabına alacak olarak kaydedilip **Maliyet - Madde** hesabına ödenerek deftere nakledilir.</span><span class="sxs-lookup"><span data-stu-id="3a521-116">Item transactions are posted by debiting the **Cost** account and crediting the **Cost - Item** account.</span></span>

<span data-ttu-id="3a521-117">Hareketler projeye nakledildikten sonra, proje bir proje sözleşmesiyle ilişkilendirilmişse, sistem tüm birikmiş hareketleri ters çevirir ve yeni faturalandırılabilir hareketler oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3a521-117">After transactions are posted to the project, if the project is associated with a project contract, the system reverses all accumulated transactions and creates new billable transactions.</span></span> <span data-ttu-id="3a521-118">Faturalandırılabilir hareketler, ilgili proje maliyet ve gelir profili ' nde tanımlanan hesap kurallarını izler.</span><span class="sxs-lookup"><span data-stu-id="3a521-118">The billable transactions follow the accounting rules defined in respective Project cost and revenue profile.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
