---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 79a7a6b1f29e5b17131b86fcd787e60ce09b15ec
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/25/2019
ms.locfileid: "34442012"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var getMailboxUsageMailboxCounts = await graphClient.Reports.GetMailboxUsageMailboxCounts('D7')
    .Request()
    .GetAsync();

```