---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: c575ccd60a5c548dee2cfca68570c74c86c4ae06
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35514108"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var me = await graphClient.Me
    .Request()
    .Select( e => new {
             e.MailboxSettings 
             })
    .GetAsync();

var mailboxSettings = me.MailboxSettings;

```