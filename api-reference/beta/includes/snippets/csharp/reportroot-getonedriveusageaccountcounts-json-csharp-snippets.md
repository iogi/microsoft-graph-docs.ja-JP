---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 64cdbe5dd19d706c570639e4bcfbe96d67a6633b
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35526822"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var getOneDriveUsageAccountCounts = await graphClient.Reports.GetOneDriveUsageAccountCounts('D7')
    .Request()
    .GetAsync();

```