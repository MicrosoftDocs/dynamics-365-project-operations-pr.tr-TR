---
title: Microsoft Project'te işlerinizi planlamak için Project Service Eklentisi'ni kullanma | MicrosoftDocs
description: Bu konu, Microsoft Project Service için Microsoft Project eklentisini ekleme, yapılandırma ve kullanma hakkında bilgi sağlar.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
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
ms.openlocfilehash: 6bc74442866caccc02e53afc913a55aab81f9629
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129702"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a>Microsoft Project'te işlerinizi planlamak için Project Service Automation Eklentisi'ni kullanma

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] tahminler içeren proje planlaması yapmanızı kolaylaştırır. İşi maliyetler, çaba ve satış değeri son teklifin gönderildiği gibi açık olacak şekilde tanımlayabilirsiniz.  

 Şimdi [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] uygulamasını yükleyebilir ve işlerinizi [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'in tanıdık ortamında planlayabilirsiniz. [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'in sağlam planlama ve yönetim yeteneklerini kullanın ve proje planınızı Project Service Automation'da güncelleştirin.  

> [!IMPORTANT]
> - SharePoint belge yönetimi özelliğini [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projeleri için [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] dosyalarınızı depolamakta kullanmak isterseniz [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] yöneticinizin belge yönetimini açması gerekir. 
> - [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)], yalnızca [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition ile uyumludur.  

## <a name="download-and-install-the-add-in"></a>Eklentiyi indirme ve yükleme  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] oturum açma bilgileriniz hazır olsun. Bu bilgiler [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'ten [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] uygulamasına bağlanmak için gerekli.  

1.  Yükleme Merkezi'nden desteklenen Project Service sürümü [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) veya [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956) için eklentiyi indirin.  

2.  İndirme bağlantısına tıklayın.  

3.  İndirme işlemi tamamlandığında, eklentiyi yüklemek için **Evet**'e tıklayın.  

## <a name="configure-the-add-in"></a>Eklentiyi yapılandırma  

1. [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'i açın ve **Project Service** sekmesine tıklayın.  

2. **Bağlan**'a tıklayın.  

3. Oturum açma bilgilerinizi girin ve **Oturum aç**'a tıklayın.  

   Artık eklentiyi kullanmaya başlayabilirsiniz.  

## <a name="read-from-a-template"></a>Şablondan okuma  
 Proje planlamanıza başlamak için [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] içinde oluşturduğunuz ve [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] içine kopyaladığınız bir şablondan okuyun. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Proje şablonu oluşturma (Project Service Automation)](../psa/create-project-template.md)  

1.  **Project Service** sekmesinden, **Okuma** > **Project Service Automation Proje Şablonu**'na tıklayın.  

2.  Listeden bir proje şablonu seçin ve **Aç**'a tıklayın.  

    > [!NOTE]
    >  Varsayılan olarak şablondan Project'e kopyalanan görevler el ile zamanlanmış olarak ayarlanır.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>Proje kaynaklarına [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] rolleri atama  

1.  Projeyi açın ve **Görev** şeridine tıklayın.  

2.  **Gantt Grafiği** menüsüne tıklayın ve **Kaynak Sayfası**'nı seçin.  

3.  Kaynak Sayfası üzerinde, **Project Service Kaynak Rolü** açılan menüsüne tıklayın ve bir Project Service Automation rolü seçin.  

## <a name="staff-your-project-with-resources"></a>Kaynaklarla projenize personel atama  

1.  Project Service sekmesinden bir satır seçin ve **Kaynak Bul**'a tıklayın.  

2.  **Kaynak Ayır** ekranında, proje için kullanmak istediğiniz kaynağı seçin.  

3.  **Ayır**'a ve sonra da **Tamam**'a tıklayın.  

## <a name="publish-your-project"></a>Projenizi yayımlama  
Proje planlamanız tamamlandığında, bir sonraki adım projenizi [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] uygulamasında içeri aktarmak ve yayımlamaktır.  

Proje, [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] uygulamasına içeri aktarılır. Fiyatlandırma ve takım oluşturma işlemi uygulanır. Projeyi [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] uygulamasında açın ve takım, proje tahminleri ve iş kırılım yapısının oluşturulup oluşturulmadığına bakın. Aşağıdaki tabloda, sonuçları yeri gösterir:


|                                                                                          |                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**Gantt Grafiği**   | [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **İş Kırılım Yapısı** ekranına içeri aktarır. |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Kaynak Sayfası** |   İçine aktarır [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **proje takım üyelerinin** ekranı.   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Kullanım kullanma**    |    Uygulamasına Omports [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Proje tahminleri** ekranı.     |

**Projenizi içeri aktarmak ve yayımlamak için**  
1. **Project Service** sekmesinden, **Yayımla** > **Yeni Project Service Automation Projesi**'ne tıklayın.  

2. **Yeni bir Project Service projesine yayımla** iletişim kutusunda, **Proje Adı** alanını doldurun ve **Müşteri**'yi seçin.  

3. İsteğe bağlı olarak, plan Project dosyasını Project Service Automation ile bağlamak için **Proje planını Project Service Automation'a bağla** seçeneğini işaretleyin.  

4. **Yayımla** öğesine tıklayın.  

   Project dosyasını [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]'a bağlamak Project dosyasını ana dosya yapar ve [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]'daki iş kırılım yapısını salt okunur olarak ayarlar.  Proje planında değişiklikler yapmak için, bunları [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'te yapmanız ve [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]'a güncelleştirme olarak yayımlamanız gerekir.  

## <a name="edit-a-project-thats-been-imported"></a>İçeri aktarılan bir projeyi düzenleme  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]'a içeri aktarılan bir proje üzerinde değişiklik yapmak için iki seçeneğiniz vardır:  

- Ana dosyayı açın ve [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'te düzenleyin.  

- Dosyanın bağlantısını kaldırın ve doğrudan Project Service içinde düzenleyin. Varsayılan olarak, [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'ten yüklenen bir proje kilitlidir ve yalnızca Project içinde düzenlenebilir. Dosyayı [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]'da düzenlemek için dosyanın bağlantısının kaldırılmış olması gerekir.  

### <a name="edit-in-pn_microsoft_project"></a>[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] içinde düzenleme  

1. Ana menüden, **Project Service** > **Projeler**'e tıklayın.  

2. Proje listesinden, [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'te oluşturduğunuz projeyi açın.  

3. Şeritteki **MS Project'te aç** öğesine tıklayın. Bu işlem, bağlantılı ana dosyayı [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'te açar.  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>Dosyanın bağlantısını kaldırma ve [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service'te düzenleme  

1. Ana menüden, **Project Service** > **Projeler**'e tıklayın.  

2. Proje listesinden, [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'te oluşturduğunuz projeyi açın.  

3. Şeritteki **MS Project bağlantısını kaldır** öğesine tıklayın.  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Project dosyasını SharePoint veya Office Grupları'na yükleme  
 Project dosyanızı SharePoint'e yükleyebilir ve [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projenizin İlişkili Belgeler bölümünde bulabilirsiniz.  Yöneticinizin SharePoint belge yönetimini yapılandırması ve Proje varlığı için açması gerekir. 

 Office Grupları kuruluysa, Project dosyanızı [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)]'e de yükleyebilirsiniz.

### <a name="upload-a-file-for-sharepoint"></a>SharePoint için dosya yükleme  

1. Ana menüden, **Project Service** > **Karşıya Yükle** öğesine tıklayın.  

2. **Project Service Automation Proje Belgelerine** öğesini seçin.  

3. **[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'te açmayı etkinleştir** iletişim kutusunda, **Evet** veya **Hayır** öğesini seçin.  

   - **Evet**'e tıkladığınızda, Project Service Automation'da **[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'te aç** düğmesini seçebilir ve [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'i başlatıp Proje dosyasını SharePoint belge kitaplığından yükleyebilirsiniz.  

   - **Hayır**'a tıkladığınızda, **[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'te Aç** düğmesinin bağlantısı çalışmaz.  

4. [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] dosyası belirli bir [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projesinin **Belgeler** bölümü altındaki [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]'da bulunabilir.  

### <a name="upload-a-file-for-office-groups"></a>Office Grupları için dosya yükleme  

1. Ana menüden, **Project Service** > **Karşıya Yükle** öğesine tıklayın.  

2. **Project Service Automation Proje Belgelerine** öğesini seçin.  

3. **[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'te açmayı etkinleştir** iletişim kutusunda, **Evet** veya **Hayır** öğesini seçin.  

   - **Evet**'e tıkladığınızda, Project Service Automation'da **[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'te aç** düğmesini seçebilir ve [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'i başlatıp Proje dosyasını SharePoint belge kitaplığından yükleyebilirsiniz.  

   - **Hayır**'a tıkladığınızda, **[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'te Aç** düğmesinin bağlantısı çalışmaz.  

4. [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] dosyası belirli bir [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projesinin **Belgeler** bölümü altındaki [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]'da bulunabilir.  

## <a name="publish--your-project-as-a-template"></a>Projenizi şablon olarak yayımlama  
 Projenizi kaydedebilir ve [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]'da bir proje şablonu olarak kaydederek yeniden kullanabilirsiniz.  Proje şablonları [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] içinde yeniden kullanılabilen planlardır. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Proje şablonu oluşturma (Project Service Automation)](../psa/create-project-template.md)  

1. **Project Service** sekmesinden, **Yayımla** > **Yeni Project Service Automation Projesi Şablonu**'na tıklayın.  

2. **Yeni bir Project Service proje şablonuna yayımla** iletişim kutusunda, **Proje şablonu adı**'nı girin.  

3. İsteğe bağlı olarak, Proje dosyasını [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ile bağlamak için **Proje planını Project Service Automation'a bağla** seçeneğini işaretleyin.  

4. **Yayımla** öğesine tıklayın.  

Project dosyasını [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]'a bağlamak Project dosyasını ana dosya yapar ve [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] şablonundaki iş kırılım yapısını salt okunur olarak ayarlar.  Proje planında değişiklikler yapmak için, bunları [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'te yapmanız ve [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]'a güncelleştirme olarak yayımlamanız gerekir.

### <a name="see-also"></a>Ayrıca bkz.  
 [Proje Yöneticisi Kılavuzu](../psa/project-manager-guide.md)
