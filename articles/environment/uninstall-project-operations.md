---
title: Dynamics 365 Project Operations uygulamasını kaldırma
description: "Bu makale, Dynamics 365 Project Operations'ı kaldırma hakkında bilgi sağlar:"
author: stsporen
ms.date: 11/09/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 33a505594d6db47b4f8a0c8a630a0836f424e7d5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911988"
---
# <a name="uninstall-dynamics-365-project-operations"></a>Dynamics 365 Project Operations uygulamasını kaldırma 

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Dynamics 365 Project Operations uygulamasını kaldırmak için , Yönetici rolüne sahip olmanız gerekir.

1. **Ayarlar** > **Çözümler**'e gidin.

    ![Ayarlar sayfası.](./media/uninstall-proj-ops-solutions.png)
  
2. Çözümleri aşağıdaki tabloda listelendikleri sırayla kaldırın. 

    | Adım | Çözüm adı                                    | Not                                                                                         |
    |------|----------------------------------------------------|----------------------------------------------------------------------------------------------|
    | 1 | msdyn_ProjectServiceUpgrade_managed.cab            | Bulunmazsa, bu çözümü atlayın.                                                            |
    | 2 | ProjectOperations_Anchor                           | Bulunmazsa, bu çözümü atlayın.                                                            |
    | 3 | Dynamics365ProjectOperationsDualWriteEntityMaps    | Bulunmazsa, bu çözümü atlayın.                                                            |
    | 4 | Dynamics365ProjectOperationsDualWrite              | Bulunmazsa, bu çözümü atlayın.                                                            |
    | 5 | ProjectService                                     | Ek notlar yok.                                                                         |
    | 6 | ProjectServiceCore_Patch                           | Ek notlar yok.                                                                         |
    | 7 | ProjectServiceCore                                 | Ek notlar yok.                                                                         |
    | 8 | ProjectServiceDeprecatedComponents                 | Bulunmazsa, bu çözümü atlayın.                                                            |
    | 9 | FieldServiceCommon                                 | Dynamics 365 Finance veya Dynamics 365 Supply Chain Management ile çift yazma gereklidir.   |
    | 10 | msdyn_AssetCommon                                  | Dynamics 365 Finance veya Dynamics 365 Supply Chain Management ile çift yazma gereklidir.   |
    | 11 | msdyn_TESA_Anchor                                  | Dynamics 365 Field Service için gereklidir.                                                     |
    | 12 | msdyn_TESA_Patch                                   | Dynamics 365 Field Service için gereklidir.                                                     |
    | 13 | msdyn_TESA                                         | Dynamics 365 Field Service için gereklidir.                                                     |
    | 14 | ResourceSchedulingControls                         | Dynamics 365 Field Service için gereklidir.                                                     |
    | 15 | MicrosoftDynamicsScheduling3_CumulativePatch       | Dynamics 365 Field Service için gereklidir.                                                     |
    | 16 | MicrosoftDynamicsScheduling_Patch_xx               | Dynamics 365 Field Service için gereklidir.                                                     |
    | 17 | MicrosoftDynamicsScheduling                        | Dynamics 365 Field Service için gereklidir.                                                     |
    | 18 | Dynamics365FinanceAndOperationsAnchor              | Bulunmazsa, bu çözümü atlayın.                                                            |
    | 19 | Dynamics365Notes                                   | Bulunmazsa, bu çözümü atlayın.                                                            |
    | 20 | Dynamics365FinanceAndOperationsDualWriteEntityMaps | Bulunmazsa, bu çözümü atlayın.                                                            |
    | 21 | DualWriteCore                                      | Bulunmazsa, bu çözümü atlayın.                                                            |
    | 22 | Dynamics365AssetManagementApp                      | Bulunmazsa, bu çözümü atlayın.                                                            |
    | 23 | Dynamics365AssetManagement                         | Bulunmazsa, bu çözümü atlayın.                                                            |
    | 24 | Dynamics365SupplyChainExtended                     | Bulunmazsa, bu çözümü atlayın.                                                            |
    | 25 | Dynamics365FinanceExtended                         | Bulunmazsa, bu çözümü atlayın.                                                            |
    | 26 | HCMCommon                                          | Bulunmazsa, bu çözümü atlayın.                                                            |
    | 27 | Dynamics365FinanceAndOperationsCommon              | Bulunmazsa, bu çözümü atlayın.                                                            |
    | 28 | Taraf                                              | Bulunmazsa, bu çözümü atlayın.                                                            |
    | 29 | Dynamics365Company                                 | Bulunmazsa, bu çözümü atlayın.                                                            |
    | 30 | CurrencyExchangeRates                              | Bulunmazsa, bu çözümü atlayın.                                                            |
    | 31 | AssetCommon                                        | Bulunmazsa, bu çözümü atlayın.                                                            |
