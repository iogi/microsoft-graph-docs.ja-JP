---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 4ffe7448a8c5cd1e8294f5a0cb77349837bb7e04
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/25/2019
ms.locfileid: "34445330"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var tiIndicators = await graphClient.Security.TiIndicators
    .Request()
    .GetAsync();

```