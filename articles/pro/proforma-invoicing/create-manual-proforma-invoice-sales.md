---
title: Proforma proje faturaları
description: Bu makalede, Project Operations'ta proforma proje faturalarına yönelik bilgiler sağlanmaktadır.
author: rumant
ms.date: 04/06/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8f028ec12aa3144a2c1bf13f6f8ce90c9de48519
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934574"
---
# <a name="proforma-project-invoices"></a>Proforma proje faturaları

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Proforma proje faturalama, müşteri faturaları oluşturmadan önce proje yöneticilerine ikinci bir onay düzeyi sağlar. Proje takım üyelerinin gönderdiği zaman, gider ve malzeme girişleri onaylandığında onayın ilk düzeyi tamamlanır.

Dynamics 365 Project Operations Lite Dağıtımı, müşteriye yönelik faturalar oluşturmak üzere tasarlanmamıştır. Aşağıdaki listede faturaların oluşturulamama nedenleri yer almaktadır:

- Vergi bilgilerini içermiyordur.
- Diğer para birimleri, faturalama para birimine dönüştürülemiyordur.
- Faturalar, yazdırılmak için doğru şekilde biçimlendirilemiyordur.

Bunun yerine, oluşturulan fatura tekliflerindeki bilgileri kullanan müşteriye yönelik faturalar oluşturmak için mali veya muhasebe sistemini kullanabilirsiniz.

## <a name="creating-project-invoices"></a>Proje faturaları oluşturma

Proje faturaları tek tek veya toplu olarak oluşturulabilir. El ile oluşturulabilirler veya otomatik çalıştırmalar halinde oluşturulmak üzere yapılandırılabilirler.

### <a name="manually-create-project-invoices"></a>Proje faturalarını el ile oluşturma 

**Proje Sözleşmeleri** listesi sayfasında, her proje sözleşmesi için ayrı olarak proje faturaları oluşturabilir veya birden çok proje sözleşmesi için toplu olarak fatura oluşturabilirsiniz.

   - Belirli bir proje sözleşmesi için fatura oluşturmak için **Proje Sözleşmeleri** listesi sayfasında, bir proje sözleşmesi açın ve ardından **Fatura Oluştur**'u seçin.

   **Faturalamaya Hazır** durumuna sahip seçili proje sözleşmesine ilişkin tüm işlemler için bir fatura oluşturulur. Bu hareketler arasında, zaman, masraf, malzeme, kilometre taşları, ürün tabanlı sözleşme satırları ve onaylanmış olabilecek diğer faturalanmamış satış yevmiye defteri satırları yer alır.

Faturaları toplu bir şekilde oluşturmak için:

1. **Proje Sözleşmeleri** listesi sayfasında, fatura oluşturmak için bir veya daha fazla proje sözleşmesi seçin ve ardından **Proje Faturaları Oluştur**'u seçin.
2. Bir uyarı iletisi, faturalar oluşturulmadan önce bir gecikme olabileceği konusunda sizi uyarır. İşlem de gösterilir. İleti kutusunu kapatmak için **Tamam**'ı seçin.

   **Faturalamaya Hazır** durumuna sahip sözleşme satırında tüm işlemler için bir fatura oluşturulur. Bu hareketler arasında, zaman, masraf, malzeme, kilometre taşları, ürün tabanlı sözleşme satırları ve onaylanmış olabilecek diğer faturalanmamış satış yevmiye defteri satırları yer alır.

3. **Satış** \> **Faturalama** \> **Faturalar**'a giderek oluşturulan faturaları görüntüleyebilirsiniz. Her proje sözleşmesi için bir fatura görürsünüz.

### <a name="set-up-automated-creation-of-project-invoices"></a>Otomatik proje faturaları oluşturmayı ayarlama 

Otomatik fatura çalıştırmayı yapılandırmak için bu adımları izleyin.

1. **Ayarlar** \> **Toplu işler**'e gidin.
2. Bir toplu iş oluşturun ve **Project Operations Fatura Oluştur** olarak adlandırın. Toplu işin adı "Faturaları oluştur" terimini içermelidir.
3. **İş türü** alanında **Hiçbiri**'ni seçin. Varsayılan olarak, **Günlük Sıklık** ve **Etkin** seçenekleri **Evet** olarak ayarlanır.
4. **İş Akışı Çalıştır**'ı seçin. **Kayıt Ara** iletişim kutusunda aşağıdaki iş akışlarını görürsünüz:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. **ProcessRunCaller**'ı ve ardından **Ekle**'yi seçin.
6. Sonraki iletişim kutusunda **Tamam**'ı seçin. **Uyku** iş akışının ardından **Süreç** iş akışı gelir.

    Ayrıca, adım 5'te **ProcessRunner**'ı seçebilirsiniz. Ardından **Tamam**'ı seçtiğinizde, bir **Süreç** iş akışının ardından bir **Uyku** iş akışı gelir.

