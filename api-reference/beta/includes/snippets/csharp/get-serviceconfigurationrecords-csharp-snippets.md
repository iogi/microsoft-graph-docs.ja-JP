---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: dba15723bd2de0d3b1414bbe02bfb7c837615dc8
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35486429"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var serviceConfigurationRecords = await graphClient.Domains["contoso.com"].ServiceConfigurationRecords
    .Request()
    .GetAsync();

```