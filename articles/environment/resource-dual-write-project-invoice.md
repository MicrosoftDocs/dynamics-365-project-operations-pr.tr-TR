---
title: Proje faturası tümleştirmesi
description: Bu konu müşteri faturalaması için Project Operations iki yazma tümleştirmesiyle ilgili bilgi sağlar.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1e7294360f041b030efca225c6754fe3bbc0eadf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581262"
---
# <a name="project-invoice-integration"></a>Proje faturası tümleştirmesi

Bu konu müşteri faturalaması için Project Operations iki yazma tümleştirmesiyle ilgili bilgi sağlar.

Proje yöneticileri Project Operations'ta proje faturalama biriktirme listesini yönetir ve Microsoft Dataverse uygulamasında müşteri için proforma fatura oluşturur . Bu proforma faturasına dayalı olarak, borç hesapları ve proje muhasebecisi müşteri tarafından müşteriye açık bir fatura oluşturur. Çift yazma tümleştirmesi, proforma fatura ayrıntılarının Finans ve Operasyon uygulamalarıyla eşitlenmesini sağlar. Müşteriye açık olan fatura deftere nakledildikten sonra, Sistem Dataverse uygulamasındaki ilgili proje fiili değerlerini Hesap ayrıntısıyla güncelleştirir. Aşağıdaki grafik, bu tümleştirmeye üst düzey kavramsal genel bakış sağlar.

   ![Proje faturası tümleştirmesi.](./media/DW5Invoicing.png)

Proje yöneticisi Dataverse'de proforma faturayı onayladıktan sonra proforma fatura üst bilgileri, **Proje faturası teklifi V2 (faturalar)** çift yazma tablo eşlemesi kullanılarak Finans ve Operasyon uygulamalarıyla eşitlenir. Bu, Dataverse'den Finans ve Operasyon uygulamalarına tek yönlü bir tümleştirmedir. Finans ve Operasyon uygulamalarında doğrudan Proje faturası tekliflerinin oluşturulması veya silinmesi desteklenmez.

Dataverse Uygulamasında fatura teyidi Ayrıca **gerçek değerler** varlığında faturalama ile ilgili kayıtlar oluşturmak için iş mantığını tetikler. Bu kayıtlar, **Project Operations tümleştirmesi gerçek değerleri (msdyn\_actuals)** çift yazma tablo eşlemesi kullanılarak Finance and Operations ile eşitlenir. Daha fazla bilgi için bkz. [Proje tahminleri ve gerçek değerler](resource-dual-write-estimates-actuals.md). 

Proje Fatura teklif satırları, dönemsel işlem, **Form hazırlamayı içe aktar** tarafından oluşturulur. Bu işlem, **gerçek değerler hazırlama** tablosundaki Faturalanan satış fiili değerleri ayrıntılarını temel alır. Daha fazla bilgi için bkz. [Proje Fatura tekliflerini yönetme](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
