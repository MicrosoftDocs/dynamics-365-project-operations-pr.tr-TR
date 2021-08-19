---
title: Satış sürecine genel bakış
description: Bu konu, temel satış süreçleri hakkında bilgi sağlar.
author: rumant
ms.date: 10/29/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 3bda8a11d0cb6fe97a3daa640bf95717ef9913000e6b1a28a0a27a35527dbf6f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991870"
---
# <a name="sales-process-overview"></a>Satış sürecine genel bakış

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Proje tabanlı bir kuruluşta kullanılan satış süreçleri, ürün tabanlı bir kuruluşta kullanılan satış süreçleriyle farklılık gösterir. Proje tabanlı kuruluşların satış döngülerinin uzun olmasından ve her bir anlaşma için teklifleri analiz etmek ve oluşturmak üzere özel tahmin teknikleri gerektirmesinden kaynaklanır. Dynamics 365 Project Operations, bir satış işleminde uygulanan aşağıdaki işlevlerden bazılarını kullanır:

- Müşteri adayı kaydı, satış işlemini izlemek için kullanılır.
- Uygun müşteri adayları fırsat olarak izlenir.
- Bir fırsat için tüm ilgili yapılara erişilebilirdir. Bu yapılar satış takımı, paydaşlar, olasılık, derecelendirme, satış aşamaları ve iş süreçlerini içerir.
- Fırsat için birden çok teklif oluşturulur.
- Bir teklif, bir satış siparişi oluşturmak için statüsü **Kazanıldı olarak kapatıldı** olarak değiştirilir. Project Operations'da, satış siparişi özelleştirilir ve proje sözleşmesi olarak adlandırılır.

## <a name="estimate-a-sale"></a>Satış tahmini
Bir satışın değeri, önceden teslim edilmiş projeler ve projelerin karmaşıklığı temel alınarak tahmin edilebilir. Önceki projelerle ilgili uzantıları içeren projeler veya satıcı uzmanlığının yüksek olduğu ve tanınmış çalışma şablonları kullanılan projeler için, daha basit bir tahmin süreci kullanabilirsiniz. Daha karmaşık projelerin genellikle daha uzun satın alma süreci bulunur. Bu nedenle, satış tahmini işleminde daha fazla aşama vardır. Sürecin başlarında, satış takımı teklif edilen her farklı iş bileşeni için yüksek düzeyli bir tahmin oluşturmak için hesap yöneticileri ve konu uzmanlarının (SME) girişini kullanır. Bu çalışma bileşenleri, teklif satırlarıyla gösterilir. 

Teklifin üst düzey tahminini oluşturabilirsiniz. Bu üst düzey tahmin en sonunda standartlaştırılmış proje şablonları kullanarak oluşturduğunuz proje planına dayalı daha ayrıntılı bir tahminle değiştirilir. Bu şablonlar bir zamanlama oluşturmanıza ve teklifte ve bileşenlerinde (teklif satırları) parasal değerleri belirlemenize yardımcı olur. 

Bir proje için birden çok teklif oluşturabilir ve bunları tek bir fırsat kaydına gruplayabilirsiniz. Sonuç olarak, bu tekliflerden biri **Kazanıldı olarak kapatıldı** şeklinde işaretlenir ve broje sözleşmesi ya da iş beyanı (SOW) oluşturulur. Proje sözleşmesi, müşteri tarafından teslimat için kabul edilen her bileşen (sözleşme satırı) için sözleşme değerini içerir. Bir iş beyanı genellikle Microsoft Word belgesi olarak oluşturulur. Projenin teslimatı sırasında müşteriye gönderilen tüm faturalar proje sözleşmesine veya iş beyanına referansta bulunur.

Ayrıca, bir teklif kazanıldığında bir proje sözleşmesi oluşturulacak şekilde, bir fırsat kaydı altında alternatif teklifler oluşturabilir veya sistemi ayarlayabilirsiniz. Bu durumda, proje sözleşme kaydına iş beyanını temsil eden bir Word belgesi ekleyebilirsiniz.

