---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: ec741e1211d495cab88e0e29a2f370e50eb9c882
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35526068"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var getSharePointSiteUsageSiteCounts = await graphClient.Reports.GetSharePointSiteUsageSiteCounts('D7')
    .Request()
    .GetAsync();

```