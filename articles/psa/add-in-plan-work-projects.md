---
title: Microsoft Project'te işlerinizi Project Service eklentisiyle planlama
description: Bu konuda, Microsoft Project Service için Microsoft Project eklentisini kullanma hakkında bilgiler sağlanmaktadır.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 01/07/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: c9628fcaf40f33d75f70ae15e37f422e65337d2c51d0d803178f8bcdfe10c7bd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993895"
---
# <a name="plan-your-work-in-microsoft-project-with-the-project-service-add-in"></a>Microsoft Project'te işlerinizi Project Service eklentisiyle planlama

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3x](../includes/cc-applies-to-psa-app-3x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] tahminler içeren proje planlaması yapmanızı kolaylaştırır. İşi maliyetler, çaba ve satış değeri son teklifin gönderildiği gibi açık olacak şekilde tanımlayabilirsiniz.  

[!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] uygulamasını yükleyebilir ve planlama işinizi [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'in tanıdık ortamında yapabilirsiniz. [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'in sağlam planlama ve yönetim yeteneklerini kullanın ve proje planınızı Project Service Automation'da güncelleştirin.  

> [!IMPORTANT]
> - SharePoint belge yönetimi özelliğini [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projeleri için [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] dosyalarınızı depolamakta kullanmak isterseniz [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] yöneticinizin belge yönetimini açması gerekir. 
> - [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)], yalnızca [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition ile uyumludur.  

## <a name="download-and-install-the-add-in"></a>Eklentiyi indirme ve yükleme  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] oturum açma bilgileriniz hazır olsun. Bu bilgiler [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'ten [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] uygulamasına bağlanmak için gerekli.  

1.  Yükleme Merkezi'nden desteklenen Project Service sürümü [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) veya [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956) için eklentiyi indirin.  

2.  İndirme bağlantısını seçin.  

3.  İndirme işlemi tamamlandığında, eklentiyi yüklemek için **Evet**'i seçin.  

## <a name="configure-the-add-in"></a>Eklentiyi yapılandırma  

1. [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'i açın ve **Project Service** sekmesini seçin.  

2. **Bağlan**'ı seçin.  

3. Oturum açma bilgilerinizi girin ve ardından **Oturum aç**'ı seçin.  

   Artık eklentiyi kullanmaya başlayabilirsiniz.  

## <a name="read-from-a-template"></a>Şablondan okuma  
 Proje planlamanıza başlamak için [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] içinde oluşturduğunuz ve [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] içine kopyaladığınız bir şablondan okuyun. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Proje şablonu oluşturma (Project Service Automation)](../psa/create-project-template.md)  

1.  **Project Service** sekmesinden, **Oku** > **Project Service Automation Proje Şablonu**'nu seçin.  

2.  Listeden bir proje şablonu seçin ve ardından **Aç**'ı seçin.  

    > [!NOTE]
    >  Varsayılan olarak şablondan Project'e kopyalanan görevler el ile zamanlanmış olarak ayarlanır.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>Proje kaynaklarına [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] rolleri atama  

1.  Projeyi açın ve **Görev** şeridini seçin.  

2. **Gantt Grafiği** menüsünü ve ardından **Kaynak Sayfası**'nı seçin.  

3. Kaynak Sayfası üzerinde, **Project Service Kaynak Rolü** açılan menüsünü ve bir Project Service Automation rolü seçin.  

## <a name="staff-your-project-with-resources"></a>Kaynaklarla projenize personel atama  

1.  Project Service sekmesinden bir satır seçin ve **Kaynakları Bul** seçeneğini belirleyin.  

2.  **Kaynak Ayır** ekranında, proje için kullanmak istediğiniz kaynağı seçin.  

3.  **Ayır**'ı ve ardından **Tamam**'ı seçin.  

## <a name="publish-your-project"></a>Projenizi yayımlama  
Proje planlamanız tamamlandığında, bir sonraki adım projenizi [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] uygulamasında içeri aktarmak ve yayımlamaktır.  

Proje, [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] uygulamasına içeri aktarılır. Fiyatlandırma ve takım oluşturma işlemi uygulanır. Projeyi [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] uygulamasında açın ve takım, proje tahminleri ve iş kırılım yapısının oluşturulup oluşturulmadığına bakın. Aşağıdaki tabloda sonuçların yeri gösterilmektedir.


|              Microsoft Project                                                           |                      Project Service Automation                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**Gantt Grafiği**   | [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **İş Kırılım Yapısı** ekranına içeri aktarır. |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Kaynak Sayfası** |   İçine aktarır [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **proje takım üyelerinin** ekranı.   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Kullanım kullanma**    |    [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Proje tahminleri** ekranına içeri aktarır.     |

**Projenizi içeri aktarmak ve yayımlamak için**  
1. **Project Service** sekmesinde, **Yayımla** > **Yeni Project Service Automation Projesi**'ne gidin.  

2. **Yeni bir Project Service projesine yayımla** iletişim kutusunda, **Proje Adı** alanını doldurun ve **Müşteri**'yi seçin.  

3. İsteğe bağlı olarak, plan Project dosyasını Project Service Automation ile bağlamak için **Proje planını Project Service Automation'a bağla** seçeneğini belirleyin.  

4. **Yayımla** öğesini seçin.  

   Project dosyasını [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]'a bağlamak Project dosyasını ana dosya yapar ve [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]'daki iş kırılım yapısını salt okunur olarak ayarlar.  Proje planında değişiklikler yapmak için, bunları [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'te yapmanız ve [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]'a güncelleştirme olarak yayımlamanız gerekir.  

## <a name="edit-a-project-thats-been-imported"></a>İçeri aktarılan bir projeyi düzenleme  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]'a içeri aktarılan bir proje üzerinde değişiklik yapmak için iki seçeneğiniz vardır:  

- Ana dosyayı açın ve [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'te düzenleyin.  

- Dosyanın bağlantısını kaldırın ve doğrudan Project Service içinde düzenleyin. Varsayılan olarak, [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'ten yüklenen bir proje kilitlidir ve yalnızca Project içinde düzenlenebilir. Dosyayı [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]'da düzenlemek için dosyanın bağlantısının kaldırılmış olması gerekir.  

### <a name="edit-in-pn_microsoft_project"></a>[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'ta düzenle  

1. Ana menüde, **Project Service** > **Projeler**'e gidin.  

2. Proje listesinden, [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'te oluşturduğunuz projeyi açın.  

3. Şeritten **MS Project'te Aç**'ı seçin. Bu işlem, bağlantılı ana dosyayı [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'te açar.  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>Dosyanın bağlantısını kaldırma ve [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service'te düzenleme  

1. Ana menüde, **Project Service** > **Projeler**'e gidin.  

2. Proje listesinden, [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'te oluşturduğunuz projeyi açın.  

3. Şeritten **MS Project bağlantısını kaldır**'ı seçin.  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Project dosyasını SharePoint veya Office Grupları'na yükleme  
 Project dosyanızı SharePoint'e yükleyebilir ve [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projenizin İlişkili Belgeler bölümünde bulabilirsiniz.  Yöneticinizin SharePoint belge yönetimini yapılandırması ve Proje varlığı için açması gerekir. 

 Office Grupları kuruluysa, Project dosyanızı [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)]'e de yükleyebilirsiniz.

### <a name="upload-a-file-for-sharepoint"></a>SharePoint için dosya yükleme  

1. Ana menüde, **Project Service** > **Yükle**'ye gidin.  

2. **Project Service Automation Proje Belgelerine** öğesini seçin.  

3. **[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'te açmayı etkinleştir** iletişim kutusunda, **Evet** veya **Hayır**'ı seçin.  

   - **Evet** seçeneğini belirlerseniz Project Service Automation'da **[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'te Aç** düğmesini seçebilir, [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'i başlatıp Project dosyasını SharePoint belge kitaplığından yükleyebilirsiniz.  

   - **Hayır** seçeneğini belirlerseniz **[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'te Aç** düğmesi çalışmaz.  

4. [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] dosyası belirli bir [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projesinin **Belgeler** bölümü altındaki [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]'da bulunabilir.  

### <a name="upload-a-file-for-office-groups"></a>Office Grupları için dosya yükleme  

1. Ana menüde, **Project Service** > **Yükle**'ye gidin.  

2. **Project Service Automation Proje Belgelerine** öğesini seçin.  

3. **[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'te açmayı etkinleştir** iletişim kutusunda, **Evet** veya **Hayır**'ı seçin.  

   - **Evet** seçeneğini belirlerseniz Project Service Automation'da **[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'te Aç** düğmesini seçebilir, [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'i başlatıp Project dosyasını SharePoint belge kitaplığından yükleyebilirsiniz.  

   - **Hayır** seçeneğini belirlerseniz **[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'te Aç** düğmesi çalışmaz.  

4. [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] dosyası belirli bir [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projesinin **Belgeler** bölümü altındaki [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]'da bulunabilir.  

## <a name="publish--your-project-as-a-template"></a>Projenizi şablon olarak yayımlama  
 Projenizi kaydedebilir ve [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]'da bir proje şablonu olarak kaydederek yeniden kullanabilirsiniz. Proje şablonları [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] içinde yeniden kullanılabilen planlardır. Daha fazla bilgi için bkz. [Proje şablonu oluşturma (Project Service Automation)](../psa/create-project-template.md). 

1. **Project Service** sekmesinde, **Yayımla** > **Yeni Project Service Automation Proje Şablonu**'na gidin.  

2. **Yeni bir Project Service proje şablonuna yayımla** iletişim kutusunda, **Proje şablonu adı**'nı girin.  

3. İsteğe bağlı olarak, Project dosyasını [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ile bağlamak için **Proje planını Project Service Automation'a bağla** seçeneğini belirleyin.  

4. **Yayımla** öğesini seçin.  

Project dosyasını [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]'a bağlamak Project dosyasını ana dosya yapar ve [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] şablonundaki iş kırılım yapısını salt okunur olarak ayarlar.  Proje planında değişiklikler yapmak için, bunları [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'te yapmanız ve [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]'a güncelleştirme olarak yayımlamanız gerekir.

## <a name="read-a-resource-loaded-schedule"></a>Kaynak yüklü zamanlamayı okuma

Project Service Automation'dan proje okurken kaynağın takvimi, masaüstü istemcisiyle eşitlenmez. Görev süreleri, çaba veya bitişte farklılıklar varsa bunun nedeni büyük olasılıkla kaynakların ve masaüstü istemcisinin projeye uygulanan aynı çalışma saati şablonu takvimine sahip olmamasıdır.


## <a name="data-synchronization"></a>Veri eşitleme
Bu bölümdeki tablolarda, Project Service Automation ve Microsoft Project masaüstü eklentisi arasında varlık verilerinin eşitlenmesi hakkında bilgiler sağlanmaktadır.

### <a name="project-task-entity-table"></a>Proje Görevi varlık tablosu
Aşağıdaki tabloda, Project Service Automation ile Microsoft Project masaüstü eklentisi arasında Proje Görevi varlık verilerinin nasıl eşitlendiği açıklanmaktadır.

| **Varlık** | **Alan** | **Microsoft Project'ten Project Service Automation'a** | **Project Service Automation'dan Microsoft Project'e** |
| --- | --- | --- | --- |
| Proje Görevi | Son Tarih | Eşitlendi | Eşitlenmedi |
| Proje Görevi | Tahmini Çalışma | Eşitlendi | Eşitlenmedi |
| Proje Görevi | MS Project İstemci Kimliği | Eşitlendi | Eşitlenmedi |
| Proje Görevi | Ana Görev | Eşitlendi | Eşitlenmedi |
| Proje Görevi | Project | Eşitlendi | Eşitlenmedi |
| Proje Görevi | Proje görevi | Eşitlendi | Eşitlenmedi |
| Proje Görevi | Proje Görevi Adı | Eşitlendi | Eşitlenmedi |
| Proje Görevi | Kaynak belirleme birimi (v3.0'da kullanımdan kaldırıldı) | Eşitlendi | Eşitlenmedi |
| Proje Görevi | Zamanlanan Süre | Eşitlendi | Eşitlenmedi |
| Proje Görevi | Başlangıç Tarihi | Eşitlendi | Eşitlenmedi |
| Proje Görevi | İKY Kimliği | Eşitlendi | Eşitlenmedi |

### <a name="team-member-entity-table"></a>Takım Üyesi varlık tablosu
Aşağıdaki tabloda, Project Service Automation ile Micros arasında Takım Üyesi varlık verilerinin nasıl eşitlendiği açıklanmaktadır

| **Varlık** | **Alan** | **Microsoft Project'ten Project Service Automation'a** | **Project Service Automation'dan Microsoft Project'e** |
| --- | --- | --- | --- |
| Takım Üyesi | MS Project İstemci Kimliği | Eşitlendi | Eşitlenmedi |
| Takım Üyesi | Pozisyon Adı | Eşitlendi | Eşitlenmedi |
| Takım Üyesi | proje | Eşitlendi | Eşitlendi |
| Takım Üyesi | Proje Takımı | Eşitlendi | Eşitlendi |
| Takım Üyesi | Kaynak Belirleme Birimi | Eşitlenmedi | Eşitlendi |
| Takım Üyesi | Rol | Eşitlenmedi | Eşitlendi |
| Takım Üyesi | Çalışma Saatleri | Eşitlenmedi | Eşitlenmedi |

### <a name="resource-assignment-entity-table"></a>Kaynak Atama varlık tablosu
Aşağıdaki tabloda, Project Service Automation ile Micros arasında Kaynak Atama varlık verilerinin nasıl eşitlendiği açıklanmaktadır

| **Varlık** | **Alan** | **Microsoft Project'ten Project Service Automation'a** | **Project Service Automation'dan Microsoft Project'e** |
| --- | --- | --- | --- |
| Kaynak Atama | Başlangıç Tarihi | Eşitlendi | Eşitlenmedi |
| Kaynak Atama | Saat Sayısı | Eşitlendi | Eşitlenmedi |
| Kaynak Atama | MS Project İstemci Kimliği | Eşitlendi | Eşitlenmedi |
| Kaynak Atama | Planlanan İş | Eşitlendi | Eşitlenmedi |
| Kaynak Atama | Project | Eşitlendi | Eşitlenmedi |
| Kaynak Atama | Proje Takımı | Eşitlendi | Eşitlenmedi |
| Kaynak Atama | Kaynak Atama | Eşitlendi | Eşitlenmedi |
| Kaynak Atama | Görev | Eşitlendi | Eşitlenmedi |
| Kaynak Atama | Bugüne Kadar | Eşitlendi | Eşitlenmedi |

### <a name="project-task-dependencies-entity-table"></a>Proje Görevi Bağımlılıkları varlık tablosu
Aşağıdaki tabloda, Project Service Automation ile Micros arasında Proje Görevi Bağımlılıkları varlık verilerinin nasıl eşitlendiği açıklanmaktadır

| **Varlık** | **Alan** | **Microsoft Project'ten Project Service Automation'a** | **Project Service Automation'dan Microsoft Project'e** |
| --- | --- | --- | --- |
| Proje Görevi Bağımlılıkları | Proje Görevi Bağımlılığı | Eşitlendi | Eşitlenmedi |
| Proje Görevi Bağımlılıkları | Bağlantı Türü | Eşitlendi | Eşitlenmedi |
| Proje Görevi Bağımlılıkları | Öncül Görev | Eşitlendi | Eşitlenmedi |
| Proje Görevi Bağımlılıkları | Project | Eşitlendi | Eşitlenmedi |
| Proje Görevi Bağımlılıkları | Ardıl Görev | Eşitlendi | Eşitlenmedi |

### <a name="additional-resources"></a>Ek kaynaklar
 [Proje Yöneticisi Kılavuzu](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]