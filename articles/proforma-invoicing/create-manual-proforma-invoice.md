---
title: Proforma faturalar
description: Bu konu, Project Operations'ta proforma faturalar hakkında bilgi sağlar.
author: rumant
manager: AnnBe
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b143ba286f25ecb23fea09a85bca06543f7f55ff
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866885"
---
# <a name="proforma-invoices"></a>Proforma faturalar

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Proforma faturalama, müşteri faturaları oluşturmadan önce proje yöneticilerine ikinci bir onay düzeyi sağlar. Proje takım üyelerinin gönderdiği zaman, gider ve malzeme girişleri onaylandığında onayın ilk düzeyi tamamlanır. Onaylı proforma faturaları, Project Operations'ın Proje Muhasebesi modülünden kullanılabilir. Proje muhasebecileri; satış vergisi, muhasebe ve fatura düzeni gibi ek güncelleştirmeler gerçekleştirebilir.


## <a name="creating-project-invoices"></a>Proje faturaları oluşturma

Proje faturaları tek tek veya toplu olarak oluşturulabilir. El ile oluşturulabilirler veya otomatik çalıştırmalar halinde oluşturulmak üzere yapılandırılabilirler.

### <a name="manually-create-project-invoices"></a>Proje faturalarını el ile oluşturma 

**Proje Sözleşmeleri** listesi sayfasından, her proje sözleşmesi için ayrı olarak proje faturaları oluşturabilir veya birden çok proje sözleşmesi için toplu olarak fatura oluşturabilirsiniz.

Belirli bir proje sözleşmesi için fatura oluşturmak üzere bu adımı izleyin.

- **Proje Sözleşmeleri** listesi sayfasında bir proje sözleşmesi açın ve sonra **Fatura oluştur** 'u seçin.

    **Faturalamaya Hazır** durumuna sahip seçili proje sözleşmesine ilişkin tüm işlemler için bir fatura oluşturulur. Bu hareketler zaman, giderler, malzemeler, kilometre taşları ve diğer faturalanmamış satış yevmiye defteri satırlarını içerir.

Faturaları toplu olarak oluşturmak için bu adımları izleyin.

1. **Proje Sözleşmeleri** listesi sayfasında, fatura oluşturmanız gereken bir veya daha fazla proje sözleşmesi seçin ve ardından **Proje Faturaları Oluştur**'u seçin.

    Bir uyarı iletisi, faturalar oluşturulmadan önce bir gecikme olabileceği konusunda sizi uyarır. İşlem de gösterilir.

2. İleti kutusunu kapatmak için **Tamam**'ı seçin.

    **Faturalamaya Hazır** durumuna sahip sözleşme satırında tüm işlemler için bir fatura oluşturulur. Bu hareketler zaman, giderler, malzemeler, kilometre taşları ve diğer faturalanmamış satış yevmiye defteri satırlarını içerir.

3. Oluşturulan faturaları görüntülemek için **Satış** \> **Faturalama** \> **Faturalar**'a gidin. Her proje sözleşmesi için bir fatura görürsünüz.

### <a name="set-up-automated-creation-of-project-invoices"></a>Otomatik proje faturaları oluşturmayı ayarlama 

Otomatik fatura çalıştırmayı yapılandırmak için bu adımları izleyin.

1. **Ayarlar** \> **Toplu işler**'e gidin.
2. Bir toplu iş oluşturun ve **Project Operations Fatura Oluştur** olarak adlandırın. Toplu işin adı "Faturaları oluştur" terimini içermelidir.
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
> Toplu faturalama yalnızca fatura zamanlamalarında yapılandırılan proje sözleşme satırlarında çalışır. Sabit fiyatlı fatura yöntemine sahip bir sözleşme satırının kilometre taşları yapılandırılmış olmalıdır. Zaman ve malzeme faturalama yöntemi içeren bir proje sözleşmesi satırı, ayarlanmış bir tarih tabanlı fatura çizelgesine gereksinim duyar. Aynı şekilde, proje tabanlı bir sözleşme satırı için de geçerlidir.      
 
### <a name="edit-a-draft-invoice"></a>Taslak bir faturayı düzenleme

Bir taslak proje faturası oluşturduğunuzda, zaman, gider ve malzeme kullanımı girişleri onaylandığında oluşturulan tüm faturalanmamış satış işlemleri faturaya alınır. Fatura hala taslak aşamasındayken aşağıdaki ayarlamaları yapabilirsiniz:

- Fatura satırı ayrıntılarını silmek veya düzenlemek.
- Miktarı ve faturalandırma türünü düzenlemek ve ayarlamak.

Bir faturayı onaylamak için **Onayla**'yı seçin. Onayla eylemi tek yönlü bir eylemdir. **Onayla**'yı seçtiğinizde, sistem faturayı salt okunur yapar ve her fatura satırı için her fatura satırı ayrıntısından faturalanan satış fiili değerleri oluşturur. Fatura satırı ayrıntısı faturalanmamış bir satış fiili değerine başvuruyorsa sistem faturalanmamış satış fiili değerini de tersine çevirir. (Bir zaman veya gider girişinden oluşturulan tüm fatura satırı ayrıntıları, faturalandırmamış bir satış fiili değerine başvuracaktır.) Genel muhasebe tümleştirme sistemleri, bu geri çevirme işlemini, süren proje işlerini (WIP) muhasebe amacıyla tersine çevirmek için kullanabilir.

### <a name="correct-a-confirmed-invoice"></a>Onaylanmış faturayı düzeltme

Onaylanmış faturalar düzenlenebilir (düzeltilebilir). Onaylı bir faturayı düzeltirken, yeni bir taslak düzeltme faturası oluşturulur. Orijinal faturadaki tüm hareketleri ve miktarları tersine çevirmek istediğiniz varsayıldığından, bu düzeltme faturası orijinal faturadaki tüm işlemleri içerir ve üzerindeki tüm miktarlar 0 (sıfır) olur.

Herhangi bir işlemin düzeltilmesi gerekmiyorsa, bunları taslak düzeltme faturasından kaldırabilirsiniz. Yalnızca kısmi miktarı ters çevirmek veya geri döndürmek isterseniz, satır ayrıntısında **Miktar** alanını düzenleyebilirsiniz. Fatura satırı ayrıntısını açarsanız, orijinal fatura miktarını görebilirsiniz. Ardından, geçerli fatura miktarını, orijinal fatura miktarından az veya daha fazla olacak şekilde düzenleyebilirsiniz.

Düzeltme faturasını onaylandıktan sonra, orijinal faturalanmış satış fiili değeri tersine çevrilir ve yeni bir faturalanmış satış fiili değeri oluşturulur. Miktar azaltılırsa, fark faturalanmamış yeni bir satış fiili değeri oluşturulmasına neden olur. Örneğin, orijinal faturalanmış satış sekiz saat içinse ve düzeltme faturası satır ayrıntısı altı saatlik bir miktar içeriyorsa, orijinal faturalanan satış satırı ters çevrilir ve iki yeni gerçek değer oluşturulur:

- Altı saat için faturalanmış satış fiili değeri.
- Kalan iki saat için faturalandırılmamış bir satış fiili değeri. Müşteriyle yapılan anlaşmaya bağlı olarak bu hareket daha sonra faturalanabilir veya borçlandırılamaz olarak işaretlenebilir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
