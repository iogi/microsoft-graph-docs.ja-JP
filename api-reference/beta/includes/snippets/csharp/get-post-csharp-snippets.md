---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 3d64ead973a051c5d3945e0ab5351a482b32642f
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35485305"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var post = await graphClient.Groups["0d75b8dc-c42d-44dd-890a-751a99c0589f"].Threads["AAQkAD8EJUmcWwTJi06Cew=="].Posts["AQMkADgAAAIJbQAAAA=="]
    .Request()
    .GetAsync();

```