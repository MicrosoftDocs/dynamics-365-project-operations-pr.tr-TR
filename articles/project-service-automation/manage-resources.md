---
title: Kaynakları yönetme
description: Bu konu, kaynakları yönetme hakkında bilgi sağlar.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 39893019-123b-4bc6-8a2b-a37bc517dc97
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 6c199cbadd1c78e7e29c0cda0febde4236a13d96
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756723"
---
# <a name="manage-resources"></a>Kaynakları yönetme

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation, kuruluşun tamamında kaynak talebine ve kullanımına ilişkin görsel bir genel bakış sağlayan bir kaynak yöneticisi panosu içerir. Aşağıdaki bilgileri görselleştirmek için bu panodaki grafikleri kullanabilirsiniz:

- **Kaynak talebi** – **Etkin Kaynak İsteği** grafiği, gönderilen kaynakları gösterir. Kaynaklar role veya projeye göre toplanır.
- **Gönderilmemiş kaynak isteği** – **Atanmamış Kaynak İsteği** grafiği gönderilmemiş tüm kaynak gereksinimlerini gösterir. Kaynak yöneticilerinin, kesin olmayan ve bir kaynak isteği üzerinden gönderilen talepleri görüntülemesine yardımcı olur.
- **Geçen hafta için faturalandırılabilir kullanım** – **Role göre kullanım** grafiği, kuruluşun role göre fiili faturalandırılabilir kullanımının role göre hedef faturalandırılabilir kullanımına olan yüzdesini gösterir.

    > [!NOTE]
    > **Role göre Kullanım** grafiğini kullanılabilir hale getirmek için, UpdateRoleUtilizatione iş akışını çalıştıran bir iş oluşturun. Bu yinelenen iş, önceki yedi gündeki faturalandırılabilir kullanımı hesaplamak için yedi günde bir çalışır. Sonuçlar role göre toplanır.

## <a name="manage-project-team-members"></a>Proje takımı üyelerini yönetme

Proje yöneticileri, projelerdeki kaynakları yönetmek için kaynak yöneticisi panosunu kullanabilir. Örneğin, bir projeye doğrudan bir takım üyesi ekleyebilir ve bir genel kaynak tarafından yakalanan kaynak gereksinimlerini karşılamak üzere bir takım üyesi ekleyebilirler.

### <a name="add-a-team-member-directly-to-a-project"></a>Bir projeye doğrudan takım üyesi ekleme

Bir projeye doğrudan bir takım üyesi eklemek için **Projeler** sayfasının **Takım** sekmesinde **Yeni**'yi seçin. **Hızlı Oluştur: Proje Takım Üyesi** iletişim kutusu görüntülenir. Bu iletişim kutusunda aşağıdaki görevleri gerçekleştirebilirsiniz:

- **Adlandırılmış kaynak ayırma** - **Ayrılabilir Kaynak** alanında, kaynağın adını seçin. Sonra rolü seçin, dönemi ayarlayın ve bir tahsisat yöntemi seçin. Seçtiğiniz adlandırılmış kaynak, seçili tahsisat yöntemi ve kaynaklar takvimi kullanılarak projeye eklenir.
- **Genel kaynak ekle** – **Ayrılabilir kaynak** alanını boş bırakın ve ardından rolü seçin, dönemi ayarlayın ve tercih edilen tahsisat yöntemini seçin. Genel bir kaynak, takımda adlandırılmış kaynakları ayırmak için kullanılan talep modelini tutacak bir yer tutucu olarak takıma eklenir. Gereksinim proje takvimine göre yapılır.
- **Kaynak kapasitesini tüketmeden takıma adlandırılmış kaynak ekle** – **Ayrılabilir kaynak** alanında bir kaynak seçin. Sonra rolü seçin, tahsisat yöntemi olarak **Hiçbiri**'ni seçin. Kaynak takıma eklenir, ancak kaynağın kapasitesi bir ayırma işlemi aracılığıyla tüketilmez.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Bir genel kaynağın kaynak gereksinimlerini karşılamak için bir takım üyesi ayırma

PSA'da, proje takımında genel bir kaynağı ayırabilir ve rolü, gerekli kapasiteyi ve bu kapasitenin nasıl dağıtıldığını belirtebilirsiniz. Kaynak gereksiniminde, genel kaynakla ilişkili öznitelikleri belirtebilirsiniz. Bu öznitelikler gerekli becerileri, tercih edilen kuruluş birimini ve tercih edilen kaynakları içerir.

