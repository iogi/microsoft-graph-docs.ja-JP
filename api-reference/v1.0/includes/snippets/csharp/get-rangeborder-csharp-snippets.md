---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: e1c06f46014b8e1afc72fd6306a9dab8a82e62d2
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35471086"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var workbookRangeBorder = await graphClient.Me.Drive.Items["{id}"].Workbook.Names["{name}"].Range().Format.Borders["{sideIndex}"]
    .Request()
    .GetAsync();

```