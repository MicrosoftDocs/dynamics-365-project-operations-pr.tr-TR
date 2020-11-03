---
title: Proje kaynaklarını ayarlama
description: Bu konu, proje kaynakları kurma veya istek gönderme hakkında bilgi sağlar.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7eec8ad5d78019219b2e04ca75eeaa5a3c8a748f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086496"
---
# <a name="set-up-project-resources"></a>Proje kaynaklarını ayarlama

[!include [banner](../includes/banner.md)]

Bir takvim ayarlamanız ve bunu bir çalışan veya iş gücü ile ilişkilendirmeniz gerekir. Takvim, projeyi ve proje için ayrılmış kaynakların çalışma süresini zamanlamak için kullanılır. Takvim ayarı sırasında, proje yöneticileri kaynak iyileştirmesinin parçası olarak kaynak dengelemesi yapabilir. Takvim zamanlamasına bağlı olarak, kaynaklara sınırlamalar konabilir. **Takvimler** sayfasında bir takvim ayarlayabilirsiniz.

Bir çalışanı proje kaynağı olarak ayarladığınızda, kaynak ayarladığınız şirkette çalışan çalışanlar arasından seçim yapabilirsiniz. Alternatif olarak, kuruluşunuzdaki diğer şirketlerden çalışanlar seçebilirsiniz. Bu çalışanlar şirketlerarası kaynaklar olarak bilinir.

Aşağıdaki yordamlarda, bir çalışanın şirketinizdeki bir proje kaynağı olarak nasıl ayarlanacağı ve bir şirketlerarası proje kaynağının nasıl ayarlanacağı açıklanmaktadır.

## <a name="set-up-a-worker-as-a-project-resource"></a>Çalışanı proje kaynağı olarak ayarlama

1. **Çalışanlar** sayfasında, **Çalışanlar** listesinde, proje kaynağı olarak eklemekte olduğunuz çalışanı seçin ve çalışan kaydını açın.
2. Eylem bölmesinde **Proje** &gt; **Kurulum** &gt; **Proje kurulumu** 'nu seçin.
3. Bir takvim seçin ve sonra sayfayı kapatın.

Ön atama türü olarak bir kaynak için varsayılan projelerini de belirtebilirsiniz. Kaynak yöneticisi veya proje yöneticisi kaynağın önceden hangi projelerde çalışacağını bildiği ön atamalar özelliği kullanılabilir. Ön atamalar, proje sponsoru ya da müşteri talebine dayanabilir. Bir projeyi önceden atamak için **Proje ata** sayfasında **Projeler** sekmesinde, **Kalan projeler** listesinden uygun projeyi seçin.

## <a name="set-up-an-intercompany-resource"></a>Şirketlerarası kaynak ayarlama

Bir çalışanı şirketlerarası kaynak olarak ayarladığınızda, ayarı hem ödünç veren şirkette, hem de ödünç alan şirkette tamamlamanız gerekir.

### <a name="in-the-lending-company"></a>Ödünç veren şirkette

1. Finance'de, ödünç veren şirketinin seçili olduğunu doğrulayın ve ardından önceki "Çalışanı proje kaynağı olarak ayarlama" bölümündeki yordamı tamamlayın.
2. **Şirketlerarası muhasebe** sayfasında, **Yeni** 'yi seçin.
3. **Tüzel kişilik kodu** alanında, ödünç veren şirketi seçin. Alanları uygun şekilde doldurun ve ardından **Kaydet** 'i seçin.
4. **Transfer fiyatları** sayfasında, **Yeni** 'yi seçin.
5. **Ödünç alan tüzel kişilik** alanında, uygun şirketi seçin.
6. Ödünç alan şirkete yalnızca bu bölümün başlangıcında oluşturduğunuz kaynağı vermek için, **Kaynak** alanında, oluşturduğunuz kaynağın adını seçin. Ödünç veren şirketteki tüm kaynakların ödünç alan şirket tarafından kullanılabilir olmasını sağlamak için **Kaynak** alanını boş bırakın.
7. **Proje yönetimi ve muhasebe parametreleri** sayfasında, **Şirketlerarası** sekmesinde, **Şirketlerarası kaynak planlama ve zaman çizelgelerini etkinleştir** seçeneğini **Evet** olarak ayarlayın.

### <a name="in-the-borrowing-company"></a>Ödünç alan şirkette

- **Kaynaklar listesi** sayfasındaki arama filtresi alanında, ödünç veren şirket için oluşturduğunuz kaynağın adını girin ve adın ödünç alan şirketin kaynak listesine eklendiğini doğrulayın.

## <a name="request-project-resources"></a>Proje kaynaklarına yönelik istekler
Proje kaynak zamanlamasının işlevselliği yalnızca kaynak yöneticilerinin görevlendirmelere veya projelere yönelik personelli kaynakları dağıtmalarını sağlar. Bu işlevi etkinleştirmek için aşağıdaki görevleri gerçekleştirin veya bunların tamamlandığından emin olun:

- Numara serilerini ayarlayın.
- Proje yönetimi ve muhasebe iş akışlarını ayarlayın.
- Kaynak isteği iş akışlarını etkinleştirin.

Önceki görevler tamamlandıktan sonra, gereksinim duydukça aşağıdaki görevleri gerçekleştirebilirsiniz:

- Geçici ayrılmış personelli bir kaynaktan kaynak isteği oluşturun.
- Kaynak isteklerini izleyin.
- Kaynak isteklerini karşılayın.
- Bir İKY'den bir personelli kaynak isteyin.
- Personelli kaynak için istekte bulunmadan bir projeye kaynak ayırın.
