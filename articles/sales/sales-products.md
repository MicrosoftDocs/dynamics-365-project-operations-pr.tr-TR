---
title: Ürünler
description: Bu konu,kuruluşunuzun sunduğu ürün ve fiyatla ilgili müşterilere bilgi sağlamak için kullanabileceğiniz ürün kataloğu hakkında bilgiler sağlar.
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
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 28397fd49ad4cdb2c820ef4b6f198f410995ba0f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898735"
---
# <a name="products"></a><span data-ttu-id="26f95-103">Ürünler</span><span class="sxs-lookup"><span data-stu-id="26f95-103">Products</span></span>

<span data-ttu-id="26f95-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="26f95-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="26f95-105">Ürünler işletmenizin omurgasıdır.</span><span class="sxs-lookup"><span data-stu-id="26f95-105">Products are the backbone of your business.</span></span> <span data-ttu-id="26f95-106">Dynamics 365 Sales Professional içinde ürün kataloğu, ürünlerin ve bunların fiyatlandırma bilgileri topluluğudur.</span><span class="sxs-lookup"><span data-stu-id="26f95-106">The product catalog in Dynamics 365 Sales Professional is a collection of products and pricing information.</span></span> <span data-ttu-id="26f95-107">Ürün kataloğunu hızlıca oluşturarak satış temsilcilerinizin satışlarını artırmasını kolaylaştırın.</span><span class="sxs-lookup"><span data-stu-id="26f95-107">Make it easier for your sales reps to increase their sales by creating a product catalog quickly.</span></span>

## <a name="add-a-product"></a><span data-ttu-id="26f95-108">Ürün ekleme</span><span class="sxs-lookup"><span data-stu-id="26f95-108">Add a product</span></span>

