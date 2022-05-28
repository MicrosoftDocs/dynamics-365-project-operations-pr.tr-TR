---
title: Proforma proje tabanlı faturaları yönetme
description: Bu konu, proforma proje tabanlı faturaları yönetme ve bunlarla çalışma hakkında bilgi sağlar.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c61b0d887ae35988f1765d40de0447aa5fd7efd4
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593774"
---
# <a name="manage-a-proforma-project-based-invoice"></a>Proforma proje tabanlı faturaları yönetme

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Dynamics 365 Project Operations'ta proforma faturalar, Dynamics 365 Sales'teki faturalar için uzantı olarak oluşturulur. Ancak Faturalandırma sırasında Sales ve Project Operations arasındaki faturalama işleminde çok çeşitli farklılıklar vardır. Örneğin, Project Operations'ta **fatura listesi** sayfasından yeni bir fatura oluşturmak mümkün değildir ancak satış içinde bunu yapmak mümkündür. Bu farklılıklar ve uzantılar, bir satış siparişi için tipik bir faturadan farklı olan projeler için faturalama işlemlerini desteklemek için kullanılan yerdir.

> [!IMPORTANT]
> Farklardan dolayı, Sales ve Project Operations'da faturaları birbirinin yerine kullanmayın.

## <a name="invoice-header"></a>Fatura başlığı

Aşağıdaki bilgiler, Project Operations'da bir Proforma fatura başlığında bulunur.

| Alan | Location | Açıklama |
| --- | --- | --- | 
| **Fatura kimliği** | **Özet** sekmesi | Proforma faturası oluşturulduğunda kimlik otomatik olarak oluşturulur. Düzenlemeden kilitlenen salt okunur bir alan. Bu alan, her proforma faturasının başvurusu olarak kullanılır. |
| **Ad** | **Özet** sekmesi | Varsayılan olarak proje sözleşmesi adına ayarlayın. Bu alan düzenlenebilir. | 
| **Para birimi** | **Özet** sekmesi | Varsayılan olarak proje sözleşmesi para birimine ayarlayın. Düzenlemeden kilitlenen salt okunur bir alan. |
| **Fiyat listesi** | **Özet** sekmesi | Varsayılan olarak proje sözleşmesi fiyat listesine ayarlayın. Düzenlemeden kilitlenen salt okunur bir alan. | 
| **Fırsat** | **Özet** sekmesi | Bağlantılı fırsata başvuru. Düzenlemeden kilitlenen salt okunur bir alan. | 
| **Sözleşme** | **Özet** sekmesi | Bağlantılı proje sözleşmesine başvuru. Düzenlemeden kilitlenen salt okunur bir alan. | 
| **Müşteri** | **Özet** sekmesi | Bağlantılı proje sözleşmesine başvuru. Düzenlemeden kilitlenen salt okunur bir alan. |
| **Açıklama** | **Özet** sekmesi | Faturayı açıklayan metin alanı. Bu alan düzenlenebilir. | 
| **Fatura** ve ilgili alanlar | **Özet sekmesi** | Varsayılanlar Proje sözleşmesi müşterisi 'den ayarlanır. Bu alan düzenlenebilir.  | 
| **Durum** | **Özet** sekmesi | Şu seçenekleri ayarlar: **Etkin**, **Kapalı**, **Ödendi** ve **İptal Edildi** ve düzenlenebilir. Project Operations için desteklenmeyen durumlar **kapandı** ve **iptal edildi**. </br> Fatura oluşturulduğunda durum **etkin** olarak ayarlanır. </br>Durum yalnızca fatura onaylandıktan sonra **ödeme** olarak ayarlanmalıdır.  | 
| **Proje Faturası Durumu** | **Özet** sekmesi | Şu seçenekleri ayarlar: **Taslak**, **İncelemede** ve **Onaylanmış** ve düzenlenebilir. Hem **taslak** hem de **Gözden geçirme durumunda** fatura düzenlenebilir. Fatura onaylandıktan sonra düzenlenemez. | 
| **Ayrıntı Tutarı** | **Özet** sekmesi | Tüm fatura satırlarındaki avanslar ve kesintiler sonrası tutarların toplamı. Düzenlemeden kilitlenen salt okunur bir alan.  Bu alan, son tutarı hesaplamak için kullanılır. | 
| **İndirim (%)** | **Özet** sekmesi | Bu alan, bir iskonto yüzdesi girmek üzere düzenlenebilir. Bu alan Project Operations işlevselliği tarafından desteklenmiyor. Bu desteklenmeyen bir alandır.|  
| **İskonto Tutarı** | **Özet** sekmesi | Bu alan, bir iskonto tutarı girmek üzere düzenlenebilir. Bu alan Project Operations işlevselliği tarafından desteklenmiyor. Bu desteklenmeyen bir alandır. |  
| **Navlun Öncesi Tutar** | **Özet sekmesi** | İndirimler uygulandıktan sonra toplam fatura tutarı. Düzenlemeden kilitlenen salt okunur bir alan. Bu alan, son tutarı hesaplamak için kullanılır.  | 
| **Navlun Tutarı** | **Özet** sekmesi | Bu alan, bir navlun tutarı girmek üzere düzenlenebilir. Bu alan Project Operations işlevselliği tarafından desteklenmiyor. Bu desteklenmeyen bir alandır. |
| **Toplam Vergi** | **Özet** sekmesi | Faturadaki tüm fatura satırlarından toplam vergi. Düzenlemeden kilitlenen salt okunur bir alan. | 
| **Toplam Tutar** | **Özet** sekmesi | İskonto ve vergilerin ardından tutarın toplamı. Toplam, müşterinin ödemesi gerekli olan tutardır. | 

