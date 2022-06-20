---
title: Takım üyesi kılavuzundan takım üyeleri ekleme
description: Bu makale, takım üyesi kaynaklarını yönetme hakkında bilgi sağlar.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 3c0c277ca1fe2b709a6ff1c626f5ea7ec63705d6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928594"
---
# <a name="add-team-members-from-the-team-member-grid"></a>Takım üyesi kılavuzundan takım üyeleri ekleme

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Dynamics 365 Project Operations, kuruluşun tamamında kaynak talebine ve kullanımına ilişkin görsel bir genel bakış sağlayan bir Kaynak yöneticisi panosu içerir. Aşağıdaki bilgileri görselleştirmek için bu panodaki grafikleri kullanabilirsiniz:

- **Kaynak talebi**: **Etkin Kaynak İsteği** grafiği, gönderilen kaynakları gösterir. Kaynaklar role veya projeye göre toplanır.
- **Gönderilmemiş kaynak isteği**: **Atanmamış Kaynak İsteği** grafiği, gönderilmemiş kaynak gereksinimlerinin tamamını gösterir. Bu grafik, Kaynak yöneticilerinin kesin olmayan ve bir kaynak isteği üzerinden gönderilen talepleri görüntülemesine yardımcı olur.
- **Geçen hafta için faturalanabilir kullanım**: **Role göre kullanım** grafiği, kuruluşun role göre gerçek faturalanabilir kullanımının role göre hedef faturalanabilir kullanıma olan yüzdesini gösterir.

    > [!NOTE]
    > **Role göre kullanım** grafiğini kullanılabilir hale getirmek için **UpdateRoleUtilizatione** iş akışını çalıştıran bir iş oluşturun. Bu yinelenen iş, önceki yedi gündeki faturalandırılabilir kullanımı hesaplamak için yedi günde bir çalışır. Sonuçlar role göre toplanır.

## <a name="manage-project-team-members"></a>Proje takımı üyelerini yönetme

Proje yöneticileri, projelerdeki kaynakları yönetmek için Kaynak yöneticisi panosunu kullanabilir. Örneğin, bir projeye doğrudan bir takım üyesi ekleyebilir ve bir genel kaynak tarafından yakalanan kaynak gereksinimlerini karşılamak üzere bir takım üyesi ekleyebilirler.

### <a name="add-a-team-member-directly-to-a-project"></a>Bir projeye doğrudan takım üyesi ekleme

Projeye doğrudan bir takım üyesi eklemek için **Projeler** formunun **Takım** sekmesinde **Yeni**'yi seçin. **Hızlı Oluştur: Proje Takım Üyesi** iletişim kutusu görüntülenir. Bu iletişim kutusunda aşağıdaki görevleri gerçekleştirebilirsiniz:

- **Adlandırılmış kaynak ayırma**: **Ayrılabilir Kaynak** alanında, kaynağın adını seçin. Sonra rolü seçin, dönemi ayarlayın ve bir tahsisat yöntemi seçin. Seçtiğiniz adlandırılmış kaynak, seçili tahsisat yöntemi ve kaynaklar takvimi kullanılarak projeye eklenir.
- **Genel kaynak ekleme**: **Ayrılabilir kaynak** alanını boş bırakın ve ardından rolü seçin, dönemi belirleyin ve tercih edilen tahsisat yöntemini seçin. Takıma, yer tutucu olarak genel bir kaynak eklenir. Yer tutucu, takımda adlandırılmış kaynakları ayırmak için kullanılan talep desenini tutar. Gereksinim proje takvimine göre yapılır.
- **Kaynak kapasitesini tüketmeden takıma adlandırılmış kaynak ekleme**: **Ayrılabilir kaynak** alanında bir kaynak seçin. Dönemi belirleyin ve ardından tahsisat yöntemi olarak **Yok**'u seçin. Kaynak takıma eklenir, ancak kaynağın kapasitesi bir ayırma işlemi aracılığıyla tüketilmez.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Bir genel kaynağın kaynak gereksinimlerini karşılamak için bir takım üyesi ayırma