1.  <span data-ttu-id="26f95-109">Sistem Yöneticisi veya Sales Manager Professional rolü ya da eşdeğer izinlere sahip olduğunuzdan emin olun, böylece Dynamics 365 Sales Professional içinde ürünler ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="26f95-109">Make sure you have the Sales Manager Professional or a System Administrator role so you can add products in Dynamics 365 Sales Professional.</span></span>
2.  <span data-ttu-id="26f95-110">Site haritasında, **Kurulum** altında **Ürünler**'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="26f95-110">In the site map, under **Setup**, select **Products**.</span></span>
3.  <span data-ttu-id="26f95-111">**Ürün Ekle**'yi seçin ve aşağıdaki bilgileri doldurun:</span><span class="sxs-lookup"><span data-stu-id="26f95-111">Select **Add Product** and fill in the following information:</span></span>

    -  <span data-ttu-id="26f95-112">**Ad**</span><span class="sxs-lookup"><span data-stu-id="26f95-112">**Name**</span></span>
    -  <span data-ttu-id="26f95-113">**Ürün Kimliği**</span><span class="sxs-lookup"><span data-stu-id="26f95-113">**Product ID**</span></span>
    -  <span data-ttu-id="26f95-114">**Ana öğe**: Ürün için bir ana ürün ailesi seçin.</span><span class="sxs-lookup"><span data-stu-id="26f95-114">**Parent**: Select a parent product family for the product.</span></span> <span data-ttu-id="26f95-115">Bir ürün ailesinde bir alt ürün oluşturuyorsanız, ana ürün ailesi adını buraya girilir.</span><span class="sxs-lookup"><span data-stu-id="26f95-115">If you're creating a child product in a product family, the name of the parent product family is populated here.</span></span> <span data-ttu-id="26f95-116">Bu, kayıt kaydedildikten sonra değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="26f95-116">This can't be changed after the record is saved.</span></span>
    -  <span data-ttu-id="26f95-117">**Geçerlilik Başlangıç Tarihi**/**Geçerlilik Bitiş Tarihi**: **Bir Geçerlilik Başlangıç Tarihi** ve **Geçerlilik Bitiş Tarihi** seçerek ürünün geçerli olacağı dönemi tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="26f95-117">**Valid From**/**Valid To**: Define the period the product is valid for by selecting a **Valid From** and **Valid To** date.</span></span>
    -  <span data-ttu-id="26f95-118">**Birim Grubu**: Bir Birim Grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="26f95-118">**Unit Group**: Select a unit group.</span></span> <span data-ttu-id="26f95-119">Birim grubu içinde bir ürünün satışa sunulduğu ve tek tek öğelerin daha büyük miktarlarda nasıl gruplandırıldığını tanımlayan çeşitli birimlerin koleksiyonudur.</span><span class="sxs-lookup"><span data-stu-id="26f95-119">A unit group is a collection of various units a product is sold in and defines how individual items are grouped into larger quantities.</span></span> <span data-ttu-id="26f95-120">Örneğin, ürün olarak tohumları ekliyorsanız, "Tohumlar" adıyla ve birincil birim olarak "paket" tanımlı bir birim grubu oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="26f95-120">For example, if you're adding seeds as a product, you might have created a unit group called "Seeds" and defined its primary unit as "packet."</span></span>
    -  <span data-ttu-id="26f95-121">**Varsayılan Birim**: Ürünün içinde en yaygın satılacağı birimi seçin.</span><span class="sxs-lookup"><span data-stu-id="26f95-121">**Default Unit**: Select the most common unit in which the product will be sold.</span></span> <span data-ttu-id="26f95-122">Biriler, ürünlerinizi sattığınız miktarlara veya ölçü birimlerine karşılık gelir.</span><span class="sxs-lookup"><span data-stu-id="26f95-122">Units are the quantities or measurements that you sell your products in.</span></span> <span data-ttu-id="26f95-123">Örneğin, bir ürün olarak tohum eklerseniz, bunları paketler, kutular veya paletler halinde satabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="26f95-123">For example, if you're adding seeds as a product, you can sell it in packets, boxes, or pallets.</span></span> <span data-ttu-id="26f95-124">Bunların her biri ürünün birimi haline gelir.</span><span class="sxs-lookup"><span data-stu-id="26f95-124">Each of these becomes a unit of the product.</span></span> <span data-ttu-id="26f95-125">Tohumlar çoğunlukla paketlerde satılıyorsa birim olarak bunu seçin.</span><span class="sxs-lookup"><span data-stu-id="26f95-125">If seeds are mostly sold in packets, select that as the unit.</span></span>
    -  <span data-ttu-id="26f95-126">**Varsayılan Fiyat Listesi**: Bu yeni bir ürünse, bu alan salt okunur durumdadır.</span><span class="sxs-lookup"><span data-stu-id="26f95-126">**Default Price List**: If this is a new product, this field is read-only.</span></span> <span data-ttu-id="26f95-127">Varsayılan fiyat listesini seçebilmek için gerekli tüm alanları doldurmanız ve kaydı kaydetmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="26f95-127">Before you can select a default price list, you must complete all the required fields and then save the record.</span></span> <span data-ttu-id="26f95-128">Varsayılan ayar listesi gerekmiyor olsa da, ürün kaydını kaydettikten sonra her ürün için varsayılan bir fiyat listesi ayarlamak oldukça yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="26f95-128">Although the default price list is not required, after you save the product record, it is a good idea to set a default price list for each product.</span></span> <span data-ttu-id="26f95-129">Ayrıca, bir müşteri kaydı bir fiyat listesi içermiyorsa, Sales teklifleri, siparişleri ve faturaları oluşturmak için varsayılan fiyatı kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="26f95-129">Then, if a customer record does not contain a price list, Sales can use the default price list for generating quotes, orders, and invoices.</span></span>
    -  <span data-ttu-id="26f95-130">**Desteklenen Ondalık Basamak Sayısı**: 0 ile 5 arasında bir tamsayı girin.</span><span class="sxs-lookup"><span data-stu-id="26f95-130">**Decimals Supported**: Enter a whole number between 0 and 5.</span></span> <span data-ttu-id="26f95-131">Ürün kesirli miktarlara bölünemiyorsa 0 yazın.</span><span class="sxs-lookup"><span data-stu-id="26f95-131">If the product can't be divided into fractional quantities, enter 0.</span></span> <span data-ttu-id="26f95-132">Ürün ilişkili bir fiyat listesine sahip değilse, teklif, sipariş veya fatura ürün kaydındaki **Miktar** alanının doğruluğu bu alandaki değerle karşılaştırılarak doğrulanır.</span><span class="sxs-lookup"><span data-stu-id="26f95-132">The precision of the **Quantity** field in the quote, order, or invoice product record is validated against the value in this field if the product does not have an associated price list.</span></span>
    -  <span data-ttu-id="26f95-133">**Konu**: Bu ürünü bir konuyla ilişkilendirin.</span><span class="sxs-lookup"><span data-stu-id="26f95-133">**Subject**: Associate this product with a subject.</span></span> <span data-ttu-id="26f95-134">Ürünlerinizi kategorilere ayırmak ve raporlara filtre uygulamak için konuları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="26f95-134">You can use subjects to categorize your products and to filter reports.</span></span>

