---
title: Yeni özel varlık formları ekleme (Project Service Automation 2. x)
description: Bu konu, Dynamics 365 Project Service Automation 2. x içindeki fırsatlar, teklifler, siparişler veya faturalar için özel varlık formlarının nasıl ekleneceği hakkında bilgi sağlar.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 9c9e31dc6d4d5a8ad5cc568f2d7d673c8703936d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284877"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a><span data-ttu-id="0a83d-103">Yeni özel varlık formları ekleme (Project Service Automation 2. x)</span><span class="sxs-lookup"><span data-stu-id="0a83d-103">Add new custom entity forms (Project Service Automation 2.x)</span></span>

[!include [banner](../../includes/psa-now-project-operations.md)]

## <a name="type-field"></a><span data-ttu-id="0a83d-104">Tür alanı</span><span class="sxs-lookup"><span data-stu-id="0a83d-104">Type field</span></span> 

<span data-ttu-id="0a83d-105">Dynamics 365 Project Service Automation, bu varlıkların **iş-tabanlı** sürümlerini **öğe-tabanlı** ve **servis-tabanlı** sürümlerden ayırmak için Fırsat, Teklif, Sipariş ve Fatura varlıklarının **Tür** (**msdyn\_ordertype**) alanını temel alır.</span><span class="sxs-lookup"><span data-stu-id="0a83d-105">Dynamics 365 Project Service Automation relies on the **Type** (**msdyn\_ordertype**) field of the Opportunity, Quote, Order, and Invoice entities to distinguish **work-based** versions of these entities from **item-based** and **service-based** versions.</span></span> <span data-ttu-id="0a83d-106">Bu varlıkların iş tabanlı sürümleri PSA tarafından yönetilir.</span><span class="sxs-lookup"><span data-stu-id="0a83d-106">Work-based versions of these entities are handled by PSA.</span></span> <span data-ttu-id="0a83d-107">Çözümün istemci tarafı ve sunucu tarafındaki bir çok iş mantığı **Tür** alanına bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="0a83d-107">Lots of business logic on the client side and server side of the solution depends on the **Type** field.</span></span> <span data-ttu-id="0a83d-108">Bu nedenle, varlıklar oluşturulduğunda alanın doğru bir değerle başlatılması önemlidir.</span><span class="sxs-lookup"><span data-stu-id="0a83d-108">Therefore, it's important that the field be initialized with a correct value when the entities are created.</span></span> <span data-ttu-id="0a83d-109">Yanlış bir değer yanlış davranışlara neden olabilir ve bazı iş mantığı düzgün çalışmayabilir.</span><span class="sxs-lookup"><span data-stu-id="0a83d-109">An incorrect value can cause incorrect behaviors, and some business logic might not run correctly.</span></span>

## <a name="automatic-form-switching"></a><span data-ttu-id="0a83d-110">Otomatik form geçişi</span><span class="sxs-lookup"><span data-stu-id="0a83d-110">Automatic form switching</span></span>

<span data-ttu-id="0a83d-111">Olası veri bozulmalarını ve satış varlığı kayıtlarının yanlış başlatılması ve düzenlemesinin neden olduğu beklenmedik davranışları önlemek için PSA artık hazır formlarda otomatik form değiştirme mantığı içermektedir.</span><span class="sxs-lookup"><span data-stu-id="0a83d-111">To avoid potential data corruption and unexpected behaviors that are caused by incorrect initialization and editing of the sales entity records, PSA now includes logic for automatic form switching in out-of-box forms.</span></span> <span data-ttu-id="0a83d-112">Bu mantık, kullanıcıları iş tabanlı sürümle veya başka bir Fırsat, Teklif, Sipariş veya Fatura varlığı türüyle çalışmaya yönelik doğru forma götürür.</span><span class="sxs-lookup"><span data-stu-id="0a83d-112">This logic takes users to the correct form for working with the work-based version or any other type of Opportunity, Quote, Order, or Invoice entity.</span></span> <span data-ttu-id="0a83d-113">Bir kullanıcı Fırsat, Teklif, Sipariş veya Fatura varlığının iş tabanlı sürümünü açtığında, form **Proje bilgilerine** geçiş yapar.</span><span class="sxs-lookup"><span data-stu-id="0a83d-113">When a user opens the work-based version of an Opportunity, Quote, Order, or Invoice entity, the form is switched to **Project Information**.</span></span>

