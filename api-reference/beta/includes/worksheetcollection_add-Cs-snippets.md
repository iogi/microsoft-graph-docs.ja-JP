---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 3a495bc94ddafdbddafd33f106c65c49410ea32d
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/25/2019
ms.locfileid: "34453132"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var name = "name-value";

await graphClient.Me.Drive.Items["{id}"].Workbook.Worksheets
    .Add(name)
    .Request()
    .PostAsync();

```