---
title: Teklif satırında tahminler oluşturma
description: Bu konu, bir projeyle ilgili teklif satırında nasıl tahmin oluşturulacağı hakkında bilgiler sağlar.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: f4010f7599b66c9ad9e49943c1c0d7d165493d60
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010315"
---
# <a name="create-estimates-on-a-quote-line"></a>Teklif satırında tahminler oluşturma

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Proje tabanlı bir teklifte, bir projeyi teslim etmek için gereken çalışmayı tahmin etmek üzere Teklif satırı ayrıntısı varlığını kullanabilirsiniz. Daha sonra bu tahmini müşteriyle paylaşabilirsiniz.

Proje tabanlı teklif satırlarında teklif satırı ayrıntıları olması gerekmez. Bunun yerine, çok sayıda teklif satırı ayrıntısı olabilir. Teklif satırı ayrıntıları zaman, gider veya ücretleri tahmin etmek için kullanılır. Dynamics 365 Project Operations, teklif satırı ayrıntılarında malzeme tahminlerine izin vermez. Bunlar işlem sınıfları olarak adlandırılır. Ayrıca, tahmini vergi tutarları bir işlem sınıfına girilebilir.

İşlem sınıflarına ek olarak, teklif satırı ayrıntıları bir işlem türüne sahiptir. Teklif satırı ayrıntıları için iki işlem türü bulunur: **Maliyet** ve **Proje Sözleşmesi**.

## <a name="estimate-by-using-a-contract"></a>Sözleşme kullanarak tahmin etme

Proje tabanlı bir sözleşme oluştururken bir Project Operations teklifi kullandıysanız, teklifteki her teklif satırı için yaptığınız tahmin proje sözleşmesine kopyalanır. Bir proje sözleşmesinin yapısı satır, satır ayrıntıları ve fatura zamanlamaları bulunan Proje teklifinin yapısına benzer.

Tahminler, proje teklifinde olduğu gibi doğrudan bir proje sözleşmesinde de yapılabilir. Bir proje teklifi için tahmin sözleşme satırları ve sözleşme satırı ayrıntıları kullanılarak yapılır. Sözleşme satırı ayrıntıları, alttaki tahmin yaklaşımı kullanılarak oluşturulan bir proje planından da oluşturulabilir.

Sözleşme satırı ayrıntıları zaman, gider veya ücretleri tahmin etmek için kullanılabilir. Ayrıca, tahmini vergi tutarları bir sözleşme satırı ayrıntısına girilebilir.

Sözleşme satırı ayrıntılarında malzeme tahminlerine izin verilmez.

Bir proje sözleşmesinde desteklenen işlemler fatura oluşturma ve onaydır. Fatura oluşturma, geçerli tarihe kadar faturalanmamış tüm satış fiili değerlerini içeren proje tabanlı bir faturanın taslağını oluşturur.

Onay sözleşmenin salt okunur olmasını sağlar ve durumunu **Taslak** durumundan **Onaylandı** değiştirir. Bu eylemi gerçekleştirdikten sonra, geri alamazsınız. Bu eylem kalıcı olduğundan, sözleşmeyi **Taslak** durumunda tutmak en iyi uygulamadır.

Taslak sözleşmeler ve onaylanan sözleşmeler arasındaki tek fark durumları ve onaylı sözleşmeler düzenlemediği halde taslak sözleşmelerin düzenlenebilmesidir. Fatura oluşturma ve fiili değerleri izleme, hem taslak sözleşmelerde hem de onaylanan sözleşmelerde yapılabilir.

Sözleşmelerde veya projelerde siparişi değiştirme desteklenmez.

## <a name="estimating-projects"></a>Projeleri tahmin etme

Zaman ve giderleri projelerde tahmin edebilir, ancak malzeme veya ücret edemezsiniz.

Zaman tahminleri, görev oluşturduğunuzda ve görevi gerçekleştirmek için gereken genel bir kaynağın özniteliklerini tanımladığınızda oluşturulur. Zaman tahminleri zamanlama görevlerinden oluşturulur. Zamanlama bağlamının dışında genel takım üyeleri oluşturursanız zaman tahminleri oluşturulmaz.

Gider tahminleri, **Tahminler** sayfasındaki ızgaraya girilebilir.

## <a name="understand-estimation"></a>Tahmini anlama

Tahmin aşamasında iş mantığını anlamak için kılavuz olarak aşağıdaki tabloyu kullanın.

