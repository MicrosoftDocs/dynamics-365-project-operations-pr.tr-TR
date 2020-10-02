---
title: Özel alanları fiyatlandırma boyutları olarak ayarlama
description: Bu konuda, özel alanları kullanarak fiyatlandırma boyutlarının ayarlanması hakkında bilgi verilmektedir.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3a2a3b48df02853e519a45dc1d37052c8ba2529d
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896620"
---
# <a name="set-up-custom-fields-as-pricing-dimensions"></a><span data-ttu-id="8b55c-103">Özel alanları fiyatlandırma boyutları olarak ayarlama</span><span class="sxs-lookup"><span data-stu-id="8b55c-103">Set up custom fields as pricing dimensions</span></span>

<span data-ttu-id="8b55c-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="8b55c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8b55c-105">Başlamadan önce, bu konunun [Özel alanlar ve varlıklar oluşturma](create-custom-fields-entities-pricing-dimensions.md) ve [Fiyat ayarı ve işlem tabanlı varlıklara gerekli özel alanlar ekleme](add-custom-fields-price-setup-transactional-entities.md) konu başlıklarındaki yordamları tamamladığınızı varsaydığını bilmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="8b55c-105">Before you begin, this topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities-pricing-dimensions.md) and [Add required custom fields to price setup and transactional entities](add-custom-fields-price-setup-transactional-entities.md).</span></span> <span data-ttu-id="8b55c-106">Bu yordamları tamamlamadıysanız geri dönüp tamamlayın ve ardından bu konuya geri dönün.</span><span class="sxs-lookup"><span data-stu-id="8b55c-106">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span> 

<span data-ttu-id="8b55c-107">Bu konuda, özel fiyatlandırma boyutlarının ayarlanması hakkında bilgi verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="8b55c-107">This topic provides information about setting up custom pricing dimensions.</span></span> <span data-ttu-id="8b55c-108">**Parametreler** sayfasındaki **Tutar Tabanlı Fiyatlandırma Boyutları** sekmesinde, fiyatlandırma boyutları varlıklarındaki kayıtları gösteren sekmedeki ızgarayı not edin.</span><span class="sxs-lookup"><span data-stu-id="8b55c-108">On the **Parameters** page, the **Amount-Based Pricing Dimensions** tab shows the records in the pricing dimension entities.</span></span> <span data-ttu-id="8b55c-109">Varsayılan olarak, bu sekmedeki ızgarada iki satır vardır:</span><span class="sxs-lookup"><span data-stu-id="8b55c-109">By default, there are two rows in the grid on this tab:</span></span>

- <span data-ttu-id="8b55c-110">**msdyn_resourcecategory** (Rol)</span><span class="sxs-lookup"><span data-stu-id="8b55c-110">**msdyn_resourcecategory** (Role)</span></span>
- <span data-ttu-id="8b55c-111">**msdyn_OrganizationalUnit** (Kuruluş Birimi)</span><span class="sxs-lookup"><span data-stu-id="8b55c-111">**msdyn_OrganizationalUnit** (Organizational Unit)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8b55c-112">Bu satırları silmeyin.</span><span class="sxs-lookup"><span data-stu-id="8b55c-112">Do not delete these rows.</span></span> <span data-ttu-id="8b55c-113">Ancak bu satırlara ihtiyacınız yoksa, **Maliyet için Geçerli**, **Satış için Geçerli** ve **Satın Alma için Geçerli** seçeneklerini **Hayır** olarak ayarlayarak belirli bir bağlamda geçersiz duruma getirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8b55c-113">However, if you do not need them, you can make them not applicable in a specific context by setting **Applicable to Cost**, **Applicable to Sales**, and **Applicable to Purchase** all to **No**.</span></span> <span data-ttu-id="8b55c-114">Bu öznitelik değerlerinin **Hayır** olarak ayarlanması alanın bir fiyatlandırma boyutu olmamasıyla aynı etkiye sahiptir.</span><span class="sxs-lookup"><span data-stu-id="8b55c-114">Setting these attribute values to **No** has the same effect of not having the field as a pricing dimension.</span></span>

