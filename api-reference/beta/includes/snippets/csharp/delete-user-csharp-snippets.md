---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 259990ecc632f46d65d5cf7f96bad6ab19d18202
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35487259"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Users["ba9a3254-9f18-4209-aeb3-9e42a35b5be4"]
    .Request()
    .DeleteAsync();

```