---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: eac7b203c4b6194a37202b1f709aa94416b60777
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35527105"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var profilePhoto = await graphClient.Users["{id|userPrincipalName}"].Photo
    .Request()
    .GetAsync();

```