---
title: Fırsat üst bilgisi/özeti
description: Bu konuda, proje tabanlı anlaşmalar ve proje tabanlı fırsat satırları hakkında bilgiler sağlanmaktadır.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1344e21d58fbc28198468146f9cea9cf00572d7d
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181251"
---
# <a name="opportunity-settings"></a>Fırsat ayarları

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_


Fırsat başlığı veya özeti, proje tabanlı bir fırsattaki tüm satırlar için geçerli olan proje tabanlı bir anlaşma hakkında genel bilgileri yakalar.

Dynamics 365 Project Operations'taki proje tabanlı fırsatlar Dynamics 365 Sales'teki fırsatların uzantılarıdır. Bu uzantılar, proje tabanlı fırsatlara özgü ve bunlar için gerekli olan ek işlevsellik sağlar. Bu uzantılar, proje tabanlı fırsatlarda bulunan yeni alanları ve şerit eylemleri içerebilir. Sales'te kullanılan bazı alanların, işlevlerin ve varsayılan mantığın Project Operations'ta kullanılmadığını görebilirsiniz.

Aşağıdaki tabloda bir proje tabanlı fırsattaki Project Operations'a özgü veya Sales'teki Fırsatlardan bazı önemli davranış değişikliklerine sahip alanlar bulunmaktadır.

| **Alan** | **Konum** | **Açıklama** | **Aşağı yönlü etki** |
| --- | --- | --- | --- |
| Tür | Genel sekmesi (gizli) | Bu seçenek kümesi alanında aşağıdaki seçenekler bulunur:</br>- İş tabanlı (yalnızca Project Operations ile kullanılabilir)</br>- Öğe tabanlı (yalnızca Project Operations ve Sales yüklendiğinde kullanılabilir)</br>- Servis bakımı tabanlı (Field Service yüklendiğinde kullanılabilir) | Project Operations kullandığınızda bu alan değeri, Fırsatı proje tabanlı olarak sınıflandıran **İş tabanlı** değerine otomatik olarak ayarlanır. Fırsat, bu anlaşma için aşağı yönlü satış sürecinde projeye özgü tüm uzantıları ve işlevleri etkinleştirmek için proje tabanlı olmalıdır. |
| Sahibi Olan Şirket | Genel sekmesi | Bu, müşteriye projeyi teslim edecek şirket veya tüzel kişiliktir. | Bu alan bilgisi, bu Fırsattan oluşturulan Proje teklifindeki ilgili alana kopyalanır. |
| İletişim | Genel sekmesi | Bu anlaşma için müşterinin birincil ilgili kişisine başvurun. | |
| Hesap | Genel sekmesi | Müşterinin şirket veya firma kaydına başvuru. | |
| Firma Yöneticisi | Genel sekmesi | Bu proje tabanlı fırsat için Firma yöneticisinin adı. | Firma yöneticisi, bu projenin tamamlanmasından sonra müşteriyle ilişkiyi yönetmekten sorumludur. Firma yöneticisine bağlı ayrılabilir kaynak kaydına göre sözleşme yapan birim varsayılan olarak ayarlanır. |
| Sözleşme Birimi | Genel sekmesi | Bu anlaşmayla ilişkili projenin veya projelerin tesliminden sorumlu olan Kuruluş birimi. | Sözleşme yapan birim, şirketin anlaşma tamamlandıktan sonra projeleri yürüten bölümüdür. Sözleşme yapan her biriminin bir para birimi vardır ve bu para birimi, proje sırasında oluşan tahmini ve gerçek maliyetleri bildirmek için kullanılır. |

Fırsatın **Özet** sekmesindeki diğer tüm alanlar ve bölümler için bkz. [Fırsat oluşturma veya düzenleme (Sales ve Satış Merkezi)](https://docs.microsoft.com/dynamics365/sales-enterprise/create-edit-opportunity-sales).
