---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 1de11cfd34dfda2b8650b4e7082499c4241a3792
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35525891"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var riskyUserHistoryItem = await graphClient.RiskyUsers["41a31b00-3b3b-42d9-8f1c-6d4f14e74c69"].History["41a31b00-3b3b-42d9-8f1c-6d4f14e74c69"]
    .Request()
    .GetAsync();

```