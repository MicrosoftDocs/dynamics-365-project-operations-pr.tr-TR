---
title: Fırsat ayarları - lite
description: Bu konu proje tabanlı anlaşmalar ve proje tabanlı fırsat satırlarıyla ilgili bilgi sağlar.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4539a34cface9999c9cd029f8d44f835a8fe27ca
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994700"
---
# <a name="header-details-for-project-opportunities"></a>Proje fırsatları için üst bilgi ayrıntıları

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Fırsat üst bilgisi, proje tabanlı fırsattaki tüm satırlar için geçerli olan proje tabanlı bir anlaşma hakkında genel bilgileri yakalar.

Dynamics 365 Project Operations'ta proje tabanlı fırsatlar, Dynamics 365 Sales'teki fırsatların uzantılarıdır. Bu uzantılar, proje tabanlı fırsatlara özgü ve bunlar için gerekli olan ek işlevsellik sağlar. Bu uzantılar, proje tabanlı fırsatlarda bulunan yeni alanları ve şerit eylemleri içerebilir. Sales'te kullanılan bazı alanların, işlevlerin ve varsayılan mantığın Project Operations'ta kullanılmadığını görebilirsiniz.

Aşağıdaki tabloda bir proje tabanlı fırsattaki Project Operations'a özgü veya Sales'teki Fırsatlardan bazı önemli davranış değişikliklerine sahip alanlar bulunmaktadır.

| **Alan** | **Konum** | **Açıklama** | **Aşağı yönlü etki** |
| --- | --- | --- | --- |
| Tür | Genel sekmesi (gizli) | Bu seçenek kümesi alanında aşağıdaki seçenekler bulunur:</br>- İş tabanlı (yalnızca Project Operations ile kullanılabilir)</br>- Öğe tabanlı (yalnızca Project Operations ve Sales yüklendiğinde kullanılabilir)</br>- Servis bakımı tabanlı (Field Service yüklendiğinde kullanılabilir) | Project Operations kullandığınızda bu alan değeri, Fırsatı proje tabanlı olarak sınıflandıran **İş tabanlı** değerine otomatik olarak ayarlanır. Fırsat, bu anlaşma için aşağı yönlü satış sürecinde projeye özgü tüm uzantıları ve işlevleri etkinleştirmek için proje tabanlı olmalıdır. |
| İletişim | Genel sekmesi | Bu anlaşma için müşterinin birincil ilgili kişisine başvurun. | |
| Hesap | Genel sekmesi | Müşterinin şirket veya firma kaydına başvuru. | |
| Firma Yöneticisi | Genel sekmesi | Bu proje tabanlı fırsat için Firma yöneticisinin adı. | Firma yöneticisi, bu projenin tamamlanmasından sonra müşteriyle ilişkiyi yönetmekten sorumludur. Firma yöneticisine bağlı ayrılabilir kaynak kaydına göre sözleşme yapan birim varsayılan olarak ayarlanır. |
| Sözleşme Birimi | Genel sekmesi | Bu anlaşmayla ilişkili projenin veya projelerin tesliminden sorumlu olan Kuruluş birimi. | Sözleşme yapan birim, şirketin anlaşma tamamlandıktan sonra projeleri yürüten bölümüdür. Sözleşme yapan her biriminin bir para birimi vardır ve bu para birimi, proje sırasında oluşan tahmini ve gerçek maliyetleri bildirmek için kullanılır. |

Fırsatın **Özet** sekmesindeki diğer tüm alanlar ve bölümler için bkz. [Fırsat oluşturma veya düzenleme (Sales ve Satış Merkezi)](/dynamics365/sales-enterprise/create-edit-opportunity-sales)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
