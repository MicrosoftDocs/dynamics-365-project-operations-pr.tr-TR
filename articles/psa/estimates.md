---
title: Tahminler
description: Bu konu Dynamics 365 Project Service Automation'da tahminler hakkında bilgi sağlar.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 1/31/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 2fa81067ad6e7c291b9ad9468db051e8f6187da9
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151457"
---
# <a name="estimates"></a>Tahminler

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Proje tabanlı bir teklifte, bir projeyi teslim etmek için gereken çalışmayı tahmin etmek üzere Teklif satırı ayrıntısı varlığını kullanabilirsiniz. Daha sonra bu tahmini müşteriyle paylaşabilirsiniz.

Proje tabanlı teklif satırlarında teklif satırı ayrıntıları olması gerekmez. Bunun yerine, çok sayıda teklif satırı ayrıntısı olabilir. Teklif satırı ayrıntıları zaman, gider veya ücretleri tahmin etmek için kullanılır. PSA teklif satırı ayrıntılarında malzeme tahminlerine izin vermez. Bunlar işlem sınıfları olarak adlandırılır. Ayrıca, tahmini vergi tutarları bir işlem sınıfına girilebilir.

İşlem sınıflarına ek olarak, teklif satırı ayrıntıları bir işlem türüne sahiptir. PSA teklif satırı ayrıntıları için iki işlem türünü destekler: **Maliyet** ve **Proje Sözleşmesi**.

## <a name="estimate-by-using-a-contract"></a>Sözleşme kullanarak tahmin etme

Proje tabanlı bir sözleşme oluştururken bir PSA teklifi kullandıysanız, teklifteki her teklif satırı için yaptığınız tahmin proje sözleşmesine kopyalanır. Bir proje sözleşmesinin yapısı satır, satır ayrıntıları ve fatura zamanlamaları bulunan Proje teklifinin yapısına benzer.

Tahminler, proje teklifinde olduğu gibi doğrudan bir proje sözleşmesinde de yapılabilir. Bir proje teklifi için tahmin sözleşme satırları ve sözleşme satırı ayrıntıları kullanılarak yapılır. Sözleşme satırı ayrıntıları, alttaki tahmin yaklaşımı kullanılarak oluşturulan bir proje planından da oluşturulabilir.

Sözleşme satırı ayrıntıları zaman, gider veya ücretleri tahmin etmek için kullanılabilir. Ayrıca, tahmini vergi tutarları bir sözleşme satırı ayrıntısına girilebilir.

PSA sözleşme satırı ayrıntılarında malzeme tahminlerine izin vermez.

Bir proje sözleşmesinde desteklenen işlemler fatura oluşturma ve onaydır. Fatura oluşturma, geçerli tarihe kadar faturalanmamış tüm satış fiili değerlerini içeren proje tabanlı bir faturanın taslağını oluşturur.

Onay sözleşmenin salt okunur olmasını sağlar ve durumunu **Taslak** durumundan **Onaylandı** değiştirir. Bu eylemi gerçekleştirdikten sonra, geri alamazsınız. Bu eylem kalıcı olduğundan, sözleşmeyi **Taslak** durumunda tutmak en iyi uygulamadır.

Taslak sözleşmeler ve onaylanan sözleşmeler arasındaki tek fark durumları ve onaylı sözleşmeler düzenlemediği halde taslak sözleşmelerin düzenlenebilmesidir. Fatura oluşturma ve fiili değerleri izleme, hem taslak sözleşmelerde hem de onaylanan sözleşmelerde yapılabilir.

PSA, sözleşmelerde veya projelerde siparişi değiştirmeyi desteklemez.

## <a name="estimating-projects"></a>Projeleri tahmin etme

Projelerde zaman ve giderleri tahmin edebilirsiniz. PSA, projelerde malzeme ve ücret tahminlerine izin vermez.

Zaman tahminleri, görev oluşturduğunuzda ve görevi gerçekleştirmek için gereken genel bir kaynağın özniteliklerini tanımladığınızda oluşturulur. Zaman tahminleri zamanlama görevlerinden oluşturulur. Zamanlama bağlamının dışında genel takım üyeleri oluşturursanız zaman tahminleri oluşturulmaz.

Gider tahminleri, **Tahminler** sayfasındaki ızgaraya girilebilir.

## <a name="understanding-estimation"></a>Tahminleri anlama

Tahmin aşamasında iş mantığını anlamak için kılavuz olarak aşağıdaki tabloyu kullanın.

