---
title: Proje faturası tümleştirmesi
description: Bu konu müşteri faturalaması için Project Operations iki yazma tümleştirmesiyle ilgili bilgi sağlar.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 37549080d76e3bffd7cb002aee8e3c46b9eeb18e3cec915cd971881b69747534
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993265"
---
# <a name="project-invoice-integration"></a>Proje faturası tümleştirmesi

Bu konu müşteri faturalaması için Project Operations iki yazma tümleştirmesiyle ilgili bilgi sağlar.

Proje yöneticileri Project Operations'ta proje faturalama biriktirme listesini yönetir ve Microsoft Dataverse uygulamasında müşteri için proforma fatura oluşturur . Bu proforma faturasına dayalı olarak, borç hesapları ve proje muhasebecisi müşteri tarafından müşteriye açık bir fatura oluşturur. Çift yazma tümleştirmesi, proforma fatura ayrıntılarının Finance and Operations uygulamalarıyla eşitlenmesini sağlar. Müşteriye açık olan fatura deftere nakledildikten sonra, Sistem Dataverse uygulamasındaki ilgili proje fiili değerlerini Hesap ayrıntısıyla güncelleştirir. Aşağıdaki grafik, bu tümleştirmeye üst düzey kavramsal genel bakış sağlar.

   ![Proje faturası tümleştirmesi.](./media/DW5Invoicing.png)

Proje Yöneticisi Dataverse'te Proforma faturayı teyit ettikten sonra, proforma fatura başlığı bilgileri Çift yazma tablo eşlemesi, **Proje Fatura teklifi v2 (faturalar)** kullanılarak Finance and Operations uygulamalarına eşitlenir. Bu, Dataverse'ten Finance and Operations uygulamalarına yönelik tek yönlü bir tümleştirmedir. Proje faturası tekliflerini doğrudan Finance and Operations uygulamalarında oluşturma veya silme desteklenmez.

Dataverse Uygulamasında fatura teyidi Ayrıca **gerçek değerler** varlığında faturalama ile ilgili kayıtlar oluşturmak için iş mantığını tetikler. Bu kayıtlar ikili yazma tablo eşlemesi, **Project Operations tümleştirmesi (msdyn\_ fiili değerleri)** kullanımı ile Finance and Operations'a eşitlenir. Daha fazla bilgi için bkz. [Proje tahminleri ve gerçek değerler](resource-dual-write-estimates-actuals.md). 

Proje Fatura teklif satırları, dönemsel işlem, **Form hazırlamayı içe aktar** tarafından oluşturulur. Bu işlem, **gerçek değerler hazırlama** tablosundaki Faturalanan satış fiili değerleri ayrıntılarını temel alır. Daha fazla bilgi için bkz. [Proje Fatura tekliflerini yönetme](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
