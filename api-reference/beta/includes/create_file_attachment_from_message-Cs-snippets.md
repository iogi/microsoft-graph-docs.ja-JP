---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 0ae5e61f0e836601728a3f2a6872276ed70cf0d7
ms.sourcegitcommit: c0df90d66cb2072848d4bb0bf730c47a601b99ce
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34546818"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var attachment = new Attachment
{
    Name = "smile",
    ContentBytes = "a0b1c76de9f7="
};

await graphClient.Me.Messages["AAMkpsDRVK"].Attachments
    .Request()
    .AddAsync(attachment);

```