---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 500cb0fac3a06d64fbf64c68d9bff132d6a0a022
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35485279"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var educationClass = new EducationClass
{
    Description = "History - World History 1",
    DisplayName = "World History Level 1"
};

await graphClient.Education.Classes["11014"]
    .Request()
    .UpdateAsync(educationClass);

```