Project Operations'ta bir proje takımında genel bir kaynak ayırabilirsiniz. Ayrıca rolü, gerekli kapasiteyi ve bu kapasitenin nasıl dağıtılacağını da belirtebilirsiniz. Kaynak gereksinimi için genel kaynakla ilişkili öznitelikleri belirtebilirsiniz. Bu öznitelikler gerekli becerileri, tercih edilen kuruluş birimini ve tercih edilen kaynakları içerir.

Geliştirici için genel bir kaynakta gerekli becerileri belirtmek üzere aşağıdaki adımları tamamlayın.

1. **Projeler** formundaki **Takım** sekmesinde, genel bir kaynak ayırmak için **Yeni**'yi seçin.
2. **Tüm Takım Üyeleri** görünümünde, **Kaynak Gereksinimi** sütununda genel kaynak için gerekli becerileri eklemek üzere bağlantıyı seçin.
3. **Kaynak Gereksinimi** formundaki **Yetenekler** ızgarasında üç nokta simgesini (**...**) ve ardından geliştiriciniz için gerekli becerileri eklemek üzere **Yeni Gereksinim Özelliği Ekle**'yi seçin.
4. Görüntülenen **Hızlı Oluştur: Gereksinim Özelliği** iletişim kutusu formunda, **Özellik** alanında gerekli beceriyi seçin.
5. **Derecelendirme değeri** alanında, söz konusu yetenek için uzmanlık düzeyini seçin. 
6. **Kaynak Gereksinimi** alanında, kaynakları kuruluş birimlerinden ve hatta adlandırılmış kaynaklardan bulmak için gereksinimi ayarlayın. Tamamladığınızda, **Kaydet** öğesini seçin.
7. **Kaynak Gereksinimi** formunda, kaynak gereksinimini karşılamak için **Ayır**'ı seçin. Ayrıca, **Tüm Takım Üyeleri** ızgarasında genel kaynağı seçebilir ve ardından **Ayır** seçeneğini belirleyebilirsiniz.

    > [!NOTE]
    > Bu örnekte, gerekli 40 saat bulunur ancak genel kaynakların ayırmaları olmadığından fiili ayrılmış saat yoktur. Ayrıca genel kaynağın eklenmesi, görev ataması kullanılarak değil doğrudan takıma eklenerek yapıldığı için atanmış saat yoktur.

    **Zamanlama Yardımcısı** formunda, kullanılabilir kaynakları kaynak gereksiniminde belirtilen gereksinimlere göre filtreleyebilirsiniz. Kaynaklar, Zamanlama Panosunda belirtilen sıralama parametrelerine göre sıralanır.

   En sık kullanılan filtrelerden bazıları şunlardır:

    - **Derecelendirmeye sahip özellikler**: Uzmanlık derecelendirmelerine ek olarak becerilere, sertifikalara ve diğer kaynak niteliklerine göre filtreler.
    - **Roller**: Ayrılabilir kaynaklara atanan varsayılan rollere göre filtreler.
    - **Kuruluş birimleri**: Ayrılabilir kaynakları atandıkları kuruluş birimlerine göre filtreler.

8. İlk gereksinim aramasının sonuçlarından memnun olmazsanız, filtre ölçütünü değiştirebilirsiniz. Sol taraftaki **Filtre Görünümü** bölmesini genişletin ve daha fazla kaynak bulmak için **Ara**'yı seçin. Sonuçların sıralanma biçimini değiştirmek için **Sırala**'yı seçin.
9. Kılavuzun en üstünde belirtildiği gibi gereksinimde belirtilen talebe göre kaynakları seçin. Izgaradaki hücrelerin seçimini temizleyebilir ve bu kaynak kapasitesini açık bırakabilirsiniz. Aynı anda yalnızca tek bir kaynak ayrılmış olarak seçilebilir.
10. Seçili kaynağı ayırmak için **Ayır**'ı seçin ve ek kaynaklar seçebilmeniz için Zamanlama Panosunu açık bırakın. Bunun yerine, seçili kaynağı ayırmak ve Zamanlama Panosunu kapatmak için **Ayır ve Çık**'ı seçin.
11. **Tüm Takım Üyeleri** görünümüne dönün. Izgarada, genel kaynağın adlandırılmış kaynak tarafından değiştirildiğine ve bu kaynak için 40 saatin ayrılmış olarak listelendiğine dikkat edin.

    > [!NOTE]
    > Atanan saatler gösterilmez, çünkü bunlar doğrudan takımda ayrılır. Bunlar görev ataması kullanılarak ayrılmamıştır.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Görevlere genel kaynaklar atama ve kaynak gereksinimleri oluşturma