## <a name="project-based-invoice-lines"></a>Proje tabanlı fatura satırları

Project Operations, her proje sözleşme satırı için her zaman bir fatura satırı vardır. Fatura satırı, hiçbir fiili değer olmasa da oluşturulur. Aşağıdaki bilgiler, bir Proforma fatura satırında bulunur.

| Alan | Location | Açıklama | 
| --- | --- | --- |
| **Fatura kimliği** | **Genel** sekmesi | Fatura kimliğine başvuru. Düzenlemeden kilitlenen salt okunur bir alan. Fatura kimliği bağlantısı, fatura başlığına geri gitmek için kullanılabilir. | 
| **Ad** | **Genel** sekmesi | Sözleşme satırı adından varsayılan olarak ayarlanan fatura satırının adı. Bu alan düzenlenebilir. |
| **Project** | **Genel** sekmesi | İlgili proje sözleşmesi satırındaki Proje. Düzenlemeden kilitlenen salt okunur bir alan. Projeye gitmek için proje bağlantısı kullanılabilir. | 
| **Faturalama Yöntemi** | **Genel** sekmesi | İlgili proje sözleşmesi satırındaki fatura yöntemi. Düzenlemeden kilitlenen salt okunur bir alan. |
| **Sözleşme Satırı Tutarı** | **Genel** sekmesi | İlgili proje sözleşme satırındaki sözleşme tutarı. Düzenlemeden kilitlenen salt okunur bir alan. | 
| **Bu Tarihe Kadar Faturalananlar** | **Genel** sekmesi | Bu faturanın tüm fatura satırı ayrıntılarındaki tutarların toplamı. Düzenlemeden kilitlenen salt okunur bir alan. | 
| **Tutar** | **Genel** sekmesi | Bu faturanın tüm fatura satırı ayrıntılarındaki tutarların toplamı. Düzenlemeden kilitlenen salt okunur bir alan. Bu alan, fatura üst bilgisindeki son tutarı hesaplamak için kullanılır. | 
| **Vergi** | **Genel** sekmesi | Bu fatura satırının tüm fatura satırı ayrıntılarındaki vergi tutarların toplamı. Düzenlemeden kilitlenen salt okunur bir alan. Bu alan, fatura üst bilgisindeki son vergi tutarı hesaplamak için kullanılır. | 
| **Toplam Tutar** | **Genel** sekmesi | Bu fatura satırının tüm ücretlendirilebilir fatura satırı ayrıntılarındaki tutarların (**Vergi + Tutarlar**) toplamı. Düzenlemeden kilitlenen salt okunur bir alan. Bu alan, fatura üst bilgisindeki son tutarı hesaplamak için kullanılır. |

