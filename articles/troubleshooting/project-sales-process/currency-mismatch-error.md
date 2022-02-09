---
title: Para birimi uyuşmazlığı hatası
description: Bu konu, belirli kayıt türlerini kaydettiğinizde oluşan para birimi uyuşmazlığı hatası hakkında sorun giderme bilgileri sağlar.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 52e33ad3728e1a393e8c7e3ca4e0a4b506d0b774
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903569"
---
# <a name="currency-mismatch-error"></a>Para birimi uyuşmazlığı hatası 

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Bir projeyi, sözleşmeyi, teklifi veya rezerve edilebilir kaynağı kaydettiğinizde, **Sahibi olunan şirket para birimi, sözleşme birimi para birimiyle eşleşmiyor hatasını alabilirsiniz. Devam etmek için farklı bir sahip şirket veya sözleşme birimi seçin**. Bunun nedeni, kayıt için sözleşme birimi para birimi ile sahip olan şirket para birimi arasında bir para birimi uyuşmazlığı olmasıdır.


## <a name="resolution"></a>Çözünürlük

Bu sorunu çözmek için aşağıdakileri yapın:
- Bu kayıt için sözleşme biriminin para birimini doğrulayın. Para birimini, kuruluş birimi kaydını açarak ve **Para Birimi** alanındaki **Genel** sekmesindeki değeri doğrulayarak görebilirsiniz.
- Sahip olan şirketin para birimini doğrulayın. Şirket kaydındaki **İlgili** > **Defterler**'e giderek para birimini görebilirsiniz. Şirketle ilişkili genel muhasebe kaydını çift tıklayın ve **Muhasebe para birimi** alanındaki **Genel** sekmesindeki değeri doğrulayın.

Sözleşme biriminde ayarlanan para birimi ve genel muhasebe kaydı eşleşmezse kaydı kaydettiğinizde yapılandırmasını ayarlayın veya farklı değerler seçin. Sistem, doğru şirketlerarası fatura akışlarını sağlamak için bu kayıtların eşleşmesini gerektirir. Şirketlerarası yapılandırmalar hakkında daha fazla bilgi için bkz. [Şirketlerarası hareket oluşturma](../../project-accounting/create-intercompany-transactions.md).

Şirket kaydında ilişkili genel muhasebe kaydı yoksa bu, ortamı ayarlarken eksik bir yapılandırma olduğunu gösterir. Yapılandırmanın sistem yöneticisi tarafından düzeltilmesi gerekir. Sistem yöneticisi **Çift yazma yapılandırmalarına** gitmeli ve bu eşlemenin ilk eşitlemesiyle **Defter çift yazma eşlemesini** durdurmalı ve yeniden başlatmalıdır ve bu ön koşuldur. Daha fazla bilgi için bkz. [Project Operations çift yazma eşlemesi sürümleri](../../environment/resource-dual-write-maps.md).