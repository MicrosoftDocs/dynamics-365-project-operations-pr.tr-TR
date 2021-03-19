---
title: Maliyet şablonlarını ayarlama
description: Bu konu, Project Operations'ta maliyet şablonlarının nasıl oluşturulacağı ve kullanılacağı hakkında bilgi sağlar.
author: sigitac
manager: tfehr
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d9dcc54e62682a02ea6cf8caca90586b4217908
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278982"
---
# <a name="set-up-cost-templates"></a>Maliyet şablonlarını ayarlama

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_


Bu konu, Project Operations'ta maliyet şablonlarının nasıl oluşturulacağı ve kullanılacağı hakkında bilgi sağlar. Maliyet şablonu şunları belirler:

- Proje tamamlanma hesaplamasının yüzdesine dahil edilecek tahmini ve gerçek işlemler için proje kategorileri. Tamamlanma yüzdesi değeri daha sonra ne kadar gelirin tanındığını hesaplamak için kullanılır.
- Tamamlanma yüzdesi otomatik olarak hesaplanırsa tamamlanma yüzdesinin değiştirilip değiştirilemeyeceği.
- Tamamlanma yüzdesinin tutarlara veya birimlere göre hesaplanıp hesaplanmadığı.

## <a name="cost-template-example"></a>Maliyet şablonu örneği

Bir müşteri için 10.000 USD sabit ücret aldığınız bir web sitesi tasarım projesi üzerinde çalışıyorsunuz. Projenin 100 saatte (5.000 USD) tamamlanacağını tahmin ediyorsunuz. Ayrıca müşterinin tesisine yapılacak ziyaretler için iki uçak bileti ve otelde dört gece konaklama (1.800 USD) tahmin ediyorsunuz. Sonuçta 6.800 USD tutarında bir tahmini maliyet var.

Ay sonunda bir tahmin oluşturmak için sabit fiyatlı gelir tanıma işlemini çalıştırdığınızda, projede 35 saat çalıştığınızı buluyorsunuz. Buna henüz uçuş ve otel masrafları dahil değil. Ayrıca proje için 100 USD maliyetle beş saatlik araştırma yapan ve daha öncesinde planlamadığınız bir yardımcınız da vardı.

Bu proje için yüzde tamamlanma değerini hesapladığınızda aşağıdaki seçimleri yapmanız gerekir:

- Tüm maliyetleri mi (saatler ve giderler) yoksa yalnızca saatleri mi dahil etmek istiyorsunuz?
- Tüm saatleri mi yoksa yalnızca planlanan saatleri mi dahil etmek istiyorsunuz?
- Tamamlanma yüzdesini planlanan saatlerin dolar maliyetine (5.000 USD) göre mi yoksa yalnızca saat sayısına (100) göre mi hesaplamak istiyorsunuz?

Bu sorulara vereceğiniz yanıtlar, maliyet şablonunda belirlediğiniz seçenekleri ve maliyet şablonu satırlarında seçtiğiniz kategorileri belirler.

Aşağıdaki tabloda bu senaryonun tamamlanma yüzdesi değerini hesaplamanın farklı yöntemlerinin sonuçları gösterilmektedir.

| Tamamlanmada temel alınan: | Dolar maliyeti veya birimler | Tamamlanma yüzdesi | Hesaplama |
| --- | --- | --- | --- |
| Tüm saatler, giderler hariç | Dolar maliyeti | %37 35 x 50 USD + 100 USD = 1.850 USD 1.850 USD/5.000 USD |
| Tüm saatler, giderler hariç | Birim | %40 | 40 saat/100 saat (planlanmamış beş saat dahil) |
| Planlanmış saatler, giderler hariç | Dolar maliyeti veya birim | %35 | 35/100 saat veya 35 x 50 USD/5.000 |
| Tüm saatler ve giderler | Dolar maliyeti | %27,2 | 1.850 USD/6.800 USD |

Maliyet şablonu oluşturmak için hangi yaklaşımın benimseneceğine karar verilmesi, bazı değerlendirmelere bağlı olabilir:

