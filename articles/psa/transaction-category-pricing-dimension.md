---
title: İşlem kategorisini fiyatlandırma boyutu olarak kullanma
description: Bu konu, işlem kategorisini fiyatlandırma boyutu olarak kullanma hakkında bilgi sağlar.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 0019571a1d37d3b6a503e7221db3c3b51365c236
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086408"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a><span data-ttu-id="190f9-103">İşlem kategorisini fiyatlandırma boyutu olarak kullanma</span><span class="sxs-lookup"><span data-stu-id="190f9-103">Use transaction category as a pricing dimension</span></span>
<span data-ttu-id="190f9-104">Bu konu, bir işlem kategorisinin fiyatlandırma boyutu olarak nasıl kullanılacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="190f9-104">This topic shows how to use a transaction category as a pricing dimension.</span></span> <span data-ttu-id="190f9-105">Başlamadan önce, önceden bir fiyatlandırma boyutu çözümü oluşturmadıysanız yeni bir tane oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="190f9-105">Before you begin, if you have not already created a pricing dimension solution, you will need to create a new one.</span></span> <span data-ttu-id="190f9-106">Zaten bir fiyatlandırma boyutu çözümünüz varsa değişikliklerinizi bu çözümde yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="190f9-106">If you already have a pricing dimension solution, then you can make your changes in that solution.</span></span> <span data-ttu-id="190f9-107">Kuruluşunuz için yeni bir fiyatlandırma boyutu çözümü oluşturmadıysanız [Özel alanlar ve varlıklar oluşturma](create-custom-fields-entities.md) konu başlığındaki yordamları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="190f9-107">If you have not created a new pricing dimension solution for your organization, complete the procedures in the [Create custom fields and entities](create-custom-fields-entities.md) topic.</span></span>

## <a name="add-transaction-category-to-forms-and-views"></a><span data-ttu-id="190f9-108">Formlara ve görünümlere işlem kategorisi ekleme</span><span class="sxs-lookup"><span data-stu-id="190f9-108">Add transaction category to forms and views</span></span>
<span data-ttu-id="190f9-109">Fiyatlandırma boyutu çözümünde, kullanıcı arabiriminde işlem kategorisini görünür kılmak için önemli varlıkların tüm formlarını ve görümlerini incelemeniz ve bu alanları bu varlıkların formlarına ve görünümlerine eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="190f9-109">To make transaction category visible in the UI in the pricing dimension solution, you will need to walk through all the forms and views of the key entities and add these fields to the forms and views of those entities.</span></span>
<span data-ttu-id="190f9-110">Aşağıdaki tabloda, yeni alanlarla güncelleştirilmesi gereken, varlığa göre listelenen kullanıma hazır form ve görünümlerin kapsamlı bir listesi yer alır.</span><span class="sxs-lookup"><span data-stu-id="190f9-110">The following table is a comprehensive list of the out-of-the box forms and views, listed by entity, that will need to be updated with the new fields.</span></span> <span data-ttu-id="190f9-111">Bu varlıklardaki özelleştirmelerinizde ek görünümler veya formlar varsa yeni alanları da bunlara ekleyin.</span><span class="sxs-lookup"><span data-stu-id="190f9-111">If there any additional views or forms in your customizations on these entities, add the new fields to those as well.</span></span>