<span data-ttu-id="8b55c-115">Bir alanın fiyatlandırma boyutu olması için:</span><span class="sxs-lookup"><span data-stu-id="8b55c-115">For a field to become a pricing dimension, it must be:</span></span>

- <span data-ttu-id="8b55c-116">**Rol Fiyatı** ve **Rol Fiyatı kar payı** varlıklarında bir alan olarak oluşturulmalıdır.</span><span class="sxs-lookup"><span data-stu-id="8b55c-116">Created as a field in the **Role Price** and **Role Price markup** entities.</span></span> <span data-ttu-id="8b55c-117">Bunun nasıl yapılacağı hakkında daha fazla bilgi için [Fiyat ayarı ve işlem tabanlı varlıklara özel alanlar ekleme](add-custom-fields-price-setup-transactional-entities.md) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="8b55c-117">For more information on how to do this, see [Add custom fields to price setup and transactional entities](add-custom-fields-price-setup-transactional-entities.md).</span></span>
- <span data-ttu-id="8b55c-118">**Fiyatlandırma Boyutu** tablosunda bir satır olarak oluşturulmalıdır.</span><span class="sxs-lookup"><span data-stu-id="8b55c-118">Created as a row in the **Pricing Dimension** table.</span></span> <span data-ttu-id="8b55c-119">Örneğin, fiyatlandırma boyutu satırlarını aşağıdaki grafikte gösterildiği şekilde ekleyin.</span><span class="sxs-lookup"><span data-stu-id="8b55c-119">For example, add pricing dimension rows as shown in the following graphic.</span></span> 

<span data-ttu-id="8b55c-120">Kaynak Çalışma saatlerinin (**msdyn_resourceworkhours**) kar payı tabanlı bir boyut olarak eklenir ve **Kar Payı Tabanlı Fiyatlandırma Boyutu** sekmesinde ızgara olarak eklenir.</span><span class="sxs-lookup"><span data-stu-id="8b55c-120">Resource Work hours (**msdyn_resourceworkhours**) is added as a markup-based dimension and has been added to the grid on the **Markup Based Pricing Dimension** tab.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8b55c-121">Bu tablodaki var olan veya yeni, tüm fiyat boyutu verileri ancak önbellek yenilendikten sonra fiyatlandırma iş mantığına yansıtılır.</span><span class="sxs-lookup"><span data-stu-id="8b55c-121">Any change to pricing dimension data in this table, existing or new, is propagated to the pricing business logic only after the cache is refreshed.</span></span> <span data-ttu-id="8b55c-122">Önbellek yenileme işlemi 10 dakika kadar sürebilir.</span><span class="sxs-lookup"><span data-stu-id="8b55c-122">The cache refresh time may take up to 10 minutes.</span></span> <span data-ttu-id="8b55c-123">Fiyatlandırma Boyutu verilerinde yapılan değişiklikler sonucunda fiyat varsayılan mantığındaki değişiklikleri görmek için bu sürenin geçmesini bekleyin.</span><span class="sxs-lookup"><span data-stu-id="8b55c-123">Allow that length of time to see the changes in price defaulting logic that must result from changes to the Pricing Dimension data.</span></span>


## <a name="attributes-of-the-pricing-dimensions-table"></a><span data-ttu-id="8b55c-124">Fiyatlandırma Boyutları Öznitelikleri tablosu</span><span class="sxs-lookup"><span data-stu-id="8b55c-124">Attributes of the Pricing Dimensions table</span></span>
<span data-ttu-id="8b55c-125">Aşağıdaki bölümlerde **Fiyatlandırma Boyutları** tablosundaki farklı öznitelikler hakkında bilgi sağlanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="8b55c-125">The following sections provide information about the different attributes in the **Pricing Dimensions** table.</span></span>

