---
title: OCR kullanarak makbuz yakalama
description: Bu konu, makbuzlar için optik karakter tanıma (OCR) işlemi hakkında bilgi sağlar.
author: suvaidya
ms.date: 11/10/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1d4c2cce88514e7822515fc407fc7cf31cb34924
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596304"
---
# <a name="capture-a-receipt-using-ocr"></a>OCR kullanarak makbuz yakalama

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Gider girişi, girişler için optik karakter tanıma (OCR) işleminin eklenmesiyle geliştirilmiştir. Bu işlevsellik, gider raporları oluştururken kullanıcı deneyimini geliştirmek için tasarlanmıştır.

## <a name="key-features"></a>Temel özellikler

- Sistem, makbuzlarda satıcı adını, tarihini ve toplam tutarı çıkarır.
- Sistem iliştirilmemiş makbuzlar ile içerisinde iliştirilmemiş dosya bulunmayan gider hareketlerini eşleştirmeyi dener.
- Makbuzlardan el ile girilmiş gider hareketleri oluşturabilirsiniz.

## <a name="attach-receipts-to-an-expense-report"></a>Gider raporuna makbuzları iliştirme

Bir gider raporu oluşturulduğunda kredi kartı hareketlerini içeren makbuzları otomatik olarak iliştirmek için aşağıdaki adımları izleyin.

  1. **Gider yönetimi** çalışma alanını açın.
  2. **Makbuzlar** sekmesinde, iliştirilmemiş makbuzların bulunduğunu doğrulayın. Makbuzları da **Makbuzlar** sekmesine yükleyebilirsiniz.
  3. **Giderler** sekmesinde, içerisinde iliştirilmemiş dosya bulunmayan giderlerin bulunduğunu doğrulayın. Genel olarak gider yöneticisi bu giderleri kredi kartı sağlayıcısından içe aktarır.
  4. **Yeni gider raporu** öğesini seçin. Gider raporu oluştururken, artık giderleri ve makbuzları da dahil edebildiğinizi unutmayın. Hem giderleri, hem de makbuzları eklerseniz, giderler için makbuzların otomatik eşleştirilmesine başlanır.

## <a name="create-or-match-receipts-to-an-expense-report"></a>Gider raporu için makbuzların oluşturulması veya eşleştirilmesi
Bir gider oluşturmak veya bir makbuzdan bir gider ile eşleştirmek için aşağıdaki adımları izleyin.

  1. Gider raporunda, **Makbuzlar** sekmesinde, **Makbuzları ekle**'yi seçerek bir makbuz iliştirin.
  2. Makbuzun karşıya yüklenen görüntüsünün altında, **Oluştur** ve **Eşleştir** seçeneklerine dikkat edin.

      - El ile girilen bir masraf hareketini oluşturmak için **Oluştur** öğesini seçin ve makbuzdan çıkarılan değerleri doldurun.
      - **Eşleştir** seçeneğini belirlediğinizde, sistem var olan bir gideri makbuz eşleştirmeye çalışır.

## <a name="installation"></a>Yükleme

Bu gelişmiş gider yeteneklerini kullanmak için, kurulumunuzda Microsoft Dynamics 365 Finance için Gider Yönetimi Hizmeti eklentisini yükleyin ve özellikleri etkinleştirin. Microsoft Dynamics Lifecycle Services (LCS) içindeki projenizden eklentiye erişebilirsiniz.

1. LCS'de oturum açın ve istenen ortamı açın.
2. **Tüm ayrıntılar**'a gidin.
3. **Koruma**'yı seçin veya **Ortam eklentileri** hızlı sekmesine kaydırın.
4. **Yeni eklenti ekle**'yi seçin.
5. **Gider Yönetim Hizmeti**'ni seçin.
6. Yükleme kılavuzunu izleyin, koşulları ve hükümleri kabul edin.
7. **Yükle**'yi seçin.

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

## <a name="frequently-asked-questions"></a>Sık sorulan sorular

**Microsoft, kendi modelleri için verilerimi mi kullanıyor?**

Hayır, Microsoft makbuz işleme servisi için genel bir makine öğrenimi modeli oluşturmuştur. Bu model, yüklediğiniz makbuzlara dayanmaz.

**Bu özellik nerede bulunur ve işlenir?**

Bu özelliğin farklı bölgelerdeki kullanılabilirliği aşağıdaki tabloda listelenmektedir. Bölgeniz şu anda desteklenmiyorsa, bölgenizdeki OCR hizmetinin kullanılabilirliğinin önceliklendirilmesi için bir istek gönderin. 

| Bölge | Destekleniyor                         |
|--------|-----------------------------------|
| ABD    | Evet                               |
| CAN    | Evet                               |
| Birleşik Krallık     | Evet                               |
| AUS    | Evet                               |
| EU     | Kısmi. Yalnızca İngilizce girişler. |
| Asya   | No                                |
| Japonya  | No                                |
| Afrika | No                                |

**Makbuzlarım nereye gönderilir?**

Finance alan verilerini çıkarmak için Cognitive Services hizmetleriyle iletişim kurar. Cognitive Services, işlem sırasında makbuzunuzun bir kopyasını 24 saat boyunca saklar. İşlem tamamlandıktan sonra, Cognitive Services makbuzu siler. Makbuzlar Finance'de saklanmaya devam eder.

Daha fazla bilgi için bkz. [Form Tanıma'nın yeni özelliği ile makbuz anlamayı etkinleştirme](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