Bir geliştirici için genel kaynaktaki gerekli becerileri belirtmek üzere bu adımları izleyin.

1. **Projeler** sayfasının **Takım** sekmesinde genel bir kaynak ayırmak için **Yeni**'yi seçin.

    ![Takımda ayrılmış genel kaynak](media/Resource-Management-image9.png)

2. **Tüm Takım Üyeleri** görünümünde, **Kaynak Gereksinimi** sütununda genel kaynak için gerekli becerileri eklemek üzere bağlantıyı seçin.

    ![Gereksinim bağlantısı](media/Resource-Management-image10.png)

3. Görüntülenen **Kaynak Gereksinimi** sayfasındaki **Yetenekler** ızgarasında üç nokta simgesini (**...**) ve ardından geliştiriciniz için gerekli becerileri eklemek üzere **Yeni Gereksinim Özelliği Ekle**'yi seçin. 

    ![Yeni Gereksinim Özelliği Ekle komutu](media/Resource-Management-image11.png)

4. Görüntülenen **Hızlı Oluştur: Gereksinim Özelliği** iletişim kutusunda, **Özellik** alanında gerekli yeteneği seçin. Ardından, **Derecelendirme değeri** alanında, söz konusu beceri için yeterlilik düzeyini seçin. Son olarak, **Kaynak Gereksinimi** alanında, kaynakları kuruluş birimlerinden veya adlandırılmış kaynaklardan bulmak için gereksinimi ayarlayın. Tamamladığınızda, **Kaydet** öğesini seçin.

    ![Hızlı Oluştur: Gereksinim Özelliği iletişim kutusu](media/Resource-Management-image12.png)

5. **Kaynak Gereksinimi** sayfasında, kaynak gereksinimini karşılamak için **Ayır**'ı seçin.

    ![Kaynak Gereksinimi sayfasındaki Ayır düğmesi](media/Resource-Management-image13.png)

    Ayrıca, **Tüm Takım Üyeleri** ızgarasında genel kaynağı seçebilir ve ardından **Ayır** seçeneğini belirleyebilirsiniz.

    ![Tüm Takım Üyeleri ızgarasındaki Ayır düğmesi](media/Resource-Management-image14.png)

    > [!NOTE]
    > Bu örnekte, gerekli 40 saat bulunur ancak genel kaynakların ayırmaları olmadığından fiili ayrılmış saat yoktur. Ayrıca, genel kaynak doğrudan takıma eklendiğinden, atanmış saatler yoktur. Görev ataması kullanılarak eklenmemiştir.

    **Zamanlama Yardımcısı** sayfasında, kullanılabilir kaynakları kaynak gereksiniminde belirtilen gereksinimlere göre filtreleyebilirsiniz. Kaynaklar, Zamanlama Panosunda belirtilen sıralama parametrelerine göre sıralanır.

    ![Zamanlama Yardımcısı sayfası](media/Resource-Management-image15.png)

    İşte sık kullanılan bazı filtreler:

    - **Bir derecelendirmeye sahip özellikler** – Yetkinlik derecelendirmelerine ek olarak becerilere, sertifikalara ve diğer kaynak niteliklerine göre filtreleyin.
    - **Roller** – Ayrılabilir kaynaklarına atanan varsayılan rollere göre filtreleyin.
    - **Kuruluş birimleri** – Ayrılabilir kaynakları atandıkları kuruluş birimlerine göre filtreleyin.

6. İlk gereksinim aramasının sonuçlarından memnun olmazsanız, filtre ölçütünü değiştirebilirsiniz. Sol taraftaki **Filtre Görünümü** bölmesini genişletin ve daha fazla kaynak bulmak için **Ara**'yı seçin.

    ![Filtre Görünümü bölmesi](media/Resource-Management-image16.png)

7. Sonuçların sıralanma biçimini değiştirmek için **Sırala**'yı seçin.

    ![Sırala komutu](media/Resource-Management-image17.png)

8. Kılavuzun en üstünde belirtildiği gibi gereksinimde belirtilen talebe göre kaynakları seçin. Izgaradaki hücrelerin seçimini temizleyebilir ve bu kaynak kapasitesini açık bırakabilirsiniz. Aynı anda yalnızca tek bir kaynak ayrılmış olarak seçilebilir.

