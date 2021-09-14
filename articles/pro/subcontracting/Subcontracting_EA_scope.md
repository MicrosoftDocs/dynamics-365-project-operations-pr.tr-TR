---
title: Ekim 2021 Erken Erişim sürümünde alt sözleşme yapma
description: Bu konu, Ekim 2021 erken erişim sürümünün parçası olan Project Operations alt sözleşme yeteneklerine genel bakış sağlar.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 21ec8355487b5e69fc5b68b11dca029e6dc04f3c
ms.sourcegitcommit: c7f891adb5c81654c01d00c6b39beed403058eb1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/14/2021
ms.locfileid: "7383719"
---
# <a name="subcontracting-in-october-2021-early-access-release"></a>Ekim 2021 Erken Erişim sürümünde alt sözleşme yapma

[!include [banner](../../includes/dataverse-preview.md)]

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Bu konu, Ekim 2021 erken erişim sürümünün parçası olan Dynamics 365 Project Operations alt sözleşme yeteneklerine genel bakış sağlar. Bu özellik kümesi, üretim ortamları veya canlı ortamlar için hazır değildir; bu nedenle bu özellikler tüm özellik kümesi yayımlanıncaya kadar erken erişim sürümünde kalacaktır. Önizleme başlığı kaldırılıncaya kadar, canlı üretim senaryolarına yönelik alt sözleşme özelliği kümesini kullanmamanız önerilir. 

Aşağıdaki listede, Ekim 2021 Erken Erişim sürümünde kullanılabilir olan özelliklerin özeti sunulmaktadır:

1. Proje yöneticisi bir satıcıyla taşeron oluşturur. Varsayılan olarak, taşeron için satıcı kaydına iliştirilmiş fiyat listeleri kullanılır. Satıcı hesabının **satıcı** veya **tedarikçi** ilişki türü vardır.

2. Proje yöneticisi tüm satınalmaları taşeronda satır maddeleri olarak listeleyebilir. Taşeron satırları zaman, masraf veya ürünler için olabilir. Alt sözleşme satırının işlem sınıfı, satırın ne için olduğunu belirler.

3. Satıcı hesap yöneticisi ve proje yöneticisi taşeron üzerinden yineleme yapabilir. Fiyatlandırma alt sözleşmeye ekli olan satın alma fiyat listelerinde ayarlanabilir.

4. Bu noktada veya işlemin ilerleyen kısmında, alt sözleşme satırı zaman içinse, satıcı hesap yöneticisi satıcı ilgili kişilerini her bir alt sözleşme satırıyla ilişkilendirir. Bu ilişkilendirme, taşeron üzerinde çalışan proje yöneticisine bilgi sağlar. Bir satıcı ilgili kişisi alt sözleşme satırıyla ilişkilendirildiğinde, ayrılabilir bir kaynak yoksa sistem, ilgili kişiden otomatik olarak ayrılabilir bir kaynak oluşturur.

5. Her taşeron satırındaki faturalama yöntemi **Sabit Fiyat** veya **Zaman ve Malzeme** olabilir. Sabit fiyatlı alt sözleşme satırları için kilometre taşı tabanlı bir fatura zamanlaması ayarlanır.

Genel bakışta özetlenen alt sözleşme için iş süreci akışındaki diğer adımlar şu anda kullanılamaz. Yeni işlev eklendikçe bu konu güncelleştirilir. 

Aşağıdaki örnek, Alt Sözleşme Erken Erişim sürecini uçtan uca iş süreciyle karşılaştırmaları olarak göstermektedir.

![Taşeron işlem akışı](../media/SubcontractingEAFlow.png)  


## <a name="quantity-based-and-work-based-subcontract-lines-early-access-release"></a>Miktar tabanlı ve iş tabanlı alt sözleşme satırları erken erişim sürümü
Ekim 2021 Erken Erişim sürümünde yalnızca miktar tabanlı alt sözleşme satırları desteklenmektedir. Bu, bir alt sözleşme satırının bir satıcıdan zaman, gider veya malzeme satın almak için kullanılabileceği ancak bir kişinin çalışmasının tamamı için kullanılmayacağı gelir. Ayrıca bu, bir alt sözleşme satırındaki satın alınan miktarın (zaman, gider veya malzeme miktarı) sistemdeki herhangi bir projede kullanılabileceği anlamına gelir.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