4.  <span data-ttu-id="26f95-135">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="26f95-135">Select **Save**.</span></span>
5.  <span data-ttu-id="26f95-136">**Ek ayrıntılar** sekmesinde **Fiyat listesi öğeleri** bölümünde, **Diğer komutlar** simgesini ve sonra **Yeni fiyat listesi öğesi ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="26f95-136">On the **Additional Details** tab, in the **Price List Items** section, select **More commands**, and then select **Add New Price List Item**.</span></span>
7.  <span data-ttu-id="26f95-137">**Ek Ayrıntılar** sekmesinde **Ürün İlişkisi** bölümünde **Diğer komutlar** simgesini seçin ve sonra **Yeni Ürün Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="26f95-137">On the **Additional Details** tab, in the **Product Relationship** section, select the **More commands** icon, and then select **Add New Product Relationship.**</span></span>
8.  <span data-ttu-id="26f95-138">**Yeni Ürünü İlişkisi** formunda, aşağıdakileri yapın ve komut çubuğunda **Kaydet ve Kapat**'ı seçin:</span><span class="sxs-lookup"><span data-stu-id="26f95-138">In the **New Product Relationship** form, enter the following details, and on the command bar, select **Save and Close**:</span></span>

    -   <span data-ttu-id="26f95-139">**İlgili Ürün**: Üzerinde çalışmakta olduğunuz var olan ürün kaydına ilgili bir ürün olarak eklemek istediğiniz ürünü seçin.</span><span class="sxs-lookup"><span data-stu-id="26f95-139">**Related Product**: Select a product that you want to add as a related product to the existing product record you're working on.</span></span>
    -   <span data-ttu-id="26f95-140">**Satış İlgi Türü**: Ürünü yukarı satış mı, çapraz satış mı, aksesuar mı, yoksa ikame ürün mü olarak eklemek istediğinizi seçin.</span><span class="sxs-lookup"><span data-stu-id="26f95-140">**Sales Relation Type**: Select whether you want to add the product as an up-sell, cross-sell, accessory, or substitute product.</span></span>
    -   <span data-ttu-id="26f95-141">**Yön**: Ürünler arasındaki ilişkinin tek yönlü mü, yoksa çift yönlü mü olacağını seçin.</span><span class="sxs-lookup"><span data-stu-id="26f95-141">**Direction**:Select whether the relationship between the products will be unidirectional or bidirectional.</span></span> <span data-ttu-id="26f95-142">Tek Yönlü'yü seçtiğinizde, **İlgili Ürün** olarak seçtiğiniz ürün varolan ürün için öneri olarak görüntülenir, ancak tersi gerçekleşmez.</span><span class="sxs-lookup"><span data-stu-id="26f95-142">When you select unidirectional, the product that you select in **Related Product** will be shown as a recommendation for the existing product but not vice versa.</span></span>

9.  <span data-ttu-id="26f95-143">Ürün formunda, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="26f95-143">On the Product form, select **Save**.</span></span>

## <a name="import-products"></a><span data-ttu-id="26f95-144">Ürünleri içeri aktar</span><span class="sxs-lookup"><span data-stu-id="26f95-144">Import products</span></span>

<span data-ttu-id="26f95-145">Toplu ürün verilerini Dynamics 365 Sales içine taşımak için alma şablonlarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="26f95-145">You can use import templates to bring bulk product data into Dynamics 365 Sales.</span></span>