9. Seçili kaynağı ayırmak için **Ayır**'ı seçin ve ek kaynaklar seçebilmeniz için Zamanlama Panosunu açık bırakın. Bunun yerine, seçili kaynağı ayırmak ve Zamanlama Panosunu kapatmak için **Ayır ve Çık**'ı seçin.

    ![Ayrılacak kaynak](media/Resource-Management-image19.png)

    Ayrılmış saatler hakkında bir bildirim alırsınız. Talep göstergeleri, ayırma gereksiniminin ne kadarının karşılandığını ve ne kadar kaldığını gösterir. Seçilen kaynağın kapasitesinin ne kadarının tüketildiğini de görebilirsiniz. Kaynak ayırmaları hakkında daha fazla ayrıntı görmek için **Genişlet**'i seçin.

9. **Tüm Takım Üyeleri** görünümüne dönün. Izgarada, genel kaynağın adlandırılmış kaynak tarafından değiştirildiğine ve bu kaynak için 40 saatin ayrılmış olarak listelendiğine dikkat edin.

    ![Güncelleştirilmiş Tüm Takım Üyeleri kılavuzu](media/Resource-Management-image20.png)

    > [!NOTE]
    > Atanan saatler gösterilmez, çünkü bunlar doğrudan takımda ayrılır. Bunlar görev ataması kullanılarak ayrılmamıştır.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Görevlere genel kaynaklar atama ve kaynak gereksinimleri oluşturma

PSA'da, görevler oluşturabilir ve bunlara genel kaynaklar atayabilirsiniz. Bu şekilde, zamanlama ve mali rakamları tahmin ederken kaynak talebi yer tutucularla temsil edilebilir. Daha sonra genel kaynaklar için kaynak gereksinimleri oluşturabilir ve bunları karşılayabilirsiniz.

1. **Projeler** sayfasındaki **Zamanlama** sekmesinde görev oluşturmak için **Ekle**'yi seçin.

    ![Yeni görev oluşturuldu](media/Resource-Management-image21.png)

2. **Kaynaklar** alanında **Kaynak Seçici** simgesini seçin. Kaynak Seçici görüntülenir ve proje için varolan takım üyelerini gösterir.

    ![Kaynak Seçici](media/Resource-Management-image22.png)

3. Yeni genel kaynağın adını girin ve **Oluştur**'u seçin.

    ![Yeni genel kaynağın adı girildi](media/Resource-Management-image23.png)

4. Görüntülenen **Hızlı Oluştur: Proje Takımı Üyesi** iletişim kutusunda, **Rol** alanında genel kaynak için rolü seçin. **Kaynak Birim** alanında, genel kaynağın kuruluş birimini seçin. Ardından **Kaydet**'i seçin.

    ![Hızlı Oluştur: Proje Takım Üyesi iletişim kutusu](media/Resource-Management-image24.png)

    Genel takım üyesi göreve atanır.

    ![Genel takım üyesi göreve atanır.](media/Resource-Management-image25.png)

    **Takım** sekmesinde, yeni genel takım üyesini görürsünüz. Yalnızca atanmış saatleri olduğuna dikkat edin. Bu saatler, genel takım üyesine atanan tüm görevlerin toplamıdır. Genel takım üyesinde henüz gerekli saatler veya bir kaynak gereksinimi yoktur.

    ![Takım sekmesindeki genel takım üyesi](media/Resource-Management-image26.png)

5. Artık, Kaynak Seçici'yi kullanarak genel takım üyesini diğer görevlere atayabilirsiniz.

    ![Kaynak Seçicide genel takım üyesi](media/Resource-Management-image27.png)

    Genel kaynağı görevlere atamayı tamamladığınızda, genel kaynak için bir kaynak gereksinimi oluşturabilirsiniz.

