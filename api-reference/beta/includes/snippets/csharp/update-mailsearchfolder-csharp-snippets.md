---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 7a8541c506be09c6aeed64673e2bfd14642ddfa8
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35504579"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var mailFolder = new MailFolder
{
    FilterQuery = "contains(subject, 'Analytics')"
};

await graphClient.Me.MailFolders["AAMkAGVmMDEzM"]
    .Request()
    .UpdateAsync(mailFolder);

```