## <a name="invoice-line-details"></a>Fatura Satırı Ayrıntıları

Bir proje faturasındaki her fatura satırı fatura satırı ayrıntılarını içerir. Bu satır ayrıntıları fatura satırı ile referansta bulunulan sözleşme satırıyla ilgili olarak faturalandırılmadığı satış fiili değerleri ve kilometre taşları ile ilgilidir. Tüm bu hareketler **Faturaya hazır** olarak işaretlenir.

**Zaman ve Malzeme Faturası** satırı için fatura satırı ayrıntıları **Fatura Satırı** sayfasında şu gruplara ayrılır: **Borçlandırılabilir**, **Borçlandırılamaz** ve **Ücretsiz**. **Borçlandırılabilir fatura satırı** ayrıntıları fatura satır toplamına kadar bilgi ekleyin. **Kapanış** ve **borçlandırılamayan fiili değerler** fatura satır toplamına eklenmez.

**Sabit Fiyat Faturası** satırı için, fatura satırı ayrıntıları, ilgili sözleşme satırında **Faturalamak için hazır** olarak işaretlenmiş kilometre taşlarından oluşturulur. Bir kilometre taşından fatura satırı ayrıntısı oluşturulduktan sonra, kilometre taşına ait faturalama durumu, **oluşturulan müşteri faturasına** güncelleştirilir.

### <a name="edit-invoice-line-details"></a>Fatura Satırı Ayrıntılarını düzenle

Aşağıdaki alanlar, faturalanmamış bir satış fiili ile desteklenen bir fatura satırı ayrıntısı ile kullanılabilir.

