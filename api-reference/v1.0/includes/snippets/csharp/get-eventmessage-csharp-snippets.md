---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 7b8464b3c30fa756ae15afa73105b517f3b05d38
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35472317"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var message = await graphClient.Me.Messages["AAMkADYAAAImV_lAAA="]
    .Request()
    .GetAsync();

```