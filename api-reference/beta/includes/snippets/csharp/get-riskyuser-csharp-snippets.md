---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 47f2b50071233c6716aee67ccd246e8f022adab4
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35525894"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var riskyUser = await graphClient.RiskyUsers["c2b6c2b9-dddc-acd0-2b39-d519d803dbc3"]
    .Request()
    .GetAsync();

```