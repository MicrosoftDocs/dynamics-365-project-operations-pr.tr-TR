---
title: Proje zamanlaması günlükleri
description: Bu konu, Proje Zamanlama Hizmeti ve Proje Zamanlaması API'larıyla ilgili hataları izlemek için Proje Zamanlaması günlüklerini kullanmanıza yardımcı olacak bilgiler ve örnekler sağlar.
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 1a58a588d3e2fb92f1b4a4ed0f6f69d0a63908db
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589542"
---
# <a name="project-scheduling-logs"></a>Proje zamanlaması günlükleri

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayan öğeleri temel alan senaryolar için Project Operations, Lite dağıtımı: anlaşmadan proforma faturaya_, _Project for the Web_

Microsoft Dynamics 365 Project Operations, birincil zamanlama altyapısı olarak [Project for the Web](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) kullanır. Project Operations kaynak atamalarını, görev bağımlılıklarını, proje demetlerini ve proje takımı üyelerini oluşturmak, güncelleştirmek ve silmek için standart Microsoft Dataverse Web uygulaması programlama arabirimlerini (API) kullanmak yerine yeni Proje Zamanlaması API'larını kullanır. Bununla birlikte oluşturma, güncelleştirme veya silme işlemleri iş kırılım yapısı (WBS) varlıklarında program aracılığıyla çalıştığında hatalar oluşabilir. Bu hataları ve işlemlerin geçmişini izlemek için iki yeni yönetim günlüğü uygulanmıştır: **İşlem Kümesi** ve **Proje Zamanlaması Hizmeti (PSS)**. Bu günlüklere erişmek için **Ayarlar**\> **Zamanlama tümleştirmesi**'ne gidin.

Aşağıdaki resimde Proje Zamanlaması günlükleri için veri modeli gösterilmektedir.