|  <span data-ttu-id="190f9-112">Varlık</span><span class="sxs-lookup"><span data-stu-id="190f9-112">Entity</span></span>        | <span data-ttu-id="190f9-113">Formlar</span><span class="sxs-lookup"><span data-stu-id="190f9-113">Forms</span></span>     |<span data-ttu-id="190f9-114">Görünümler</span><span class="sxs-lookup"><span data-stu-id="190f9-114">Views</span></span>        |
| ------------------------------|---------------------------------|----------------------------------|
|  <span data-ttu-id="190f9-115">Rol Fiyatı</span><span class="sxs-lookup"><span data-stu-id="190f9-115">Role Price</span></span>|<span data-ttu-id="190f9-116">• Bilgi</span><span class="sxs-lookup"><span data-stu-id="190f9-116">• Information</span></span> |<span data-ttu-id="190f9-117">• Etkin Kaynak Kategorisi Fiyatları</span><span class="sxs-lookup"><span data-stu-id="190f9-117">• Active Resource Category Prices</span></span><br> <span data-ttu-id="190f9-118">• Kaynak Kategorisi Fiyatı İlişkili Görünümü</span><span class="sxs-lookup"><span data-stu-id="190f9-118">• Resource Category Price Associated View</span></span>|
|  <span data-ttu-id="190f9-119">Rol Fiyatı Kar Payı</span><span class="sxs-lookup"><span data-stu-id="190f9-119">Role Price Markup</span></span>|<span data-ttu-id="190f9-120">• Bilgi</span><span class="sxs-lookup"><span data-stu-id="190f9-120">• Information</span></span>|<span data-ttu-id="190f9-121">• Etkin Rol Fiyatı Kar Payı</span><span class="sxs-lookup"><span data-stu-id="190f9-121">• Active Role Price Markup</span></span><br><span data-ttu-id="190f9-122">• Rol Fiyatı Kar Payı İlişkili Görünümü</span><span class="sxs-lookup"><span data-stu-id="190f9-122">• Role Price Markup Associated View</span></span>|
|  <span data-ttu-id="190f9-123">Teklif satırı ayrıntısı</span><span class="sxs-lookup"><span data-stu-id="190f9-123">Quote line detail</span></span>|<span data-ttu-id="190f9-124">• Proje Bilgileri</span><span class="sxs-lookup"><span data-stu-id="190f9-124">• Project Information</span></span><br><span data-ttu-id="190f9-125">• Hızlı Proje Oluştur</span><span class="sxs-lookup"><span data-stu-id="190f9-125">• Project Quick Create</span></span>|<span data-ttu-id="190f9-126">• Etkin Teklif Satırı Ayrıntısı</span><span class="sxs-lookup"><span data-stu-id="190f9-126">• Active Quote Line Detail</span></span><br><span data-ttu-id="190f9-127">• Birleşik Teklif Satırı Ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="190f9-127">• Combined Quote Line Details</span></span><br><span data-ttu-id="190f9-128">• Teklif Satırı Ayrıntısı ilişkili görünümü</span><span class="sxs-lookup"><span data-stu-id="190f9-128">• Quote Line Detail associated view</span></span>|
|  <span data-ttu-id="190f9-129">Proje Sözleşme satırı ayrıntısı</span><span class="sxs-lookup"><span data-stu-id="190f9-129">Project Contract line detail</span></span>|<span data-ttu-id="190f9-130">• Proje Bilgileri</span><span class="sxs-lookup"><span data-stu-id="190f9-130">• Project Information</span></span><br><span data-ttu-id="190f9-131">• Hızlı Proje Oluştur</span><span class="sxs-lookup"><span data-stu-id="190f9-131">• Project Quick Create</span></span>|<span data-ttu-id="190f9-132">• Birleşik Sözleşme satırı Ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="190f9-132">• Combined Contract line Details</span></span><br><span data-ttu-id="190f9-133">• Etkin Sözleşme Satırı Ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="190f9-133">• Active Contract Line Details</span></span><br><span data-ttu-id="190f9-134">• Sözleşme Satırı Ayrıntısı ilişkili görünümü</span><span class="sxs-lookup"><span data-stu-id="190f9-134">• Contract Line Detail associated view</span></span>|
|  <span data-ttu-id="190f9-135">Proje Görevi</span><span class="sxs-lookup"><span data-stu-id="190f9-135">Project Task</span></span>|<span data-ttu-id="190f9-136">• Bilgi</span><span class="sxs-lookup"><span data-stu-id="190f9-136">• Information</span></span><br><span data-ttu-id="190f9-137">• Yeni Form</span><span class="sxs-lookup"><span data-stu-id="190f9-137">• New Form</span></span>||
|  <span data-ttu-id="190f9-138">Proje Takımı Üyesi</span><span class="sxs-lookup"><span data-stu-id="190f9-138">Project Team Member</span></span>|<span data-ttu-id="190f9-139">• Bilgi</span><span class="sxs-lookup"><span data-stu-id="190f9-139">• Information</span></span><br><span data-ttu-id="190f9-140">• Yeni Form</span><span class="sxs-lookup"><span data-stu-id="190f9-140">• New Form</span></span>|<span data-ttu-id="190f9-141">• Etkin Proje Takımı Üyeleri</span><span class="sxs-lookup"><span data-stu-id="190f9-141">• Active Project Team Members</span></span><br><span data-ttu-id="190f9-142">• Proje Takımı Üyeleri</span><span class="sxs-lookup"><span data-stu-id="190f9-142">• Project Team Members</span></span><br><span data-ttu-id="190f9-143">• Proje Takımı üyeleri ilişkili görünümü</span><span class="sxs-lookup"><span data-stu-id="190f9-143">• Project Team members associated View</span></span>|
|  <span data-ttu-id="190f9-144">Zaman Girişi</span><span class="sxs-lookup"><span data-stu-id="190f9-144">Time Entry</span></span>|<span data-ttu-id="190f9-145">• Bilgi</span><span class="sxs-lookup"><span data-stu-id="190f9-145">• Information</span></span><br><span data-ttu-id="190f9-146">• Zaman Girişi Oluştur</span><span class="sxs-lookup"><span data-stu-id="190f9-146">• Create Time Entry</span></span>|<span data-ttu-id="190f9-147">• Tarihe Göre Zaman Girişlerim</span><span class="sxs-lookup"><span data-stu-id="190f9-147">• My Time Entries By Date</span></span><br><span data-ttu-id="190f9-148">• Bu hafta için Zaman Girişlerim</span><span class="sxs-lookup"><span data-stu-id="190f9-148">• My time Entries for this week</span></span><br><span data-ttu-id="190f9-149">• Onaylanacak zaman girişleri</span><span class="sxs-lookup"><span data-stu-id="190f9-149">• Time entries for approval</span></span>|
|  <span data-ttu-id="190f9-150">Yevmiye Defteri Satırı</span><span class="sxs-lookup"><span data-stu-id="190f9-150">Journal Line</span></span>|<span data-ttu-id="190f9-151">• Bilgi</span><span class="sxs-lookup"><span data-stu-id="190f9-151">• Information</span></span><br><span data-ttu-id="190f9-152">• Hızlı oluşturma</span><span class="sxs-lookup"><span data-stu-id="190f9-152">• Quick create</span></span>|<span data-ttu-id="190f9-153">• Etkin yevmiye defteri satırları</span><span class="sxs-lookup"><span data-stu-id="190f9-153">• Active journal lines</span></span><br><span data-ttu-id="190f9-154">• Yevmiye Defteri Satırı ilişkili görünümü</span><span class="sxs-lookup"><span data-stu-id="190f9-154">• Journal Line associated view</span></span>|
|  <span data-ttu-id="190f9-155">Fatura Satırı Ayrıntısı</span><span class="sxs-lookup"><span data-stu-id="190f9-155">Invoice Line Detail</span></span>|<span data-ttu-id="190f9-156">• Bilgi</span><span class="sxs-lookup"><span data-stu-id="190f9-156">• Information</span></span><br><span data-ttu-id="190f9-157">• Hızlı oluşturma</span><span class="sxs-lookup"><span data-stu-id="190f9-157">• Quick create</span></span>|<span data-ttu-id="190f9-158">• Etkin Fatura Satırı Ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="190f9-158">• Active Invoice Line Details</span></span><br><span data-ttu-id="190f9-159">• Borçlandırılabilir Fatura İşlemleri</span><span class="sxs-lookup"><span data-stu-id="190f9-159">• Chargeable Invoice Transactions</span></span><br><span data-ttu-id="190f9-160">• Ücretsiz Fatura İşlemleri</span><span class="sxs-lookup"><span data-stu-id="190f9-160">• Complimentary Invoice Transactions</span></span><br><span data-ttu-id="190f9-161">• Fatura Satırı Ayrıntısı ilişkili görünümü</span><span class="sxs-lookup"><span data-stu-id="190f9-161">• Invoice Line Detail associated view</span></span><br><span data-ttu-id="190f9-162">• Borçlandırılamaz Fatura İşlemleri</span><span class="sxs-lookup"><span data-stu-id="190f9-162">• Non-Chargeable Invoice Transactions</span></span>|
|  <span data-ttu-id="190f9-163">Gerçek</span><span class="sxs-lookup"><span data-stu-id="190f9-163">Actual</span></span>|<span data-ttu-id="190f9-164">• Bilgi</span><span class="sxs-lookup"><span data-stu-id="190f9-164">• Information</span></span><br><span data-ttu-id="190f9-165">• Etkin Gerçek Tutarlar</span><span class="sxs-lookup"><span data-stu-id="190f9-165">• Active Actuals</span></span>|<span data-ttu-id="190f9-166">• Gerçek Tutar İlişkili görünümü</span><span class="sxs-lookup"><span data-stu-id="190f9-166">• Actual Associated view</span></span>|

