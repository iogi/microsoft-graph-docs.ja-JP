---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 8e5eee0f52fdc3a57b28e08240be8321b826eab3
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35503436"
---
```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

await graphClient.BookingBusinesses["Contosolunchdelivery@M365B489948.onmicrosoft.com"].StaffMembers["5fae928f-6d2d-417a-ad96-4b0caeb362d6"]
    .Request()
    .DeleteAsync();

```