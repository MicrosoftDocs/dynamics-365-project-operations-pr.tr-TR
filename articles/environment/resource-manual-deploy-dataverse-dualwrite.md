---
title: Çift yazma desteği bulunan Project Operations Dataverse uygulamasını el ile dağıtma
description: Bu makalede, Project Operations Dataverse uygulamasının ikili yazma desteği olacak şekilde el ile nasıl dağıtılacağı açıklanmaktadır.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: be80ea3956fbf0264c2eeb7a5e30dd50b77e3c78
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912034"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a>Çift yazma desteği bulunan Project Operations Dataverse uygulamasını el ile dağıtma

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Bu makalede, Microsoft Dataverse'de Microsoft Dynamics 365 Project Operations'ın, ikili yazmayı destekleyecek şekilde nasıl el ile dağıtılacağı açıklanmaktadır. Project Operations ortamın yapılandırmasını algılar ve önkoşulların karşılanması durumunda çift yazma için ek destek sağlar.

Microsoft Dynamics Lifecycle Services (LCS) üzerinden dağıtım sırasında bu makaledeki adımları izlediyseniz Microsoft Power Platform entegrasyonu dağıtımını atlayabilirsiniz (daha önce Common Data Service ortamı olarak bilinirdi).

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
6. Dili doğrulayın ve ardından para biriminin Finans ve Operasyon uygulamalarınızın para birimiyle eşleştiğini doğrulayın.
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

Dataverse ortamı dağıtıldıktan sonra Finans ve Operasyon uygulamalarınızda bağlantıyı ayarlayabilirsiniz. [Ortamınızı bağlamak için çift yazma sihirbazını kullanma](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment) bölümündeki adımları izleyin.