## <a name="configure-the-sales-process"></a>Satış sürecini yapılandırma
Satış sürecinizi yapılandırmak için, iş süreci akışlarını kullanabilirsiniz. Bu akışlar, satış sürecinin aşamalarında ileri doğru hareket etmek için kılavuzlu bir görsel arabirim sağlar.

Örneğin, şirketiniz satış sürecinde aşağıdaki altı aşama bulunabilir:

1. Nitelikli Hale Getir
2. Tahmin
3. Dahili inceleme
4. Sözleşme
5. Teslim Et
6. Kapat
 
Kuruluşunuz geliştikçe aynı anlaşmayı temsil etmek için farklı varlıklar kullanabilir. Satış sürecinin başlarında, bir anlaşma Fırsat varlığı ile temsil edilir. Zaman geçtikçe ve daha fazla ayrıntı ortaya çıktığında, bir veya daha fazla teklif oluşturmak için yüksek düzeyde tahminler kullanabilirsiniz. Bu tekliflerinden biri dahili ve müşteri paydaşları tarafından gözden geçirilirse, Teklif varlığı anlaşmayı temsil eder. Müşteri teklifi kabul ettikten sonra, bir proje sözleşmesi veya iş beyanı anlaşmayı temsil eder. Bu davranışı desteklemek için, iş süreci akışları yapılandırılır ve böylece süreçteki her aşama farklı bir veritabanı tablosuna bağlanır.

Satış sürecindeki **Uygun bul** aşaması bir Fırsat varlığıyla desteklenebilir. **Tahmin** ve **Dahili İnceleme** aşamaları bir Teklif varlığıyla desteklenebilir. **Sözleşme**, **Teslimat** ve **Kapatma** aşamaları, bir Proje Sözleşmesi varlığı tarafından desteklenebilir.

Anlaşmaşarı aşamalar arasında ilerlettiğinizde, süreç boyunca size yol göstermek için uygun varlık kaydını oluşturmanız istenir. Aşamalar koşullu olabilir. Örneğin, yalnızca teklif özel bir fiyat listesi kullanılması durumunda teklifin dahili olarak gözden geçirilmesini gerekli kılarsanız, bu koşulu iş sürecinin uygun aşamasında yapılandırabilirsiniz. Ardından **Dahili İnceleme** aşaması yalnızca özel fiyat listesi kullanan teklifler için gösterilir. Diğer tüm anlaşmalar ve teklifler için **Tahmin** aşamasının ardından **Sözleşme** aşaması gelir.

> [!NOTE]
> Project Operations'da Fırsat, Teklif, Sipariş ve Fatura varlık kayıtları için belirli sayfalar vardır. Bu kayıtları, bu varlıkların proje bilgileri sayfalarını kullanarak oluşturmanız gerekir. Aksi takdirde, **Proje bilgileri** sayfasından kayıtları açamazsınız. **Proje bilgileri** sayfasından bir kayıt açmak isterseniz , kaydı silip bu varlık türlerinin her birine yönelik iş mantığının, kaydın **Tür** alanının doğru şekilde ayarlanmasını ve tüm zorunlu kavramların doğru şekilde başlatılmasını sağlayan **Proje bilgileri** sayfasını kullanarak yeniden oluşturmanız gerekir.


## <a name="track-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Satış döngüsündeki tekliflerde ve proje planlarında incelemeleri izleme
Project Operations'da, teklife yapılan düzeltmeleri izleyemezsiniz. Bunun yerine, varolan teklifi **Kaybedildi olarak kapatıldı** şeklinde işaretleyip yeni bir teklif oluşturmanız gerekir. Bir teklifi kopyalayabilir veya proje tabanlı teklifi çoğaltabilirsiniz.

## <a name="track-comments-and-approvals-of-quotes-and-project-contracts"></a>Tekliflerin ve proje sözleşmelerinin açıklamalarını ve onaylarını izleme
Tekliflerin ve proje sözleşmelerini inceleme ve onaylama işlemini, kayıt duvarını ve gönderileri kullanarak yönetebilirsiniz. Kuruluşunuz, iş öğelerinin incelenmesi ve onaylanması ile ilgili bildirimlerini atamak, yeniden yönlendirmek, ilerletmek ve yönetmek için özel iş akışları ve eklentiler oluşturabilir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]