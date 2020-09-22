---
title: Varlık, denetim ve kullanıcı arabirimi değişiklikleri (Project Service Automation 3. x)
description: Bu konu Microsoft Dynamics Project Service Automation 3. x'e yönelik çözüm değişiklikleri açıklamaktadır.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/15/2019
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 9f8828c6-541c-4945-8c99-5785118e191d
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
ms.openlocfilehash: 56aa0bb8272b886bcd15dadd0f74fff3bc43e26b
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756665"
---
# <a name="entity-control-and-user-interface-changes-project-service-automation-3x"></a>Varlık, denetim ve kullanıcı arabirimi değişiklikleri (Project Service Automation 3. x)
Microsoft Dynamics Project Service Automation (PSA) 3.x'in sürümüyle varlıklarda, denetimlerde, görünümlerde ve kullanıcı arabiriminde pek çok değişiklik yapıldı. Bu konuda, bu önemli değişiklikler hakkında önemli bilgiler sağlanmaktadır:

## <a name="parent-child-relationships-for-sales-document-sales-document-line-sales-document-line-detail-entities"></a>Satış belgesi, satış belgesi satırı, satış belgesi satırı ayrıntı varlıkları için üst-alt öğe ilişkileri
3.0 sürümünden önceki Dynamics 365 Project Service Automation (PSA) sürümlerinde satış belgeleri, satış belgesi satırları ve satış belgesi satır ayrıntısı varlıkları arasındaki bazı ilişkiler ilgili varlığın GUID'inin dize gösterimini tutan bize alanları aracılığıyla uygulanıyordu. Bunun nedeni, bu ilişkilerin tipik Dynamics CRM varlık ilişkilerine benzer şekilde çalışmasını ve dize alanlarının arama alanları gibi davranmasını sağlamak için çözümün sunucu ve istemci tarafında belirgin bir özel kod gerektiren platform kısıtlamalarıydı.

PSA 3.0 satış belgesi ve satış belgesi satırı varlıkları arasında yeni varlık ilişkilerinden yararlanacak şekilde güncelleştirilmiştir.

Arama alanları artık varlıklara olan başvuruları belirtmek için kullanılabildiğinden, önceki sürümlerdeki ilgili varlığın GUID değerini tutan alanlara artık gerek duyulmuyor ve bu nedenle bu alanlar kullanım dışı bırakıldı. Eski dize alanları tarafından tanımlanan ilişkileri işleyen özel istemci ve sunucu tarafı kodları da kullanımdan kaldırıldı.

### <a name="entity-schema-changes"></a>Varlık şeması değişiklikleri
Aşağıdaki tabloda, kullanım dışı bırakılan dize alanlarının bire bir listesi ve varlıklar için yeni arama alanları sağlanmaktadır. 

 Varlık |   Kullanım dışı bırakılan alan (Dize) | Yeni alan (Arama)
--- | --- | ---
invoicedetail (Fatura Satırı) |  msdyn_contractline |    msdyn_contractlineid
msdyn_actual (Fiili değer) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_contractlineinvoiceschedule (Proje Sözleşme Satırı Fatura Zamanlaması) |    msdyn_contractline |    msdyn_contractlineid
msdyn_contractlinescheduleofvalue (Proje Sözleşme Satırı Kilometre Taşı) |   msdyn_contractline |    msdyn_contractlineid
msdyn_fact (Olgu) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_invoicelinetransaction (Fatura Satırı Ayrıntısı) | msdyn_invoiceline <br> msdyn_salescontractline | msdyn_invoicelineid <br> msdyn_salescontractlineid
msdyn_journalline (Tevmiye Defteri Satırı) |  msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlineresourcecategory (Proje Sözleşmesi Satırı Kaynak Kategorisi) | msdyn_salescontractline |   msdyn_contractlineid
msdyn_orderlinetransaction (Proje Sözleşme Satırı Ayrıntısı) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlinetransactioncategory (Proje Sözleşme Satırı İşlem Kategorisi) |   msdyn_contractline |    msdyn_contractlineid
msdyn_orderlinetransactionclassification (Proje Sözleşme Satırı İşlem Sınıflandırması) |   msdyn_contractline |    msdyn_contractlineid
msdyn_quotelineinvoiceschedule (Teklif Satırı Fatura Zamanlaması) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelineresourcecategory (Teklif Satırı Kaynak Kategorisi) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinescheduleofvalue (Teklif Satırı Kilometre Taşı) | msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransaction (Teklif Satırı Ayrıntısı) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactioncategory (Teklif Satırı İşlem Kategorisi) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactionclassification (Teklif Satırı İşlem Sınıflandırması) |  msdyn_quoteline |   msdyn_quotelineid
SalesOrderDetail (Sipariş Satırı) | msdyn_quotelineid | msdyn_quoteline 

### <a name="deprecated-custom-views-and-controls"></a>Kullanım dışı özel görünümler ve denetimler
Aşağıdaki özel görünümler ve denetimler ve bunların ilgili mimarileri kullanım dışı bırakılmıştır.

- Borçlandırılabilirlik görünümü.
- Teklif satırı için **Proje bilgileri** sayfasında teklif satırı ayrıntılarını göstermeye yönelik özel kılavuz denetimleri.
- Satış siparişi satırı için **Proje bilgileri** sayfasında proje sözlşeme satırı ayrıntılarını göstermeye yönelik özel kılavuz denetimleri.

> [!NOTE]
> Kullanımdan kaldırılmış kaynakların tam listesi için [Project Service Automation v3.x'te kullanımdan kaldırılan web kaynakları](../developer-guides/web-resources-deprecated-v3.x.md).

## <a name="unified-client-interface-app-module"></a>Birleşik İstemci Arabirimi Uygulama Modülü
Birleşik İstemci Arabirimi (UCI) Uygulama Modüllerinin kullanıma sunulmasıyla, PSA site haritası girişleri sistemden kaldırılmıştır.  
UCI Uygulama Modülü yalnızca formların PSA sürümlerini içerdiğinden Fırsat, Teklif, Sipariş, Fatura için form geçişi ile ilgili işlevler artık gerekli olmadığı için kullanım dışı bırakılmıştır.  

Aşağıdaki web kaynakları kullanım dışı bırakıldı:

- msdyn_\SalesDocument\SalesDocumentFormLoader.js
- msdyn_\SalesDocument\PSSalesDocumentCustomFormIds.js

> [!NOTE]
> Kullanım dışı bırakılan kaynakların tam listesi için bkz. [Project Service Automation v3.x'te kullanımdan kaldırılan web kaynakları](../developer-guides/web-resources-deprecated-v3.x.md).