## <a name="set-up-transaction-category-as-a-pricing-dimension"></a><span data-ttu-id="190f9-167">İşlem kategorisini fiyatlandırma boyutu olarak ayarlama</span><span class="sxs-lookup"><span data-stu-id="190f9-167">Set up transaction category as a pricing dimension</span></span>

1. <span data-ttu-id="190f9-168">Web arabiriminde **Project Service** > **Ayarlar** > **Parametreler** 'e gidin.</span><span class="sxs-lookup"><span data-stu-id="190f9-168">In the web interface, go to **Project Service** > **Settings** > **Parameters**.</span></span> 
2. <span data-ttu-id="190f9-169">**Parametreler** sayfasındaki **Tutar Tabanlı Fiyatlandırma Boyutları** sekmesinde, **Fiyatlandırma Boyutları** varlığındaki kayıtları gösteren sekmedeki ızgarayı not edin.</span><span class="sxs-lookup"><span data-stu-id="190f9-169">On the **Parameters** page, on the **Amount-Based Pricing Dimensions** tab, note the grid on the tab shows the records in the **Pricing Dimensions** entity.</span></span>
3. <span data-ttu-id="190f9-170">**İşlem Kategorisi** 'ni bu listeye ekleyin ve **Maliyet için Geçerli** ve **Satış için Geçerli** alanlarını **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="190f9-170">Add **Transaction Category** to this list and set the **Applicable to Cost** and **Applicable to Sale** fields set to **Yes**.</span></span>
4. <span data-ttu-id="190f9-171">**Boyut Türü** alanında **Tutar tabanlı** öğesini ve ardından maliyet ve satışla ilgili **İşlem Kategorisi** için önceliği seçin.</span><span class="sxs-lookup"><span data-stu-id="190f9-171">In the **Dimension Type** field, select **Amount-based** , and then select the priority for **Transaction Category** related to cost and sales.</span></span>