| Senaryo                                                                                                                                                                                                                                                                                                                                          | Varlık kaydı                                                                                                                                                                                                       | İşlem Türü | İşlem Sınıfı | Ek bilgiler                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Bir teklifteki satış saati değerini tahmin etmeniz gerektiğinde                                                                                                                                                                                                                                                                                    | Teklif satırı ayrıntısı (QLD) kaydı oluşturulur                                                                                                                                                                               | Proje sözleşmesi | Time        | Satış tarafı QLD satırındaki işlem kaynağı alanı Maliyet tarafı teklif satırı ayrıntısına başvurur. |
|                                                                                                                                                                                                                                                                                     | İkinci bir teklif satırı ayrıntısı kaydı, karşılık gelen maliyet değerlerini depolamak için sistem tarafından oluşturulur. Tüm parasal olmayan alanlar sistem tarafından satış teklif satırı ayrıntısından Maliyet teklif satırı ayrıntısına kopyalanır.                                                                                                                                                                               | Maliyet | Time        | Satış tarafı teklif satırı ayrıntısıı satırındaki işlem kaynağı alanı Maliyet tarafı teklif satırı ayrıntısına başvurur. |
| Bir sözleşmedeki satış saati değerini tahmin etmeniz gerektiğinde                                                                                                                                                                                                                                                                                 | Proje sözleşme satırı ayrıntısı (CLD) kaydı oluşturulur                                                                                                                                                                    | Proje Sözleşmesi | Time        | Satış tarafı CLD satırındaki işlem kaynağı alanı Maliyet sözleşme satırı ayrıntısına başvurur.      |
|                                                                                                                                                                                                                                                                                  | İkinci bir sözleşme satırı ayrıntısı kaydı, karşılık gelen maliyet değerlerini depolamak için sistem tarafından oluşturulur. Tüm parasal olmayan alanlar sistem tarafından satış proje satırı ayrıntısından maliyet proje satırı ayrıntısına kopyalanır.                                                                                                                                                                    | Maliyet | Time        | Satış tarafı CLD satırındaki işlem kaynağı alanı Maliyet sözleşme satırı ayrıntısına başvurur.      |
| Kullanıcı bir proje görevindeki kaynağı tanımladığında                                                                                                                                                                                                                                                                                            | Gerekli tüm fiyatlandırma boyutlarıyla bir görev oluşturulduğunda görevin satış değerini gösteren tahmin satırı kaydı oluşturulur. Rol ve kuruluş birimleri, fiyatlandırma boyutlarıdır | Proje Sözleşmesi | Zaman        |                                                                                   |
|     | Gerekli tüm fiyatlandırma boyutlarıyla bir görev oluşturulduğunda görevin maliyet değerini gösteren tahmin satırı kaydı oluşturulur. Tüm parasal olmayan alanlar sistem tarafından satış tahmin satıırndan maliyet tahmin satırına kopyalanır. Rol ve kuruluş birimi, hem maliyet hem de fatura oranları için fiyatlandırma boyutlarıdır.                                                                                                                                                                                                                | Maliyet             | Zaman           |                                                                                   |



## <a name="customize-the-quote-line-detail-and-contract-line-detail-entities"></a>Teklif satırı ayrıntısını ve Sözleşme satırı ayrıntısı varlıklarını özelleştirme

Teklif satırı ayrıntısına bir özel alan eklediyseniz ve sistemin alanın değerini oluşturduğu ilgili maliyet satırında varsayılan değer olarak girmesini istiyorsanız, PreOperationContractLineDetailUpdate ve PreOperationQuoteLineDetailUpdatee eklentisini kullanın. Bu eklentilerin teklif satırı ayrıntısı veya sözleşme satırı ayrıntısı değiştirildikten sonra yeniden kaydedilmesi gerekir. İşlemi tamamlamak için aşağıdaki adımları uygulayın:

1. PluginRegistrationTool'u açın ve çevrimiçi kurulumunuza bağlanın.
2. **Ara**'y seçin ve güncelleştirilecek eklentiyi arayın.
3. Eklentiyi seçin ve sonra ana sayfada **Seç**'i seçin.
4. Güncelleştirilecek eklentinin adımını seçin, sağ tıklayın ve ardından **Güncelleştir**'i seçin.
5. **Varolan Adımı Güncelleştir** iletişim kutusunda, **Filtre Öznitelikleri** alanında üç nokta düğmesini (**...**) seçin:
6. **Öznitelikleri Seç** iletişim kutusunda, özel öznitelikler için onay kutularını seçin.
7. İletişim kutusunu kapatmak için **Tamam**'ı seçin ve ardından **Adımı Güncelleştir**'i seçin.
8. İkinci eklenti için 1 - 7 arasındaki adımları yineleyin:
9. PluginRegistrationTool'u kapatın.


[!INCLUDE[footer-include](../includes/footer-banner.md)]