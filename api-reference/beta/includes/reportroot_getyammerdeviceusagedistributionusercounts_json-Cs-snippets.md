---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: a1409e2e4219de38ef33d7ebbf0a552b42390a6e
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/25/2019
ms.locfileid: "34482081"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var getYammerDeviceUsageDistributionUserCounts = await graphClient.Reports.GetYammerDeviceUsageDistributionUserCounts('D7')
    .Request()
    .GetAsync();

```