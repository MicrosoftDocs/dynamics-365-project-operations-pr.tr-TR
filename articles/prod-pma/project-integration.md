---
title: Microsoft Project Client tümleştirmesi
description: Proje zamanlamasını planlamak ve sürdürmek karmaşık olabilir, bu nedenle proje yöneticilerinin bu görevi yönetmesine yardımcı olacak araçları kullanmaları gerekir. Microsoft Project Client ile tümleştirme, bir proje iş kırılım yapısını açmak ve yönetmek için destek sağlar.
author: Yowelle
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: e93d23559d1f3aca9022cd97dae3b0726bb5ca05
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289348"
---
# <a name="microsoft-project-client-integration"></a>Microsoft Project Client tümleştirmesi

[!include [banner](../includes/banner.md)]

Proje zamanlamasını planlamak ve sürdürmek karmaşık olabilir, bu nedenle proje yöneticilerinin bu görevi yönetmesine yardımcı olacak araçları kullanmaları gerekir. Microsoft Project Client ile tümleştirme, bir proje iş kırılım yapısını açmak ve yönetmek için destek sağlar. Proje yöneticisi değişiklikleri Dynamics 365 Finance proje iş kırılım yapısına tekrar yayımlayabilir.

> [!NOTE]
> Temmuz güncelleştirmesi'ni (sürüm 10.0.4) kullanıyorsanız, KB 4054797 ve 4055884 yüklemelisiniz.

## <a name="configure-the-microsoft-project-client-add-in"></a>Microsoft Project Client eklentisini yapılandırma
Microsoft Project Client ile tümleştirmeyi etkinleştirmek için Microsoft Dynamics 365 eklentisinin kullanıcının istemci Microsoft Proje uygulamasında yüklenmesi gerekir. Bu, **Proje yönetimi çalışma alanı** açılarak yapılır.

• Çalışma alanının **Bağlantılar** > **Kurulum** bölümünden **Proje istemcisi eklentisini yapılandır** seçeneğini tıklayın.

• **Aç**'a tıklayıp ardından sorulduğunda **Çalıştır**'a tıklayın.

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>Microsoft Project Client'da var olan bir taslak iş kırılım yapısını açma ve düzenleme
Dynamics 365 Finance'deki bir projede iş kırılım yapısı oluşturulmuşsa, iş kırılım yapısı; taslak durumdaysa, Microsoft Project Client uygulamasında açılabilir. **Proje** sayfasında açmak için, **Plan** sekmesinden **Microsoft Project'te aç**'ı tıklayın. Bu sayfa, **Microsoft Dynamics 365** sekmesinden **Aç**'a tıklayarak Microsoft Project Client uygulaması içinden de açılabilir. Listeden **Yasal varlığı** ve **Proje**'yi seçin.

> [!NOTE]
> Tarayıcı olarak Internet Explorer uygulamasını kullanıyorsanız, dosyanın karşıdan yüklendiği konumdan el ile açmak için **Kaydet**'e tıklamanız gerekir. Veya dosyayı Microsoft Project Client'da açmak için **Kaydet ve Aç**'ı tıklayın. Kaydederken dosya adını yeniden adlandırmayın.

Microsoft Project Client'ı kullanarak dosyada herhangi bir değişiklik yapmadan önce, onu kullanıma almanız gerekir. **Microsoft Dynamics 365** sekmesinde **Kullanıma al**'a tıklayın. Bu, diğer kullanıcıların, iş kırılım yapısını aynı anda Finance içinden düzenlemelerini engeller. Herhangi bir düzenleme yaptıktan sonra iş kırılım yapısını yayımlamak için, **Microsoft Dynamics 365** sekmesinde **Teslim et** öğesini tıklayın.

Proje ekibi Finance içindeki projeye zaten eklenmişse, kaynak listesi takım üyeleriyle doldurulur. Proje ekibi henüz projeye eklenmemişse, **Microsoft Dynamics 365** sekmesindeki **Kaynaklar** düğmesini tıklayarak kaynakları seçebilir ve ekibi Microsoft Project Client içinde oluşturabilirsiniz. 

Aşağıdaki veriler teslim işleminin bir parçası olarak Finance ile eşitlenecek:

• Görev adı

• Başlangıç tarihi

• Bitiş tarihi

• Öncüller

• Kaynak adları

• Kategori

• Kaynak kategorisi

• Çalışma saatleri

• Notlar

• Öncelik

> [!NOTE]
> Microsoft Project Client dosyanıza başka sütunlar eklerseniz, bunlar dosyaya kaydedilmez ve dosya yeniden açıldığında görüntülenmez.

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Microsoft Project Client kullanarak var olan bir proje için iş kırılım yapısı oluşturma
Microsoft Project Client kullanarak iş kırılım yapısı oluşturmak için aşağıdaki adımları izleyin:


1.  Microsoft Project Client'ı açın.

2.  **Microsoft Dynamics 365** sekmesinde **Aç** öğesini tıklayın.

3.  Projeye ait **Yasal varlık** öğesini seçin.

4.  **Proje**'yi seçin.

5.  **Microsoft Dynamics 365** sekmesinde **Kullanıma al** seçeneğini tıklayın.

6.  Finance'te yayımlamaya hazır olduğunuzda, **Microsoft Dynamics 365** sekmesinde **Teslim et** öğesini tıklayın.

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Microsoft Project Client kullanarak var olan bir proje için var olan iş kırılım yapısını değiştirme
Microsoft Project Client'ı kullanarak yeni bir iş kırılım yapısı oluşturmak ve var olan bir proje için var olan bir iş kırılım yapısını değiştirmek için şu adımları izleyin:

1.  Microsoft Project Client'ı açın.

2.  Microsoft Project Client'da zamanlama oluşturun.

3.  **Microsoft Dynamics 365** sekmesinde, **Değişiklikleri kaydet** > **Varolan projeyi değiştir** seçeneğine tıklayın.

4.  Projeye ait **Yasal varlık** öğesini seçin.

5.  **Proje**'yi seçin.

6.  **Tamam**'a tıklayın.

## <a name="create-a-new-project-from-within-microsoft-project-client"></a>Microsoft Project Client içinden yeni proje oluşturma


1.  Microsoft Project Client'ı açın.

2.  Microsoft Project Client'da zamanlama oluşturun.

3.  **Microsoft Dynamics 365** sekmesinde, **Değişiklikleri kaydet** > **Yeni projeye kaydet** seçeneğine tıklayın.

4.  Projeye ait **Yasal varlık** öğesini seçin.

5.  Gerekirse **Proje kimliğini** girin.

6.  **Proje adını** girin.

7.  **Proje türünü**, **Proje grubunu** ve **Proje sözleşme kimliğini** seçin. Alternatif olarak, **Yeni**'yi tıklayarak yeni bir proje sözleşmesi oluşturabilirsiniz.

8.  Kaynak için kullanılacak **Takvimi** seçin.

11. **Tamam**'a tıklayın.


[!INCLUDE[footer-include](../includes/footer-banner.md)]