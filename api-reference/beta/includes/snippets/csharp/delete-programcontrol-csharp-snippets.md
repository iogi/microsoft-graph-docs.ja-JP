---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: dd6f968606f74e19e4ad6708b11231f8c4052244
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35526180"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.ProgramControls["7e59d237-2fb0-4e5d-b7bb-d4f9f9129213"]
    .Request()
    .DeleteAsync();

```