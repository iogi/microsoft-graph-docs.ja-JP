---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 94fcf705ef40e5070a8efcdee82e99b4d0b1c680
ms.sourcegitcommit: b18f978808fef800bff9e587464a5f3e18eb7687
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/25/2019
ms.locfileid: "35861260"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.Me.Drive.Items["{item-id}"]
    .Request()
    .DeleteAsync();

```