<span data-ttu-id="0a83d-114">Otomatik form geçişi mantığı **formId** değeri ile **msdyn\_ordertype** alanı arasındaki eşlemeye dayanır.</span><span class="sxs-lookup"><span data-stu-id="0a83d-114">The automatic form switching logic relies on the mapping between the **formId** value and the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="0a83d-115">Tüm kullanıma hazır formlar bu eşlemeye eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="0a83d-115">All out-of-box forms have been added to that mapping.</span></span> <span data-ttu-id="0a83d-116">Ancak, varlığın hangi sürümünün işleneceğini belirtmek için özel formlar el ile eklenmelidir.</span><span class="sxs-lookup"><span data-stu-id="0a83d-116">However, custom forms must be manually added to indicate which version of the entity they are intended to handle.</span></span> <span data-ttu-id="0a83d-117">Bu, **msdyn\_ordertype** alanını temel alır.</span><span class="sxs-lookup"><span data-stu-id="0a83d-117">This is based on the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="0a83d-118">Eşlemede form geçişi eksikse mantık, varlığın **msdyn\_ordertype** alanına kaydedilen değere göre, kullanıma hazır forma geçiş yapar.</span><span class="sxs-lookup"><span data-stu-id="0a83d-118">If the form switching is missing from the mapping, logic will switch to the out-of-box form, based on the value that is saved in the **msdyn\_ordertype** field of the entity.</span></span>

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a><span data-ttu-id="0a83d-119">Özel formlar ekleme ve form geçişi mantığını açma</span><span class="sxs-lookup"><span data-stu-id="0a83d-119">Add custom forms and turn on the form switching logic</span></span>

<span data-ttu-id="0a83d-120">Aşağıdaki örnek, nasıl özel bir formun (**Proje Bilgilerim**) iş tabanlı fırsatlarla çalışacak şekilde nasıl ekleneceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="0a83d-120">The following example shows how to add a custom form, **My Project Information**, so that it works with work-based opportunities.</span></span> <span data-ttu-id="0a83d-121">Aynı süreç teklifler, siparişler ve faturalarla çalışacak şekilde özel formlar eklemek için de kullanılır.</span><span class="sxs-lookup"><span data-stu-id="0a83d-121">The same process is used to add custom forms so that they work with quotes, orders, and invoices.</span></span>

<span data-ttu-id="0a83d-122">**Proje Bilgileri** formunun özel sürümünü oluşturmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="0a83d-122">Follow these steps to create a custom version of the **Project Information** form.</span></span>

1. <span data-ttu-id="0a83d-123">Fırsat varlığında, **Proje bilgileri** formunu açın ve **Proje Bilgilerim** adı altında bir kopyasını kaydedin.</span><span class="sxs-lookup"><span data-stu-id="0a83d-123">In the Opportunity entity, open the **Project Information** form, and save a copy under the name **My Project Information**.</span></span>
2. <span data-ttu-id="0a83d-124">Yeni formu açın ve özelliklerinde, **Proje Bilgileri** formundaki form başlatma komut dosyalarının bulunduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="0a83d-124">Open the new form, and then, in the properties, make sure that the form initialization scripts from the **Project Information** form are present.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="0a83d-125">Komut dosyalarını kaldırmayın.</span><span class="sxs-lookup"><span data-stu-id="0a83d-125">Don't remove the scripts.</span></span> <span data-ttu-id="0a83d-126">Aksi takdirde, bazı veriler yanlış başlatılabilir.</span><span class="sxs-lookup"><span data-stu-id="0a83d-126">Otherwise, some data might be initialized incorrectly.</span></span>

