---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 796b1d9aef3ac56745a70da4c79945a3530a3cb0
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35526027"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var outlookTask = new OutlookTask
{
    AssignedTo = "Dana Swope",
    Subject = "Shop for children's weekend",
    StartDateTime = new DateTimeTimeZone
    {
        DateTime = "2016-05-03T09:00:00",
        TimeZone = "Eastern Standard Time"
    },
    DueDateTime = new DateTimeTimeZone
    {
        DateTime = "2016-05-05T16:00:00",
        TimeZone = "Eastern Standard Time"
    }
};

await graphClient.Me.Outlook.Tasks
    .Request()
    .Header("Prefer","outlook.timezone=\"Pacific Standard Time\"")
    .AddAsync(outlookTask);

```