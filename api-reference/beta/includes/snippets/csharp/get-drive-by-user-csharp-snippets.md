---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 12d9a5707e6c6c23d76417f6f9dfc0e278a786b0
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35504512"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var drive = await graphClient.Users["{idOrUserPrincipalName}"].Drive
    .Request()
    .GetAsync();

```