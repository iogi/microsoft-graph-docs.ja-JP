---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 345c58fc0dc9263f0c91efbdc14dcc978451b75d
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35527563"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var inputIds = new List<String>()
{
    "{rest-formatted-id-1}",
    "{rest-formatted-id-2}"
};

var sourceIdType = ExchangeIdFormat.RestId;

var targetIdType = ExchangeIdFormat.RestImmutableEntryId;

await graphClient.Me
    .TranslateExchangeIds(inputIds,targetIdType,sourceIdType)
    .Request()
    .PostAsync();

```