## <a name="revise-a-product"></a><span data-ttu-id="26f95-146">Ürünü düzeltme</span><span class="sxs-lookup"><span data-stu-id="26f95-146">Revise a product</span></span>

<span data-ttu-id="26f95-147">Özellikleri hemen gerektiği gibi düzelterek ve bilgileri yeniden yayımlayarak ürün stokunu güncel tutun; böylece, satış aracılarınızın stoktaki en son değişiklikleri görebilir.</span><span class="sxs-lookup"><span data-stu-id="26f95-147">Keep the product inventory updated by quickly revising properties for the products, as required, and republishing the information so that your sales agents can see the latest changes to the inventory.</span></span>

1.  <span data-ttu-id="26f95-148">Şu güvenlik rollerinden birine ya da eşdeğer izinlere sahip olduğunuzdan emin olun: Sistem Yöneticisi, Sistem Özelleştirici, Satış Yöneticisi, Satış Başkan Yardımcısı, Pazarlama Başkan Yardımcısı veya CEO-İşletme Yöneticisi.</span><span class="sxs-lookup"><span data-stu-id="26f95-148">Make sure that you have one of the following security roles or equivalent permissions: System Administrator, System Customizer, Sales Manager, Vice President of Sales, Vice President of Marketing, or CEO-Business Manager.</span></span>
2.  <span data-ttu-id="26f95-149">Site haritasında **Ürünler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="26f95-149">In the site map, select **Products**.</span></span>
3.  <span data-ttu-id="26f95-150">Değiştirmek istediğiniz etkin bir ürünü seçin; komut çubuğunda **Düzelt**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="26f95-150">Open an active product that you want to change, and on the command bar, select **Revise**.</span></span>
4.  <span data-ttu-id="26f95-151">**Düzeltmeyi Onayla** iletişim kutusunda **Onayla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="26f95-151">In the **Confirm Revise** dialog box, select **Confirm**.</span></span> <span data-ttu-id="26f95-152">Ürün durumu **Düzeltme Yapılıyor** olarak değişir.</span><span class="sxs-lookup"><span data-stu-id="26f95-152">This will change the product status to **Under Revision**.</span></span>
5.  <span data-ttu-id="26f95-153">Değişiklikleri yaptıktan sonra, komut çubuğunda, **Yayınla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="26f95-153">After you're done making changes, on the command bar, select **Publish**.</span></span>

    > [!TIP]
    > <span data-ttu-id="26f95-154">Değişiklikleri geri almak ve ürünün son etkin sürümüne devam etmek için **Geri al** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="26f95-154">To revert the changes and continue with the last active version of the product, select **Revert**.</span></span> <span data-ttu-id="26f95-155">Ürünün durumu **Etkin** olarak değişir.</span><span class="sxs-lookup"><span data-stu-id="26f95-155">This changes the status of the product back to **Active**.</span></span>

## <a name="clone-a-product"></a><span data-ttu-id="26f95-156">Ürün kopyalama</span><span class="sxs-lookup"><span data-stu-id="26f95-156">Clone a product</span></span> 

<span data-ttu-id="26f95-157">Yeni bir ürün oluşturduğunuzda var olan birini kopyalayarak zaman kazanın.</span><span class="sxs-lookup"><span data-stu-id="26f95-157">When you're creating a new product, save time by cloning an existing one.</span></span> <span data-ttu-id="26f95-158">Böylece, özgün kaydın ad ve kimlik dışında olan tüm ayrıntılarını içeren kopyası oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="26f95-158">This creates a copy of the original record with all the details except for the name and ID.</span></span>

