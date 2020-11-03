---
title: Gider girişi işleme
description: Bu konu, makbuzlar için optik karakter tanıma (OCR) işlemi hakkında bilgi sağlar. Bu özellik, Microsoft Dynamics 365 Finance üzerinde gider raporları oluştururken kullanıcı deneyimini geliştirmek için tasarlanmıştır.
author: stsporen
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 31c08ea264e6caec3217f4b424275495f39123e3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086482"
---
# <a name="expense-receipt-processing"></a>Gider girişi işleme

[!include [banner](../includes/banner.md)]

Gider girişi, girişler için optik karakter tanıma (OCR) işleminin eklenmesiyle geliştirilmiştir. Bu özellik, gider raporları oluştururken kullanıcı deneyimini geliştirmek için tasarlanmıştır.

## <a name="key-features"></a>Temel özellikler

- Makbuzlarda satıcı adını, tarihini ve toplam tutarı çıkarır.
- Özellik iliştirilmemiş makbuzlar ile içerisinde iliştirilmemiş dosya bulunmayan gider hareketlerini eşleştirmeyi dener.
- Kullanıcılar, Makbuzlardan el ile girilmiş gider hareketleri oluşturabilir.

## <a name="usage-examples"></a>Kullanım örnekleri

Bir gider raporu oluşturulduğunda kredi kartı hareketlerini içeren makbuzları otomatik olarak iliştirmek için aşağıdaki adımları izleyin:

  1. **Gider yönetimi** çalışma alanını açın.
  2. **Makbuzlar** sekmesinde, iliştirilmemiş makbuzların bulunduğunu doğrulayın. Makbuzları da **Makbuzlar** sekmesine yükleyebilirsiniz.
  3. **Giderler** sekmesinde, içerisinde iliştirilmemiş dosya bulunmayan giderlerin bulunduğunu doğrulayın. Genel olarak gider yöneticisi bu giderleri kredi kartı sağlayıcısından içe aktarır.
  4. **Yeni gider raporu** öğesini seçin. Gider raporu oluştururken, artık giderleri ve makbuzları da dahil edebildiğinizi unutmayın. Hem giderleri, hem de makbuzları eklerseniz, giderler için makbuzların otomatik eşleştirilmesine başlanır.

Bir gider oluşturmak veya bir makbuzdan bir gider ile eşleştirmek için aşağıdaki adımları izleyin:

  1. Gider raporunda, **Makbuzlar** sekmesinde, **Makbuzları ekle** 'yi seçerek bir makbuz iliştirin.
  2. Makbuzun karşıya yüklenen görüntüsünün altında, **Oluştur** ve **Eşleştir** seçeneklerine dikkat edin.

      - El ile girilen bir masraf hareketini oluşturmak için **Oluştur** öğesini seçin ve makbuzdan çıkarılan değerleri doldurun.
      - **Eşleştir** seçeneğini belirlediğinizde, sistem var olan bir gideri makbuz eşleştirmeye çalışır.

## <a name="installation"></a>Yükleme

Bu özellik, masraf deneyimini basitleştirmeye yardımcı olmak için **Gider raporları yeniden düzenleme** özelliğiyle birlikte çalışır. Bu özellik yalnızca, korumalı alan ve üretim olan katman 2 + ortamlarda kullanılabilir.

Bu gelişmiş gider özelliklerini kullanmak için, Microsoft Dynamics 365 Finance için Gider Yönetimi Hizmeti eklentisini yükledikten sonra, örneğinizde özellikleri açın. Microsoft Dynamics Lifecycle Services (LCS) içindeki projenizden eklentiye erişebilirsiniz.

1. LCS'de oturum açın ve istenen ortamı açın.
2. **Tüm ayrıntılar** 'a gidin.
3. **Koruma** 'yı seçin veya **Ortam eklentileri** hızlı sekmesine kaydırın.
4. **Yeni eklenti ekle** 'yi seçin.
5. **Gider Yönetim Hizmeti** 'ni seçin.
6. Yükleme kılavuzunu izleyin, koşulları ve hükümleri kabul edin.
7. **Yükle** 'yi seçin.

**Özellik Yönetimi** çalışma alanında, aşağıdaki özellikleri açın:

- Gider raporlarını yeniden tasarlama
- Otomatik eşleştirme ve makbuzdan gider oluşturma

Bu özellikleri açtığınızda aşağıdaki eylemler gerçekleşir:

- Var olan **Gider yönetimi** çalışma alanı yeni çalışma alanıyla değiştirilir.
- Gider alanı görünürlüğü için yeni bir menü öğesi eklenir.
- Önceki **Gider raporları** sayfasını **Gider yönetimi > Giderlerim > Gider raporları** öğesine giderek yine açabilirsiniz.
- İş akışları ve onaylar sizi var olan gider raporları sayfasına götürür.
- Makbuzlar Microsoft Azure Cognitive Services aracılığı ile işlenir ve meta veriler çıkarılarak eklenir.
- Eşleştirilmiş, ancak iliştirilmemiş makbuzları içeren bir gider raporu oluşturmanıza olanak sağlayan bir seçenek eklenmiştir.
- Gider raporlarına eklenen bir seçenek, bir makbuzdan bir gider satırı oluşturmanıza olanak sağlar veya var olan bir makbuzu var olan bir gider satırıyla eşleştirmeye çalışır.

Harcama raporlarının yeniden görüntüsü hakkında daha fazla bilgi için bkz. [Gider raporları yeniden düzenleme](ExpenseWorkspaceNew.md).

## <a name="frequently-asked-questions"></a>Sık sorulan sorular

**Microsoft, kendi modelleri için verilerimi mi kullanıyor?**

Hayır, Microsoft makbuz işleme servisi için genel bir makine öğrenimi modeli oluşturmuştur. Bu model, yüklediğiniz makbuzlara dayanmaz.

**Bu özellik nerede bulunur ve işlenir?**

Şu anda Amerika Birleşik Devletleri desteklenmektedir.

**Makbuzlarım nereye gönderilir?**

Finance alan verilerini çıkarmak için Cognitive Services hizmetleriyle iletişim kurar. Cognitive Services, işlem sırasında makbuzunuzun bir kopyasını 24 saat boyunca saklar. İşlem tamamlandıktan sonra, Cognitive Services makbuzu siler. Makbuzlar Finance'de saklanmaya devam eder.

Daha fazla bilgi için bkz. [Form Tanıma'nın yeni özelliği ile makbuz anlamayı etkinleştirme](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).
