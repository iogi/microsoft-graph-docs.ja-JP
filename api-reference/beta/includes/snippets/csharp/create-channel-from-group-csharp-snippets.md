---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: cac770ea5ab74c855869e626b57a9828b1205ac5
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35487160"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var channel = new Channel
{
    DisplayName = "Architecture Discussion",
    Description = "This channel is where we debate all future architecture plans"
};

await graphClient.Teams["{id}"].Channels
    .Request()
    .AddAsync(channel);

```