---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 1052dc2ac96b0ede0e76b023954b5de7bf2bcba0
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35526487"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var conversation = new Conversation
{
    Topic = "New head count",
    Threads = new List<ConversationThread>()
    {
        new ConversationThread
        {
            Posts = new List<Post>()
            {
                new Post
                {
                    Body = new ItemBody
                    {
                        ContentType = BodyType.Html,
                        Content = "The confirmation will come by the end of the week."
                    },
                    NewParticipants = new List<Recipient>()
                    {
                        new Recipient
                        {
                            EmailAddress = new EmailAddress
                            {
                                Name = "Adele Vance",
                                Address = "AdeleV@contoso.onmicrosoft.com"
                            }
                        }
                    }
                }
            }
        }
    }
};

await graphClient.Groups["29981b6a-0e57-42dc-94c9-cd24f5306196"].Conversations
    .Request()
    .AddAsync(conversation);

```