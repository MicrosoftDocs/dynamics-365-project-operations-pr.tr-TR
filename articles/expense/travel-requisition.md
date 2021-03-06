---
title: Seyahat talepleri
description: Bu konuda, seyahat talepleri hakkında bilgiler sağlanmaktadır.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 0261405abb9305d7f6abcde9cb90d9b184868580
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906368"
---
# <a name="travel-requisitions"></a>Seyahat talepleri

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Seyahat talebi, seyahat amacıyla oluşacak giderleri listeler. Seyahat talebi, incelenmek üzere gönderilir ve giderleri yetkilendirmek için kullanılabilir.

Kuruluştan tahsil edilecek giderleri oluşturmadan önce seyahat talebi göndermeniz gerekebilir. Bu gereksinim, giderleri şirket kredi kartından ödediğinizde, nakit avans olarak aldığınız nakdi harcadığınızda ya da kuruluşun tazmin edeceği cepten yapılan harcamalar durumunda da geçerlidir.

Seyahat talepleri ve ilkeler, kuruluşun giderlerini yönetmeye yardımcı olmak için kullanılabilir. Örneğin, kuruluşunuz seyahat yapılmasını gerektiren bir sabit fiyatlı projede çalışıyorsa projenin takım üyelerinin seyahat giderleri proje bütçesini aşmamalıdır. Seyahat giderlerinin harcanmadan önce onaylanmasını gerektirerek kuruluşun projenin bütçeyi aşmamasını sağlamasına yardımcı olabilir.

## <a name="configuration"></a>Yapılandırma 

Seyahat Talepleri, Gider Yönetimi Parametreleri'ndeki "Seyahatin önceden yetkilendirilmesi zorunludur" seçeneğini etkinleştirerek "zorunlu" olarak yapılandırılabilir. 

## <a name="create-and-submit-a-travel-requisition"></a>Seyahat talebi oluşturma ve gönderme

1. **Giderlerim: Seyahat Talebi**'ne gidin ve **Yeni Seyahat Talebi**'ni seçin.
2. Talep için bir amaç ve hedef girin.
3. **Seyahat açıklaması** alanında, diğer ek bilgileri girin. 
4. Uçuş, yemek veya araç kiralama gibi beklenen giderlerin her biri için bir gider satırı öğesi oluşturun. Her giderin tahmini tarihini, tahmini tutarını ve para birimini ekleyin. 
5. Beklenen giderleri eklemeyi bitirdiğinizde, **Kaydet**'i seçin.
6. Seyahat talebini göndermeye hazır olduğunuzda **İş Akışı** > **Gönder**'i seçin.

Onaylanan seyahat taleplerinizi **Giderlerim: Seyahat Talebi** altından görüntüleyebilirsiniz. 

## <a name="view-available-travel-requisitions"></a>Kullanılabilir seyahat taleplerini görüntüleme

Tüm seyahat taleplerinizi **Giderlerim: Seyahat Talepleri** altından görüntüleyebilirsiniz.

## <a name="approve-travel-requisitions"></a>Seyahat taleplerini onaylama

Onaylamak istediğiniz seyahat talebini seçin ve ardından **İş Akışı** > **Onayla** seçeneğini belirleyin.  

## <a name="submit-an-expense-report-using-your-approved-travel-requisition"></a>Onaylanmış seyahat talebinizi kullanarak bir gider raporu gönderme

1. Yeni bir gider raporu oluşturun ve gider raporu başlığında, onaylanmış seyahat talepleri listesinden **Seyahat talebine eşle**'yi seçin.
2. **Seyahat talebi tutarı** alanı, gider raporu başlığında otomatik olarak güncelleştirilir.
3. Yolculuk için oluşan her gideri ekleyin. **Önceden Yetkilendirilmiş** alanı etkinse belirli bir gider kategorisine ilişkin mutabık olunan tutar ve yetkilendirilmiş tutar güncelleştirilir.

> [!NOTE]
> Gider raporunu, onaylanmış bir seyahat talebiyle eşlediğinizde işlem tutarı, yetkilendirilmiş tutardan daha fazla olamaz. 
