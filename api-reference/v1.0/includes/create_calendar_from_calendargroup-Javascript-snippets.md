---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 88dace4232bad5fe7b9fc382a4b0e74d2ddaa0dc
ms.sourcegitcommit: 4fa6b745383bb0c1864b65d612d811d64cdc079f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/25/2019
ms.locfileid: "34456005"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const calendar = {
  name: "name-value",
  color: {
  }
};

let res = await client.api('/me/calendarGroups/{id}/calendars')
    .post({calendar : calendar});

```