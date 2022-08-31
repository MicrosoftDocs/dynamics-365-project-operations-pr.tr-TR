---
title: Kapalı projelerle ilgili girişi engellemek için proje durumunu eşitleme
description: Bu makalede, etkin olmayan veya kapalı projelerle ilgili girişi önlemek için Proje Durumunun nasıl eşitleneceği açıklanmaktadır.
author: ryansandnessMSFT
ms.date: 08/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandnessMSFT
ms.openlocfilehash: 7a306da164235f36d9ed5e69196508dce6d257de
ms.sourcegitcommit: 6b6c2bfd04e3e613ed1f38355c7cd47c3a56748d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348034"
---
# <a name="sync-project-status-to-prevent-entry-against-closed-projects"></a>Kapalı projelerle ilgili girişi engellemek için proje durumunu eşitleme

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

## <a name="scenario"></a>Senaryo

Contoso, kaynağı/stoğu tutulmayan senaryolar için Microsoft Dynamics 365 Project Operations ile yayınlanır. Normal iş etkinliğinin bir parçası olarak, projeler tamamlanabilir veya beklemeye alınabilir. Herhangi bir masraf veya fatura oluşturulamayacağını doğrulamak için projeyi devre dışı bırakabilirsiniz.

## <a name="solution"></a>Çözüm

### <a name="prerequisites"></a>Önkoşullar

-   Microsoft Dynamics 365 Finance 10.0.29 veya üstü yüklü olmalıdır.
-   Projeler V2 (msdyn \_projects) için Çift Yazma eşlemesi 1.0.0.3 aşağıda açıklandığı gibi yüklenmelidir veya el ile yapılandırılmalıdır.

### <a name="create-an-updated-version-of-the-project-operations-integration-projects-v2-dual-write-map"></a>Project Operations tümleştirmesi Projects V2 çift yazma eşlemesinin güncellenen sürümünü oluşturma

Project Operations Projects V2 çift yazma eşlemesi güncelleştirmek için:

1. **Veri yönetimi** çalışma alanına gidin ve **Çift yazma**'yı seçin.
2. **Çift yazma** kutucuğunu seçin.
3. **Tablo eşleme** sütunundan **Project V2 (msdyn\_ projects)** konumunu bulup seçin ve Durdur'u seçin.
4. Eşlemeyi açmak için eşleme adını seçin ve **[Hiçbiri]** öğesini seçin.
5. Sütun seç diyalog kutusundan **statecode\[Proje Durumu \]** öğesini ve ardından Tamam'ı seçin. Listeyi daraltmak için filtre değerinde **durum** yazabilirsiniz.
6.  Dönüşümü düzenlemek için **eşleme türü** sütununda **Dönüşüm ekle veya düzenle**'yi seçin.
7.  **Dönüştürme türü** alanından **ValueMap** seçeneğini belirleyin.
8.  **Değer eşleme ekle**'yi seçin ve ardından aşağıdaki **Tuşlar** ve **Değerleri** ekleyin:

   Tuş       | Değer 
   ----------|-------
   InProcess | 0     
   Tamamlandı | Kategori 1     

![Çift yazma eşlemesini gösteren ekran görüntüsü](media/projectstage-dw-mapping.png)

9. **Kaydet**'i seçin.
10. **Çift yazma > Projects V2 (msdyn_projects)** sayfasının üst kısmından **Kaydet**'i seçin.
11. **Tablo ekle**'den **Yayımcı** alanında **CDS Varsayılan Yayımcı** seçeneğini belirleyin.
12. **Sürüm alanını** 1.0.0.3 olarak ayarlayın.
13. Bir **Tanım** girin ve ardından **Kaydet**'i seçin.
14. **Dual-write > Projects V2 (msdyn_projects)** sayfasının üst kısmından eşlemeyi başlatmak için **Çalıştır** öğesini seçin ve çalıştırmadan önce onay istenirse **Evet**'i seçin. 

### <a name="close-a-newly-completed-project"></a>Yeni tamamlanan projeyi kapatma

Dynamics 365 Finance **'işlemde** veya **tamamlanmış** projeleri birbirinden ayırmak için **proje aşaması** alanını kullanır. **Tamamlanmış** projeler, masrafları karşılayamaz veya müşterilere fatura edilemez.

1. Devre dışı bırakmak için bir proje açın.
2. Şeritten **Devre dışı bırak**'ı seçin.

> [!NOTE]
> Her ikisi de finans bağlamında aynı davranacağı için bir projeyi devre dışı bırakabilir veya kapatabilirsiniz.

3. Finance içinde **Tüm projeler listesi** sayfasını açın.
4. Devre dışı bırakılan projenin listede görünmeyeceğini onaylayın.
5. Listenin üzerindeki **projeleri göster** filtresinde, değeri **Etkin** iken **Tümü** olarak değiştirin.
6. Artık devre dışı bırakılan projeyi görürsünüz.

Finance uygulamasında bu projeye için zaman veya gideri günlüğe kaydetmeye çalışırsanız seçim için projeyi görmemeniz gerekir. Bir giderde proje numarasını el ile girerseniz "Proje aşaması bitti, projede kayda izin vermiyor" şeklinde bir ileti görürsünüz. Faturalama ve diğer fatura işlevleri, kapalı bir proje bağlamında olacağı gibi devre dışı bırakılmalıdır.

