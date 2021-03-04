---
title: Proje takımı üyeleri
description: Bu konuda, proje takımı üyesinin bilgileri, öznitelikler ve zamanlama ile çalışma hakkında bilgiler sağlanmaktadır.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3985febf62a520619e05bbb9a307195009e4b100
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127452"
---
# <a name="project-team-members"></a>Proje takımı üyeleri

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Proje takımı üyeleri, bir proje üzerindeki çalışmayı tamamlayan proje katılımcılarıdır. Takım üyesi ızgarasının amacı, çalışmayı taahhüt eden adlandırılmış kaynakların ve yer tutucu kaynaklar olan ve daha sonra kadroya alınacak genel takım üyelerinin bir listesini sağlamaktır.

Proje yöneticisi ve diğer proje katılımcıları, projede kimlerin çalışacağını takım üyesi ızgarasından görme yeteneğine sahiplerdir. Ayrıca ayırmalarının özetini, planlanan çalışma süresini ve bireysel kaynak atamalarını görüntüleyebilirler. Takım üyesi ızgarası, Proje yöneticilerinin genel takım üyeleri için kaynak gereksinimlerini tanımlamalarına ve var olan takım üyelerinin ayırmalarını yönetmelerine olanak tanır.

Aşağıdaki tabloda bir proje takımı üyesinin temel öznitelikleri listelenmektedir.

| Alan adı          | Veri Akışı Açıklaması                                                                                                                                                                  |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tahsisat yöntemi        | Projede kaynakları ayırmak için kullanılan tahsisat yöntemi.                                                                         |
| Fatura Türü             | Takım üyesinin faturalanabilir olarak sınıflandırılıp sınıflandırılmayacağını seçin.                                                                                                                                       |
| Ayrılabilir Kaynak        | Genel kaynağın yerini almak üzere seçilen ayrılabilir kaynak.                                                                                                                   |
| Silme Durumu            | PSS'ye gönderilen bir silme isteği olup olmadığını ve PSS'nin başarılı şekilde ve beklenen zaman aralığında yanıt verip vermediğini izlemeye yönelik takım üyesi silme durumu. |
| Toplam Çalışma Süresi (Saat)     | Takım üyesinin atamalarındaki çalışmalarının toplamı.                                                                                                                         |
| Tamamlanan Çalışma Süresi (Saat) | Takım üyesinin atamalarında gerçekleştirdiği çalışmayı izler.                                                                                           |
| Kalan Çalışma Süresi (Saat) | Takım üyesinin atamalarında henüz gerçekleştirmediği çalışmayı izler.                                                                                    |
| Bitiş                   | Kaynak takım üyeliği bitiş tarihi.                                                                                                                                            |
| Kesin Ayrılan Saat Sayısı        | Takım üyesinin kesin olarak ayrılmış saatleri.                                                                                                                                                                |
| Pozisyon Adı            | Genel kaynağı tanımlamak için kullanılan ad.                                                                                                                                   |
| Kaynak Belirleme Birimi          | İşi yapan kaynağın kuruluş birimi.                                                                                                                      |
| Projeyi Onaylayan         | Takım üyesinin zaman ve giderleri onaylayıp onaylayamayacağını seçin.                                                                                                                     |
| Gerekli Saat Sayısı           | Takım üyesi gereksinimindeki takım üyesi için gereken saat sayısı.                                                                                                                       |
| Rol                     | Takım üyesinin bu takımda oynadığı rol.                                                                                                                                |
| Pozisyon Açıklaması     | Bu takım üyesinin rolünün açıklamasını girin.                                                                                                                             |
| Geçici Ayrılan Saat Sayısı        | Takım üyesinin geçici olarak ayrılmış saatleri.                                                                                                                                                                 |
| Başlat                    | Kaynak takım üyeliği başlangıç tarihi.                                                                                                                                          |

Takım üyesi ızgarasından aşağıdaki eylemler gerçekleştirilebilir:

- **Ayır**: Karma ayırma yönteminden yararlanan kuruluşlar için ayırma eylemi, kullanıcıların genel takım üyesinden oluşturulan kaynak gereksinimlerini temel alarak adlandırılmış bir kaynak ayrılmasına olanak tanır
- **Gereksinim Oluştur**: Bu eylem, gereksinimi oluşturur.
- **Desen Belirtin**: Proje yöneticilerinin kaynak gereksinimi sınırlarını ayrıntılı düzeyde ayarlamasına olanak tanır. Proje yöneticileri, varsayılan dağıtımın uygun olmadığı durumlarda sınırları projenin özel ihtiyaçlarına göre ayarlayabilir.
- **İstek Gönder**: Merkezi ayırma yöntemini kullanan kuruluşlar içindir.
- **Düzenle**: Kuruluş birimi, rol ve pozisyon adı da dahil olmak üzere takım üyesi öznitelikleri düzenlenebilir.
- **Ayırma İşlemlerini Koru**: Kaynak ayırmalarının güncelleştirilmesi gerektiğinde ayırma işlemlerini korumak Proje yöneticisinin aşağıdakileri ayarlamasına izin verir:

    - Başlat
    - End
    - Toplam çalışma tahsisatı

- **Yeni**: Proje yöneticileri, zamanlamayı kullanarak doğrudan kaynak eklemenin yanı sıra takım üyesi ızgarasından adlandırılmış veya genel takım üyelerine yenilerini ekleyebilir.
- **Sil**: Proje yöneticisi, artık projeye katılmayacak kaynakları bir veya daha fazla takım üyesi seçerek silebilir. Takım üyesinin silinmesi, ilişkili tüm kaynak atamalarını da siler ve var olan tüm ayırmaları iptal eder.


[!INCLUDE[footer-include](../includes/footer-banner.md)]