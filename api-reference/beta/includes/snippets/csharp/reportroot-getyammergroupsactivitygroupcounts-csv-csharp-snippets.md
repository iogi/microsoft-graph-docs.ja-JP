---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 899cef16b608d38516189727631c35cb333cf476
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35486990"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var getYammerGroupsActivityGroupCounts = await graphClient.Reports.GetYammerGroupsActivityGroupCounts('D7')
    .Request()
    .GetAsync();

```