5. **Takım** sekmesinde genel kaynağı ve ardından **Gereksinim Oluştur**'u seçin.

    ![Gereksinim Oluştur komutu](media/Resource-Management-image28.png)

    Gereksinim oluşturulduğunda, genel takım üyesi gerekli saatlere ve kaynak gereksinimi için bir bağlantıya sahip olur.

    ![Kaynak gereksinimi bağlantısı](media/Resource-Management-image29.png)

    Adlandırılmış bir kaynağı ayırdıktan sonra genel kaynak takımdan kaldırılır ve adlandırılan kaynakla değiştirilir.

    ![Genel kaynak adlandırılan kaynakla değiştirildi](media/Resource-Management-image30.png)

    **Zamanlama** sekmesinde genel kaynak atamaları kaldırılır ve adlandırılan kaynakla değiştirilir.

    ![Zamanlama sekmesinde Genel kaynak atamaları adlandırılan kaynakla değiştirildi](media/Resource-Management-image31.png)

    > [!NOTE]
    > Bu davranış, yalnızca adlandırılmış bir kaynak genel kaynak gereksinimi için tam olarak ayrılmış olduğunda oluşur. Adlandırılmış bir kaynak genel kaynak gereksiniminin kısmen yerine geçiyorsa veya birden çok adlandırılmış kaynak genel kaynak gereksiniminin yerini alıyorsa, genel kaynak göreve atanmış durumda kalır.

    Aşağıdaki örnekte, beş günlük bir süre için 80 saatlik bir görev (beş gün boyunca günde 16 saat) planlamış ve **İşlevsel**olarak adlandırılan genel kaynağa atanmıştır.

    ![İşlevsel genel kaynağa atanan seksen saat, beş günlük görev](media/Resource-Management-image32.png)

    Gereksinimi oluşturduğunuzda, beş gün boyunca 80 saat içindir.

    ![Beş gün boyunca 80 saat için oluşturulan gereksinim](media/Resource-Management-image33.png)

    Kullanılabilir kaynaklar her gün yalnızca sekiz saat çalıştığından, gereksinimi karşılamak için iki kaynak gerekir.

    ![İkinci kaynak](media/Resource-Management-image35.png)

    **Takım** sekmesinde, artık genel kaynağın gerekli saati olmadığını ancak atanan saatlerin yerine getirme işlemini gerçekleştiren iki adlandırılmış kaynakla birlikte görüntülenmeye devam ettiğini görebilirsiniz.

    ![Takım sekmesindeki adlandırılmış iki kaynak](media/Resource-Management-image36.png)

    **Zamanlama** sekmesinde, genel kaynak göreve atanmış olarak kalır.

    ![Zamanlama sekmesindeki Genel kaynaklar](media/Resource-Management-image37.png)

Bu davranış daha az öngörülebilir bir zamanlama üretebileceğinden, PSA göreve her iki kaynağı atamaz. Bu basit örnekte, saatleri iki kaynak arasında eşit olarak bölmek kolaydır. Ancak, birden çok görev ve birden çok kaynak içeren daha karmaşık senaryolarda, PSA'nın birden çok görev arasında birden çok kaynak için alınan ayırmaları nasıl ayıracağıyla ilgili varsayımlar yapması gerekir.

Bu nedenle, bu senaryolarda proje yöneticisi birden çok ayırmanın ayrıştırılmasından ve gerektiği gibi atanmasından sorumludur. Ayırmaları tahsis etmek için, proje yöneticisi görevleri genel kaynaklardan adlandırılan kaynaklara atar ve ardından tahsisatın ayırmalarla birlikte düzgün çalıştığından emin olmak için **Mutabakat** görünümünü kullanır.

### <a name="edit-a-resource-requirement"></a>Bir kaynak gereksinimini düzenleme

Bir kaynak gereksinimi oluşturulduktan sonra, bir proje yöneticisi veya kaynak yöneticisi Zamanlama Panosu kullanıldığında arama ölçütlerini hassaslaştırmak için ayrıntıları düzenlemek isteyebilir. Kaynak gereksinimini düzenlemek için aşağıdaki adımları uygulayın.

1. **Projeler** sayfasının **Takım** sekmesinde genel bir kaynaktaki herhangi bir gereksinime bağlantıyı seçin.
2. Görüntülenen **Kaynak Gereksinimi** sayfasında, çeşitli öznitelikleri güncelleştirebilirsiniz. İşte bazı örnekler:

    - Ad
    - Başlangıç Tarihi
    - Bitiş Tarihi
    - Süre
    - Kaynak Türü

**Kaynak Gereksinimi** sayfasında, proje yöneticisi veya kaynak yöneticisi aşağıdaki bilgileri de tanımlayabilir:

- Beceriler
- Roller
- Kaynak tercihleri
- Tercih edilen kuruluş birimi

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Bir projede ayrıldıktan sonra kaynak ayırmaları güncelleştirme

Bir proje takımına genel veya adlandırılmış bir kaynak ekledikten sonra, kaynak ayırmalarını değiştirebilirsiniz.

