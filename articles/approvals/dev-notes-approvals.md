---
title: Onaylar için geliştirici notları
description: Bu konu, onaylarla çalışma hakkında ek geliştirici bilgileri sağlar.
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 9e4e910d0ff0a5f2603148fcc5daa0d423a4d174
ms.sourcegitcommit: a9dbcd3aff4c6ae495412e4980e105ae160fd1ec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/10/2020
ms.locfileid: "4483972"
---
# <a name="developer-notes-for-approvals"></a>Onaylar için geliştirici notları

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Dynamics 365 Project Operations, onay aşamalarında doğru kayıt geçişini güvence altına alan doğrulama mantığını içerir. Kayıt geçişlerini düzeltme: 

  - Tüm destekleyici satırlar, günlük ve gerçek değerler gibi ilgili tablolarda oluşturulur.
  - Onaylayan, devam etmeden önce projede bir **proje onaylayan** olarak işaretlendi.
