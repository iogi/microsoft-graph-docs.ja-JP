---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: ed6ad941a791eebaf15154efa7602805c3b87f01
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35471670"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var groupIds = new List<String>()
{
    "groupIds-value"
};

await graphClient.Groups["{id}"]
    .CheckMemberGroups(groupIds)
    .Request()
    .PostAsync();

```