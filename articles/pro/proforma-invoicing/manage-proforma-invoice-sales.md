---
title: Proforma proje faturalarını yönetme
description: Bu konu, proforma proje faturalarıyla çalışma hakkında bilgi sağlar.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f14cf9d5ee25247500180081b8f407ee311db481a5ef5eac330e75d45baba54a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997450"
---
# <a name="manage-a-proforma-project-invoice"></a>Proforma proje faturalarını yönetme 

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Dynamics 365 Project Operations'ta proforma faturalar, Dynamics 365 Sales'teki faturalar için uzantı olarak oluşturulur. Ancak Faturalandırma sırasında Sales ve Project Operations arasındaki faturalama işleminde çok çeşitli farklılıklar vardır. Örneğin, Project Operations'ta **fatura listesi** sayfasından yeni bir fatura oluşturmak mümkün değildir ancak satış içinde bunu yapmak mümkündür. Bu farklılıklar ve uzantılar, bir satış siparişi için tipik bir faturadan farklı olan projeler için faturalama işlemlerini desteklemek için kullanılan yerdir.

> [!IMPORTANT]
> Farklardan dolayı, Sales ve Project Operations'da faturaları birbirinin yerine kullanmayın.

## <a name="invoice-header"></a>Fatura başlığı

Aşağıdaki bilgiler, Project Operations'da bir Proforma fatura başlığında bulunur.

| Alan | Konum | Veri Akışı Açıklaması | Aşağı yönlü etki |
| --- | --- | --- | --- |
| **Fatura kimliği** | **Özet** sekmesi | Proforma faturası oluşturulduğunda kimlik otomatik olarak oluşturulur. Düzenlemeden kilitlenen salt okunur bir alan. | Bu alan, her proforma faturasının başvurusu olarak kullanılır. |
| **Ad** | **Özet** sekmesi | Varsayılan olarak proje sözleşmesi adına ayarlayın. Bu alan Kullanıcı tarafından düzenlenebilir. | &nbsp;  |
| **Para Birimi** | **Özet** sekmesi | Varsayılan olarak proje sözleşmesi para birimine ayarlayın. Düzenlemeden kilitlenen salt okunur bir alan. |&nbsp; |
| **Fiyat listesi** | **Özet** sekmesi | Varsayılan olarak proje sözleşmesi fiyat listesine ayarlayın. Düzenlemeden kilitlenen salt okunur bir alan. | &nbsp; |
| **Fırsat** | **Özet** sekmesi | Bağlantılı fırsata başvuru. Düzenlemeden kilitlenen salt okunur bir alan. | &nbsp;  |
| **Sözleşme** | **Özet** sekmesi | Bağlantılı proje sözleşmesine başvuru. Düzenlemeden kilitlenen salt okunur bir alan. | &nbsp; |
| **Müşteri** | **Özet** sekmesi | Bağlantılı proje sözleşmesine başvuru. Düzenlemeden kilitlenen salt okunur bir alan. |&nbsp;  |
| **Açıklama** | **Özet** sekmesi | Faturayı açıklayan metin alanı. Bu alan Kullanıcı tarafından düzenlenebilir. | &nbsp; |
| **Fatura** ve ilgili alanlar | **Özet sekmesi** | Varsayılanlar Proje sözleşmesi müşterisi 'den ayarlanır. Bu alan Kullanıcı tarafından düzenlenebilir.  | &nbsp; |
| **Statü** | **Özet** sekmesi | Şu seçenekleri ayarlar: **Etkin**, **kapanmış**, **ödenmiş** ve **iptal edilmiş** ve Kullanıcı tarafından düzenlenebilir. | Project Operations için desteklenmeyen durumlar **kapandı** ve **iptal edildi**. </br> Fatura oluşturulduğunda durum **etkin** olarak ayarlanır. </br>Durum yalnızca fatura onaylandıktan sonra **ödeme** olarak ayarlanmalıdır. |
| **Proje Faturası Durumu** | **Özet** sekmesi | Şu seçenekleri ayarlar: **Taslak**, **incelemede** ve **Onaylanmış**; ve Kullanıcı tarafından düzenlenebilir. | Hem **taslak** hem de **Gözden geçirme durumunda** fatura düzenlenebilir. Fatura onaylandıktan sonra düzenlenemez. |
| **Ayrıntı Tutarı** | **Özet** sekmesi | Tüm fatura satırlarındaki avanslar ve kesintiler sonrası tutarların toplamı. Düzenlemeden kilitlenen salt okunur bir alan. | Bu alan, son tutarı hesaplamak için kullanılır. |
| **İndirim (%)** | **Özet** sekmesi | Bu alan, bir iskonto yüzdesi girmek üzere düzenlenebilir. Bu alan Project Operations işlevselliği tarafından desteklenmiyor. | Bu desteklenmeyen bir alandır. |
| **İskonto Tutarı** | **Özet** sekmesi | Bu alan, bir iskonto tutarı girmek üzere düzenlenebilir. Bu alan Project Operations işlevselliği tarafından desteklenmiyor. | Bu desteklenmeyen bir alandır. |
| **Navlun Öncesi Tutar** | **Özet sekmesi** | İndirimler uygulandıktan sonra toplam fatura tutarı. Düzenlemeden kilitlenen salt okunur bir alan. | Bu alan, son tutarı hesaplamak için kullanılır. |
| **Navlun Tutarı** | **Özet** sekmesi | Bu alan, bir navlun tutarı girmek üzere düzenlenebilir. Bu alan Project Operations işlevselliği tarafından desteklenmiyor. | Bu desteklenmeyen bir alandır. |
| **Toplam Vergi** | **Özet** sekmesi | Faturadaki tüm fatura satırlarından toplam vergi. Düzenlemeden kilitlenen salt okunur bir alan. | Yok. |
| **Toplam Tutar** | **Özet** sekmesi | İskonto ve vergilerin ardından tutarın toplamı. | Toplam, müşterinin ödemesi gerekli olan tutardır. |
## <a name="project-based-invoice-lines"></a>Proje tabanlı fatura satırları

