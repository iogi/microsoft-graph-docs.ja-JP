---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 6253573e4713824e1bcfb7e24389c42633515778
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35496041"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var id = "id-value";

var groupId = "groupId-value";

var renameAs = "renameAs-value";

await graphClient.Me.Onenote.Sections["{id}"]
    .CopyToNotebook(id,groupId,renameAs,siteCollectionId,siteId)
    .Request()
    .PostAsync();

```