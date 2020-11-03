---
title: Beceriler ve sertifikalar
description: Bu konuda, kaynaklara beceri ve sertifika özellikleri ekleme hakkında bilgiler sağlanmaktadır.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4c814754e68b3a1a8bf8784434d45010bf8d0123
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086241"
---
# <a name="skills-and-certifications"></a><span data-ttu-id="70595-103">Beceriler ve sertifikalar</span><span class="sxs-lookup"><span data-stu-id="70595-103">Skills and certifications</span></span>
<span data-ttu-id="70595-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="70595-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="70595-105">Özellikler, bir kaynağın yeteneklerini tanımlamak için kullanılan öznitelikleri zenginleştirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="70595-105">Characteristics are used to enrich the attributes used to describe the abilities of a resource.</span></span> <span data-ttu-id="70595-106">Kaynağın her özelliği **Beceri** veya **Sertifika** olarak tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="70595-106">Each characteristic of a resource can be described as a **Skill** or a **Certification**.</span></span>

<span data-ttu-id="70595-107">Kaynak gereksinimlerine özellikler eklemek, kaynağın bir projedeki görevleri tamamlamak için ihtiyaç duyduğu bilgi veya uzmanlığı belgelemenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="70595-107">Adding characteristics to resource requirements lets you document the knowledge or expertise needed by a resource to complete tasks on a project.</span></span> <span data-ttu-id="70595-108">Özellikler, kaynak gereksinimini planlarken gerekli özelliklere sahip olan kaynakları belirlemek için var olan kaynakların listesini filtrelemenize olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="70595-108">Characteristics let you filter the list of available resources to those resources that have the required characteristics when scheduling the resource requirement.</span></span>

## <a name="add-characteristics"></a><span data-ttu-id="70595-109">Özellikler ekle</span><span class="sxs-lookup"><span data-stu-id="70595-109">Add characteristics</span></span>

1. <span data-ttu-id="70595-110">Ana menüden **Kaynaklar** 'ı açın ve **Kaynaklar** bölümünde, **Beceriler** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="70595-110">From the main menu, open **Resources** and in the **Resources** section, select **Skills**.</span></span>
2. <span data-ttu-id="70595-111">Özellik eklemek için **Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="70595-111">Select **New** to add characteristics.</span></span>
3. <span data-ttu-id="70595-112">Gerekli alanları doldurun ve **Özellik Türü** 'nü seçin.</span><span class="sxs-lookup"><span data-stu-id="70595-112">Fill in the required fields and select the **Characteristic Type**.</span></span>

## <a name="assign-characteristics-to-resources"></a><span data-ttu-id="70595-113">Özelliklere kaynak atama</span><span class="sxs-lookup"><span data-stu-id="70595-113">Assign characteristics to resources</span></span>

1. <span data-ttu-id="70595-114">Ana menüden, **Kaynaklar** > **Ayrılabilir Kaynaklar** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="70595-114">From the main menu, select **Resources** > **Bookable Resources**.</span></span> <span data-ttu-id="70595-115">**Etkin Ayrılabilir Kaynaklar** sayfası açılır ve sistemde var olan tüm kaynakların bir listesini görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="70595-115">The **Active Bookable Resources** page opens and you can view a list of all available resources in the system.</span></span>
2. <span data-ttu-id="70595-116">Listeden ayrılabilir bir kaynağın adını seçin.</span><span class="sxs-lookup"><span data-stu-id="70595-116">From the list, select the name of a bookable resource.</span></span>
3. <span data-ttu-id="70595-117">**Project Service** bölümünde, **+Ayrılabilir Kaynak Özellikleri kaydı ekle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="70595-117">In the **Project Service** section, select **+Add Bookable Resource Characteristics record**.</span></span>
4. <span data-ttu-id="70595-118">Açılan açılır pencerede gerekli özellikleri bulup seçin ve kaynak için bir **Derecelendirme Değeri** ekleyin.</span><span class="sxs-lookup"><span data-stu-id="70595-118">In the pop-up window that opens, find and select the required characteristics, and add a **Rating Value** for the resource.</span></span>
5. <span data-ttu-id="70595-119">**Kaydet ve Kapat** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="70595-119">Select **Save & Close**.</span></span>

## <a name="assign-characteristics-to-resource-requirements"></a><span data-ttu-id="70595-120">Kaynak gereksinimlerine özellikler atama</span><span class="sxs-lookup"><span data-stu-id="70595-120">Assign characteristics to resource requirements</span></span>

1. <span data-ttu-id="70595-121">Takım üyesi ızgarasında, güncelleştirilmesi gereken özelliklere sahip genel takım üyesini bulun ve çift tıklayın.</span><span class="sxs-lookup"><span data-stu-id="70595-121">In the team member grid, find and double-click the generic team member with the characteristics that need to be updated.</span></span>
2. <span data-ttu-id="70595-122">**Proje Takımı üyesi Ayrıntısı** 'nda, **Kaynak Gereksinimi** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="70595-122">In the **Project Team member Detail** , select the **Resource Requirement** tab.</span></span>
3. <span data-ttu-id="70595-123">**Beceriler** alt ızgarasında, **+Yeni Gereksinim Özelliği Ekle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="70595-123">In the **Skills** subgrid, select **+Add new Requirement Characteristic.**</span></span>
4. <span data-ttu-id="70595-124">Hızlı oluşturma bölmesinde, gerekli özellikleri bulup seçin ve bir **Derecelendirme Değeri** ekleyin.</span><span class="sxs-lookup"><span data-stu-id="70595-124">In the quick create pane, find and select the required characteristics and add a **Rating Value**.</span></span>
5. <span data-ttu-id="70595-125">**Kaydet ve Kapat** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="70595-125">Select **Save & Close**.</span></span>