Project Operations, her proje sözleşme satırı için her zaman bir fatura satırı vardır. Fatura satırı, hiçbir fiili değer olmasa da oluşturulur. Aşağıdaki bilgiler, bir Proforma fatura satırında bulunur.

| Alan | Konum | Veri Akışı Açıklaması | Aşağı yönlü etki |
| --- | --- | --- | --- |
| **Fatura kimliği** | **Genel** sekmesi | Fatura kimliğine başvuru. Düzenlemeden kilitlenen salt okunur bir alan. | Fatura kimliği bağlantısı, fatura başlığına geri gitmek için kullanılabilir. |
| **Ad** | **Genel** sekmesi | Sözleşme satırı adından varsayılan olarak ayarlanan fatura satırının adı. Bu alan Kullanıcı tarafından düzenlenebilir. | &nbsp; |
| **Project** | **Genel** sekmesi | İlgili proje sözleşmesi satırındaki Proje. Düzenlemeden kilitlenen salt okunur bir alan. | Projeye gitmek için proje bağlantısı kullanılabilir. |
| **Faturalama Yöntemi** | **Genel** sekmesi | İlgili proje sözleşmesi satırındaki fatura yöntemi. Düzenlemeden kilitlenen salt okunur bir alan. | &nbsp; |
| **Sözleşme Satırı Tutarı** | **Genel** sekmesi | İlgili proje sözleşme satırındaki sözleşme tutarı. Düzenlemeden kilitlenen salt okunur bir alan. | &nbsp; |
| **Bu Tarihe Kadar Faturalananlar** | **Genel** sekmesi | Bu faturanın tüm fatura satırı ayrıntılarındaki tutarların toplamı. Düzenlemeden kilitlenen salt okunur bir alan. | &nbsp; |
| **Tutar** | **Genel** sekmesi | Bu faturanın tüm fatura satırı ayrıntılarındaki tutarların toplamı. Düzenlemeden kilitlenen salt okunur bir alan. | Bu alan, fatura üst bilgisindeki son tutarı hesaplamak için kullanılır. |
| **Vergi** | **Genel** sekmesi | Bu fatura satırının tüm fatura satırı ayrıntılarındaki vergi tutarların toplamı. Düzenlemeden kilitlenen salt okunur bir alan. | Bu alan, fatura üst bilgisindeki son vergi tutarı hesaplamak için kullanılır. |
| **Toplam Tutar** | **Genel** sekmesi | Bu fatura satırının tüm ücretlendirilebilir fatura satırı ayrıntılarındaki tutarların (**Vergi + Tutarlar**) toplamı. Düzenlemeden kilitlenen salt okunur bir alan. | Bu alan, fatura üst bilgisindeki son tutarı hesaplamak için kullanılır. |


