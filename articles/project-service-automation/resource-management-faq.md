---
title: Kaynak yönetimiyle ilgili SSS
description: Bu konu, kaynak yönetimi hakkında sık sorulan sorulara yanıt sağlar.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: fdf7f1e2-e4a2-4c68-aa03-4a41c7b10531
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 87da759b3b30ed6d38866c045194cde79837c209
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756687"
---
# <a name="resource-management-faq"></a>Kaynak yönetimiyle ilgili SSS

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a>Takım üyesi ile kaynak gereksinimi arasındaki fark nedir?

Proje takım üyesi ayrılmış veya fazladan ayrılmış görevlere atanabilir ve onaylayan olarak ayarlanabilir. Kaynak gereksinimi, bir proje takımı üyesi olmadan, talebin bir taslak notu olarak var olabilir. 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a>Önerilen saatler ve geçici ayrılan saatler arasındaki fark nedir?

Önerilen saatler ve geçici ayrılan saatler görünürlükte farklıdır. Önerilen saatler yalnızca kaynak yöneticileri ve talebi bir kaynak isteği kullanarak başlatan proje yöneticisi tarafından görünür. Geçici ayrılan saatler, Zamanlama Panosuna erişimi olan herkese görünür.

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a>Takımdaki kaynaklar için geçici ayrılan saatleri nasıl görebilirim?

Kaynak gereksinimi ayırdığınızda geçici ayırmalar yapılabilir. Proje takımında geçici ayrılan kaynaklar, geçici ayrılan saatleri olan takım üyeleri olarak görünür. Üyeler Zamanlama Panosunda da görünür.

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a>Ayırdığım bir kaynak için (genel veya adlandırılmış) gerekli saatleri ve başlangıç ile bitiş tarihlerini nasıl değiştiririm?

Kaynaklar ayrıldıktan sonra, gerekli değişiklikleri yapmak için **Ayırma İşlemlerini Koru**'yu seçin.

## <a name="what-resources-types-does-project-service-automation-support"></a>Project Service Automation hangi kaynak türlerini destekler?

Kaynak türlerinden yalnızca **Kullanıcı** ve **İlgili Kişi**, Dynamics 365 Project Service Automation'da desteklenir. Başka tür kaynaklar oluşturabilseniz de (örneğin, **Ekipman** ve **Grup**) bunlar için herhangi bir uçtan uca servis talebi desteklenmez.

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a>Atama ve ayırma arasındaki fark nedir?

Atamalar, kaynakların proje zamanlamasındaki proje görevlerine atanmasıdır. Kaynaklar, gerçek veya genel kaynak olabilir. Ayırmalar, kaynakların bir projeye kalıcı veya geçici tahsisatıdır. Kalıcı ayırmalar, bir kaynağın kapasitesini tüketir. İdeal olarak, gerçek kaynaklar için ayırma ve atamalar uyuşmalıdır çünkü farklı değillerdir. Ancak PSA bu uyuşmayı zorunlu kılmaz. Mutabakat görünümü; proje yöneticisine, bir kaynağın ayırma ve atamalarının uyuşmadığı yerleri gösterir.
