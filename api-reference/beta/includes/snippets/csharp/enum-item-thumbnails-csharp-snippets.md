---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 5d833b357aafbdb88eb518f16c68109b4774f9ad
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35485323"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var thumbnails = await graphClient.Me.Drive.Items["{item-id}"].Thumbnails
    .Request()
    .GetAsync();

```