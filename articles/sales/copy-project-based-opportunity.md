---
title: Proje tabanlı fırsatları kopyalama
description: Bu konuda Project Operations'ta proje tabanlı fırsatların kopyalanması hakkında bilgi sağlanır.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 83fe41cb16be6bdd91219fc59e517ae0e5848afec5f771edde575bb5c24f9865
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999745"
---
# <a name="copy-project-based-opportunities"></a>Proje tabanlı fırsatları kopyalama

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_


Proje Fırsatları, yeni proje fırsatları oluşturmak için kolayca kopyalanabilir. 

1. **Proje Fırsatları** listesi sayfasına gidin ve listeden bir fırsat seçin. Veya, belirli bir fırsatın Ayrıntılar sayfasını açın. 
2. Her iki sayfadan birinden **Kopyala**'yı seçin. Aşağıdaki alan bilgilerini içeren bir iletişim kutusu açılır. Bu iletişim kutusunda seçtiğiniz değerlere bağlı olarak kopyalama işlemi değişebilir.

    | **Alan** | **Açıklama** | **Aşağı yönlü etki** |
    | --- | --- | --- |
    | Başlık | Hedef fırsatın ilgili konusunu girin. İletişim kutusu açıldığında sistem bunu **-kopya** ifadesi eklenmiş olarak kaynak fırsatın konu kısmı olarak ayarlar. | Bu alanda aşağı yönlü etki yoktur. |
    | Hesap | Müşterinin şirket veya firma kaydına başvurular. İletişim kutusu açıldığında sistem bunu kaynak fırsatındaki firma olarak ayarlar. | Bu alan, fırsattaki birincil müşteridir. |
    | Sözleşme Birimi | Bu anlaşmayla ilişkili projelerin tesliminden sorumlu olan kuruluş birimi. İletişim kutusu açıldığında sistem bunu kaynak fırsatındaki sözleşme birimi olarak ayarlar. | Sözleşme birimi, şirketin anlaşma kapatıldıktan sonra projeleri yürüten bölümüdür. Sözleşme yapan her biriminin bir para birimi vardır ve bu para birimi, proje sırasında oluşan tahmini ve gerçek maliyetleri bildirmek için kullanılır. |
    | Para birimi | Anlaşmanın işlem gördüğü para birimidir. İletişim kutusu açıldığında sistem bunu kaynak fırsatındaki para birimi olarak ayarlar. | Para birimi, Fiyat listesine varsayılan olarak ve teklifte mali tahminler oluşturmak için kullanılır. Zaman zaman, anlaşma kazanıldığında müşteriyi faturalamak için kullanılır. |
    | Fiyatlandırmayı kopyala | Fırsattaki fiyatlandırmasının kaynak fırsattan kopyalanıp kopyalanmayacağını belirten bir Evet/Hayır değeri. | **Evet** seçilirse Fiyat listeleri kaynaktan hedef fırsata kopyalanır. **Hayır** seçilirse fiyat listeleri, ayarlanan en son fiyat listelerine göre yeniden varsayılan hale getirilir. |

3. **Tamam**'ı seçin. Sistem, seçilen parametrelere göre proje fırsatının bir kopyasını oluşturur ve yeni proje fırsatı açılır.


[!INCLUDE[footer-include](../includes/footer-banner.md)]