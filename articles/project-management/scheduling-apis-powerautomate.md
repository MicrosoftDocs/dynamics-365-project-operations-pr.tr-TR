---
title: Power Automate ile Proje zamanlama API'lerini kullanma
description: Bu makalede, Proje zamanlaması uygulama programlama arabirimlerini (API'ler) kullanan örnek bir akış sağlanmaktadır.
author: ruhercul
ms.date: 01/26/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: afec082c680596e8dcb8ec0b350b4bb7853c49ff
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/02/2022
ms.locfileid: "9404412"
---
# <a name="use-project-schedule-apis-with-power-automate"></a>Power Automate ile Proje zamanlama API'lerini kullanma

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Bu makalede, Microsoft Power Automate kullanılarak eksiksiz bir proje planının nasıl oluşturulacağını, İşlem Setinin nasıl oluşturulacağını ve bir varlığın nasıl güncelleştirileceğini gösteren örnek bir akışı açıklanmaktadır. Örnekte bir projenin, proje ekibi üyesinin, İşlem Kümelerinin, proje görevlerinin ve kaynak atamalarının nasıl oluşturulacağı gösterilmektedir. Bu makalede ayrıca bir varlığın nasıl güncelleştirildiği ve bir işlem kümesinin nasıl yürütüleceği de açıklanmaktadır.

Aşağıda, bu makaledeki örnek akışta belgelenen adımların tam listesi bulunmaktadır:

1. [PowerApps tetikleyicisi oluşturma](#1)
2. [Bir proje oluştur](#2)
3. [Takım üyesi için bir değişken başlatma](#3)
4. [Genel bir takım üyesi oluşturma](#4)
5. [İşlem kümesi oluşturma](#5)
6. [Proje paketi oluşturma](#6)
7. [Bağlantı durumu için değişken başlatma](#7)
8. [Görev sayısı için bir değişken başlatma](#8)
9. [Proje görev kimliği için değişken başlatma](#9)
10. [Bitiş noktası](#10)
11. [Proje görevi ayarlama](#11)
12. [Proje görevi oluşturma](#12)
13. [Kaynak ataması oluşturma](#13)
14. [Değişkeni azaltma](#14)
15. [Proje görevini yeniden adlandırma](#15)
16. [İşlem Kümesi çalıştırma](#16)

## <a name="assumptions"></a>Varsayımlar

Bu makalede, Dataverse platformu, bulut akışları ve Proje Zamanlaması Uygulama Programlama Arabirimi (API) hakkında temel bilgilere sahip olduğunuz varsayılmaktadır. Daha fazla bilgi için bu makaledeki [Başvurular](#references) bölümüne bakın.

## <a name="create-a-flow"></a>Akış oluşturma

### <a name="select-an-environment"></a>Ortam seçme

Power Automate akışını ortamınızda oluşturabilirsiniz.

1. <https://flow.microsoft.com> adresine gidin ve oturum açmak için yönetici kimlik bilgilerinizi kullanın.
2. Sağ üst köşede, **Ortamlar**'ı seçin.
3. Listede, Dynamics 365 Project Operations'ın yüklendiği ortamı seçin.

### <a name="create-a-solution"></a>Çözüm oluşturma

[Çözüm odaklı akış](/power-automate/overview-solution-flows) oluşturmak için bu adımları izleyin. Çözüme odaklı akış oluşturarak, akışı daha sonra kullanmak üzere daha kolay dışa aktarabilirsiniz.

1. Gezinti bölmesinde **Çözümler**'i seçin.
2. **Çözümler** sayfasında, **Yeni çözüm**'ü seçin.
3. **Yeni çözüm** iletişim kutusunda, gerekli alanları ayarlayın ve ardından **Oluştur**'u seçin.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a>Adım 1: PowerApps tetikleyicisi oluşturma

1. **Çözümler** sayfasında, oluşturduğunuz çözümü seçin ve ardından **Yeni**'yi seçin.
2. Sol bölmede, **Bulut akışları** \> **Otomasyon** \> **Bulut akışı** \> **Anlık** öğesini seçin.
3. **Akış adı** alanına **API Demo Akışını Zamanla** yazın.
4. **Bu akışın nasıl tetikleneceğini seçin** listesinde, **Power Apps**'i seçin. Power Apps tetikleyicisi oluşturduğunuzda mantığı yazar olarak siz belirlersiniz. Bu makalede, test amacıyla giriş parametrelerini boş bırakın.
5. **Oluştur** seçeneğini belirleyin.

## <a name="step-2-create-a-project"></a><a id="2"></a>Adım2: Proje oluşturun

Örnek bir proje oluşturmak için aşağıdaki adımları izleyin.

1. Oluşturduğunuz akışta **Yeni adım**'ı seçin.

    ![Yeni bir adım ekleme.](media/newstep.png)

2. **Bir işlem seçin** iletişim kutusunda, arama alanına **bağlı olmayan eylem gerçekleştir** yazın. Ardından, **Eylemler** sekmesinde, sonuç listesinden işlemi seçin.

    ![Bir işlem seçme.](media/chooseactiontab.png)

3. Yeni adımda, üç noktayı (**...**) ve ardından **Yeniden Adlandır**'ı seçin.

![Adımı yeniden adlandırma.](media/renamestep.png)

4. Adımı, **Proje Oluştur** olarak yeniden adlandırın.
5. **Eylem Adı** alanında, **msdyn\_CreateProjectV1** öğesini seçin.
6. **msdyn\_subject** alanının altında **Dinamik içerik ekle**'yi seçin.
7. **İfade** sekmesinde, işlev alanına **Proje adı - utcNow()** girin.
8. **Tamam**'ı seçin.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a>Adım 3: Takım üyesi için bir değişken başlatma

1. Akışta, **Yeni adım**'ı seçin.
2. **Bir işlem seçin** iletişim kutusunda, arama alanına **değişken başlat** yazın. Ardından, **Eylemler** sekmesinde, sonuç listesinden işlemi seçin.
3. Yeni adımda, üç noktayı (**...**) ve ardından **Yeniden Adlandır**'ı seçin.
4. Adımı, **Takım üyesini başlat** olarak yeniden adlandırın.
5. **Ad** alanına **TeamMemberAction** yazın.
6. **Tür** alanında **Dize**'yi seçin.
7. **Değer** alanına **msdyn\_CreateTeamMemberV1** yazın.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a>4. Adım: Genel bir takım üyesi oluşturma

1. Akışta, **Yeni adım**'ı seçin.
2. **Bir işlem seçin** iletişim kutusunda, arama alanına **bağlı olmayan eylem gerçekleştir** yazın. Ardından, **Eylemler** sekmesinde, sonuç listesinden işlemi seçin.
3. Yeni adımda, üç noktayı (**...**) ve ardından **Yeniden Adlandır**'ı seçin.
4. Adımı, **Takım Üyesi Oluştur** olarak yeniden adlandırın.
5. **Eylem Adı** alanı için, **Dinamik içerik** iletişim kutusunda **TeamMemberAction**'ı seçin.
6. **Eylem Parametreleri** alanına aşağıdaki parametre bilgilerini girin.

    ```
    {
        "TeamMember": {
            "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projectteam",
            "msdyn_projectteamid": "@{guid()}",
            "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
            "msdyn_name": "ScheduleAPIDemoTM1"
        }
    } 
    ```

    Parametrelerin açıklamasını aşağıda bulabilirsiniz:

    - **\@\@odata.type** – Varlık adı. Örneğin, **"Microsoft.Dynamics.CRM.msdyn\_projectteam"** yazın.
    - **msdyn\_projectteamid** – Proje takımı kimliğinin birincil anahtarı. Değer, genel olarak benzersiz bir tanımlayıcı (GUID) ifadesidir.   Kimlik, ifade sekmesinden oluşturulur.

    - **msdyn\_project\@odata.bind** – Sahip olunan projenin proje kimliği. Değer olarak, "Proje Oluştur" adımının yanıtından gelen dinamik içerik kullanılır. Tam yolu girdiğinizden ve parantezler arasına dinamik içerik eklediğinizden emin olun. Tırnak işaretleri gereklidir. Örneğin, **"/msdyn\_projects(ADD DYNAMIC CONTENT)"** yazın.
    - **msdyn\_name** – Takım üyesinin adı. Örneğin, **"ScheduleAPIDemoTM1"** yazın.

## <a name="step-5-create-an-operation-set"></a><a id="5"></a>Adım 5: İşlem Kümesi oluşturma

1. Akışta, **Yeni adım**'ı seçin.
2. **Bir işlem seçin** iletişim kutusunda, arama alanına **bağlı olmayan eylem gerçekleştir** yazın. Ardından, **Eylemler** sekmesinde, sonuç listesinden işlemi seçin.
3. Yeni adımda, üç noktayı (**...**) ve ardından **Yeniden Adlandır**'ı seçin.
4. Adımı **İşlem Kümesi Oluştur** olarak yeniden adlandırın.
5. **Eylem Adı** alanında, **msdyn\_CreateOperationSetV1** Dataverse özel eylemini seçin.
6. **Açıklama** alanına **ScheduleAPIDemoOperationSet** yazın.
7. **Proje** alanına **/msdyn\_projects(** yazın.
8. **Dinamik içerik** iletişim kutusunda, **msdyn\_CreateProjectV1Response ProjectId** öğesini seçin.
9. **Proje** alanına **)** yazın.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a>6. Adım: Proje paketi oluşturma

1. Akışta, **Yeni adım**'ı seçin.
2. **Bir işlem seçin** iletişim kutusunda, arama alanına **yeni satır ekle** yazın. Ardından, **Eylemler** sekmesinde, sonuç listesinden işlemi seçin.
3. Yeni adımda, üç noktayı (**...**) ve ardından **Yeniden Adlandır**'ı seçin.
4. Adımı **Paket Oluştur** olarak yeniden adlandırın.
5. **Tablo Adı** alanında, **Proje Paketleri**'ni seçin.
6. **Ad** alanına **ScheduleAPIDemoBucket1** yazın.
7. **Proje** alanı için, **Dinamik içerik** iletişim kutusunda **msdyn\_CreateProjectV1Response ProjectId** öğesini seçin.

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a>Adım 7: Bağlantı durumu için değişken başlatma

1. Akışta, **Yeni adım**'ı seçin.
2. **Bir işlem seçin** iletişim kutusunda, arama alanına **değişken başlat** yazın. Ardından, **Eylemler** sekmesinde, sonuç listesinden işlemi seçin.
3. Yeni adımda, üç noktayı (**...**) ve ardından **Yeniden Adlandır**'ı seçin.
4. Adımı **LinkStatus başlat** olarak yeniden adlandırın.
5. **Ad** alanında, **linkstatus** yazın.
6. **Tür** alanında **Tam sayı**'yı seçin.
7. **Değer** alanına **192350000** yazın.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a>Adım 8: Görev sayısı için bir değişken başlatma

1. Akışta, **Yeni adım**'ı seçin.
2. **Bir işlem seçin** iletişim kutusunda, arama alanına **değişken başlat** yazın. Ardından, **Eylemler** sekmesinde, sonuç listesinden işlemi seçin.
3. Yeni adımda, üç noktayı (**...**) ve ardından **Yeniden Adlandır**'ı seçin.
4. Adımı **Görev sayısı başlangıcı** olarak yeniden adlandırın.
5. **Ad** alanında, **görev sayısı** yazın.
6. **Tür** alanında **Tam sayı**'yı seçin.
7. **Değer** alanına **5** yazın.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a>Adım 9: Proje görev kimliği için değişken başlatma

1. Akışta, **Yeni adım**'ı seçin.
2. **Bir işlem seçin** iletişim kutusunda, arama alanına **değişken başlat** yazın. Ardından, **Eylemler** sekmesinde, sonuç listesinden işlemi seçin.
3. Yeni adımda, üç noktayı (**...**) ve ardından **Yeniden Adlandır**'ı seçin.
4. Adımı **ProjectTaskID başlat** olarak yeniden adlandırın.
5. **Ad** alanında, **görev sayısı** yazın.
6. **Tür** alanında **Dize**'yi seçin.
7. **Değer** alanı için ifade oluşturucusuna **guid()** ifadesini girin.

## <a name="step-10-do-until"></a><a id="10"></a>Adım 10: Bitiş noktası

1. Akışta, **Yeni adım**'ı seçin.
2. **İşlem seçin** iletişim kutusunda, arama alanına **Bitiş noktası** yazın. Ardından, **Eylemler** sekmesinde, sonuç listesinden işlemi seçin.
3. Koşullu bildirimdeki ilk değeri, **Dinamik içerik** iletişim kutusundan **görev sayısı** değişkeni olarak ayarlayın.
4. Koşulu **küçüktür veya eşittir** olarak ayarlayın.
5. Koşullu ifadedeki ikinci değeri **0** olarak ayarlayın.

## <a name="step-11-set-a-project-task"></a><a id="11"></a>Adım 11: Proje görevi belirleme

1. Akışta, **Yeni adım**'ı seçin.
2. **İşlem seçin** iletişim kutusunda, arama alanına **değişken ayarla** yazın. Ardından, **Eylemler** sekmesinde, sonuç listesinden işlemi seçin.
3. Yeni adımda, üç noktayı (**...**) ve ardından **Yeniden Adlandır**'ı seçin.
4. Adımı **Proje Görevini Ayarla** olarak yeniden adlandırın.
5. **Ad** alanında, **msdyn\_projecttaskid** öğesini seçin.
6. **Değer** alanı için ifade oluşturucusuna **guid()** ifadesini girin.

## <a name="step-12-create-a-project-task"></a><a id="12"></a>12. Adım: Proje görevi oluşturma

Geçerli projeye ve oluşturduğunuz proje paketine ait benzersiz bir kimliğe sahip bir proje görevi oluşturmak için bu adımları izleyin.

1. Akışta, **Yeni adım**'ı seçin.
2. **Bir işlem seçin** iletişim kutusunda, arama alanına **bağlı olmayan eylem gerçekleştir** yazın. Ardından, **Eylemler** sekmesinde, sonuç listesinden işlemi seçin.
3. Adımda, üç noktayı (**...**) ve ardından **Yeniden adlandır**'ı seçin.
4. Adımı **Proje Görevi Oluştur** olarak yeniden adlandırın.
5. **Eylem Adı** alanında, **msdyn\_PssCreateV1** öğesini seçin.
6. **Varlık** alanına aşağıdaki parametre bilgilerini girin.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
        "msdyn_subject": "ScheduleAPIDemoTask1",
        "msdyn_projectbucket@odata.bind": "/msdyn_projectbuckets(@{outputs('Create_Project_Buckets')?['body/msdyn_projectbucketid']})",
        "msdyn_start": "@{addDays(utcNow(), 1)}",
        "msdyn_scheduledstart": "@{utcNow()}",
        "msdyn_scheduledend": "@{addDays(utcNow(), 5)}",
        "msdyn_LinkStatus": "192350000"
    }
    ```

    Parametrelerin açıklamasını aşağıda bulabilirsiniz:

    - **\@\@odata.type** – Varlık adı. Örneğin, **"Microsoft.Dynamics.CRM.msdyn\_projecttask"** yazın.
    - **msdyn\_projecttaskid** – Görevin benzersiz kimliği. Değer, **msdyn\_projecttaskid** öğesinden dinamik bir değişkene ayarlanmalıdır.
    - **msdyn\_project\@odata.bind** – Sahip olunan projenin proje kimliği. Değer olarak, "Proje Oluştur" adımının yanıtından gelen dinamik içerik kullanılır. Tam yolu girdiğinizden ve parantezler arasına dinamik içerik eklediğinizden emin olun. Tırnak işaretleri gereklidir. Örneğin, **"/msdyn\_projects(ADD DYNAMIC CONTENT)"** yazın.
    - **msdyn\_subject** – Herhangi bir görev adı.
    - **msdyn\_projectbucket\@odata.bind** – Görevleri içeren proje paketi. Değer, "Paket Oluştur" adımının yanıtından gelen dinamik içerik olacaktır. Tam yolu girdiğinizden ve parantezler arasına dinamik içerik eklediğinizden emin olun. Tırnak işaretleri gereklidir. Örneğin, **"/msdyn\_projectbuckets(ADD DYNAMIC CONTENT)"** yazın.
    - **msdyn\_start** – Başlangıç tarihi için dinamik içerik. Örneğin, yarın **"addDays(utcNow(), 1)"** olarak gösterilir.
    - **msdyn\_scheduledstart** – Zamanlanan başlangıç tarihi. Örneğin, yarın **"addDays(utcNow(), 1)"** olarak gösterilir.
    - **msdyn\_scheduleend** – Zamanlanan bitiş tarihi. Gelecekte bir tarih seçin. Örneğin, **"addDays(utcNow(), 5)"** seçeneğini belirtin.
    - **msdyn\_LinkStatus** – Bağlantı durumu. Örneğin, **"192350000"** adresini girin.

7. **OperationSetId** alanı için **Dinamik içerik** iletişim kutusunda **msdyn\_CreateOperationSetV1Response** öğesini seçin.

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a>Adım 13: Kaynak ataması oluşturma

1. Akışta, **Yeni adım**'ı seçin.
2. **Bir işlem seçin** iletişim kutusunda, arama alanına **bağlı olmayan eylem gerçekleştir** yazın. Ardından, **Eylemler** sekmesinde, sonuç listesinden işlemi seçin.
3. Adımda, üç noktayı (**...**) ve ardından **Yeniden adlandır**'ı seçin.
4. Adımı **Atama Oluştur** olarak yeniden adlandırın.
5. **Eylem Adı** alanında, **msdyn\_PssCreateV1** öğesini seçin.
6. **Varlık** alanına aşağıdaki parametre bilgilerini girin.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_resourceassignment",
        "msdyn_resourceassignmentid": "@{guid()}",
        "msdyn_name": "ScheduleAPIDemoAssign1",
        "msdyn_taskid@odata.bind": "/msdyn_projecttasks(@{variables('msdyn_projecttaskid')})",
        "msdyn_projectteamid@odata.bind": "/msdyn_projectteams(@{outputs('Create_Team_Member')?['body/TeamMemberId']})",
        "msdyn_projectid@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})"
    }
    ```

7. **OperationSetId** alanı için **Dinamik içerik** iletişim kutusunda **msdyn\_CreateOperationSetV1Response** öğesini seçin.

## <a name="step-14-decrement-a-variable"></a><a id="14"></a>Adım 14: Değişkeni azaltma

1. Akışta, **Yeni adım**'ı seçin.
2. **İşlem seçin** iletişim kutusunda, arama alanına **azaltma değişkeni** yazın. Ardından, **Eylemler** sekmesinde, sonuç listesinden işlemi seçin.
3. **Ad** alanında, **görev sayısı**'nı seçin.
4. **Değer** alanına **1** yazın.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a>15. Adım: Proje görevini yeniden adlandırma

1. Akışta, **Yeni adım**'ı seçin.
2. **Bir işlem seçin** iletişim kutusunda, arama alanına **bağlı olmayan eylem gerçekleştir** yazın. Ardından, **Eylemler** sekmesinde, sonuç listesinden işlemi seçin.
3. Adımda, üç noktayı (**...**) ve ardından **Yeniden adlandır**'ı seçin.
4. Adımı **Proje Görevini Yeniden Adlandır** olarak yeniden adlandırın.
5. **Eylem Adı** alanında, **msdyn\_PssUpdateV1** öğesini seçin.
6. **Varlık** alanına aşağıdaki parametre bilgilerini girin.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. **OperationSetId** alanı için **Dinamik içerik** iletişim kutusunda **msdyn\_CreateOperationSetV1Response** öğesini seçin.

## <a name="step-16-run-an-operation-set"></a><a id="16"></a>Adım 16: İşlem Kümesi çalıştırma

1. Akışta, **Yeni adım**'ı seçin.
2. **Bir işlem seçin** iletişim kutusunda, arama alanına **bağlı olmayan eylem gerçekleştir** yazın. Ardından, **Eylemler** sekmesinde, sonuç listesinden işlemi seçin.
3. Adımda, üç noktayı (**...**) ve ardından **Yeniden adlandır**'ı seçin.
4. Adımı **İşlem Kümesi Yürüt** olarak yeniden adlandırın.
5. **Eylem Adı** alanında, **msdyn\_ExecuteOperationSetV1** öğesini seçin.
6. **OperationSetId** alanı için **Dinamik içerik** iletişim kutusunda **msdyn\_CreateOperationSetV1Response OperationSetId** öğesini seçin.

## <a name="references"></a>Başvurular

- [Akışların Dataverse ile nasıl tümleştirildiğine genel bakış - Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [Zamanlama varlıkları ile işlemler gerçekleştirmek için Proje zamanlama API'larını kullanma](schedule-api-preview.md)
- [Bulut akışlarına genel bakış - Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [Çözüm odaklı akışlara genel bakış - Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