1. **Projeler** sayfasının **Takım** sekmesinde bir takım üyesi seçin ve ardından **Ayırmaları Koru**'yu seçin.

    ![Seçilen takım üyesi için Zamanlama Panosu açıldı](media/Resource-Management-image40.png)

    Zamanlama Panosu görüntülenir ve proje takımı üyesinin ayırmalarını gösterir. Bu proje ve takım üyesinin kapasitesini tüketen diğer projelere ayrılmış saatleri görüntülemek için takım üyesinin kaydını genişletin.

2. Genişletmek veya kısaltmak için, ayırmayı seçin ve sürükleyin. Ayırmayı ayarlamanızı sağlayan **Kaynak Ayırma Oluştur** iletişim kutusu görüntülenir.

    ![Kaynak Ayırma Oluştur iletişim kutusu](media/Resource-Management-image41.png)

3. Ayırmaya sağ tıklayın. Daha sonra aşağıdaki eylemleri gerçekleştirmek için kısayol menüsünü kullanabilirsiniz:

    - Ayırma durumunu değiştirin.
    - Ayırmayı düzenleyin.
    - Proje takımında bir kaynağı değiştirin.

### <a name="change-the-booking-status"></a>Ayırma durumunu değiştime

Herhangi bir varsayılan veya özel ayırma durumunu değiştirebilirsiniz.

![Durumu Değiştir komutu](media/Resource-Management-image42.png)

PSA'da aşağıdaki durumlar bulunur:

- **İptal edildi** – Bu durum kaynağa ilişkin ayırmayı iptal eder ve kaynağın kapasitesini serbest bırakır.
- **Kesin Ayırma** – Bu durum kaynağın kapasitesini kullanır. **Projeler** sayfasındaki **Tüm Takım Üyeleri** ızgarasında **Ayırmaları Koru**'yu açtığınızda ayırma genellikle bu duruma sahiptir.
- **Geçici Ayırma** – Bu durum bir takıma bir kaynak ekler ancak kaynağın kapasitesini kullanmaz. Kaynağın olası bir iş için rezerve edildiğini ancak başka projelerde gereksinim duyulursa hala kapasiteye sahip olduğunu gösterir. Genel kaynak kullanılabilirliği görünümünde, geçici ayırmalar kesin ayırmalardan farklı bir duruma sahiptir.
- **Önerildi** – Bu durum bir kaynak için bir kaynak yöneticisinin veya proje yöneticisinin teklifini temsil eder. Teklifler bir kaynağın kapasitesini tüketmez ve kaynak proje takımına eklenmez. Kaynağı takımda kesin olarak ayırmak için proje yöneticisinin teklifi kabul etmesi gerekir.

### <a name="submit-resource-requests"></a>Kaynak istekleri gönder

Kaynak talepleri, kaynak yöneticisi tarafından karşılanması gereken talebi (kaynak gereksinimi) gerçekleştirmek için kullanılır. Zaten takımda bulunan genel bir kaynak için doğrudan bir kaynak isteği gönderebilirsiniz. Bir kaynak isteği iki şekilde karşılanabilir:

- Kaynak yöneticisi isteği doğrudan karşılar. Bu durumda, genel kaynağın yerini adlandırılmış bir kaynağı bulunan sabit bir ayırma alır.
- Kaynak yöneticisi proje yöneticisine bir kaynak önerir ve proje yöneticisi önerilen kaynağı onaylar veya reddeder.

#### <a name="direct-fulfillment-of-resource-requests"></a>Kaynak isteklerini doğrudan karşılama

Bir kaynak gereksinimi oluşturulduğunda, proje yöneticisi kaynağı ve ardından **İstek Gönder**'i seçerek genel kaynak için kaynak isteği gönderebilir.

![İstek Gönder düğmesi](media/Resource-Management-image45.png)

Kaynakla ilgili yorumlar, isteği karşılayan kaynak yöneticisine sağlanabilir. İstek gönderildikten sonra, takım üyesinin **Durum** alanı **Gönderildi** olarak değiştirilir.

![İsteğe bağlı açıklamalar girme](media/Resource-Management-image46.png)

Kaynak yöneticisi isteği yerine getirince, genel takım üyesi **Tüm takım üyeleri** ızgarasındaki adlandırılmış kaynakla değiştirilir.

