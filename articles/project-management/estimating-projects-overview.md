---
title: Mali tahmin kavramları
description: Bu konu, Project Operations'ta projelerin mali tahminleri hakkında bilgi sağlar.
author: rumant
ms.date: 03/22/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 338d2924f0e2a4a7fb943686eaad421a892dce70
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597776"
---
# <a name="financial-estimation-concepts"></a>Mali tahmin kavramları

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Dynamics 365 Project Operations'ta artık iki aşamada projelerinizin mali tahminini gerçekleştirebilirsiniz: 
1. Anlaşma yapılmadan, satış öncesi aşaması sırasında. 
2. Proje sözleşmesi oluşturulduktan sonra, yürütme aşaması sırasında. 

Aşağıdaki 3 sayfadan birini kullanarak, proje tabanlı çalışmalar için bir mali tahmin oluşturabilirsiniz:
- **Teklif satırı** sayfası, teklif satırı ayrıntılarını kullanarak.  
- **Teklif sözleşmesi satırı** sayfası, sözleşme satırı ayrıntılarını kullanarak. 
- **Proje** sayfası, **Görevler** veya **Gider Tahminleri** sekmesi sayfalarını kullanarak.

## <a name="use-a-project-quote-to-create-an-estimate"></a>Tahmin oluşturmak için bir proje teklifi kullanma
Proje tabanlı bir teklifte, bir projeyi teslim etmek için gereken çalışmayı tahmin etmek üzere **Teklif satırı ayrıntısı** varlığını kullanabilirsiniz. Daha sonra bu tahmini müşteriyle paylaşabilirsiniz.

Proje tabanlı teklif satırlarında teklif satırı sıfır da olabilir, birden çok da olabilir. Teklif satırı ayrıntıları zaman, gider veya ücretleri tahmin etmek için kullanılır. Microsoft Dynamics 365 Project Operations, teklif satırı ayrıntılarında malzeme tahminlerine izin vermez. Bunlar işlem sınıfları olarak adlandırılır. Ayrıca, tahmini vergi tutarları bir işlem sınıfına girilebilir.

İşlem sınıflarına ek olarak, teklif satırı ayrıntıları bir işlem türüne sahiptir. Teklif satırı ayrıntıları için iki hareket türü desteklenir: **Maliyet** ve **Proje Sözleşmesi**.

## <a name="use-a-project-contract-to-create-an-estimate"></a>Tahmin oluşturmak için bir proje sözleşmesi kullanma

Proje tabanlı bir sözleşme oluştururken bir teklif kullandıysanız, teklifteki her teklif satırı için yaptığınız tahmin proje sözleşmesine kopyalanır. Bir proje sözleşmesinin yapısı satır, satır ayrıntıları ve fatura zamanlamaları bulunan Proje teklifinin yapısına benzer.

Tahminler, proje teklifinde olduğu gibi doğrudan bir proje sözleşmesinde de yapılabilir. Bir proje teklifi için tahmin sözleşme satırları ve sözleşme satırı ayrıntıları kullanılarak yapılır. Sözleşme satırı ayrıntıları, alttaki tahmin yaklaşımı kullanılarak oluşturulan bir proje planından da oluşturulabilir.

Sözleşme satırı ayrıntıları zaman, gider veya ücretleri tahmin etmek için kullanılabilir. Ayrıca, tahmini vergi tutarları bir sözleşme satırı ayrıntısına girilebilir.

Sözleşme satırı ayrıntılarında malzeme tahminlerine izin verilmez.

## <a name="use-a-project-to-create-an-estimate"></a>Tahmin oluşturmak için bir proje kullanma 

Projelerde zaman ve giderleri tahmin edebilirsiniz. Project Operations, projelerde malzeme veya ücret tahminlerini desteklemez.

Zaman tahminleri, görev oluşturduğunuzda ve görevi gerçekleştirmek için gereken genel bir kaynağın özniteliklerini tanımladığınızda oluşturulur. Zaman tahminleri zamanlama görevlerinden oluşturulur. Zamanlama bağlamının dışında genel takım üyeleri oluşturursanız zaman tahminleri oluşturulmaz.

Gider tahminleri, **Gider Tahminleri** sayfasındaki ızgaraya girilebilir.

Proje planındaki her bir görevde işçilik veya zaman ve giderler için alttan üste ayrıntılı tahminler oluşturabildiğiniz için bir proje için tahmin oluşturma en iyi uygulama olarak kabul edilir. Daha sonra bu ayrıntılı tahmini, her teklif satırı için tahminler oluşturmak ve müşteri için daha güvenilir bir teklif oluşturmak amacıyla kullanabilirsiniz. Proje planını kullanarak teklif satırında ayrıntılı bir tahmin içe aktardığınızda veya oluşturduğunuzda, Project Operations bu tahminlerin satış değerlerini ve maliyet değerlerini içe aktarır. İçe aktarma işleminden sonra proje teklifinde kârlılık, marjlar ve uygulanabilirliği görüntüleyebilirsiniz.

## <a name="understanding-estimates"></a>Tahminleri anlama

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

Teklif satırı ayrıntısına bir özel alan eklediyseniz ve sistemin alanın değerini oluşturduğu ilgili maliyet satırında varsayılan değer olarak girmesini istiyorsanız, **PreOperationContractLineDetailUpdate** ve **PreOperationQuoteLineDetailUpdate** eklentisini kullanın. Bu eklentilerin teklif satırı ayrıntısı veya sözleşme satırı ayrıntısı değiştirildikten sonra yeniden kaydedilmesi gerekir. İşlemi tamamlamak için aşağıdaki adımları uygulayın:

1. PluginRegistrationTool'u açın ve çevrimiçi kurulumunuza bağlanın.
2. **Ara**'y seçin ve güncelleştirilecek eklentiyi arayın.
3. Eklentiyi seçin ve sonra ana sayfada **Seç**'i tıklayın.
4. Güncelleştirilecek eklentinin adımını seçin, sağ tıklayın ve ardından **Güncelleştir**'i seçin.
5. **Varolan Adımı Güncelleştir** iletişim kutusunda, **Filtre Öznitelikleri** alanında üç nokta düğmesini (**...**) seçin:
6. **Öznitelikleri Seç** iletişim kutusunda, özel öznitelikler için onay kutularını seçin.
7. İletişim kutusunu kapatmak için **Tamam**'ı seçin ve ardından **Adımı Güncelleştir**'i seçin.
8. İkinci eklenti için 1 - 7 arasındaki adımları yineleyin:
9. **PluginRegistrationTool**'u kapatın.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