## <a name="invoice-line-details"></a>Fatura Satırı Ayrıntıları

Bir proje faturasındaki her fatura satırı fatura satırı ayrıntılarını içerir. Bu satır ayrıntıları fatura satırı ile referansta bulunulan sözleşme satırıyla ilgili olarak faturalandırılmadığı satış fiili değerleri ve kilometre taşları ile ilgilidir. Tüm bu hareketler **Faturaya hazır** olarak işaretlenir.

**Zaman ve Malzeme Faturası** satırı için fatura satırı ayrıntıları **Fatura Satırı** sayfasında şu gruplara ayrılır: **Borçlandırılabilir**, **Borçlandırılamaz** ve **Ücretsiz**. **Borçlandırılabilir fatura satırı** ayrıntıları fatura satır toplamına kadar bilgi ekleyin. **Ücretsiz** ve **Borçlandırılamayan Gerçek Değerler**, fatura satırı toplamına ulaşmıyor.

**Sabit Fiyat Faturası** satırı için, fatura satırı ayrıntıları, ilgili sözleşme satırında **Faturalamak için hazır** olarak işaretlenmiş kilometre taşlarından oluşturulur. Bir kilometre taşından fatura satırı ayrıntısı oluşturulduktan sonra, kilometre taşına ait faturalama durumu, **oluşturulan müşteri faturasına** güncelleştirilir.

### <a name="edit-invoice-line-details"></a>Fatura Satırı Ayrıntılarını düzenle

Aşağıdaki alanlar, faturalanmamış bir satış fiili ile desteklenen bir fatura satırı ayrıntısı ile kullanılabilir:

