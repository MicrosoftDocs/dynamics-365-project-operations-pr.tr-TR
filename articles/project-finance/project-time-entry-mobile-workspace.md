---
title: Project Time Entry mobil çalışma alanı
description: Bu konuda, Project time entry mobil çalışma alanı hakkında bilgi sağlanır. Bu çalışma alanı, kullanıcıların mobil cihazlarını kullanarak bir projeye zaman girmesini ve bunları kaydedebilmelerini sağlar.
author: KimANelson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: ee11f7f392676adb59bd25f6549737482faf5fdb
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756648"
---
# <a name="project-time-entry-mobile-workspace"></a>Project Time Entry mobil çalışma alanı

[!include [banner](../includes/banner.md)]

Bu konuda, **Project time entry** mobil çalışma alanı hakkında bilgi sağlanır. Bu çalışma alanı, kullanıcıların mobil cihazlarını kullanarak bir projeye zaman girmesini ve bunları kaydedebilmelerini sağlar.

Bu mobil çalışma alanı, Dynamics 365 Unified Ops mobil uygulaması birlikte kullanılmak üzere tasarlanmıştır. 

## <a name="overview"></a>Genel bakış
Günlük çalışmanın bir parçası olarak, proje kaynakları çoğu zaman tesiste veya seyahat halinde bulunur. **Proje zaman girişi** mobil çalışma alanı, kullanıcıların, seçtikleri mobil cihazda bir projeye ilişkin faturalandırılabilir veya faturalandırılamayan bir süre girmesine izin verir. Bu nedenle, proje kaynakları zaman girişlerini istedikleri zaman ve bir istedikleri bir yerde kaydedebilir. Kaydedilmiş olan saat girişlerini de görebilirler. 

Özellikle, **Proje time entry** mobil çalışma alanında, kullanıcılar şu görevleri gerçekleştirebilir:

-   Seçili herhangi bir tarih için, belirli bir görevde harcadığınız saat sayısını girme.
-   Zaman girilecek projeyi bulmak için proje adına veya müşteriye göre arama yapma.
-   Zaman harcadığınız bir kategori ve etkinlik belirtme.
-   Saati proje için faturalandırılabilir veya faturalandırılamayan olarak kaydetme.
-   İsteğe bağlı olarak saatler için harici veya dahili yorumlar girme.

## <a name="prerequisites"></a>Ön koşullar
Kuruluşunuz için dağıtılan Microsoft Dynamics 365 sürümüne bağlı olarak ön koşullar farklılık gösterir.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Dynamics 365 Finance kullananlar için ön koşullar
Finans kuruluşunuz için dağıtılmışsa, sistem yöneticisinin **Project time entry** mobil çalışma alanını yayımlaması gerekir. Yönergeler için bkz. [Mobil çalışma alanı yayınlama](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Platform Güncelleştirme 3 veya daha sonrasını içeren 1611 sürümünü kullananlar için ön koşullar
Kuruluşunuz için Platform güncelleştirmesi 3 veya daha sonraki bir sürümü bulunan 1611 sürümü dağıtılmışsa, sistem yöneticisi aşağıdaki ön koşulları tamamlamalıdır. 

<table>
<thead>
<tr class="header">
<th>Önkoşul</th>
<th>Rol</th>
<th>Açıklama</th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td>KB 4018050 uygulayın.</td>
<td>Sistem yöneticisi</td>
<td>KB 4018050, <strong>Project time entry</strong> mobil çalışma alanını içeren bir X + + güncelleştirmesi veya meta veri düzeltmesidir. KB 4018050 uygulamak için, sistem yöneticinizin aşağıdaki adımları izlemesi gerekir.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Microsoft Dynamics Lifecycle Services'ten (LCS) meta veri düzeltmesini indirin</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Meta veri düzeltmesini yükleyin</a>.</li>
<li><strong>ApplicationSuite</strong> ve <strong>ProjectMobile</strong> modellerini içeren <a href="../../dev-itpro/deployment/create-apply-deployable-package.md">dağıtılabilir bir paket oluşturun</a> ve ardından dağıtılabilir paketi LCS'ye yükleyin.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Dağıtılabilir paketi uygulayın</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td><strong>Project time entry</strong> mobil çalışma alanını yayımlayın.</td>
<td>Sistem yöneticisi</td>
<td>Bkz. <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Mobil çalışma alanı yayınlama</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Mobil uygulamayı indirme ve yükleme

Finance and Operations mobil uygulamasını indirip ve yükleyin:

-   [Android telefonlar için](https://go.microsoft.com/fwlink/?linkid=850662)
-   [iPhone'lar için](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Mobil uygulamada oturum açma
1.  Mobil cihazınızda uygulamayı açın.
2.  Dynamics 365 URL'sini girin.
3.  İlk kez oturum açtığınızda kullanıcı adınızı ve parolanızı girmeniz istenir. Kimlik bilgilerinizi girin.
4.  Oturum açtıktan sonra, şirketiniz için kullanılabilir olan çalışma alanları gösterilir. Sistem yöneticisi daha sonra yeni bir çalışma alanı yayımladığında, mobil çalışma alanları listesini yenilemeniz gerektiğini unutmayın.

[![Çekerek yenileme](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Project time entry mobil çalışma alanını kullanarak zaman girme
1.  Mobil cihazınızdan **Project time entry** çalışma alanını seçin.
2.  **Time Entry** bölümünü seçin. Geçerli haftanın takvim tarihleri gösterilir.
3.  Seçili bir tarih için, **Eylemler** &gt; **Yeni giriş** seçeneğini belirleyin.
4.  Kaydedilecek saat sayısını girin.
5.  Zaman girişi için projeyi seçin. Listede çevrimdışı kullanım için uygulamanıza yüklenen projeler gösterilir. Varsayılan olarak, 50 öğe yüklenir, ancak geliştirici bu sayıyı değiştirebilir. Daha fazla bilgi için bkz. [Mobil platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
6.  Projeniz listede yoksa, **Ara** seçeneğini belirleyin. Ada göre arayın veya proje adına veya müşteriye göre arama yapmak için geçiş yapın.
7.  Bir kategori seçin. Listede çevrimdışı kullanım için uygulamanıza yüklenen kategoriler gösterilir. Varsayılan olarak, 50 öğe yüklenir, ancak geliştirici bu sayıyı değiştirebilir. Daha fazla bilgi için bkz. [Mobil platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
8.  Kategoriniz listede yoksa, **Ara** seçeneğini belirleyin. Kategoriye göre arayın veya kategori adına göre arama yapmak için geçiş yapın.
9.  Etkinlik seçin. Listede çevrimdışı kullanım için uygulamanıza yüklenen etkinlikler gösterilir. Varsayılan olarak, 50 öğe yüklenir, ancak geliştirici bu sayıyı değiştirebilir. Daha fazla bilgi için bkz. [Mobil platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
10. Etkinliğiniz listede yoksa, **Ara** seçeneğini belirleyin. Etkinlik numarasına göre arayın veya amaca göre aramaya geçiş yapın.

11. Satır özelliğini seçin.
12. İsteğe bağlı: Herhangi bir harici veya dahili yorum girin.
13. **Bitti**'yi seçin.
