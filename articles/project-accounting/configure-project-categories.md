---
title: Proje kategorilerini yapılandırma
description: Bu konuda, proje kategorilerini ayarlama hakkında bilgiler sağlanmaktadır.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b7adf61a82714a0148d9c8b1d2b2b37fd611c1cf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287532"
---
# <a name="configure-project-categories"></a>Proje kategorilerini yapılandırma

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Project Operations, projelerde gelir ve giderleri kategorilere ayıran güçlü özellikler sunar. Kategoriler, proje işlemlerini raporlayıp analiz etme ve genel muhasebe defterine nakletme işlemini yönlendirme olanağı sağlar.

Aşağıdaki diyagramda, işlem kategorileri, paylaşılan kategoriler ve proje kategorileri arasındaki bağıntı gösterilmektedir. 

İşlem kategorileri, proje işlemlerinin temel gruplarıdır. Bu grupların içinde, uygulamalar ve modüller arasında paylaşılabilen bir dizi paylaşılan kategori bulunur. Daha fazla ayrıntı vermek gerekirse proje kategorileri en ayrıntılı kategori düzeyidir. Proje kategorileri tüzel kişiliğe, modüle ve uygulamaya özeldir.

![İşlem kategorileri, paylaşılan kategoriler ve proje kategorileri arasındaki bağıntı](media/project-categories.png)

## <a name="transaction-categories"></a>Hareket kategorileri

İşlem kategorileri, proje işlemlerinin temel gruplarını temsil eder ve şirkete veya işlem türüne özgü değildir. Örneğin, Contoso Robotics, Proje işlemlerini gruplandırmak için Tasarım, Seyahat, Kurulum ve Servis İşlemi kategorilerini kullanır.

İşlem kategorileri Project Operations modülünde tanımlanır. 
1. Formu açmak için **Ayarlar** \> **İşlem Kategorileri**'ne gidin. 
2. **Yeni**'yi veya **Excel'den içeri aktar**'ı seçerek yeni bir işlem kategorisi oluşturun.

## <a name="shared-categories"></a>Paylaşılan kategoriler

Dynamics 365; Dynamics 365 Finance, Dynamics 365 Supply Chain ve Dynamics 365 Project Operations gibi farklı uygulamalarda giderleri kategorilere ayırmak için Paylaşılan kategoriler kavramını kullanır. Oluşturulan her İşlem kategorisi için Project Operations, otomatik olarak dört ilgili Paylaşılan kategori oluşturur: Saat, Gider, Ücretler ve Öğe. **Proje yönetimi ve muhasebe** \> **Kurulum** \> **Kategoriler** \> **Paylaşılan Kategoriler**'e giderek paylaşılan kategorileri inceleyip ayarlayabilirsiniz.

## <a name="project-categories"></a>Proje kategorileri

Proje kategorileri, kategori yapılandırmasının en ayrıntılı düzeyini temsil eder ve ayrı olarak ve her şirket için bir Proje muhasebecisi tarafından yapılandırılmalıdır.

1. **Proje Yönetimi ve Muhasebe** \> **Kurulum** \> **Kategoriler** \> **Proje kategorileri**'ne gidin.
2. **Yeni**'yi seçin.
3. Önceki bölümde oluşturduğunuz Paylaşılan kategorinin **Kategori Kimliği**'ni seçin. Project Operations, yalnızca işlem kategorileriyle ilişkili paylaşılan kategorilerin kullanılmasına izin verir.
4. Kategori grubu seçin.

## <a name="category-groups"></a>Kategori grupları

Kategori grupları, ilgili Proje kategorileri arasında öncelikle deftere nakil profilleri olmak üzere özellikleri paylaşmak için kullanılır. Her işlem türü için en az bir kategori grubu olmalıdır ve her proje kategorisi bir gruba atanır.

Project Operations'ta deftere nakil özellikleri, proje maliyeti ve gelir profili kuralları, proje kategorileri ve kategori grupları ile tanımlanır. **Proje yönetimi ve muhasebe** \> **Kurulum** \> **Kategoriler** \> **Kategori grupları**'na giderek kategori gruplarını ayarlayabilirsiniz.


[!INCLUDE[footer-include](../includes/footer-banner.md)]