| Alan | Veri Akışı Açıklaması | Aşağı yönlü etki |
| --- | --- | --- |
| **Fatura Satırı** | **Fatura satırı kimliğine** başvuru. Salt Okunur alan, düzenleme için kilitli. | Bu bağlantı, fatura başlığına geri gitmek için kullanılabilir. |
| **Açıklama** | Fatura satırı ayrıntısının açıklaması. Varsayılan olarak , **zaman girişindeki** **dahili Yorumlar** alanında ve **gider girişindeki** **Açıklama** alanından ayarlanır. Alan Kullanıcı tarafından düzenlenebilir.| &nbsp; |
| **Harici Açıklama** | Fatura satırı ayrıntısının açıklaması. Varsayılan olarak , **zaman girişindeki** **Harici Yorumlar** alanında ve **gider girişindeki** **Açıklama** alanından ayarlanır. Alan Kullanıcı tarafından düzenlenebilir. | Bu açıklama, müşteriye gönderilecek yazdırılmış faturada ne olacağını belirlemek için kullanılabilir. Project Operations'da, bir Proforma faturası fatura için yazdırma ayarlarını yapılandırmak için gerekli olan tüm işlevselliğe sahip değildir. |
| **Başlangıç Tarihi** | Varsayılan olarak kaynak gerçek tarafından ayarlanır. Düzenlemeden kilitlenen salt okunur bir alan. | Bu alan, kaynak fiili tarafından yedeklenmeyen yeni bir fatura satırı ayrıntısı üzerinde düzenlenebilir. |
| **Project** | Varsayılan olarak kaynak gerçek tarafından ayarlanır. Düzenlemeden kilitlenen salt okunur bir alan. | İlgili sözleşme satırındaki projeye varsayılan olarak ayarlayın. |
| **Görev** | Varsayılan olarak kaynak gerçek tarafından ayarlanır. Düzenlemeden kilitlenen salt okunur bir alan. | Bu alan, kaynak fiili tarafından yedeklenmeyen yeni bir fatura satırı ayrıntısı üzerinde düzenlenebilir. Bir açılan liste, ilgili proje sözleşmesi satırıyla ilişkili tüm görevleri gösterir.  |
| **İşlem kategorisi** | Varsayılan olarak kaynak gerçek tarafından ayarlanır. Düzenlemeden kilitlenen salt okunur bir alan. | Alan, kaynak fiili tarafından yedeklenmeyen yeni bir fatura satırı ayrıntısı üzerinde düzenlenebilir. |
| **Rol** | Varsayılan olarak kaynak gerçek tarafından ayarlanır. Düzenlemeden kilitlenen salt okunur bir alan. | Alan, kaynak fiili tarafından yedeklenmeyen yeni bir fatura satırı ayrıntısı üzerinde düzenlenebilir. |
| **Ayrılabilir Kaynak** | Varsayılan olarak kaynak gerçek tarafından ayarlanır. Düzenlemeden kilitlenen salt okunur bir alan. | Alan, kaynak fiili tarafından yedeklenmeyen yeni bir fatura satırı ayrıntısı üzerinde düzenlenebilir. |
| **Kaynak Belirleme Birimi** | Varsayılan olarak kaynak gerçek tarafından ayarlanır. Düzenlemeden kilitlenen salt okunur bir alan. | Alan, kaynak fiili tarafından yedeklenmeyen yeni bir fatura satırı ayrıntısı üzerinde düzenlenebilir. |
| **Miktar** | Varsayılan olarak kaynak gerçek tarafından ayarlanır. Düzenlemeden kilitlenen salt okunur bir alan. | Alan, kaynak fiili tarafından yedeklenmeyen yeni bir fatura satırı ayrıntısı üzerinde düzenlenebilir. |
| **Birim Çizelgesi** | Zaman için fatura satır ayrıntısı için bu her zaman zaman olarak ayarlanmış ve düzenlenemez. Giderler için bu, varsayılan olarak kaynak gider fiili öğesinden ayarlanır. Düzenlemeden kilitlenen salt okunur bir alan. | Gerçek tarafından yedeklenmeyen yeni bir fatura satır ayrıntısı için varsayılan olarak **saate** göre ayarlayın. |
| **Birim** | Varsayılan olarak kaynak gerçek tarafından ayarlanır. Düzenlemeden kilitlenen salt okunur bir alan. | Alan, kaynak fiili tarafından yedeklenmeyen yeni bir fatura satırı ayrıntısı üzerinde düzenlenebilir. |
| **Fiyat** | Varsayılan olarak kaynak gerçek tarafından ayarlanır. Düzenlemeden kilitlenen salt okunur bir alan. | Alan, kaynak fiili tarafından yedeklenmeyen yeni bir fatura satırı ayrıntısı üzerinde düzenlenebilir. Değer girilmezse, **kaydetmeden** sonra varsayılan olarak ayarlanır. |
| **Para Birimi** | Varsayılan olarak kaynak gerçek tarafından ayarlanır. Düzenlemeden kilitlenen salt okunur bir alan. | Gerçek yedekleme olmadan yeni bir fatura ayrıntısı oluştururken fatura başlığından varsayılan olarak ayarlanır.  Düzenlemeden kilitlenen salt okunur bir alan. |
| **Tutar** | Varsayılan olarak kaynak gerçek tarafından ayarlanır. Düzenlemeden kilitlenen salt okunur bir alan. | Gerçek yedek olmadan yeni bir fatura ayrıntısı yaratılırken **miktar\*fiyatı** olarak hesaplanır. **Kaydettikten** sonra hesaplanır. Düzenlemeden kilitlenen salt okunur bir alan. |
| **Vergi** | Varsayılan olarak kaynak gerçek tarafından ayarlanır. Alan Kullanıcı tarafından düzenlenebilir | Bu alan, gerçek bir yedek olmadan yeni bir fatura satır ayrıntısı oluştururken Kullanıcı tarafından düzenlenebilir. |
| **Toplam Tutar** | Hesaplanan bir alan, **Tutar + Vergi** olarak hesaplanır. Düzenlemeden kilitlenen salt okunur bir alan. | &nbsp; |
| **Fatura Türü** | Varsayılan olarak kaynak gerçek tarafından ayarlanır. Alan Kullanıcı tarafından düzenlenebilir. | **Borçlandırılabilir** satır, fatura satır toplamına eklenir. **Tamamlayıcı** ve **borçlandırılamayan**, fatura satır toplamndan hariç kalır. |
| **Ürün Seç** | Kaynak gerçek değerinden varsayılan olarak ayarlanan bu alan salt okunurdur. | Yedekleme gerçek değeri olmadan yeni bir fatura satırı oluşturduğunuzda bu alan düzenlenemez. |
| **Ürün** | Kaynak gerçek değerinden varsayılan olarak ayarlanan bu alan salt okunurdur. | Yedekleme gerçek değeri olmadan yeni bir fatura satırı oluştursanız bu satırın düzenlenebilmesi için **Ürün Seç** alanının **Varolan ürün** olarak ayarlanması gerekir. |
| **Ürün Adı** | Kaynak gerçek değerinden varsayılan olarak ayarlanan bu alan salt okunurdur. | Ürün kimliğinin katalogdan seçildiği yeni bir fatura satır ayrıntısında bu alan ürün adına ayarlanır. Serbest ürünler için bu alan serbest ada ayarlanmıştır. |
| **Serbest Ürün Açıklaması** | Kaynak gerçek değerinden varsayılan olarak ayarlanan bu alan salt okunurdur. | Yedekleme gerçek değeri olmadan yeni bir fatura satır ayrıntısı oluşturduğunuzda ürün için bir serbest açıklaması ekleyebilirsiniz. |
| **İşlem Türü** | Varsayılan olarak kaynak gerçek tarafından ayarlanır. Düzenlemeden kilitlenen salt okunur bir alan. | Gerçek yedek olmadan yeni bir **Fatura satırı ayrıntısı** oluştururken varsayılan olarak **Faturalanan Satışlar** ve kilitli olarak ayarlayın.  |
| **İşlem Sınıfı** | Varsayılan olarak kaynak gerçek tarafından ayarlanır. Düzenlemeden kilitlenen salt okunur bir alan. | Kullanıcının yedekleme gerçek değeri olmadan **Fatura satırı ayrıntısı** oluştururken **Zaman**, **Gider**, **Malzeme** veya **Ücret** ayrıntı satırı oluşturmasına bağlı olarak varsayılan olarak ayarlanır. Düzenlemeye karşı kilitlendi. |

