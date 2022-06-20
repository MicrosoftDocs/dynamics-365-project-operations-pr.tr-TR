---
title: Güvenlik modeli
description: Bu makalede, Dynamics 365 Project Operations'taki güvenlik modeli hakkında bilgiler verilmektedir.
author: stsporen
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 2f4992b1ea0c2b93a83c6c2c9a146a7610afc5fe
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924546"
---
# <a name="security-model"></a>Güvenlik Modeli

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_



Microsoft Dynamics 365 Project Operations, Microsoft Office Grupları ile iş birliği yapan rol tabanlı bir iş güvenliği modeline izin veren benzersiz bir güvenlik modeli içerir. 


## <a name="security-roles"></a>Güvenlik rolleri
Project Operations ön uç özellikleri aşağıdaki rolleri içerir:

| Rol                          | Veri Akışı Açıklaması                                                                                                                                                                 | Scope |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| Uygulama yöneticisi              | Projeler arası raporlamayı destekler.                                                                                                            | İş birimi              |
| Projeyi onaylayan              | Projeyle ilgili zaman ve giderleri onaylar.                                                                                                                              | İş birimi |
| Proje faturalama yöneticisi | Fatura teklifini oluşturur.                                                                                                                                                 | İş birimi |
| Proje yöneticisi               | Proje planını oluşturur ve kaynakları ister.                                                                                                                              | İş birimi |
| Proje kaynağı              | Ayrılabilen ve zamanı raporlayan takım üyeleridir.                                                                                                          | İş birimi|
| Kaynak yöneticisi              | Karma Proje yöneticisi + Kaynak yöneticisi yapılandırmasını ve tek ve merkezi bir Kaynak yöneticisi rolünü desteklemek için ayrılmış, kaynak isteklerini ve ayırmaları karşılama gibi tüm kaynak yönetimi işlevleri. | İş birimi |


Web için Microsoft Project aşağıdaki rolleri içerir:

| Rol           | Veri Akışı Açıklaması                                                                                                        | Scope  |
|----------------|--------------------------------------------------------------------------------------------------------------------|--------|
| Proje kullanıcısı   | Kendi projelerini oluşturabilen ve kendisiyle paylaşılan projeleri görüntüleyebilen ve birlikte çalışılabilen Proje kullanıcısı. | Kullanıcı   |
| Proje sistemi | Uygulama bağlamı için kullanılan rol. Müşteriler bu sistem rolünü kullanmamalıdır.                                    | Global |

## <a name="security-enforcement"></a>Güvenlik uygulayıcı
Proje düzeyinde gerçekleştirilen eylemler, oturum açmış kullanıcı bağlamında gerçekleştirilir. Bu, bir proje oluşturmak, açmak veya silmek için kullanıcının CDS'ye mevcut bir erişimi olması gerektiği anlamına gelir. CDS'ye erişim, platforma dahil edilen olası mekanizmalardan herhangi biri aracılığıyla verilebilir. Örneğin, daha geniş kapsamı olan bir kullanıcı, projeye erişebilir veya açık proje paylaşma eylemi gerçekleştirilmişse kullanıcıya erişim verilir.

Project Operations'ta proje oluştururken bunu dikkate almak önemlidir.

## <a name="modern-group-collaboration-with-project-operations"></a>Project Operations ile modern grup işbirliği
Web için Project ve Project Operations, işbirliği için modern grupları destekler. Bir grup aracılığıyla projeye eklenen kullanıcılar, proje planını düzenleyebilir.

Web için Project, atamadan sonra kullanıcıları otomatik olarak gruba ekler.

Gruplar, proje izinleri ve destekleyici işbirliği yapıtları ile işbirliği içinde çalışılmasını sağlar. Aşağıdaki diyagramda, grup atama sürecinde meydana gelen olaylar ve durum değişiklikleri gösterilmektedir.

Project Operations, örtük eylem yoluyla bir grup oluşturmaz ve bunu yalnızca baskın grupların açık eylemi aracılığıyla gerçekleştirir.

**Grup yönetimi** iletişim kutusundaki grup üyesi araması, ortamın güvenlik grubunun bir parçası olarak ayarlananlarla sınırlıdır. Daha fazla bilgi için bkz. [Ortamlara kullanıcı erişimini denetleme: güvenlik grupları ve lisanslar](/power-platform/admin/control-user-access).

![Grup modu.](./media/groupsmode.png)

1. Proje, oluşturan Kullanıcı tarafından oluşturulur ve sahiplenilir.
2. Proje sahibi, takımla güncelleştirilir.
3. Sahibi olan takım, belirtilen veya oluşturulan Office Grubu ile eşlenir.
4. Projenin özgün sahibi, Office Grubuna eklenir.

## <a name="deployment-recommendation"></a>Dağıtım önerisi
Office grubu işbirliği modeli geliştikçe, zaman içinde daha ayrıntılı kontrol sağlamayan işlevler eklenecektir. Şu anda Project Operations'ı dağıtan müşterilerin geleneksel Microsoft Dynamics 365 güvenlik modeline odaklanmaları teşvik edilmektedir.

Daha fazla bilgi için bkz. [Common Data Service'te Güvenlik](/power-platform/admin/wp-security).

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a>Project Operations ve Microsoft Dynamics 365 Finance güvenliği
Project Operations aşağıdaki rolleri içerir:

- Proje yöneticisi
- Proje muhasebecisi

Finance'ta güvenlik hakkında daha fazla bilgi için bkz. [Rol tabanlı güvenlik](/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).




[!INCLUDE[footer-include](../includes/footer-banner.md)]