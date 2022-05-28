---
title: Project Operations çift yazma tümleştirmesi
description: Bu konu, Project Operations iki yazma tümleştirilmesine yönelik bir genel bakış sağlar.
author: sigitac
ms.date: 04/28/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9b57b8bab9a6821e71a16b191804af21ae5d0b5a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582780"
---
# <a name="project-operations-dual-write-integration-overview"></a>Project Operations çift yazma tümleştirmesine genel bakış

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Project Operations, Microsoft Dataverse ve Dynamics 365 Finance arasında verileri eşitlemek için [çift yazma özelliklerini](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) kullanır.

Aşağıdaki şekil, verilerin Dataverse ve Finance arasındaki tümleştirmenin bir parçası olarak nasıl eşitleneceğini gösterir.

![Project Operations veri akışları genel bakış.](./media/ProjectOperationsFlows.jpg)

Dataverse'te Project Operations, Power Platform özelliklerini kullanarak modern bir kullanıcı arabirimi (UI) ve kolay kod/düşük kodlu genişletilebilirlik sağlar. Proje yöneticileri, kaynak yöneticileri, proje ekibi üyeleri ve diğer ön ofis paylaştıkça etkinliklerini Dataverse'te Project Operations'da gerçekleştirin.

Finance uygulamasındaki Project Operations, Proje muhasebesi ve gelir tanıma desteği sağlar. Project Operations, satış vergisi hesaplaması, para birimi döviz kurları, mali boyut raporlaması ve daha fazlası için finans bölümünde mali çerçeveye eklenir. Proje muhasebecisi genellikle finans unsura dayalıdır.

Project Operations tümleştirmesi aşağıdaki bileşen tümleştirmesiyle oluşur:


- [Project Operations kurulumu ve yapılandırma verileri tümleştirmesi](resource-dual-write-setup-integration.md) 
- [Proje tahminleri ve gerçek değerler](resource-dual-write-estimates-actuals.md)
- [Proje faturaları](resource-dual-write-project-invoice.md)
- [Gider yönetimi](resource-dual-write-expense.md)
- [Satıcı faturası](resource-dual-write-vendor-invoice.md)