Aşağıdaki alanlar,kilometre taşı ile desteklenen bir fatura satırı ayrıntısı ile kullanılabilir:

| Alan | Veri Akışı Açıklaması | Aşağı yönlü etki |
| --- | --- | --- |
| **Fatura Satırı** | **Fatura satırı kimliğine** başvuru. Düzenlemeden kilitlenen salt okunur bir alan. | Bu bağlantı, fatura başlığına geri gitmek için kullanılabilir. |
| **Açıklama** | Fatura satırı ayrıntısının açıklaması. Varsayılan olarak kaynak kilometre taşına ait açıklama olarak ayarlayın. | &nbsp; |
|**Harici Açıklama** | Kaynak kilometre taşına ait açıklama üzerinden varsayılan olarak ayarlanan fatura satırı detayına ilişkin açıklama. | Bu alan, müşteriye gönderilecek yazdırılmış faturada ne olacağını belirlemek için kullanılabilir. Project Operations'da, bir Proforma faturası fatura için yazdırma ayarlarını yapılandırmak için gerekli olan tüm işlevselliğe sahip değildir. |
| **Başlangıç Tarihi** | Varsayılan olarak kaynak **kilometre taşına** ait kilometre taşı tarihinden göre ayarlayın. Düzenlemeden kilitlenen salt okunur bir alan. | &nbsp; |
| **Project** | Varsayılan olarak kaynak kilometre taşı tarafından ayarlanır. Düzenlemeden kilitlenen salt okunur bir alan. | &nbsp; |
| **Görev** | Varsayılan olarak kaynak kilometre taşı tarafından ayarlanır. Düzenlemeden kilitlenen salt okunur bir alan. | &nbsp; |
| **İşlem kategorisi** | Düzenlemeden kilitlenen salt okunur bir alan. | &nbsp; |
| **Rol** | Düzenlemeden kilitlenen salt okunur bir alan. | &nbsp; |
| **Ayrılabilir Kaynak** | Düzenlemeden kilitlenen salt okunur bir alan. | &nbsp; |
| **Kaynak Belirleme Birimi** | Düzenlemeden kilitlenen salt okunur bir alan. | &nbsp; |
| **Birim Çizelgesi** | Düzenlemeden kilitlenen salt okunur bir alan. | &nbsp; |
| **Birim** | Düzenlemeden kilitlenen salt okunur bir alan. | &nbsp; |
| **Fiyat** | Varsayılan olarak kaynak kilometre taşına ait tutar olarak ayarlayın. Düzenlemeden kilitlenen salt okunur bir alan. | &nbsp; |
| **Para Birimi** | Varsayılan olarak kaynak kilometre taşı tarafından ayarlanır. Düzenlemeden kilitlenen salt okunur bir alan. |&nbsp; |
| **Tutar** | Varsayılan olarak kaynak kilometre taşına ait tutar olarak ayarlayın. Düzenlemeden kilitlenen salt okunur bir alan. | &nbsp; |
| **Vergi** | Varsayılan olarak kaynak kilometre taşına ait vergi tutar olarak ayarlayın. Düzenlemeden kilitlenen salt okunur bir alan. | &nbsp; |
| **Toplam Tutar** | Varsayılan olarak kaynak kilometre taşına ait genişletilmiş tutar olarak ayarlayın. Alan Kullanıcı tarafından düzenlenebilir | &nbsp; |
| **Fatura Türü** | Varsayılan olarak her zaman **Borçlandırılabilir** olarak ayarlayın. Düzenlemeden kilitlenen salt okunur bir alan. | &nbsp; |
| **İşlem Türü** | Varsayılan olarak kaynak kilometre taşı tarafından ayarlanır. Düzenlemeden kilitlenen salt okunur bir alan. | &nbsp; |
| **İşlem Sınıfı** | Varsayılan olarak kaynak kilometre taşı tarafından ayarlanır. Düzenlemeden kilitlenen salt okunur bir alan. | &nbsp; |