3. <span data-ttu-id="0a83d-127">Formda **Tür** **(msdyn\_ordertype**) alanının bulunduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="0a83d-127">Verify that the **Type** (**msdyn\_ordertype**) field is present in the form.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="0a83d-128">Bu alanı kaldırmayın.</span><span class="sxs-lookup"><span data-stu-id="0a83d-128">Don't remove this field.</span></span> <span data-ttu-id="0a83d-129">Aksi takdirde, başlatma komut dosyaları başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="0a83d-129">Otherwise, the initialization scripts will fail.</span></span>

4. <span data-ttu-id="0a83d-130">Yeni formun **formId** değerini bulun.</span><span class="sxs-lookup"><span data-stu-id="0a83d-130">Find the **formId** value of the new form.</span></span> <span data-ttu-id="0a83d-131">Bu adımı iki farklı yolla tamamlayabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="0a83d-131">You can complete this step in two ways:</span></span>

    - <span data-ttu-id="0a83d-132">Bir yönetilmeyen çözümün parçası olarak **Proje Bilgilerim** formunu dışa aktarın ve ardından dışa aktarılan çözümün customization.xml dosyasında **formId** değerini arayın.</span><span class="sxs-lookup"><span data-stu-id="0a83d-132">Export the **My Project Information** form as part of an unmanaged solution, and then look up the **formId** value in the customization.xml file of the exported solution.</span></span>
    - <span data-ttu-id="0a83d-133">Form düzenleyicisinde **Proje Bilgilerim** formunu açın ve aşağıdaki örnekte gösterildiği gibi URL'deki **fromId** parametresinin yanındaki genel benzersiz tanımlayıcıyı (GUID) arayın.</span><span class="sxs-lookup"><span data-stu-id="0a83d-133">Open the **My Project Information** form in the form editor, and then look for the globally unique identifier (GUID) next to the **fromId** parameter in the URL, as shown in the following illustration.</span></span>

    ![URL'deki yeni formun formId değeri.](media/how-to-add-custom-forms-in-v2.0.png)

5. <span data-ttu-id="0a83d-135">msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js web kaynağını düzenleyerek **formId** değeri için bir **msdyn\_ordertype** eşlemesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0a83d-135">Create an **msdyn\_ordertype** mapping for the **formId** value by editing the msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js web resource.</span></span> <span data-ttu-id="0a83d-136">Kodu kaynaktan kaldırın ve aşağıdaki kodla değiştirin.</span><span class="sxs-lookup"><span data-stu-id="0a83d-136">Remove the code from the resource, and replace it with the following code.</span></span>

    ```javascript
    define(["require", "exports"], function (require, exports) {
        "use strict";
        var SalesDocumentCustomFormIds = (function () {
            function SalesDocumentCustomFormIds() {
            }
            SalesDocumentCustomFormIds.overwriteFormIds = function (mappedFormIds) {
                /*
                ---- Notes ----
                mappedFormIds[SalesEntity][OrderType] => The array of forms IDs that support particular entity and order type
                Add or overwrite customized formId for the particular entity and order type by calling:
                    mappedFormIds[<EntityType>][<msdyn_ordertype>].push("<formId>");
                Allowed msdyn_ordertype values for reference:
                    ServiceBased: 690970002 (Field Service version of the entity)
                    WorkBased: 192350001 (PSA version of the entity)
                    ItemBased: 192350000 (Regular out of the box entity)
                Uncomment and update one of the following lines to register custom PSA form for required entity:
                */      
                //mappedFormIds[1][192350001].push("<formId>"); //Quote
                //mappedFormIds[5][192350001].push("<formId>"); //Quote Line
                //mappedFormIds[2][192350001].push("<formId>"); //Sales Order
                //mappedFormIds[6][192350001].push("<formId>"); //Sales Order Line
                // In this example we have added new form for Opportunity
                mappedFormIds[0][192350001].push("192EE537-DCC4-45D3-B7AF-EA694B9113D2"); //Opportunity
                //mappedFormIds[4][192350001].push("<formId>"); //Opportunity Line
            };
            return SalesDocumentCustomFormIds;
        }());
        exports.default = SalesDocumentCustomFormIds;
    });
    ```

6. <span data-ttu-id="0a83d-137">Özelleştirmeleri kaydedin ve yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="0a83d-137">Save and then publish the customizations.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]