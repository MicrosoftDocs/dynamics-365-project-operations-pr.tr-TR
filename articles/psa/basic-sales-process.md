---
title: Satış süreçleri
description: Bu konu, temel satış süreçleri hakkında bilgi sağlar.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 5f01ba14baa0a2378b0a230a46aed3a682342ce6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014230"
---
# <a name="sales-processes"></a>Satış süreçleri

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Proje tabanlı bir kuruluşta kullanılan satış süreçleri, ürün tabanlı bir kuruluşta kullanılan satış süreçleriyle farklılık gösterir. Bu fark, proje tabanlı kuruluşların satış döngülerinin uzun olmasından ve her bir anlaşma için teklifleri analiz etmek ve oluşturmak üzere özel tahmin teknikleri gerektirmesinden kaynaklanır. Dynamics 365 Project Service Automation, Dynamics 365 Sales'de satış işleminde kullanılan aynı işlevlerden bazılarını kullanır. İşte bazı örnekler:

- Müşteri adayı varlığı, satış işlemini izlemek için kullanılır.
- Uygun müşteri adayları fırsat olarak izlenir. Satış süreci de fırsatla başlayabilir.
- Bir fırsat için tüm ilgili yapılara erişilir. Bu yapılar satış takımı, paydaşlar, olasılık, derecelendirme, satış aşamaları ve iş süreçlerini içerir.
- Fırsat için birden çok teklif oluşturulur.
- Bir teklif, bir satış siparişi oluşturmak için **Kazanıldı olarak kapatıldı** olarak işaretlenir. PSA'da, satış siparişi özelleştirilir ve proje sözleşmesi olarak adlandırılır.

Aşağıdaki resimde proje tabanlı bir kuruluştaki tipik bir satış işlemi gösterilmektedir.

> ![Proje tabanlı bir kuruluşta satış işlemi](media/basic-guide-1.png)

## <a name="estimating-a-sale"></a>Satış tahmini
Bir satışın değeri, önceden teslim edilmiş projeler ve projelerin karmaşıklığı temel alınarak tahmin edilebilir. Önceki projelerle ilgili uzantıları içeren projeler veya satıcı uzmanlığının yüksek olduğu ve tanınmış çalışma şablonları kullanılan projeler için, daha basit bir tahmin süreci kullanabilirsiniz. Daha karmaşık projelerin genellikle daha uzun satın alma süreci bulunur. Bu nedenle, satış tahmini işleminde daha fazla aşama vardır. Sürecin başlarında, satış takımı teklif edilen her farklı iş bileşeni için yüksek düzeyli bir tahmin oluşturmaya başlamak için hesap yöneticileri ve konu uzmanlarının (SME) girişini kullanır. Bu çalışma bileşenleri, teklif satırlarıyla gösterilir. 

Teklifin üst düzey tahminini oluşturabilirsiniz. Bu üst düzey tahmin en sonunda standartlaştırılmış proje şablonları kullanarak oluşturduğunuz proje planına dayalı daha ayrıntılı bir tahminle değiştirilir. Bu şablonlar bir zamanlama oluşturmanıza ve teklifte ve bileşenlerinde (teklif satırları) parasal değerleri belirlemenize yardımcı olur. 

Bir proje için birden çok teklif oluşturabilir ve bunları tek bir fırsat varlığı türünde gruplayabilirsiniz. Sonuç olarak, bu tekliflerden biri **Kazanıldı olarak kapatıldı** şeklinde işaretlenir ve broje sözleşmesi ya da iş beyanı (SOW) oluşturulur. Proje sözleşmesi, müşteri tarafından teslimat için kabul edilen her bileşen (sözleşme satırı) için sözleşme değerini içerir. Bir iş beyanı genellikle Microsoft Word belgesi olarak oluşturulur. Projenin teslimatı sırasında müşteriye gönderilen tüm faturalar proje sözleşmesine veya iş beyanına referansta bulunur.

Ayrıca, bir teklif kazanıldığında bir proje sözleşmesi oluşturulacak şekilde, bir fırsat varlık türü altında alternatif teklifler oluşturabilir veya sistemi ayarlayabilirsiniz. Bu durumda, proje sözleşme kaydına iş beyanını temsil eden bir Word belgesi ekleyebilirsiniz.

![Proje sözleşmesi oluşturmak için teklifi kapatma](media/basic-guide-2.png)

## <a name="configuring-the-sales-process"></a>Satış sürecini yapılandırma
Satış sürecinizi yapılandırmak için, Microsoft Dynamics 365 uygulamasında iş süreci akışlarını (BPF) kullanabilirsiniz. İş süreci akışları, satış personelinize şirketinizdeki tipik aşamalar arasında ilerlemek için kullanabildiği, destekli bir görsel arabirim sunar.

Örneğin, şirketiniz satış sürecinde aşağıdaki altı aşama bulunabilir:

1. Uygun Bul
2. Tahmin
3. Dahili inceleme
4. Sözleşme
5. Teslim Et
6. Kapat

Bu altı aşama, oluşturduğunuz her fırsat varlığı türünde genişletmeyi seçtiğiniz köşeli ayraçlarla (\>) gösterilir.

