---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: e826eef104b1b63c40f7552f2a944e09352ac946
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/25/2019
ms.locfileid: "34440276"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var message = new Message
{
    Subject = "Did you see last night's game?",
    Importance = Importance.Low,
    Body = new ItemBody
    {
        ContentType = BodyType.Html,
        Content = "They were <b>awesome</b>!"
    },
    ToRecipients = new List<Recipient>()
    {
        new Recipient
        {
            EmailAddress = new EmailAddress
            {
                Address = "AdeleV@contoso.onmicrosoft.com"
            }
        }
    }
};

await graphClient.Me.Messages
    .Request()
    .AddAsync(message);

```