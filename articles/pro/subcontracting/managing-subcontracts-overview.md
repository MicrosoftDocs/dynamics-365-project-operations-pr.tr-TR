---
title: Project Operations'da alt sözleşme yönetimi
description: Bu makale, tipik proje tabanlı organizasyonlardaki uçtan uca taşeron yönetimi işlemine genel bir bakış sağlar.
author: rumant
ms.date: 08/02/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8f5e025b5f741935494349fb1bdfd3a19bacb5e1
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911529"
---
# <a name="subcontract-management-in-project-operations"></a>Project Operations'da alt sözleşme yönetimi

[!include [banner](../../includes/dataverse-preview.md)]

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Bu makale, proje tabanlı organizasyonlardaki uçtan uca taşeron yönetimi işlemine genel bir bakış sağlar. Hizmetler için alt sözleşme yapma işlemi, tipik olarak aşağıdaki diyagramda gösterilen iş süreci akışını izler.

![Taşeron işlem akışı](../media/SubcontractingProcessFlow.png)

Aşağıdaki listede, alt sözleşme sürecinin adım adım açıklaması sunulmaktadır.

1. Proje yöneticisi bir satıcıyla taşeron oluşturur. Varsayılan olarak, taşeron için satıcı kaydına iliştirilmiş fiyat listeleri kullanılır. Satıcı hesabının **satıcı** veya **tedarikçi** ilişki türü vardır.
2. Proje yöneticisi tüm satınalmaları taşeronda satır maddeleri olarak listeleyebilir. Taşeron satırları zaman, masraf veya ürünler için olabilir. Alt sözleşme satırının işlem sınıfı, satırın ne için olduğunu belirler.
3. Satıcı hesap yöneticisi ve proje yöneticisi taşeron üzerinden yineleme yapabilir. Fiyatlandırma alt sözleşmeye ekli olan satın alma fiyat listelerinde ayarlanabilir.
4. Bu noktada veya işlemin ilerleyen kısmında, alt sözleşme satırı zaman içinse, satıcı hesap yöneticisi satıcı ilgili kişilerini her bir alt sözleşme satırıyla ilişkilendirir. Bu ilişkilendirme, taşeron üzerinde çalışan proje yöneticisine bilgi sağlar. Bir satıcı ilgili kişisi alt sözleşme satırıyla ilişkilendirildiğinde, ayrılabilir bir kaynak yoksa sistem, ilgili kişiden otomatik olarak ayrılabilir bir kaynak oluşturur.
5. Her taşeron satırındaki faturalama yöntemi **Sabit Fiyat** veya **Zaman ve Malzeme** olabilir. Sabit fiyatlı alt sözleşme satırları için kilometre taşı tabanlı bir fatura zamanlaması ayarlanır.
6.  Alt sözleşme ayarlandıktan ve anlaşma tamamlandıktan sonra, onaylanır. Onaylanan alt sözleşmelerde düzenleme yapılamaz ancak değişiklikler olursa alt sözleşme 'düzenlemeler için yeniden açılabilir'; durumu **Onaylandı** yerine **Taslak** durumuna döner ve anlaşma yeniden açılabilir. 
7.  Bir projede bir genel takım üyesi oluştururken, takım üyesi bir alt sözleşme satırıyla ilişkilendirilebilir. Bu, alt yüklenici kapasitesiyle genel takım üyesi işe alma gereksinimini gösterir.
8.  Adlandırılmış takım üyeleri doğrudan proje üzerinde veya kaynak zamanlama deneyimleri kullanılıp ayrılarak oluşturulabilir. Adlandırılmış bir proje takımı üyesi sözleşmeli bir çalışansa, bunu bir alt sözleşme satırıyla ilişkilendirebilirsiniz. Bu, bir alt sözleşme satırındaki kullanılabilir kapasiteyi aşağıya çeker.
9.  Alt yüklenici kaynakları projelerde ve proje görevlerinde zaman, gider ve malzeme kullanımını kaydedip ardından onay için gönderebilirler. Bu çalışanlar için de aynıdır. Zamanı kaydederken, sözleşmeli çalışan belirli bir alt sözleşme ve alt sözleşme satırını seçebilir.
10. Onay sonrasında, alt sözleşmeler tarafından onaylanan zaman proje maliyeti fiili değerlerini, sözleşmeli çalışanın satın alma fiyatına veya projede gerçekleştirilen role göre kaydeder.
11. Satıcı faturaları ve satıcı fatura kalemleri, satıcı kaynakları tarafından gerçekleştirilen iş veya satıcı tarafından sağlanan ürünler için sisteme kaydedilebilir. Satıcı faturası satırları bir projeye özel ve bir zaman, gider, ürün/malzeme, kilometre taşı ya da ücret işlem sınıfında olmalıdır. İsteğe bağlı olarak, satıcı faturası satırları bir alt sözleşme satırına referansta bulunabilir.
12. Sistem, alt sözleşme satırı ve projeyle eşleşen tüm maliyet fiili değerlerini otomatik olarak satıcı faturasıyla ilişkilendirir. Bu,3 yönlü eşleştirme ve doğrulama işlemini kolaylaştırır.
13. Proje yöneticisi otomatik olarak eşleştirilen proje fiili değerlerini inceleyebilir, diğer proje maliyet değerlerini kaldırabilir veya ekleyebilir ve doğrulama işlemini tamamlayabilir.
14. Tüm satırlarda doğrulama işleminin tamamlanması, satıcı faturasını **Ödeme için hazır** olarak işaretler. Bu aşamada, satıcı faturası ve satırları, satıcıya ödemeyi işlemek için bir Muhasebe veya Borç sistemine aktarılabilir. Önceden kaydedilen proje maliyetleri tersine çevrilir ve satıcı fatura satırındaki fiili maliyetler projeye kaydedilir.

## <a name="quantity-based-subcontract-lines-and-work-based-subcontract-lines"></a>Miktar tabanlı alt sözleşme satırları ve iş tabanlı alt sözleşme satırları

Alt sözleşme satırı miktar tabanlı veya iş tabanlı olabilir. 

Bir alt sözleşme satırı **Miktar tabanlı** olduğunda, zaman, gider veya malzeme alt sözleşme satırındaki satın alınan miktar herhangi bir projede kullanılabilir.

Bir alt sözleşme satırı **İş tabanlı** olduğunda, alt sözleşme satırı proje planındaki bir düğümle temsil edilen bir iş gövdesiyle eşlenir. Alt sözleşme satırının değeri, ilgili işi teslim etmek için gerekli olan tüm bileşenlerin toplamıdır. Bunlar, alt sözleşme satırı ayrıntıları olarak modellenir ve bir zaman, gider veya malzeme koleksiyonu olabilir. İş tabanlı alt sözleşme satırı için, alt sözleşme satırı aynı zamanda tek bir projeye tahsis edilmiş olur. Bu tür alt sözleşmeler şu anda Project Operations tarafından desteklenmemektedir.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

