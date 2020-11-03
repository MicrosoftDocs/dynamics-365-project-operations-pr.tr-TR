---
title: Proje güncelleştirme
description: Bu konuda, Project Operations projelerini güncelleştirme hakkında bilgiler sağlanmaktadır.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 5c9cd0c7c6886bd454c5f2ef2ae7f20d1707293f
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086179"
---
# <a name="update-a-project"></a><span data-ttu-id="d72d7-103">Proje güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="d72d7-103">Update a project</span></span>

<span data-ttu-id="d72d7-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="d72d7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d72d7-105">Aşağıda, bir proje oluşturulduktan ve mevcut güncelleştirmeler uygulandıktan sonra güncelleştirilebilecek alanların özeti verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="d72d7-105">Below is a summary of the fields that can be updated on a project after it has been created and any applicable implications of the updates.</span></span>

## <a name="project-detail-fields"></a><span data-ttu-id="d72d7-106">Proje ayrıntısı alanları</span><span class="sxs-lookup"><span data-stu-id="d72d7-106">Project detail fields</span></span>

- <span data-ttu-id="d72d7-107">**Ad** : Projenin başlığı.</span><span class="sxs-lookup"><span data-stu-id="d72d7-107">**Name** : The title of the project.</span></span>
- <span data-ttu-id="d72d7-108">**Açıklama** : Projeye genel bakış.</span><span class="sxs-lookup"><span data-stu-id="d72d7-108">**Description** : An overview of the project.</span></span>
- <span data-ttu-id="d72d7-109">**Müşteri** : Projenin teslim edileceği şirket.</span><span class="sxs-lookup"><span data-stu-id="d72d7-109">**Customer** : The company the project will be delivered to.</span></span>
- <span data-ttu-id="d72d7-110">**Takvim şablonu** : Projenin çalışma saatleri.</span><span class="sxs-lookup"><span data-stu-id="d72d7-110">**Calendar template** : The working hours of the project.</span></span> <span data-ttu-id="d72d7-111">Alan değiştirildiğinde, tüm zamanlama yeniden hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="d72d7-111">When the field is changed, the entire schedule is recalculated.</span></span>
- <span data-ttu-id="d72d7-112">**Para Birimi** : Projenin para birimi.</span><span class="sxs-lookup"><span data-stu-id="d72d7-112">**Currency** : The currency for the project.</span></span> <span data-ttu-id="d72d7-113">Bu alanın varsayılan değeri, sözleşme biriminde tanımlanan para birimine göre belirlenir.</span><span class="sxs-lookup"><span data-stu-id="d72d7-113">This field defaults based on the currency defined in the contracting unit.</span></span> <span data-ttu-id="d72d7-114">Sözleşme birimi güncelleştirildiğinde alan da güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="d72d7-114">When the contracting unit is updated, the field is also updated.</span></span>
- <span data-ttu-id="d72d7-115">**Sözleşme Birimi** : Satışı kazanmak ve iş ve servislerin müşteriye teslimini yönetmekten birincil olarak sorumlu olan şirket grubunu veya bölümü gösteren kuruluş birimidir.</span><span class="sxs-lookup"><span data-stu-id="d72d7-115">**Contracting Unit** : The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> 
- <span data-ttu-id="d72d7-116">**Proje Yöneticisi** : Zaman girişlerini ve giderleri inceleme ve onaylama yetkisine sahip proje takımı üyesi.</span><span class="sxs-lookup"><span data-stu-id="d72d7-116">**Project Manager** : The project team member who has the authority to review and approve time entries and expenses.</span></span>

## <a name="estimate-fields"></a><span data-ttu-id="d72d7-117">Tahmin alanları</span><span class="sxs-lookup"><span data-stu-id="d72d7-117">Estimate fields</span></span>

- <span data-ttu-id="d72d7-118">**Tahmini Başlangıç Tarihi** : Projenin başlayacağı tarih.</span><span class="sxs-lookup"><span data-stu-id="d72d7-118">**Estimated Start Date** : The date that the project will begin.</span></span> <span data-ttu-id="d72d7-119">Bu alan güncelleştirildiğinde, projedeki tüm görevler yeni başlangıç tarihine göre uygun şekilde taşınır.</span><span class="sxs-lookup"><span data-stu-id="d72d7-119">When this field is updated, any tasks on the project will move proportionately with the start new start date.</span></span>
- <span data-ttu-id="d72d7-120">**Bitiş Tarihi** : Projenin bitmesi planlanan tarih.</span><span class="sxs-lookup"><span data-stu-id="d72d7-120">**Finish Date** : The date that the project is scheduled to end.</span></span>
- <span data-ttu-id="d72d7-121">**Çalışma Süresi** : Projenin tahmini çalışma süresi.</span><span class="sxs-lookup"><span data-stu-id="d72d7-121">**Effort** : The estimated effort of the project.</span></span> <span data-ttu-id="d72d7-122">Görevler projeye eklendikten sonra bu alan düzenlenemez.</span><span class="sxs-lookup"><span data-stu-id="d72d7-122">When tasks are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="d72d7-123">**Tahmini İşçilik Maliyeti** : Projenin tahmini işçilik maliyeti.</span><span class="sxs-lookup"><span data-stu-id="d72d7-123">**Estimated Labor Cost** : The estimated labor cost of the project.</span></span> <span data-ttu-id="d72d7-124">İşçilik maliyetleri projeye eklendikten sonra bu alan düzenlenemez.</span><span class="sxs-lookup"><span data-stu-id="d72d7-124">When labor costs are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="d72d7-125">**Tahmini Giderler** : Projenin tahmini giderleri.</span><span class="sxs-lookup"><span data-stu-id="d72d7-125">**Estimated Expenses** : The estimated expenses of the project.</span></span> <span data-ttu-id="d72d7-126">Giderler projeye eklendikten sonra bu alan düzenlenemez.</span><span class="sxs-lookup"><span data-stu-id="d72d7-126">When expenses are added to the project, this field is no longer editable.</span></span>

## <a name="project-actual-fields"></a><span data-ttu-id="d72d7-127">Projenin gerçek değer alanları</span><span class="sxs-lookup"><span data-stu-id="d72d7-127">Project actual fields</span></span>
- <span data-ttu-id="d72d7-128">**Fiili Başlangıç** : Projenin başlatıldığı tarih.</span><span class="sxs-lookup"><span data-stu-id="d72d7-128">**Actual Start** : The date that the project started.</span></span>
- <span data-ttu-id="d72d7-129">**Fiili Bitiş** : Proje tamamlandığında güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="d72d7-129">**Actual Finish** : To be updated when a project has been completed.</span></span>

## <a name="project-status-fields"></a><span data-ttu-id="d72d7-130">Proje durumu alanları</span><span class="sxs-lookup"><span data-stu-id="d72d7-130">Project status fields</span></span>

- <span data-ttu-id="d72d7-131">**Genel Proje Durumu** : Proje yöneticisinin sağladığı genel proje durumu.</span><span class="sxs-lookup"><span data-stu-id="d72d7-131">**Overall Project Status** : The overall project health provided by the Project manager.</span></span>
- <span data-ttu-id="d72d7-132">**Yorumlar** : Proje yöneticisinin sağladığı, projenin geçerli durumuyla ilgili bir anlatım.</span><span class="sxs-lookup"><span data-stu-id="d72d7-132">**Comments** : A narrative regarding the current health of the project provided by the Project manager.</span></span>