| Alan | Açıklama |
| --- | --- | 
| **Fatura Satırı** | **Fatura satırı kimliğine** başvuru. Bu alan salt okunur ve düzenlemeye karşı kilitlidir. Bu bağlantı, fatura başlığına geri gitmek için kullanılabilir. | 
| **Açıklama** | Fatura satırı ayrıntısının açıklaması. Varsayılan olarak , **zaman girişindeki** **dahili Yorumlar** alanında ve **gider girişindeki** **Açıklama** alanından ayarlanır. Alan düzenlenebilir.| 
| **Harici Açıklama** | Fatura satırı ayrıntısının açıklaması. Varsayılan olarak , **zaman girişindeki** **Harici Yorumlar** alanında ve **gider girişindeki** **Açıklama** alanından ayarlanır. Alan düzenlenebilir. Bu açıklama, müşteriye gönderilecek yazdırılmış faturada ne olacağını belirlemek için kullanılabilir. Project Operations'da, bir Proforma faturası fatura için yazdırma ayarlarını yapılandırmak için gerekli olan tüm işlevselliğe sahip değildir. | 
| **Başlangıç Tarihi** | Kaynak gerçek değerinden varsayılan olarak ayarlanan bu alan salt okunurdur. |
| **Project** | İlgili sözleşme satırında kaynak gerçek değerinden varsayılan olarak ayarlanan bu alan salt okunurdur. |  
| **Görev** | Varsayılan olarak kaynak gerçek tarafından ayarlanır. Düzenlemeden kilitlenen salt okunur bir alan. |
| **İşlem kategorisi** | Varsayılan olarak kaynak gerçek tarafından ayarlanır. Düzenlemeden kilitlenen salt okunur bir alan. | 
| **Rol** | Varsayılan olarak kaynak gerçek tarafından ayarlanır. Düzenlemeden kilitlenen salt okunur bir alan. |  
| **Ayrılabilir Kaynak** | Varsayılan olarak kaynak gerçek tarafından ayarlanır. Düzenlemeden kilitlenen salt okunur bir alan. | 
| **Kaynak Atayan Şirket** | Varsayılan olarak kaynak gerçek tarafından ayarlanır. Düzenlemeden kilitlenen salt okunur bir alan. | 
| **Kaynak Belirleme Birimi** | Varsayılan olarak kaynak gerçek tarafından ayarlanır. Düzenlemeden kilitlenen salt okunur bir alan. | 
| **Miktar** | Varsayılan olarak kaynak gerçek tarafından ayarlanır. Düzenlemeden kilitlenen salt okunur bir alan. |  
| **Birim Çizelgesi** | Zaman için fatura satır ayrıntısı için bu her zaman zaman olarak ayarlanmış ve düzenlenemez. Giderler için bu, varsayılan olarak kaynak gider fiili öğesinden ayarlanır. Düzenlemeden kilitlenen salt okunur bir alan. | 
| **Birim** | Varsayılan olarak kaynak gerçek tarafından ayarlanır. Düzenlemeden kilitlenen salt okunur bir alan. |  
| **Fiyat** | Varsayılan olarak kaynak gerçek tarafından ayarlanır. Düzenlemeden kilitlenen salt okunur bir alan. |
| **Para birimi** | Varsayılan olarak kaynak gerçek tarafından ayarlanır. Düzenlemeden kilitlenen salt okunur bir alan. | 
| **Miktar** | Varsayılan olarak kaynak gerçek tarafından ayarlanır. Düzenlemeden kilitlenen salt okunur bir alan. | 
| **Vergi** | Varsayılan olarak kaynak gerçek tarafından ayarlanır. Alan düzenlenebilir.| 
| **Toplam Tutar** | Hesaplanan bir alan, **Tutar + Vergi** olarak hesaplanır. Düzenlemeden kilitlenen salt okunur bir alan. | 
| **Fatura Türü** | Varsayılan olarak kaynak gerçek tarafından ayarlanır. Alan düzenlenebilir. **Borçlandırılabilir** satır, fatura satır toplamına eklenir. **Tamamlayıcı** ve **borçlandırılamayan**, fatura satır toplamndan hariç kalır.| 
| **Ürün Seç** | Varsayılan olarak kaynak gerçek tarafından ayarlanır. Düzenlemeden kilitlenen salt okunur bir alan. |
| **Ürün** | Varsayılan olarak kaynak gerçek tarafından ayarlanır. Düzenlemeden kilitlenen salt okunur bir alan. | 
| **Ürün Adı** | Varsayılan olarak kaynak gerçek tarafından ayarlanır. Düzenlemeden kilitlenen salt okunur bir alan. |  
| **Serbest Ürün Açıklaması** | Varsayılan olarak kaynak gerçek tarafından ayarlanır. Düzenlemeden kilitlenen salt okunur bir alan. |
| **İşlem Türü** | Kaynak gerçek değerinden **Faturalanan Satış**'a varsayılan olarak ayarlanan bu alan salt okunurdur. |  
| **İşlem Sınıfı** | Varsayılan olarak kaynak gerçek tarafından ayarlanır. Düzenlemeden kilitlenen salt okunur bir alan. | 

Aşağıdaki alanlar, kilometre taşı ile desteklenen bir fatura satırı ayrıntısı ile kullanılabilir.