Project Operations'ta görevler oluşturabilir ve ardından bunlara genel kaynaklar atayabilirsiniz. Böylece, zamanlama ve mali rakamları tahmin ederken kaynak talebi yer tutucularla temsil edilebilir. Daha sonra genel kaynaklar için kaynak gereksinimleri oluşturabilir ve bunları karşılayabilirsiniz.

1. **Projeler** formundaki **Zamanlama** sekmesinde görev oluşturmak için **Ekle**'yi seçin.
2. **Kaynaklar** alanında **Kaynak Seçici** simgesini seçin. Kaynak Seçici görüntülenir ve proje için varolan takım üyelerini gösterir.
3. Yeni genel kaynağın adını girin ve **Oluştur**'u seçin.
4. Görüntülenen **Hızlı Oluştur: Proje Takımı Üyesi** iletişim kutusunda, **Rol** alanında genel kaynak için rolü seçin. 
5. **Kaynak Birim** alanında, genel kaynağın kuruluş birimini seçin. Ardından **Kaydet**'i seçin. Genel takım üyesi göreve atanır.

   **Takım** sekmesinde, yeni genel takım üyesini görürsünüz. Yalnızca atanmış saatleri olduğuna dikkat edin. Bu saatler, genel takım üyesine atanan tüm görevlerin toplamıdır. Genel takım üyesinde gerekli saatler veya bir kaynak gereksinimi yoktur.

6. Artık, Kaynak Seçici'yi kullanarak genel takım üyesini diğer görevlere atayabilirsiniz.

   Genel kaynağı görevlere atamayı tamamladığınızda, genel kaynak için bir kaynak gereksinimi oluşturabilirsiniz.

7. **Takım** sekmesinde genel kaynağı ve ardından **Gereksinim Oluştur**'u seçin. Gereksinim oluşturulduğunda, genel takım üyesi gerekli saatlere ve kaynak gereksinimi için bir bağlantıya sahip olur.

  Adlandırılmış bir kaynağı ayırdıktan sonra genel kaynak takımdan kaldırılır ve adlandırılan kaynakla değiştirilir. **Zamanlama** sekmesinde genel kaynak atamaları kaldırılır ve adlandırılan kaynakla değiştirilir.

  > [!NOTE]
  > Bu davranış, yalnızca adlandırılmış bir kaynak genel kaynak gereksinimi için tam olarak ayrılmış olduğunda oluşur. Adlandırılmış bir kaynak genel kaynak gereksiniminin kısmen yerine geçiyorsa veya birden çok adlandırılmış kaynak genel kaynak gereksiniminin yerini alıyorsa, genel kaynak göreve atanmış durumda kalır.

Project Operations, göreve kaynakların her ikisini de atamaz çünkü bu davranış daha az öngörülebilir bir zamanlama oluşturur. Bu basit örnekte, saatleri iki kaynak arasında eşit olarak bölmek kolaydır. Ancak, birden çok görev ve birden çok kaynak içeren daha karmaşık senaryolarda, PSA'nın birden çok görev arasında birden çok kaynak için alınan ayırmaları nasıl ayıracağıyla ilgili varsayımlar yapması gerekir.

Bu nedenle, bu senaryolarda Proje yöneticisi, birden çok ayırmanın ayrıştırılmasından ve gerektiği gibi atanmasından sorumludur. Proje yöneticisi, ayırmaları tahsis etmek için görevleri genel kaynaklardan adlandırılan kaynaklara atar ve ardından tahsisatın ayırmalarla birlikte düzgün çalıştığından emin olmak için **Mutabakat** görünümünü kullanır.

### <a name="edit-a-resource-requirement"></a>Bir kaynak gereksinimini düzenleme

