---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 95451e738fc7d0fc0b6d8b15dad2a29c0113ea7e
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35485882"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var workbookChartLegend = new WorkbookChartLegend
{
    Visible = true,
    Position = "position-value",
    Overlay = true
};

await graphClient.Me.Drive.Items["{id}"].Workbook.Worksheets["{id|name}"].Charts["{name}"].Legend
    .Request()
    .UpdateAsync(workbookChartLegend);

```