| Alan | Açıklama |
| --- | --- | 
| **Fatura Satırı** | **Fatura satırı kimliğine** başvuru. Düzenlemeden kilitlenen salt okunur bir alan. Bu bağlantı, fatura başlığına geri gitmek için kullanılabilir.  | 
| **Açıklama** | Fatura satırı ayrıntısının açıklaması. Varsayılan olarak kaynak kilometre taşına ait açıklama olarak ayarlayın. | 
|**Harici Açıklama** | Kaynak kilometre taşına ait açıklama üzerinden varsayılan olarak ayarlanan fatura satırı detayına ilişkin açıklama. Bu alan, müşteriye gönderilecek yazdırılmış faturada ne olacağını belirlemek için kullanılabilir. Project Operations'da, bir Proforma faturası fatura için yazdırma ayarlarını yapılandırmak için gerekli olan tüm işlevselliğe sahip değildir. | 
| **Başlangıç Tarihi** | Varsayılan olarak kaynak **kilometre taşına** ait kilometre taşı tarihinden göre ayarlayın. Düzenlemeden kilitlenen salt okunur bir alan. | 
| **Project** | Varsayılan olarak kaynak kilometre taşı tarafından ayarlanır. Düzenlemeden kilitlenen salt okunur bir alan. |
| **Görev** | Varsayılan olarak kaynak kilometre taşı tarafından ayarlanır. Düzenlemeden kilitlenen salt okunur bir alan. | 
| **İşlem kategorisi** | Düzenlemeden kilitlenen salt okunur bir alan. |
| **Rol** | Düzenlemeden kilitlenen salt okunur bir alan. | 
| **Ayrılabilir Kaynak** | Düzenlemeden kilitlenen salt okunur bir alan. | 
| **Kaynak Belirleme Birimi** | Düzenlemeden kilitlenen salt okunur bir alan. | 
| **Birim Çizelgesi** | Düzenlemeden kilitlenen salt okunur bir alan. | 
| **Birim** | Düzenlemeden kilitlenen salt okunur bir alan. | 
| **Fiyat** | Varsayılan olarak kaynak kilometre taşına ait tutar olarak ayarlayın. Düzenlemeden kilitlenen salt okunur bir alan. |
| **Para Birimi** | Varsayılan olarak kaynak kilometre taşı tarafından ayarlanır. Düzenlemeden kilitlenen salt okunur bir alan. |
| **Tutar** | Varsayılan olarak kaynak kilometre taşına ait tutar olarak ayarlayın. Düzenlemeden kilitlenen salt okunur bir alan. | 
| **Vergi** | Varsayılan olarak kaynak kilometre taşına ait vergi tutar olarak ayarlayın. Düzenlemeden kilitlenen salt okunur bir alan. |
| **Toplam Tutar** | Varsayılan olarak kaynak kilometre taşına ait genişletilmiş tutar olarak ayarlayın. Alan düzenlenebilir. | 
| **Fatura Türü** | Varsayılan olarak her zaman **Borçlandırılabilir** olarak ayarlayın. Düzenlemeden kilitlenen salt okunur bir alan. |
| **İşlem Türü** | Varsayılan olarak kaynak kilometre taşı tarafından ayarlanır. Düzenlemeden kilitlenen salt okunur bir alan. | 
| **İşlem Sınıfı** | Varsayılan olarak kaynak kilometre taşı tarafından ayarlanır. Düzenlemeden kilitlenen salt okunur bir alan. | 

## <a name="refresh-invoice-transactions"></a>Fatura İşlemlerini Yenile

Fatura oluşturulduktan sonra gelen fiili değerleri varsa, bu fiili değerleri faturaya dahil edebilirsiniz.

1. **Faturalama biriktirme listesi** görünümünde verileri **Faturaya hazır** olarak işaretleyin.   
2. Taslak proforma faturasını açın ve **Eylemler** şeridinde **Fatura Satırı İşlemlerini Yenile**'yi seçin.

  Fatura satırı ayrıntıları, geçmiş tarihli ve **Faturalamak için hazır** olarak işaretlenmiş ancak faturaya dahil edilmemiş tüm gerçek değerler için oluşturulur.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
