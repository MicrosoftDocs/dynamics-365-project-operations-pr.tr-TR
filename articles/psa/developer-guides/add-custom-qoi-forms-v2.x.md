---
title: Yeni özel varlık formları ekleme (Project Service Automation 2. x)
description: Bu konu, Dynamics 365 Project Service Automation 2. x içindeki fırsatlar, teklifler, siparişler veya faturalar için özel varlık formlarının nasıl ekleneceği hakkında bilgi sağlar.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: ffc702bbe9cedb2a0cc8da8d8f58e48005950127
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584344"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a>Yeni özel varlık formları ekleme (Project Service Automation 2. x)

[!include [banner](../../includes/psa-now-project-operations.md)]

## <a name="type-field"></a>Tür alanı 

Dynamics 365 Project Service Automation, bu varlıkların **iş-tabanlı** sürümlerini **öğe-tabanlı** ve **servis-tabanlı** sürümlerden ayırmak için Fırsat, Teklif, Sipariş ve Fatura varlıklarının **Tür** (**msdyn\_ordertype**) alanını temel alır. Bu varlıkların iş tabanlı sürümleri PSA tarafından yönetilir. Çözümün istemci tarafı ve sunucu tarafındaki bir çok iş mantığı **Tür** alanına bağlıdır. Bu nedenle, varlıklar oluşturulduğunda alanın doğru bir değerle başlatılması önemlidir. Yanlış bir değer yanlış davranışlara neden olabilir ve bazı iş mantığı düzgün çalışmayabilir.

## <a name="automatic-form-switching"></a>Otomatik form geçişi

Olası veri bozulmalarını ve satış varlığı kayıtlarının yanlış başlatılması ve düzenlemesinin neden olduğu beklenmedik davranışları önlemek için PSA artık hazır formlarda otomatik form değiştirme mantığı içermektedir. Bu mantık, kullanıcıları iş tabanlı sürümle veya başka bir Fırsat, Teklif, Sipariş veya Fatura varlığı türüyle çalışmaya yönelik doğru forma götürür. Bir kullanıcı Fırsat, Teklif, Sipariş veya Fatura varlığının iş tabanlı sürümünü açtığında, form **Proje bilgilerine** geçiş yapar.

Otomatik form geçişi mantığı **formId** değeri ile **msdyn\_ordertype** alanı arasındaki eşlemeye dayanır. Tüm kullanıma hazır formlar bu eşlemeye eklenmiştir. Ancak, varlığın hangi sürümünün işleneceğini belirtmek için özel formlar el ile eklenmelidir. Bu, **msdyn\_ordertype** alanını temel alır. Eşlemede form geçişi eksikse mantık, varlığın **msdyn\_ordertype** alanına kaydedilen değere göre, kullanıma hazır forma geçiş yapar.

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a>Özel formlar ekleme ve form geçişi mantığını açma

Aşağıdaki örnek, nasıl özel bir formun (**Proje Bilgilerim**) iş tabanlı fırsatlarla çalışacak şekilde nasıl ekleneceğini gösterir. Aynı süreç teklifler, siparişler ve faturalarla çalışacak şekilde özel formlar eklemek için de kullanılır.

**Proje Bilgileri** formunun özel sürümünü oluşturmak için bu adımları izleyin.

1. Fırsat varlığında, **Proje bilgileri** formunu açın ve **Proje Bilgilerim** adı altında bir kopyasını kaydedin.
2. Yeni formu açın ve özelliklerinde, **Proje Bilgileri** formundaki form başlatma komut dosyalarının bulunduğundan emin olun. 

    > [!IMPORTANT]
    > Komut dosyalarını kaldırmayın. Aksi takdirde, bazı veriler yanlış başlatılabilir.

3. Formda **Tür** **(msdyn\_ordertype**) alanının bulunduğunu doğrulayın. 

    > [!IMPORTANT]
    > Bu alanı kaldırmayın. Aksi takdirde, başlatma komut dosyaları başarısız olur.

4. Yeni formun **formId** değerini bulun. Bu adımı iki farklı yolla tamamlayabilirsiniz:

    - Bir yönetilmeyen çözümün parçası olarak **Proje Bilgilerim** formunu dışa aktarın ve ardından dışa aktarılan çözümün customization.xml dosyasında **formId** değerini arayın.
    - Form düzenleyicisinde **Proje Bilgilerim** formunu açın ve aşağıdaki örnekte gösterildiği gibi URL'deki **fromId** parametresinin yanındaki genel benzersiz tanımlayıcıyı (GUID) arayın.

    ![URL'deki yeni formun formId değeri.](media/how-to-add-custom-forms-in-v2.0.png)

5. msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js web kaynağını düzenleyerek **formId** değeri için bir **msdyn\_ordertype** eşlemesi oluşturun. Kodu kaynaktan kaldırın ve aşağıdaki kodla değiştirin.

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

6. Özelleştirmeleri kaydedin ve yayımlayın.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
