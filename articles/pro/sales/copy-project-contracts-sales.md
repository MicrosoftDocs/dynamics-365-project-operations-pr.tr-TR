---
title: Proje sözleşmelerini kopyalama
description: Bu konuda,Project Operations'ta proje sözleşmelerini kopyalama hakkında bilgiler sağlanmaktadır.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6da8e3ba8e062f3e06dc7f440caebdd93e496c65
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086229"
---
# <a name="copying-project-contracts"></a>Proje sözleşmelerini kopyalama

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Varolan sözleşmelerin kopyalarını iki şekilde yaparak kolayca yeni proje sözleşmeleri oluşturabilirsiniz: 

  - **Proje Sözleşmeleri** listesi sayfasında bir proje sözleşmesi açın ve sonra **Kopyala** 'yı seçin.
  - **Proje Sözleşmesi** ayrıntıları sayfasında **Kopyala** 'yı seçin.

Kopyalanan sözleşmenin parametrelerini seçebileceğiniz iletişim kutusu sayfası açılır. Aşağıdaki alanlar, iletişim kutusuna dahil edilir. Bu iletişim kutusunda seçtiğiniz değerlere bağlı olarak kopyalama işlemi değişebilir.

| **Alan** | **İlgi, amaç ve kılavuz** | **Aşağı yönlü etki** |
| --- | --- | --- |
| Başlık | Hedef Sözleşmenin konusunu girin. İletişim kutusu sayfası açıldığında sistem bu alanı, **kopya** ifadesi eklenmiş kaynak sözleşmesinin adı olarak ayarlar. | Bu alanda aşağı yönlü etki yoktur. |
| Müşteri | Müşterinin şirket veya firma kaydına başvuru. İletişim kutusu açıldığında sistem bu alanı kaynak sözleşmesindeki firma olarak ayarlar. | Bu alan, sözleşmedeki birincil müşteridir. |
| Sözleşme Birimi | Bu anlaşmayla ilişkili projelerin tesliminden sorumlu olan kuruluş birimi. İletişim kutusu sayfası açıldığında sistem bunu kaynak sözleşmedeki sözleşme birimi olarak ayarlar. | Sözleşme yapan birim, şirketin anlaşma kapatıldıktan sonra projeleri yürüten bölümüdür. Sözleşme yapan her biriminin bir para birimi vardır. Bu para birimi, proje sırasında oluşan tahmini ve gerçek maliyetleri bildirmek için kullanılır. |
| Para birimi | Anlaşmanın işlem gördüğü para birimidir. İletişim kutusu sayfası açıldığında sistem alanı kaynak sözleşmedeki para birimi olarak ayarlar. Para birimi değiştirilemiyor. Böyleyse kaynak sözleşmedeki fiyat listeleri artık alakalı olmadığından, **Kopyalama Fiyatlandırması** alanı her zaman **Hayır** olarak ayarlanır. | Para birimi, bir fiyat listesini varsayılan olarak belirlemek, sözleşme üzerine bir mali tahmin oluşturmak ve sonunda anlaşma kazanıldığında müşteriye fatura kesmek için kullanılır. |
| Talep Edilen Teslimat Tarihi | Müşteri tarafından istenen teslim tarihi. | Bu tarih, belirli bir sıklıkta faturalama tarihleri oluştururken bitiş tarihi olarak kullanılır. |
| Fiyatlandırmayı kopyala | Sözleşme üzerindeki fiyatlandırmanın kaynak sözleşmeden kopyalanması gerekip gerekmediğini gösterir. | Alan **Evet** olarak seçilirse proje fiyat listesi ve ürün fiyat listesi başvuruları kaynak sözleşmeden hedef sözleşmeye kopyalanır. **Hayır** seçilirse fiyat listeleri, firma veya proje parametrelerinde ayarlanan en son fiyat listelerine göre yeniden varsayılan hale getirilir. |

İletişim sayfasında **Tamam** 'ı seçtiğinizde sistem, seçilen parametrelere göresözleşmenin bir kopyasını oluşturur. Yeni sözleşme açılacak.

Aşağıdaki bilgiler **Kaynak** 'tan **Hedef teklife** kopyalanmaz:

  - Fatura zamanlamaları
  - Sözleşme ve sözleşme satırı müşterileri
  - Proje tabanlı sözleşme satırlarında proje başvurusu
  - Müşteri bütçe bilgileri

Bu bilgiler sözleşmelere özgü olduğu için bu alanlar ve kayıtlar kopyalanmaz. Projeler ve ürünler için sözleşme satırları, sözleşme satırı ayrıntılarına ilişkin tahminler ve sözleşme düzeyinde aşılmaz değerler kopyalanır. Varsayılan fiyat ve maliyet oranları **Parametreleri kopyala** iletişim sayfasında seçilen **Fiyatlandırmayı kopyala** alanına bağlıdır.
