---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 5dae900427d3e2b59152efc8d6b5cc3efe4cca5e
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35503725"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var group = await graphClient.Groups["b320ee12-b1cd-4cca-b648-a437be61c5cd"]
    .Request()
    .Select( e => new {
             e.AllowExternalSenders,
             e.AutoSubscribeNewMembers,
             e.IsSubscribedByMail,
             e.UnseenCount 
             })
    .GetAsync();

```