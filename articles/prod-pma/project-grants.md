---
title: Proje izinleri
description: Bu konu, nasıl bir verme oluşturulacağını veya değiştirileceğini açıklar.
author: RadhikaRS
manager: AnnBe
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: dfd91e859244cc03b9b358b057bded79eeea0182
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289393"
---
# <a name="project-grants"></a>Proje izinleri

[!include [banner](../includes/banner.md)]

Verme, belirli bir amaç veya proje için para hediyendir. Genellikle, bir verme işlemiyle ilgili sınırlamalar vardır. Proje yönetimi ve muhasebesinde, izin verebilir ve izleyebilir ve bunların projelerine ve proje sözleşmelerine İlişkiler tanımlayabilirsiniz. Örneğin, aşağıdaki görevleri gerçekleştirebilirsiniz:

- İlişkilendir **Proje** ve **Proje sözleşmesi ayrıntıları** sayfalarına bağlantılar aracılığıyla projelerle kaynakları ve finansmanı sağlar .
- Bir durumundan diğerine hareket ederken, verme izni girin ve değişiklikleri izleyin.
- Maliyetleri, talep edilen tutarları girin ve miktarları izleyin.
- Ana şablon oluşturun ve onlarla alt izin vermeleri ilişkilendirin.

Tüm ayrıntıları yeni bir kayda girerek bir verme oluşturabilir veya varolan bir izin ayrıntıları kopyalayıp bunları güncelleştirebilirsiniz.

## <a name="create-a-new-grant"></a>Yeni izin oluşturun

1. **Proje yönetimi ve muhasebe** \> **İzinler** \> **İzinler** bölümüne gidin.
2. **Yeni** \> **İzin** seçin.
3. İzin verme Ayrıntıları sayfasının **genel** Hızlı sekmesinde, **izin verme kimliği** alanında, izin ver için alfanümerik bir tanımlayıcı girin.
4. **İzin Adı** kutusunda, izin için benzersiz bir ad girin.
5. **Açıklama** alanında, yeni izin ver hakkında ayrıntılı bilgi ekleyin.

    Sayfadaki diğer alanların çoğu isteğe bağlıdır ve istediğiniz kadar fazla bilgi girebilirsiniz.

    Aşağıdaki listede, ayrıntıları ver sayfasının her bir hızlı sekmesinde belirtilen bilgiler açıklanmaktadır:

    - **Genel** – İzin adını, durumunu, açıklamasını, amacını ve tutarını girin.
    - **İlgili kişi bilgileri** – Personel üyeleriyle ilgili ayrıntıları, izini yöneten departmanı ve iznin müşteri ya da organizasyon verme kaynağını girin. Ayrıca, organizasyonunuzun, izni alan ve sonra başka bir alıcıya aktaran bir doğrudan varlık olup olmadığını da belirtebilirsiniz. İzin sağlayan kuruluş için telefon numaraları ve e-posta adresleri gibi ilgili kişi bilgilerini eklemek için **Ekle**'yi seçin.
    - **Tarihler ve son tarihler** – İzin ve izin uygulamasıyla ilgili tarihleri girin. Örnekler arasında uygulama son tarihi, gönderim tarihi ve iznin onaylandığı veya reddedildiği tarih bulunur.
    - **İlişkili projeler ve proje sözleşmeleri** – yalnızca **genel** hızlı sekmesindeki **izin durumu** alanı **etkin** veya **verilen** olarak ayarlanmışsa , bu hızlı sekmeye bilgi girebilirsiniz. İlgili görevi gerçekleştirmek için aşağıdaki seçenekler arasından seçim yapın:

        - **Fon Kaynağı Ekle** – İzin için yeni bir fonlama kaynak ekleyin. Tüm ayrıntıları hemen girebilir veya varsayılan bilgileri kullanıp daha sonra güncelleştirebilirsiniz.
        - **Proje sözleşmesi Ekle** – Proje sözleşme bilgilerini ekleyin veya güncelleştirin.
        - **Proje Ekle** – proje ayrıntıları ekleyin veya güncelleştirin.

    - **Kurulum** – Bu bilgi gerekiyorsa, eşleşen fonlarla ilgili ayrıntıları girin. Ödül kazandıkları çoğu kuruluş, alıcıların verilen tutara verilen tutarla eşleşmesi için belirli bir miktarda para veya kaynak harcamalarına gerek duyar. **Yerel proje veya izleme kimliği** alanında, proje tanımlayıcısından farklı bir tanımlayıcı girebilirsiniz.

        > [!NOTE]
        > İzin öğesinin bir kısmı farklı bir kuruluşa kazanılır, **alt verici** seçeneğini **Evet** olarak ayarlayın. ABD 'de verilen izinler için, bir eyalet vekaleti veya federal vekalet altında bir izi olup olmayacağını belirtebilirsiniz.

    - **Alçalma ayrıntıları** – İzin fonlarının ne sıklıkla çekilebileceği, faturalanabileceği veya harcanabileceği hakkında bilgi ekleyin veya güncelleştirin.

## <a name="create-a-new-grant-from-a-copy"></a>Kopyadan yeni bir izin oluşturma

1. **Proje yönetimi ve muhasebe** \> **İzinler** \> **İzinler** bölümüne gidin.
2. **Yeni** \> **İzinden kopyala**'yı seçin.
3. Yeni izin ver için alfasayısal bir tanımlayıcı ve ad girin ve **Tamam** 'ı seçin.
4. Verme ayrıntıları sayfasında, kopyalanan kaydın ayrıntılarını gözden geçirin ve gerekli değişiklikleri yapın. Sayfadaki alanların çoğu isteğe bağlıdır.

## <a name="view-or-modify-grant-details"></a>İzin ayrıntılarını görüntüleme veya değiştirme

1. **Proje yönetimi ve muhasebe** \> **İzinler** \> **İzinler** bölümüne gidin.
2. Değiştirilecek izni seçin.
3. Eylem Bölmesi'ndeki **İzin** sekmesinde, **Sürüdr** grubunda **Düzenle** seçeneğini tıklayın.
4. İzin ayrıntılarını gözden geçirin ve gerekli değişiklikleri yapın.


[!INCLUDE[footer-include](../includes/footer-banner.md)]