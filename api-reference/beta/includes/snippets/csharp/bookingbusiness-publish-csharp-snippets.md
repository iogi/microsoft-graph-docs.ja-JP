---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 5669fc602f905dda8d5fda80a7efe4a5f3872aa6
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35526265"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.BookingBusinesses["Contosolunchdelivery@M365B489948.onmicrosoft.com"]
    .Publish(bookingBusiness)
    .Request()
    .PostAsync();

```