---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: a70d8a20232feeed475e8ef9a1bbc11c1b1492f9
ms.sourcegitcommit: 3f7bac952864cfa67f749d902d9897f08534c0e3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/16/2019
ms.locfileid: "35736953"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

let res = await client.api('/me/calendarView/delta')
    .header('Prefer','odata.maxpagesize=2')
    .skiptoken('R0usmci39OQxqJrxK4')
    .get();

```