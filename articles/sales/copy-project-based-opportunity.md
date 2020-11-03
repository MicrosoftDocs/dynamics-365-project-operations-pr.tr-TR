---
title: Proje tabanlı fırsatları kopyalama
description: Bu konuda Project Operations'ta proje tabanlı fırsatların kopyalanması hakkında bilgi sağlanır.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 89f5a63581f36b30634bdd302a6d360d6b5e75bd
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086263"
---
# <a name="copy-project-based-opportunities"></a>Proje tabanlı fırsatları kopyalama

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_


Proje Fırsatları, yeni proje fırsatları oluşturmak için kolayca kopyalanabilir. 

1. **Proje Fırsatları** listesi sayfasına gidin ve listeden bir fırsat seçin. Veya, belirli bir fırsatın Ayrıntılar sayfasını açın. 
2. Her iki sayfadan birinden **Kopyala** 'yı seçin. Aşağıdaki alan bilgilerini içeren bir iletişim kutusu açılır. Bu iletişim kutusunda seçtiğiniz değerlere bağlı olarak kopyalama işlemi değişebilir.

    | **Alan** | **İlgi, amaç ve kılavuz** | **Aşağı yönlü etki** |
    | --- | --- | --- |
    | Başlık | Hedef fırsatın ilgili konusunu girin. İletişim kutusu açıldığında sistem bunu **-kopya** ifadesi eklenmiş olarak kaynak fırsatın konu kısmı olarak ayarlar. | Bu alanda aşağı yönlü etki yoktur. |
    | Hesap | Müşterinin şirket veya firma kaydına başvurular. İletişim kutusu açıldığında sistem bunu kaynak fırsatındaki firma olarak ayarlar. | Bu alan, fırsattaki birincil müşteridir. |
    | Sözleşme Birimi | Bu anlaşmayla ilişkili projelerin tesliminden sorumlu olan kuruluş birimi. İletişim kutusu açıldığında sistem bunu kaynak fırsatındaki sözleşme birimi olarak ayarlar. | Sözleşme birimi, şirketin anlaşma kapatıldıktan sonra projeleri yürüten bölümüdür. Sözleşme yapan her biriminin bir para birimi vardır ve bu para birimi, proje sırasında oluşan tahmini ve gerçek maliyetleri bildirmek için kullanılır. |
    | Para birimi | Anlaşmanın işlem gördüğü para birimidir. İletişim kutusu açıldığında sistem bunu kaynak fırsatındaki para birimi olarak ayarlar. | Para birimi, Fiyat listesine varsayılan olarak ve teklifte mali tahminler oluşturmak için kullanılır. Zaman zaman, anlaşma kazanıldığında müşteriyi faturalamak için kullanılır. |
    | Fiyatlandırmayı kopyala | Fırsattaki fiyatlandırmasının kaynak fırsattan kopyalanıp kopyalanmayacağını belirten bir Evet/Hayır değeri. | **Evet** seçilirse Fiyat listeleri kaynaktan hedef fırsata kopyalanır. **Hayır** seçilirse fiyat listeleri, ayarlanan en son fiyat listelerine göre yeniden varsayılan hale getirilir. |

3. **Tamam** 'ı seçin. Sistem, seçilen parametrelere göre proje fırsatının bir kopyasını oluşturur ve yeni proje fırsatı açılır.