Kaynak gereksinimi oluşturulduktan sonra Proje yöneticisi veya Kaynak yöneticisi, Zamanlama Panosu kullanımındaki arama ölçütlerini hassaslaştırmak için ayrıntıları düzenlemek isteyebilir. Kaynak gereksinimini düzenlemek için aşağıdaki adımları uygulayın.

1. **Projeler** formunda, **Takım** sekmesinde, genel bir kaynakla ilgili herhangi bir gereksinimin bağlantısını seçin.
2. Görünen **Kaynak Gereksinimi** formunda, gerekli alan bilgilerini girin

   **Kaynak Gereksinimi** formunda, Proje yöneticisi veya Kaynak yöneticisi becerileri, rolleri, kaynak tercihlerini ve tercih edilen kuruluş birimini de tanımlayabilir.

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Bir projede ayrıldıktan sonra kaynak ayırmaları güncelleştirme

Bir proje takımına genel veya adlandırılmış bir kaynak ekledikten sonra, kaynak ayırmalarını değiştirebilirsiniz.

1. **Projeler** formunda, **Takım** sekmesinde bir takım üyesi seçin ve ardından **Ayırma İşlemlerini Koru**'yu seçin.
 
   Zamanlama Panosu görüntülenir ve proje takımı üyesinin ayırmalarını gösterir. Bu proje ve takım üyesinin kapasitesini tüketen diğer projelere ayrılmış saatleri görüntülemek için takım üyesinin kaydını genişletin.

2. Genişletmek veya kısaltmak için, ayırmayı seçin ve sürükleyin. Ayırmayı ayarlamanızı sağlayan **Kaynak Ayırma Oluştur** iletişim kutusu görüntülenir.
3. Ayırmaya sağ tıklayın. Daha sonra aşağıdaki eylemleri gerçekleştirmek için kısayol menüsünü kullanabilirsiniz:

    - Ayırma durumunu değiştime
    - Ayırmayı düzenleme
    - Proje takımında bir kaynağı değiştirme

### <a name="change-the-booking-status"></a>Ayırma durumunu değiştime

Herhangi bir varsayılan veya özel ayırma durumunu değiştirebilirsiniz.

Project Operations'ta aşağıdaki durumlar bulunur:

- **İptal Edildi**: Kaynağa ilişkin ayırmayı iptal eder ve kaynağın kapasitesini serbest bırakır.
- **Kesin Ayırma**: Kaynağın kapasitesini tüketir. **Projeler** formundaki **Tüm Takım Üyeleri** ızgarasında **Ayırma İşlemlerini Koru**'yu açtığınızda ayırma genellikle bu durumdadır.
- **Geçici Ayırma**: Takıma bir kaynak ekler ancak kaynağın kapasitesini tüketmez. Bu durum, kaynağın olası bir iş için ayrıldığını ancak başka projelerde gereksinim duyulursa hala kapasitesi olduğunu gösterir. Genel kaynak kullanılabilirliği görünümünde, geçici ayırmalar kesin ayırmalardan farklı bir duruma sahiptir.
- **Önerildi**: Kaynak yöneticisinin veya Proje yöneticisinin bir kaynağı teklif ettiğini ifade eder. Teklifler bir kaynağın kapasitesini tüketmez ve kaynak proje takımına eklenmez. Kaynağı takımda kesin olarak ayırmak için Proje yöneticisinin teklifi kabul etmesi gerekir.

### <a name="submit-resource-requests"></a>Kaynak isteklerini gönderme

Kaynak istekleri, Kaynak yöneticisi tarafından yerine getirilmesi gereken talebi veya kaynak gereksinimini gerçekleştirmek için kullanılır. Zaten takımda bulunan genel bir kaynak için doğrudan bir kaynak isteği gönderebilirsiniz. Bir kaynak isteği iki şekilde karşılanabilir:

- Kaynak yöneticisi isteği doğrudan karşılar. Bu durumda, genel kaynağın yerini adlandırılmış bir kaynağı bulunan sabit bir ayırma alır.
- Kaynak yöneticisi, Proje yöneticisine bir kaynak önerir ve Proje yöneticisi önerilen kaynağı onaylar veya reddeder.

#### <a name="direct-fulfillment-of-resource-requests"></a>Kaynak isteklerini doğrudan karşılama

