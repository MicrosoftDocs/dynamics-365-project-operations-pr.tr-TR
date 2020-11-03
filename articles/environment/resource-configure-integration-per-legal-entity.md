---
title: Her tüzel kişilik için Project Operations tümleştirmesini yapılandırma
description: Bu konuda Project Operations'ta tüzel varlık entegrasyonu ayarlama hakkında bilgi sağlanır.
author: sigitac
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c0e02ef2d17bf49209369f7adad681d9a5981e2a
ms.sourcegitcommit: 91ad491e94a421f256a378b0f4b26ed48c67bc93
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/22/2020
ms.locfileid: "4096776"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a><span data-ttu-id="691b1-103">Her tüzel kişilik için Project Operations tümleştirmesini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="691b1-103">Configure Project Operations integration per legal entity</span></span> 

<span data-ttu-id="691b1-104">_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="691b1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="691b1-105">Bu konu, her yasal varlık için Dynamics 365 Project Operations'ı yapılandırmak için gereken adımları açıklar.</span><span class="sxs-lookup"><span data-stu-id="691b1-105">This topic walks you through the steps required to configure Dynamics 365 Project Operations per legal entity.</span></span>

## <a name="enable-feature-keys-in-dynamics-365-finance"></a><span data-ttu-id="691b1-106">Dynamics 365 Finance'te özellik anahtarlarını etkinleştir</span><span class="sxs-lookup"><span data-stu-id="691b1-106">Enable feature keys in Dynamics 365 Finance</span></span>

<span data-ttu-id="691b1-107">Gerekli özellikleri etkinleştirmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="691b1-107">Complete the following steps to enable required features.</span></span>

1. <span data-ttu-id="691b1-108">Dynamics 365 Finance'te **Özellik yönetimi** çalışma alanına gidin.</span><span class="sxs-lookup"><span data-stu-id="691b1-108">In Dynamics 365 Finance, go to the **Feature Management** workspace.</span></span>
2. <span data-ttu-id="691b1-109">**Özellik listesinde** , aşağıdaki özellikleri bulun ve etkinleştirin:</span><span class="sxs-lookup"><span data-stu-id="691b1-109">In **Feature list** , find and enable the following features:</span></span>
  
    - <span data-ttu-id="691b1-110">**Bir proje için birden çok sözleşme satırını etkinleştirme**</span><span class="sxs-lookup"><span data-stu-id="691b1-110">**Enable multiple contract lines for a project**</span></span>
    - <span data-ttu-id="691b1-111">**Dynamics 365 Customer Engagement'ta Project Operations'ı etkinleştirin**</span><span class="sxs-lookup"><span data-stu-id="691b1-111">**Enable Project Operations on Dynamics 365 Customer Engagement**</span></span>

> [!NOTE]
> <span data-ttu-id="691b1-112">**Özellik anahtarlarını** listede göremiyorsanız, Finance sürümünüzün en düşük sürüm gereksinimini (uygulama sürümü 10.0.13 uygulanmış veya daha yüksek) karşıladığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="691b1-112">If you don't see **Feature keys** listed, verify that your Finance version meets the minimum version requirement (application version 10.0.13 with all quality updates applied or higher).</span></span> <span data-ttu-id="691b1-113">Özellik listesini yenilemek için **güncelleştirmeleri denetle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="691b1-113">Select **Check for updates** to refresh the feature list.</span></span>

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a><span data-ttu-id="691b1-114">Geçerli bir varlık için Project Operations dağıtımı senaryosu tanımlayın</span><span class="sxs-lookup"><span data-stu-id="691b1-114">Define the Project Operations deployment scenario for a legal entity</span></span>

<span data-ttu-id="691b1-115">Geçerli bir varlık düzeyinde Dynamics 365 Customer Engagement'ta Project Operations'ı etkinleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="691b1-115">You can enable Project Operations on Dynamics 365 Customer Engagement on a legal entity level.</span></span> <span data-ttu-id="691b1-116">Kaynak/Stoklanmayan tabanlı senaryolarda Dynamics 365 Customer Engagement'ta Project Operations'ı kullanarak bir yasal varlığınız olabilir.</span><span class="sxs-lookup"><span data-stu-id="691b1-116">You can have one legal entity using Project Operations on Dynamics 365 Customer Engagement for resource/non-stocked based scenarios.</span></span> <span data-ttu-id="691b1-117">Aynı ortamda, Stoklanmayan/üretim emri senaryoları için Project Operations'ı kullanarak başka bir tüzel kişiliye sahip olabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="691b1-117">In the same environment, you can have another legal entity using Project Operations for stocked/production order scenarios.</span></span>

