---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: ea6d8b793d7d381a3523a67bffc217a74cff20cd
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/25/2019
ms.locfileid: "34443300"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var chatMessage = new ChatMessage
{
    Body = new ItemBody
    {
        ContentType = BodyType.Html,
        Content = "Hello World"
    }
};

await graphClient.Teams["{id}"].Channels["{id}"].Messages["{id}"].Replies
    .Request()
    .AddAsync(chatMessage);

```