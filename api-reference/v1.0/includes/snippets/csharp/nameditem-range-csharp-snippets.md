---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 16bdbb0dd2d7ee3e5c0cc35e65e05ed00499d29b
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35495722"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Me.Drive.Items["{id}"].Workbook.Names["{name}"]
    .Range()
    .Request()
    .PostAsync();

```