![Proje Zamanlaması günlükleri için veri modeli.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>İşlem Kümesi günlüğü

İşlem Kümesi günlüğü projeler, proje görevleri, kaynak atamaları, görev bağımlılıkları, proje demetleri veya proje takım üyelerinde bir toplu işteki bir veya birden çok oluşturma, güncelleştirme veya silme işlemini çalıştırmak için kullanılan bir işlem kümesi yürütmesini izler. **Durumdaki İşlem** alanı işlem kümesinin genel durumunu gösterir. İşlem kümesi yükü ayrıntıları, ilgili İşlem Kümesi Ayrıntı kayıtlarında yakalanır.

### <a name="operation-set"></a>İşlem Kümesi

Aşağıdaki tabloda **İşlem Kümesi** varlığıyla ilgili alanlar gösterilmektedir.

| SchemaName            | Description                                                                                                  | DisplayName            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | İşlem kümesinin tamamlandığı veya başarısız olduğu tarih/saat.                                                | CompletedOn            |
| msdyn_correlationid   | İsteğin **correlationId** değeri.                                                                  | CorrelationId          |
| msdyn_description     | İşlem kümesinin açıklaması.                                                                        | Description            |
| msdyn_executedon      | Kaydın çalıştırıldığı tarih/saat.                                                                       | Yürütülme Zamanı            |
| msdyn_operationsetId  | Varlık kurulumlarının benzersiz tanımlayıcısı.                                                                   | OperationSet           |
| msdyn_Project         | İşlem kümesi ile ilgili proje.                                                            | Project                |
| msdyn_projectid       | İsteğin **projectId** değeri.                                                                      | ProjectId (Kullanım dışı) |
| msdyn_projectName     | Uygulanamaz.                                                                                              | Uygulanamaz         |
| msdyn_PSSErrorLog     | İşlem kümesiyle ilişkilendirilmiş Proje Zamanlama Hizmeti hata günlüğünün benzersiz tanımlayıcısı. | PSS Hata Günlüğü          |
| msdyn_PSSErrorLogName | Uygulanamaz.                                                                                              | Uygulanamaz         |
| msdyn_status          | İşlem kümesinin durumu.                                                                             | Status                 |
| msdyn_statusName      | Uygulanamaz.                                                                                              | Uygulanamaz         |
| msdyn_useraadid       | Bu isteğin ait olduğu kullanıcının Azure Active Directory (Azure AD) nesne kimliği.                     | UserAADID              |

### <a name="operation-set-detail"></a>İşlem Kümesi Ayrıntısı

Aşağıdaki tabloda **İşlem Kümesi Ayrıntısı** varlığıyla ilgili alanlar gösterilmektedir.

| SchemaName                 | Description                                                                                 | DisplayName           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | İstek için seri hale getirilmiş Dataverse alanları.                                            | CdsPayload            |
| msdyn_entityname           | İstek varlığının adı.                                                     | EntityName            |
| msdyn_httpverb             | İstek yöntemi.                                                                         | HTTP Fiili (Kullanım dışı) |
| msdyn_httpverbName         | Uygulanamaz.                                                                             | Uygulanamaz        |
| msdyn_operationset         | Kaydın ait olduğu işlem kümesinin benzersiz tanımlayıcısı.                      | OperationSet          |
| msdyn_operationsetdetailId | Varlık kurulumlarının benzersiz tanımlayıcısı.                                                  | OperationSet Ayrıntısı   |
| msdyn_operationsetName     | Uygulanamaz.                                                                             | Uygulanamaz        |
| msdyn_operationtype        | İşlem kümesi ayrıntısı için işlem türü.                                             | OperationType         |
| msdyn_operationtypeName    | Uygulanamaz.                                                                             | Uygulanamaz        |
| msdyn_psspayload           | İstek için serileştirilmiş Proje Zamanlama Hizmeti alanları.                           | PssPayload            |
| msdyn_recordid             | İstek kaydının tanımlayıcısı.                                                       | Kayıt Kimliği             |
| msdyn_requestnumber        | İsteklerin alındığı sırayı tanımlayana otomatik oluşturulmuş numara. | İstek Numarası        |

## <a name="project-scheduling-service-error-logs"></a>Proje Zamanlama Hizmeti hata günlükleri

Project Zamanlama Hizmeti hata günlükleri, Proje Zamanlama Hizmeti **Kaydet** veya **Aç** işlemi gerçekleştirmeye çalıştığında oluşan yakalama hatalarını kaydeder. Bu günlüklerin oluşturulduğu üç desteklenen senaryo vardır:

- Kullanıcı tarafından başlatılan eylemler kritik şekilde başarısız olur (örneğin, eksik ayrıcalıklar nedeniyle atama oluşturulamaz).
- Proje Zamanlama Hizmeti bir varlıkta oluşturamaz, güncelleştiremez veya bir varlıkta herhangi bir basamaklandırma işlemi gerçekleştiremez.
- Bir kayıt açılamadığında (örneğin, bir proje açıldığında veya bir takım üyesinin bilgileri güncelleştirildiğinde) oluşan kullanıcı deneyimi hataları.

### <a name="project-scheduling-service-log"></a>Proje Zamanlama Hizmeti günlüğü

Aşağıdaki tabloda Proje Zamanlama Hizmeti günlüğüne dahil olan alanlar gösterilmektedir.

| SchemaName          | Description                                                                    | DisplayName    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | Özel durumun çağrı yığını.                                               | Çağrı Yığını     |
| msdyn_correlationid | Hatanın bağıntı kimliği.                                               | CorrelationId  |
| msdyn_errorcode     | Dataverse hata kodunu veya HTTP hata kodunu depolamak için kullanılan bir alan. | Hata Kodu     |
| msdyn_HelpLink      | Genel Yardım belgesi bağlantısı.                                       | Yardım Bağlantısı      |
| msdyn_log           | Proje Zamanlama Hizmetinden alınan günlük.                                   | Günlük            |
| msdyn_project       | Hata günlüğüyle ilişkili proje.                             | Project        |
| msdyn_projectName   | İşlem kümesinin yükü kalıcı olacaksa projenin adı. | Uygulanamaz |
| msdyn_psserrorlogId | Varlık kurulumlarının benzersiz tanımlayıcısı.                                     | PSS Hata Günlüğü  |
| msdyn_SessionId     | Proje oturum kimliği.                                                        | Oturum Kimliği     |

## <a name="error-log-cleanup"></a>Hata günlüğü temizleme

Varsayılan olarak Proje Zamanlama Hizmeti hata günlükleri ve İşlem Kümesi günlüğü her 90 günde bir temizlenebilir. 90 günden eski tüm kayıtlar silinir. Bununla birlikte, **Proje Parametreleri** sayfasında **msdyn_StateOperationSetAge** alanının değerini değiştirerek yöneticiler temizleme aralığını 1 ile 120 gün arasında olacak şekilde ayarlayabilirler. Bu değeri değiştirmek için çeşitli yöntemler kullanılabilir:

- Özel bir sayfa oluşturup **Eski İşlem Kümesi Süresi** alanı ekleyerek **Proje Parametresi** varlığını özelleştirin.
- [WebApi yazılım geliştirme kiti (SDK)](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord) kullanan istemci kodunu kullanın.
- Modeli temelli uygulamalarda Xrm SDK **updateRecord** yöntemini (istemci API Başvurusu) kullanan Hizmet SDK kodunu kullanın. Power Apps, **updateRecord** yöntemi için bir açıklama ve desteklenen parametreler içerir.

    ```C#
    Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter').then(function (response) {
        parameter = response.entities[0];
        var staleOperationValue = prompt("All records older than (x) days will be deleted, please enter X between 1 to 90 days", 1)
        var newData = {};
        newData.msdyn_projectparameterid = parameter.msdyn_projectparameterid;
        newData.msdyn_staleoperationsetage = parseInt(staleOperationValue);
        Xrm.WebApi.updateRecord("msdyn_projectparameter", parameter.msdyn_projectparameterid, newData).then(
            function success(result) {
                console.log("Project Parameter: Stale Operation Expiry is set to: " + newData.msdyn_staleoperationsetage);
                // perform operations on record update
                Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter')
                .then(function (response2) { console.log("Confirmed Project Parameter: Stale Operation Expiry is set to: " + response2.entities[0].msdyn_staleoperationsetage) });
            },
            function (error) {
                console.log("Failed to Update Project Ednpoint with error: " + error.message);
            // handle error conditions
            }
        );
    });
    ```
