---
title: Satıcı bekletmeye genel bakış
description: Bu makale, satıcı bekletme özelliklerine genel bir bakış sağlar.
author: sigitac
ms.date: 10/01/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 680786f239125905f3b8746cb8318732aa74d9e0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916864"
---
# <a name="vendor-retention-overview"></a>Satıcı bekletmeye genel bakış

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Kuruluşunuz, kuruluşunuz için projelerde çalışan satıcılara yapılacak ödemelerin bir kısmını tutmak isteyebilir. Örneğin, satıcınıza ödeme yapmadan önce, sağladıkları öğelerin ve hizmetlerin beklentilerinize uygun olduğundan emin olmak isteyebilirsiniz.

Satıcılarla proje satın almaları için görüşme yaparken tutulacak yüzde veya tutarı içeren satıcı bekletme koşullarını belirtebilirsiniz. Satıcı öğeleri ve hizmetleri teslime ettiğinde, belirtilen bekletme yüzdesini veya tutarını satıcıya yaptığınız ödemeden düşersiniz. Proje tamamlandığında veya satıcı sözleşmesinde belirtilen geçici bir aşamaya ulaşıldığında, tutulan tutarı serbest bırakıp satıcıya ödeme oluşturursunuz.

## <a name="vendor-retention-example"></a>Satıcı bekletme örneği

Aşağıdaki örnekte, bir proje için tamamlanan yüzdeye göre satıcı fatura tutarının belirli bir yüzdesinin nasıl bekletileceği gösterilmektedir.

Contoso Robotics ABD, donanım yenileme projesi için 100 saat eğitim sunması için Fabrikam satıcısıyla sözleşme yapmıştır. Toplam sözleşme değeri, saat başına 300 USD'den 30.000 USD'dir.

Eğitim aşağıdaki zamanlama ile üç aşamada teslim edilecektir:

- Aşama 1: 50 saat veya projenin yüzde 50'si
- Aşama 2: 30 saat veya toplamda projenin yüzde 80'si
- Aşama 3: 20 saat veya projenin yüzde 100'ü

Aşağıdaki tabloda bekletme koşulları verilmektedir.

| **Teslim edilen birimlerin yüzdesi** | **Bekletilecek yüzde** | **Serbest bırakılacak yüzde** |
| --- | --- | --- |
| %50 | %20 | %0 |
| %80 | %10 | %10 |
| 100% | %0 | 100% |

İşlemler aşağıdaki tutarlara neden olur:

- Aşama 1:
  - Ödenecek tutar 50 x 300 veya 15.000.
  - Tutarın yüzde 20'si veya 3.000 bekletilir ve sonraki bir aşamada serbest bırakılır.
  - Satıcıya ödenen tutar 12.000.
- Aşama 2:
  - Ödenecek tutar 30 x 300 veya 9.000.
  - Tutarın yüzde %10'u veya 900 bekletilir.
  - Aşama 1'de bekletilen 3.000'nin %10'u veya 300 serbest bırakılır.
  - Satıcıya ödenen tutar 8.400. Bu tutar şu şekildedir: 9.000 eksi bekletilen 900 artı Aşama 1'de tutulan ve şimdi serbest bırakılan 300.
- Aşama 3:
  - Ödenecek tutar 20 x 300 veya 6.000.
  - Bekletilen tutar yok.
  - Serbest bırakılan tutar 3.600. Bu tutar şunları içerir: Aşama 1'de bekletilen 3.000 eksi Aşama 1'den Aşama 2'de serbest bırakılan 300 artı Aşama 2'de bekletilen 900.
  - Satıcıya ödenen tutar 9.600. Bu tutar şunları içerir: Bekletilen tutar olan 3.600 artı tamamlanan Aşama 3 için 6.000.

Üç aşama tamamlandıktan sonra satıcıya ödenen toplam tutar, satınalma siparişinin toplam tutarı olan (15.000 + 9.000 + 6.000) 30.000'dir.
