---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 991fc7fdb44c0af9bd4567da5e09e55983deb958
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35513461"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var storageLocation = "storageLocation-value";

await graphClient.Users["{id}"]
    .ExportPersonalData(storageLocation)
    .Request()
    .PostAsync();

```