![Tüm Takım Üyeleri ızgarasında adlandırılmış kaynakla değiştirilen genel takım üyesi](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Kaynak istekleri için kaynak teklifi kullanma

Kaynak Yöneticisi kaynak isteğinde bir kaynağı doğrudan ayırmak yerine proje yöneticisine kaynak önerebilir. Bir kaynak yöneticisi, gereksinimler için tam eşleşme yoksa bu seçeneği kullanabilir. Kaynak Yöneticisi bir kaynak önerdiğinde, proje yöneticisi genel takım üyesinin **Durum** alanının **İnceleme Gerekli** şeklinde değiştiğini görür.

![Genel takım üyesinin durumu İnceleme Gerekli olarak değiştirildi](media/Resource-Management-image48.png)

Önerilen kaynağı, teklifin ayırma etkisinin görselleştirmesiyle birlikte görüntülemek için **İnceleme Gerekli** durumuna sahip takım üyesine çift tıklayın. Ardından **Önerilen Kaynaklar** sekmesini seçin.

![Önerilen Kaynaklar sekmesi](media/Resource-Management-image49.png)

Önerilen tüm kaynakları kabul etmek için **Tüm Teklifleri Kabul Et**'i veya reddetmek için **Tüm Teklifleri Reddet**'i seçin. Önerilen kaynakları kabul ederseniz, bunlar projede takım üyesi olarak kesin şekilde ayrılır ve genel kaynakların yerini alır.

> [!NOTE]
> Önerilen tüm kaynakları kabul etmeniz veya reddetmeniz gerekir. Bunları kısmen kabul edemez veya reddedemezsiniz.

### <a name="substitute-a-resource-on-the-project-team"></a>Proje takımında bir kaynağı değiştirme

Bazen bir proje yöneticisinin bir projedeki ayrılmış bir takım üyesini değiştirmesi gerekir.

1. **Projeler** sayfasının **Takım** sekmesinde değişim gerektiren kaynağı ve ardından **Ayırmaları Koru**'yu seçin.
2. Kaynağa atanan projeleri görüntülemek için kaynağı genişletin.

    ![Atanan projeleri göstermek için genişletilmiş kaynak](media/Resource-Management-image50.png)

3. Projeye sağ tıklayın ve ardından **Kaynağı Değiştir**'i seçin.
4. Geçerli kaynağın yerine almak istediğiniz kaynağı biliyorsanız, adı seçin veya yazın, sonra **Yeniden ata**'yı seçin.

    ![İkame kaynak belirtme](media/Resource-Management-image51.png)

    Alternatif olarak, bir kaynağı aramak için şu adımları izleyin:

    1. **İkame Bul**'u seçin.

        ![İkame kaynak arama](media/Resource-Management-image52.png)

        Zamanlama Yardımcısı, kullanılabilir alternatifler için bir liste döndürür. Zamanlama Yardımcısı'nda uygun bir ikame bulmak için kullanılabilir kaynaklara daha fazla filtre uygulayabilirsiniz.

        ![Kullanılabilir ikamelerin listesi](media/Resource-Management-image53.png)

    2. Kaynağı değiştirmek için, istediğiniz kaynağı seçin ve **Değiştir**'i seçin.

        ![İkame kaynak seçildi](media/Resource-Management-image54.png)

    Ayırmalar ve atamalar yeni kaynakla değiştirilir.

    ![Ayırmalar ve atamalar yeni kaynakla değiştirildi](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a>Takım üyesi ayırmaları ve atamaları arasında mutabakat sağlama

Takım üyeleri için, atamalar ve ayırmalar çok sıkı şekilde eşleştirilmez. Başka bir deyişle, kaynaklar atamalara sahip olabilir ancak herhangi bir ayırma olmayabilir veya ayırmaları varken atamaları olmayabilir. İdeal olarak, ayırmalar ve atamaların, kaynakların görev atamalarını gerçekleştirmek için kapasiteyi taahhüt edebilecekleri şekilde uyumlu olması gerekir. Bununla birlikte, ayırmalar kullanılabilirliğine dayalı olabilir ve proje devam ederken görev zamanlamaları değiştirilebilir. Bu nedenle, ayırmalar ve atamaların çok sıkı şekilde eşlenmemesi esneklik sağlar.

PSA'da proje yöneticilerinin proje takımları için takım üyesi ayırmaları ile atamaları arasında mutabakat sağlamasına olanak tanıyan **Mutabakat** sekmesi bulunur.

![Mutabakat sekmesi](media/Resource-Management-image56.png)

**Mutabakat** sekmesi ayırmaları ve atamaları her takım üyesi için bireysel görev ataması düzeyinde gösterir. Hücrelerde aylardan günlere kadar olan dönemleri temsil eden saatleri gösterir.

Sekme ayrıca, toplam sütunuyla birlikte proje için genel bir net toplam gösterir.

Her kaynak için sekme, takım üyesinin projedeki ayırmaları ile takım üyesinin görev atamalarının toplu değeri arasındaki farkı hesaplar. İdeal olarak, bu fark 0 (sıfır) olmalıdır. Başka bir deyişle, ayırmalar ile görev atamaları arasında fark olmamalıdır. İki koşula dikkat çekmek için farklılıklar renkli ve gölgeli olarak belirtilir:

- **Ayırma eksikliği** – Ayırma eksikliği bir kaynakta ayırmadan daha fazla atama varsa oluşur. Bu kapasite ayrılmadığından bir proje yöneticisi eksikliği gidermek için kaynağın ayırmalarını uzatarak bu koşulu düzeltmek isteyebilir.
- **Aşırı ayırmalar** – Aşırı ayırmalar bir kaynak projeye ayrıldığında ancak görevlere atanmadığında oluşur. Bu koşul, görev ataması gerçekleşmeden önce kaynağın projeye ayrılmış olduğu durumlarda kabul edilebilir. Ancak diğer durumlarda kaynak görevlere atanmak üzere planlanmaz. Bu durumlarda Proje Yöneticisi, kapasitenin başka bir projede kullanılabilmesi için kaynağın ayırmalarını iptal etmeyi düşünmelidir.

Bazı durumlarda, zamanı gün düzeyinden daha yüksek bir düzeyde (örneğin, ay düzeyi) görüntülediğinizde, kaynak için sıfır (başka bir deyişle, ayırmalar = atamalar) net farkını görebilirsiniz. Ancak, zamanı hafta düzeyinde görüntülerseniz ayın ilk haftasında 0 (sıfır) saat atama ve 40 saat ayırma ve ayın ikinci haftasında 40 saat atama ve 0 (sıfır) saat ayırma olduğunu görebilirsiniz. Genel olarak, ayırmalar ve atamalar üzerinde mutabakat sağlanır, ancak bunlar bir haftadan diğerine farklılık gösterir.

Zamanı daha yüksek düzeylerde görüntülediğinizde **Mutabakat** sekmesindeki hücrelerde alt zaman düzeylerinde farklar olduğunu bildiren bir gösterge bulunur. Bir hücreye çift tıklayarak, farkı yakından görüntüleyebilirsiniz. Daha sonra uzaklaştırmak için sağ tıklayabilirsiniz. Bir kaynağı seçip, ardından kılavuz araç çubuğundaki **Sonraki fark** denetimini kullanarak, bu kaynağın ayırmaları ve atamaları arasındaki sonraki farka gidebilirsiniz. Daha sonra geri gitmek için **Önceki fark** denetimini kullanabilirsiniz. Ayrıca **Ayarlar** altındaki fark göstergesini ve gezinme davranışını devre dışı bırakabilirsiniz.

![Fark göstergesi](media/Resource-Management-image57.png)

Bir kaynak için görev atamalarınızın olması ancak ayırmalarınızın olmaması durumunda **Projeler** sayfasındaki **Mutabakat** sekmesinde ayırma eksikliğini ve ardından **Ayırmayı Genişlet**'i seçin. **Ayırmayı Genişlet** iletişim kutusu görüntülenir ve kaynağın eksikliğini ele almak için gereken ayırmayı gösterir. Ayrıca, kaynağın tüm projeler veya diğer zamanlanabilir varlıklardaki varolan ayırmalarını da gösterir. Kaynağın kullanılabilirliğinden bağımsız olarak, kaynak için ayırma oluşturmak üzere **Tamam**'ı seçerseniz, fazladan ayırmaya neden olabilirsiniz.

![Ayırmayı Genişlet iletişim kutusu](media/Resource-Management-image58.png)

Ardından proje yöneticisi veya kaynak yöneticisi, bir kaynağın kapasitesi üzerinde ayrılmış olduğu durumları yönetmek için Zamanlama Panosunu kullanabilir.