- Maliyet şablonuna planlanmamış saatleri eklerseniz proje bitmeden yüzde 100 tamamlanma oranına ulaşma riskiyle karşılaşırsınız. Bunun nedeni, gerçek saatlerin planlanan saatlerden daha fazla olmasıdır. Tabloda listelenen ilk iki yöntemden birini kullanırsanız sapmaların farkına vardığınızda planı (tahmin edilen birimler) değiştirmelisiniz. Bu durumda, projeyi bitirmek için neyin gerekli olduğu konusundaki bilgilerinize göre saatler ekler veya çıkarırsınız. Projenin tamamlanması için 65 saat daha gerekiyorsa toplamı 105 olacak şekilde plana beş saat eklersiniz. Yardımcınızın beş saatlik bir araştırma daha yapacağını biliyorsanız toplam 110 saat olacaktır.
- Tabloda listelenen üçüncü yöntemi kullanırsanız tamamlanma yüzdesi hesaplamasının doğru olmasını sağlamak için planlanan saatleri yalnızca kendi zamanınız için güncelleştirmeniz gerekir. Planlanmamış saatler kaydedildiğinde karlılığınız değişir ancak bilinen bir tamamlanma yüzdesi yolunu izlemeye devam edersiniz.
- Tabloda listelenen dördüncü yöntemi kullandığınızda giderlerin, düzensiz zamanlarda ortaya çıkması ve tamamlanma durumu ilerlemenize yansıtılmaması riskiyle karşılaşırsınız. Bu nedenle, giderlerin dahil edilirse tamamlanma yüzdenizin istenenden daha fazla dalgalanmasına neden olabilir. Örneğin, henüz uçuş yapmadığınız için hesaplamayı yalnızca zamana göre yapacak olsaydınız tamamlanma yüzdeniz yüzde 35 veya yüzde 37 yerine yüzde 27 olurdu. İki gece konaklamalı bir seyahat gerçekleştirmiş olsaydınız ve uçuş ve otel maliyetlerinizi doğru tahmin etmiş olsaydınız tamamlanma yüzdesi yüzde 40,4 (işçilik için 1850 USD ve giderler için 900 USD = 2750 USD/6800 USD = yüzde 40,4) olurdu. Bu nedenle, tek bir gidiş dönüş uçak yolculuğunun masrafları, tamamlanma yüzdesini yüzde 27'den yüzde 40'a değiştirirdi.

## <a name="create-cost-templates"></a>Maliyet şablonları oluşturma
Maliyet şablonları oluşturmak için şu adımları izleyin:

1. Maliyet şablonlarına erişmek için Dynamics 365 Finance ortamında **Proje yönetimi ve muhasebe** > **Kurulum** > **Tahminler** > **Maliyet şablonu**'na gidin.
2. Yeni maliyet şablonu oluşturmak için **Yeni**'yi seçin. Ad ve açıklama girin.
3. Her hareket türü için maliyet satırı kimliği sağlayın.
4. Varsayılan bir tamamlama yöntemi seçin:

  - **Otomatik**: Projenin tamamlanma yüzdesini otomatik olarak hesaplar. Elde edilen değer değiştirilemez.
  - **El ile**: Projenin tamamlanma yüzdesini otomatik olarak hesaplar. Elde edilen değer değiştirilebilir.

  > [!NOTE]
  > El ile hesaplamalar için tamamlanma yüzdesi, **Tahmin** sayfasında **Genel** sekmesindeki **El ile hesaplama** bölümünde tutulur.

5. **Tamamlanmada temel alınan**'da, aşağıdaki değerlerden birini seçin:

  - **Tutar**: Muhasebe para birimindeki tutar, tamamlanma yüzdesini hesaplar.
  - **Birim**: Miktar, tamamlanma yüzdesini hesaplar.
  - **Düz çizgi**: Sistem, projenin uzunluğunu belirlemek için proje başlangıç ve bitiş tarihlerini kullanarak oransal bir şekilde tamamlanma yüzdesini hesaplar.

6. Maliyet şablonunun maliyet satırlarını gözden geçirmek için **Maliyet satırları**'nı seçin. Her işlem türü için en az bir maliyet satırı gereklidir. Ancak aynı işlem türleri için birden çok maliyet satırı oluşturabilir ve bu satırlar için istenen öznitelikleri ayarlayabilirsiniz.
7. **Kategoriler** sekmesinde, maliyet şablonu satırına dahil edilecek proje kategorilerini seçin.
8. **Genel** sekmesinde, bu satırın tamamlanma yüzdesi hesaplamasına dahil edilip edilmeyeceğini seçin.
9. Tamamlanma yüzdesini hesaplarken kullanılacak tamamlama maliyeti yöntemini seçin.


[!INCLUDE[footer-include](../includes/footer-banner.md)]