### <a name="pricing-dimension-name"></a><span data-ttu-id="8b55c-126">Fiyatlandırma Boyutu Adı</span><span class="sxs-lookup"><span data-stu-id="8b55c-126">Pricing Dimension Name</span></span>
<span data-ttu-id="8b55c-127">Bu değer özel fiyatlandırma boyutlarının **Rol Fiyatı** tablosuna eklenen alanın şema adıyla aynı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="8b55c-127">This value should be the exact same as the schema name of the field that is added to the **Role Price** table for custom pricing dimensions.</span></span> <span data-ttu-id="8b55c-128">**Rol Fiyatı** tablosuna alan hakkında daha fazla bilgi için [Fiyat ayarı ve işlem tabanlı varlıklara özel alanlar ekleme](add-custom-fields-price-setup-transactional-entities.md) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="8b55c-128">For more information about adding fields to the **Role Price** table, see [Add custom fields to price setup and transactional entities](add-custom-fields-price-setup-transactional-entities.md).</span></span>

### <a name="type-of-dimension"></a><span data-ttu-id="8b55c-129">Boyut türü</span><span class="sxs-lookup"><span data-stu-id="8b55c-129">Type of dimension</span></span>
<span data-ttu-id="8b55c-130">İki tür fiyatlandırma boyutu vardır:</span><span class="sxs-lookup"><span data-stu-id="8b55c-130">There are two types of pricing dimensions:</span></span>
  
  - <span data-ttu-id="8b55c-131">**Tutar tabanlı boyutlar**: Giriş bağlamlarından alınan boyut değerleri **Rol Fiyatı** satırındaki boyut değerleriyle eşleştirilir ve fiyat/maliyet varsayılan olarak doğrudan **Rol Fiyatı** tablosundan ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="8b55c-131">**Amount-based dimensions**: The dimension values from the input context are matched to the dimension values on **Role Price** line and the price/cost is defaulted directly from the **Role Price** table.</span></span>
  - <span data-ttu-id="8b55c-132">**Kar payı tabanlı boyutlar**: Bunlar fiyat/maliyet almak için aşağıdaki 3 adımlı işlemi kullanacağı boyutlardır:</span><span class="sxs-lookup"><span data-stu-id="8b55c-132">**Markup-based dimensions**: These are dimensions where the following three-step process to get the price/cost is used:</span></span>
 
    1. <span data-ttu-id="8b55c-133">Taban fiyatı almak için giriş bağlamından kar payı tabanlı olmayan boyut değerleri Rol Fiyatı satırıyla eşleştirilir.</span><span class="sxs-lookup"><span data-stu-id="8b55c-133">The non-markup-based dimension values from the input context are matched to the Role Price line to get the base rate.</span></span>
    2. <span data-ttu-id="8b55c-134">Kar payı yüzdesi almak için giriş bağlamından tüm boyut değerleri **Rol Fiyatı Kar Payı** satırıyla eşleştirilir.</span><span class="sxs-lookup"><span data-stu-id="8b55c-134">The dimension values from the input context are matched to the **Role Price Markup** line to get a markup percentage.</span></span>
    3. <span data-ttu-id="8b55c-135">İkinci adımda elde edilen kar payı yüzdesi son fiyat/maliyet değerine ulaşmak için ilk adımdaki **Rol Fiyatı** tablosundan alınan taban fiyata uygulanır.</span><span class="sxs-lookup"><span data-stu-id="8b55c-135">The markup percentage from the second step is applied to the base rate obtained from the **Role Price** table in the first step to arrive at final price/cost.</span></span>
   
   <span data-ttu-id="8b55c-136">Aşağıdaki tabloda fiyat kar paylarını hesaplama gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="8b55c-136">The following table illustrates the calculation of price markups.</span></span>
  