| Senaryo                                                                                                                                                                                                                                                                                                                                          | Varlık kaydı                                                                                                                                                                                                       | İşlem Türü | İşlem Sınıfı | Ek bilgiler                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Bir teklifteki satış saati değerini tahmin etmeniz gerektiğinde                                                                                                                                                                                                                                                                                    | Teklif satırı ayrıntısı (QLD) kaydı oluşturulur                                                                                                                                                                               | Proje sözleşmesi | Time        | Satış tarafı QLD satırındaki işlem kaynağı alanı Maliyet tarafı teklif satırı ayrıntısına başvurur. |
|                                                                                                                                                                                                                                                                                     | İkinci bir teklif satırı ayrıntısı kaydı, karşılık gelen maliyet değerlerini depolamak için sistem tarafından oluşturulur. Tüm parasal olmayan alanlar sistem tarafından satış teklif satırı ayrıntısından Maliyet teklif satırı ayrıntısına kopyalanır.                                                                                                                                                                               | Maliyet | Time        | Satış tarafı teklif satırı ayrıntısıı satırındaki işlem kaynağı alanı Maliyet tarafı teklif satırı ayrıntısına başvurur. |
| Bir sözleşmedeki satış saati değerini tahmin etmeniz gerektiğinde                                                                                                                                                                                                                                                                                 | Proje sözleşme satırı ayrıntısı (CLD) kaydı oluşturulur                                                                                                                                                                    | Proje Sözleşmesi | Time        | Satış tarafı CLD satırındaki işlem kaynağı alanı Maliyet sözleşme satırı ayrıntısına başvurur.      |
|                                                                                                                                                                                                                                                                                  | İkinci bir sözleşme satırı ayrıntısı kaydı, karşılık gelen maliyet değerlerini depolamak için sistem tarafından oluşturulur. Tüm parasal olmayan alanlar sistem tarafından satış proje satırı ayrıntısından maliyet proje satırı ayrıntısına kopyalanır.                                                                                                                                                                    | Maliyet | Time        | Satış tarafı CLD satırındaki işlem kaynağı alanı Maliyet sözleşme satırı ayrıntısına başvurur.      |
| Kullanıcı bir proje görevindeki kaynağı tanımladığında                                                                                                                                                                                                                                                                                            | Gerekli tüm fiyatlandırma boyutlarıyla bir görev oluşturulduğunda görevin satış değerini gösteren tahmin satırı kaydı oluşturulur. Rol ve kuruluş birimleri, OOB Project Service fiyatlandırma boyutlarıdır | Proje Sözleşmesi | Time        |                                                                                   |
|     | Gerekli tüm fiyatlandırma boyutlarıyla bir görev oluşturulduğunda görevin maliyet değerini gösteren tahmin satırı kaydı oluşturulur. Tüm parasal olmayan alanlar sistem tarafından satış tahmin satıırndan maliyet tahmin satırına kopyalanır. Rol ve kuruluş birimi, hem maliyet hem de fatura oranları için OOB PSA fiyatlandırma boyutlarıdır.                                                                                                                                                                                                                | Maliyet             | Time           |                                                                                   |



## <a name="customizing-the-quote-line-detail-and-contract-line-detail-entities"></a>Teklif satırı ayrıntısını ve Sözleşme satırı ayrıntısı varlıklarını özelleştirme

Teklif satırı ayrıntısına bir özel alan eklediyseniz ve sistemin alanın değerini oluşturduğu ilgili maliyet satırında varsayılan değer olarak girmesini istiyorsanız, PreOperationContractLineDetailUpdate ve PreOperationQuoteLineDetailUpdatee eklentisini kullanın. Bu eklentilerin teklif satırı ayrıntısı veya sözleşme satırı ayrıntısı değiştirildikten sonra yeniden kaydedilmesi gerekir. İşlemi tamamlamak için aşağıdaki adımları uygulayın:

1. PluginRegistrationTool'u açın ve çevrimiçi kurulumunuza bağlanın.
2. **Ara**'y seçin ve güncelleştirilecek eklentiyi arayın.

    ![Arama Ağacı iletişim kutusu](media/basic-guide-19.png)

3. Eklentiyi seçin ve sonra ana sayfada **Seç**'i seçin.
4. Güncelleştirilecek eklentinin adımını seçin, sağ tıklayın ve ardından **Güncelleştir**'i seçin.

    ![Eklentide bir adım seçme](media/basic-guide-20.png)

5. **Varolan Adımı Güncelleştir** iletişim kutusunda, **Filtre Öznitelikleri** alanında üç nokta düğmesini (**...**) seçin:
 
    ![Varolan Adımı Güncelleştir iletişim kutusu](media/basic-guide-21.png)

6. **Öznitelikleri Seç** iletişim kutusunda, özel öznitelikler için onay kutularını seçin.

    ![Öznitelik Seç iletişim kutusu](media/basic-guide-22.png)

7. İletişim kutusunu kapatmak için **Tamam**'ı seçin ve ardından **Adımı Güncelleştir**'i seçin.
 
    ![Adımı Güncelleştir düğmesi](media/basic-guide-23.png)

8. İkinci eklenti için 1 - 7 arasındaki adımları yineleyin:
9. PluginRegistrationTool'u kapatın.


[!INCLUDE[footer-include](../includes/footer-banner.md)]