### <a name="create-new-invoice-line-details"></a>Yeni Fatura Satırı Ayrıntıları oluştur

Zaman ve malzeme fatura satırlarında, yeni fatura satırı ayrıntıları oluşturabilirsiniz. Bu fatura satırı ayrıntıları gerçek tarafından yedeklenmez. Zaman ve malzeme faturası satırının fatura satırındaki sözleşme satırına dahil edilen hareket sınıfları için yeni bir fatura satırı ayrıntısı oluşturmak üzere **Yeni**'yi seçebilirsiniz.

## <a name="refresh-invoice-transactions"></a>Fatura İşlemlerini Yenile

Fatura oluşturulduktan sonra gelen fiili değerleri varsa, bu fiili değerleri faturaya dahil edebilirsiniz.

1. **Faturalama biriktirme listesi** görünümünde verileri **Faturaya hazır** olarak işaretleyin.   
2. Taslak proforma faturayı açın ve şerit **Eylemleri**'nde **Fatura satırı hareketlerini Yenile**'yi tıklatın.

  Bu, tarihlenen ve **Faturaya hazır** olarak işaretlenen tüm fiili için fatura satırı ayrıntılarını oluşturur ancak faturaya dahil edilmez.

## <a name="product-based-invoice-lines"></a>Ürün tabanlı fatura satırları

Project Operations'ta, proje tabanlı fatura satırlarıyla birlikte, herhangi bir projeye veya tüm projelere uygulanabilen ürünler için fatura satırları oluşturabilirsiniz. Bu fatura satırları ürün tabanlı sözleşme satırları olarak oluşturulur ve bunlar, faturaya hazır olarak işaretlendikten sonra, ürün tabanlı fatura satırları olarak eklenir.

Ürün tabanlı fatura satırlarını ekledikten sonra, bunlar değiştirilemez. Ancak bunlar taslak proforma faturadan silinebilir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
