---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: c2f55681c11c1f854715227faecaf95a80b9210a
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35526095"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var administrativeUnit = new AdministrativeUnit
{
    DisplayName = "Seattle District Technical Schools",
    Description = "Seattle district technical schools administration",
    Visibility = "true"
};

await graphClient.AdministrativeUnits
    .Request()
    .AddAsync(administrativeUnit);

```