1.  <span data-ttu-id="26f95-159">Şu güvenlik rollerinden birine ya da eşdeğer izinlere sahip olduğunuzdan emin olun: Sistem Yöneticisi, Sistem Özelleştirici, Satış Yöneticisi, Satış Başkan Yardımcısı, Pazarlama Başkan Yardımcısı veya CEO-İşletme Yöneticisi.</span><span class="sxs-lookup"><span data-stu-id="26f95-159">Make sure that you have one of the following security roles or equivalent permissions: System Administrator, System Customizer, Sales Manager, Vice President of Sales, Vice President of Marketing, or CEO-Business Manager.</span></span>
2.  <span data-ttu-id="26f95-160">Site haritasında **Ürünler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="26f95-160">In the site map, select **Products**.</span></span>
3.  <span data-ttu-id="26f95-161">Kopyalamak istediğiniz bir ürün satış kaydı seçin ve komut çubuğunda **Kopyala**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="26f95-161">Select a product record that you want to clone, and on the command bar, select **Clone**.</span></span> <span data-ttu-id="26f95-162">Bir onay iletişim kutusu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="26f95-162">A confirmation dialog box appears.</span></span>
4.  <span data-ttu-id="26f95-163">**Onayla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="26f95-163">Select **Confirm**.</span></span>

<span data-ttu-id="26f95-164">Yeni ürün kaydı, adı ve kimliği dışında özgün olanla aynı ayrıntılara sahip olarak açılır.</span><span class="sxs-lookup"><span data-stu-id="26f95-164">A new product record opens with the same details as the original one except for the name and ID.</span></span>

## <a name="retire-a-product"></a><span data-ttu-id="26f95-165">Ürünü kullanım dışına alma</span><span class="sxs-lookup"><span data-stu-id="26f95-165">Retire a product</span></span> 

<span data-ttu-id="26f95-166">Kuruluşunuz artık ürün satmıyorsa, ürün artık satış aracılarınızda olmayacak şekilde kullanım dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="26f95-166">If your organization doesn't sell a product anymore, retire it so that the product is no longer available to your sales agents.</span></span>

1.  <span data-ttu-id="26f95-167">Sistem Yöneticisi veya Sales Professional Yöneticisi rolü ya da eşdeğer izinlere sahip olduğunuzdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="26f95-167">Make sure that you have the System Administrator or Sales Professional Manager role or equivalent permissions.</span></span>
2.  <span data-ttu-id="26f95-168">Site haritasında **Ürünler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="26f95-168">In the site map, select **Products**.</span></span>
3.  <span data-ttu-id="26f95-169">Değiştirmek istediğiniz etkin bir ürünü seçin; komut çubuğunda **Kullanım dışı bırak**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="26f95-169">Open an active product that you want to retire, and on the command bar, select **Retire**.</span></span>
4.  <span data-ttu-id="26f95-170">**Kullanım Dışı Bırakmayı Onayla** iletişim **Onayla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="26f95-170">In the **Confirm Retire** dialog box, select **Confirm**.</span></span>


## <a name="delete-a-product"></a><span data-ttu-id="26f95-171">Ürünü silme</span><span class="sxs-lookup"><span data-stu-id="26f95-171">Delete a product</span></span>

<span data-ttu-id="26f95-172">Bir ürününü satışını durdurmak için ürünü silin.</span><span class="sxs-lookup"><span data-stu-id="26f95-172">To stop selling a product, delete it.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="26f95-173">Silinen kayıtları kurtaramazsınız.</span><span class="sxs-lookup"><span data-stu-id="26f95-173">You can't recover a deleted record.</span></span>

1.  <span data-ttu-id="26f95-174">Sistem Yöneticisi veya Sales Professional Yöneticisi rolü ya da eşdeğer izinlere sahip olduğunuzdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="26f95-174">Make sure that you have the System Administrator or Sales Professional Manager role or equivalent permissions.</span></span>
2.  <span data-ttu-id="26f95-175">Site haritasında **Ürünler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="26f95-175">In the site map, select **Products**.</span></span>
3.  <span data-ttu-id="26f95-176">Silmek istediğiniz bir ürün satış kaydı seçin ve komut çubuğunda **Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="26f95-176">Select a product record you want to delete, and on the command bar, select **Delete**.</span></span>
4.  <span data-ttu-id="26f95-177">**Silme Onayı** iletişim kutusunda **Devam et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="26f95-177">In the **Confirm Deletion** dialog box, select **Continue**.</span></span>
 
 ## <a name="quantity-factors-for-products"></a><span data-ttu-id="26f95-178">Ürünler için miktar faktörleri</span><span class="sxs-lookup"><span data-stu-id="26f95-178">Quantity factors for products</span></span>