| <span data-ttu-id="8b55c-137">Rol</span><span class="sxs-lookup"><span data-stu-id="8b55c-137">Role</span></span>        | <span data-ttu-id="8b55c-138">Kuruluş Birimi</span><span class="sxs-lookup"><span data-stu-id="8b55c-138">Org Unit</span></span>    |<span data-ttu-id="8b55c-139">İş Konumu</span><span class="sxs-lookup"><span data-stu-id="8b55c-139">Work Location</span></span>      |<span data-ttu-id="8b55c-140">Standart Başlık</span><span class="sxs-lookup"><span data-stu-id="8b55c-140">Standard Title</span></span>      |<span data-ttu-id="8b55c-141">Kaynak Çalışma Saatleri</span><span class="sxs-lookup"><span data-stu-id="8b55c-141">Resource Work Hours</span></span>      |  <span data-ttu-id="8b55c-142">Kar Payı</span><span class="sxs-lookup"><span data-stu-id="8b55c-142">Mark Up</span></span>|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | <span data-ttu-id="8b55c-143">Contoso Hindistan</span><span class="sxs-lookup"><span data-stu-id="8b55c-143">Contoso India</span></span>|<span data-ttu-id="8b55c-144">Yerinde</span><span class="sxs-lookup"><span data-stu-id="8b55c-144">Onsite</span></span>            |                    |<span data-ttu-id="8b55c-145">Fazla Mesai</span><span class="sxs-lookup"><span data-stu-id="8b55c-145">Overtime</span></span>                 |<span data-ttu-id="8b55c-146">15</span><span class="sxs-lookup"><span data-stu-id="8b55c-146">15</span></span>     |
|             | <span data-ttu-id="8b55c-147">Contoso Hindistan</span><span class="sxs-lookup"><span data-stu-id="8b55c-147">Contoso India</span></span>|<span data-ttu-id="8b55c-148">Yerel</span><span class="sxs-lookup"><span data-stu-id="8b55c-148">Local</span></span>             |                    |<span data-ttu-id="8b55c-149">Fazla Mesai</span><span class="sxs-lookup"><span data-stu-id="8b55c-149">Overtime</span></span>                 |<span data-ttu-id="8b55c-150">10</span><span class="sxs-lookup"><span data-stu-id="8b55c-150">10</span></span>     |
|             | <span data-ttu-id="8b55c-151">Contoso ABD</span><span class="sxs-lookup"><span data-stu-id="8b55c-151">Contoso US</span></span>   |<span data-ttu-id="8b55c-152">Yerel</span><span class="sxs-lookup"><span data-stu-id="8b55c-152">Local</span></span>             |                    |<span data-ttu-id="8b55c-153">Fazla Mesai</span><span class="sxs-lookup"><span data-stu-id="8b55c-153">Overtime</span></span>                 |<span data-ttu-id="8b55c-154">20</span><span class="sxs-lookup"><span data-stu-id="8b55c-154">20</span></span>     |


<span data-ttu-id="8b55c-155">Taban fiyatı 100 ABD Doları olan Contoso Hindistan'dan bir kaynak yerinde çalışıyorsa ve zaman girişinde 8 saat Normal ve 2 saat de fazla mesai girişi yaparsa, fiyatlandırma altyapısı 8 saat için taban fiyatı olarak 100 ABD Doları kullanarak 800 ABD Doları elde edilir.</span><span class="sxs-lookup"><span data-stu-id="8b55c-155">If a resource from Contoso India whose base rate is 100 USD is working onsite, and they log 8 hours of Regular time and 2 hours of overtime on the time entry, the pricing engine will use the base rate of 100 for the 8 hours to record 800 USD.</span></span> <span data-ttu-id="8b55c-156">2 saatlik fazla mesai için 100 ABD Doları değerindeki taban fiyata %15 kar payı eklenir ve 115 ABD Doları elde edilir. Toplamda maliyet 230 USD Doları kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="8b55c-156">For the 2 hours overtime, a markup of 15% will be applied to the base rate of 100 to get a unit price of 115 USD and will record a total cost of 230 USD.</span></span>

### <a name="applicable-to-cost"></a><span data-ttu-id="8b55c-157">Maliyet için Geçerli</span><span class="sxs-lookup"><span data-stu-id="8b55c-157">Applicable to Cost</span></span> 
<span data-ttu-id="8b55c-158">Bu değer **Evet** olarak ayarlandığında maliyet ve kar payı oranları alınırken **Rol Fiyatı** ve **Rol Fiyatı Kar Payı** ile eşleştirmek için giriş bağlamından gelen boyut değerinin kullanılması gerektiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="8b55c-158">If this is set to **Yes**, it indicates that the dimension value from the input context should be used to match to the **Role Price** and **Role Price Markup** when retrieving the cost and markup rates.</span></span>

