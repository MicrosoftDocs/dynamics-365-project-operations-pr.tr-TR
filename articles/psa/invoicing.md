---
title: Project Service Automation'da faturalama
description: Bu konu faturalama hakkında bilgi sağlar.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: e0dc911bb0ca72af547262a5716ef1091ea81c81
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6015085"
---
# <a name="invoicing-in-project-service-automation"></a>Project Service Automation'da faturalama

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation'da faturalama, müşteri faturaları oluşturmadan önce proje yöneticilerine ikinci bir onay düzeyi verdiğinden dolayı faydalıdır. Proje takım üyelerinin gönderdiği zaman ve gider girişleri onaylandığında onayın ilk düzeyi tamamlanır.

PSA, aşağıdaki nedenlerden dolayı müşteriye yönelik faturalar oluşturmak üzere tasarlanmamıştır:

- Vergi bilgilerini içermez.
- Doğru yapılandırılmış döviz kurlarını kullanarak diğer para birimlerini faturalama para birimine dönüştüremez.
- Faturaları, yazdırılabilmeleri için doğru olarak biçimlendiremez.

Bunun yerine, PSA'da oluşturulan fatura tekliflerinden bilgileri kullanan müşteriye yönelik faturalar oluşturmak için mali veya muhasebe sistemini kullanabilirsiniz.

## <a name="creating-project-invoices-in-psa"></a>PSA'da proje faturaları oluşturma

Proje faturaları tek tek veya toplu olarak oluşturulabilir. El ile oluşturulabilirler veya otomatik çalıştırmalar halinde oluşturulmak üzere yapılandırılabilirler.

### <a name="manually-create-project-invoices-in-psa"></a>PSA'da proje faturalarını el ile oluşturma

**Proje Sözleşmeleri** listesi sayfasından, her proje sözleşmesi için ayrı olarak proje faturaları oluşturabilir veya birden çok proje sözleşmesi için toplu olarak fatura oluşturabilirsiniz.

Belirli bir proje sözleşmesi için fatura oluşturmak üzere bu adımı izleyin.

- **Proje Sözleşmeleri** listesi sayfasında bir proje sözleşmesi açın ve sonra **Fatura oluştur** 'u seçin.

    ![Belirli bir proje sözleşmesi için proje faturaları oluşturma](media/CreateProjectInvoicesOneByOne.png)

    **Faturalamaya Hazır** durumuna sahip seçili proje sözleşmesine ilişkin tüm işlemler için bir fatura oluşturulur. Bu işlemler zaman, gider, kilometre taşları ve ürün tabanlı sözleşme satırlarını içerir.

Faturaları toplu olarak oluşturmak için bu adımları izleyin.

1. **Proje Sözleşmeleri** listesi sayfasında, fatura oluşturmanız gereken bir veya daha fazla proje sözleşmesi seçin ve ardından **Proje Faturaları Oluştur**'u seçin.

    ![Proje faturalarını toplu oluşturma](media/CreateProjectInvoicesBulk.png)

    Bir uyarı iletisi, faturalar oluşturulmadan önce bir gecikme olabileceği konusunda sizi uyarır. İşlem de gösterilir.

2. İleti kutusunu kapatmak için **Tamam**'ı seçin.

    **Faturalamaya Hazır** durumuna sahip sözleşme satırında tüm işlemler için bir fatura oluşturulur. Bu işlemler zaman, gider, kilometre taşları ve ürün tabanlı sözleşme satırlarını içerir.

3. Oluşturulan faturaları görüntülemek için **Satış** \> **Faturalama** \> **Faturalar**'a gidin. Her proje sözleşmesi için bir fatura görürsünüz.

### <a name="set-up-automated-creation-of-project-invoices-in-psa"></a>PSA'da otomatik proje faturaları oluşturmayı ayarlama

PSA'da otomatik fatura çalıştırmayı yapılandırmak için bu adımları izleyin.

1. **Project Service** \> **Ayarlar** \> **Toplu İşler** bölümüne gidin.
2. Bir toplu iş oluşturun ve **PSA Fatura Oluştur** olarak adlandırın. Toplu işin adı "Faturaları oluştur" terimini içermelidir.
3. **İş türü** alanında **Hiçbiri**'ni seçin. Varsayılan olarak, **Günlük Sıklık** ve **Etkin** seçenekleri **Evet** olarak ayarlanır.
4. **İş Akışı Çalıştır**'ı seçin. **Kayıt Ara** iletişim kutusunda üç iş akışı görürsünüz:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. **ProcessRunCaller**'ı ve ardından **Ekle**'yi seçin.
6. Sonraki iletişim kutusunda **Tamam**'ı seçin. **Uyku** iş akışının ardından **Süreç** iş akışı gelir.

    Ayrıca, adım 5'te **ProcessRunner**'ı seçebilirsiniz. Ardından **Tamam**'ı seçtiğinizde, bir **Süreç** iş akışının ardından bir **Uyku** iş akışı gelir.

**ProcessRunCaller** ve **ProcessRunner** iş akışları faturaları oluşturur. **ProcessRunCaller** **ProcessRunner**'ı çağırır. **ProcessRunner**, faturaları gerçekte oluşturan iş akışıdır. Bu, fatura oluşturulması için gereken tüm sözleşme satırlarından geçer ve bu satırlar için faturalar oluşturur. Faturaların oluşturulması gereken sözleşme satırlarını belirlemek için, iş sözleşme satırları için fatura çalıştırma tarihlerine bakar. Bir sözleşmeye ait olan sözleşme satırları aynı fatura çalıştırma tarihine sahipse, işlemler iki fatura satırı bulunan tek bir faturada birleştirilir. Fatura oluşturulacak bir işlem yoksa, iş fatura oluşturmayı atlar.