<span data-ttu-id="26f95-179">Miktar faktörleri abonelik tabanlı ürünlerin satışını destekler.</span><span class="sxs-lookup"><span data-stu-id="26f95-179">Quantity factors support the sale of subscription-based products.</span></span> <span data-ttu-id="26f95-180">Abonelik tabanlı ürünler için, teklif veya proje sözleşmesi satırındaki miktar kullanıcı ay sayısı olarak ifade edilir.</span><span class="sxs-lookup"><span data-stu-id="26f95-180">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user months.</span></span>

<span data-ttu-id="26f95-181">Genellikle abonelik yazılımının fiyatı, katalogda kullanıcı başına aylık fiyat olarak depolanır.</span><span class="sxs-lookup"><span data-stu-id="26f95-181">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="26f95-182">Bununla birlikte, bunun yerine başka zaman açıklamaları da kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="26f95-182">However, you can use other time descriptions instead.</span></span> <span data-ttu-id="26f95-183">Satış işlemi sırasında, teklif satırındaki fiyat genellikle BT satış aracısı tarafından sağlanan ve indirim uygulanan kullanıcı başına aylık fiyattır.</span><span class="sxs-lookup"><span data-stu-id="26f95-183">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="26f95-184">Her anlaşmanın farklı sayıda kullanıcısı ve farklı abonelik ayı sayısı vardır.</span><span class="sxs-lookup"><span data-stu-id="26f95-184">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="26f95-185">Teklif satırının tutarını hesaplamak için kullanılan miktar bir kullanıcı sayısı ve abonelik ayları sayısı ürünüdür.</span><span class="sxs-lookup"><span data-stu-id="26f95-185">The quantity that is used to compute the amount of the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="26f95-186">Miktar faktörleri ürün özniteliklerine dayanır.</span><span class="sxs-lookup"><span data-stu-id="26f95-186">Quantity factors rely on product attributes.</span></span> <span data-ttu-id="26f95-187">Bir ürün için belirli özellikler yapılandırdığınızda miktar faktörleri olarak bu özelliklerin bir alt kümesini veya tüm özellikleri işaretleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="26f95-187">When you configure specific properties for a product, you can flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="26f95-188">Sistem, yalnızca sayısal veri türüne sahip sayısal özellikleri veya ürün özelliklerini miktar faktörü olarak işaretlenmiş olarak doğrular.</span><span class="sxs-lookup"><span data-stu-id="26f95-188">The system validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="26f95-189">Miktar faktörlerinin yapılandırıldığı bir ürün bir teklif satırına eklendiğinde, teklif satırındaki **Miktar** alanı salt okunur bir alan haline gelir.</span><span class="sxs-lookup"><span data-stu-id="26f95-189">When a product that quantity factors are configured for is added to a quote line, the **Quantity** field on the quote line becomes a read-only field.</span></span> <span data-ttu-id="26f95-190">Miktar faktörleri olan ürün özelliklerinin değerlerini girdikten sonra teklif satırı miktarını hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="26f95-190">After you enter values for product properties that are quantity factors, the quantity of the quote line is calculated.</span></span>

<span data-ttu-id="26f95-191">Örneğin, aşağıdaki özellikler varsa:</span><span class="sxs-lookup"><span data-stu-id="26f95-191">For example, if there are the following properties:</span></span> 

- <span data-ttu-id="26f95-192">**Kullanıcı sayısı**: kullanıcı sayısı</span><span class="sxs-lookup"><span data-stu-id="26f95-192">**No of users**: The number of users</span></span> 
- <span data-ttu-id="26f95-193">**Ay sayısı**: abonelik ayları sayısı</span><span class="sxs-lookup"><span data-stu-id="26f95-193">**No of Months**: The number of subscription months</span></span>
- <span data-ttu-id="26f95-194">**Ürün SKU'su**</span><span class="sxs-lookup"><span data-stu-id="26f95-194">**Product SKU**</span></span> 

<span data-ttu-id="26f95-195">**Kullanıcı Sayısı** ve **Ay Sayısı** özellikleri ürün satırının özellikleri düzenlenerek miktar faktörü olarak işaretlenebilir.</span><span class="sxs-lookup"><span data-stu-id="26f95-195">The **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span> 