---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: b797523f5bd8b20faaf589ecaa45892d2a227907
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35527154"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var tables = await graphClient.Me.Drive.Items["{id}"].Workbook.Tables
    .Request()
    .GetAsync();

```