---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 795a14729d85d3262edc6e7aa6a5be05aad21b4a
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35471567"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var attachment = await graphClient.Me.Messages["AAMkADA1M-zAAA="].Attachments["AAMkADA1M-CJKtzmnlcqVgqI="]
    .Request()
    .Expand("itemattachment/item")
    .GetAsync();

```