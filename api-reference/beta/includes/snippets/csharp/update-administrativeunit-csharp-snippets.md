---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 2a7a517483ba57a9aa98e69fc400ea95c8dffcde
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35527216"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var administrativeUnit = new AdministrativeUnit
{
    DisplayName = "displayName-value",
    Description = "description-value",
    Visibility = "visibility-value"
};

await graphClient.AdministrativeUnits["{id}"]
    .Request()
    .UpdateAsync(administrativeUnit);

```