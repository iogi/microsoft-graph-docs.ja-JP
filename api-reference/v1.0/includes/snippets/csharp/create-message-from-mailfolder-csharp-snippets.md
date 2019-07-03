---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 1f1e53b6a4e8eddc6439e9ef463f8b271daa3fba
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35471499"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var message = new Message
{
    ReceivedDateTime = "datetime-value",
    SentDateTime = "datetime-value",
    HasAttachments = true,
    Subject = "subject-value",
    Body = new ItemBody
    {
        ContentType = BodyType.Text,
        Content = "content-value"
    },
    BodyPreview = "bodyPreview-value"
};

await graphClient.Me.MailFolders["{id}"].Messages
    .Request()
    .AddAsync(message);

```