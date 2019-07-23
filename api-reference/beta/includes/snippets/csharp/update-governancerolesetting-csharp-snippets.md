---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: d6d45ece72e7986c2759d68b5c171c14a8ee2b95
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35526910"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var governanceRoleSetting = new GovernanceRoleSetting
{
    AdminEligibleSettings = new List<GovernanceRuleSetting>()
    {
        new GovernanceRuleSetting
        {
            RuleIdentifier = "ExpirationRule",
            Setting = "{\"permanentAssignment\":false,\"maximumGrantPeriodInMinutes\":129600}"
        }
    }
};

await graphClient.PrivilegedAccess["pimforazurerbac"].RoleSettings["5fb5aef8-1081-4b8e-bb16-9d5d0385bab5"]
    .Request()
    .UpdateAsync(governanceRoleSetting);

```