### <a name="applicable-to-sales"></a><span data-ttu-id="8b55c-159">Satış için Geçerli</span><span class="sxs-lookup"><span data-stu-id="8b55c-159">Applicable to Sales</span></span>
<span data-ttu-id="8b55c-160">Bu değer **Evet** olarak ayarlandığında fatura ve kar payı oranları alınırken **Rol Fiyatı** ve **Rol Fiyatı Kar Payı** ile eşleştirmek için giriş bağlamından gelen boyut değerinin kullanılması gerektiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="8b55c-160">If this is set to **Yes**, it indicates that the dimension value from the input context should be used to match to the **Role Price** and **Role Price Markup** when retrieving the bill and markup rates.</span></span>

### <a name="applicable-to-purchase"></a><span data-ttu-id="8b55c-161">Satın Alma için Geçerli</span><span class="sxs-lookup"><span data-stu-id="8b55c-161">Applicable to Purchase</span></span>
<span data-ttu-id="8b55c-162">Bu değer **Evet** olarak ayarlandığında satınalma fiyatı alınırken **Rol Fiyatı** ve **Rol Fiyatı Kar Payı** ile eşleştirmek için giriş bağlamından gelen boyut değerinin kullanılması gerektiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="8b55c-162">If this is set to **Yes**, it indicates that the dimension value from the input context should be used to match to the **Role Price** and **Role Price Markup** when retrieving the purchase price.</span></span> <span data-ttu-id="8b55c-163">Alt üstlenici senaryoları desteklenmez, bu nedenle bu alan kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="8b55c-163">Subcontracting scenarios are not supported, so this field is not used.</span></span> 

### <a name="priority"></a><span data-ttu-id="8b55c-164">Öncelik</span><span class="sxs-lookup"><span data-stu-id="8b55c-164">Priority</span></span>
<span data-ttu-id="8b55c-165">Boyut önceliğinin ayarlanması fiyatlandırma işlevinin giriş boyutu değerleri ve **Rol Fiyatı** veya **Rol Fiyatı Kar Payı** tablolarından alınan değerler arasında tam bir eşleşme bulamadığında bile bir fiyat üretmesine yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="8b55c-165">Setting the dimension priority helps pricing produce a price even when it can't find an exact match between the input dimension values and the values from the **Role Price** or **Role Price Markup** tables.</span></span> <span data-ttu-id="8b55c-166">Bu senaryoda boyutları öncelik sıralarına göre ölçerek eşleşmeyen boyut değerleri için null değerler kullanılır.</span><span class="sxs-lookup"><span data-stu-id="8b55c-166">In this scenario, null values are used for unmatched dimension values by weighing the dimensions in order of their priority.</span></span>

- <span data-ttu-id="8b55c-167">**Maliyet Önceliği**: Bir boyutun maliyet önceliği değeri maliyet fiyatları ayarıyla eşleştirilirken bu boyutun ağırlığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8b55c-167">**Cost Priority**: The value of a dimension's cost priority will indicate the weight of that dimension when matching against the setup of cost prices.</span></span> <span data-ttu-id="8b55c-168">**Maliyet Önceliği** değeri **Maliyet için Geçerli** olan boyutlar arasında benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="8b55c-168">The value of **Cost Priority** must be unique across dimensions that are **Applicable to Cost**.</span></span>
- <span data-ttu-id="8b55c-169">**Satış Önceliği**: Bir boyutun satış önceliği değeri satış fiyatları veya fatura oranları ayarıyla eşleştirilirken bu boyutun ağırlığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8b55c-169">**Sales Priority**: The value of dimension's sales priority will indicate the weight of that dimension when matching against the setup of sales prices or bill rates.</span></span> <span data-ttu-id="8b55c-170">**Satış Önceliği** değeri **Satış için Geçerli** olan boyutlar arasında benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="8b55c-170">The value of **Sales Priority** must be unique across dimensions that are **Applicable to Sales**.</span></span>