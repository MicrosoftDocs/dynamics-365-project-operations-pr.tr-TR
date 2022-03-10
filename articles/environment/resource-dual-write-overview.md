---
title: Project Operations çift yazma tümleştirmesi
description: Bu konu, Project Operations iki yazma tümleştirilmesine yönelik bir genel bakış sağlar.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: b65c40e8aaa9524c1c634738dadd23f21e86e2ec095c47bc849467c8806addbc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007935"
---
# <a name="project-operations-dual-write-integration-overview"></a>Project Operations çift yazma tümleştirmesine genel bakış

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Project Operations, Microsoft Dataverse ve Dynamics 365 Finance arasında verileri eşitlemek için [çift yazma yeteneklerini](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) kullanır.

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