1. <span data-ttu-id="691b1-118">Dynamics 365 Finance'te **Proje yönetimi ve muhasebe** > **Kurulum** > **Genel Proje yönetimi ve muhasebe parametreleri** 'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="691b1-118">In Dynamics 365 Finance, go to **Project management and accounting** > **Setup** > **Global project management and accounting parameters**.</span></span>
2. <span data-ttu-id="691b1-119">Kullanılabilir geçerli varlıklar listesinde, birden çok sözleşme satırı ve Dynamics 365 Customer Engagement özellikler üzerinde Project Operations'ın etkinleştirildiği varlıkları seçin.</span><span class="sxs-lookup"><span data-stu-id="691b1-119">In the list of available legal entities, select entities where multiple contract lines and Project Operations on Dynamics 365 Customer Engagement features will be enabled.</span></span> <span data-ttu-id="691b1-120">Stoğu/üretim emri senaryoları seçili olmadığı için Project Operations'ı kullanacak hukuk tüzel vrlıkları bırakın.</span><span class="sxs-lookup"><span data-stu-id="691b1-120">Leave legal entities that will be using Project Operations for stocked/production order scenarios unselected.</span></span>

> [!NOTE]
> <span data-ttu-id="691b1-121">Yasal bir varlık, yalnızca varolan bir proje içermiyorsa seçilebilir.</span><span class="sxs-lookup"><span data-stu-id="691b1-121">A legal entity can be selected only if it doesn't have any existing projects.</span></span>

## <a name="configure-project-management-and-accounting-parameters"></a><span data-ttu-id="691b1-122">Proje yönetimi ve muhasebeye genel bakış parametrelerini yapılandırın</span><span class="sxs-lookup"><span data-stu-id="691b1-122">Configure Project management and accounting parameters</span></span>

<span data-ttu-id="691b1-123">Dynamics 365 Customer Engagement üzerinde Project Operations kullanan her bir tüzel kişiliği bir varsayılan parametre kümesi gerektirir.</span><span class="sxs-lookup"><span data-stu-id="691b1-123">Each legal entity using Project Operations on Dynamics 365 Customer Engagement needs a set of default parameters.</span></span> <span data-ttu-id="691b1-124">Bu parametreler **Proje yönetimi ve hesap oluşturma parametreleri** sayfasındaki **Project Operations** sekmesinde yapılandırılır .</span><span class="sxs-lookup"><span data-stu-id="691b1-124">These parameters are configured on the **Project Operations** tab on the **Project management and accounting parameters** page.</span></span> <span data-ttu-id="691b1-125">Parametreler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="691b1-125">The parameters are:</span></span>

  - <span data-ttu-id="691b1-126">**Fatura türü varsayılanları** : Project Operations, satır özellikleri finans ile eşlenmesi gereken sabit bir faturalama türü varsayılan kümesi kullanır.</span><span class="sxs-lookup"><span data-stu-id="691b1-126">**Billing type defaults** : Project Operations uses a fixed set of billing type defaults that must be mapped to line properties Finance.</span></span> <span data-ttu-id="691b1-127">Her faturalama türü için bir kayıt oluşturun: **belirtilmemiş** , **Borçlandırılabilir** , **borçlandırılamayan** , **Kapanış** ve **kullanılamaz**.</span><span class="sxs-lookup"><span data-stu-id="691b1-127">Create a record for each billing type: **Not specified** , **Chargeable** , **Non-chargeable** , **Complimentary** , and **Not available**.</span></span>
  - <span data-ttu-id="691b1-128">**Proje kategorisi Varsayılanları** : her hareket türü için kullanılacak varsayılan Proje kategorilerini seçin.</span><span class="sxs-lookup"><span data-stu-id="691b1-128">**Project category defaults** : Select the default project categories to be used for each transaction type.</span></span> <span data-ttu-id="691b1-129">Bu varsayılanlar **Project Operations tümleştirme günlüğünde** ve proje fiili için herhangi bir hareket kategorisinin belirtilmediğinde tahminlerde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="691b1-129">These defaults will be used in the **Project Operations Integration journal** and in estimates where no transaction category is specified for the project actual.</span></span>
  - <span data-ttu-id="691b1-130">**Tahminler** : Zaman ve gider tahminlerinde kullanılacak tahmin modelini seçin.</span><span class="sxs-lookup"><span data-stu-id="691b1-130">**Forecasts** : Select the forecast model to be used for time and expense estimates.</span></span>