![Dynamics 365'te iş süreci yapılandırması](media/basic-guide-3.png)
 
Kuruluşunuz geliştikçe aynı anlaşmayı temsil etmek için farklı varlıklar kullanabilir. Satış sürecinin başlarında, bir anlaşma Fırsat varlığı ile temsil edilir. Zaman geçtikçe ve daha fazla ayrıntı ortaya çıktığında, bir veya daha fazla teklif oluşturmak için yüksek düzeyde tahminler kullanabilirsiniz. Bu tekliflerinden biri dahili ve müşteri paydaşları tarafından gözden geçirilirse, Teklif varlığı anlaşmayı temsil eder. Müşteri teklifi kabul ettikten sonra, bir proje sözleşmesi veya iş beyanı anlaşmayı temsil eder. Bu davranışı desteklemek için, iş süreci akışları yapılandırılır ve böylece süreçteki her aşama farklı bir veritabanı tablosuna bağlanır.

Satış sürecindeki **Uygun bul** aşaması bir Fırsat varlığıyla desteklenebilir. **Tahmin** ve **Dahili İnceleme** aşamaları bir Teklif varlığıyla desteklenebilir. **Sözleşme**, **Teslimat** ve **Kapatma** aşamaları, bir Proje Sözleşmesi varlığı tarafından desteklenebilir.

Anlaşmaşarı aşamalar arasında ilerlettiğinizde, süreç boyunca size yol göstermek için uygun varlık kaydını oluşturmanız istenir. Aşamalar koşullu olabilir. Örneğin, yalnızca teklif özel bir fiyat listesi kullanılması durumunda teklifin dahili olarak gözden geçirilmesini gerekli kılarsanız, bu koşulu iş sürecinin uygun aşamasında yapılandırabilirsiniz. Ardından **Dahili İnceleme** aşaması yalnızca özel fiyat listesi kullanan teklifler için gösterilir. Diğer tüm anlaşmalar ve teklifler için **Tahmin** aşamasının ardından **Sözleşme** aşaması gelir.

> [!NOTE]
> PSA'da Fırsat, Teklif, Sipariş ve Fatura varlıkları için belirli sayfalar vardır. Bu varlıklar için proje bilgileri sayfalarını kullanarak proje hizmeti fırsatları, teklifler, siparişler ve faturalar oluşturmanız gerekir. Kayıt oluşturmak için başka bir sayfa kullanırsanız, kaydı **Proje bilgileri** sayfasından açamazsınız. **Proje** bilgileri sayfasından bir kayıt açmak isterseniz, kaydı silip **Proje bilgileri** sayfasını kullanarak yeniden oluşturmanız gerekir. **Proje bilgileri** sayfasında, bu varlık türlerinin her biri için iş mantığı, kaydın **Tür** alanının doğru şekilde ayarlanmasını ve tüm zorunlu kavramların doğru şekilde başlatılmasını sağlar.

> ![Yeni sipariş için proje bilgileri](media/basic-guide-4.png)
 
## <a name="differences-between-project-service-automation-and-sales"></a>Project Service Automation ve Sales arasındaki farklar
PSA uygulamasındaki satış süreci, Sales'deki satış sürecinin temel yeteneklerini kullansa da, proje tabanlı kuruluşların iş uygulamalarındaki varyasyonlar nedeniyle bazı önemli farklılıklar vardır. İşte bazı örnekler:

- **Proje teklifleri** - Project Service Automation'da teklife bir tekliften proje sözleşmesi oluşturulduktan sonra kapanır. Sales'de bir teklifi kazandıktan sonra teklifi açık bir şekilde bırakabilirsiniz. Bu farkın nedeni, teklif ve proje sözleşmesi arasındaki bir eşleşmenin proje tabanlı kuruluşlar açısından için daha iyi olmasıdır. 
- **Etkinleştirme ve düzeltmeler** – PSA'da, etkinleştirme ve düzeltmeler proje teklifleri için desteklenmez. Sales'de, ek düzenlemeleri engellemek için teklif kilitlenebilir.
- **Bir teklifi kaybedildi veya kazanıldı olarak kapatma** - PSA uygulamasında, bir proje teklifi kazanıldı veya kaybedildi olarak kapatıldığında, fırsat açık kalır. Fırsatın diğer tüm teklifleri kaybedildi olarak kapatılır. Sales'de bir teklif kazanıldı veya kaybedildi olarak kapatıldığında, kullanıcıdan fırsat üzerinde eylem yapması istenir. Kullanıcı girdisine bağlı olarak, temeldeki fırsat kapatılabilir veya açık bırakılabilir.

## <a name="tracking-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Satış döngüsündeki tekliflerde ve proje planlarında incelemeleri izleme
PSA'da, teklife yapılan düzeltmeleri izleyemezsiniz. Bunun yerine, varolan teklifi **Kaybedildi olarak kapatıldı** şeklinde işaretleyip yeni bir teklif oluşturmanız gerekir. PSA kullanarak bir teklifi kopyalayabilir veya proje tabanlı teklifi çoğaltabilirsiniz.

## <a name="tracking-comments-and-approvals-of-quotes-and-project-contracts"></a>Tekliflerin ve proje sözleşmelerinin açıklamalarını ve onaylarını izleme
Tekliflerin ve proje sözleşmelerini inceleme ve onaylama işlemini, kayıt duvarını ve gönderileri kullanarak yönetebilirsiniz. Kuurluşunuz, inceleme ve onaylama iş öğesi bildirimlerini atamak, yeniden yönlendirmek, ilerletmek ve yönetmek için özel iş akışları ve eklentiler oluşturabilir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]