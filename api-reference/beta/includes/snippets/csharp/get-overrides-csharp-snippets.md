---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: eac21e21b84c269c7875d567c33362e2be77c26d
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35486575"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var overrides = await graphClient.Me.InferenceClassification.Overrides
    .Request()
    .GetAsync();

```