**ProcessRunCaller** ve **ProcessRunner** iş akışları faturaları oluşturur. **ProcessRunCaller** **ProcessRunner**'ı çağırır. **ProcessRunner**, faturaları oluşturan iş akışıdır. Bu iş akışı, fatura oluşturulması için gereken tüm sözleşme satırlarından geçer ve faturaları oluşturur. Faturaların oluşturulması gereken sözleşme satırlarını belirlemek için, iş akışı sözleşme satırları için fatura çalıştırma tarihlerine bakar. Bir sözleşmeye ait olan sözleşme satırları aynı fatura çalıştırma tarihine sahipse, işlemler iki fatura satırı bulunan tek bir faturada birleştirilir. Fatura oluşturulacak bir işlem yoksa fatura oluşturulmaz.

**ProcessRunner** çalışması bittikten sonra, **ProcessRunCaller** öğesini çağırır, bitiş saati sağlar ve kapatılır. **ProcessRunCaller** daha sonra belirtilen bitiş saatinden itibaren 24 saat çalışan bir zamanlayıcı başlatır. Zamanlayıcının sonunda **ProcessRunCaller** kapatılır.

Fatura oluşturmaya yönelik toplu iş yinelenen bir iştir. Bu toplu iş birçok defa çalıştırılırsa işin birden çok kopyası oluşturulur ve hatalara yol açabilir. Bu sorunu çözmek için toplu işi yalnızca bir kez başlatın ve yalnızca çalışmayı durdurduğunda yeniden başlatın.

> [!NOTE]
> Toplu faturalama yalnızca fatura zamanlamalarında yapılandırılan proje sözleşme satırlarında çalışır. Sabit fiyatlı fatura yöntemine sahip bir sözleşme satırının kilometre taşları yapılandırılmış olmalıdır. Zaman ve malzeme faturalama yöntemi içeren bir proje sözleşmesi satırı, ayarlanmış bir tarih tabanlı fatura çizelgesine gereksinim duyar. Aynı şekilde, proje tabanlı bir sözleşme satırı için de geçerlidir.      
 
### <a name="edit-a-draft-invoice"></a>Taslak bir faturayı düzenleme

Bir taslak proje faturası oluşturduğunuzda, zaman ve gider girişleri onaylandığında oluşturulan tüm faturalandırılmamış satış işlemleri faturaya alınır. Fatura hala taslak aşamasındayken aşağıdaki ayarlamaları yapabilirsiniz:

- Fatura satırı ayrıntılarını silmek veya düzenlemek.
- Miktarı ve faturalandırma türünü düzenlemek ve ayarlamak.
- Zaman, gider, malzeme ve ücretleri faturadaki hareketler olarak doğrudan eklemek. Bu işlem sınıflarına izin veren bir sözleşme satırıyla eşlenmiş fatura satırı varsa, bu özelliği kullanabilirsiniz.

Bir faturayı onaylamak için **Onayla**'yı seçin. Bu eylem, tek yönlü bir eylemdir. **Onayla**'yı seçtiğinizde, fatura salt okunur olur ve her fatura satırı için her fatura satırı ayrıntısından faturalanan satış fiili değerleri oluşturur. Fatura satırı ayrıntısı faturalanmamış bir satış fiili değerine başvuruyorsa faturalanmamış satış gerçek değeri de tersine çevrilir. Bir zaman, masraf veya malzeme kullanımı girişinden oluşturulan tüm fatura satırı ayrıntıları, faturalanmamış bir satış gerçek değerine başvurur. Genel muhasebe tümleştirme sistemleri, bu tersine çevirme işlemini, devam eden (WIP) proje işlerini muhasebe amacıyla tersine çevirmek için kullanabilir.

### <a name="correct-a-confirmed-invoice"></a>Onaylanmış faturayı düzeltme

Onaylanan faturalar düzenlenebilir. Onaylı bir faturayı düzeltirken, yeni bir taslak düzeltme faturası oluşturulur. Orijinal faturadaki tüm hareketleri ve miktarları tersine çevirmek istediğiniz varsayıldığından, bu düzeltme faturası orijinal faturadaki tüm işlemleri içerir ve üzerindeki tüm miktarlar sıfır olur.

Düzeltilmesi gereken hareket yoksa bunları taslak düzeltme faturasından kaldırabilirsiniz. Yalnızca kısmi miktarı ters çevirmek veya geri döndürmek isterseniz, satır ayrıntısında **Miktar** alanını düzenleyebilirsiniz. Fatura satırı ayrıntısını açarsanız, orijinal fatura miktarını görebilirsiniz. Ardından, geçerli fatura miktarını, orijinal fatura miktarından az veya daha fazla olacak şekilde düzenleyebilirsiniz.

Düzeltme faturasını onaylandıktan sonra, orijinal faturalanmış satış fiili değeri tersine çevrilir ve yeni bir faturalanmış satış fiili değeri oluşturulur. Miktar azaltılırsa fark faturalanmamış yeni bir satış gerçek değeri oluşturulmasına neden olur. Örneğin, orijinal faturalanmış satış sekiz saat içinse ve düzeltme faturası satır ayrıntısı altı saatlik bir miktar içeriyorsa, orijinal faturalanan satış satırı ters çevrilir ve iki yeni gerçek değer oluşturulur:

- Altı saat için faturalanmış satış fiili değeri.
- Kalan iki saat için faturalanmamış bir satış fiili değeri. Müşteriyle yapılan anlaşmaya bağlı olarak bu hareket daha sonra faturalanabilir ya da borçlandırılamaz olarak işaretlenebilir.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