Kaynak gereksinimi oluşturulduğunda Proje yöneticisi, kaynağı ve ardından **İstek Gönder**'i seçerek genel kaynak için kaynak isteği gönderebilir. Kaynakla ilgili yorumlar, isteği karşılayan Kaynak yöneticisine sağlanabilir. İstek gönderildikten sonra, takım üyesinin **Durum** alanı **Gönderildi** olarak değiştirilir. Kaynak yöneticisi isteği karşıladığında genel takım üyesi, **Tüm takım üyeleri** ızgarasındaki adlandırılmış kaynakla değiştirilir.

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Kaynak istekleri için kaynak teklifi kullanma

Kaynak Yöneticisi, kaynak isteğinde bir kaynağı doğrudan ayırmak yerine Proje yöneticisine kaynak önerebilir. Kaynak yöneticisi, gereksinimler için tam eşleşme yoksa bu seçeneği kullanabilir. Kaynak Yöneticisi bir kaynak önerdiğinde Proje yöneticisi, genel takım üyesinin **Durum** alanının **İnceleme Gerekiyor** olarak değiştiğini görür.

Önerilen kaynağı, teklifin ayırmasının etkisini görmek için bir görselleştirmeyle birlikte görüntüleyebilirsiniz. 

1. **İnceleme Gerekiyor** durumuna sahip takım üyesine çift tıklayın. 
2. **Önerilen Kaynaklar** sekmesini seçin.
3. Önerilen tüm kaynakları kabul etmek için **Tüm Teklifleri Kabul Et**'i veya reddetmek için **Tüm Teklifleri Reddet**'i seçin. Önerilen kaynakları kabul ederseniz, bunlar projede takım üyesi olarak kesin şekilde ayrılır ve genel kaynakların yerini alır.

> [!NOTE]
> Önerilen tüm kaynakları kabul etmeniz veya reddetmeniz gerekir. Bunları kısmen kabul edemez veya reddedemezsiniz.

### <a name="substitute-a-resource-on-the-project-team"></a>Proje takımında bir kaynağı değiştirme

Bazen, Proje yöneticisinin bir projedeki ayrılmış bir takım üyesini ikame etmesi gerekir.

1. **Projeler** formundaki **Takım** sekmesinde ikame edilmesi gereken kaynağı seçin ve ardından **Ayırma İşlemlerini Koru** seçeneğini belirleyin.
2. Kaynağa atanan projeleri görüntülemek için kaynağı genişletin.
3. Projeye sağ tıklayın ve ardından **Kaynağı Değiştir**'i seçin.
4. Geçerli kaynağı ikame etmek istediğiniz kaynağı biliyorsanız adını seçin veya yazın ve ardından **Yeniden Ata**'yı seçin.

Veya. kaynak aramanız gerekirse aşağıdaki adımları tamamlayın.

1. **İkame Bul**'u seçin.

   Zamanlama Yardımcısı, kullanılabilir alternatifler için bir liste döndürür. Zamanlama Yardımcısı'nda uygun bir ikame bulmak için kullanılabilir kaynaklara daha fazla filtre uygulayabilirsiniz.

2. Kaynağı değiştirmek için, istediğiniz kaynağı seçin ve **Değiştir**'i seçin.   

   Ayırmalar ve atamalar yeni kaynakla değiştirilir.

## <a name="reconcile-team-member-bookings-and-assignments"></a>Takım üyesi ayırmaları ve atamaları arasında mutabakat sağlama

Takım üyeleri için, atamalar ve ayırmalar çok sıkı şekilde eşleştirilmez. Başka bir deyişle, kaynaklar atamalara sahip olabilir ancak herhangi bir ayırma olmayabilir veya ayırmaları varken atamaları olmayabilir. İdeal olarak, ayırmalar ve atamaların, kaynakların görev atamalarını gerçekleştirmek için kapasiteyi taahhüt edebilecekleri şekilde uyumlu olması gerekir. Bununla birlikte, ayırmalar kullanılabilirliğine dayalı olabilir ve proje devam ederken görev zamanlamaları değiştirilebilir. Bu nedenle, ayırmalar ve atamaların çok sıkı şekilde eşlenmemesi esneklik sağlar.