**ProcessRunner** çalışması bittikten sonra, **ProcessRunCaller** öğesini çağırır, bitiş saati sağlar ve kapatılır. **ProcessRunCaller** daha sonra belirtilen bitiş saatinden itibaren 24 saat çalışan bir zamanlayıcı başlatır. Zamanlayıcının sonunda **ProcessRunCaller** kapatılır.

Fatura oluşturmaya yönelik toplu iş yinelenen bir iştir. Bu toplu iş birçok defa çalıştırılırsa, işin birden çok kopyası oluşturulur ve hatalara yol açar. Bu nedenle, toplu işi yalnızca bir kez başlatmanız gerekir ve yalnızca çalışmayı durdurduğunda yeniden başlatılmalıdır.

> [!NOTE]
> Project Service Automation'ta toplu faturalama yalnızca fatura zamanlamalarında yapılandırılan proje sözleşme satırları için çalışır. Sabit fiyatlı fatura yöntemine sahip bir sözleşme satırının kilometre taşları yapılandırılmış olmalıdır. Zaman ve malzeme faturalama yöntemi içeren bir proje sözleşmesi satırı, ayarlanmış bir tarih tabanlı fatura çizelgesine gereksinim duyar. Bir teklif satırını temel alan bir proje bağlamında faturalama sıklıklarını ayarlama hakkında bilgi, konu, [teklif ve teklif satırlarında verilmiştir](basic-quote-lines.md#invoice-schedule). Aynı şekilde, proje tabanlı bir sözleşme satırı için de geçerlidir.      
 
### <a name="edit-a-draft-psa-invoice"></a>Taslak bir PSA faturasını düzenleme

Bir taslak proje faturası oluşturduğunuzda, zaman ve gider girişleri onaylandığında oluşturulan tüm faturalanmamış satış işlemleri faturaya alınır. Fatura hala taslak aşamasındayken aşağıdaki ayarlamaları yapabilirsiniz:

- Fatura satırı ayrıntılarını silmek veya düzenlemek.
- Miktarı ve faturalandırma türünü düzenlemek ve ayarlamak.
- Zaman, gider ve ücretleri faturadaki işlemler olarak doğrudan eklemek. Bu işlem sınıflarına izin veren bir sözleşme satırıyla eşlenmiş fatura satırı varsa, bu özelliği kullanabilirsiniz.

Bir faturayı onaylamak için **Onayla**'yı seçin. Onayla eylemi tek yönlü bir eylemdir. **Onayla**'yı seçtiğinizde, sistem faturayı salt okunur yapar ve her fatura satırı için her fatura satırı ayrıntısından faturalanan satış fiili değerleri oluşturur. Fatura satırı ayrıntısı faturalanmamış bir satış fiili değerine başvuruyorsa sistem faturalanmamış satış fiili değerini de tersine çevirir. (Bir zaman veya gider girişinden oluşturulan tüm fatura satırı ayrıntıları, faturalandırmamış bir satış fiili değerine başvuracaktır.) Genel muhasebe tümleştirme sistemleri, bu geri çevirme işlemini, süren proje işlerini (WIP) muhasebe amacıyla tersine çevirmek için kullanabilir.

### <a name="correct-a-confirmed-psa-invoice"></a>Onaylanmış PSA faturasını düzeltme

Onaylanmış PSA faturaları düzenlenebilir (düzeltilebilir). Onaylı bir faturayı düzeltirken, yeni bir taslak düzeltme faturası oluşturulur. Orijinal faturadaki tüm hareketleri ve miktarları tersine çevirmek istediğiniz varsayıldığından, bu düzeltme faturası orijinal faturadaki tüm işlemleri içerir ve üzerindeki tüm miktarlar 0 (sıfır) olur.

Herhangi bir işlemin düzeltilmesi gerekmiyorsa, bunları taslak düzeltme faturasından kaldırabilirsiniz. Yalnızca kısmi miktarı ters çevirmek veya geri döndürmek isterseniz, satır ayrıntısında **Miktar** alanını düzenleyebilirsiniz. Fatura satırı ayrıntısını açarsanız, orijinal fatura miktarını görebilirsiniz. Ardından, geçerli fatura miktarını, orijinal fatura miktarından az veya daha fazla olacak şekilde düzenleyebilirsiniz.

Düzeltme faturasını onaylandıktan sonra, orijinal faturalanmış satış fiili değeri tersine çevrilir ve yeni bir faturalanmış satış fiili değeri oluşturulur. Miktar azaltılırsa, fark faturalanmamış yeni bir satış fiili değeri oluşturulmasına neden olur. Örneğin, orijinal faturalanmış satış sekiz saat içinse ve düzeltme faturası satır ayrıntısı altı saatlik bir miktar içeriyorsa, PSA orijinal faturalanan satış satırını ters çevirir ve iki yeni fiili değer oluşturur:

- Altı saat için faturalanmış satış fiili değeri.
- Kalan iki saat için faturalanmamış bir satış fiili değeri. Müşteriyle yapılan anlaşmaya bağlı olarak bu hareket daha sonra faturalanabilir veya borçlandırılamaz olarak işaretlenebilir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]