---
title: Çift yazma desteği bulunan Project Operations Dataverse uygulamasını el ile dağıtma
description: Bu konu, Project Operations Dataverse uygulamasının çift yazma desteği sağlamak için el ile nasıl dağıtılacağını açıklar.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2ad147da542fc9e7a2705da7a834d1a6512907e5
ms.sourcegitcommit: 205a94ab4168de25b102f31d00a691c8205ba63e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/18/2021
ms.locfileid: "6274032"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a>Çift yazma desteği bulunan Project Operations Dataverse uygulamasını el ile dağıtma

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Bu konu, Microsoft Dataverse'de Microsoft Dynamics 365 Project Operations uygulamasının çift yazma desteği sağlamak için el ile nasıl dağıtılacağını açıklar. Project Operations ortamın yapılandırmasını algılar ve önkoşulların karşılanması durumunda çift yazma için ek destek sağlar.

Microsoft Dynamics Lifecycle Services (LCS) üzerinden dağıtım sırasında, bu konudaki yönergeleri takip ettiyseniz, Microsoft Power Platform tümleştirmesi (önceden Common Data Service ortamı olarak biliniyordu) dağıtımını atlayabilirsiniz.

Çift yazmayı desteklemesi için Dataverse'te Project Operations dağıtma işleminin dört adımı vardır:

1. [Dataverse'de çift yazmayı destekleyen yeni bir ortam oluşturma](#create).
2. [Çift yazma önkoşullarını ortama ekleme](#prerequisites).
3. [Project Operations Dataverse uygulamasını ekleme](#dataverse).
4. [Ortamlarınıza bağlantı verme](#link).

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a>Dataverse'de çift yazmayı destekleyen yeni bir ortam oluşturma

Bu yordamı tamamlayabilmeniz için, Yönetici olarak oturum açmalısınız.

1. [Power Platform yönetim merkezini](https://admin.powerplatform.com) açın ve yönetici olarak oturum açın.
2. Yeni bir ortam oluşturun ve ortama ad verin.
3. Ortam türünü seçin. Deneme teklifine kaydolduysanız, **Deneme (abonelik tabanlı)** seçeneğini belirleyin.
4. Dağıtım bölgesini onaylayın.
5. **Bu ortam için veritabanı oluştur** seçeneğini etkinleştirin. 
6. Dili onaylayın ve ardından para biriminin Finance and Operations uygulamalarınızın para birimiyle eşleştiğini onaylayın.
7. **Dynamics 365 uygulamaları** seçeneğini etkinleştirin ve **Bu uygulamaları otomatik olarak dağıt** alanının **Hiçbiri** olarak ayarlandığını onaylayın.
8. Güvenlik grubu gerekiyorsa, bir güvenlik grubu ekleyin.
9. Ortam oluşturmak için **Kaydet**'i seçin.
10. Dağıtım tamamlanıncaya ve ortam **Hazır** durumuna ulaşıncaya kadar bekleyin.

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a>Çift yazma önkoşullarını ortama ekleme

Çift yazma desteği, **Şirket** varlığı gibi temel varlıklara eklenen ek alanlar içerir. Mevcut bir ortama çift yazma desteği ekliyorsanız, desteği etkinleştirmek için verileri güncelleştirmeniz gerekebilir. Verileri önyüklemek hakkında daha fazla bilgi için bkz. [Şirket verilerini önyükleme](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data). Çift yazma hakkında daha fazla bilgi için bkz. [Çift yazma sistem gereksinimleri](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).

Çift yazma önkoşullarını ortamınıza eklemek için bu yordamı izleyin.

1. Oluşturduğunuz ortamı açın ve ardından **Kaynak** \> **Dynamics 365 uygulamaları**'na gidin.
2. Uygulama listesinde **Çift yazma temel çözümü**'nü seçin ve kurun.
3. Yükleme tamamlanıncaya kadar bekleyin. Ardından uygulama listesinde **Çift yazma uygulama düzenlemesi çözümü**'nü seçin ve kurun.

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a>Project Operations Dataverse uygulamasını ekleme

Bu yordamı yalnızca, Project Operations yüklemeden önce önceki yordamları tamamladıysanız tamamlayabilirsiniz. Yükleme sırasında sistem, ortam yapılandırmasını analiz eder ve gerekirse çift yazma desteğini ekler.

1. Oluşturduğunuz ortamı açın ve ardından **Kaynak** \> **Dynamics 365 uygulamaları**'na gidin.
2. Uygulama listesinde **Microsoft Dynamics 365 Project Operations**'u seçin ve kurun.

## <a name="link-your-environments"></a><a name="link"></a>Ortamlarınıza bağlantı verme

Dataverse ortamı dağıtıldıktan sonra, Finance and Operations uygulamalarınızda bağlantıyı ayarlayabilirsiniz. [Ortamınızı bağlamak için çift yazma sihirbazını kullanma](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment) bölümündeki adımları izleyin.