Project Operations, Proje yöneticilerinin takım üyelerinin ayırmalarını ve proje takımları için atamalarını mutabık kılmasına olanak tanıyan bir **Mutabakat** sekmesine sahiptir.

**Mutabakat** sekmesi ayırmaları ve atamaları her takım üyesi için bireysel görev ataması düzeyinde gösterir. Hücrelerde aylardan günlere kadar olan dönemleri temsil eden saatleri gösterir.

Sekme ayrıca, toplam sütunuyla birlikte proje için genel bir net toplam gösterir.

Her kaynak için sekme, takım üyesinin projedeki ayırmaları ile takım üyesinin görev atamalarının toplu değeri arasındaki farkı hesaplar. İdeal olarak, bu fark 0 (sıfır) olmalıdır. Başka bir deyişle, ayırmalar ile görev atamaları arasında fark olmamalıdır. İki koşula dikkat çekmek için farklılıklar renkli ve gölgeli olarak belirtilir:

- **Ayırma eksikliği**: Kaynakta, ayırmadan daha fazla atama varsa oluşur. Proje yöneticisi, bu kapasite ayrılmadığından eksikliği gidermek için kaynağın ayırmalarını uzatarak bu durumu düzeltmek isteyebilir.
- **Aşırı ayırmalar**: Kaynak, projeye ayrıldığında ancak görevlere atanmadığında oluşur. Bu koşul, görev ataması gerçekleşmeden önce kaynağın projeye ayrılmış olduğu durumlarda kabul edilebilir. Ancak diğer durumlarda kaynak görevlere atanmak üzere planlanmaz. Bu durumlarda Proje Yöneticisi, kapasitenin başka bir projede kullanılabilmesi için kaynağın ayırmalarını iptal etmeyi düşünmelidir.

Bazı durumlarda, zamanı gün düzeyinden daha yüksek bir düzeyde, örneğin ay düzeyinde görüntülediğinizde kaynak için net farkı sıfır olarak görebilirsiniz. Başka bir deyişle, ayırmalar = atamalar. Ancak, zamanı hafta düzeyinde görüntülerseniz ayın ilk haftasında 0 (sıfır) saat atama ve 40 saat ayırma ve ayın ikinci haftasında 40 saat atama ve 0 (sıfır) saat ayırma olduğunu görebilirsiniz. Genel olarak, ayırmalar ve atamalar üzerinde mutabakat sağlanır, ancak bunlar bir haftadan diğerine farklılık gösterir.

Zamanı daha yüksek düzeylerde görüntülediğinizde **Mutabakat** sekmesindeki hücrelerde alt zaman düzeylerinde farklar olduğunu bildiren bir gösterge bulunur. Yakınlaştırarak farkı görmek için bir hücreye çift tıklayın. Daha sonra uzaklaştırmak için sağ tıklayabilirsiniz. Kaynağı seçip ardından kılavuz araç çubuğunda **Sonraki fark**'ı seçerek bu kaynağın ayırmaları ve atamaları arasındaki sonraki farka gidebilirsiniz. Geri dönmek için **Önceki fark**'ı seçin. Ayrıca **Ayarlar** altındaki fark göstergesini ve gezinme davranışını devre dışı bırakabilirsiniz.

Kaynak için görev atamalarınızın olduğu ama ayırmalarınızın olmadığı bir durumda **Projeler** formundaki **Mutabakat** sekmesinde ayırma eksikliğini seçin ve ardından **Ayırmayı Uzat** seçeneğini belirleyin. **Ayırmayı Genişlet** iletişim kutusu görüntülenir ve kaynağın eksikliğini ele almak için gereken ayırmayı gösterir. İletişim kutusu, kaynağın tüm projeler veya diğer zamanlanabilir varlıklarda var olan ayırmalarını da gösterir. Kaynağın kullanılabilirliğinden bağımsız olarak, kaynak için ayırma oluşturmak üzere **Tamam**'ı seçerseniz, fazladan ayırmaya neden olabilirsiniz.

Ardından Proje yöneticisi veya Kaynak yöneticisi, bir kaynağın kapasitesi üzerinde ayrılmış olan durumları yönetmek için Zamanlama Panosu'nu kullanabilir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]